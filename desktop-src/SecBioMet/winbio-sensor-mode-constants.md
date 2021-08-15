---
title: WINBIO_SENSOR_MODE costanti (Winbio \_ types.h)
description: Impostare la modalità dell'adattatore del sensore.
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
ms.openlocfilehash: 9e8f0cb4592931629e6feec4fff4a6ac3e5986d3b199afee719dd8dae67a9580
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118909329"
---
# <a name="winbio_sensor_mode-constants"></a>Costanti \_ SENSOR \_ MODE WINBIO

I valori seguenti vengono usati nella funzione [**SensorAdapterSetMode**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_set_mode_fn) per impostare la modalità dell'adattatore del sensore.



| Costante                                                                                                                                                                                                        | Descrizione                                                                                                                                                    |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_SENSOR_UNKNOWN_MODE"></span><span id="winbio_sensor_unknown_mode"></span><dl> <dt>**MODALITÀ SCONOSCIUTA DEL SENSORE WINBIO \_ \_ \_**</dt> </dl>          | La modalità operativa non è nota.<br/>                                                                                                                    |
| <span id="WINBIO_SENSOR_BASIC_MODE"></span><span id="winbio_sensor_basic_mode"></span><dl> <dt>**MODALITÀ DI BASE DEL SENSORE WINBIO \_ \_ \_**</dt> </dl>                | Usare il sensore in modalità di base. Il sensore funge solo da dispositivo di acquisizione. Le funzionalità di elaborazione o archiviazione di onboarding esistenti non vengono usate.<br/> |
| <span id="WINBIO_SENSOR_ADVANCED_MODE"></span><span id="winbio_sensor_advanced_mode"></span><dl> <dt>**MODALITÀ AVANZATA DEL SENSORE WINBIO \_ \_ \_**</dt> </dl>       | Usare il sensore in modalità avanzata. Il sensore può acquisire campioni ed eseguire funzioni di corrispondenza e archiviazione.<br/>                                     |
| <span id="WINBIO_SENSOR_NAVIGATION_MODE"></span><span id="winbio_sensor_navigation_mode"></span><dl> <dt>**MODALITÀ DI NAVIGAZIONE DEL SENSORE WINBIO \_ \_ \_**</dt> </dl> | Usare il sensore come un blocco del mouse. Questa opzione non è attualmente supportata.<br/>                                                                                 |
| <span id="WINBIO_SENSOR_SLEEP_MODE"></span><span id="winbio_sensor_sleep_mode"></span><dl> <dt>**MODALITÀ SOSPENSIONE SENSORE WINBIO \_ \_ \_**</dt> </dl>                | Usare il sensore in modalità sospensione.<br/>                                                                                                                   |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                                    |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                                                       |
| Intestazione<br/>                   | <dl> <dt>Winbio \_ types.h (include Winbio.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti dell'applicazione client](client-application-constants.md)
</dt> </dl>

 

 





