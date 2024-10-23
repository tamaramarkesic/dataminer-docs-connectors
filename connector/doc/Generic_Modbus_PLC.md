---
uid: Connector_help_Generic_Modbus_PLC
---

# Generic Modbus PLC

The **Generic Modbus PLC** connector displays an overview of all the inputs and outputs provided by an Excel file.

## About

The connector will poll all the inputs and outputs with the bus address configured for the element.

To import or export Excel files, the Microsoft.ACE.OLEDB.12.0 is necessary on the server. You can download this from the following page: <https://www.microsoft.com/en-us/download/details.aspx?id=23734>

If you want to use the export function, you need to provide an empty Excel file with or without headers. When an export is created, the tables will then be placed on the sheets of the Excel file.

### Version Info

| **Range** | **Description**                        | **DCF Integration** | **Cassandra Compliant** |
|------------------|----------------------------------------|---------------------|-------------------------|
| 1.0.0.x          | Initial version.                       | No                  | Yes                     |
| 1.0.1.x          | Major change by QA (DisplayKey).       | No                  | Yes                     |
| 1.0.2.x          | Major change: changed naming.          | No                  | Yes                     |
| 1.0.3.x          | Major change: Configuration template changed. Primary keys and Display keys for Alarm table changed.          | No                  | Yes                     |

### Product Info

| Range | Supported Firmware Version |
|------------------|-----------------------------|
| 1.0.0.x          | Any                         |
| 1.0.3.x          | Any                         |

## Installation and configuration

### Creation

#### Serial Main connection

This connector uses a serial connection and requires the following input during element creation:

SERIAL CONNECTION:

- Interface connection:

  - **IP address/host**: The polling IP of the device.
  - **IP port**: 502
  - **Bus address**: The bus address of the device. Range: *0* to *255*.

### Configuration

When you use this connector for the first time on a DMA, define **Import File Path**. If you can not find your configuration file in **File Name of the Imported Excel** dropdown, use a **Refresh Files** button, then try again. Choose the configuration file and **Import File** button.

You can use **Template.xls** and populate it with data for your element. 

## Usage

### General
On General page, you can choose which pages needs to be shown in connector. For example, if you want use element just for **Analog Input** registers, you can **hide** the rest of the registers pages. 

You can also choose **Polling Control** with two options: Poll Continuous (for fast polling of all of registers) and Poll By Timer (for this mode you can define Polling Interval).

### Import/Export

On this page, you can **import** an Excel file in order to populate the tables, so that the connector can effectively start polling the connections.

You can also **export** the tables from the element to an Excel file here.

### Alarms 

On this page you can use **Event Alarm Request** to Enable or Disable polling of alarm. **Alarm polling interval** can also be set. 

Alarms table shows the informations with Description and Unit identifier of the device alarm is retrieved from. 

### Analog Input

This page displays the **Analog** **Input** connections with the current value and all the information imported from the Excel file.

### Analog Output

This page displays the **Analog** **Output** connections with the current value and all the information from the Excel file. The current value can also be modified here.

### Digital Input

This page displays the **Digital Input** connections with the current value and all the information from the Excel file.

### Digital Output

This page displays the **Digital Output** connections with the current value and all the information from the Excel file. The current value can also be modified here.
