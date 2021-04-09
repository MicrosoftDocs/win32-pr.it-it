---
description: Definisce una patch di \# controllo Zier B&233;. La matrice definisce i punti di controllo per la patch.
ms.assetid: vs|directx_sdk|~\patch.htm
title: Patch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 480457b3dd3800aca8b23210e3fe653b4e713e94
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103875966"
---
# <a name="patch"></a><span data-ttu-id="0b556-104">Patch</span><span class="sxs-lookup"><span data-stu-id="0b556-104">Patch</span></span>

<span data-ttu-id="0b556-105">Definisce una patch di controllo di Bézier.</span><span class="sxs-lookup"><span data-stu-id="0b556-105">Defines a Bézier control patch.</span></span> <span data-ttu-id="0b556-106">La matrice definisce i punti di controllo per la patch.</span><span class="sxs-lookup"><span data-stu-id="0b556-106">The array defines the control points for the patch.</span></span>

``` syntax
template Patch
{
    < A3EB5D44-FC22-429D-9AFB-3221CB9719A6 >
    DWORD nControlIndices;
    array DWORD controlIndices[nControlIndices];
} 
```

<span data-ttu-id="0b556-107">Dove:</span><span class="sxs-lookup"><span data-stu-id="0b556-107">Where:</span></span>

-   <span data-ttu-id="0b556-108">nControlIndices: numero di indici dei punti di controllo.</span><span class="sxs-lookup"><span data-stu-id="0b556-108">nControlIndices - Number of control point indices.</span></span>
-   <span data-ttu-id="0b556-109">Array DWORD controlIndices \[ nControlIndices \] -matrice di indici di punti di controllo.</span><span class="sxs-lookup"><span data-stu-id="0b556-109">array DWORD controlIndices\[nControlIndices\] - Array of control point indices.</span></span>

<span data-ttu-id="0b556-110">Il tipo di patch è definito dal numero di punti di controllo, come illustrato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="0b556-110">The type of patch is defined by the number of control points, as shown in the following table.</span></span>



| <span data-ttu-id="0b556-111">Numero di punti di controllo</span><span class="sxs-lookup"><span data-stu-id="0b556-111">Number of control points</span></span> | <span data-ttu-id="0b556-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="0b556-112">Type</span></span>                              |
|--------------------------|-----------------------------------|
| <span data-ttu-id="0b556-113">10</span><span class="sxs-lookup"><span data-stu-id="0b556-113">10</span></span>                       | <span data-ttu-id="0b556-114">Patch triangolare Bézier cubica</span><span class="sxs-lookup"><span data-stu-id="0b556-114">Cubic Bézier triangular patch</span></span>     |
| <span data-ttu-id="0b556-115">15</span><span class="sxs-lookup"><span data-stu-id="0b556-115">15</span></span>                       | <span data-ttu-id="0b556-116">Patch triangolare Béziers quartica</span><span class="sxs-lookup"><span data-stu-id="0b556-116">Quartic Bézier triangular patch</span></span>   |
| <span data-ttu-id="0b556-117">16</span><span class="sxs-lookup"><span data-stu-id="0b556-117">16</span></span>                       | <span data-ttu-id="0b556-118">Patch rettangolare di Bézier a cubi quadre</span><span class="sxs-lookup"><span data-stu-id="0b556-118">Cubic Bézier quad rectangle patch</span></span> |



 

<span data-ttu-id="0b556-119">L'ordine dei punti di controllo viene fornito in un modello a spirale, come illustrato nei diagrammi seguenti per le patch triangolari e rettangolari.</span><span class="sxs-lookup"><span data-stu-id="0b556-119">The order of the control points are given in a spiral pattern, as shown in the following diagrams for triangular and rectangular patches.</span></span>

<span data-ttu-id="0b556-120">Le patch triangolari usano il modello seguente.</span><span class="sxs-lookup"><span data-stu-id="0b556-120">Triangular patches use the following pattern.</span></span>

![diagramma del modello per le patch triangolari](images/tripatch.png)

<span data-ttu-id="0b556-122">Le patch rettangolari usano il modello seguente.</span><span class="sxs-lookup"><span data-stu-id="0b556-122">Rectangular patches use the following pattern.</span></span>

![diagramma del modello per le patch rettangolari](images/quadpatch.png)

## <a name="see-also"></a><span data-ttu-id="0b556-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0b556-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b556-125">Modelli</span><span class="sxs-lookup"><span data-stu-id="0b556-125">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



