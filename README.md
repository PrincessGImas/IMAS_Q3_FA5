# Names of people
names = ["Me", "Lia", "Jake"]

# Steps per day for each person
steps = [
    [4500, 5200, 4800, 5000, 5300],
    [4000, 4100, 3900, 4200, 4600],
    [6000, 5800, 5900, 6100, 6200]
]

# Calculate total steps per day
total_per_day = []

# Number of days (assuming each row has the same number of days)
num_days = len(steps[0])

for day in range(num_days):
    day_total = 0
    for person in range(len(names)):
        day_total += steps[person][day]
    total_per_day.append(day_total)

# Print total steps per day
for i, total in enumerate(total_per_day):
    print(f"Day {i+1} total steps: {total}")

# Identify the most active day
max_steps = max(total_per_day)
most_active_day = total_per_day.index(max_steps) + 1
print(f"\nMost active day overall: Day {most_active_day} ({max_steps} steps)")
