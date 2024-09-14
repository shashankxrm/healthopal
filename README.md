# CarePulse

CarePulse is a patient management system that allows users to register on the platform with their medical history and preferred doctor, and book appointments at a convenient date and time. The platform also includes an admin panel for doctors, where they can manage appointment requests, including scheduling or canceling appointments. Patients are notified of decisions via a messaging service.

## Features

- **User Registration**: Users can register with their personal and medical details, including a preferred doctor.
- **Appointment Booking**: Users can book appointments with a doctor of their choice at a specific date and time.
- **Admin Panel for Doctors**: Doctors can view appointment requests, cancel or reschedule appointments.
- **Messaging System**: Patients receive notifications regarding their appointment status through a messaging service.
- **Secure Admin Access**: Admin access is secured by a passkey known only to doctors and hospital staff.

## Tech Stack

- **Frontend**: [Next.js](https://nextjs.org/), [Tailwind CSS](https://tailwindcss.com/), [ShadCN](https://shadcn.dev/)
- **Backend**: [Appwrite](https://appwrite.io/)
- **Messaging**: [Twilio](https://www.twilio.com/)
- **Programming Language**: [TypeScript](https://www.typescriptlang.org/)

## Screenshots

<!-- Add project screenshots here -->
- ![Screenshot 1]()
- ![Screenshot 2]()
  
## Installation

To set up and run this project locally, follow these steps:

1. Clone the repository:
    ```bash
    git clone https://github.com/shashank/healthopal.git
    ```

2. Navigate to the project directory:
    ```bash
    cd healthopal
    ```

3. Install the dependencies:
    ```bash
    npm install
    ```

4. Set up Appwrite and Twilio:
    - Follow the official documentation for [Appwrite](https://appwrite.io/docs) and [Twilio](https://www.twilio.com/docs/usage/tutorials).
    - Add your environment variables for Appwrite and Twilio in a `.env` file.

5. Run the application:
    ```bash
    npm run dev
    ```

6. Open your browser and go to `http://localhost:3000` to use the application.

## Usage

- **Register** as a new user, providing your personal details, medical history, and preferred doctor.
- **Book an appointment** by choosing a date and time with a doctor.
- **Admin access**: Doctors can log in via the admin page (using a secure passkey) to view and manage appointment requests.
- **Messaging**: Patients receive updates via Twilio's messaging service for appointment confirmations or changes.

## Project Structure

```bash
📦app
 ┣ 📂admin
 ┃ ┗ 📜page.tsx
 ┣ 📂patients
 ┃ ┗ 📂[userId]
 ┃ ┃ ┣ 📂new-appointment
 ┃ ┃ ┃ ┣ 📂success
 ┃ ┃ ┃ ┃ ┗ 📜page.tsx
 ┃ ┃ ┃ ┗ 📜page.tsx
 ┃ ┃ ┗ 📂register
 ┃ ┃ ┃ ┗ 📜page.tsx
 ┣ 📜global-error.tsx
 ┣ 📜globals.css
 ┣ 📜layout.tsx
 ┣ 📜loading.tsx
 ┗ 📜page.tsx

📦components
 ┣ 📂forms
 ┃ ┣ 📜AppointmentForm.tsx
 ┃ ┣ 📜PatientForm.tsx
 ┃ ┗ 📜RegisterForm.tsx
 ┣ 📂table
 ┃ ┣ 📜DataTable.tsx
 ┃ ┗ 📜columns.tsx
 ┣ 📂ui
 ┃ ┣ 📜alert-dialog.tsx
 ┃ ┣ 📜button.tsx
 ┃ ┣ 📜checkbox.tsx
 ┃ ┣ 📜command.tsx
 ┃ ┣ 📜dialog.tsx
 ┃ ┣ 📜form.tsx
 ┃ ┣ 📜input-otp.tsx
 ┃ ┣ 📜input.tsx
 ┃ ┣ 📜label.tsx
 ┃ ┣ 📜popover.tsx
 ┃ ┣ 📜radio-group.tsx
 ┃ ┣ 📜select.tsx
 ┃ ┣ 📜separator.tsx
 ┃ ┣ 📜table.tsx
 ┃ ┗ 📜textarea.tsx
 ┣ 📜AppointmentModal.tsx
 ┣ 📜CustomFormField.tsx
 ┣ 📜FileUploader.tsx
 ┣ 📜PasskeyModal.tsx
 ┣ 📜StatCard.tsx
 ┣ 📜StatusBadge.tsx
 ┣ 📜SubmitButton.tsx
 ┗ 📜theme-provider.tsx

📦lib
 ┣ 📂actions
 ┃ ┣ 📜appointment.actions.ts
 ┃ ┗ 📜patient.actions.ts
 ┣ 📜appwrite.config.ts
 ┣ 📜utils.ts
 ┗ 📜validation.ts
