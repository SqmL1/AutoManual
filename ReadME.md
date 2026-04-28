# Auto Manual

Auto Manual is an Android application designed to act as a digital garage and maintenance log. It allows users to quickly import vehicle specifications via VIN decoding and keep track of specific maintenance jobs, required tools, and compatible parts.

## Features

* **Instant VIN Decoding:** Integrates with the free, public NHTSA vPIC API to automatically parse a 17-digit VIN into accurate year, make, model, and engine specifications.
* **Digital Garage:** Saves decoded vehicles to a local database and displays them in a reactive, scrollable list.
* **Vehicle Dashboard:** Custom routing to a vehicle-specific dashboard to manage maintenance jobs and view detailed specs.
* **Offline Storage:** Uses a local SQLite database to ensure the user's garage is always accessible without a network connection.

## Tech Stack & Architecture

This project is built using modern Android development practices in Java:
* **Architecture:** MVVM (Model-View-ViewModel)
* **Local Database:** Room Persistence Library (Entities, DAOs)
* **Networking:** Retrofit2 & Gson for API calls
* **Reactive UI:** LiveData & RecyclerView

## Usage Example

1. Launch the app to view the main Garage screen.
2. Enter a valid 17-digit VIN. For example, entering a standard VIN for a 2002 Lexus IS300 will instantly hit the NHTSA API and return the 3.0L 6-Cylinder engine specs.
3. Tap **Decode VIN** to fetch the data and save the vehicle to the local Room database.
4. Tap the newly generated vehicle card in the RecyclerView to navigate to that specific car's maintenance dashboard.

## Setup & Installation

1. Clone this repository.
2. Open the project in **Android Studio**.
3. Allow Gradle to sync and download the required dependencies (Room, Retrofit, Lifecycle components).
4. Run the application on an emulator or physical device. 
