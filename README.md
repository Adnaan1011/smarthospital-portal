# Smart Hospital – Token Booking & Queue Management System

A frontend hospital management prototype built with HTML, CSS, JavaScript, and Bootstrap. It provides separate views for patients, receptionists, doctors, and administrators, with appointment booking and queue-status management.

## Features

### Patient
- Patient registration and login
- Appointment booking with doctor and department selection
- Automatically generated appointment time slots
- Prevents booking a slot already booked for the same doctor and date/time
- View upcoming appointments and appointment history
- View appointment and queue information
- Cancel appointments

### Receptionist
- View appointments and filter them by date
- Manage patient appointment statuses and queue
- Register/book appointments for walk-in patients
- View appointment, waiting, and completed counts

### Doctor
- Three separate demo doctor accounts: Dr. Rahul Sharma, Dr. Priya Reddy, and Dr. Anil Kumar
- All three doctor accounts open the shared `doctordashboard.html` page
- Each doctor sees their own profile and appointments assigned to them
- Filter appointments by date
- View the patient waiting queue
- Update consultation and completion statuses

### Administrator
- View patient and appointment statistics
- Add and remove doctors
- Add and remove departments
- Filter appointment summaries
- View daily queue reports and search records

## Technologies Used
- HTML5 – webpage structure
- CSS3 – styles and layout
- JavaScript – application logic, validation, booking, and dashboard interactions
- Bootstrap 5 – UI components and responsive layout
- Browser Local Storage – frontend data persistence
- Visual Studio Code – development editor
- Live Server – local development server

## Project Structure
```text
project intern/
├── admin.html
├── admin.css
├── appointment.html
├── dashboard.css
├── doctordashboard.html
├── login.html
├── medicalrecords.html
├── onlinedocconsult.html
├── patientdashboard.html
├── pdashboard.css
├── recept.html
├── recept.css
├── register.html
├── register.css
├── style.css
└── images/
    ├── image.png
    ├── logo.jpeg
    └── smart-hospital.gif
```

## How to Run
1. Download or clone this project and extract the project folder.
2. Open the folder in Visual Studio Code.
3. Install the **Live Server** extension if it is not already installed.
4. Open `login.html` in VS Code.
5. Right-click inside the file and select **Open with Live Server**.
6. The website will open in your browser. Use the same browser and Live Server address when testing the dashboards so they can access the same Local Storage data.

## Demo Staff Accounts
These demo staff accounts are defined in the frontend login code. The three doctors use separate credentials but share the same doctor dashboard page:

| Role | Email | Password |
|---|---|---|
| Doctor – Dr. Rahul Sharma | rahul@hospital.com | rahul123 |
| Doctor – Dr. Priya Reddy | priya@hospital.com | priya123 |
| Doctor – Dr. Anil Kumar | anil@hospital.com | anil123 |
| Receptionist | receptionist@hospital.com | receptionist123 |
| Admin | admin@hospital.com | admin123 |

Patients should register through the registration page and then sign in using their registered credentials.

## Local Storage Data
The application uses browser Local Storage for its frontend data. Common keys include:

| Key | Purpose |
|---|---|
| `hospitalPatients` | Registered patient information |
| `hospitalAppointments` | Appointment details and appointment statuses |
| `hospitalDoctors` | Doctor records used by management and booking screens |
| `hospitalDepartments` | Department records |
| `loggedInPatient` | Patient login/session information used by the frontend |
| `loggedInUser` | Staff login/session information used by the frontend |

Data is saved in the browser and is not stored in a shared server database. Use the same browser profile and origin/Live Server port while testing.

## Appointment Statuses
Appointment status values used by the frontend include:
- `CONFIRMED`
- `WAITING`
- `CALLED`
- `IN_CONSULTATION`
- `COMPLETED`
- `CANCELLED`

Status updates are stored with the appointment record and can be read by the connected dashboards.

## Mock Data
Default doctors and departments are initialized by the application where needed. Patient and appointment records are created through registration and booking flows rather than supplied as fixed sample records. See `mock-data.json` for the documented default doctor and department records, appointment status values, Local Storage keys, record formats, and demo login account details. This JSON file is documentation/reference data; the frontend does not automatically load it. The actual login credentials are validated by the JavaScript in `login.html`.


## Limitations
- Frontend prototype; no backend API or server-side database
- Local Storage data is specific to a browser profile and website origin
- Demo login credentials are hardcoded in the frontend and are not secure for production use
- No real-time multi-device synchronization
- No real SMS/email notification or payment integration
- Not intended for handling real patient health information


## Future Improvements
- Add a backend API and database (for example, Node.js or Python with MySQL)
- Implement secure server-side authentication and role permissions
- Add real-time queue updates
- Add appointment reminders through email or SMS
- Deploy the application to a secure hosting environment
- Improve accessibility and responsive behavior across devices

## Disclaimer
This project is a frontend demonstration/prototype for learning and internship presentation purposes. It is not a production hospital system and should not be used to store real patient or sensitive medical data.
