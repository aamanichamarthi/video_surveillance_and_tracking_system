# video_surveillance_and_tracking_system

This project is a Face Entry System that uses face recognition to track individuals. It includes a graphical user interface (GUI) for adding new users and their images, a camera feed for real-time face detection and tracking, and a separate interface to view user details and their last known location and time.

# Features
User Registration: Add new users with their name, roll number, and an image through a user-friendly GUI.

Face Recognition & Tracking: Utilize a connected camera to detect and recognize registered faces.

Location and Time Tracking: Automatically updates the last known location and time for recognized individuals in a database.

User Detail Retrieval: View a user's name, last known location, and the time they were last seen by entering their roll number.

SQLite Database: Stores user information including ID, name, location, and timestamp.

# Project Structure
gui.py: This file contains the Tkinter-based graphical user interface for adding new users to the system. It allows users to input a name and roll number, upload an image, and save this information to the database.

main.py: This script handles the core face recognition functionality. It loads encoded faces from the images/ directory, captures video from a camera, detects known faces, updates their location and time in the database, and displays the camera feed with bounding boxes and names.

Track.py: This file provides a separate GUI to query and display the details of a registered user, including their name, last known location, and the timestamp of their last detection, along with their image.

data_handling.py: This utility script interacts with the data.db SQLite database. It contains commented-out code for creating, dropping, and deleting records from the USER table, and currently, it prints all entries in the USER table.

simple_facerec.py: This module (a custom class SimpleFacerec) provides simplified face recognition functionalities, including loading encoding images and detecting known faces in a given frame.

data.db: This is the SQLite database file that stores all user information. The USER table within this database has columns for id (primary key), name, location, and time.
