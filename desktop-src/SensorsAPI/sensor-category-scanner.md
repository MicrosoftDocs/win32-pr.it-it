---
description: La categoria SENSOR \_ CATEGORY SCANNER contiene sensori che forniscono informazioni \_ ottenute dall'analisi.
ms.assetid: 98a772c9-2a21-489f-ad8d-3b772b7ff892
title: SENSOR_CATEGORY_SCANNER (Sensors.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59af4dbcd4ce4687a7fe2853384b4b19287cd95a0dd2033e7af031d2289f3d87
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126591"
---
# <a name="sensor_category_scanner"></a>SCANNER \_ DI CATEGORIE DI \_ SENSORI

La categoria SENSOR \_ CATEGORY SCANNER contiene sensori che forniscono informazioni \_ ottenute dall'analisi.

**Tipi di sensori definiti dalla piattaforma**

Questa categoria include i tipi di sensori definiti dalla piattaforma seguenti.



| Tipo di sensore                                                                                                                                                                                                                                                                                           | Descrizione                                                     |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------|
| <span id="SENSOR_TYPE_BARCODE_SCANNER"></span><span id="sensor_type_barcode_scanner"></span><dl> <dt>**SENSORE \_ TYPE \_ BARCODE \_ SCANNER**</dt> <dt>{990B3D8F-85BB-45FF-914D-998C04F372DF}</dt> </dl> | Sensori che usano la scansione ottico per leggere i codici a barre.<br/> |
| <span id="SENSOR_TYPE_RFID_SCANNER"></span><span id="sensor_type_rfid_scanner"></span><dl> <dt>**SENSORE \_ TYPE \_ RFID \_ SCANNER**</dt> <dt>{44328EF5-02DD-4E8D-AD5D-9249832B2ECA}</dt> </dl>          | Sensori di analisi id radiofrequenza.<br/>                 |



**Campi dati definiti dalla piattaforma**

Le chiavi di proprietà definite dalla piattaforma per questa categoria si basano sul GUID DELLO SCANNER SENSOR \_ DATA \_ \_ \_ TYPE:

{D7A59A3C-3421-44AB-8D3A-9DE8AB6C4CAE}

Questa categoria include i campi dati definiti dalla piattaforma seguenti.



| Nome del campo dati e PID                                                                                                                                                                                                                                                                     | Descrizione                                                            |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_RFID_TAG_40_BIT"></span><span id="sensor_data_type_rfid_tag_40_bit"></span><dl> <dt>**SENSORE \_ DATA \_ TYPE \_ RFID TAG \_ \_ 40 \_ BIT**</dt> <dt>(PID = 2)</dt> </dl> | **Interfaccia utente \_ VT8**<br/> Valore del tag ID della frequenza radio a 40 bit.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                           |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                            |
| Intestazione<br/>                   | <dl> <dt>Sensors.h</dt> </dl> |



 

 




