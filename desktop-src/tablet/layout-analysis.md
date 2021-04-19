---
description: L'analisi del layout opera su una raccolta Strokes e classifica i tratti in elementi di grafia e disegno. L'oggetto divisore consente di accedere alle funzionalità di analisi del layout di Tablet PC.
ms.assetid: ac30d5c2-13a1-4f9e-a519-2bf428e21c75
title: Analisi del layout
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0901e7c7df96bec5ea3972f643469033fbb22ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313448"
---
# <a name="layout-analysis"></a>Analisi del layout

L'analisi del layout opera su una raccolta [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) e classifica i tratti in elementi di grafia e disegno. L'oggetto [**divisore**](inkdivider-class.md) consente di accedere alle funzionalità di analisi del layout di Tablet PC.

Nella tabella seguente vengono descritti i tipi di elementi strutturali dell'enumerazione [**InkDivisionType**](/windows/win32/api/msinkaut15/ne-msinkaut15-inkdivisiontype) in cui l'oggetto [**divisore**](inkdivider-class.md) classifica i tratti.



| Tipo          | Descrizione                                                                      |
|---------------|----------------------------------------------------------------------------------|
| **Segmento**   | Segmento di riconoscimento.<br/>                                                |
| **Linea**      | Riga di grafia che contiene uno o più segmenti di riconoscimento.<br/> |
| **Paragraph** | Un blocco di tratti che contiene una o più righe di grafia.<br/>    |
| **Disegno**   | Input penna che non è a grafia.<br/>                                          |



 

L' **oggetto** [**divisore**](inkdivider-class.md) dispone di una raccolta [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) , che viene analizzata dinamicamente ogni volta che si aggiunge o si elimina dalla raccolta. L'oggetto **divisore** non è serializzabile e non è possibile salvarne lo stato di analisi. Di conseguenza, l'oggetto **divisore** è progettato per le applicazioni che devono distinguere tra input grafia misto e input di disegno, ma non è necessario analizzare nuovamente grandi quantità di input penna tra le sessioni.

È possibile ottenere uno snapshot statico del risultato dell'analisi corrente, restituito in un oggetto [**DivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) . È possibile ottenere oggetti [**DivisionUnit**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunit) , ognuno dei quali rappresenta un singolo elemento strutturale di un oggetto **DivisionResult** . Gli oggetti **DivisionResult** e **DivisionUnit** non sono serializzabili. Tuttavia, le informazioni sullo stato di questi oggetti sono disponibili.

L'oggetto [**divisore**](inkdivider-class.md) funziona solo con la grafia da sinistra a destra. Affinché l'oggetto **divisore** analizzi correttamente le lingue verticali, ad esempio il cinese, i caratteri devono essere disegnati da sinistra a destra anziché dall'alto verso il basso.

 

