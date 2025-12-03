# Variable Dictionary

This dictionary describes all variables used in the retail sales project, including original fields from the raw datasets and the engineered features created during preprocessing.

---

## 1. Categorías (`categorias.csv`)

| Variable        | Type    | Description |
|-----------------|---------|-------------|
| **ID_Categoria** | Integer | Unique identifier of the product category. |
| **Categoría**     | String  | Name of the category (e.g., Carnes, Lácteos). |
| **Descripción**   | String  | Text description of the category. |

---

## 2. Clientes (`clientes.csv`)

| Variable           | Type   | Description |
|--------------------|--------|-------------|
| **ID_Cliente**      | Integer | Unique identifier of each customer. |
| **Nombre**          | String  | Customer’s first name. |
| **Apellido**        | String  | Customer’s last name. |
| **Email**           | String  | Customer’s email address. |
| **Fecha_Resgistro** | Date    | Registration date (converted from string). |
| **Región**          | String  | Geographic region of the customer. |

---

## 3. Métodos de Pago (`metodos_pago.csv`)

| Variable     | Type    | Description |
|--------------|---------|-------------|
| **ID_Metodo** | Integer | Unique payment method ID. |
| **Método**     | String  | Name of the payment method. |
| **Descripción** | String  | Details or notes about the payment method. |

---

## 4. Productos (`productos.csv`)

| Variable           | Type    | Description |
|--------------------|---------|-------------|
| **ID_Producto**     | Integer | Unique product ID. |
| **Nombre_producto** | String  | Product name. |
| **Categoría**        | String  | Product category (joins with Categorías table). |
| **Precio_Unitario**  | Float   | Product price (cleaned: comma → decimal). |
| **Stock**            | Integer | Units available in inventory. |

---

## 5. Ventas (`ventas.csv`)

| Variable        | Type   | Description |
|-----------------|--------|-------------|
| **ID_Venta**     | Integer | Unique sale transaction ID. |
| **Fecha**        | Date    | Transaction date (standardized to datetime). |
| **ID_Cliente**   | Integer | Customer ID for the sale. |
| **ID_Producto**  | Integer | Product ID purchased. |
| **Cantidad**     | Integer | Quantity of items sold. |
| **Método_Pago**  | Integer | Payment method used (joins with Métodos de Pago). |
| **Estado**       | String  | Transaction status (all “Completa”). |

---

# Engineered Variables (Created During Data Preprocessing)

These variables were generated during the data cleaning and transformation process.

| Variable     | Type    | Description |
|--------------|---------|-------------|
| **anio**      | Integer | Year extracted from `Fecha`. |
| **mes**       | Integer | Month extracted from `Fecha`. |
| **semana**    | Integer | ISO week number extracted from `Fecha`. |
| **ingreso**   | Float   | Revenue: `Cantidad × Precio_Unitario`. |

---

# Final Master Table

The final merged dataset (`master.parquet`) contains:

- All fields from **Ventas**
- Customer information from **Clientes**
- Product details from **Productos**
- Category information from **Categorías**
- Payment method information from **Métodos de Pago**
- Engineered variables (`anio`, `mes`, `semana`, `ingreso`)

---