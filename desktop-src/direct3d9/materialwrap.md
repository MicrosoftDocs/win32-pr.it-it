---
description: Definisce un set di due valori booleani utilizzati nel modello MeshFaceWraps per definire la topologia di trama di una singola faccia. Usare anziché Boolean2d quando le coordinate di trama (u, v) si estendono nell'intervallo da 0 a 2 anziché da 0 a 1.
ms.assetid: 0d1755fc-66cb-4372-b9d0-fb320c55d6a7
title: MaterialWrap
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6797719919a4f52421751a5cad008aa8a581089a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303845"
---
# <a name="materialwrap"></a><span data-ttu-id="086d3-104">MaterialWrap</span><span class="sxs-lookup"><span data-stu-id="086d3-104">MaterialWrap</span></span>

<span data-ttu-id="086d3-105">Definisce un set di due valori booleani utilizzati nel modello [**MeshFaceWraps**](meshfacewraps.md) per definire la topologia di trama di una singola faccia.</span><span class="sxs-lookup"><span data-stu-id="086d3-105">Defines a set of two Boolean values used in the [**MeshFaceWraps**](meshfacewraps.md) template to define the texture topology of an individual face.</span></span> <span data-ttu-id="086d3-106">Usare anziché [**Boolean2d**](boolean2d.md) quando le coordinate di trama (u, v) si estendono nell'intervallo da 0 a 2 anziché da 0 a 1.</span><span class="sxs-lookup"><span data-stu-id="086d3-106">Use instead of [**Boolean2d**](boolean2d.md) when the texture coordinates (u, v) span the range of 0 to 2 instead of 0 to 1.</span></span>

``` syntax
template MaterialWrap
{
    < 4885ae60-78e8-11cf-8f52-0040333594a3 >
    Boolean u;
    Boolean v;
} 
```

<span data-ttu-id="086d3-107">Dove:</span><span class="sxs-lookup"><span data-stu-id="086d3-107">Where:</span></span>

-   <span data-ttu-id="086d3-108">valore u-Boolean.</span><span class="sxs-lookup"><span data-stu-id="086d3-108">u - Boolean value.</span></span> <span data-ttu-id="086d3-109">Vedere [**valore booleano**](boolean.md).</span><span class="sxs-lookup"><span data-stu-id="086d3-109">See [**Boolean**](boolean.md).</span></span>
-   <span data-ttu-id="086d3-110">v: valore booleano.</span><span class="sxs-lookup"><span data-stu-id="086d3-110">v - Boolean value.</span></span> <span data-ttu-id="086d3-111">Vedere [**valore booleano**](boolean.md).</span><span class="sxs-lookup"><span data-stu-id="086d3-111">See [**Boolean**](boolean.md).</span></span>

> [!Note]  
> <span data-ttu-id="086d3-112">Il modello [**MeshFaceWraps**](meshfacewraps.md) non viene più usato.</span><span class="sxs-lookup"><span data-stu-id="086d3-112">The [**MeshFaceWraps**](meshfacewraps.md) template is no longer used.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="086d3-113">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="086d3-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="086d3-114">Modelli</span><span class="sxs-lookup"><span data-stu-id="086d3-114">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



