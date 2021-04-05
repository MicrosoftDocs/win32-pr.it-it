---
title: Rendering del contenuto
description: Rendering del contenuto
ms.assetid: 9a3baa33-dac4-4742-8f80-33b05caada09
keywords:
- Windows Media Format SDK, rendering del contenuto
- Formato avanzato dei sistemi (ASF), rendering del contenuto
- ASF (Advanced Systems Format), rendering del contenuto
- ASF (Advanced Systems Format), rendering del contenuto
- ASF (formato avanzato dei sistemi), rendering del contenuto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d6a171ce9b404c4cc16862ffd64b53ada5821b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856849"
---
# <a name="rendering-content"></a>Rendering del contenuto

Windows Media Format SDK non fornisce routine per il rendering del contenuto fornito dall'oggetto Reader. Se si scrivono applicazioni per riprodurre il contenuto nei file ASF, è necessario implementare le routine di rendering personalizzate.

È necessario prestare attenzione quando si esegue il rendering del contenuto per assicurarsi che venga eseguito il rendering degli esempi in ordine di presentazione e che gli esempi di flussi diversi vengano sincronizzati durante il rendering. Il metodo utilizzato per garantire la sincronizzazione dei flussi dipenderà dalla tecnica di rendering utilizzata per l'applicazione. In generale, se si dispone di flussi audio e video, è necessario eseguire la sincronizzazione con il flusso audio, perché l'incoerenza nel flusso audio è più evidente rispetto ad alcuni frame rilasciati in un flusso video.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Lettura di file ASF**](reading-asf-files.md)
</dt> <dt>

[**Per recuperare esempi di supporti con il Reader asincrono**](to-retrieve-media-samples-with-the-asynchronous-reader.md)
</dt> <dt>

[**Per recuperare esempi di supporti con il lettore sincrono**](to-retrieve-media-samples-with-the-synchronous-reader.md)
</dt> </dl>

 

 




