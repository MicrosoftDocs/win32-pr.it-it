---
description: Aggiunge un nuovo IContextLink alla raccolta di collegamenti di contesto dell'oggetto IContextNode.
ms.assetid: b7b9da10-3015-4976-bc4e-1a7f69b7c85b
title: 'Metodo IContextNode:: AddContextLink (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.AddContextLink
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: eccfcc8be51ff951c1bcd6de55bd3a0f89cdc201
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307445"
---
# <a name="icontextnodeaddcontextlink-method"></a><span data-ttu-id="4f1f6-103">Metodo IContextNode:: AddContextLink</span><span class="sxs-lookup"><span data-stu-id="4f1f6-103">IContextNode::AddContextLink method</span></span>

<span data-ttu-id="4f1f6-104">Aggiunge un nuovo [**IContextLink**](icontextlink.md) alla raccolta di collegamenti di contesto dell'oggetto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="4f1f6-104">Adds a new [**IContextLink**](icontextlink.md) to the [**IContextNode**](icontextnode.md) object's collection of context links.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f1f6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4f1f6-105">Syntax</span></span>


```C++
HRESULT AddContextLink(
  [in]  IContextNode         *pDestinationNode,
  [in]  ContextLinkDirection linkDirection,
  [out] IContextLink         **ppContextLinkToAdd
);
```



## <a name="parameters"></a><span data-ttu-id="4f1f6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4f1f6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f1f6-107">*pDestinationNode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4f1f6-107">*pDestinationNode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f1f6-108">[**IContextNode**](icontextnode.md) di destinazione per il nuovo [**IContextLink**](icontextlink.md).</span><span class="sxs-lookup"><span data-stu-id="4f1f6-108">The destination [**IContextNode**](icontextnode.md) for the new [**IContextLink**](icontextlink.md).</span></span>

</dd> <dt>

<span data-ttu-id="4f1f6-109">*linkDirection* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4f1f6-109">*linkDirection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f1f6-110">Direzione dell'oggetto [**IContextLink**](icontextlink.md) da creare.</span><span class="sxs-lookup"><span data-stu-id="4f1f6-110">The direction of [**IContextLink**](icontextlink.md) object to create.</span></span>

</dd> <dt>

<span data-ttu-id="4f1f6-111">*ppContextLinkToAdd* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4f1f6-111">*ppContextLinkToAdd* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4f1f6-112">Puntatore al nuovo oggetto [**IContextLink**](icontextlink.md) .</span><span class="sxs-lookup"><span data-stu-id="4f1f6-112">A pointer to the new [**IContextLink**](icontextlink.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f1f6-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4f1f6-113">Return value</span></span>

<span data-ttu-id="4f1f6-114">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="4f1f6-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4f1f6-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="4f1f6-115">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="4f1f6-116">Per evitare una perdita di memoria, chiamare [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su \* *ppContextLinkToAdd* quando non è più necessario usare il nodo di contesto.</span><span class="sxs-lookup"><span data-stu-id="4f1f6-116">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppContextLinkToAdd* when you no longer need to use the context node.</span></span>

 

<span data-ttu-id="4f1f6-117">Questo oggetto [**IContextNode**](icontextnode.md) è il nodo di origine (vedere [**IContextLink:: GetSourceNode**](icontextlink-getsourcenode.md)) per il nuovo oggetto [**IContextLink**](icontextlink.md) .</span><span class="sxs-lookup"><span data-stu-id="4f1f6-117">This [**IContextNode**](icontextnode.md) object is the source node (see [**IContextLink::GetSourceNode**](icontextlink-getsourcenode.md)) for the new [**IContextLink**](icontextlink.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f1f6-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4f1f6-118">Requirements</span></span>



| <span data-ttu-id="4f1f6-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f1f6-119">Requirement</span></span> | <span data-ttu-id="4f1f6-120">Valore</span><span class="sxs-lookup"><span data-stu-id="4f1f6-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f1f6-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4f1f6-121">Minimum supported client</span></span><br/> | <span data-ttu-id="4f1f6-122">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="4f1f6-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="4f1f6-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4f1f6-123">Minimum supported server</span></span><br/> | <span data-ttu-id="4f1f6-124">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="4f1f6-124">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="4f1f6-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4f1f6-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f1f6-126"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="4f1f6-126"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="4f1f6-127">DLL</span><span class="sxs-lookup"><span data-stu-id="4f1f6-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f1f6-128"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f1f6-128"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="4f1f6-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4f1f6-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f1f6-130">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="4f1f6-130">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="4f1f6-131">**IContextLink**</span><span class="sxs-lookup"><span data-stu-id="4f1f6-131">**IContextLink**</span></span>](icontextlink.md)
</dt> <dt>

[<span data-ttu-id="4f1f6-132">**IContextLinks**</span><span class="sxs-lookup"><span data-stu-id="4f1f6-132">**IContextLinks**</span></span>](icontextlinks.md)
</dt> <dt>

[<span data-ttu-id="4f1f6-133">**ContextLinkDirection**</span><span class="sxs-lookup"><span data-stu-id="4f1f6-133">**ContextLinkDirection**</span></span>](contextlinkdirection.md)
</dt> <dt>

[<span data-ttu-id="4f1f6-134">**IContextNode::D eleteContextLink**</span><span class="sxs-lookup"><span data-stu-id="4f1f6-134">**IContextNode::DeleteContextLink**</span></span>](icontextnode-deletecontextlink.md)
</dt> <dt>

[<span data-ttu-id="4f1f6-135">**IContextNode::GetContextLinks**</span><span class="sxs-lookup"><span data-stu-id="4f1f6-135">**IContextNode::GetContextLinks**</span></span>](icontextnode-getcontextlinks.md)
</dt> <dt>

[<span data-ttu-id="4f1f6-136">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="4f1f6-136">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

