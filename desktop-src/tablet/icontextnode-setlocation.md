---
description: Aggiorna l'area di questo IContextNode.
ms.assetid: e7001411-17e4-4f33-af04-dd3220275895
title: 'Metodo IContextNode:: selocation (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.SetLocation
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 20daefeab7a9e36d5e968d5d14bfa5110d733487
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307417"
---
# <a name="icontextnodesetlocation-method"></a><span data-ttu-id="31d55-103">Metodo IContextNode:: selocation</span><span class="sxs-lookup"><span data-stu-id="31d55-103">IContextNode::SetLocation method</span></span>

<span data-ttu-id="31d55-104">Aggiorna l'area di questo [**IContextNode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="31d55-104">Updates the area of this [**IContextNode**](icontextnode.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="31d55-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="31d55-105">Syntax</span></span>


```C++
HRESULT SetLocation(
  [in] IAnalysisRegion *pIAnalysisRegion
);
```



## <a name="parameters"></a><span data-ttu-id="31d55-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="31d55-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31d55-107">*pIAnalysisRegion* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="31d55-107">*pIAnalysisRegion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31d55-108">[**IAnalysisRegion**](ianalysisregion.md) che descrive l'area in cui impostare la posizione dell'oggetto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="31d55-108">The [**IAnalysisRegion**](ianalysisregion.md) describing the area to which to set the [**IContextNode**](icontextnode.md) object's location.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31d55-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="31d55-109">Return value</span></span>

<span data-ttu-id="31d55-110">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="31d55-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="31d55-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="31d55-111">Remarks</span></span>

<span data-ttu-id="31d55-112">Usare questo metodo per aggiornare la posizione del nodo di contesto (vedere [**IContextNode:: getLocation**](icontextnode-getlocation.md)).</span><span class="sxs-lookup"><span data-stu-id="31d55-112">Use this method to update the context node's location (see [**IContextNode::GetLocation**](icontextnode-getlocation.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="31d55-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="31d55-113">Requirements</span></span>



| <span data-ttu-id="31d55-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="31d55-114">Requirement</span></span> | <span data-ttu-id="31d55-115">Valore</span><span class="sxs-lookup"><span data-stu-id="31d55-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31d55-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="31d55-116">Minimum supported client</span></span><br/> | <span data-ttu-id="31d55-117">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="31d55-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="31d55-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="31d55-118">Minimum supported server</span></span><br/> | <span data-ttu-id="31d55-119">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="31d55-119">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="31d55-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="31d55-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="31d55-121"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="31d55-121"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="31d55-122">DLL</span><span class="sxs-lookup"><span data-stu-id="31d55-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31d55-123"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31d55-123"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="31d55-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="31d55-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31d55-125">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="31d55-125">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="31d55-126">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="31d55-126">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="31d55-127">**IContextNode:: GetLocation**</span><span class="sxs-lookup"><span data-stu-id="31d55-127">**IContextNode::GetLocation**</span></span>](icontextnode-getlocation.md)
</dt> <dt>

[<span data-ttu-id="31d55-128">**IContextNode::GetPartiallyPopulated**</span><span class="sxs-lookup"><span data-stu-id="31d55-128">**IContextNode::GetPartiallyPopulated**</span></span>](icontextnode-getpartiallypopulated.md)
</dt> <dt>

[<span data-ttu-id="31d55-129">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="31d55-129">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




