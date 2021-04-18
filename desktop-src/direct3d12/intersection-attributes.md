---
title: Struttura degli attributi di intersezione
description: Struttura dichiarata in HLSL per rappresentare gli attributi hit per l'intersezione del triangolo a funzione fissa o il rettangolo di delimitazione allineato all'asse per l'intersezione primitiva procedurale.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: language-reference
ms.date: 05/31/2018
ms.openlocfilehash: b2f1dd8fee7371f81dd538b6ea6622f22e3bfd3d
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/12/2021
ms.locfileid: "106320435"
---
# <a name="intersection-attributes-structure"></a><span data-ttu-id="43ff4-103">Struttura degli attributi di intersezione</span><span class="sxs-lookup"><span data-stu-id="43ff4-103">Intersection attributes structure</span></span> 

<span data-ttu-id="43ff4-104">Struttura dichiarata in HLSL per rappresentare gli attributi hit per l'intersezione del triangolo a funzione fissa o il rettangolo di delimitazione allineato all'asse per l'intersezione primitiva procedurale.</span><span class="sxs-lookup"><span data-stu-id="43ff4-104">A structure declared in HLSL to represent hit attributes for fixed-function triangle intersection or axis-aligned bounding box for procedural primitive intersection.</span></span>

## <a name="fixed-function-triangle-intersection"></a><span data-ttu-id="43ff4-105">Intersezione del triangolo a funzione fissa</span><span class="sxs-lookup"><span data-stu-id="43ff4-105">Fixed-function triangle intersection</span></span>

<span data-ttu-id="43ff4-106">La struttura seguente viene dichiarata in HLSL per rappresentare gli attributi di hit per l'intersezione del triangolo a funzione fissa:</span><span class="sxs-lookup"><span data-stu-id="43ff4-106">The following structure is declared in HLSL to represent hit attributes for fixed-function triangle intersection:</span></span>


```
struct BuiltInTriangleIntersectionAttributes
{
    float2 barycentrics;
};
```

<span data-ttu-id="43ff4-107">[Tutti](any-hit-shader.md) gli hit shader richiamati e [più vicini](closest-hit-shader.md) richiamati usando l'intersezione del triangolo a funzione fissa devono usare questa struttura per gli attributi hit.</span><span class="sxs-lookup"><span data-stu-id="43ff4-107">[Any hit](any-hit-shader.md) and [closest hit](closest-hit-shader.md) shaders invoked using fixed-function triangle intersection must use this structure for hit attributes.</span></span> <span data-ttu-id="43ff4-108">Dato gli attributi a0, a1 e a2 per i 3 vertici di un triangolo, barycentrics. x è il peso per a1 e barycentrics. y è il peso per a2.</span><span class="sxs-lookup"><span data-stu-id="43ff4-108">Given attributes a0, a1 and a2 for the 3 vertices of a triangle, barycentrics.x is the weight for a1 and barycentrics.y is the weight for a2.</span></span>  <span data-ttu-id="43ff4-109">Ad esempio, l'app può interpolare eseguendo: a = a0 + barycentrics. x \* (a1-a0) + barycentrics. y \* (a2-a0).</span><span class="sxs-lookup"><span data-stu-id="43ff4-109">For example, the app can interpolate by doing:  a = a0 + barycentrics.x \* (a1-a0) + barycentrics.y\* (a2 – a0).</span></span>

## <a name="axis-aligned-bounding-box-for-procedural-primitive-intersection"></a><span data-ttu-id="43ff4-110">Rettangolo di delimitazione allineato all'asse per l'intersezione primitiva procedurale</span><span class="sxs-lookup"><span data-stu-id="43ff4-110">Axis-aligned bounding box for procedural primitive intersection</span></span>

<span data-ttu-id="43ff4-111">Quando vengono usati i rettangoli di delimitazione allineati all'asse per l'intersezione con le primitive procedurali, viene attivata un'intersezione shader.</span><span class="sxs-lookup"><span data-stu-id="43ff4-111">When axis-aligned bounding boxes are used for intersection with procedural primitives, an intersection shader is triggered.</span></span>  <span data-ttu-id="43ff4-112">Lo shader fornisce una struttura dell'attributo di intersezione definita dall'utente alla chiamata [**ReportHit**](reporthit-function.md) .</span><span class="sxs-lookup"><span data-stu-id="43ff4-112">That shader provides a user-defined intersection attribute structure to the [**ReportHit**](reporthit-function.md) call.</span></span>  <span data-ttu-id="43ff4-113">Tutti gli hit e gli hit shader associati nello stesso gruppo di hit con questa intersezione shader devono usare la stessa struttura per gli attributi hit, anche se non si fa riferimento agli attributi.</span><span class="sxs-lookup"><span data-stu-id="43ff4-113">The any hit and closest hit shaders bound in the same hit group with this intersection shader must use the same structure for hit attributes, even if the attributes are not referenced.</span></span>  <span data-ttu-id="43ff4-114">La dimensione massima della struttura dell'attributo è 32 byte, definita come **D3D12 \_ RAYTRACING \_ Max \_ Attribute \_ size \_ in \_ bytes**.</span><span class="sxs-lookup"><span data-stu-id="43ff4-114">The maximum attribute structure size is 32 bytes, defined as **D3D12\_RAYTRACING\_MAX\_ATTRIBUTE\_SIZE\_IN\_BYTES**.</span></span>


