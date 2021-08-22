---
description: Usato dal modello Mesh per definire i visi di una mesh. Ogni elemento della matrice nFaceVertexIndices fa riferimento a un vertice mesh usato per creare il viso.
ms.assetid: 38c40ebe-eca2-4dd9-95b8-b396225e3050
title: MeshFace
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83ea35d1db9e33644638455bc42cc2cbef320f748d96b086037dea6f10607dbe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119563531"
---
# <a name="meshface"></a>MeshFace

Usato dal modello [**Mesh**](mesh.md) per definire i visi di una mesh. Ogni elemento della matrice nFaceVertexIndices fa riferimento a un vertice mesh usato per creare il viso.

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
-   array DWORD faceVertexIndices \[ nFaceVertexIndices \] - Matrice di indici.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Modelli](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



