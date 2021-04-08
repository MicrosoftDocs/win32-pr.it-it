---
description: La \_ categoria Sensor \_ other Category contiene sensori che supportano la classe personalizzata nel driver della classe HID.
ms.assetid: 866F7BF4-15CC-4F69-9510-B5858D47C4D0
title: SENSOR_CATEGORY_OTHER (Sensors. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e26ece66ae74e873c48cd973cc447beec2dd8f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049422"
---
# <a name="sensor_category_other"></a>categoria di sensori \_ \_ altro

La \_ categoria Sensor \_ other Category contiene sensori che supportano la classe personalizzata nel driver della classe HID.

<dl> <dt>

<span id="SENSOR_TYPE_CUSTOM"></span><span id="sensor_type_custom"></span>**tipo di sensore \_ \_ personalizzato**
</dt> <dd> <dl> <dt>

{E83AF229-8640-4D18-A213-E22675EBB2C3}
</dt> <dt>



Sensore personalizzato che supporta la classe personalizzata nel driver della classe HID.


</dt> </dl> </dd> </dl>

**Campi dati definiti dalla piattaforma**

Le chiavi delle proprietà definite dalla piattaforma per questa categoria sono basate \_ sul \_ GUID personalizzato del tipo di dati del sensore \_ \_ :

{B14C764F-07CF-41E8-9D82-EBE3D0776A6F}

Questa categoria include i campi dati definiti dalla piattaforma seguenti.



| Nome del campo dati e PID                                                                                                                                                                                                                                                                                    | Descrizione                                                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_CUSTOM_USAGE"></span><span id="sensor_data_type_custom_usage"></span><dl> <dt>**Sensore \_ di \_ \_ \_ Utilizzo personalizzato del tipo di dati**</dt> <dt> (PID = 5)</dt> </dl>                          | **\_UI4 VT**<br/> Utilizzo HID che può essere utilizzato per distinguere più sensori personalizzati.<br/> |
| <span id="SENSOR_DATA_TYPE_CUSTOM_BOOLEAN_ARRAY"></span><span id="sensor_data_type_custom_boolean_array"></span><dl> <dt>**Sensore \_ di \_ \_ \_ \_ Matrice booleana personalizzata del tipo di dati**</dt> <dt> (PID = 6)</dt> </dl> | **\_UI4 VT**<br/> Matrice di valori booleani per un sensore personalizzato specificato.<br/>                  |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE1"></span><span id="sensor_data_type_custom_value1"></span><dl> <dt>**Sensore \_ di Tipo di dati \_ \_ personalizzato \_ value1**</dt> <dt> (PID = 7)</dt> </dl>                       | **VT \_ UI4 VT \| \| \_ R4**<br/> Uno dei sei valori disponibili per un sensore personalizzato specificato.<br/>       |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE2"></span><span id="sensor_data_type_custom_value2"></span><dl> <dt>**Sensore \_ di \_Tipo di \_ dati \_ value2 personalizzato**</dt> <dt> (PID = 8)</dt> </dl>                       | **VT \_ UI4 VT \| \| \_ R4**<br/> Uno dei sei valori disponibili per un sensore personalizzato specificato.<br/>       |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE3"></span><span id="sensor_data_type_custom_value3"></span><dl> <dt>**Sensore \_ di Tipo di dati \_ \_ personalizzato \_ valore3**</dt> <dt> (PID = 9)</dt> </dl>                       | **VT \_ UI4 VT \| \| \_ R4**<br/> Uno dei sei valori disponibili per un sensore personalizzato specificato.<br/>       |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE4"></span><span id="sensor_data_type_custom_value4"></span><dl> <dt>**Sensore \_ di Tipo di dati \_ \_ personalizzato \_ VALUE4**</dt> <dt> (PID = 10)</dt> </dl>                      | **VT \_ UI4 VT \| \| \_ R4**<br/> Uno dei sei valori disponibili per un sensore personalizzato specificato.<br/>       |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE5"></span><span id="sensor_data_type_custom_value5"></span><dl> <dt>**Sensore \_ di Tipo di dati \_ \_ personalizzato \_ VALUE5**</dt> <dt> (PID = 11)</dt> </dl>                      | **VT \_ UI4 VT \| \| \_ R4**<br/> Uno dei sei valori disponibili per un sensore personalizzato specificato.<br/>       |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE6"></span><span id="sensor_data_type_custom_value6"></span><dl> <dt>**Sensore \_ di Tipo di dati \_ \_ personalizzato \_ VALUE6**</dt> <dt> (PID = 12)</dt> </dl>                      | **VT \_ UI4 VT \| \| \_ R4**<br/> Uno dei sei valori disponibili per un sensore personalizzato specificato.<br/>       |



## <a name="remarks"></a>Commenti

Un sensore che supporta la classe generica nel driver della classe HID viene mappato a una delle altre categorie definite (biometrica, elettrica, ambientale e così via).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                           |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                            |
| Intestazione<br/>                   | <dl> <dt>Sensori. h</dt> </dl> |



 

 




