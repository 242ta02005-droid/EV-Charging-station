# EV-Charging-station
# EV Charging Station
# Python Simulation Program

print("======================================")
print("          EV CHARGING STATION")
print("======================================")

# Input
battery_capacity = float(input("Enter battery capacity (kWh): "))
current_charge = float(input("Enter current battery level (%): "))
charging_power = float(input("Enter charging power (kW): "))

# Validation
if battery_capacity <= 0 or charging_power <= 0:
    print("\n❌ Invalid input!")

elif current_charge < 0 or current_charge > 100:
    print("\n❌ Battery percentage must be between 0 and 100.")

elif current_charge == 100:
    print("\n🔋 Battery is already fully charged.")
    print("🟢 Charging not required.")

else:
    # Energy required
    energy_required = battery_capacity * (100 - current_charge) / 100

    # Charging time
    charging_time = energy_required / charging_power

    print("\n----------- CHARGING STATUS -----------")
    print("Battery Capacity :", battery_capacity, "kWh")
    print("Current Charge   :", current_charge, "%")
    print("Charging Power   :", charging_power, "kW")
    print("Energy Required  :", round(energy_required, 2), "kWh")
    print("Estimated Time   :", round(charging_time, 2), "hours")

    print("\n🟢 EV CHARGING STARTED")
    print("⚡ Power supplied to EV")
    print("🔋 Battery charging...")
