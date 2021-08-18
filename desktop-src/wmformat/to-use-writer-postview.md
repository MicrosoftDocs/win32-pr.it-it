---
title: Per usare Postview writer
description: Per usare Postview writer
ms.assetid: 9da3c749-f6bd-43b5-9eff-3a637ddef048
keywords:
- Advanced Systems Format (ASF), writer postview
- ASF (Advanced Systems Format), writer postview
- Advanced Systems Format (ASF), postviewing
- ASF (Advanced Systems Format), postviewing
- postview writer
- postviewing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7800f3ba50f9f1d61793a0d2ada2db0c03d6b88551ac1147e17872aa8e428c39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118196405"
---
# <a name="to-use-writer-postview"></a>Per usare Postview writer

L'oggetto writer fornisce funzionalità di postviewing in modo che sia possibile verificare il contenuto scritto senza dover configurare l'oggetto lettore. L'oggetto writer non supporta la postviewing per il contenuto audio.

Il postviewer del writer funziona in modo molto identico all'oggetto lettore asincrono, solo con un minor numero di funzionalità. Per informazioni dettagliate sulla lettura dei supporti digitali, vedere [Lettura di file ASF.](reading-asf-files.md)

Per implementare il postviewer, seguire questa procedura.

1.  Implementare il callback [**IWMWriterPostViewCallback::OnPostViewSample.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostviewcallback-onpostviewsample) Questo metodo è essenzialmente lo stesso di [**IWMReaderCallback::OnSample,**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) ad eccezione del fatto che specifica i numeri di flusso anziché gli output.
2.  Configurare per la scrittura come di consueto.
3.  Ottenere un puntatore [**all'interfaccia IWMWriterPostView**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostview) dell'oggetto writer chiamando **IWMWriter::QueryInterface**.
4.  Impostare il callback per il postviewer da usare chiamando [**IWMWriterPostView::SetPostViewCallback**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostview-setpostviewcallback).
5.  Per ogni flusso per cui si vogliono ricevere esempi postview, chiamare [**IWMWriterPostView::SetReceivePostViewSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostview-setreceivepostviewsamples). È possibile verificare se un flusso è impostato per ricevere esempi postview chiamando [**IWMWriterPostView::GetReceivePostViewSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostview-getreceivepostviewsamples).
6.  È possibile modificare i formati di esempio, proprio come si farebbe con i formati di output nell'oggetto reader o nell'oggetto lettore sincrono.
7.  Quando si inizia a scrivere il file, si inizieranno a ricevere esempi nell'implementazione del metodo di callback **OnPostViewSample.**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfaccia IWMWriterPostViewCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostviewcallback)
</dt> <dt>

[**Scrittura di file ASF**](writing-asf-files.md)
</dt> </dl>

 

 




