# APK Distribution

This repository contains APK files for our application. These APKs are separated into two distinct folders based on their intended use:

## 1. Master Folder
- **Folder Name:** `master`
- **Purpose:** This folder contains the APK files that are linked to the production environment. These APKs represent stable, fully tested versions that are automatically deployed to clients through the app.
- **Usage:** The application is configured via `appsettings.json` to automatically use the APKs from this folder in production environments.

## 2. Demo Folder
- **Folder Name:** `demo`
- **Purpose:** This folder contains the APK files that are linked to the testing environment. These APKs are connected to our testing servers and may include features or updates that are still under development.
- **Usage:** The application is configured via `appsettings.json` to automatically use the APKs from this folder in testing environments, allowing internal teams to verify new changes.
