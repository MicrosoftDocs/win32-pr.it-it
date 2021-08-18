---
description: La raccolta Strokes analizzata dall'oggetto Divider viene mantenuta nella proprietà Strokes dell'oggetto Divider.
ms.assetid: c2def964-6f2d-4b79-bfbf-a6719baf3c13
title: Uso di una raccolta Strokes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35673ef17882f246969e7c74869f47b09b604195c74bb1456c3624713a42045d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119221871"
---
# <a name="working-with-a-strokes-collection"></a>Uso di una raccolta Strokes

La [**raccolta Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) analizzata [**dall'oggetto Divider**](inkdivider-class.md) viene mantenuta nella [**proprietà Strokes**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_strokes) dell'oggetto **Divider.** Poiché una **raccolta Strokes** è un riferimento ai dati dell'input penna e non sono i dati effettivi, le modifiche nell'oggetto [**Ink**](inkdisp-class.md) padre della raccolta **Strokes** possono invalidare la **raccolta Strokes.** Per altre informazioni sui dati dell'input penna, vedere [Dati input penna](ink-data.md). Per altre informazioni sulla raccolta di input penna, vedere [Raccolta input penna](ink-collection.md).

Per mantenere sincronizzata la proprietà [**Strokes**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_strokes) dell'oggetto [**Divider**](inkdivider-class.md) con un oggetto [**Ink,**](inkdisp-class.md) usare gli eventi [**InkAdded**](inkdisp-inkadded.md) e [**InkDeleted**](inkdisp-inkdeleted.md) dell'oggetto **Ink** per restare in ascolto dei tratti che devono essere aggiunti o rimossi dall'oggetto **Divider.** Vengono illustrati i casi in cui i tratti vengono aggiunti, eliminati, ritagliati o suddivisi all'interno **dell'oggetto Ink.** Lo spostamento, il ridimensionamento o altre trasformazioni sui tratti nell'oggetto **Ink** non generano eventi **InkAdded** **o InkDeleted.** Per riflettere una trasformazione di questo tipo nella proprietà **Strokes** dell'oggetto **Divider,** eseguire la stessa trasformazione sui tratti nell'oggetto **Divider.**

La [**proprietà Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) dell'oggetto [**DivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) contiene una copia dei tratti nell'oggetto [**Divider**](inkdivider-class.md) al momento della creazione dell'oggetto **DivisionResult.** È possibile confrontare **le proprietà Strokes** di due **oggetti DivisionResult** per determinare se i tratti sono stati modificati tra le due volte in cui è stato chiamato il metodo Divide. [](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-divide)

La [**proprietà Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionunit-get_strokes) dell'oggetto [**DivisionUnit**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunit) contiene il subset dei tratti nell'oggetto [**DivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) che corrispondono a questo elemento. È possibile passare questi tratti a un [**recognizerContext**](inkrecognizercontext-class.md) separato per ottenere un risultato di riconoscimento per l'elemento. Poiché gli elementi di scrittura manuale esistono a diversi livelli di dettaglio, le [**raccolte Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) per elementi diversi possono sovrapporsi. Ad esempio, la **raccolta Strokes** per un elemento segmento di riconoscimento sarà un subset della raccolta **Strokes** per l'elemento linea di cui il segmento di riconoscimento fa parte.

 

 
