---
description: La proprietà \_ PKEY AudioEndpoint Disable SysFx specifica se gli effetti di sistema sono abilitati nel flusso in modalità condivisa che passa da o verso \_ il dispositivo endpoint \_ audio.
ms.assetid: 9e73e9b6-1864-49cb-adf8-233cc1f9bfe5
title: PKEY_AudioEndpoint_Disable_SysFx (Mmdeviceapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f8f4e5b54773cc6fcdc14ed7788a8ce6c3da2bf28666109c1404095c0c5c12a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118005230"
---
# <a name="pkey_audioendpoint_disable_sysfx"></a>PKEY \_ AudioEndpoint \_ Disable \_ SysFx

La **proprietà \_ PKEY AudioEndpoint Disable \_ \_ SysFx** specifica se gli effetti di sistema sono abilitati nel flusso in modalità condivisa che passa da o verso il dispositivo endpoint audio.

Gli effetti di sistema vengono implementati come oggetti di elaborazione audio (APO) che possono essere inseriti in un flusso audio. Gli APO sono moduli software che eseguono funzioni di elaborazione audio, ad esempio il controllo del volume e la conversione del formato. La disabilitazione degli effetti di sistema per un dispositivo endpoint consente al flusso associato di passare attraverso gli APO senza modifiche.

Per altre informazioni sugli effetti di sistema in Windows Vista, vedere i white paper intitolato "Custom Audio Effects in Windows Vista" (Effetti audio personalizzati in Windows Vista) e "Reusing Windows Vista Audio System Effects" (Riutilizzo degli effetti del sistema audio di Windows Vista) nel sito Web Audio Device Technologies for Windows (Tecnologie per dispositivi audio [per Windows).](https://www.microsoft.com/whdc/device/audio/default.mspx)

Questa proprietà si applica solo agli apo degli effetti locali e globali installati dal file inf che ha installato la scheda audio a cui è connesso il dispositivo endpoint. Inoltre, questa proprietà influisce solo sul dispositivo endpoint di destinazione. Non ha alcun effetto sugli effetti del sistema per qualsiasi altro dispositivo endpoint, anche se si connettono alla stessa scheda.

Il **membro vt** della **struttura PROPVARIANT** è impostato su **VT \_ UI4.**

Il **membro ulVal** della **struttura PROPVARIANT** è impostato su **ENDPOINT \_ SYSFX \_ ENABLED** se gli effetti di sistema sono abilitati o su **ENDPOINT \_ SYSFX \_ DISABLED** se sono disabilitati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Mmdeviceapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà dell'endpoint audio**](audio-endpoint-properties.md)
</dt> <dt>

[Proprietà audio principali](core-audio-properties.md)
</dt> </dl>

 

 




