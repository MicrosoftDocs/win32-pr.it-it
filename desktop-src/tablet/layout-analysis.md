---
description: L'analisi del layout opera su una raccolta Strokes e classifica i tratti in elementi di scrittura manuale e disegno. L'oggetto Divider consente di accedere alle funzionalità di analisi del layout di Tablet PC.
ms.assetid: ac30d5c2-13a1-4f9e-a519-2bf428e21c75
title: Analisi del layout
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8131859dd7e4c7bd6927db42bd605541001ac0f1222bfbf27b0e59809d4b7bd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119934821"
---
# <a name="layout-analysis"></a>Analisi del layout

L'analisi del layout opera su [**una raccolta Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) e classifica i tratti in elementi di scrittura manuale e disegno. [**L'oggetto Divider**](inkdivider-class.md) consente di accedere alle funzionalità di analisi del layout di Tablet PC.

La tabella seguente descrive i tipi di elementi strutturali [**dell'enumerazione InkDivisionType**](/windows/win32/api/msinkaut15/ne-msinkaut15-inkdivisiontype) in cui l'oggetto [**Divider**](inkdivider-class.md) classifica i tratti.



| Tipo          | Descrizione                                                                      |
|---------------|----------------------------------------------------------------------------------|
| **Segmento**   | Segmento di riconoscimento.<br/>                                                |
| **Linea**      | Riga di grafia che contiene uno o più segmenti di riconoscimento.<br/> |
| **Paragraph** | Blocco di tratti che contiene una o più righe di scrittura manuale.<br/>    |
| **Disegno**   | Input penna non scritto a mano.<br/>                                          |



 

[**L'oggetto Divider**](inkdivider-class.md) ha [**una raccolta Strokes,**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) che l'oggetto **Divider** analizza in modo dinamico ogni volta che si aggiunge o si elimina dalla raccolta. **L'oggetto Divider** non è serializzabile e non è possibile salvarne lo stato di analisi. Di **conseguenza, l'oggetto Divider** è progettato per le applicazioni che devono distinguere tra grafia mista e input di disegno, ma non devono rianare grandi quantità di input penna tra le sessioni.

È possibile ottenere uno snapshot statico del risultato dell'analisi corrente, che viene restituito in un [**oggetto DivisionResult.**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) È possibile ottenere [**oggetti DivisionUnit,**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunit) ognuno dei quali rappresenta un singolo elemento strutturale di un **oggetto DivisionResult.** Gli **oggetti DivisionResult** **e DivisionUnit** non sono serializzabili. Tuttavia, sono disponibili informazioni sullo stato da questi oggetti.

[**L'oggetto Divider**](inkdivider-class.md) funziona solo con la scrittura da sinistra a destra. Perché **l'oggetto Divider** analizzi correttamente le lingue verticali, ad esempio il cinese, i caratteri devono essere disegnati da sinistra a destra anziché dall'alto verso il basso.

 

