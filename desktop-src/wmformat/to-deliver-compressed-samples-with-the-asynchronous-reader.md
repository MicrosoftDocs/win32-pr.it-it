---
title: Per distribuire esempi compressi con il lettore asincrono
description: Per distribuire esempi compressi con il lettore asincrono
ms.assetid: 488baa3c-8863-4afc-89b2-fe55823e5db9
keywords:
- Advanced Systems Format (ASF), distribuzione di esempi compressi
- ASF (Advanced Systems Format), distribuzione di esempi compressi
- Advanced Systems Format (ASF), lettori asincroni
- ASF (Advanced Systems Format),lettori asincroni
- Advanced Systems Format (ASF), esempi compressi
- ASF (Advanced Systems Format), esempi compressi
- lettori asincroni, distribuzione di esempi compressi
- lettori asincroni, esempi compressi
- esempi compressi, distribuzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd9199fb1deefdd3c7408bc9039639bd723b06c380c03d249c9c71a1d792c1e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118699931"
---
# <a name="to-deliver-compressed-samples-with-the-asynchronous-reader"></a>Per distribuire esempi compressi con il lettore asincrono

Il lettore asincrono può distribuire esempi compressi da flussi in file ASF. Le applicazioni in genere forniscono esempi compressi quando si copia un flusso da un file a un altro. Non è consigliabile ricomprimere i dati ricostruiti da un flusso compresso, perché i dati vengono persi nel processo di codifica. I supporti digitali compressi più di una volta avranno una notevole riduzione della qualità.

L Windows Media Format SDK non fornisce metodi per decodificare i dati dopo che sono stati estratti da un file ASF. Se si ricevono esempi compressi e in un secondo momento si vuole decomprimerli, sarà necessario fornire il proprio codice per eseguire questa operazione. Un modo per aggirare questa limitazione è scrivere gli esempi compressi in un nuovo file ASF e quindi rilevarli in normali esempi non compressi.

Per ricevere esempi compressi con il lettore asincrono, seguire questa procedura.

1.  Implementare il callback [**IWMReaderCallbackAdvanced::OnStreamSample.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample) Questo callback è fondamentalmente identico in funzione a [**IWMReaderCallback::OnSample,**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) ad eccezione del fatto che fornisce esempi in base al numero di flusso e gli esempi sono ancora compressi.
2.  Prima di avviare la riproduzione, ottenere un puntatore [**all'interfaccia IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced) dell'oggetto reader chiamando **IWMReader::QueryInterface.**
3.  Configurare il lettore per distribuire esempi compressi per il flusso desiderato chiamando [**IWMReaderAdvanced::SetReceiveStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setreceivestreamsamples).
4.  Ripetere il passaggio 3 per ogni flusso per il quale si desidera il recapito di campioni compressi.

> [!Note]  
> I flussi di immagini non sono validi per il recapito di flussi compressi. Se si copia un flusso di immagini da un file a un altro, non funzionerà nel nuovo file. Per copiare un flusso di immagine da un file a un altro, recuperare gli esempi del flusso di immagini in base al numero di output e includerli nel nuovo file come se si include un nuovo flusso immagine.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfaccia IWMReaderCallbackAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallbackadvanced)
</dt> <dt>

[**Lettura di file con il lettore asincrono**](reading-files-with-the-asynchronous-reader.md)
</dt> </dl>

 

 




