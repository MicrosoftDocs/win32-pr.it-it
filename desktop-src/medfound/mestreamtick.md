---
description: Segnala che a un flusso multimediale non sono disponibili dati a un'ora specificata.
ms.assetid: 1a00fff1-c3ab-4965-a663-3c15bb48ea98
title: Evento MEStreamTick (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27123569e991043a534883964ba94e4955d60a40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307991"
---
# <a name="mestreamtick-event"></a>Evento MEStreamTick

Segnala che a un flusso multimediale non sono disponibili dati a un'ora specificata.

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE           | Descrizione                                                                   |
|-------------------|-------------------------------------------------------------------------------|
| \_I8 VT<br/> | Data e ora in cui si verifica il gap, in unità di 100 nanosecondi.<br/> <br/> |



## <a name="remarks"></a>Commenti

Questo evento segnala un gap nei dati. L'evento notifica ai componenti downstream di non prevedere i dati all'ora specificata.

L'evento deve essere inviato da qualsiasi oggetto genera i timestamp per gli esempi di supporti nel flusso. A seconda del formato dei dati, è possibile:

-   Il flusso multimediale nell'origine supporto (interfaccia [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) ) o
-   Trasformazione del decodificatore (interfaccia [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) ).

Durante il gap, l'oggetto deve inviare l'evento con la stessa frequenza con cui produrrebbe normalmente esempi. Per video, inviare un evento per ogni frame mancante. Per l'audio, inviare l'evento almeno una volta al secondo durante il gap. Il valore dell'evento è il timestamp dell'esempio mancante. Inviare tutti gli eventi MEStreamTick necessari per colmare il gap nei dati.

Se un'origine multimediale presenta diversi flussi e si verifica un gap in più di un flusso, ogni flusso deve inviare eventi MEStreamTick. Se, ad esempio, è presente un gap nei dati audio e video, entrambi i flussi inviano l'evento.

L'evento MEStreamTick non completa una richiesta [**IMFMediaStream:: RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) . L'origine multimediale deve comunque inviare un evento [MEMediaSample](memediasample.md) per ogni chiamata a **RequestSample**.

I sink di supporto non possono utilizzare direttamente questo evento. Per segnalare un gap nel flusso a un sink multimediale, chiamare [**IMFStreamSink::P lacemarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) con un marcatore di segno di **MFSTREAMSINK \_ \_** . Quando necessario, la pipeline Media Foundation Converte gli eventi MEStreamTick in marcatori di segno di **MFSTREAMSINK \_ \_** .

Non impostare l'attributo [**di \_ discontinuità MFSampleExtension**](mfsampleextension-discontinuity-attribute.md) nel successivo esempio di supporto dopo un evento MEStreamTick. L'attributo di **\_ discontinuità MFSampleExtension** implica che il timestamp è discontinuo con i timestamp precedenti, mentre MEStreamTick implica che i timestamp sono continui ma alcuni dati risultano mancanti.

> [!Note]  
> Una versione precedente della documentazione ha erroneamente dichiarato che l'esempio dopo un evento MEStreamTick deve avere l'attributo [**di \_ discontinuità MFSampleExtension**](mfsampleextension-discontinuity-attribute.md) .

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Mfobjects. h (include Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Eventi Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




