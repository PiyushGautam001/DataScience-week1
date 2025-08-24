def calculate_average_temperature():
    print("1. Enter temperatures manually")
    print("2. Use predefined temperatures")

    try:
        choice = int(input("Enter your choice: "))

        if choice == 1:
            num_temperatures = int(input("Enter the number of temperatures: "))
            if num_temperatures <= 0:
                print("Number of temperatures must be greater than 0.")
                return
            temperatures = []
            for i in range(num_temperatures):
                temperature = float(input(f"Enter temperature {i+1}: "))
                temperatures.append(temperature)
        elif choice == 2:
            temperatures = [25, 30, 28, 22, 35]
            print("Predefined temperatures:", temperatures)
        else:
            print("Invalid choice")
            return

        average_temperature = sum(temperatures) / len(temperatures)


