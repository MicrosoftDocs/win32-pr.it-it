---
title: Per recapitare esempi compressi con il lettore asincrono
description: Per recapitare esempi compressi con il lettore asincrono
ms.assetid: 488baa3c-8863-4afc-89b2-fe55823e5db9
keywords:
- Advanced Systems Format (ASF), distribuzione di esempi compressi
- ASF (Advanced Systems Format), distribuzione di esempi compressi
- ASF (Advanced Systems Format), Reader asincroni
- ASF (formato avanzato dei sistemi), Reader asincroni
- ASF (Advanced Systems Format), esempi compressi
- ASF (Advanced Systems Format), esempi compressi
- Reader asincroni, distribuzione di esempi compressi
- Reader asincroni, esempi compressi
- esempi compressi, distribuzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4ce835075f5bd760014a3b1b776ba3627adb076
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723535"
---
# <a name="to-deliver-compressed-samples-with-the-asynchronous-reader"></a>Per recapitare esempi compressi con il lettore asincrono

Il lettore asincrono può recapitare esempi compressi dai flussi nei file ASF. Le applicazioni in genere inviano esempi compressi quando si copia un flusso da un file a un altro. Non è consigliabile ricomprimere i dati ricostruiti da un flusso compresso, perché i dati vengono persi nel processo di codifica. I file multimediali digitali compressi più di una volta avranno una notevole riduzione della qualità.

Windows Media Format SDK non fornisce alcun metodo per la decodifica dei dati dopo che è stato Estratto da un file ASF. Se si ricevono esempi compressi e successivamente si desidera decomprimerli, sarà necessario fornire il proprio codice a tale scopo. Per aggirare questa limitazione, è possibile scrivere gli esempi compressi in un nuovo file ASF e quindi leggerli nuovamente in campioni normali non compressi.

Per ricevere esempi compressi con il lettore asincrono, seguire questa procedura.

1.  Implementare il callback [**IWMReaderCallbackAdvanced:: OnStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample) . Questo callback è sostanzialmente identico nella funzione di [**IWMReaderCallback:: OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) con la differenza che fornisce esempi in base al numero di flusso e gli esempi sono ancora compressi.
2.  Prima di avviare la riproduzione, ottenere un puntatore all'interfaccia [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced) dell'oggetto Reader chiamando **IWMReader:: QueryInterface**.
3.  Configurare il Reader per il recapito di esempi compressi per il flusso desiderato chiamando [**IWMReaderAdvanced:: SetReceiveStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setreceivestreamsamples).
4.  Ripetere il passaggio 3 per ogni flusso per il quale si desidera il recapito di esempio compresso.

> [!Note]  
> I flussi di immagini non sono validi per il recapito di flussi compressi. Se si copia un flusso di immagini da un file a un altro, non funzionerà nel nuovo file. Per copiare un flusso di immagini da un file a un altro, recuperare gli esempi di flusso dell'immagine in base al numero di output e includerli nel nuovo file come se fosse incluso un nuovo flusso di immagine.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfaccia IWMReaderCallbackAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallbackadvanced)
</dt> <dt>

[**Lettura di file con il lettore asincrono**](reading-files-with-the-asynchronous-reader.md)
</dt> </dl>

 

 




