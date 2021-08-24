---
description: PatchMesh definisce una mesh definita dalle patch di Bézier, incluso un elenco di vertici e le patch per la mesh tramite l'indicizzazione nella matrice dei vertici.
ms.assetid: vs|directx_sdk|~\patchmesh.htm
title: PatchMesh
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b3bc3c243fb42014ba18aac134ea008d5818e249a601858be6724d5a0fd7310
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746921"
---
# <a name="patchmesh"></a>PatchMesh

Definisce una mesh definita dalle patch di Bézier. La prima matrice è un elenco di vertici e la seconda definisce le patch per la mesh tramite l'indicizzazione nella matrice dei vertici.

``` syntax
template PatchMesh
{
    < D02C95CC-EDBA-4305-9B5D-1820D7704BBF >
    DWORD nVertices;
    array Vector vertices[nVertices];
    DWORD nPatches;
    array Patch patches[nPatches];
    [ ... ]
}
```

Dove:

-   nVertices : numero di vertici.
-   vertices \[ nVertices \] - Matrice di vertici. Vedere [**Vettore**](vector.md).
-   nPatches : numero di patch.
-   patches \[ nPatches \] - Matrice di patch. Vedere [**Patch**](patch.md).
-   \[ ... \] - Qui è possibile usare qualsiasi modello di file con estensione x. In questo modo l'architettura è estensibile.

Le patch usano i vertici nella matrice di vertici come punti di controllo per ogni patch. Si tratta di un modello legacy. Il modello di mesh patch più recente è [**PatchMesh9.**](patchmesh9.md)

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Modelli](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



