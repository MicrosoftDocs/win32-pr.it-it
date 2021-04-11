---
description: La \_ Proprietà pkey AudioEndpoint \_ FullRangeSpeakers specifica la maschera Channel-Configuration per gli altoparlanti con intervallo completo connessi al dispositivo dell'endpoint audio.
ms.assetid: c0a54b3d-84dc-4771-8891-167ce00e2218
title: PKEY_AudioEndpoint_FullRangeSpeakers (mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0990d08e3d78eddf0fa6397e888b1e26c9f9a767
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127442"
---
# <a name="pkey_audioendpoint_fullrangespeakers"></a>PKEY \_ AudioEndpoint \_ FullRangeSpeakers

La proprietà **pkey \_ AudioEndpoint \_ FullRangeSpeakers** specifica la maschera Channel-Configuration per gli altoparlanti con intervallo completo connessi al dispositivo dell'endpoint audio. La maschera indica la configurazione fisica degli altoparlanti con intervallo completo e specifica l'assegnazione di canali a tali altoparlanti.

Il membro **VT** della struttura **PROPVARIANT** è impostato su VT \_ UI4.

Il membro **uintVal** della struttura **PROPVARIANT** contiene una maschera di configurazione del canale di cui viene eseguito il cast nel tipo **uint**.

Un altoparlante con intervallo completo è in grado di riprodurre suoni nell'intervallo completo, da bassi a acuti. In genere, gli altoparlanti più grandi sono di intervallo completo, ma gli altoparlanti più piccoli sono significativamente meno in grado di riprodurre suoni bassi. In Windows Vista, il motore audio utilizza questa proprietà per gestire i livelli bassi nel flusso di output audio che viene riprodotto dal dispositivo dell'endpoint audio.

La maschera Channel-Configuration per questa proprietà è nello stesso formato della maschera Channel-Configuration della proprietà [**pkey \_ AudioEndpoint \_ PhysicalSpeakers**](pkey-audioendpoint-physicalspeakers.md) . Per ulteriori informazioni sulle maschere di Channel-Configuration, vedere gli argomenti seguenti:

-   Descrizione della \_ proprietà di configurazione del canale audio KSPROPERTY \_ \_ nella documentazione di Windows DDK.
-   Il white paper denominato "supporto driver audio per le configurazioni dell'altoparlante Home Theater" nel sito Web [tecnologie per dispositivi audio per Windows](https://www.microsoft.com/whdc/device/audio/default.mspx) .

Il sistema ottiene la maschera di configurazione del canale per la \_ Proprietà pkey AudioEndpoint \_ FullRangeSpeakers dall'utente. L'utente immette queste informazioni tramite il pannello di controllo multimediale di Windows Mmsys.cpl. Per ulteriori informazioni su Mmsys.cpl, vedere la documentazione di Windows DDK.

La maschera Channel-Configuration per la \_ Proprietà pkey AudioEndpoint \_ FullRangeSpeakers di un dispositivo endpoint audio è un subset della maschera Channel-Configuration per la proprietà pkey \_ AudioEndpoint \_ PhysicalSpeakers dello stesso dispositivo.

Se, ad esempio, un dispositivo endpoint audio aziona un set di 5,1 altoparlanti surround, la maschera Channel-Configuration per la \_ Proprietà pkey AudioEndpoint \_ PHYSICALSPEAKERS è KSAUDIO \_ speaker \_ 5POINT1. Questa maschera indica la presenza di altoparlanti front-left, Front-Right, Front-Center, Side-Left e side-right, oltre a un subwoofer. Se gli altoparlanti front-left e front-right sono sufficientemente grandi per produrre suoni bassi, ma il lato anteriore e quello inferiore non sono disponibili, la maschera Channel-Configuration per la proprietà PKEY \_ AudioEndpoint \_ FULLRANGESPEAKERS è KSAUDIO \_ speaker \_ stereo, che indica solo gli altoparlanti front-left e front-right. Channel-Configuration Masks KSAUDIO \_ speaker \_ 5POINT1 e KSAUDIO \_ speaker \_ stereo sono definiti nel file di intestazione Ksmedia. h.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Mmdeviceapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà endpoint audio**](audio-endpoint-properties.md)
</dt> <dt>

[Proprietà audio principali](core-audio-properties.md)
</dt> <dt>

[**PKEY \_ AudioEndpoint- \_ Proprietà PhysicalSpeakers**](pkey-audioendpoint-physicalspeakers.md)
</dt> </dl>

 

 




