---
description: Il file seguente definisce un cubo semplice con quattro lati rossi e due lati verdi. In questo file, le informazioni facoltative vengono utilizzate per aggiungere informazioni all'oggetto dati definito dal modello mesh.
ms.assetid: 310981bf-3536-43dd-ad7c-40ab6c8ef6c4
title: Definizione di un cubo semplice (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9d92d1b97a16e3a26f58281f9621282d3bdc487
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104480725"
---
# <a name="defining-a-simple-cube-direct3d-9"></a><span data-ttu-id="f6bc0-104">Definizione di un cubo semplice (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="f6bc0-104">Defining a Simple Cube (Direct3D 9)</span></span>

<span data-ttu-id="f6bc0-105">Il file seguente definisce un cubo semplice con quattro lati rossi e due lati verdi.</span><span class="sxs-lookup"><span data-stu-id="f6bc0-105">The following file defines a simple cube that has four red sides and two green sides.</span></span> <span data-ttu-id="f6bc0-106">In questo file, le informazioni facoltative vengono utilizzate per aggiungere informazioni all'oggetto dati definito dal modello [**mesh**](mesh.md) .</span><span class="sxs-lookup"><span data-stu-id="f6bc0-106">In this file, optional information is used to add information to the data object defined by the [**Mesh**](mesh.md) template.</span></span>


```
Material RedMaterial {
1.000000;0.000000;0.000000;1.000000;;    // R = 1.0, G = 0.0, B = 0.0
0.000000;
0.000000;0.000000;0.000000;;
0.000000;0.000000;0.000000;;
}

Material GreenMaterial {
0.000000;1.000000;0.000000;1.000000;;     // R = 0.0, G = 1.0, B = 0.0
0.000000;
0.000000;0.000000;0.000000;;
0.000000;0.000000;0.000000;;
}

// Define a mesh with 8 vertices and 12 faces (triangles). Use 
// optional data objects in the mesh to specify materials, normals,
// and texture coordinates.
Mesh CubeMesh {
8;                                // 8 vertices.
1.000000;1.000000;-1.000000;,     // Vertex 0.
-1.000000;1.000000;-1.000000;,    // Vertex 1.
-1.000000;1.000000;1.000000;,     // And so on.
1.000000;1.000000;1.000000;,
1.000000;-1.000000;-1.000000;,
-1.000000;-1.000000;-1.000000;,
-1.000000;-1.000000;1.000000;,
1.000000;-1.000000;1.000000;;

12;                      // 12 faces.
3;0,1,2;,                // Face 0 has three vertices.
3;0,2,3;,                // And so on.
3;0,4,5;,
3;0,5,1;,
3;1,5,6;,
3;1,6,2;,
3;2,6,7;,
3;2,7,3;,
3;3,7,4;,
3;3,4,0;,
3;4,7,6;,
3;4,6,5;;

// All required data has been defined. Now define optional data
// using the hierarchical nature of the file format.
MeshMaterialList {
2;                    // Number of materials used.
12;                   // A material for each face.
0,                    // Face 0 uses the first material.
0,
0,
0,
0,
0,
0,
0,
1,                    // Face 8 uses the second material.
1,
1,
1;;
{RedMaterial}         // References to the definitions
{GreenMaterial}       // of material 0 and 1.
}
MeshNormals {
8;                    // Define 8 normals.
0.333333;0.666667;-0.666667;,
-0.816497;0.408248;-0.408248;,
-0.333333;0.666667;0.666667;,
0.816497;0.408248;0.408248;,
0.666667;-0.666667;-0.333333;,
-0.408248;-0.408248;-0.816497;,
-0.666667;-0.666667;0.333333;,
0.408248;-0.408248;0.816497;;
12;                   // For the 12 faces, define the normals.
3;0,1,2;,
3;0,2,3;,
3;0,4,5;,
3;0,5,1;,
3;1,5,6;,
3;1,6,2;,
3;2,6,7;,
3;2,7,3;,
3;3,7,4;,
3;3,4,0;,
3;4,7,6;,
3;4,6,5;;
}
MeshTextureCoords {
8;                        // Define texture coords for each vertex.
0.000000;1.000000;
1.000000;1.000000;
0.000000;1.000000;
1.000000;1.000000;
0.000000;0.000000;
1.000000;0.000000;
0.000000;0.000000;
1.000000;0.000000;;
}
```



## <a name="related-topics"></a><span data-ttu-id="f6bc0-107">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f6bc0-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6bc0-108">File X (legacy)</span><span class="sxs-lookup"><span data-stu-id="f6bc0-108">X Files (Legacy)</span></span>](x-files--legacy-.md)
</dt> </dl>

 

 



