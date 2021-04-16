---
description: L'oggetto DivisionResult rappresenta uno snapshot dell'analisi del layout dei tratti contenuti dall'oggetto divisore. Contiene le informazioni di raggruppamento e classificazione tratto dall'analisi del layout.
ms.assetid: 2bcf5223-7bf4-420c-8f04-a972f04f262d
title: Utilizzo dell'oggetto DivisionResult
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0b9874f4a9d2e6bc4390d98803c2344308fc3e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526887"
---
# <a name="working-with-the-divisionresult-object"></a>Utilizzo dell'oggetto DivisionResult

L'oggetto **DivisionResult** rappresenta uno snapshot dell'analisi del layout dei tratti contenuti dall'oggetto **divisore** . Contiene le informazioni di raggruppamento e classificazione tratto dall'analisi del layout.

È possibile ottenere informazioni dall'oggetto **DivisionResult** in base al tipo di elemento strutturale, ad esempio disegno o righe di grafia. L'oggetto **DivisionResult** può essere mantenuto dopo che l'oggetto **divisore** è stato eliminato definitivamente. In automazione, questo oggetto viene chiamato oggetto [**interfaccia IInkDivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) .

La proprietà [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) dell'oggetto **DivisionResult** contiene una copia della raccolta **Strokes** nell'oggetto **divisore** al momento della creazione dell'oggetto **DivisionResult** .

L'enumerazione [**InkDivisionType**](/windows/win32/api/msinkaut15/ne-msinkaut15-inkdivisiontype) definisce i tipi di elementi strutturali riconosciuti dall'analisi del layout.

Il metodo [**ResultByType**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-resultbytype) dell'oggetto **DivisionResult** restituisce una raccolta **DivisionUnits** che contiene tutti gli elementi strutturali di un tipo specificato. Un singolo elemento strutturale è rappresentato da un oggetto **DivisionUnit** . Ogni volta che si chiama il metodo **ResultByType** , l'oggetto **DivisionResult** crea una raccolta **DivisionUnits** . Per ulteriori informazioni sull'oggetto **DivisionUnit** , vedere [utilizzo dell'oggetto DivisionUnit](working-with-the-divisionunit-object.md).

 

 
