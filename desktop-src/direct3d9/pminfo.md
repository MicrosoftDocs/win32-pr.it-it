---
description: Non supportata. Usato internamente da DirectX.
ms.assetid: 8a07357f-d4e8-4104-9d21-51c3e8b8d6d2
title: PMInfo
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b4217e2a044e39a7125705f1d3863b9737120e8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304066"
---
# <a name="pminfo"></a><span data-ttu-id="363ab-104">PMInfo</span><span class="sxs-lookup"><span data-stu-id="363ab-104">PMInfo</span></span>

<span data-ttu-id="363ab-105">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="363ab-105">Not supported.</span></span> <span data-ttu-id="363ab-106">Usato internamente da DirectX.</span><span class="sxs-lookup"><span data-stu-id="363ab-106">Used internally by DirectX.</span></span>

``` syntax
template PMInfo 
{ 
    < B6C3E656-EC8B-4b92-9B62-681659522947 > 
    DWORD nAttributes; 
    array PMAttributeRange attributeRanges[nAttributes]; 
    DWORD nMaxValence; 
    DWORD nMinLogicalVertices; 
    DWORD nMaxLogicalVertices; 
    DWORD nVSplits; 
    array PMVSplitRecord splitRecords[nVSplits]; 
    DWORD nAttributeMispredicts; 
    array DWORD attributeMispredicts[nAttributeMispredicts]; 
}
```

## <a name="see-also"></a><span data-ttu-id="363ab-107">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="363ab-107">See also</span></span>

<dl> <dt>

[<span data-ttu-id="363ab-108">Modelli</span><span class="sxs-lookup"><span data-stu-id="363ab-108">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



