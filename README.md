# PYTHON-WEEK-5
File Handling 
# File Creation
try:
    with open("my_file.txt", 'w') as file:
        file.write("This is line 1\n")
        file.write("12345\n")
        file.write("Another line here\n")
        print("File created and initial content written successfully.")
except PermissionError:
    print("Permission denied. Cannot create the file.")
except Exception as e:
    print("An error occurred:", str(e))

# File Reading and Display
try:
    with open("my_file.txt", 'r') as file:
        print("Contents of my_file.txt:")
        for line in file:
            print(line.strip())
except FileNotFoundError:
    print("File not found. Cannot read the content.")
except Exception as e:
    print("An error occurred:", str(e))

# File Appending
try:
    with open("my_file.txt", 'a') as file:
        file.write("Appending line 1\n")
        file.write("98765\n")
        file.write("One more line for append\n")
        print("Content appended to my_file.txt.")
except PermissionError:
    print("Permission denied. Cannot append to the file.")
except Exception as e:
    print("An error occurred:", str(e))
