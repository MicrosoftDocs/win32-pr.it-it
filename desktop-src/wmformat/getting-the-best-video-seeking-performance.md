---
title: Ottenere le migliori prestazioni di ricerca video
description: Ottenere le migliori prestazioni di ricerca video
ms.assetid: 21269f0c-fc3a-46fc-88b4-f71828b5d5a7
keywords:
- Windows Media Format SDK, migliori prestazioni di ricerca video
- Advanced Systems Format (ASF), migliori prestazioni di ricerca video
- ASF (Advanced Systems Format), migliori prestazioni di ricerca video
- ASF (Advanced Systems Format), prestazioni di ricerca video
- ASF (Advanced Systems Format), prestazioni di ricerca video
- ASF (Advanced Systems Format), prestazioni
- ASF (formato avanzato dei sistemi), prestazioni
- ricerca video
- prestazioni, ricerca video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c95feb9158bbab09ce28024100f3ebbffb56ad9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298511"
---
# <a name="getting-the-best-video-seeking-performance"></a>Ottenere le migliori prestazioni di ricerca video

La ricerca di contenuto in un file è un'operazione molto comune che potenzialmente rappresenta un problema di prestazioni. Il video codificato con il codec Windows Media Video 9 è costituito principalmente da frame Delta, che registrano solo le modifiche in relazione al frame precedente. La ricostruzione di frame Delta richiede tempo, in particolare se i fotogrammi chiave sono lontani. Per ulteriori informazioni sulla configurazione di fotogrammi chiave per una ricerca efficiente, vedere [configurazione dei flussi video per la ricerca delle prestazioni](configuring-video-streams-for-seeking-performance.md).

Oltre alla configurazione corretta, è possibile migliorare le prestazioni di ricerca usando l'indicizzazione dei frame per il flusso video. La ricerca di un numero di frame è in genere più veloce rispetto alla ricerca di un'ora di presentazione.

Se si cerca in un file con più flussi, è necessario selezionare solo i flussi necessari. Ogni flusso configurato per la lettura influirà sulle prestazioni della ricerca, perché tutti i flussi selezionati sono sincronizzati quando si cerca un punto in un file.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Lettura di file ASF**](reading-asf-files.md)
</dt> <dt>

[**Per eseguire la ricerca in base al numero di frame utilizzando il Reader asincrono**](to-seek-by-frame-number-using-the-asynchronous-reader.md)
</dt> <dt>

[**Per eseguire la ricerca in base al numero di frame utilizzando il lettore sincrono**](to-seek-by-frame-number-using-the-synchronous-reader.md)
</dt> <dt>

[**Per eseguire ricerche in base al tempo tramite il Reader asincrono**](to-seek-by-time-using-the-asynchronous-reader.md)
</dt> <dt>

[**Per eseguire ricerche in base al tempo tramite il lettore sincrono**](to-seek-by-time-using-the-synchronous-reader.md)
</dt> </dl>

 

 




