---
description: Specifica i dati della mesh meno i dati di posizione.
ms.assetid: 30a95ca3-84ab-475d-9654-a3853263056b
title: FVFData
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d52af6096357c4855d2dc34442c6cd4814b6713b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123855"
---
# <a name="fvfdata"></a><span data-ttu-id="b1bdf-103">FVFData</span><span class="sxs-lookup"><span data-stu-id="b1bdf-103">FVFData</span></span>

<span data-ttu-id="b1bdf-104">Specifica i dati della mesh meno i dati di posizione.</span><span class="sxs-lookup"><span data-stu-id="b1bdf-104">Specifies the mesh data minus the position data.</span></span>

``` syntax
template FVFData
{
    < B6E70A0E-8EF9-4e83-94AD-ECC8B0C04897 >
    DWORD dwFVF;
    DWORD nDWords;
    array DWORD data[nDWords];
} 
```

<span data-ttu-id="b1bdf-105">Dove:</span><span class="sxs-lookup"><span data-stu-id="b1bdf-105">Where:</span></span>

-   <span data-ttu-id="b1bdf-106">dwFVF: codice FVF.</span><span class="sxs-lookup"><span data-stu-id="b1bdf-106">dwFVF - A FVF code.</span></span>
-   <span data-ttu-id="b1bdf-107">nDWords-dati binari.</span><span class="sxs-lookup"><span data-stu-id="b1bdf-107">nDWords - Binary data.</span></span> <span data-ttu-id="b1bdf-108">Numero di DWORD.</span><span class="sxs-lookup"><span data-stu-id="b1bdf-108">The number of DWORDS.</span></span>
-   <span data-ttu-id="b1bdf-109">Data \[ nDWords \] : matrice di DWORD che contiene i dati in ogni elemento vertice.</span><span class="sxs-lookup"><span data-stu-id="b1bdf-109">data\[nDWords\] - Array of DWORDS that contain the data in each vertex element.</span></span>

## <a name="see-also"></a><span data-ttu-id="b1bdf-110">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b1bdf-110">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1bdf-111">Modelli</span><span class="sxs-lookup"><span data-stu-id="b1bdf-111">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



