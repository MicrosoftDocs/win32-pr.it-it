---
description: Definisce una mesh definita dalle patch di Bézier. La prima matrice è un elenco di vertici e la seconda matrice definisce le patch per la mesh mediante l'indicizzazione nella matrice di vertici.
ms.assetid: vs|directx_sdk|~\patchmesh.htm
title: PatchMesh
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fcdefac9799736c796aef7cbb7222ab1942540d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520890"
---
# <a name="patchmesh"></a>PatchMesh

Definisce una mesh definita dalle patch di Bézier. La prima matrice è un elenco di vertici e la seconda matrice definisce le patch per la mesh mediante l'indicizzazione nella matrice di vertici.

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
-   vertici \[ nVertices \] : matrice di vertici. Vedere [**vector**](vector.md).
-   nPatches: numero di patch.
-   patch \[ nPatches \] : matrice di patch. Vedere [**patch**](patch.md).
-   \[ ... \] -È possibile usare qualsiasi modello di file con estensione x. Questa operazione rende l'architettura estendibile.

Le patch usano i vertici nella matrice di vertici come punti di controllo per ogni patch. Si tratta di un modello legacy. Il modello mesh patch più recente è [**PatchMesh9**](patchmesh9.md).

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Modelli](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



