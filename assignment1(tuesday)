test_cases = int(input())

for _ in range(test_cases):
    item_count, max_capacity = map(int, input().split())
    objects = []

    for _ in range(item_count):
        item_value, item_weight = map(int, input().split())
        value_density = item_value / item_weight
        objects.append((value_density, item_value, item_weight))

    # Sort by value density (descending)
    objects.sort(key=lambda x: x[0], reverse=True)

    max_value = 0.0
    remaining_capacity = max_capacity

    for density, value, weight in objects:
        if remaining_capacity == 0:
            break

        if weight <= remaining_capacity:
            max_value += value
            remaining_capacity -= weight
        else:
            max_value += density * remaining_capacity
            break

    print(f"{max_value:.6f}")


# Sample Input (paste this when running)
# 1
# 3 50
# 60 10
# 100 20
# 120 30
