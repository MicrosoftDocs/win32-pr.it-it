---
description: 'Altre informazioni su: PKEY_AudioEndpoint_PhysicalSpeakers'
ms.assetid: 20049071-0a14-421e-8bc5-04af9c7117b0
title: PKEY_AudioEndpoint_PhysicalSpeakers (mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6a627ec97dc329f50cc58a15d0df516f598af86
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524081"
---
# <a name="pkey_audioendpoint_physicalspeakers"></a>PKEY \_ AudioEndpoint \_ PhysicalSpeakers

La proprietà **pkey \_ AudioEndpoint \_ PhysicalSpeakers** specifica la maschera canale-configurazione per il dispositivo dell'endpoint audio. La maschera indica la configurazione fisica di un set di altoparlanti e specifica l'assegnazione dei canali agli altoparlanti. Per ulteriori informazioni sulle maschere di Channel-Configuration, vedere gli argomenti seguenti:

1.  Descrizione della \_ proprietà di configurazione del canale audio KSPROPERTY \_ \_ nella documentazione di Windows DDK.
2.  Il white paper denominato "supporto driver audio per le configurazioni dell'altoparlante Home Theater" nel sito Web [tecnologie per dispositivi audio per Windows](https://www.microsoft.com/whdc/device/audio/default.mspx) .

Il membro **VT** della struttura **PROPVARIANT** è impostato su VT \_ UI4.

Il membro **uintVal** della struttura **PROPVARIANT** contiene una maschera di configurazione del canale di cui viene eseguito il cast nel tipo **uint**.

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
</dt> </dl>

 

 




