---
description: Il mapping di rilievo è una forma speciale di mapping dell'ambiente speculare o diffuso che simula i riflessi di oggetti finemente a tessellati senza richiedere un numero estremamente elevato di poligoni.
ms.assetid: 3e195e4f-3fa9-43c4-b2e5-42a6b3aaccf2
title: Bump Mapping (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bb10a3a01ff3b7989cd7c44f95d6980cb08a86c00b3e9a0fc02173e349d4968
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118805831"
---
# <a name="bump-mapping-direct3d-9"></a>Bump Mapping (Direct3D 9)

Il mapping di rilievo è una forma speciale di mapping dell'ambiente speculare o diffuso che simula i riflessi di oggetti finemente a tessellati senza richiedere un numero estremamente elevato di poligoni. Il mapping di urto implementato da Direct3D può essere descritto in modo accurato come perturbazione delle coordinate di trama per pixel di mappe di ambiente speculari o diffuse, perché si forniscono informazioni sul contorno della mappa di rilievo in termini di valori delta, che il sistema si applica alle coordinate di trama di una mappa dell'ambiente nella fase successiva della trama. I valori delta sono codificati nel formato pixel della superficie della mappa di rilievo (vedere [Bump Map Pixel Formats](bump-map-pixel-formats.md)).

Il mapping di urti si basa sulla fusione di più trame. Ciò significa che il dispositivo deve supportare almeno due fasi di fusione. uno per la mappa di rilievo e un altro per una mappa dell'ambiente. Sono necessarie almeno tre fasi di fusione della trama per applicare una mappa di trama di base aggiuntiva, che è il caso più comune. Il diagramma seguente mostra le relazioni tra la trama di base, la mappa di rilievo e la mappa dell'ambiente nella cascata di fusione della trama.

![diagramma della cascata di fusione della trama](images/bumpmap-tcascade.png)

È necessario preparare le fasi della trama in modo appropriato per abilitare il mapping di urto. Gli argomenti seguenti introducono il mapping di rilievo e forniscono informazioni dettagliate su come usarlo nelle applicazioni:

-   [Formati di pixel della mappa in rilievo](bump-map-pixel-formats.md)
-   [Formule di mapping di rilievo](bump-mapping-formulas.md)
-   [Uso di Bump Mapping](using-bump-mapping.md)

Direct3D non supporta in modo nativo le mappe di altezza. si tratta semplicemente di un formato pratico in cui archiviare e visualizzare i dati di contorno. L'applicazione può archiviare le informazioni sui contorni in qualsiasi formato o persino generare una mappa di rilievo procedurale.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Pixel Pipeline](pixel-pipeline.md)
</dt> </dl>

 

 



