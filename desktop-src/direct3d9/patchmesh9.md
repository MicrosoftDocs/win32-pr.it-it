---
description: Definisce una mesh definita dalle patch di Bézier. La prima matrice è un elenco di vertici e la seconda matrice definisce le patch per la mesh mediante l'indicizzazione nella matrice di vertici.
ms.assetid: 642ca513-c83e-4c6d-845c-0eaecc232728
title: PatchMesh9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b3d8232fe8c83358feb216acfb45a7877d7acb9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304384"
---
# <a name="patchmesh9"></a>PatchMesh9

Definisce una mesh definita dalle patch di Bézier. La prima matrice è un elenco di vertici e la seconda matrice definisce le patch per la mesh mediante l'indicizzazione nella matrice di vertici.

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

-   Type-patch mesh Type: Rectangle, Triangle o N-patch.
-   Grado di grado delle variabili nell'equazione della curva.
-   Base: tipo di base di una superficie di patch di ordine superiore.
-   nVertices: numero di vertici.
-   vertici \[ nVertices \] : matrice di vertici. Vedere [**vector**](vector.md).
-   nPatches: numero di patch.
-   patch \[ nPatches \] : matrice di patch. Vedere [**patch**](patch.md).
-   \[ ... \] -È possibile usare qualsiasi modello di file con estensione x. Questa operazione rende l'architettura estendibile.

Le patch usano i vertici nella matrice di vertici come punti di controllo per ogni patch.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Modelli](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



