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
# <a name="meshnormals"></a><span data-ttu-id="27c51-103">MeshNormals</span><span class="sxs-lookup"><span data-stu-id="27c51-103">MeshNormals</span></span>

<span data-ttu-id="27c51-104">Definisce le normali per una mesh.</span><span class="sxs-lookup"><span data-stu-id="27c51-104">Defines normals for a mesh.</span></span> <span data-ttu-id="27c51-105">La prima matrice di vettori è costituita dai normali vettori e la seconda matrice è una matrice di indici che specifica quali normali devono essere applicati a una determinata faccia.</span><span class="sxs-lookup"><span data-stu-id="27c51-105">The first array of vectors is the normal vectors themselves, and the second array is an array of indexes specifying which normals should be applied to a given face.</span></span> <span data-ttu-id="27c51-106">Il valore del membro nFaceNormals deve essere uguale al numero di visi in una mesh.</span><span class="sxs-lookup"><span data-stu-id="27c51-106">The value of the nFaceNormals member should be equal to the number of faces in a mesh.</span></span>

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

<span data-ttu-id="27c51-107">Dove:</span><span class="sxs-lookup"><span data-stu-id="27c51-107">Where:</span></span>

-   <span data-ttu-id="27c51-108">nNormals: numero di normali.</span><span class="sxs-lookup"><span data-stu-id="27c51-108">nNormals - Number of normals.</span></span>
-   <span data-ttu-id="27c51-109">Vettore di matrice Normals \[ nNormals \] : matrice di normali.</span><span class="sxs-lookup"><span data-stu-id="27c51-109">array Vector normals\[nNormals\] - Array of normals.</span></span> <span data-ttu-id="27c51-110">Vedere [**vector**](vector.md).</span><span class="sxs-lookup"><span data-stu-id="27c51-110">See [**Vector**](vector.md).</span></span>
-   <span data-ttu-id="27c51-111">nFaceNormals-numero di normali facciali.</span><span class="sxs-lookup"><span data-stu-id="27c51-111">nFaceNormals - Number of face normals.</span></span>
-   <span data-ttu-id="27c51-112">Array MeshFace faceNormals \[ nFaceNormals \] -Array of Mesh Face Normals.</span><span class="sxs-lookup"><span data-stu-id="27c51-112">array MeshFace faceNormals\[nFaceNormals\] - Array of mesh face normals.</span></span> <span data-ttu-id="27c51-113">Vedere [**MeshFace**](meshface.md).</span><span class="sxs-lookup"><span data-stu-id="27c51-113">See [**MeshFace**](meshface.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="27c51-114">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="27c51-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27c51-115">Modelli</span><span class="sxs-lookup"><span data-stu-id="27c51-115">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



