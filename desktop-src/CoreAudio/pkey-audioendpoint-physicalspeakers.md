---
description: 'Altre informazioni su: PKEY_AudioEndpoint_PhysicalSpeakers'
ms.assetid: 20049071-0a14-421e-8bc5-04af9c7117b0
title: PKEY_AudioEndpoint_PhysicalSpeakers (Mmdeviceapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 358623626274a0ab3a0898e9e912e4f5f990c14d00dd6f6ef57bb4050297403f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118406417"
---
# <a name="pkey_audioendpoint_physicalspeakers"></a>PKEY \_ AudioEndpoint \_ PhysicalSpeakers

La **proprietà PKEY \_ AudioEndpoint \_ PhysicalSpeakers** specifica la maschera di configurazione del canale per il dispositivo endpoint audio. La maschera indica la configurazione fisica di un set di altoparlanti e specifica l'assegnazione dei canali agli altoparlanti. Per altre informazioni sulle maschere di configurazione del canale, vedere quanto segue:

1.  Descrizione della proprietà KSPROPERTY AUDIO CHANNEL CONFIG nella \_ \_ documentazione Windows \_ DDK.
2.  Il white paper dal titolo "Supporto dei driver audio per le configurazioni degli altoparlanti home theater" nel sito [Web di Audio Device Technologies for Windows.](https://www.microsoft.com/whdc/device/audio/default.mspx)

Il **membro vt** della **struttura PROPVARIANT** è impostato su VT \_ UI4.

Il **membro uintVal** della **struttura PROPVARIANT** contiene una maschera di configurazione del canale di cui viene eseguito il cast al **tipo UINT**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Mmdeviceapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà dell'endpoint audio**](audio-endpoint-properties.md)
</dt> <dt>

[Proprietà audio di base](core-audio-properties.md)
</dt> </dl>

 

 




