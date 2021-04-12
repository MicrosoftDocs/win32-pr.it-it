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
# <a name="mesh"></a><span data-ttu-id="df163-104">Mesh</span><span class="sxs-lookup"><span data-stu-id="df163-104">Mesh</span></span>

<span data-ttu-id="df163-105">Definisce una mesh semplice.</span><span class="sxs-lookup"><span data-stu-id="df163-105">Defines a simple mesh.</span></span> <span data-ttu-id="df163-106">La prima matrice è un elenco di vertici e la seconda matrice definisce i visi della mesh mediante l'indicizzazione nella matrice di vertici.</span><span class="sxs-lookup"><span data-stu-id="df163-106">The first array is a list of vertices, and the second array defines the faces of the mesh by indexing into the vertex array.</span></span>

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

<span data-ttu-id="df163-107">Dove:</span><span class="sxs-lookup"><span data-stu-id="df163-107">Where:</span></span>

-   <span data-ttu-id="df163-108">nVertices: numero di vertici.</span><span class="sxs-lookup"><span data-stu-id="df163-108">nVertices - Number of vertices.</span></span>
-   <span data-ttu-id="df163-109">vertici del vettore di matrice \[ nVertices \] : matrice di vertici, ognuno di tipo Vector.</span><span class="sxs-lookup"><span data-stu-id="df163-109">array Vector vertices\[nVertices\] - Array of vertices, each of type Vector.</span></span> <span data-ttu-id="df163-110">Vedere [**vector**](vector.md).</span><span class="sxs-lookup"><span data-stu-id="df163-110">See [**Vector**](vector.md).</span></span>
-   <span data-ttu-id="df163-111">nFaces: numero di visi.</span><span class="sxs-lookup"><span data-stu-id="df163-111">nFaces - Number of faces.</span></span>
-   <span data-ttu-id="df163-112">Array MeshFace Faces \[ nFaces \] -Array of visi, ognuno di tipo MeshFace.</span><span class="sxs-lookup"><span data-stu-id="df163-112">array MeshFace faces\[nFaces\] - Array of faces, each of type MeshFace.</span></span> <span data-ttu-id="df163-113">Vedere [**MeshFace**](meshface.md).</span><span class="sxs-lookup"><span data-stu-id="df163-113">See [**MeshFace**](meshface.md).</span></span>
-   <span data-ttu-id="df163-114">\[ ... \] -È possibile usare qualsiasi modello di file con estensione x.</span><span class="sxs-lookup"><span data-stu-id="df163-114">\[ ... \] - Any .x file template can be used here.</span></span> <span data-ttu-id="df163-115">Questa operazione rende l'architettura estendibile.</span><span class="sxs-lookup"><span data-stu-id="df163-115">This makes the architecture extensible.</span></span> <span data-ttu-id="df163-116">I modelli [**Material**](material.md) e [**TextureFilename**](texturefilename.md) vengono in genere utilizzati.</span><span class="sxs-lookup"><span data-stu-id="df163-116">[**Material**](material.md) and [**TextureFilename**](texturefilename.md) templates are typically used.</span></span>

## <a name="see-also"></a><span data-ttu-id="df163-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="df163-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df163-118">Modelli</span><span class="sxs-lookup"><span data-stu-id="df163-118">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



