---
description: PatchMesh definisce una mesh definita dalle patch di Bézier, incluso un elenco di vertici e le patch per la mesh tramite l'indicizzazione nella matrice dei vertici.
ms.assetid: vs|directx_sdk|~\patchmesh.htm
title: PatchMesh
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fabb3846246c7fb76a7146baf0b30bd9730fe24b
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404714"
---
# <a name="patchmesh"></a>PatchMesh

Definisce una mesh definita dalle patch di Bézier. La prima matrice è un elenco di vertici e la seconda matrice definisce le patch per la mesh tramite l'indicizzazione nella matrice dei vertici.

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

-   nVertices: numero di vertici.
-   vertices \[ nVertices \] : matrice di vertici. Vedere [**Vector.**](vector.md)
-   nPatches: numero di patch.
-   patches \[ nPatches \] : matrice di patch. Vedere [**Patch**](patch.md).
-   \[ ... \] - Qui è possibile usare qualsiasi modello di file con estensione x. In questo modo l'architettura è estensibile.

Le patch usano i vertici nella matrice di vertici come punti di controllo per ogni patch. Si tratta di un modello legacy. Il modello patch mesh più recente è [**PatchMesh9.**](patchmesh9.md)

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Modelli](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



