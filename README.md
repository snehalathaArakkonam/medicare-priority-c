# 🏥 Hospital Management System with Patient Queue

A comprehensive **C-based Hospital Management System** featuring a **Priority Queue** for efficient patient management. This system implements all core hospital operations using linked lists, file handling, structures, and sorting algorithms.

---

## 📋 Features

### Core Concepts Implemented
| Concept | Implementation |
|---------|---------------|
| **Linked Lists** | Dynamic patient queue with real-time additions/deletions |
| **File Handling** | Binary storage for all records (patients, doctors, appointments, etc.) |
| **Structures** | Patient, Doctor, Appointment, Medicine, Bill, MedicalRecord structs |
| **Priority Queues** | Emergency (1) > Critical (2) > Normal (3) patient prioritization |
| **Sorting Algorithms** | Queue prioritization based on emergency level |

### Key Features
- ✅ Priority-based patient queue management
- ✅ Complete patient registration and tracking
- ✅ Doctor management with specialization tracking
- ✅ Appointment scheduling and management
- ✅ Medical records with diagnosis and treatment
- ✅ Medicine inventory with low-stock alerts
- ✅ Billing system with payment tracking
- ✅ Admin dashboard with real-time statistics
- ✅ Binary file storage for data persistence
- ✅ Activity logging for audit trail
- ✅ Input validation for all user inputs

---

## 📁 Project Structure
hospital_management/
├── hospital.c # Main file (900+ lines)
├── patient_queue.c # Patient queue functions (200 lines)
├── doctor_module.c # Doctor management (180 lines)
├── appointment_module.c # Appointment management (160 lines)
├── medical_module.c # Medical records (150 lines)
├── inventory_module.c # Medicine inventory (140 lines)
├── billing_module.c # Billing system (160 lines)
├── admin_module.c # Admin dashboard (120 lines)
├── patients.dat # Binary patient data
├── doctors.dat # Binary doctor data
├── appointments.dat # Binary appointment data
├── medical_records.dat # Binary medical records
├── medicines.dat # Binary inventory data
├── bills.dat # Binary billing data
├── hospital.log # Activity log file
├── README.md # This file
└── Makefile # Build automation

---

## 🚀 Installation & Setup

### Prerequisites
- **Compiler**: GCC (GNU Compiler Collection)
- **OS**: Linux, macOS, or Windows (with MinGW)
- **Memory**: 50MB+ free space

### Compilation

**Using Makefile:**
```bash
make all
```

**Manual compilation:**
```bash
gcc hospital.c -o hospital
```

**With warnings enabled:**
```bash
gcc -Wall -Wextra hospital.c -o hospital
```

### Running the Program

```bash
./hospital        # Linux/macOS
hospital.exe      # Windows
```

---

## 📖 Usage Guide

### Main Menu
========================================
HOSPITAL MANAGEMENT SYSTEM
Patient Queue with Priority
========================================

Patient Management

Doctor Management

Appointment Management

Medical Records

Inventory Management

Billing System

Admin Dashboard

Exit

---

## 📊 Module Functions Summary

### Module 1: Patient Management (200 lines)
- `registerPatient()` - Register new patient
- `displayAllPatients()` - Show all patients
- `searchPatient()` - Search by ID/name/disease
- `updatePatient()` - Modify patient details
- `deletePatient()` - Remove patient record
- `addToQueue()` - Add patient to priority queue
- `removeFromQueue()` - Remove patient from queue
- `displayQueue()` - Show all queues
- `getNextPatient()` - Get next patient by priority
- `queueReport()` - Queue statistics

### Module 2: Doctor Management (180 lines)
- `addDoctor()` - Add new doctor
- `displayAllDoctors()` - Show all doctors
- `searchDoctor()` - Search by ID/specialization
- `updateDoctor()` - Modify doctor details
- `deleteDoctor()` - Remove doctor
- `assignPatient()` - Assign patient to doctor
- `doctorSchedule()` - Show doctor schedule
- `doctorReport()` - Doctor statistics

### Module 3: Appointment Management (160 lines)
- `createAppointment()` - Create new appointment
- `displayAppointments()` - Show all appointments
- `searchAppointment()` - Search by patient/doctor
- `cancelAppointment()` - Cancel appointment
- `updateAppointment()` - Modify appointment
- `doctorAppointments()` - Get doctor's appointments
- `patientAppointments()` - Get patient's appointments
- `appointmentReport()` - Appointment statistics

### Module 4: Medical Records (150 lines)
- `addRecord()` - Add medical record
- `displayRecords()` - Show all records
- `searchRecord()` - Search by patientID
- `updateRecord()` - Modify record
- `deleteRecord()` - Delete record
- `medicineList()` - Show medicine list
- `followUpReminder()` - Generate follow-up list

### Module 5: Inventory Management (140 lines)
- `addMedicine()` - Add new medicine
- `displayMedicines()` - Show all medicines
- `searchMedicine()` - Search by name/category
- `updateStock()` - Update medicine quantity
- `deleteMedicine()` - Remove medicine
- `lowStockAlert()` - Check low stock
- `expiryAlert()` - Check expiry
- `inventoryReport()` - Inventory summary

### Module 6: Billing System (160 lines)
- `generateBill()` - Create bill for patient
- `displayBills()` - Show all bills
- `searchBill()` - Search by patientID
- `payBill()` - Record payment
- `updateBill()` - Modify bill
- `deleteBill()` - Delete bill
- `pendingBills()` - Show unpaid bills
- `revenueReport()` - Total revenue

### Module 7: Admin Dashboard (120 lines)
- `totalPatients()` - Count all patients
- `totalDoctors()` - Count all doctors
- `totalAppointments()` - Count appointments
- `emergencyCount()` - Emergency queue count
- `criticalCount()` - Critical queue count
- `normalCount()` - Normal queue count
- `revenueReport()` - Total revenue
- `pendingBillsCount()` - Unpaid bills
- `averageWaitTime()` - Average waiting time
- `dashboard()` - Display all statistics

---

## 🔒 Security & Data Integrity

- ✅ **Unique ID Validation**: Patient/Doctor IDs must be unique
- ✅ **Input Validation**: All inputs validated before processing
- ✅ **Binary Storage**: Data preserved in binary format
- ✅ **Activity Logging**: All operations logged with timestamps
- ✅ **Error Handling**: File operations checked for errors
- ✅ **Memory Management**: Proper use of malloc/free

---

## ⚠️ Limitations

- ❌ No external database (file-based only)
- ❌ No GUI (console application only)
- ❌ No web connectivity
- ❌ No multi-threading
- ❌ Single-user system

---

## 🛠️ Troubleshooting

### Compilation Errors

**Problem**: `gcc: command not found`
```bash
# Linux (Ubuntu/Debian)
sudo apt-get install gcc

# macOS
sudo apt-get install gcc

# Windows
# Install MinGW from https://www.mingw-w64.org/
```

**Problem**: `undefined reference`
```bash
# Compile all source files together
gcc hospital.c patient_queue.c doctor_module.c -o hospital
```

### Runtime Errors

**Problem**: Data files not created
- Solution: Program creates files automatically on first run
- Check current directory for `.dat` files

**Problem**: Segmentation fault
- Solution: Ensure all pointers are initialized
- Check memory allocation with `malloc()`

---

## 📝 Future Enhancements

Potential improvements for version 2.0:

1. **Multi-user support** with authentication
2. **GUI interface** using GTK or similar
3. **Database integration** (MySQL/SQLite)
4. **Web interface** for remote access
5. **Email notifications** for appointments
6. **Advanced reporting** with charts/graphs
7. **Backup system** for data recovery
8. **Multi-language support**

---

## 📄 License

This project is open-source and available for educational purposes.

---

## 👨‍💻 Author

**Hospital Management System**
- Language: C
- Lines of Code: ~900+ (main file)
- Total Modules: 7
- Data Files: 6 binary + 1 log

---

## 🙏 Acknowledgments

Built with core C concepts:
- Linked Lists
- File Handling
- Structures
- Priority Queues
- Sorting Algorithms

---

## 📞 Support

For issues or questions:
1. Check the **Troubleshooting** section
2. Review **Test Cases** for examples
3. Examine `hospital.log` for activity details

---

**Happy Coding! 🏥**
