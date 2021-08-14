---
title: Per usare postview writer
description: Per usare postview writer
ms.assetid: 9da3c749-f6bd-43b5-9eff-3a637ddef048
keywords:
- Advanced Systems Format (ASF),writer postview
- ASF (Advanced Systems Format),writer postview
- Advanced Systems Format (ASF), postviewing
- ASF (Advanced Systems Format), postviewing
- writer postview
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
# <a name="to-use-writer-postview"></a>Per usare postview writer

L'oggetto writer fornisce funzionalità di postviewing che consentono di verificare il contenuto scritto senza dover configurare l'oggetto lettore. L'oggetto writer non supporta la visualizzazione di postview per il contenuto audio.

Il postviewer del writer funziona in modo molto uguale all'oggetto reader asincrono, solo con meno funzionalità. Per informazioni dettagliate sulla lettura di file multimediali digitali, vedere [Lettura di file ASF.](reading-asf-files.md)

Per implementare il postviewer, seguire questa procedura.

1.  Implementare il callback [**IWMWriterPostViewCallback::OnPostViewSample.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostviewcallback-onpostviewsample) Questo metodo è essenzialmente uguale a [**IWMReaderCallback::OnSample,**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) ad eccezione del fatto che specifica i numeri di flusso anziché gli output.
2.  Configurare la scrittura come di consueto.
3.  Ottenere un puntatore [**all'interfaccia IWMWriterPostView**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostview) dell'oggetto writer chiamando **IWMWriter::QueryInterface.**
4.  Impostare il callback per il postviewer da usare chiamando [**IWMWriterPostView::SetPostViewCallback.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostview-setpostviewcallback)
5.  Per ogni flusso per cui si vogliono ricevere esempi di postview, chiamare [**IWMWriterPostView::SetReceivePostViewSamples.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostview-setreceivepostviewsamples) È possibile verificare se un flusso è impostato per ricevere esempi di postview chiamando [**IWMWriterPostView::GetReceivePostViewSamples.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostview-getreceivepostviewsamples)
6.  È possibile modificare i formati di esempio, esattamente come si farebbe con i formati di output nell'oggetto reader o nell'oggetto reader sincrono.
7.  Quando inizi a scrivere il file, inizi a ricevere esempi nell'implementazione del metodo di callback **OnPostViewSample.**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfaccia IWMWriterPostViewCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostviewcallback)
</dt> <dt>

[**Scrittura di file ASF**](writing-asf-files.md)
</dt> </dl>

 

 




