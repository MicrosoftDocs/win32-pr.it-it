---
title: Costanti WINBIO_SENSOR_MODE (tipi WinBio \_ . h)
description: Impostare la modalità adattatore del sensore.
ms.assetid: fceaed5c-de59-4da7-9d7a-adeef353292f
topic_type:
- apiref
api_name:
- WINBIO_SENSOR_UNKNOWN_MODE
- WINBIO_SENSOR_BASIC_MODE
- WINBIO_SENSOR_ADVANCED_MODE
- WINBIO_SENSOR_NAVIGATION_MODE
- WINBIO_SENSOR_SLEEP_MODE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fedf419a64b3629d0cccbcb3d56de31a4adf383
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743671"
---
# <a name="winbio_sensor_mode-constants"></a>\_Costanti della \_ modalità sensore WINBIO

I valori seguenti vengono usati nella funzione [**SensorAdapterSetMode**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_set_mode_fn) per impostare la modalità adattatore del sensore.



| Costante                                                                                                                                                                                                        | Descrizione                                                                                                                                                    |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_SENSOR_UNKNOWN_MODE"></span><span id="winbio_sensor_unknown_mode"></span><dl> <dt>**\_ \_ modalità sconosciuta del sensore WINBIO \_**</dt> </dl>          | La modalità operativa non è nota.<br/>                                                                                                                    |
| <span id="WINBIO_SENSOR_BASIC_MODE"></span><span id="winbio_sensor_basic_mode"></span><dl> <dt>**\_modalità di \_ base del sensore WINBIO \_**</dt> </dl>                | Usare il sensore in modalità di base. Il sensore funge solo da dispositivo di acquisizione. Non vengono usate le funzionalità di elaborazione onboarding o di archiviazione esistenti.<br/> |
| <span id="WINBIO_SENSOR_ADVANCED_MODE"></span><span id="winbio_sensor_advanced_mode"></span><dl> <dt>**\_ \_ modalità avanzata del sensore WINBIO \_**</dt> </dl>       | Usare il sensore in modalità avanzata. Il sensore può acquisire esempi ed eseguire funzioni di archiviazione e corrispondenti.<br/>                                     |
| <span id="WINBIO_SENSOR_NAVIGATION_MODE"></span><span id="winbio_sensor_navigation_mode"></span><dl> <dt>**\_modalità di \_ navigazione del sensore WINBIO \_**</dt> </dl> | Utilizzare il sensore come pad del mouse. Questa opzione non è attualmente supportata.<br/>                                                                                 |
| <span id="WINBIO_SENSOR_SLEEP_MODE"></span><span id="winbio_sensor_sleep_mode"></span><dl> <dt>**\_ \_ modalità sospensione sensore \_ WINBIO**</dt> </dl>                | Utilizzare il sensore in modalità sospensione.<br/>                                                                                                                   |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                                    |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                                                       |
| Intestazione<br/>                   | <dl> <dt>\_Tipi WinBio. h (includere WinBio. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti dell'applicazione client](client-application-constants.md)
</dt> </dl>

 

 





