---
description: L'oggetto divisore fornisce funzionalità di analisi del layout che classificano e raggruppano i tratti in elementi strutturali diversi.
ms.assetid: 9e4ed24f-4451-431c-9f0f-2f1c4f5e5084
title: Analisi dell'input penna con l'oggetto divisore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37f1df175f8746e56cf6ebd1b222b3901fbef36e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525315"
---
# <a name="ink-analysis-with-the-divider-object"></a>Analisi dell'input penna con l'oggetto divisore

L'oggetto [divisore](/previous-versions/ms583616(v=vs.100)) fornisce funzionalità di analisi del layout che classificano e raggruppano i tratti in elementi strutturali diversi.

## <a name="divider-object"></a>Oggetto divisore

L'oggetto [divisore](/previous-versions/ms583616(v=vs.100)) analizza i tratti quando vengono aggiunti o rimossi. È possibile recuperare la classificazione e il raggruppamento correnti dei tratti analizzati in un oggetto [DivisionResult](/previous-versions/ms583620(v=vs.100)) chiamando il metodo [divide](/previous-versions/ms568936(v=vs.100)) dell'oggetto divisore.

I tratti analizzati dall'oggetto [divisore](/previous-versions/ms583616(v=vs.100)) vengono conservati nella proprietà [Strokes](/previous-versions/ms582090(v=vs.100)) dell'oggetto divisore. Poiché una raccolta [Strokes](/previous-versions/ms552701(v=vs.100)) è un riferimento ai dati di input penna e non è i dati effettivi, le modifiche nell'oggetto [input penna](/previous-versions/ms583670(v=vs.100)) padre della raccolta Strokes possono invalidare la raccolta Strokes. Per ulteriori informazioni sui dati Ink, vedere [input penna](ink-data.md).

L'oggetto [divisore](/previous-versions/ms583616(v=vs.100)) utilizza un contesto di riconoscimento per migliorare l'analisi dei segmenti di riconoscimento e generare testo di riconoscimento per gli elementi di grafia. Se un contesto di riconoscimento non è assegnato alla proprietà [RecognizerContext](/previous-versions/ms582089(v=vs.100)) dell'oggetto divisore o i riconoscitori non sono installati, la funzionalità di analisi del layout esegue la divisione del segmento di riconoscimento e nessun testo è associato all'oggetto [DivisionResult](/previous-versions/ms583620(v=vs.100)) . Per ulteriori informazioni sul riconoscimento di input penna, vedere [input penna](ink-recognition.md).

## <a name="divisionresult-object"></a>Oggetto DivisionResult

Ogni oggetto [DivisionResult](/previous-versions/ms583620(v=vs.100)) registra l'analisi del layout dei tratti contenuti nell'oggetto [divisore](/previous-versions/ms583616(v=vs.100)) nel momento in cui viene chiamato il metodo [divide](/previous-versions/ms568936(v=vs.100)) . L'oggetto DivisionResult archivia inoltre una copia dei tratti utilizzati nell'analisi.

L'oggetto [DivisionResult](/previous-versions/ms583620(v=vs.100)) raggruppa i risultati dell'analisi in base al tipo di elemento strutturale. Il metodo [**ResultByType**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-resultbytype) dell'oggetto DivisionResult restituisce in una raccolta [DivisionUnits](/previous-versions/ms583625(v=vs.100)) la raccolta di tutti gli elementi strutturali di un determinato tipo. L'enumerazione [InkDivisionType](/previous-versions/ms552251(v=vs.100)) definisce i tipi di elemento riconosciuti dall'analisi del layout.

Nella tabella seguente vengono descritti i tipi di elemento nell'enumerazione [InkDivisionType](/previous-versions/ms552251(v=vs.100)) .



| Nome                 | Descrizione                                                                      |
|----------------------|----------------------------------------------------------------------------------|
| Segment<br/>   | Segmento di riconoscimento.<br/>                                                |
| Linea<br/>      | Riga di grafia che contiene uno o più segmenti di riconoscimento.<br/> |
| Paragraph<br/> | Un blocco di tratti che contiene una o più righe di grafia.<br/>    |
| Disegno<br/>   | Input penna non di testo.<br/>                                                 |



 

Nell'immagine seguente viene illustrato un esempio dei diversi tipi di elemento riconosciuti dall'oggetto [DivisionResult](/previous-versions/ms583620(v=vs.100)) .

![illustrazione dei diversi tipi di elemento riconosciuti dall'oggetto DivisionResult](images/5f2ab955-1f74-4b71-b3ba-8d1ca23e0578.gif)

## <a name="divisionunits-collection-and-divisionunit-objects"></a>Oggetti Collection e DivisionUnit di DivisionUnits

Ogni raccolta [DivisionUnits](/previous-versions/ms583625(v=vs.100)) è una copia del risultato dell'analisi del layout per un singolo tipo di elemento strutturale. L'oggetto [DivisionUnit](/previous-versions/ms583624(v=vs.100)) rappresenta un singolo elemento nella raccolta DivisionUnits. Ogni elemento strutturale presenta un riferimento ai tratti che compongono l'elemento. Se sono installati i riconoscitori, gli elementi della grafia hanno il testo di riconoscimento disponibile. Gli elementi del segmento di linea e riconoscimento includono inoltre una matrice di rotazione che può ruotare i tratti di un elemento da verticale a orizzontale.

Nell'argomento di [esempio Ink divisori](ink-divider-sample.md) viene illustrato come utilizzare un oggetto [divisore](/previous-versions/ms583616(v=vs.100)) con oggetti [Ink](/previous-versions/ms583670(v=vs.100)) per eseguire l'analisi del layout dell'input penna.

Per ulteriori informazioni sull'utilizzo dell'analisi dell'input penna, vedere [l'oggetto divisore](the-divider-object.md).

 

