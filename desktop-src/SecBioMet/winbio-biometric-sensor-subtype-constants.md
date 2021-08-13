---
title: WINBIO_BIOMETRIC_SENSOR_SUBTYPE costanti (Winbio \_ types.h)
description: Specificare una maschera di bit per l'onboarding delle funzionalità del sensore.
ms.assetid: ED2A26BC-AED4-4304-9A17-A9BA126B0AFC
topic_type:
- apiref
api_name:
- WINBIO_SENSOR_SUBTYPE_UNKNOWN
- WINBIO_FP_SENSOR_SUBTYPE_SWIPE
- WINBIO_FP_SENSOR_SUBTYPE_TOUCH
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08cb98e4645b3e65a5dd56d60450acbc0d949ea673afec25baba6d335217ffa0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118911034"
---
# <a name="winbio_biometric_sensor_subtype-constants"></a>Costanti \_ \_ SUBTYPE SENSORE BIOMETRICO WINBIO \_

Le costanti seguenti possono essere usate come maschera di bit per il *parametro Capabilities* della struttura [**WINBIO \_ UNIT \_ SCHEMA.**](winbio-unit-schema.md) Si riferiscono alle funzionalità del sensore di onboarding.



| Costante                                                                                                                                                                                                            | Descrizione                                        |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------|
| <span id="WINBIO_SENSOR_SUBTYPE_UNKNOWN"></span><span id="winbio_sensor_subtype_unknown"></span><dl> <dt>**SOTTOTIPO SENSORE WINBIO \_ \_ \_ SCONOSCIUTO**</dt> </dl>     | I sottotipi di sensore non sono noti.<br/>      |
| <span id="WINBIO_FP_SENSOR_SUBTYPE_SWIPE"></span><span id="winbio_fp_sensor_subtype_swipe"></span><dl> <dt>**SCORRIMENTO DEL \_ \_ \_ SOTTOTIPO DEL SENSORE FP \_ WINBIO**</dt> </dl> | Il sensore supporta gli scorrimenti delle impronte digitali.<br/> |
| <span id="WINBIO_FP_SENSOR_SUBTYPE_TOUCH"></span><span id="winbio_fp_sensor_subtype_touch"></span><dl> <dt>**TOCCO DEL SOTTOTIPO \_ DEL SENSORE FP WINBIO \_ \_ \_**</dt> </dl> | Il sensore supporta i tocchi delle dita.<br/>     |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                                    |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                                                       |
| Intestazione<br/>                   | <dl> <dt>Winbio \_ types.h (include Winbio.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti dell'applicazione client](client-application-constants.md)
</dt> <dt>

[**SCHEMA UNITÀ \_ WINBIO \_**](winbio-unit-schema.md)
</dt> </dl>

 

 





