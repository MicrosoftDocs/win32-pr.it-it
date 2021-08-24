---
description: L'oggetto Divider fornisce funzionalità di analisi del layout che classificano e raggruppano i tratti in elementi strutturali diversi.
ms.assetid: 9e4ed24f-4451-431c-9f0f-2f1c4f5e5084
title: Analisi dell'input penna con l'oggetto divisore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d036428bbe32c42e6419c2218e6196a0b89a892137e55d141d5553d360c0a652
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939557"
---
# <a name="ink-analysis-with-the-divider-object"></a>Analisi dell'input penna con l'oggetto divisore

[L'oggetto Divider](/previous-versions/ms583616(v=vs.100)) fornisce funzionalità di analisi del layout che classificano e raggruppano i tratti in elementi strutturali diversi.

## <a name="divider-object"></a>Oggetto Divider

[L'oggetto Divider](/previous-versions/ms583616(v=vs.100)) analizza i tratti durante l'aggiunta o la rimozione. È possibile recuperare la classificazione e il raggruppamento correnti dei tratti analizzati in un [oggetto DivisionResult](/previous-versions/ms583620(v=vs.100)) chiamando il [metodo Divide](/previous-versions/ms568936(v=vs.100)) dell'oggetto Divider.

I tratti analizzati [dall'oggetto Divider](/previous-versions/ms583616(v=vs.100)) vengono mantenuti nella [proprietà Strokes](/previous-versions/ms582090(v=vs.100)) dell'oggetto Divider. Poiché una [raccolta Strokes](/previous-versions/ms552701(v=vs.100)) è un riferimento ai dati dell'input penna e non sono i dati effettivi, le modifiche nell'oggetto [Ink](/previous-versions/ms583670(v=vs.100)) padre della raccolta Strokes possono invalidare la raccolta Strokes. Per altre informazioni sui dati dell'input penna, vedere [Dati input penna](ink-data.md).

[L'oggetto Divider](/previous-versions/ms583616(v=vs.100)) usa un contesto di riconoscimento per migliorare l'analisi dei segmenti di riconoscimento e per generare il testo di riconoscimento per gli elementi di scrittura manuale. Se un contesto di riconoscimento non è assegnato alla proprietà [RecognizerContext](/previous-versions/ms582089(v=vs.100)) dell'oggetto Divider o dei riconoscitori non è installato, la funzionalità di analisi del layout esegue la divisione del segmento di riconoscimento e nessun testo viene associato all'oggetto [DivisionResult.](/previous-versions/ms583620(v=vs.100)) Per altre informazioni sul riconoscimento dell'input penna, vedere [Riconoscimento input penna](ink-recognition.md).

## <a name="divisionresult-object"></a>Oggetto DivisionResult

Ogni [oggetto DivisionResult](/previous-versions/ms583620(v=vs.100)) registra l'analisi del layout dei tratti contenuti nell'oggetto [Divider](/previous-versions/ms583616(v=vs.100)) nel momento in cui [viene](/previous-versions/ms568936(v=vs.100)) chiamato il metodo Divide. L'oggetto DivisionResult archivia anche una copia dei tratti usati nell'analisi.

[L'oggetto DivisionResult](/previous-versions/ms583620(v=vs.100)) raggruppa i risultati dell'analisi in base al tipo di elemento strutturale. Il [**metodo ResultByType**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-resultbytype) dell'oggetto DivisionResult restituisce in una [raccolta DivisionUnits](/previous-versions/ms583625(v=vs.100)) la raccolta di tutti gli elementi strutturali di un determinato tipo. [L'enumerazione InkDivisionType](/previous-versions/ms552251(v=vs.100)) definisce i tipi di elemento che l'analisi del layout riconosce.

Nella tabella seguente vengono descritti i tipi di elemento [nell'enumerazione InkDivisionType.](/previous-versions/ms552251(v=vs.100))



| Nome                 | Descrizione                                                                      |
|----------------------|----------------------------------------------------------------------------------|
| Segment<br/>   | Segmento di riconoscimento.<br/>                                                |
| A linee<br/>      | Riga di scrittura manuale che contiene uno o più segmenti di riconoscimento.<br/> |
| Paragraph<br/> | Blocco di tratti che contiene una o più righe di scrittura manuale.<br/>    |
| Disegno<br/>   | Input penna che non è testo.<br/>                                                 |



 

L'immagine seguente mostra un esempio dei diversi tipi di elemento che [l'oggetto DivisionResult](/previous-versions/ms583620(v=vs.100)) riconosce.

![Illustrazione dei diversi tipi di elementi che l'oggetto divisionresult riconosce](images/5f2ab955-1f74-4b71-b3ba-8d1ca23e0578.gif)

## <a name="divisionunits-collection-and-divisionunit-objects"></a>Oggetti DivisionUnits Collection e DivisionUnit

Ogni [raccolta DivisionUnits](/previous-versions/ms583625(v=vs.100)) è una copia del risultato dell'analisi del layout per un singolo tipo di elemento strutturale. [L'oggetto DivisionUnit](/previous-versions/ms583624(v=vs.100)) rappresenta un singolo elemento nella raccolta DivisionUnits. Ogni elemento strutturale ha un riferimento ai tratti che costituiscono l'elemento. Se i riconoscitori sono installati, gli elementi di grafia hanno testo di riconoscimento disponibile. Gli elementi dei segmenti di linea e di riconoscimento includono anche una matrice di rotazione che può ruotare i tratti di un elemento da verticale a orizzontale.

[L'argomento Ink Divider Sample illustra](ink-divider-sample.md) come usare un oggetto [Divider](/previous-versions/ms583616(v=vs.100)) con oggetti [Ink](/previous-versions/ms583670(v=vs.100)) per eseguire l'analisi del layout dell'input penna.

Per altre informazioni sull'uso dell'analisi dell'input penna, vedere [L'oggetto divisore](the-divider-object.md).

 

