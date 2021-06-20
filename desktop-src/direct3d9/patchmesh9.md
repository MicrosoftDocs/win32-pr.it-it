---
description: PatchMesh9 definisce una mesh definita dalle patch di Bézier, incluso un elenco di vertici e le patch per la mesh tramite l'indicizzazione nella matrice di vertici.
ms.assetid: 642ca513-c83e-4c6d-845c-0eaecc232728
title: PatchMesh9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 811e593117f2ec57a4718ea8078d96bcea87e71f
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404704"
---
# <a name="patchmesh9"></a>PatchMesh9

Definisce una mesh definita dalle patch di Bézier. La prima matrice è un elenco di vertici e la seconda definisce le patch per la mesh tramite l'indicizzazione nella matrice dei vertici.

``` syntax
template PatchMesh9
{
    < B9EC94E1-B9A6-4251-BA18-94893F02C0EA >
    DWORD Type;
    DWORD Degree;
    DWORD Basis;
    DWORD nVertices;
    array Vector vertices[nVertices];
    DWORD nPatches;
    array Patch patches[nPatches];
    [ ... ]
} 
```

Dove:

-   Tipo - Tipo di mesh patch: rettangolo, triangolo o N-patch.
-   Grado: grado delle variabili nell'equazione della curva.
-   Base: tipo di base di una superficie patch di ordine elevato.
-   nVertices : numero di vertici.
-   vertices \[ nVertices \] - Matrice di vertici. Vedere [**Vettore**](vector.md).
-   nPatches : numero di patch.
-   patches \[ nPatches \] - Matrice di patch. Vedere [**Patch**](patch.md).
-   \[ ... \] - Qui è possibile usare qualsiasi modello di file con estensione x. In questo modo l'architettura è estensibile.

Le patch usano i vertici nella matrice di vertici come punti di controllo per ogni patch.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Modelli](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



