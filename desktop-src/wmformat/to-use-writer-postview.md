---
title: Per utilizzare PostView writer
description: Per utilizzare PostView writer
ms.assetid: 9da3c749-f6bd-43b5-9eff-3a637ddef048
keywords:
- Formato avanzato dei sistemi (ASF), PostView writer
- ASF (formato avanzato dei sistemi), PostView writer
- Formato avanzato dei sistemi (ASF), visualizzazione
- ASF (formato avanzato dei sistemi), visualizzazione
- PostView writer
- visualizzazione in anteprima
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abb3c1c83ebd38ff04c2022e529693d3d43b8b35
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "104516669"
---
# <a name="to-use-writer-postview"></a>Per utilizzare PostView writer

L'oggetto writer fornisce funzionalità di visualizzazione in modo che sia possibile verificare il contenuto scritto senza dover impostare l'oggetto Reader. L'oggetto writer non supporta l'anteprima per il contenuto audio.

Il revisore del writer funziona in modo molto simile all'oggetto Reader asincrono, solo con meno funzionalità. Per informazioni dettagliate sulla lettura di file multimediali digitali, vedere la pagina relativa alla [lettura di file ASF](reading-asf-files.md).

Per implementare il postvisore, seguire questa procedura.

1.  Implementare il callback [**IWMWriterPostViewCallback:: OnPostViewSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostviewcallback-onpostviewsample) . Questo metodo è essenzialmente lo stesso di [**IWMReaderCallback:: OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) , ad eccezione del fatto che specifica i numeri di flusso anziché gli output.
2.  Configurare per la scrittura come di consueto.
3.  Ottenere un puntatore all'interfaccia [**IWMWriterPostView**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostview) dell'oggetto writer chiamando **IWMWriter:: QueryInterface**.
4.  Impostare il callback per il postvisore da utilizzare chiamando [**IWMWriterPostView:: SetPostViewCallback**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostview-setpostviewcallback).
5.  Per ogni flusso per il quale si desidera ricevere gli esempi di PostView, chiamare [**IWMWriterPostView:: SetReceivePostViewSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostview-setreceivepostviewsamples). È possibile verificare se un flusso è impostato per ricevere esempi di PostView chiamando [**IWMWriterPostView:: GetReceivePostViewSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostview-getreceivepostviewsamples).
6.  È possibile modificare i formati di esempio, esattamente come i formati di output nell'oggetto Reader o nell'oggetto Reader sincrono.
7.  Quando si inizia a scrivere il file, si inizierà a ricevere esempi nell'implementazione del metodo di callback **OnPostViewSample** .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfaccia IWMWriterPostViewCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostviewcallback)
</dt> <dt>

[**Scrittura di file ASF**](writing-asf-files.md)
</dt> </dl>

 

 




