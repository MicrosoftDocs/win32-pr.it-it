---
description: Utilizzato in un oggetto mesh per specificare il materiale da applicare ai visi. Il membro nMaterials specifica il numero di materiali presenti e i materiali specificano il materiale da applicare.
ms.assetid: b38fd445-1a31-41ed-abbe-084abfe1c221
title: MeshMaterialList
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b746802dc3ef54a8feacc8ddfdaa0db1e45112b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303721"
---
# <a name="meshmateriallist"></a><span data-ttu-id="e4184-104">MeshMaterialList</span><span class="sxs-lookup"><span data-stu-id="e4184-104">MeshMaterialList</span></span>

<span data-ttu-id="e4184-105">Utilizzato in un oggetto mesh per specificare il materiale da applicare ai visi.</span><span class="sxs-lookup"><span data-stu-id="e4184-105">Used in a mesh object to specify which material applies to which faces.</span></span> <span data-ttu-id="e4184-106">Il membro nMaterials specifica il numero di materiali presenti e i materiali specificano il materiale da applicare.</span><span class="sxs-lookup"><span data-stu-id="e4184-106">The nMaterials member specifies how many materials are present, and materials specify which material to apply.</span></span>

``` syntax
template MeshMaterialList
{
    < F6F23F42-7686-11CF-8F52-0040333594A3 >
    DWORD nMaterials;
    DWORD nFaceIndexes;
    array DWORD faceIndexes[nFaceIndexes];
    [Material <3D82AB4D-62DA-11CF-AB39-0020AF71E433>]
} 
```

<span data-ttu-id="e4184-107">Dove:</span><span class="sxs-lookup"><span data-stu-id="e4184-107">Where:</span></span>

-   <span data-ttu-id="e4184-108">nMaterials-un valore DWORD.</span><span class="sxs-lookup"><span data-stu-id="e4184-108">nMaterials - A DWORD.</span></span> <span data-ttu-id="e4184-109">Il numero di materiali.</span><span class="sxs-lookup"><span data-stu-id="e4184-109">The number of materials.</span></span>
-   <span data-ttu-id="e4184-110">nFaceIndexes-un valore DWORD.</span><span class="sxs-lookup"><span data-stu-id="e4184-110">nFaceIndexes - A DWORD.</span></span> <span data-ttu-id="e4184-111">Numero di indici.</span><span class="sxs-lookup"><span data-stu-id="e4184-111">The number of indices.</span></span>
-   <span data-ttu-id="e4184-112">faceIndexes \[ nFaceIndexes \] : matrice di DWORD contenenti gli indici dei volti.</span><span class="sxs-lookup"><span data-stu-id="e4184-112">faceIndexes\[nFaceIndexes\] - An array of DWORDs containing the face indices.</span></span>

## <a name="see-also"></a><span data-ttu-id="e4184-113">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e4184-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4184-114">Modelli</span><span class="sxs-lookup"><span data-stu-id="e4184-114">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



