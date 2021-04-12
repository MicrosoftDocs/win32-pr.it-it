---
description: Descrive una dichiarazione del vertice.
ms.assetid: 6a95bdf6-8767-4ad3-bcec-b32858d25571
title: DeclData
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89a26d667f853db3044db3155c55eb4a6d941c6e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481116"
---
# <a name="decldata"></a><span data-ttu-id="c69ea-103">DeclData</span><span class="sxs-lookup"><span data-stu-id="c69ea-103">DeclData</span></span>

<span data-ttu-id="c69ea-104">Descrive una dichiarazione del vertice.</span><span class="sxs-lookup"><span data-stu-id="c69ea-104">Describes a vertex declaration.</span></span>

``` syntax
template DeclData
{
    < BF22E553-292C-4781-9FEA-62BD554BDD93 >
    DWORD nElements;
    array VertexElement Elements[nElements];
    DWORD nDWords;
    array DWORD data[nDWords];
} 
```

<span data-ttu-id="c69ea-105">Dove:</span><span class="sxs-lookup"><span data-stu-id="c69ea-105">Where:</span></span>

-   <span data-ttu-id="c69ea-106">nElements: numero di elementi di dichiarazione del vertice.</span><span class="sxs-lookup"><span data-stu-id="c69ea-106">nElements - Number of vertex declaration elements.</span></span>
-   <span data-ttu-id="c69ea-107">Elements \[ nElements \] -matrice di elementi di dichiarazione vertici.</span><span class="sxs-lookup"><span data-stu-id="c69ea-107">Elements\[nElements\] - Array of vertex declaration elements.</span></span>
-   <span data-ttu-id="c69ea-108">nDWords: numero di DWORD.</span><span class="sxs-lookup"><span data-stu-id="c69ea-108">nDWords - Number of DWORDS.</span></span>
-   <span data-ttu-id="c69ea-109">Data \[ nDWords \] : matrice di DWORD che contiene i dati in ogni elemento vertice.</span><span class="sxs-lookup"><span data-stu-id="c69ea-109">data\[nDWords\] - Array of DWORDS that contain the data in each vertex element.</span></span>

## <a name="see-also"></a><span data-ttu-id="c69ea-110">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c69ea-110">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c69ea-111">Modelli</span><span class="sxs-lookup"><span data-stu-id="c69ea-111">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



