---
description: La categoria dei sensori \_ \_ biometrici contiene sensori che forniscono informazioni sugli esseri viventi.
ms.assetid: dfc7ad46-c13b-46d1-8854-0d93ecaac55a
title: SENSOR_CATEGORY_BIOMETRIC (Sensors. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71660c7bc94037c21502c91e017a8eba369766a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128746"
---
# <a name="sensor_category_biometric"></a>\_biometria categoria \_ sensore

La categoria dei sensori \_ \_ biometrici contiene sensori che forniscono informazioni sugli esseri viventi.

**Tipi di sensore definiti dalla piattaforma**

Questa categoria include i tipi di sensore definiti dalla piattaforma seguenti.



| Tipo di sensore                                                                                                                                                                                                                                                                                           | Descrizione                                     |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------|
| <span id="SENSOR_TYPE_HUMAN_PRESENCE"></span><span id="sensor_type_human_presence"></span><dl> <dt>**Sensore \_ di Digitare \_ la \_ presenza umana**</dt> <dt>{C138C12B-AD52-451c-9375-87F518FF10C6}</dt> </dl>    | Sensori che rilevano la presenza umana.<br/>  |
| <span id="SENSOR_TYPE_HUMAN_PROXIMITY"></span><span id="sensor_type_human_proximity"></span><dl> <dt>**Sensore \_ di Digitare \_ \_ prossimità umana**</dt> <dt>{5220DAE9-3179-4430-9F90-06266D2A34DE}</dt> </dl> | Sensori che rilevano la vicinanza umana.<br/> |
| <span id="SENSOR_TYPE_TOUCH"></span><span id="sensor_type_touch"></span><dl> <dt>**Sensore \_ di Digitare \_ touch**</dt> <dt>{17DB3018-06C4-4F7D-81AF-9274B7599C27}</dt> </dl>                                | Sensori di tocco.<br/>                       |



**Campi dati definiti dalla piattaforma**

Le chiavi delle proprietà definite dalla piattaforma per questa categoria sono basate sul \_ tipo di dati Sensor \_ \_ Biometric \_ GUID:

{2299288A-6D9E-4B0B-B7EC-3528F89E40AF}

Questa categoria include i campi dati definiti dalla piattaforma seguenti.



| Nome del campo dati e PID                                                                                                                                                                                                                                                                                         | Descrizione                                                                                               |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_HUMAN_PRESENCE"></span><span id="sensor_data_type_human_presence"></span><dl> <dt>**Sensore \_ di \_ \_ \_ Presenza umana del tipo di dati**</dt> <dt>(PID = 2)</dt> </dl>                          | **\_bool VT**<br/> **True** quando un uomo utilizza il computer.<br/>                           |
| <span id="SENSOR_DATA_TYPE_HUMAN_PROXIMITY_METERS"></span><span id="sensor_data_type_human_proximity_meters"></span><dl> <dt>**Sensore \_ di Tipo di dati \_ \_ \_ \_ contatori di prossimità umana**</dt> <dt>(PID = 3)</dt> </dl> | **\_R4 VT**<br/> Distanza tra un uomo e il computer, in metri.<br/>                    |
| <span id="SENSOR_DATA_TYPE_TOUCH_STATE"></span><span id="sensor_data_type_touch_state"></span><dl> <dt>**Sensore \_ di \_ \_ \_ Stato tocco del tipo di dati**</dt> <dt>(PID = 4)</dt> </dl>                                   | **\_bool VT**<br/> **True** quando viene toccato il sensore tattile; in caso contrario, **false**.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                           |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                            |
| Intestazione<br/>                   | <dl> <dt>Sensori. h</dt> </dl> |



 

 




