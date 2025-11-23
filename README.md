# repair-phantom
# 🚴 BIKEfixers 🚴: Professional Bike Repair at Home

[cite_start]This is a Python command-line application designed to manage service bookings for **BIKEfixers**, a professional bike repair service[cite: 3]. [cite_start]It handles booking creation, viewing, searching, and deletion, with persistent data storage[cite: 4, 5, 26, 35].

## ✨ Features

* [cite_start]**Main Menu:** Provides an interactive console menu for easy navigation[cite: 42, 43].
* [cite_start]**Book a Repair:** Collects customer details (name, phone, address, date, time) and allows selection of a bike issue from a predefined list (e.g., Flat Tire, Brake Problems)[cite: 10, 15, 16].
* [cite_start]**View All Bookings:** Loads and displays every booking stored in the system[cite: 23].
* [cite_start]**View Today's Bookings:** Filters and displays only the bookings scheduled for the current date[cite: 32].
* [cite_start]**Search Booking:** Allows searching for a booking by matching the customer's **name** or **phone number**[cite: 26, 28].
* [cite_start]**Delete Booking:** Users can select a numbered booking from the list to permanently remove it from the system[cite: 35, 37].
* [cite_start]**Persistent Data:** All booking information is stored in a file named `bookings.txt`[cite: 1, 4, 5].

## 🛠️ Requirements

* Python 3.x

## 🚀 How to Run

1.  **Save the Code:** Ensure the provided Python code is saved as `bike_repair.py` (or similar) in a local directory.
2.  **Run from Terminal:** Open your terminal or command prompt, navigate to the project directory, and execute the script:

    ```bash
    python bike_repair.py
    ```

3.  [cite_start]**Use the Menu:** The application will launch into the main menu[cite: 42, 43]:

    ```
    ============================================================
                  🚴 BIKEfixers 🚴
            Professional Bike Repair at Home
    ============================================================

    MAIN MENU
    ---------
    1. Book a Repair
    2. View All Bookings
    3. View Today's Bookings
    4. Search Booking
    5. Delete Booking
    6. Exit
    ---------

    Enter your choice (1-6): 
    ```

## 💾 Data Storage

[cite_start]Booking data is stored in the **`bookings.txt`** file[cite: 1]. [cite_start]If the file does not exist, the application creates an empty one on startup[cite: 1, 2].

* **File Name:** `bookings.txt`
* [cite_start]**Format:** Each booking is saved as a single line, with fields separated by the pipe character (`|`)[cite: 6].
* **Fields Order:** Name | Phone | Address | Date (YYYY-MM-DD) | Time (HH:MM) | Issue | Details | [cite_start]Booked At Timestamp[cite: 4, 5].

---

## 💻 Code Structure Overview

[cite_start]The core logic is contained within the `BikeRepairService` class[cite: 1].

| Method | Description |
| :--- | :--- |
| `__init__` | [cite_start]Initializes the class and calls `ensure_file_exists`[cite: 1]. |
| `ensure_file_exists` | [cite_start]Checks for and creates the `bookings.txt` file if missing[cite: 1, 2]. |
| `save_booking` | [cite_start]Appends a new, pipe-delimited booking record with a current timestamp to the file[cite: 3, 5]. |
| `load_bookings` | Reads the `bookings.txt` file and returns a list of booking dictionaries[cite: 6, 7]. |
| `book_repair` | [cite_start]Guides the user through collecting booking details and confirmation[cite: 10, 20, 21]. |
| `view_bookings` | [cite_start]Displays all loaded bookings[cite: 23, 24]. |
| `view_today_bookings` | [cite_start]Filters and displays bookings matching the current date[cite: 32, 33]. |
| `search_booking` | [cite_start]Searches bookings based on name or phone number and prints matches[cite: 26, 28]. |
| `delete_booking` | [cite_start]Prompts for a booking number to delete, removes it, and rewrites the file[cite: 35, 38, 39]. |
| `run` | [cite_start]Contains the main application loop and menu logic[cite: 42, 44]. |

---

Would you like to know more about the available bike issue options, or do you have any specific code lines you'd like me to explain?
