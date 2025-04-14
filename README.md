## 🧑‍🤝‍🧑 Java Group Assignment: **Ride Sharing System**

### 🚘 Project Name: `RideShareLite`

---

### 🧠 Objective:
In this group project, your team will build a **Ride Sharing System** in Java. You'll apply OOP principles like:
- Constructor overloading
- Static variables & methods
- Static factory methods
- Good encapsulation & code structure

> Additionally, you’ll use **GitHub collaboration best practices** – **feature branches**, **pull requests**, and one member will act as the **integration lead**, managing the final merge to the `main` branch.

---

### 👥 Team Setup:

Each team has 3–4 students.  
- Each team member must work on a **separate class or feature branch**
- One student (Team Lead) will:
  - Create the main GitHub repo
  - Create the `main` branch
  - Review and merge all feature branches via Pull Requests

---

## 🧱 Tasks & Roles:

### 🧍 Team Member 1: `Driver.java`
- Fields: `name`, `driverId`, `vehicleType`, `rating`
- Static field: `driverCount`
- Static method: `generateDriverId()`
- Constructors:
  - No-arg (sets default name/vehicle)
  - Parameterized (name + vehicle)
- Static factory method: `Driver.register(String name, String vehicleType)`

---

### 🧍 Team Member 2: `Rider.java`
- Fields: `name`, `riderId`, `location`
- Static field: `riderCount`
- Constructor: default & parameterized
- Static factory method: `Rider.create(String name, String location)`

---

### 🧍 Team Member 3: `Trip.java`
- Fields: `tripId`, `Driver`, `Rider`, `distance`, `fare`
- Static method: `calculateFare(double distance)`
- Constructor: takes all fields
- Factory method: `Trip.bookTrip(Rider rider, Driver driver, double distance)`

---

### ✅ Final Integration: `RideShareTest.java`
Team lead merges all classes and writes test code that:
- Creates drivers/riders/trips
- Displays object info
- Shows total drivers and riders
- Uses factory methods and overloaded constructors

---

## 📂 Folder Structure

```
/RideShareLite
├── /src
│   ├── Driver.java
│   ├── Rider.java
│   ├── Trip.java
│   └── RideShareTest.java
└── README.md
```

---

## 🧑‍💻 Git Collaboration Instructions

### 🧑‍💼 Team Lead – Initial Setup:

```bash
# Create the main repo on GitHub
git clone https://github.com/<your-username>/RideShareLite.git
cd RideShareLite
git checkout -b main
git push -u origin main
```

Create a shared repo link and invite team members with **Write Access**.

---

### 👤 Each Team Member – Feature Branch Workflow:

```bash
# Fork and clone the main repo (if not already cloned)
git clone https://github.com/<team-lead-username>/RideShareLite.git
cd RideShareLite

# Pull the latest changes just in case
git pull origin main

# Create your own branch
git checkout -b feature/driver-class    # change name per your task

# Add your class and commit changes
git add src/Driver.java
git commit -m "Add Driver class with constructor and static methods"
git push origin feature/driver-class
```

> 🔁 Replace `driver-class` with your task: `rider-class`, `trip-class`, etc.

---

### 🔀 Opening a Pull Request

On GitHub:
1. Go to your feature branch.
2. Click **"Compare & Pull Request"**
3. Set **base** as `main` and **compare** as your branch.
4. Add title & description, assign to **team lead** to review.

---

### 🧑‍💼 Team Lead – Merging

```bash
# Pull and checkout main
git checkout main
git pull origin main

# Merge PRs after review
git merge feature/driver-class
git push origin main
```

Repeat for all branches.

---

## 📊 Sample Output (from `RideShareTest.java`)

```java
Driver d1 = Driver.register("Alice", "Sedan");
Rider r1 = Rider.create("Bob", "Downtown");

Trip t1 = Trip.bookTrip(r1, d1, 12.5);

System.out.println(d1);
System.out.println(r1);
System.out.println(t1);

System.out.println("Total Drivers: " + Driver.getDriverCount());
System.out.println("Total Riders: " + Rider.getRiderCount());
```

---

## 📋 README.md should include:
- Project description
- How to compile and run
- Contributors
- Java concepts used
- Example output

---

## ✅ Submission Instructions
1. One team member submits the **main repo link** via GitHub Classroom.
2. Ensure `main` contains:
   - All Java files
   - A working `RideShareTest.java` demo
   - A `README.md`

---

## 🧠 Concepts Covered:
- Constructor overloading
- Static fields/methods
- Factory methods
- Git collaboration & merge flow
- Clean code & separation of concerns
