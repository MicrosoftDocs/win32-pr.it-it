---
description: Definisce una mesh semplice. La prima matrice è un elenco di vertici e la seconda matrice definisce i visi della mesh mediante l'indicizzazione nella matrice di vertici.
ms.assetid: vs|directx_sdk|~\mesh.htm
title: Mesh
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ced60785a5f013db7fc26e4d203119a160953b65
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104480700"
---
# <a name="mesh"></a>Mesh

Definisce una mesh semplice. La prima matrice è un elenco di vertici e la seconda matrice definisce i visi della mesh mediante l'indicizzazione nella matrice di vertici.

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
-   vertici del vettore di matrice \[ nVertices \] : matrice di vertici, ognuno di tipo Vector. Vedere [**vector**](vector.md).
-   nFaces: numero di visi.
-   Array MeshFace Faces \[ nFaces \] -Array of visi, ognuno di tipo MeshFace. Vedere [**MeshFace**](meshface.md).
-   \[ ... \] -È possibile usare qualsiasi modello di file con estensione x. Questa operazione rende l'architettura estendibile. I modelli [**Material**](material.md) e [**TextureFilename**](texturefilename.md) vengono in genere utilizzati.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Modelli](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



