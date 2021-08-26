---
title: Rendering del contenuto
description: Rendering del contenuto
ms.assetid: 9a3baa33-dac4-4742-8f80-33b05caada09
keywords:
- Windows MEDIA Format SDK, rendering del contenuto
- Advanced Systems Format (ASF), rendering del contenuto
- ASF (Advanced Systems Format), rendering del contenuto
- Advanced Systems Format (ASF), rendering del contenuto
- ASF (Advanced Systems Format),rendering del contenuto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7add8d31f1fd025327325256e56c9f38faa4c97fd7e2aa206cedfebcc84c1302
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119929659"
---
# <a name="rendering-content"></a>Rendering del contenuto

L Windows Media Format SDK non fornisce routine per il rendering del contenuto fornito dall'oggetto lettore. Se si scrivono applicazioni per riprodurre il contenuto nei file ASF, è necessario implementare routine di rendering personalizzate.

È necessario prestare attenzione durante il rendering del contenuto per assicurarsi che il rendering degli esempi sia eseguito in ordine di tempo di presentazione e che i campioni di flussi diversi siano sincronizzati durante il rendering. Il metodo utilizzato per garantire che la sincronizzazione dei flussi dipersi dalla tecnica di rendering utilizzata per l'applicazione. In generale, se si dispone di flussi audio e video, è consigliabile eseguire la sincronizzazione con il flusso audio, perché l'incoerenza nel flusso audio è più evidente di alcuni fotogrammi rilasciati in un flusso video.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Lettura di file ASF**](reading-asf-files.md)
</dt> <dt>

[**Per recuperare esempi multimediali con il lettore asincrono**](to-retrieve-media-samples-with-the-asynchronous-reader.md)
</dt> <dt>

[**Per recuperare esempi di file multimediali con il lettore sincrono**](to-retrieve-media-samples-with-the-synchronous-reader.md)
</dt> </dl>

 

 




