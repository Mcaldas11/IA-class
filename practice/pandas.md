# Pandas - IA-class

## Phase 1: Data Audit

**Cleaning:**  
How many customers are missing age? Fill these values with the median age.

**Cardinality:**  
How many unique values are there in the `suporte_tecnico` column? And in the target column?

**Frequency:**  
What percentage of customers have "Canceled" the service? (Tip: use `value_counts(normalize=True)`).

---

## Phase 2: Filters and Logic

**Segmentation:**  
Create a new DataFrame called `clientes_premium` that contains only those who pay a monthly fee greater than 15.00 and have been in the service for more than 12 months.

**Removal:**  
Does the `id_cliente` column help predict user behavior? If not, remove it from the DataFrame.

---

## Phase 3: Model Preparation (Encoding)

**Manual Mapping:**  
Turn the target column into numbers: True -> 0, Canceled -> 1.

**Binary Mapping:**  
Transform the `suporte_tecnico` column into: No -> 0, Yes -> 1.

---

## Phase 4: ML Insights

**Grouping:**  
What is the average `meses_contrato` for those who canceled vs. those who are loyal?

**Correlation:**  
Is there any strong relationship between the monthly fee and the numerical target?

[Link to the dataset](https://moodle.esmad.ipp.pt/pluginfile.php/15405/mod_page/content/3/dados_streaming.csv)

---

## EXTRA

Create a new variable that helps the model understand the value of each customer. Create a column called `Total_amount`:

- Multiply the monthly fee by the number of contract months.
- Business rule: If the `Total_amount` is greater than 500, the customer is considered "VIP" (1), otherwise "Normal" (0).