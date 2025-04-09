# Gearbox Filter Fouling Detection API

This API provides tools for managing and analyzing wind farms and wind turbines. It consists of multiple controllers, each with specific functionalities designed to streamline operations and enhance anomaly detection.

## Endpoints

### 1. Wind Turbine Controller
- **Purpose**: Lists all wind turbines within a specific wind farm.
- **Endpoint**: `/windTurbines`
- **Parameters**:
  - `parcName_prefix` (required): The ID of the wind farm to retrieve the list of turbines.

---

### 2. Parc Controller
- **Purpose**: Retrieves a list of all wind farms managed by the tool.
- **Endpoint**: `/parcs`
- **Response**: Returns a list of wind farms.

---

### 3. Admin Controller
- **Purpose**: Provides administrative operations for managing wind turbine models.
- **Endpoints**:
  - **Add a Model**: `/windTurbine`
  - **Delete a Model**: `/windTurbine/{windTurbineId}`
  - **Update a Model**: `/windTurbine/{windTurbineId}`
- **Description**: These endpoints allow the addition, deletion, or updating of a model associated with wind turbines.

---

### 4. Predict Controller
- **Purpose**: Predicts anomalies for a wind turbine based on SCADA data over a specified period.
- **Endpoint**: `/predict/{windTurbineId}`
- **Parameters**:
  - `windTurbineId ` (required): The ID of the wind turbine to analyze.
  - `data` (required): The SCADA data file for the turbine.
  - `aggregator` (required): The period for prediction (`week` or `month`).
- **Description**: This endpoint provides anomaly predictions to identify potential issues before they escalate.

---

## Usage

Each endpoint is designed to address specific needs related to wind farm and turbine management. For detailed usage instructions and parameter requirements, refer to the yaml documentation.

---

## Contact

For questions or further assistance, please contact the development team: ahmed.mabrouk@engie.com

---

Feel free to adapt or expand this file based on your project specifics and additional details. Let me know if you'd like further refinements! 😊
