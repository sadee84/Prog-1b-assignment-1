# Prog-1b-assignment-1
Practical assignment 
# MediCare Hospital Patient Admission System

A console-based, menu-driven Java application that helps administrative staff at MediCare Hospital manage patient records and hospital bed allocations for one ward of 20 beds.

**Author:** Sade Mzila
**Module:** PROG1B
**Institution:** Emeris University, Sandton Campus
**Project type:** Java Ant project (Apache NetBeans), JUnit 4

---

## Features

| Feature | What it does |
|---|---|
| Patient management | Register, search (by Patient ID), update, delete and display patients |
| Bed management | 20 beds (B01 to B20) in a 4 x 5 layout; allocate, release, view layout, available and occupied beds |
| Reports | All patients, available beds, occupied beds, total patients, total occupied beds, occupancy percentage |
| Patient categories | Enum for Inpatient, Outpatient and Emergency; `Inpatient` extends `Patient` |
| Sorting | Sort patients by surname or Patient ID (selection sort) |
| Unit testing | 19 JUnit tests |

## Programming concepts used

- Sorting arrays (selection sort) and passing arrays to methods using the `length` field
- Two-dimensional array for the ward layout and nested loops
- Enum with enum methods
- `ArrayList` class
- Inheritance, `super()` constructor calls and method overriding (`displayDetails()`)
- Information hiding (private fields with validated setters)
- Exception handling (three custom exceptions)
- Unit testing with JUnit

## Project structure

```
MediCareAdmissionSystem/
  src/hospital/
    Main.java                       Console menu
    HospitalSystem.java             Logic: patients, beds, reports, sorting
    Patient.java                    Base class
    Inpatient.java                  Subclass with ward and bed number
    PatientCategory.java            Enum
    Bed.java                        One hospital bed
    DuplicatePatientException.java  Custom exception
    PatientNotFoundException.java   Custom exception
    BedAllocationException.java     Custom exception
  test/hospital/
    HospitalSystemTest.java         JUnit tests
```

## Assumptions

- The hospital has one ward with exactly 20 beds.
- Each inpatient may occupy only one bed, and a bed holds only one inpatient at a time.
- Outpatients and Emergency patients do not require a bed.
- All information is stored in memory while the program runs.
- Patient IDs are not case-sensitive (`p001` is the same as `P001`).

## How to run

1. Install a JDK (17 or newer) and Apache NetBeans.
2. In NetBeans, choose **File > Open Project** and select the `MediCareAdmissionSystem` folder.
3. Right-click the project and choose **Clean and Build**, then **Run**.
4. The main class is `hospital.Main`.

## How to run the unit tests

1. Right-click the project and choose **Test**.
2. The Test Results window should show **19 tests passed, 0 failures, 0 errors**.

If the tests fail with `NoClassDefFoundError: org/hamcrest/SelfDescribing`, open **Project Properties > Libraries > Run Tests** and make sure **JUnit 4.13** and **Hamcrest 1.3** are listed under **Classpath** (not Modulepath).

## References (IIE Harvard Anglia)

JUnit Team (n.d.) *JUnit 4*. Available at: https://junit.org/junit4/ (Accessed: 17 October 2026).

Oracle (n.d.) *Java Platform, Standard Edition API specification*. Available at: https://docs.oracle.com/en/java/javase/17/docs/api/ (Accessed: 17 October 2026).
