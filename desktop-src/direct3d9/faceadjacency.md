---
description: "FaceAdjacency: viene creata un'istanza di questo modello per ogni mesh, che contiene informazioni sui vertici nella mesh duplicati l'uno dell'altro."
ms.assetid: dd30b3d6-767a-4d87-9b5c-1324738bcbb2
title: FaceAdjacency
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0508b822f45c6796a793dc4b17caeaa1e30b4c3d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090509"
---
# <a name="faceadjacency"></a>FaceAdjacency

Viene creata un'istanza di questo modello per ogni mesh, che contiene informazioni sui vertici nella mesh duplicati l'uno dell'altro. I duplicati vengono restituiti quando un vertice si trova su un gruppo di arrotondamento o un limite di materiale. Lo scopo di questo modello è consentire al caricatore di determinare quali vertici che presentano parametri periferici diversi sono in realtà gli stessi vertici nel modello. Alcune applicazioni ,ad esempio la semplificazione della mesh, possono usare queste informazioni.

``` syntax
template FaceAdjacency
{
    < A64C844A-E282-4756-8B80-250CDE04398C >
    DWORD nIndices;
    array DWORD indices[nIndices];
} 
```

Dove:

-   nIndices : numero di indici nella mesh.
-   indici \[ nIndices \] : matrice di indici.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Modelli](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



