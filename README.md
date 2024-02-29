# CrimeLister App

<img width="228" alt="Screenshot 2024-02-29 at 2 29 39 PM" src="https://github.com/mar19a/RecyclerViewCriminalIntent/assets/84360137/5e42b46d-025d-4cc1-a9ef-b95b75648fa0">


This repository contains the source code for the CrimeLister Android application. The app has been enhanced from the initial example used in class (example #10) to showcase advanced features of the `RecyclerView`. The application now supports two types of rows in the `RecyclerView`: a normal row and a row for more serious crimes.

## Features

- **Two Types of Rows**: The application utilizes the `RecyclerView.Adapter`'s view type feature to differentiate between normal crimes and more serious crimes that require police intervention.
- **Dynamic Row Generation**: Based on the `requiresPolice` property of the `Crime` object, the `RecyclerView` dynamically decides which type of view should be loaded.
- **Enhanced Crime Object**: A new boolean property, `requiresPolice`, has been added to the `Crime` model to support this feature.
- **Custom View Logic**: Within the `CrimeListAdapter`, the `getItemViewType(Int)` function has been implemented to return different view types based on the crime's seriousness.
- **Adaptive View Holders**: The `onCreateViewHolder(ViewGroup, Int)` function has been updated to inflate different layouts depending on the `viewType`. A new layout with a "call police" button is used for more serious crimes.

## Implementation Details

- `getItemViewType(Int)`: This function checks the `requiresPolice` property of each `Crime` object and returns an integer representing the view type (normal or serious).
- `onCreateViewHolder(ViewGroup, Int)`: Based on the viewType, this function inflates either the normal row layout or the layout for serious crimes. Each layout corresponds to a different `ViewHolder`.
- `requiresPolice` Property: Added to the `Crime` class, this boolean value determines the type of crime and subsequently, the type of row used in the list.

## Getting Started

To use this application:

1. Clone the repository to your local machine.
2. Open the project in Android Studio.
3. Run the application on your device or emulator.

## Contributing

We welcome contributions to improve this application further:

1. Fork the project to your GitHub account.
2. Create a new branch for your feature (`git checkout -b feature/AmazingFeature`).
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`).
4. Push to the branch (`git push origin feature/AmazingFeature`).
5. Open a pull request.

Thank you for your interest in contributing to the CrimeLister app!

## License

This project is licensed under the MIT License - see the LICENSE file for details.
