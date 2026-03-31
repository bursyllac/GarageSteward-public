# Garage Steward

Support repository for the iOS app **Garage Steward** — the app that makes tracking your vehicle maintenance easy.

<!-- [Download on the App Store](https://apps.apple.com/us/app/garage-steward/id6760867947) -->

---

## Concepts

### Vehicles

Add your vehicles to the app and keep track of their maintenance history, fuel economy, and upcoming service needs.

### Service Log Entries

A service log entry is anything you want to track on your vehicle: a maintenance operation, an engine revision, a technical inspection, an insurance policy renewal, and more.

### Service Log Categories

Every log entry belongs to a category (Maintenance, Engine Revision, Insurance, etc.). You'll find a pre-defined list in the **Settings** page. You can use it as-is, or add and remove categories to suit your needs.

Categories can be either:

- **Non-recurrent** — one-time operations like replacing a light bulb or a ball bearing.
- **Recurrent** — operations that repeat on a schedule, like revisions, inspections, or insurance renewals.

Every recurrent category has a **dominant expiry criteria**: either **Time** or **Mileage**. This determines what information you need to provide:

- **Time-based** categories require at least an expiry date.
- **Mileage-based** categories require at least a due mileage.
- If you provide both, you'll be notified based on whichever comes first.

### Attention Items

Attention items are the app's way of telling you something needs care. They are generated per vehicle and per recurrent category. When a due mileage or expiry date is approaching, the entry becomes an Attention Item — it will appear on the **Home** screen and the **Vehicle Details** screen, and trigger notifications.
Only one Attention Item per category for every vehicle can be active at a time. When you log a new service entry for that category, the previous Attention Item is considered resolved.

If, for example, you often travel between two countries and you need to track the road tax for each country, you will need to have separate categories for each type of road tax so that the app will generate Attention Items for each of them.
Same principle apply for insurance policies: if you need to track two different insurance policies for the same vehicle, you will need to have two separate categories for them.

### Fueling Records

Track your fuel economy by logging your fuelings. For accurate tracking, each time you fuel your vehicle, add:

- The **odometer reading**
- The **trip reading** (distance driven on the fuel you added)
- The **quantity of fuel**

Only full-tank fuelings are used when calculating fuel economy.

## How Mileage Tracking Works

The app doesn't read your odometer directly. Instead, it learns your current mileage from the data you provide — fueling records, service log entries, and their odometer readings. The more consistently you log, the more accurately the app can notify you about upcoming service needs.

If you want to be even more precise, you can always update your vehicle's mileage manually using the shortcut available in the app.

## iCloud Sync

Your data syncs automatically across all your devices via iCloud. A few things to keep in mind:

- Make sure iCloud is enabled for Garage Steward in your device settings (Settings > [your name] > iCloud).
- After a fresh install or reinstall, it may take a few minutes for your data to appear.
- As a backup option, you can export and import your data via CSV files in the **Settings** menu.

## CSV Import / Export

You can export the service history log and the fueling records as CSV files. You can use the CSV files to backup your data, or to modify it easier on a computer. You can also import CSV files to add new records to the app.

**Service log**: Easiest way to make sure your CSV file is correctly formatted is to export your service log and use the exported file as a template.
The columns separator for the service log is comma (,). The first row of the CSV file must be the header row. If you want to import a service log CSV file for an existing vehicle, you need to make sure the Vehicle ID column matches the vehicle database ID in the app. You can find the Vehicle ID of a vehicle by exporting the service log.
The mandatory columns for the service log are: **Category** and **Title**. If there's no **Vehicle ID**, the app will ask you to create a new vehicle for the imported entries.
If the category you want to import doesn't match the existing ones in the app, it will be created automatically.

**Fuelings log**: In order to import fueling records you need to already have the vehicle in the app. We recommend exporting the fueling log for that vehicle and using the exported file as a template.
If the CSV file does not contain the units of measurement, the header of the CSV file must contain the following columns: **Date**, **Odometer**, **Trip**, **Quantity**, **Total price**, **Currency**, **Type**. For type, the number 1 means the fueling was a full-tank fueling.
If the CSV file contains the units of measurement, the header of the CSV file must contain the following columns: **Date**, **Odometer**, **Trip**, **Quantity**, **Total price**, **Currency**, **Type**, **Fueling ID**, **Distance unit**, **Fueling unit**.
If the CSV file does not contains the units of measurement, you will need to select them in the menu so that the app can correctly import the data.
The mandatory columns for the fueling are **Odometer**, **Trip**, **Quantity**.


## Support

If you encounter any issues, feel free to open a ticket in the [Issues](../../issues) tab.
