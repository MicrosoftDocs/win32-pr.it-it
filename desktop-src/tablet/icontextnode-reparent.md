---
description: Sposta questo oggetto IContextNode dalla raccolta del nodo di contesto padre dei sottonodi alla raccolta di sottonodi del nodo di contesto specificato.
ms.assetid: e19ecbe3-f7aa-499c-86a1-236dc9056fd9
title: 'Metodo IContextNode:: Reparent (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.Reparent
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 805b96b2a392a4f7b70aa4ce5913b48ffaf33551
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049522"
---
# <a name="icontextnodereparent-method"></a><span data-ttu-id="39b39-103">Metodo IContextNode:: Reparent</span><span class="sxs-lookup"><span data-stu-id="39b39-103">IContextNode::Reparent method</span></span>

<span data-ttu-id="39b39-104">Sposta questo oggetto [**IContextNode**](icontextnode.md) dalla raccolta del nodo di contesto padre dei sottonodi alla raccolta di sottonodi del nodo di contesto specificato.</span><span class="sxs-lookup"><span data-stu-id="39b39-104">Moves this [**IContextNode**](icontextnode.md) object from its parent context node's collection of subnodes to the specified context node's collection of subnodes.</span></span>

## <a name="syntax"></a><span data-ttu-id="39b39-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="39b39-105">Syntax</span></span>


```C++
HRESULT Reparent(
  [in] IContextNode *pNewParent
);
```



## <a name="parameters"></a><span data-ttu-id="39b39-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="39b39-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39b39-107">*pNewParent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="39b39-107">*pNewParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39b39-108">Nuovo nodo padre per questo oggetto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="39b39-108">The new parent node for this [**IContextNode**](icontextnode.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39b39-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="39b39-109">Return value</span></span>

<span data-ttu-id="39b39-110">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="39b39-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="39b39-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="39b39-111">Requirements</span></span>



| <span data-ttu-id="39b39-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="39b39-112">Requirement</span></span> | <span data-ttu-id="39b39-113">Valore</span><span class="sxs-lookup"><span data-stu-id="39b39-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39b39-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="39b39-114">Minimum supported client</span></span><br/> | <span data-ttu-id="39b39-115">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="39b39-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="39b39-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="39b39-116">Minimum supported server</span></span><br/> | <span data-ttu-id="39b39-117">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="39b39-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="39b39-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="39b39-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="39b39-119"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="39b39-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="39b39-120">DLL</span><span class="sxs-lookup"><span data-stu-id="39b39-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39b39-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39b39-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="39b39-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="39b39-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39b39-123">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="39b39-123">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="39b39-124">**IContextNode:: GetParentNode**</span><span class="sxs-lookup"><span data-stu-id="39b39-124">**IContextNode::GetParentNode**</span></span>](icontextnode-getparentnode.md)
</dt> <dt>

[<span data-ttu-id="39b39-125">**IContextNode::GetSubNodes**</span><span class="sxs-lookup"><span data-stu-id="39b39-125">**IContextNode::GetSubNodes**</span></span>](icontextnode-getsubnodes.md)
</dt> <dt>

[<span data-ttu-id="39b39-126">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="39b39-126">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




