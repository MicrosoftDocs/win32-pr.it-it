---
description: "VertexDuplicationIndices: viene creata un'istanza di questo modello per ogni mesh, che contiene informazioni sui vertici nella mesh duplicati l'uno dell'altro."
ms.assetid: 43417389-69c1-4af6-92c2-75b621f9c165
title: VertexDuplicationIndices
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a9ac9b43e0aa05d75727e24bb4677ef0b21fcb41366800185551c48f5fb76f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118290336"
---
# <a name="vertexduplicationindices"></a>VertexDuplicationIndices

Viene creata un'istanza di questo modello per ogni mesh, che contiene informazioni sui vertici nella mesh duplicati l'uno dell'altro. I duplicati vengono restituiti quando un vertice si trova su un gruppo di smussamento o un limite di materiale. Lo scopo di questo modello è consentire al caricatore di determinare quali vertici che presentano parametri periferici diversi sono in realtà gli stessi vertici nel modello. Alcune applicazioni ,ad esempio la semplificazione della mesh, possono usare queste informazioni.

``` syntax
template VertexDuplicationIndices 
{ 
    < B8D65549-D7C9-4995-89CF-53A9A8B031E3 > 
    DWORD nIndices; 
    DWORD nOriginalVertices; 
    array DWORD indices[nIndices]; 
}
```

Dove:

-   nIndices : numero di indici dei vertici. Questo è il numero di vertici nella mesh.
-   nOriginalVertices: numero di vertici nella mesh prima che si verifichi una duplicazione.
-   Il valore indice n contiene l'indice dei vertici che vertex n nella matrice dei vertici per la mesh avrebbe avuto se non si fosse verificata \[ \] alcuna \[ \] duplicazione. Gli indici in questa matrice che sono gli stessi, pertanto, indicano vertici duplicati.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Modelli](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



