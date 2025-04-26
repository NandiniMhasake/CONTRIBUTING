# CONTRIBUTING
#!/bin/bash

# Function to calculate Simple Interest
calculate_simple_interest() {
    # Formula: Simple Interest (SI) = (Principal * Rate * Time) / 100
    principal=$1
    rate=$2
    time=$3

    simple_interest=$(echo "scale=2; ($principal * $rate * $time) / 100" | bc)

    echo "The Simple Interest is: $simple_interest"
}

# User input for principal, rate, and time
echo "Enter the principal amount:"
read principal
echo "Enter the rate of interest (in %):"
read rate
echo "Enter the time period (in years):"
read time

# Call the function with user input
calculate_simple_interest $principal $rate $time
