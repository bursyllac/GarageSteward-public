# Garage Steward

Support repository for the iOS app **Garage Steward** — the app that makes tracking your vehicle maintenance easy.

Download on the App Store: (https://apps.apple.com/us/app/garage-steward/id6760867947)

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

## Support

If you encounter any issues, feel free to open a ticket in the [Issues](../../issues) tab.
