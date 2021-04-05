---
title: Flussi arbitrari
description: Flussi arbitrari
ms.assetid: 81fd3b07-7cf2-4013-97ed-9718142ca4c3
keywords:
- Windows Media Format SDK, flussi arbitrari
- ASF (Advanced Systems Format), flussi arbitrari
- ASF (formato avanzato dei sistemi), flussi arbitrari
- Windows Media Format SDK, flussi
- Formato di sistemi avanzati (ASF), flussi
- ASF (formato avanzato dei sistemi), flussi
- flussi arbitrari
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe28a3b30e0f711c69998b78c81fc1e745fe6360
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707870"
---
# <a name="arbitrary-streams"></a>Flussi arbitrari

Oltre ai flussi audio e video e ai flussi di immagini, un file ASF può contenere i flussi che contengono una varietà di dati. Gli oggetti di Windows Media Format SDK forniscono supporto per flussi di script, flussi di trasferimento di file, flussi Web e flussi di dati arbitrari. Tutti questi tipi di flusso sono arbitrari, ovvero non viene eseguita alcuna convalida dei dati da parte dell'oggetto di lettura. Quando si includono flussi di questi tipi nei file, assicurarsi che l'applicazione di lettura esegua la convalida o il controllo dei dati per garantire che il contenuto non sia stato danneggiato o intenzionalmente modificato da terze parti dannose.

Sebbene gli oggetti di questo SDK non verifichino o convalidano i dati in flussi arbitrari, diversi tipi di flussi arbitrari sono supportati in modo nativo. Nella tabella seguente sono elencati i tipi di flusso arbitrari predefiniti. Sono supportati anche i flussi di script, ma vengono descritti separatamente nella sezione [comandi script](script-commands.md) . Per ulteriori informazioni sulla creazione di tipi personalizzati, vedere [flussi di dati arbitrari personalizzati](custom-arbitrary-data-streams.md).



| Tipo arbitrario                   | Descrizione                                                       |
|----------------------------------|-------------------------------------------------------------------|
| [Flussi di testo](text-streams.md) | Contengono stringhe di testo.                                             |
| [Flussi di file](file-streams.md) | Contenere uno o più file di dati.                                   |
| [Flussi Web](web-streams.md)   | Contiene file di dati equivalenti alla versione memorizzata nella cache di pagine Web. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Funzionalità file ASF**](asf-file-features.md)
</dt> <dt>

[**Flussi audio e video**](audio-and-video-streams.md)
</dt> <dt>

[**Configurazione di tipi di flusso arbitrari**](configuring-arbitrary-stream-types.md)
</dt> </dl>

 

 




