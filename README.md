# TDD Data Processing Task

## Objective
Create a Python script using TDD that processes customer, order, and payment data. The script should merge the data, handle inconsistencies, compute total payments, and output the result to a CSV file.

## Instructions
1. Write unit tests using `unittest` or `pytest` in `tests/test_process_data.py`.
2. Implement the data processing logic in `scripts/process_data.py` to pass the tests.
3. Your script should:
   - Merge data from `raw_customers.csv`, `raw_orders.csv`, and `raw_payments.csv`.
   - Handle cases where orders have no matching customers.
   - Compute the total payment amount for each customer.
   - Write the output to `customer_summary.csv`.

## Data
- The data files are located in the `data/` folder.
- `raw_customers.csv` contains customer information.
- `raw_orders.csv` contains order details.
- `raw_payments.csv` contains payment information.

## Acceptance Criteria
- Your script follows TDD principles (write tests first).
- The script successfully merges the data and produces the correct output.
- All tests must pass.
- Code is clean, well-documented, and properly structured.

## How to Run Tests
```bash
# Navigate to the repository's root directory
python -m unittest discover tests/

