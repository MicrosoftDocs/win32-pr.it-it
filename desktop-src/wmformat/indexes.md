---
title: Indici
description: Indici
ms.assetid: 54c694f6-3c10-4d7c-bcd1-f2b17d652e8e
keywords:
- Windows Media Format SDK, indici
- ASF (Advanced Systems Format), indici
- ASF (formato avanzato dei sistemi), indici
- Windows Media Format SDK, indici temporali
- ASF (Advanced Systems Format), indici temporali
- ASF (formato avanzato dei sistemi), indici temporali
- Windows Media Format SDK, indici basati su frame
- ASF (Advanced Systems Format), indici basati su frame
- ASF (formato avanzato dei sistemi), indici basati su frame
- Windows Media Format SDK, codici temporali SMPTE
- ASF (Advanced Systems Format), codici temporali SMPTE
- ASF (Advanced Systems Format), codici temporali SMPTE
- indici, informazioni
- indici temporali
- indici basati su frame
- Codici temporali SMPTE, indici
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d2e5a194f9c495720cbc40ccdb192509723eee0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856697"
---
# <a name="indexes"></a>Indici

Un requisito comune per le applicazioni che leggono i file multimediali digitali è la possibilità di ricercare un punto specifico nel contenuto. La ricerca può essere difficile perché non vi è alcuna garanzia che i vari flussi in un file includano campioni con orari di avvio simultanei. Questo problema viene risolto con l'uso degli *indici*. Un indice è un oggetto in un file ASF che equivale ai campioni video con le relative ore di presentazione. Per i flussi audio non è richiesto alcun indice perché i dati audio sono strettamente connessi all'ora di presentazione rispetto ai dati video.

L'oggetto indicizzatore di Windows Media Format SDK può creare tre diversi tipi di indici: indici temporali, indici basati su frame e indici di codice in tempo SMPTE.

Gli indici temporali sono il tipo più comune. Equivalgono semplicemente agli esempi video con i tempi di presentazione corrispondenti.

Un indice basato su frame equivale a esempi video con numeri di fotogrammi video e tempi di presentazione. I numeri di frame sono particolarmente utili nelle applicazioni che modificano il video.

Un indice del codice ora SMTP è il tipo di indice più raro. Usa il codice di ora SMPTE come base dell'indice e può essere usato solo in flussi con timestamp SMPTE inclusi negli esempi. Per altre informazioni sul codice ora SMPTE, vedere [supporto del codice ora SMPTE](smpte-time-code-support.md).

Un file ASF può contenere un indice di ogni tipo per ogni flusso video che contiene. Come impostazione predefinita, viene incluso un indice temporale per ogni flusso video nei file creati dall'oggetto writer. È possibile modificare le impostazioni di indicizzazione automatica per i file in base alle esigenze.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Funzionalità file ASF**](asf-file-features.md)
</dt> <dt>

[**Operazioni con gli indici**](working-with-indexes.md)
</dt> <dt>

[**Lettura di file con il lettore asincrono**](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[**Lettura di file con il lettore sincrono**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




