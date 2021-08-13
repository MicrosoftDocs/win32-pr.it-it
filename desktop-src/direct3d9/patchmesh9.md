---
description: PatchMesh9 definisce una mesh definita dalle patch di Bézier, incluso un elenco di vertici e le patch per la mesh tramite l'indicizzazione nella matrice dei vertici.
ms.assetid: 642ca513-c83e-4c6d-845c-0eaecc232728
title: PatchMesh9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20216bcfa33c3e3ef36dea999a6fef10384719254f4874a1da3907aa02551a3a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118798537"
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

 

 



