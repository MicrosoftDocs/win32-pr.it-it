---
title: Per implementare il callback OnSample
description: Per implementare il callback OnSample
ms.assetid: 83bce8ee-6ce8-4079-9c87-2314824b1946
keywords:
- Advanced Systems Format (ASF), implementazione del callback di OnStatus
- ASF (Advanced Systems Format), implementazione del callback di OnStatus
- ASF (Advanced Systems Format), callback di OnStatus
- ASF (formato avanzato dei sistemi), callback OnStatus
- ASF (Advanced Systems Format), Reader asincroni
- ASF (formato avanzato dei sistemi), Reader asincroni
- Reader asincroni, implementazione del callback di OnStatus
- Metodo di callback OnStatus, implementazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2f19e81df5ee4769e1353c299a14626cb1a9aed
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "104336649"
---
# <a name="to-implement-the-onsample-callback"></a>Per implementare il callback OnSample

Il lettore asincrono recapita esempi all'applicazione di controllo in base all'ordine in fase di presentazione effettuando chiamate al metodo di callback [**IWMReaderCallback:: OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) . Quando si crea un'applicazione utilizzando il Reader asincrono, è necessario implementare **OnSample** per gestire gli esempi non compressi. In genere, le funzioni o i metodi creati per eseguire il rendering del contenuto verranno chiamati dall'interno di **OnSample**.

L'implementazione tipica del callback **OnSample** include i passaggi seguenti.

1.  Recuperare il percorso e le dimensioni del buffer che contiene l'esempio chiamando [**INSSBuffer:: GetBufferAndLength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-getbufferandlength) sul buffer passato come *pSample*.
2.  Creare un ramo della logica a seconda del numero di output. Il numero di output viene passato a **OnSample** come *dwOutputNumber*.
3.  Includere la logica di rendering per ogni numero di output che si desidera supportare. Se si esegue il rendering di esempi da più output, potrebbe essere necessario sincronizzare il rendering.

Le applicazioni che recapitano esempi compressi dai file ASF devono implementare il metodo di callback [**IWMReaderCallbackAdvanced:: OnStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample) . **OnStreamSample** funziona in modo quasi identico a **OnSample**, ad eccezione del fatto che riceve campioni compressi per numero di flusso anziché campioni non compressi per numero di output.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfaccia IWMReaderCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback)
</dt> <dt>

[**Interfaccia IWMReaderCallbackAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallbackadvanced)
</dt> <dt>

[**Lettura di file con il lettore asincrono**](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[**Utilizzo dei metodi di callback**](using-the-callback-methods.md)
</dt> </dl>

 

 




