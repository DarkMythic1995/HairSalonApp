# HairSalonApp

A .NET MAUI application for booking hair salon appointments, integrated with an ASP.NET Core API for email notifications and SQLite for local storage.

### Prerequisites

- .NET 9.0 SDK
- Visual Studio 2022 (17.12 or later) with .NET MAUI workload
- Docker Desktop (for running the companion API)

### Setup

1. Clone or download the repository from GitHub.
2. Open `HairSalonApp.sln` in Visual Studio.
3. Restore NuGet packages (e.g., `sqlite-net-pcl` v1.9.172, `CommunityToolkit.Mvvm`).
4. Ensure `logo.png` is in `Resources/Images` and fonts (`GreatVibes-Regular.ttf`, `OpenSans-Regular.ttf`, `OpenSans-Semibold.ttf`) are in `Resources/Fonts`.
5. Run the companion ASP.NET Core API (`hairsalonapp-api`) on `http://localhost:8080` ([see [hairsalonapp-api repository](https://github.com/DarkMythic1995/hairsalonapp-api).
6. Build and run on Windows Machine (Debug | Any CPU).

### Features

- **Appointment Booking**: Book appointments with real-time validation for customer name, date, time, service, stylist, contact info, and client status.
- **Local Storage**: Save appointments to SQLite database (`HairSalonApp.db3`).
- **Email Notifications**: Send appointment details to `blueskiessalon@gmail.com` via API.
- **UI Design**: Custom color scheme (background: `#f4f4f4`, buttons: `#cad4c6`, text: `#74746f`) with `GreatVibes` cursive font for labels and a logo for branding.

### Project Structure

- `MainPage.xaml`: Home page with navigation to book appointments.
- `AppointmentPage.xaml`: Form for booking appointments with validation.
- `ViewModels/`: MVVM view models (`MainViewModel.cs`, `AppointmentViewModel.cs`).
- `Models/`: Data models (`Appointment.cs`, `Service.cs`).
- `Services/`: Database service (`DatabaseService.cs` for SQLite).
- `Converters/`: XAML converters for validation.
- `Resources/Images/`: Logo (`logo.png`).

### Notes

- The companion `hairsalonapp-api` repository must be running for email functionality.
- Android emulator support requires cleartext HTTP configuration (not included in this release).
- SQLite database is generated at `C:\Users\<your-username>\AppData\Local\HairSalonApp.db3` on Windows.
- Replace `logo.png` with your salon’s logo for custom branding.

### License

[MIT License]
