---
description: Definisce una mesh semplice. La prima matrice è un elenco di vertici e la seconda matrice definisce le visi della mesh tramite l'indicizzazione nella matrice dei vertici.
ms.assetid: vs|directx_sdk|~\mesh.htm
title: Mesh
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4ce4cf6fb6a3eee3417a7d0fe1594164c1e22df9d118f4f995955f8070fc015
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119240741"
---
# <a name="mesh"></a>Mesh

Definisce una mesh semplice. La prima matrice è un elenco di vertici e la seconda matrice definisce le visi della mesh tramite l'indicizzazione nella matrice dei vertici.

``` syntax
template Mesh
{
    <3D82AB44-62DA-11CF-AB39-0020AF71E433>
    DWORD nVertices;
    array Vector vertices[nVertices];
    DWORD nFaces;
    array MeshFace faces[nFaces];
    [...]
}
```

Dove:

-   nVertices: numero di vertici.
-   array Vector vertices \[ nVertices \] : matrice di vertici, ognuno di tipo Vector. Vedere [**Vector.**](vector.md)
-   nFaces: numero di visi.
-   array MeshFace faces \[ nFaces \] : matrice di visi, ognuno di tipo MeshFace. Vedere [**MeshFace.**](meshface.md)
-   \[ ... \] - Qui è possibile usare qualsiasi modello di file con estensione x. In questo modo l'architettura è estensibile. [**Vengono in**](material.md) genere usati i modelli Material [**e TextureFilename.**](texturefilename.md)

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Modelli](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



