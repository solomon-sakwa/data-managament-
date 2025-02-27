import matplotlib.pyplot as plt

# Data for malaria positivity rates (Year vs. Percentage)
years = [2011, 2012, 2013, 2014, 2015]
positivity_rates = [44.86, 23.01, 22.45, 21.89, 20.71]  # in percentage

# Create the line plot
plt.figure(figsize=(8, 5))
plt.plot(years, positivity_rates, marker='o', linestyle='-', color='red', linewidth=2, markersize=8)

# Adding labels and title
plt.xlabel("Year")
plt.ylabel("Malaria Positivity Rate (%)")
plt.title("Annual Malaria Positivity Rate (2011-2015)")
plt.xticks(years)  # Ensure year labels are properly placed
plt.grid(True, linestyle="--", alpha=0.6)

# Annotate the highest and lowest points
plt.annotate(f"{positivity_rates[0]}%", (years[0], positivity_rates[0]), textcoords="offset points", xytext=(-10,5), ha='center', fontsize=10, color="blue")
plt.annotate(f"{positivity_rates[-1]}%", (years[-1], positivity_rates[-1]), textcoords="offset points", xytext=(-10,-15), ha='center', fontsize=10, color="blue")

# Show the plot
plt.show()
