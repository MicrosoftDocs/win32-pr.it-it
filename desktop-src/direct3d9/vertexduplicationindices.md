---
description: "VertexDuplicationIndices: viene creata un'istanza di questo modello per ogni mesh, che contiene informazioni sui vertici nella mesh duplicati l'uno dell'altro."
ms.assetid: 43417389-69c1-4af6-92c2-75b621f9c165
title: VertexDuplicationIndices
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b33a8c5fca4f479eec6e9864d4528d4e3e4a1e32
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090179"
---
# <a name="vertexduplicationindices"></a>VertexDuplicationIndices

Viene creata un'istanza di questo modello per ogni mesh, che contiene informazioni sui vertici nella mesh duplicati l'uno dell'altro. I duplicati si verificano quando un vertice si trova su un gruppo di smussamento o un limite materiale. Lo scopo di questo modello è consentire al caricatore di determinare quali vertici che presentano parametri periferici diversi sono effettivamente gli stessi vertici nel modello. Alcune applicazioni ,ad esempio la semplificazione della mesh, possono usare queste informazioni.

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

-   nIndices: numero di indici dei vertici. Questo è il numero di vertici nella mesh.
-   nOriginalVertices: numero di vertici nella mesh prima che si verifichi qualsiasi duplicazione.
-   Gli indici di valore n contiene l'indice dei vertici che il vertice n nella matrice dei vertici per la mesh avrebbe avuto se non fosse stata \[ \] \[ \] verificata alcuna duplicazione. Gli indici in questa matrice che sono gli stessi, pertanto, indicano vertici duplicati.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Modelli](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



