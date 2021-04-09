---
description: La \_ categoria sensore categoria \_ Light contiene sensori che forniscono informazioni sulle caratteristiche di Light.
ms.assetid: 0327bda5-f1d7-476d-9f0f-f4d60a6a106f
title: SENSOR_CATEGORY_LIGHT (Sensors. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca14bba297a8f445312873fc810e7d0b5ba13a4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878906"
---
# <a name="sensor_category_light"></a>\_categoria sensore \_ chiaro

La \_ categoria sensore categoria \_ Light contiene sensori che forniscono informazioni sulle caratteristiche di Light.

**Tipi di sensore definiti dalla piattaforma**

Questa categoria include i tipi di sensore definiti dalla piattaforma seguenti.



| Tipo di sensore                                                                                                                                                                                                                                                                                     | Descrizione                       |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------|
| <span id="SENSOR_TYPE_AMBIENT_LIGHT"></span><span id="sensor_type_ambient_light"></span><dl> <dt>**Sensore \_ di TIPO \_ \_ luce ambiente**</dt> <dt>{97F115C8-599A-4153-8894-D2D12899918A}</dt> </dl> | Sensori di luce di ambiente.<br/> |



**Campi dati definiti dalla piattaforma**

Le chiavi di proprietà definite dalla piattaforma per questa categoria sono basate \_ sul \_ tipo di dati GUID luce del sensore \_ \_ :

{E4C77CE2-DCB7-46E9-8439-4FEC548833A6}

Questa categoria include i campi dati definiti dalla piattaforma seguenti.



| Nome del campo dati e PID                                                                                                                                                                                                                                                                                                | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_LIGHT_CHROMACITY__"></span><span id="sensor_data_type_light_chromacity__"></span><dl> <dt> **Tipo di dati del sensore \_ \_ \_ Light \_ CHROMACITY**</dt> <dt>(PID = 4)</dt> </dl>                     | **VT \_ vettore \| VT \_ UI1**<br/> Cromaticità come matrice calcolata di valori float.<br/> I dati per i tipi di vettore vengono sempre serializzati come **VT \_ Ui1** (una matrice di caratteri senza segno a 1 byte). Questo campo dati contiene effettivamente ogni valore come valore reale IEEE a 4 byte (**VT \_ R4**).<br/> Per informazioni sull'utilizzo delle matrici, vedere [recupero di tipi di vettori](retrieving-vector-types.md).<br/> |
| <span id="SENSOR_DATA_TYPE_LIGHT_LEVEL_LUX"></span><span id="sensor_data_type_light_level_lux"></span><dl> <dt>**Sensore \_ di Tipo di dati \_ \_ \_ livello leggero \_ Lux**</dt> <dt> (PID = 2)</dt> </dl>                            | **\_R4 VT**<br/> Livello di illuminazione, in Lux.<br/>                                                                                                                                                                                                                                                                                                                                                              |
| <span id="SENSOR_DATA_TYPE_LIGHT_TEMPERATURE_KELVIN"></span><span id="sensor_data_type_light_temperature_kelvin"></span><dl> <dt>**Sensore \_ di \_Temperatura luce tipo di dati \_ \_ \_ Kelvin**</dt> <dt> (PID = 3)</dt> </dl> | **\_R4 VT**<br/> Temperatura del colore, in gradi Kelvin.<br/>                                                                                                                                                                                                                                                                                                                                                   |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                           |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                            |
| Intestazione<br/>                   | <dl> <dt>Sensori. h</dt> </dl> |



 

 




