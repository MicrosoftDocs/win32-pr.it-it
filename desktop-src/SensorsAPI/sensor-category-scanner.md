---
description: La \_ categoria Sensor Category \_ scanner contiene sensori che forniscono informazioni ottenute tramite l'analisi.
ms.assetid: 98a772c9-2a21-489f-ad8d-3b772b7ff892
title: SENSOR_CATEGORY_SCANNER (Sensors. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b38fdb3358ff3ce2ae96ce901972cc6842a0d1b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966572"
---
# <a name="sensor_category_scanner"></a>\_scanner categoria \_ sensori

La \_ categoria Sensor Category \_ scanner contiene sensori che forniscono informazioni ottenute tramite l'analisi.

**Tipi di sensore definiti dalla piattaforma**

Questa categoria include i tipi di sensore definiti dalla piattaforma seguenti.



| Tipo di sensore                                                                                                                                                                                                                                                                                           | Descrizione                                                     |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------|
| <span id="SENSOR_TYPE_BARCODE_SCANNER"></span><span id="sensor_type_barcode_scanner"></span><dl> <dt>**Sensore \_ di Digitare \_ Barcode \_ scanner**</dt> <dt>{990B3D8F-85BB-45FF-914D-998C04F372DF}</dt> </dl> | Sensori che usano l'analisi ottica per leggere i codici a barre.<br/> |
| <span id="SENSOR_TYPE_RFID_SCANNER"></span><span id="sensor_type_rfid_scanner"></span><dl> <dt>**Sensore \_ di Digitare \_ RFID \_ scanner**</dt> <dt>{44328EF5-02DD-4E8D-AD5D-9249832B2ECA}</dt> </dl>          | Sensori di scansione con ID frequenza radio.<br/>                 |



**Campi dati definiti dalla piattaforma**

Le chiavi delle proprietà definite dalla piattaforma per questa categoria sono basate \_ sul \_ \_ GUID dello scanner del tipo di dati del sensore \_ :

{D7A59A3C-3421-44AB-8D3A-9DE8AB6C4CAE}

Questa categoria include i campi dati definiti dalla piattaforma seguenti.



| Nome del campo dati e PID                                                                                                                                                                                                                                                                     | Descrizione                                                            |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_RFID_TAG_40_BIT"></span><span id="sensor_data_type_rfid_tag_40_bit"></span><dl> <dt>**Sensore \_ di Tipo di dati \_ \_ \_ tag RFID \_ 40 \_ bit**</dt> <dt>(PID = 2)</dt> </dl> | **\_UI8 VT**<br/> valore del tag ID frequenza radio a 40 bit.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                           |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                            |
| Intestazione<br/>                   | <dl> <dt>Sensori. h</dt> </dl> |



 

 




