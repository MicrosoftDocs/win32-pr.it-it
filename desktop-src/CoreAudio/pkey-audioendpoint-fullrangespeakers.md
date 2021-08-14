---
description: La proprietà PKEY \_ AudioEndpoint FullRangeSpeakers specifica la maschera di configurazione del canale per gli altoparlanti a gamma completa connessi al \_ dispositivo endpoint audio.
ms.assetid: c0a54b3d-84dc-4771-8891-167ce00e2218
title: PKEY_AudioEndpoint_FullRangeSpeakers (Mmdeviceapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad27e5623189ce3ba78707377837493c1ea8dccb248d02ddd3d8e2c64570bed6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118406447"
---
# <a name="pkey_audioendpoint_fullrangespeakers"></a>PKEY \_ AudioEndpoint \_ FullRangeSpeakers

La **proprietà PKEY \_ AudioEndpoint \_ FullRangeSpeakers** specifica la maschera di configurazione del canale per gli altoparlanti a gamma completa connessi al dispositivo endpoint audio. La maschera indica la configurazione fisica degli altoparlanti a gamma completa e specifica l'assegnazione dei canali a tali altoparlanti.

Il **membro vt** della **struttura PROPVARIANT** è impostato su VT \_ UI4.

Il **membro uintVal** della **struttura PROPVARIANT** contiene una maschera di configurazione del canale di cui viene eseguito il cast al **tipo UINT**.

Un altoparlante a gamma completa è in grado di riprodurre suoni per l'intera gamma, dal basso all'acuto. In genere, gli altoparlanti più grandi sono a gamma completa, ma gli altoparlanti più piccoli sono significativamente meno in grado di riprodurre suoni bassi. In Windows Vista, il motore audio usa questa proprietà per gestire i livelli di bassi nel flusso di output audio riprodotto dal dispositivo endpoint audio.

La maschera di configurazione del canale per questa proprietà ha lo stesso formato della maschera di configurazione del canale per la [**proprietà PKEY \_ AudioEndpoint \_ PhysicalSpeakers.**](pkey-audioendpoint-physicalspeakers.md) Per altre informazioni sulle maschere di configurazione del canale, vedere quanto segue:

-   Descrizione della proprietà KSPROPERTY AUDIO CHANNEL CONFIG nella \_ \_ documentazione Windows \_ DDK.
-   Il white paper dal titolo "Supporto dei driver audio per le configurazioni degli altoparlanti home theater" nel sito [Web di Audio Device Technologies for Windows.](https://www.microsoft.com/whdc/device/audio/default.mspx)

Il sistema ottiene la maschera di configurazione del canale per la proprietà PKEY \_ AudioEndpoint \_ FullRangeSpeakers dall'utente. L'utente immette queste informazioni tramite il Windows di controllo multimediale, Mmsys.cpl. Per altre informazioni sui Mmsys.cpl, vedere la documentazione Windows DDK.

La maschera di configurazione del canale per la proprietà PKEY AudioEndpoint FullRangeSpeakers di un dispositivo endpoint audio è un subset della maschera di configurazione del canale per la proprietà \_ \_ PKEY \_ AudioEndpoint \_ PhysicalSpeakers dello stesso dispositivo.

Ad esempio, se un dispositivo endpoint audio guida un set di altoparlanti surround 5.1, la maschera di configurazione del canale per la proprietà PKEY \_ AudioEndpoint \_ PhysicalSpeakers è KSAUDIO \_ SPEAKER \_ 5POINT1. Questa maschera indica la presenza di altoparlanti front-left, front-right, front-center, side-left e side-right, oltre a un subwoofer. Se gli altoparlanti front-left e front-right sono sufficientemente grandi per produrre suoni bassi, ma gli altoparlanti front-center e laterali più piccoli non lo sono, la maschera di configurazione del canale per la proprietà PKEY \_ AudioEndpoint \_ FullRangeSpeakers è KSAUDIO SPEAKER STEREO, che indica solo gli altoparlanti \_ \_ front-left e front-right. Le maschere di configurazione del canale KSAUDIO SPEAKER 5POINT1 e KSAUDIO SPEAKER STEREO sono definite nel file di intestazione \_ \_ \_ \_ Ksmedia.h.

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
</dt> <dt>

[**Proprietà PKEY \_ AudioEndpoint \_ PhysicalSpeakers**](pkey-audioendpoint-physicalspeakers.md)
</dt> </dl>

 

 




