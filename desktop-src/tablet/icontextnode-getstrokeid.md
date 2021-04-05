---
description: Recupera l'identificatore del tratto per il tratto a cui fa riferimento un valore di indice all'interno dell'oggetto IContextNode.
ms.assetid: faac142e-cac1-45f9-9b40-76c50ac7006b
title: 'Metodo IContextNode:: GetStrokeId (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetStrokeId
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: b193b3719ac6b67284e3ff8c4297455888f6c9cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751842"
---
# <a name="icontextnodegetstrokeid-method"></a><span data-ttu-id="9effb-103">Metodo IContextNode:: GetStrokeId</span><span class="sxs-lookup"><span data-stu-id="9effb-103">IContextNode::GetStrokeId method</span></span>

<span data-ttu-id="9effb-104">Recupera l'identificatore del tratto per il tratto a cui fa riferimento un valore di indice all'interno dell'oggetto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="9effb-104">Retrieves the stroke identifier for the stroke referenced by an index value within the [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="9effb-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9effb-105">Syntax</span></span>


```C++
HRESULT GetStrokeId(
  [in]  ULONG ulIndex,
  [out] LONG  *plStrokeId
);
```



## <a name="parameters"></a><span data-ttu-id="9effb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9effb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9effb-107">*ulIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9effb-107">*ulIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9effb-108">Indice del tratto da restituire.</span><span class="sxs-lookup"><span data-stu-id="9effb-108">The index of the stroke to be returned.</span></span>

</dd> <dt>

<span data-ttu-id="9effb-109">*plStrokeId* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9effb-109">*plStrokeId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9effb-110">Identificatore del tratto per il tratto a cui fa riferimento il parametro *ulIndex* all'interno dell'oggetto [**IContextNode**](icontextnode.md) corrente.</span><span class="sxs-lookup"><span data-stu-id="9effb-110">The stroke identifier for the stroke referenced by the *ulIndex* parameter within the current [**IContextNode**](icontextnode.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9effb-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9effb-111">Return value</span></span>

<span data-ttu-id="9effb-112">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="9effb-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9effb-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9effb-113">Requirements</span></span>



| <span data-ttu-id="9effb-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="9effb-114">Requirement</span></span> | <span data-ttu-id="9effb-115">Valore</span><span class="sxs-lookup"><span data-stu-id="9effb-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9effb-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9effb-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9effb-117">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="9effb-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="9effb-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9effb-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9effb-119">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="9effb-119">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="9effb-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9effb-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="9effb-121"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="9effb-121"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="9effb-122">DLL</span><span class="sxs-lookup"><span data-stu-id="9effb-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9effb-123"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9effb-123"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="9effb-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9effb-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9effb-125">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="9effb-125">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="9effb-126">**IContextNode:: GetStrokeIds**</span><span class="sxs-lookup"><span data-stu-id="9effb-126">**IContextNode::GetStrokeIds**</span></span>](icontextnode-getstrokeids.md)
</dt> <dt>

[<span data-ttu-id="9effb-127">**IContextNode::GetStrokeCount**</span><span class="sxs-lookup"><span data-stu-id="9effb-127">**IContextNode::GetStrokeCount**</span></span>](icontextnode-getstrokecount.md)
</dt> <dt>

[<span data-ttu-id="9effb-128">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="9effb-128">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




