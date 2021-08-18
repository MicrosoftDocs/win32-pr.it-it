---
description: L'oggetto Divider consente di accedere alle funzionalità di analisi del layout di Tablet PC.
ms.assetid: 9fa299fe-3713-4fa8-95c6-be15f144103a
title: Uso dell'oggetto Divisore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a31c7ab0c99c0ac4007abe164a887694c8e41fb8c8892dfe2637efaf25b10f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966570"
---
# <a name="working-with-the-divider-object"></a>Uso dell'oggetto Divisore

[L'oggetto Divider](/previous-versions/ms583616(v=vs.100)) consente di accedere alle funzionalità di analisi del layout di Tablet PC.

Nel codice gestito è possibile creare [un'istanza](/previous-versions/ms583616(v=vs.100)) dell'oggetto Divider chiamando uno dei costruttori [divider.](/previous-versions/ms839465(v=msdn.10)) In Automazione si chiama [**l'oggetto InkDivider**](inkdivider-class.md) e può essere creata un'istanza chiamando il metodo [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) in C++.

È possibile ottenere uno snapshot del risultato dell'analisi corrente chiamando il [metodo Divide](/previous-versions/ms839461(v=msdn.10)) dell'oggetto [Divider.](/previous-versions/ms583616(v=vs.100)) Il risultato dell'analisi viene restituito in [un oggetto DivisionResult.](/previous-versions/ms839371(v=msdn.10)) Ogni volta che si chiama il metodo Divide, l'oggetto Divider crea un oggetto DivisionResult. Per altre informazioni sull'oggetto DivisionResult, vedere [Utilizzo dell'oggetto DivisionResult](working-with-the-divisionresult-object.md).

La [raccolta Strokes](/previous-versions/ms552701(v=vs.100)) analizzata [dall'oggetto Divider](/previous-versions/ms583616(v=vs.100)) è contenuta nella [proprietà Strokes](/previous-versions/ms839422(v=msdn.10)) dell'oggetto Divider. L'oggetto Divider analizza in modo dinamico la raccolta Strokes durante l'aggiunta o l'eliminazione dalla raccolta. Per altre informazioni sulla proprietà Strokes dell'oggetto Divider, vedere [Utilizzo di una raccolta Strokes](working-with-a-strokes-collection.md).

[L'oggetto Divider](/previous-versions/ms583616(v=vs.100)) usa un contesto di riconoscimento per migliorare l'analisi dei segmenti di riconoscimento e per generare il testo di riconoscimento per gli elementi di scrittura manuale. È possibile impostare il contesto del riconoscimento usando la [proprietà RecognizerContext](/previous-versions/ms839415(v=msdn.10)) dell'oggetto Divider. La proprietà RecognizerContext non può essere modificata dopo che i tratti sono stati assegnati all'oggetto Divider. Per altre informazioni sulla proprietà RecognizerContext dell'oggetto Divider, vedere [Uso di un contesto di riconoscimento](working-with-a-recognizer-context.md).

> [!Caution]  
> Nel codice gestito, è necessario chiamare il [metodo Dispose](/previous-versions/ms839450(v=msdn.10)) su questo oggetto prima che eserviti l'ambito. Questo oggetto gestisce risorse non gestite. L'attendibilità della finalizzazione per questo oggetto può causare perdite di memoria ed eccezioni all'interno dell'applicazione.

 

 

 
