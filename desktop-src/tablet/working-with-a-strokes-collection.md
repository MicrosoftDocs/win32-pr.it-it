---
description: La raccolta Strokes analizzata dall'oggetto divisore viene mantenuta nella proprietà Strokes dell'oggetto divisore.
ms.assetid: c2def964-6f2d-4b79-bfbf-a6719baf3c13
title: Utilizzo di una raccolta Strokes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdeb03ce8168cec489dfed954a091f50f8d846d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306695"
---
# <a name="working-with-a-strokes-collection"></a>Utilizzo di una raccolta Strokes

La raccolta [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) analizzata dall'oggetto [**divisore**](inkdivider-class.md) viene mantenuta nella proprietà [**Strokes**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_strokes) dell'oggetto **divisore** . Poiché una raccolta **Strokes** è un riferimento ai dati di input penna e non è i dati effettivi, le modifiche nell'oggetto [**input penna**](inkdisp-class.md) padre della raccolta **Strokes** possono invalidare la raccolta **Strokes** . Per ulteriori informazioni sui dati Ink, vedere [input penna](ink-data.md). Per altre informazioni sulla raccolta di input penna, vedere [input penna](ink-collection.md).

Per fare in modo che la proprietà [**Strokes**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_strokes) dell'oggetto [**divisore**](inkdivider-class.md) sia sincronizzata con un oggetto [**Ink**](inkdisp-class.md) , usare gli eventi [**InkAdded**](inkdisp-inkadded.md) e [**InkDeleted**](inkdisp-inkdeleted.md) dell'oggetto **Ink** per restare in ascolto dei tratti che devono essere aggiunti o rimossi dall'oggetto **divisore** . Vengono illustrati i casi in cui i tratti vengono aggiunti, eliminati, tagliati o divisi nell'oggetto **input penna** . Lo stato di trasferimento, il ridimensionamento o altre trasformazioni sui tratti nell'oggetto **Ink** non generano eventi **InkAdded** o **InkDeleted** . Per riflettere tale trasformazione nella proprietà **Strokes** dell'oggetto **divisore** , eseguire la stessa trasformazione sui tratti nell'oggetto **divisore** .

La proprietà [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) dell'oggetto [**DivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) contiene una copia dei tratti nell'oggetto [**divisore**](inkdivider-class.md) al momento della creazione dell'oggetto **DivisionResult** . È possibile confrontare le proprietà **Strokes** di due oggetti **DivisionResult** per determinare se i tratti sono stati modificati tra le due volte in cui è stato chiamato il metodo [**divide**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-divide) .

La proprietà [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionunit-get_strokes) dell'oggetto [**DivisionUnit**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunit) contiene il subset dei tratti nell'oggetto [**DivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) che corrispondono a questo elemento. È possibile passare questi tratti a un oggetto [**RecognizerContext**](inkrecognizercontext-class.md) separato per ottenere un risultato di riconoscimento per l'elemento. Poiché gli elementi di grafia esistono a diversi livelli di dettaglio, le raccolte di [**tratti**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) per diversi elementi possono sovrapporsi. Ad esempio, la raccolta **Strokes** per un elemento del segmento di riconoscimento sarà un subset della raccolta **Strokes** per l'elemento line di cui fa parte il segmento di riconoscimento.

 

 
