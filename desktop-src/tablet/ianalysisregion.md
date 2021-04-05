---
description: Espone metodi e proprietà per un'area che rappresenta un'area di un documento.
ms.assetid: ee823a9e-a144-4394-847e-abf390fb839a
title: Interfaccia IAnalysisRegion (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: c9c5e7653790e193c03b1cf4e0c489ea39c3eec3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751858"
---
# <a name="ianalysisregion-interface"></a><span data-ttu-id="8cdf5-103">Interfaccia IAnalysisRegion</span><span class="sxs-lookup"><span data-stu-id="8cdf5-103">IAnalysisRegion interface</span></span>

<span data-ttu-id="8cdf5-104">Espone metodi e proprietà per un'area che rappresenta un'area di un documento.</span><span class="sxs-lookup"><span data-stu-id="8cdf5-104">Exposes methods and properties for a region that represents an area of a document.</span></span>

## <a name="members"></a><span data-ttu-id="8cdf5-105">Membri</span><span class="sxs-lookup"><span data-stu-id="8cdf5-105">Members</span></span>

<span data-ttu-id="8cdf5-106">L'interfaccia **IAnalysisRegion** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="8cdf5-106">The **IAnalysisRegion** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="8cdf5-107">**IAnalysisRegion** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="8cdf5-107">**IAnalysisRegion** also has these types of members:</span></span>

-   [<span data-ttu-id="8cdf5-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="8cdf5-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="8cdf5-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="8cdf5-109">Methods</span></span>

<span data-ttu-id="8cdf5-110">L'interfaccia **IAnalysisRegion** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="8cdf5-110">The **IAnalysisRegion** interface has these methods.</span></span>



| <span data-ttu-id="8cdf5-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="8cdf5-111">Method</span></span>                                                           | <span data-ttu-id="8cdf5-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8cdf5-112">Description</span></span>                                                                                                                                    |
|:-----------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8cdf5-113">**Clone**</span><span class="sxs-lookup"><span data-stu-id="8cdf5-113">**Clone**</span></span>](ianalysisregion-clone.md)                           | <span data-ttu-id="8cdf5-114">Crea una copia di **IAnalysisRegion**.</span><span class="sxs-lookup"><span data-stu-id="8cdf5-114">Creates a copy of the **IAnalysisRegion**.</span></span><br/>                                                                                          |
| [<span data-ttu-id="8cdf5-115">**ExcludeRectangle**</span><span class="sxs-lookup"><span data-stu-id="8cdf5-115">**ExcludeRectangle**</span></span>](ianalysisregion-excluderectangle.md)     | <span data-ttu-id="8cdf5-116">Limita l'area di **IAnalysisRegion** alla parte dell'area che non interseca il rettangolo specificato.</span><span class="sxs-lookup"><span data-stu-id="8cdf5-116">Restricts the area of the **IAnalysisRegion** to the portion of its area that does not intersect the specified rectangle.</span></span><br/>           |
| [<span data-ttu-id="8cdf5-117">**ExcludeRegion**</span><span class="sxs-lookup"><span data-stu-id="8cdf5-117">**ExcludeRegion**</span></span>](ianalysisregion-excluderegion.md)           | <span data-ttu-id="8cdf5-118">Limita l'area di **IAnalysisRegion** alla parte dell'area che non interseca il **IAnalysisRegion** specificato.</span><span class="sxs-lookup"><span data-stu-id="8cdf5-118">Restricts the area of the **IAnalysisRegion** to the portion of its area that does not intersect the specified **IAnalysisRegion**.</span></span><br/> |
| [<span data-ttu-id="8cdf5-119">**GetBounds**</span><span class="sxs-lookup"><span data-stu-id="8cdf5-119">**GetBounds**</span></span>](ianalysisregion-getbounds.md)                   | <span data-ttu-id="8cdf5-120">Recupera il rettangolo di delimitazione di **IAnalysisRegion**.</span><span class="sxs-lookup"><span data-stu-id="8cdf5-120">Retrieves the bounding rectangle of the **IAnalysisRegion**.</span></span><br/>                                                                        |
| [<span data-ttu-id="8cdf5-121">**GetRegionScans**</span><span class="sxs-lookup"><span data-stu-id="8cdf5-121">**GetRegionScans**</span></span>](ianalysisregion-getregionscans.md)         | <span data-ttu-id="8cdf5-122">Recupera una matrice di rettangoli che definisce l'area di **IAnalysisRegion**.</span><span class="sxs-lookup"><span data-stu-id="8cdf5-122">Retrieves an array of rectangles that defines the area of the **IAnalysisRegion**.</span></span><br/>                                                  |
| [<span data-ttu-id="8cdf5-123">**IntersectRectangle**</span><span class="sxs-lookup"><span data-stu-id="8cdf5-123">**IntersectRectangle**</span></span>](ianalysisregion-intersectrectangle.md) | <span data-ttu-id="8cdf5-124">Limita l'area di questo **IAnalysisRegion** all'area creata dalla relativa intersezione con il rettangolo specificato.</span><span class="sxs-lookup"><span data-stu-id="8cdf5-124">Restricts the area of this **IAnalysisRegion** to the area created by its intersection with the specified rectangle.</span></span><br/>                |
| [<span data-ttu-id="8cdf5-125">**IntersectRegion**</span><span class="sxs-lookup"><span data-stu-id="8cdf5-125">**IntersectRegion**</span></span>](ianalysisregion-intersectregion.md)       | <span data-ttu-id="8cdf5-126">Limita l'area di **IAnalysisRegion** all'area creata dalla relativa intersezione con il **IAnalysisRegion** specificato.</span><span class="sxs-lookup"><span data-stu-id="8cdf5-126">Restricts the area of the **IAnalysisRegion** to the area created by its intersection with the specified **IAnalysisRegion**.</span></span><br/>       |
| [<span data-ttu-id="8cdf5-127">**IntersectsWith**</span><span class="sxs-lookup"><span data-stu-id="8cdf5-127">**IntersectsWith**</span></span>](ianalysisregion-intersectswith.md)         | <span data-ttu-id="8cdf5-128">Determina se l'area del **IAnalysisRegion** interseca il rettangolo specificato.</span><span class="sxs-lookup"><span data-stu-id="8cdf5-128">Determines whether the area of the **IAnalysisRegion** intersects with the specified rectangle.</span></span><br/>                                     |
| [<span data-ttu-id="8cdf5-129">**IsEmpty**</span><span class="sxs-lookup"><span data-stu-id="8cdf5-129">**IsEmpty**</span></span>](ianalysisregion-isempty.md)                       | <span data-ttu-id="8cdf5-130">Recupera un valore che indica se **IAnalysisRegion** rappresenta un'area vuota.</span><span class="sxs-lookup"><span data-stu-id="8cdf5-130">Retrieves a value indicating whether the **IAnalysisRegion** represents an empty region.</span></span><br/>                                            |
| [<span data-ttu-id="8cdf5-131">**IsInfinite**</span><span class="sxs-lookup"><span data-stu-id="8cdf5-131">**IsInfinite**</span></span>](ianalysisregion-isinfinite.md)                 | <span data-ttu-id="8cdf5-132">Recupera un valore che indica se **IAnalysisRegion** rappresenta un'area infinita.</span><span class="sxs-lookup"><span data-stu-id="8cdf5-132">Retrieves a value indicating whether the **IAnalysisRegion** represents an infinite region.</span></span><br/>                                         |
| [<span data-ttu-id="8cdf5-133">**MakeEmpty**</span><span class="sxs-lookup"><span data-stu-id="8cdf5-133">**MakeEmpty**</span></span>](ianalysisregion-makeempty.md)                   | <span data-ttu-id="8cdf5-134">Riduce il **IAnalysisRegion** per rappresentare un'area vuota.</span><span class="sxs-lookup"><span data-stu-id="8cdf5-134">Reduces the **IAnalysisRegion** to represent an empty area.</span></span><br/>                                                                         |
| [<span data-ttu-id="8cdf5-135">**MakeInfinite**</span><span class="sxs-lookup"><span data-stu-id="8cdf5-135">**MakeInfinite**</span></span>](ianalysisregion-makeinfinite.md)             | <span data-ttu-id="8cdf5-136">Espande **IAnalysisRegion** per rappresentare un'area infinita.</span><span class="sxs-lookup"><span data-stu-id="8cdf5-136">Expands the **IAnalysisRegion** to represent an infinite area.</span></span><br/>                                                                      |
| [<span data-ttu-id="8cdf5-137">**UnionRectangle**</span><span class="sxs-lookup"><span data-stu-id="8cdf5-137">**UnionRectangle**</span></span>](ianalysisregion-unionrectangle.md)         | <span data-ttu-id="8cdf5-138">Espande l'area di questo **IAnalysisRegion** all'area creata dalla relativa unione con il rettangolo specificato.</span><span class="sxs-lookup"><span data-stu-id="8cdf5-138">Expands the area of this **IAnalysisRegion** to the area created by its union with the specified rectangle.</span></span><br/>                         |
| [<span data-ttu-id="8cdf5-139">**UnionRegion**</span><span class="sxs-lookup"><span data-stu-id="8cdf5-139">**UnionRegion**</span></span>](ianalysisregion-unionregion.md)               | <span data-ttu-id="8cdf5-140">Espande l'area di questo **IAnalysisRegion** all'area creata dalla relativa unione con il **IAnalysisRegion** specificato.</span><span class="sxs-lookup"><span data-stu-id="8cdf5-140">Expands the area of this **IAnalysisRegion** to the area created by its union with the specified **IAnalysisRegion**.</span></span><br/>               |



 

## <a name="remarks"></a><span data-ttu-id="8cdf5-141">Commenti</span><span class="sxs-lookup"><span data-stu-id="8cdf5-141">Remarks</span></span>

<span data-ttu-id="8cdf5-142">Questa interfaccia rappresenta un'area costruita da aree rettangolari.</span><span class="sxs-lookup"><span data-stu-id="8cdf5-142">This interface represents an area that is constructed from rectangular regions.</span></span> <span data-ttu-id="8cdf5-143">[**IInkAnalyzer**](iinkanalyzer.md) restituisce o interpreta le coordinate di un'area all'interno dello spazio delle coordinate in cui riceve i dati del tratto.</span><span class="sxs-lookup"><span data-stu-id="8cdf5-143">The [**IInkAnalyzer**](iinkanalyzer.md) returns or interprets an area's coordinates within the coordinate space in which it receives stroke data.</span></span>

<span data-ttu-id="8cdf5-144">Per ottenere i limiti correnti di **IAnalysisRegion**, usare il metodo [**IAnalysisRegion:: GetBounds**](ianalysisregion-getbounds.md) o [**IAnalysisRegion:: GetRegionScans**](ianalysisregion-getregionscans.md).</span><span class="sxs-lookup"><span data-stu-id="8cdf5-144">To get the current bounds of the **IAnalysisRegion**, use [**IAnalysisRegion::GetBounds Method**](ianalysisregion-getbounds.md) or [**IAnalysisRegion::GetRegionScans Method**](ianalysisregion-getregionscans.md).</span></span>

<span data-ttu-id="8cdf5-145">Per modificare l'area di un **IAnalysisRegion** esistente, utilizzare i metodi seguenti.</span><span class="sxs-lookup"><span data-stu-id="8cdf5-145">To modify the area of an existing **IAnalysisRegion**, use the following methods.</span></span>

-   [<span data-ttu-id="8cdf5-146">**IAnalysisRegion::ExcludeRectangle**</span><span class="sxs-lookup"><span data-stu-id="8cdf5-146">**IAnalysisRegion::ExcludeRectangle**</span></span>](ianalysisregion-excluderectangle.md)
-   [<span data-ttu-id="8cdf5-147">**Metodo IAnalysisRegion:: ExcludeRegion**</span><span class="sxs-lookup"><span data-stu-id="8cdf5-147">**IAnalysisRegion::ExcludeRegion Method**</span></span>](ianalysisregion-excluderegion.md)
-   [<span data-ttu-id="8cdf5-148">**Metodo IAnalysisRegion:: IntersectRectangle**</span><span class="sxs-lookup"><span data-stu-id="8cdf5-148">**IAnalysisRegion::IntersectRectangle Method**</span></span>](ianalysisregion-intersectrectangle.md)
-   [<span data-ttu-id="8cdf5-149">**Metodo IAnalysisRegion:: IntersectRegion**</span><span class="sxs-lookup"><span data-stu-id="8cdf5-149">**IAnalysisRegion::IntersectRegion Method**</span></span>](ianalysisregion-intersectregion.md)
-   [<span data-ttu-id="8cdf5-150">**Metodo IAnalysisRegion:: MakeEmpty**</span><span class="sxs-lookup"><span data-stu-id="8cdf5-150">**IAnalysisRegion::MakeEmpty Method**</span></span>](ianalysisregion-makeempty.md)
-   [<span data-ttu-id="8cdf5-151">**Metodo IAnalysisRegion:: MakeInfinite**</span><span class="sxs-lookup"><span data-stu-id="8cdf5-151">**IAnalysisRegion::MakeInfinite Method**</span></span>](ianalysisregion-makeinfinite.md)
-   [<span data-ttu-id="8cdf5-152">**Metodo IAnalysisRegion:: UnionRectangle**</span><span class="sxs-lookup"><span data-stu-id="8cdf5-152">**IAnalysisRegion::UnionRectangle Method**</span></span>](ianalysisregion-unionrectangle.md)
-   [<span data-ttu-id="8cdf5-153">**Metodo IAnalysisRegion:: UnionRegion**</span><span class="sxs-lookup"><span data-stu-id="8cdf5-153">**IAnalysisRegion::UnionRegion Method**</span></span>](ianalysisregion-unionregion.md)

<span data-ttu-id="8cdf5-154">Questa interfaccia è equivalente alla classe System. Windows. Ink. AnalysisCore. AnalysisRegionBase nel .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="8cdf5-154">This interface is equivalent to the System.Windows.Ink.AnalysisCore.AnalysisRegionBase class in the .NET Framework.</span></span>

## <a name="requirements"></a><span data-ttu-id="8cdf5-155">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8cdf5-155">Requirements</span></span>



| <span data-ttu-id="8cdf5-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="8cdf5-156">Requirement</span></span> | <span data-ttu-id="8cdf5-157">Valore</span><span class="sxs-lookup"><span data-stu-id="8cdf5-157">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8cdf5-158">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8cdf5-158">Minimum supported client</span></span><br/> | <span data-ttu-id="8cdf5-159">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="8cdf5-159">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="8cdf5-160">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8cdf5-160">Minimum supported server</span></span><br/> | <span data-ttu-id="8cdf5-161">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="8cdf5-161">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="8cdf5-162">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8cdf5-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="8cdf5-163"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="8cdf5-163"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="8cdf5-164">DLL</span><span class="sxs-lookup"><span data-stu-id="8cdf5-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8cdf5-165"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8cdf5-165"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="8cdf5-166">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8cdf5-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cdf5-167">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="8cdf5-167">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="8cdf5-168">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="8cdf5-168">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

