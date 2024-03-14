# ticket_manager
def calculate_fare(distance):
  if distance <= 5:
    return 2.50
  elif 5 < distance <= 10:
    return 3.00
  else:
    return 3.50

def main():
  # Get the number of passengers (with error handling)
  while True:
    try:
      num_passengers = int(input())
      if num_passengers > 0:
        break
      else:
        print()
    except ValueError:
      print()

  # Initialize total fare
  total_fare = 0.0

  # Loop through each passenger
  for _ in range(num_passengers):
    # Get the distance traveled (with error handling)
    while True:
      try:
        distance = float(input())
        if distance >= 0:
        break
        else:
          print()
      except ValueError:
        print()

    # Calculate fare for this passenger
    fare = calculate_fare(distance)

    # Add fare to total
    total_fare += fare

  # Display the total fare
  print(f"{total_fare:.2f}")

if __name__ == "__main__":
  main()
