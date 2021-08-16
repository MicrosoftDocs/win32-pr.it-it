---
title: Indici
description: Indici
ms.assetid: 54c694f6-3c10-4d7c-bcd1-f2b17d652e8e
keywords:
- Windows Media Format SDK, indici
- Advanced Systems Format (ASF), indexes
- ASF (Advanced Systems Format), indici
- Windows Media Format SDK, indici temporali
- Advanced Systems Format (ASF), indici temporali
- ASF (Advanced Systems Format), indici temporali
- Windows Media Format SDK, indici basati su frame
- Advanced Systems Format (ASF), indici basati su frame
- ASF (Advanced Systems Format), indici basati su frame
- Windows Media Format SDK, codici temporici SMPTE
- Advanced Systems Format (ASF), codici di ora SMPTE
- ASF (Advanced Systems Format), codici di ora SMPTE
- indici, informazioni
- indici temporali
- indici basati su frame
- codici di tempo SMPTE, indici
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71af891ba2986d3ece1eb2d4cc7eb7ff4086c06eee1f60eabb2210bdc8b6bacd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118702485"
---
# <a name="indexes"></a>Indici

Un requisito comune per le applicazioni che leggono file multimediali digitali è la possibilità di cercare un punto specifico nel contenuto. La ricerca può essere difficile perché non esiste alcuna garanzia che i vari flussi in un file presentino esempi con orari di inizio simultanei. Questo problema viene risolto con l'uso *di indici*. Un indice è un oggetto in un file ASF che equivale agli esempi video con i relativi orari di presentazione. Non è necessario alcun indice per i flussi audio perché i dati audio sono più strettamente connessi all'ora di presentazione rispetto ai dati video.

L'oggetto indicizzatore di Windows Media Format SDK può creare tre diversi tipi di indici: indici temporali, indici basati su frame e indici time code SMPTE.

Gli indici temporali sono il tipo più comune. Equano semplicemente gli esempi di video con i tempi di presentazione corrispondenti.

Un indice basato su frame equivale agli esempi di video con i numeri di fotogrammi video e i tempi di presentazione. I numeri di fotogramma sono particolarmente utili nelle applicazioni che modificano i video.

Un indice smtpe time code è il tipo più raro di indice. Usa il timestamp SMPTE time code come base dell'indice e può essere usato solo nei flussi con timestamp SMPTE inclusi nei relativi esempi. Per altre informazioni su SMPTE time code, vedere Supporto del codice temporale [SMPTE](smpte-time-code-support.md).

Un file ASF può contenere un indice di ogni tipo per ogni flusso video in esso contenuto. Come impostazione predefinita, viene incluso un indice temporale per ogni flusso video nei file creati dall'oggetto writer. È possibile modificare le impostazioni di indicizzazione automatica per i file in base alle esigenze.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Funzionalità dei file ASF**](asf-file-features.md)
</dt> <dt>

[**Operazioni con gli indici**](working-with-indexes.md)
</dt> <dt>

[**Lettura di file con il lettore asincrono**](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[**Lettura di file con il lettore sincrono**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




