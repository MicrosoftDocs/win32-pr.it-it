---
description: Elimina un oggetto IContextLink dalla raccolta di collegamenti dell'oggetto IContextNode.
ms.assetid: c4a69a74-30d6-4099-a02a-13c8a2e52bc7
title: Metodo IContextNode::D eleteContextLink (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.DeleteContextLink
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ac5676635bec961129078ed8689169d1a81cd87d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307441"
---
# <a name="icontextnodedeletecontextlink-method"></a><span data-ttu-id="9fe8b-103">IContextNode::D Metodo eleteContextLink</span><span class="sxs-lookup"><span data-stu-id="9fe8b-103">IContextNode::DeleteContextLink method</span></span>

<span data-ttu-id="9fe8b-104">Elimina un oggetto [**IContextLink**](icontextlink.md) dalla raccolta di collegamenti dell'oggetto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="9fe8b-104">Deletes an [**IContextLink**](icontextlink.md) object from the [**IContextNode**](icontextnode.md) object's link collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fe8b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9fe8b-105">Syntax</span></span>


```C++
HRESULT DeleteContextLink(
  [in] IContextLink *pContextLinkToDelete
);
```



## <a name="parameters"></a><span data-ttu-id="9fe8b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9fe8b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9fe8b-107">*pContextLinkToDelete* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9fe8b-107">*pContextLinkToDelete* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fe8b-108">Oggetto [**IContextLink**](icontextlink.md) da eliminare.</span><span class="sxs-lookup"><span data-stu-id="9fe8b-108">The [**IContextLink**](icontextlink.md) object to delete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9fe8b-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9fe8b-109">Return value</span></span>

<span data-ttu-id="9fe8b-110">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="9fe8b-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9fe8b-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="9fe8b-111">Remarks</span></span>

<span data-ttu-id="9fe8b-112">Un collegamento di contesto ha un nodo di origine e un nodo di destinazione (vedere [**IContextLink:: GetSourceNode**](icontextlink-getsourcenode.md) e [**IContextLink:: GetDestinationNode**](icontextlink-getdestinationnode.md)).</span><span class="sxs-lookup"><span data-stu-id="9fe8b-112">A context link has a source node and a destination node (see [**IContextLink::GetSourceNode**](icontextlink-getsourcenode.md) and [**IContextLink::GetDestinationNode**](icontextlink-getdestinationnode.md)).</span></span> <span data-ttu-id="9fe8b-113">Questo metodo rimuove il [**IContextLink**](icontextlink.md) dalla raccolta di collegamenti di contesto di entrambi i nodi di origine e di destinazione (vedere [**IContextNode:: GetContextLinks**](icontextnode-getcontextlinks.md)).</span><span class="sxs-lookup"><span data-stu-id="9fe8b-113">This method removes the [**IContextLink**](icontextlink.md) from both the source and destination nodes' collection of context links (see [**IContextNode::GetContextLinks**](icontextnode-getcontextlinks.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="9fe8b-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9fe8b-114">Requirements</span></span>



| <span data-ttu-id="9fe8b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="9fe8b-115">Requirement</span></span> | <span data-ttu-id="9fe8b-116">Valore</span><span class="sxs-lookup"><span data-stu-id="9fe8b-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fe8b-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9fe8b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9fe8b-118">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="9fe8b-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="9fe8b-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9fe8b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9fe8b-120">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="9fe8b-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="9fe8b-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9fe8b-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="9fe8b-122"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="9fe8b-122"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="9fe8b-123">DLL</span><span class="sxs-lookup"><span data-stu-id="9fe8b-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9fe8b-124"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9fe8b-124"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="9fe8b-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9fe8b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fe8b-126">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="9fe8b-126">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="9fe8b-127">**IContextLink**</span><span class="sxs-lookup"><span data-stu-id="9fe8b-127">**IContextLink**</span></span>](icontextlink.md)
</dt> <dt>

[<span data-ttu-id="9fe8b-128">**IContextNode::AddContextLink**</span><span class="sxs-lookup"><span data-stu-id="9fe8b-128">**IContextNode::AddContextLink**</span></span>](icontextnode-addcontextlink.md)
</dt> <dt>

[<span data-ttu-id="9fe8b-129">**IContextNode::GetContextLinks**</span><span class="sxs-lookup"><span data-stu-id="9fe8b-129">**IContextNode::GetContextLinks**</span></span>](icontextnode-getcontextlinks.md)
</dt> <dt>

[<span data-ttu-id="9fe8b-130">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="9fe8b-130">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




