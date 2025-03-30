# Project Description

This repository contains an analysis of IoT device telemetry data collected from three smart devices between July 12-20, 2020. The dataset includes measurements of temperature, humidity, air quality (CO, LPG, smoke), light status, and motion detection.

| Dataset | [telemetry_data.csv](https://drive.google.com/file/d/1LLvC8VJbfBYmFm22uP7gqgNPByg8GCY7/view?usp=sharing) |
|----------|------|


**Key features of this project:**
- Data cleaning and preprocessing (outlier removal, unit conversion)
- Time series visualization of temperature and humidity trends
- Distribution analysis of sensor readings
- Device-specific comparison of measurements
- Encoding of categorical variables for analysis

# Dataset Overview

- **Time period**: 2020-07-12 to 2020-07-20
- **Record count**: 385,464 measurements
- **Devices**:
  - 00:0f:00:70:91:0a (106,187 records)
  - 1c:bf:ce:15:ec:4d (101,056 records)
  - b8:27:eb:bf:9d:51 (178,221 records)
- **Measurements range**:
  - Temperature: 65.66°F to 86.36°F
  - Humidity: 46.60% to 90.70%
# Data Visualizations

## Time Series Analysis

| ![Temperature Trends](https://github.com/user-attachments/assets/853acd8b-c00b-4daf-8306-0993edca9117) | ![Humidity Trends](https://github.com/user-attachments/assets/507828fe-9e7b-4126-bbe4-a4d033e365b7) |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| *Rolling average temperature (20-point window)*                                                        | *Humidity measurements with rolling average*                                                       |

<div style="display: flex; justify-content: space-between;">
<div style="width: 48%; border: 1px solid #ddd; padding: 10px; border-radius: 5px;">



## Univariate Analysis

<table>
  <tr>
    <td align="center" width="20%">
      <img src="https://github.com/user-attachments/assets/0e67f000-d89b-4514-bf4c-69a2ad9f7d9e" width="100%">
      <br><strong>CO Distribution</strong>
      <br><em>Right-skewed (0.004-0.006 range)</em>
    </td>
    <td align="center" width="20%">
      <img src="https://github.com/user-attachments/assets/886d9bb3-83ad-422b-bf23-21a282cc4186" width="100%">
      <br><strong>Humidity</strong>
      <br><em>Bimodal patterns</em>
    </td>
    <td align="center" width="20%">
      <img src="https://github.com/user-attachments/assets/6bfb1f4f-6252-49c0-ace2-bbeff3329270" width="100%">
      <br><strong>Liquid Petroleum Gas</strong>
      <br><em>Centered at 0.007</em>
    </td>
    <td align="center" width="20%">
      <img src="https://github.com/user-attachments/assets/255c526e-ad46-4027-a0db-6ca7a93a5197" width="100%">
      <br><strong>Smoke</strong>
      <br><em>Most <0.02</em>
    </td>
    <td align="center" width="20%">
      <img src="https://github.com/user-attachments/assets/ce5e16b6-f1f4-4c2f-99dc-b545b2228221" width="100%">
      <br><strong>Log-Transformed</strong>
      <br><em>Underlying patterns</em>
    </td>
  </tr>
</table>

---

## Multivariate Analysis

<table>
  <tr>
    <td align="center" width="20%">
      <img src="https://github.com/user-attachments/assets/af0dc650-41e1-4204-98db-d8cf921e7d8c" width="100%">
      <br><strong>Environmental Correlations</strong>
      <br><em>Factor relationships</em>
    </td>
    <td align="center" width="20%">
      <img src="https://github.com/user-attachments/assets/7efac3de-abcb-4f6c-8af7-96b25fd3d016" width="100%">
      <br><strong>Device Humidity</strong>
      <br><em>Variations across sensors</em>
    </td>
    <td align="center" width="20%">
      <img src="https://github.com/user-attachments/assets/3c7f3816-83d3-43b5-a246-1224e859cccd" width="100%">
      <br><strong>CO by Device</strong>
      <br><em>Concentration patterns</em>
    </td>
    <td align="center" width="20%">
      <img src="https://github.com/user-attachments/assets/f8d35cb6-9301-4c7d-85df-b1251cbfbc4e" width="100%">
      <br><strong>Smoke by Device</strong>
      <br><em>Detection patterns</em>
    </td>
    <td align="center" width="20%">
      <img src="https://github.com/user-attachments/assets/81b00bbe-1399-46c4-8471-1f589abaec7e" width="100%">
      <br><strong>Device Temperatures</strong>
      <br><em>Calibration differences</em>
    </td>
  </tr>
</table>


# Insights

1. **Device Consistency**: While all devices show similar patterns, there are consistent offsets in measurements (especially temperature), suggesting potential calibration differences.

2. **Environmental Conditions**: The bimodal humidity distribution and device-specific patterns indicate the sensors may be monitoring different microenvironments.

3. **Air Quality**: Most gas measurements (CO, smoke) show generally good air quality with occasional higher readings.
   
4. **Temporal Patterns**: Both temperature and humidity show clear daily cycles, as expected in most environments.



