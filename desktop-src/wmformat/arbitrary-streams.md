---
title: Codice Flussi
description: Codice Flussi
ms.assetid: 81fd3b07-7cf2-4013-97ed-9718142ca4c3
keywords:
- Windows Media Format SDK, flussi arbitrari
- Advanced Systems Format (ASF), flussi arbitrari
- ASF (Advanced Systems Format), flussi arbitrari
- Windows MEDIA Format SDK, flussi
- Advanced Systems Format (ASF), flussi
- ASF (Advanced Systems Format), flussi
- flussi arbitrari
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b2cc0587758af8dfa3d4ee05b1a51943a89684629fe2182f5a33fdabbdb68e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118434717"
---
# <a name="arbitrary-streams"></a>Codice Flussi

Oltre ai flussi audio e video e ai flussi di immagini, un file ASF può contenere flussi contenenti un'ampia gamma di dati. Gli oggetti di Windows Media Format SDK forniscono il supporto per flussi di script, flussi di trasferimento di file, flussi Web e flussi di dati arbitrari. Tutti questi tipi di flusso sono arbitrari, ovvero non viene eseguita alcuna convalida dei dati dall'oggetto di lettura. Quando si includono flussi di questi tipi nei file, assicurarsi che l'applicazione di lettura esegua la convalida o il controllo dei dati per assicurarsi che il contenuto non sia stato danneggiato o intenzionalmente danneggiato da terze parti malintenzionate.

Anche se gli oggetti di questo SDK non verificano o convalidano i dati in flussi arbitrari, sono supportati in modo nativo diversi tipi di flussi arbitrari. Nella tabella seguente sono elencati i tipi di flusso arbitrari predefiniti. Sono supportati anche i flussi di script, ma vengono illustrati separatamente nella [sezione Comandi script.](script-commands.md) Per altre informazioni sulla creazione di tipi personalizzati, vedere [Custom Arbitrary Data Flussi](custom-arbitrary-data-streams.md).



| Tipo arbitrario                   | Descrizione                                                       |
|----------------------------------|-------------------------------------------------------------------|
| [Flussi di testo](text-streams.md) | Contengono stringhe di testo.                                             |
| [File Flussi](file-streams.md) | Contengono uno o più file di dati.                                   |
| [Web Flussi](web-streams.md)   | Contengono file di dati equivalenti alla versione memorizzata nella cache delle pagine Web. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Funzionalità dei file ASF**](asf-file-features.md)
</dt> <dt>

[**Audio e video Flussi**](audio-and-video-streams.md)
</dt> <dt>

[**Configurazione di tipi di flusso arbitrari**](configuring-arbitrary-stream-types.md)
</dt> </dl>

 

 




