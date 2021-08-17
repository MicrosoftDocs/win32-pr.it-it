---
description: La categoria SENSOR \_ CATEGORY BIOMETRIC contiene sensori che forniscono informazioni sugli esseri \_ umani.
ms.assetid: dfc7ad46-c13b-46d1-8854-0d93ecaac55a
title: SENSOR_CATEGORY_BIOMETRIC (Sensors.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1551a82e359d2277c8b46f227d7a72660b1419b3ba3ddfcf58bdd4ac1de5425b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118889577"
---
# <a name="sensor_category_biometric"></a>CATEGORIA DI \_ SENSORI \_ BIOMETRICA

La categoria SENSOR \_ CATEGORY BIOMETRIC contiene sensori che forniscono informazioni sugli esseri \_ umani.

**Tipi di sensori definiti dalla piattaforma**

Questa categoria include i tipi di sensori definiti dalla piattaforma seguenti.



| Tipo di sensore                                                                                                                                                                                                                                                                                           | Descrizione                                     |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------|
| <span id="SENSOR_TYPE_HUMAN_PRESENCE"></span><span id="sensor_type_human_presence"></span><dl> <dt>**SENSORE \_ DIGITARE \_ PRESENZA \_ UMANA**</dt> <dt>{C138C12B-AD52-451C-9375-87F518FF10C6}</dt> </dl>    | Sensori che rilevano la presenza umana.<br/>  |
| <span id="SENSOR_TYPE_HUMAN_PROXIMITY"></span><span id="sensor_type_human_proximity"></span><dl> <dt>**SENSORE \_ TYPE \_ HUMAN \_ PROXIMITY**</dt> <dt>{5220DAE9-3179-4430-9F90-06266D2A34DE}</dt> </dl> | Sensori che rilevano la prossimità umana.<br/> |
| <span id="SENSOR_TYPE_TOUCH"></span><span id="sensor_type_touch"></span><dl> <dt>**SENSORE \_ TYPE \_ TOUCH**</dt> <dt>{17DB3018-06C4-4F7D-81AF-9274B7599C27}</dt> </dl>                                | Sensori di tocco.<br/>                       |



**Campi dati definiti dalla piattaforma**

Le chiavi di proprietà definite dalla piattaforma per questa categoria sono basate sul GUID BIOMETRICO SENSOR \_ DATA \_ \_ \_ TYPE:

{2299288A-6D9E-4B0B-B7EC-3528F89E40AF}

Questa categoria include i campi dati definiti dalla piattaforma seguenti.



| Nome del campo dati e PID                                                                                                                                                                                                                                                                                         | Descrizione                                                                                               |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_HUMAN_PRESENCE"></span><span id="sensor_data_type_human_presence"></span><dl> <dt>**SENSORE \_ TIPO \_ DI DATI PRESENZA \_ \_ UMANA**</dt> <dt>(PID = 2)</dt> </dl>                          | **VT \_ BOOL**<br/> **TRUE** quando un essere umano usa il computer.<br/>                           |
| <span id="SENSOR_DATA_TYPE_HUMAN_PROXIMITY_METERS"></span><span id="sensor_data_type_human_proximity_meters"></span><dl> <dt>**SENSORE \_ TIPO \_ DI \_ DATI \_ CONTATORI DI PROSSIMITÀ \_ UMANA**</dt> <dt>(PID = 3)</dt> </dl> | **VT \_ R4**<br/> Distanza tra un essere umano e il computer, in metri.<br/>                    |
| <span id="SENSOR_DATA_TYPE_TOUCH_STATE"></span><span id="sensor_data_type_touch_state"></span><dl> <dt>**SENSORE \_ TIPO \_ DI DATI TOUCH \_ \_ STATE**</dt> <dt>(PID = 4)</dt> </dl>                                   | **VT \_ BOOL**<br/> **TRUE** quando il sensore tocco viene toccato; in caso contrario, **FALSE.**<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                           |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                            |
| Intestazione<br/>                   | <dl> <dt>Sensors.h</dt> </dl> |



 

 




