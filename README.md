def calculate_average(score1, score2, score3):
    return (score1 + score2 + score3) / 3


students = int(input("How many students? "))

if students < 3:
    students = 3
    print("Minimum is 3 students.")

for i in range(students):
    print("\nStudent", i + 1)

    name = input("Enter name: ")

    activity1 = float(input("Activity 1: "))
    activity2 = float(input("Activity 2: "))
    activity3 = float(input("Activity 3: "))

    average = calculate_average(activity1, activity2, activity3)

    if average >= 90:
        status = "Excellent"
    elif average >= 80:
        status = "Very Good"
    elif average >= 75:
        status = "Passed"
    else:
        status = "Failed"

    print("\n--- Student Result ---")
    print("Name:", name)
    print("Activity 1:", activity1)
    print("Activity 2:", activity2)
    print("Activity 3:", activity3)
    print("Average:", round(average, 2))
    print("Status:", status)
