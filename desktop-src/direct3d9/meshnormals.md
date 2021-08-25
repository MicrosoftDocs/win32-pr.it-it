---
description: Definisce le normali per una mesh.
ms.assetid: 05f17128-dfc9-4a78-b23c-0420a1c3d1bd
title: MeshNormals
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02a261dd8dbd46cf26116657b983eca4f693603869a80bf2fb110c0f165221ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119846461"
---
# <a name="meshnormals"></a>MeshNormals

Definisce le normali per una mesh. La prima matrice di vettori è i vettori normali stessi e la seconda matrice è una matrice di indici che specifica quali normali devono essere applicate a un determinato viso. Il valore del membro nFaceNormals deve essere uguale al numero di visi in una mesh.

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

-   nNormals : numero di normali.
-   array Vector normals \[ nNormals \] : matrice di normali. Vedere [**Vettore**](vector.md).
-   nFaceNormals : numero di normali del viso.
-   array MeshFace faceNormals \[ nFaceNormals \] : matrice di normali del viso mesh. Vedere [**MeshFace**](meshface.md).

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Modelli](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



