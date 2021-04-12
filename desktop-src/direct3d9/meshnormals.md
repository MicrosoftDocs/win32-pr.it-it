---
description: Definisce le normali per una mesh.
ms.assetid: 05f17128-dfc9-4a78-b23c-0420a1c3d1bd
title: MeshNormals
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65b9e0ffc89af5a0a55ef7bd1fa2575a4943137e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104225423"
---
# <a name="meshnormals"></a>MeshNormals

Definisce le normali per una mesh. La prima matrice di vettori è costituita dai normali vettori e la seconda matrice è una matrice di indici che specifica quali normali devono essere applicati a una determinata faccia. Il valore del membro nFaceNormals deve essere uguale al numero di visi in una mesh.

``` syntax
template MeshNormals
{
    < F6F23F43-7686-11cf-8F52-0040333594A3 >
    DWORD nNormals;
    array Vector normals[nNormals];
    DWORD nFaceNormals;
    array MeshFace faceNormals[nFaceNormals];
} 
```

Dove:

-   nNormals: numero di normali.
-   Vettore di matrice Normals \[ nNormals \] : matrice di normali. Vedere [**vector**](vector.md).
-   nFaceNormals-numero di normali facciali.
-   Array MeshFace faceNormals \[ nFaceNormals \] -Array of Mesh Face Normals. Vedere [**MeshFace**](meshface.md).

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Modelli](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



