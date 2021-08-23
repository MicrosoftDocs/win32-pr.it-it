---
title: Per implementare il callback OnSample
description: Per implementare il callback OnSample
ms.assetid: 83bce8ee-6ce8-4079-9c87-2314824b1946
keywords:
- Advanced Systems Format (ASF), implementazione del callback OnStatus
- ASF (Advanced Systems Format), implementazione del callback OnStatus
- Advanced Systems Format (ASF), callback OnStatus
- ASF (Advanced Systems Format),callback OnStatus
- Advanced Systems Format (ASF), lettori asincroni
- ASF (Advanced Systems Format),lettori asincroni
- lettori asincroni, implementazione del callback OnStatus
- Metodo di callback OnStatus, implementazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc00523ae28ec14feefb8249ff86a2b1600629c84cb245eb627b59b619a28a17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027289"
---
# <a name="to-implement-the-onsample-callback"></a>Per implementare il callback OnSample

Il lettore asincrono fornisce esempi all'applicazione di controllo nell'ordine in fase di presentazione effettuando chiamate al metodo di callback [**IWMReaderCallback::OnSample.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) Quando si crea un'applicazione usando il lettore asincrono, è necessario implementare **OnSample** per gestire gli esempi non compressi. In genere, le funzioni o i metodi creati per eseguire il rendering del contenuto vengono chiamati dall'interno di **OnSample.**

L'implementazione tipica del callback **OnSample** include i passaggi seguenti.

1.  Recuperare la posizione e le dimensioni del buffer contenente l'esempio chiamando [**INSSBuffer::GetBufferAndLength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-getbufferandlength) nel buffer passato *come pSample.*
2.  Creare un ramo della logica a seconda del numero di output. Il numero di output viene passato a **OnSample** *come dwOutputNumber.*
3.  Includere la logica di rendering per ogni numero di output che si vuole supportare. Se si esegue il rendering di esempi da più output, potrebbe essere necessario sincronizzare il rendering.

Le applicazioni che forniscono esempi compressi da file ASF devono implementare il metodo di callback [**IWMReaderCallbackAdvanced::OnStreamSample.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample) **OnStreamSample funziona** quasi in modo identico a **OnSample,** ad eccezione del fatto che riceve campioni compressi in base al numero di flusso anziché in base al numero di output.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfaccia IWMReaderCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback)
</dt> <dt>

[**Interfaccia IWMReaderCallbackAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallbackadvanced)
</dt> <dt>

[**Lettura di file con il lettore asincrono**](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[**Uso dei metodi di callback**](using-the-callback-methods.md)
</dt> </dl>

 

 




