---
description: La \_ \_ categoria elettrica categoria sensori contiene sensori che forniscono informazioni sui sistemi elettrici.
ms.assetid: c4efa821-fb9f-4606-898a-5be103581f39
title: SENSOR_CATEGORY_ELECTRICAL (Sensors. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b3487b779cfefc78a541fcc72d1f2c5c5e7c0db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306354"
---
# <a name="sensor_category_electrical"></a>categoria di sensori \_ \_ elettrica

La \_ \_ categoria elettrica categoria sensori contiene sensori che forniscono informazioni sui sistemi elettrici.

**Tipi di sensore definiti dalla piattaforma**

Questa categoria include i tipi di sensore definiti dalla piattaforma seguenti.



| Tipo di sensore                                                                                                                                                                                                                                                                                              | Descrizione                             |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------|
| <span id="SENSOR_TYPE_CAPACITANCE"></span><span id="sensor_type_capacitance"></span><dl> <dt>**Sensore \_ di \_Capacità del tipo**</dt> <dt>{CA2FFB1C-2317-49C0-A0B4-B63CE63461A0}</dt> </dl>                 | Sensori di capacità.<br/>         |
| <span id="SENSOR_TYPE_CURRENT"></span><span id="sensor_type_current"></span><dl> <dt>**Sensore \_ di Digitare \_ Current**</dt> <dt>{5ADC9FCE-15A0-4BBE-A1AD-2D38A9AE831C}</dt> </dl>                             | Sensori di corrente elettrica.<br/>  |
| <span id="SENSOR_TYPE_ELECTRICAL_POWER"></span><span id="sensor_type_electrical_power"></span><dl> <dt>**Sensore \_ di Digitare \_ \_ energia elettrica**</dt> <dt>{212F10F5-14AB-4376-9A43-A7794098C2FE}</dt> </dl> | Sensori di energia elettrica.<br/>    |
| <span id="SENSOR_TYPE_FREQUENCY"></span><span id="sensor_type_frequency"></span><dl> <dt>**Sensore \_ di \_Frequenza di tipo**</dt> <dt>{8CD2CBB6-73E6-4640-A709-72AE8FB60D7F}</dt> </dl>                       | Sensore di frequenza elettrica.<br/> |
| <span id="SENSOR_TYPE_INDUCTANCE"></span><span id="sensor_type_inductance"></span><dl> <dt>**Sensore \_ di TIPO \_ induttanza**</dt> <dt>{DC1D933F-C435-4C7D-A2FE-607192A524D3}</dt> </dl>                    | Sensori di induttanza.<br/>          |
| <span id="SENSOR_TYPE_POTENTIOMETER"></span><span id="sensor_type_potentiometer"></span><dl> <dt>**Sensore \_ di DIGITARE il \_ potenziometro**</dt> <dt>{2B3681A9-CADC-45AA-A6FF-54957C8BB440}</dt> </dl>           | Potenziometri.<br/>              |
| <span id="SENSOR_TYPE_RESISTANCE"></span><span id="sensor_type_resistance"></span><dl> <dt>**Sensore \_ di \_Resistenza al tipo**</dt> <dt>{9993D2C8-C157-4A52-A7B5-195C76037231}</dt> </dl>                    | Sensori di resistenza.<br/>          |
| <span id="SENSOR_TYPE_VOLTAGE"></span><span id="sensor_type_voltage"></span><dl> <dt>**Sensore \_ di \_Tensione di tipo**</dt> <dt>{C5484637-4fb7-4953-98B8-A56D8AA1FB1E}</dt> </dl>                             | Sensori di tensione.<br/>             |



**Campi dati definiti dalla piattaforma**

Le chiavi delle proprietà definite dalla piattaforma per questa categoria sono basate \_ sul \_ GUID elettrico del tipo di dati del sensore \_ \_ :

{BBB246D1-E242-4780-A2D3-CDED84F35842}

Questa categoria include i campi dati definiti dalla piattaforma seguenti.



| Nome del campo dati e PID                                                                                                                                                                                                                                                                                                         | Descrizione                                                                                   |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_CAPACITANCE_FARAD"></span><span id="sensor_data_type_capacitance_farad"></span><dl> <dt>**Sensore \_ di Capacità del tipo di dati \_ \_ \_ farad**</dt> <dt> (PID = 4)</dt> </dl>                                | **VT \_ R8**<br/> Capacità in farad.<br/>                                       |
| <span id="SENSOR_DATA_TYPE_CURRENT_AMPS"></span><span id="sensor_data_type_current_amps"></span><dl> <dt>**Sensore \_ di \_Tipo di \_ dati \_ ampère correnti**</dt> <dt>(PID = 3)</dt> </dl>                                                | **VT \_ R8**<br/> Corrente in ampere.<br/>                                          |
| <span id="SENSOR_DATA_TYPE_ELECTRICAL_FREQUENCY_HERTZ"></span><span id="sensor_data_type_electrical_frequency_hertz"></span><dl> <dt>**Sensore \_ di \_Frequenza elettrica del tipo di dati \_ \_ \_ Hertz**</dt> <dt>(PID = 9)</dt> </dl>     | **VT \_ R8**<br/> Frequenza elettrica in Hertz.<br/>                               |
| <span id="SENSOR_DATA_TYPE_ELECTRICAL_PERCENT_OF_RANGE"></span><span id="sensor_data_type_electrical_percent_of_range"></span><dl> <dt>**Sensore \_ di \_Tipo \_ di dati \_ percentuale elettrica \_ dell' \_ intervallo**</dt> <dt>(PID = 8)</dt> </dl> | **VT \_ R8**<br/> Potenziometro letto come percentuale dell'intervallo possibile.<br/> |
| <span id="SENSOR_DATA_TYPE_ELECTRICAL_POWER_WATTS"></span><span id="sensor_data_type_electrical_power_watts"></span><dl> <dt>**Sensore \_ di Tipo di dati \_ \_ \_ alimentazione elettrica \_ watt**</dt> <dt> (PID = 7)</dt> </dl>                | **VT \_ R8**<br/> Potenza elettrica in watt.<br/>                                   |
| <span id="SENSOR_DATA_TYPE_INDUCTANCE_HENRY"></span><span id="sensor_data_type_inductance_henry"></span><dl> <dt>**Sensore \_ di Tipo di dati \_ \_ induttanza \_ Henry**</dt> <dt>(PID = 6)</dt> </dl>                                    | **VT \_ R8**<br/> Induttanza in henris.<br/>                                       |
| <span id="SENSOR_DATA_TYPE_RESISTANCE_OHMS"></span><span id="sensor_data_type_resistance_ohms"></span><dl> <dt>**Sensore \_ di Resistenza al tipo di dati \_ \_ \_ Ohm**</dt> <dt>(PID = 5)</dt> </dl>                                       | **VT \_ R8**<br/> Resistenza in ohm.<br/>                                          |
| <span id="SENSOR_DATA_TYPE_VOLTAGE_VOLTS"></span><span id="sensor_data_type_voltage_volts"></span><dl> <dt>**Sensore \_ di \_Tensione del \_ tipo \_ di dati**</dt> <dt>(PID = 2)</dt> </dl>                                             | **VT \_ R8**<br/> Potenziale elettrico in volt.<br/>                               |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                           |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                            |
| Intestazione<br/>                   | <dl> <dt>Sensori. h</dt> </dl> |



 

 




