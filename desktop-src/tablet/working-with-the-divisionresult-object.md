---
description: L'oggetto DivisionResult rappresenta uno snapshot dell'analisi del layout dei tratti contenuti nell'oggetto Divider. Contiene le informazioni di classificazione e raggruppamento dei tratti dall'analisi del layout.
ms.assetid: 2bcf5223-7bf4-420c-8f04-a972f04f262d
title: Utilizzo dell'oggetto DivisionResult
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b1bb001ecc57c0925253b01b129e0c6fcf0c0243c5a77f0eb697e2cc5c618d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118715071"
---
# <a name="working-with-the-divisionresult-object"></a>Utilizzo dell'oggetto DivisionResult

**L'oggetto DivisionResult** rappresenta uno snapshot dell'analisi del layout dei tratti contenuti nell'oggetto **Divider.** Contiene le informazioni di classificazione e raggruppamento dei tratti dall'analisi del layout.

È possibile ottenere informazioni dall'oggetto **DivisionResult in** base al tipo di elemento strutturale, ad esempio disegno o linee di scrittura manuale. **L'oggetto DivisionResult** può essere mantenuto dopo l'eliminazione dell'oggetto Divider.  In Automazione questo oggetto è denominato [**oggetto interfaccia IInkDivisionResult.**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult)

La [**proprietà Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) dell'oggetto **DivisionResult** contiene una copia della raccolta **Strokes** nell'oggetto **Divider** al momento della creazione dell'oggetto **DivisionResult.**

[**L'enumerazione InkDivisionType**](/windows/win32/api/msinkaut15/ne-msinkaut15-inkdivisiontype) definisce i tipi di elementi strutturali che l'analisi del layout riconosce.

Il [**metodo ResultByType**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-resultbytype) dell'oggetto **DivisionResult** restituisce una **raccolta DivisionUnits** che contiene tutti gli elementi strutturali di un determinato tipo. Un singolo elemento strutturale è rappresentato da un **oggetto DivisionUnit.** Ogni volta che si chiama il **metodo ResultByType,** l'oggetto **DivisionResult** crea una **raccolta DivisionUnits.** Per altre informazioni **sull'oggetto DivisionUnit,** vedere [Utilizzo dell'oggetto DivisionUnit](working-with-the-divisionunit-object.md).

 

 
