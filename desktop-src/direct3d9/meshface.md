---
description: Utilizzato dal modello mesh per definire i visi di una rete. Ogni elemento della matrice nFaceVertexIndices fa riferimento a un vertice mesh usato per compilare la faccia.
ms.assetid: 38c40ebe-eca2-4dd9-95b8-b396225e3050
title: MeshFace
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a9e8b73efb214f7a767d986830cccc83ee6cbc1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123444"
---
# <a name="meshface"></a>MeshFace

Utilizzato dal modello [**mesh**](mesh.md) per definire i visi di una rete. Ogni elemento della matrice nFaceVertexIndices fa riferimento a un vertice mesh usato per compilare la faccia.

``` syntax
template MeshFace
{
    < 3D82AB5F-62DA-11cf-AB39-0020AF71E433 >
    DWORD nFaceVertexIndices;
    array DWORD faceVertexIndices[nFaceVertexIndices];
} 
```

Dove:

-   nFaceVertexIndices: numero di indici.
-   Array DWORD faceVertexIndices \[ nFaceVertexIndices \] -matrice di indici.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Modelli](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



