---
description: Recupera il tipo dell'oggetto IContextNode.
ms.assetid: 285384ce-5cdc-47f5-a1c4-6c6d7f18e215
title: 'Metodo IContextNode:: GetType (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetType
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 68b657d9acd6f25f7c067e339ec42c6994a34c48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129494"
---
# <a name="icontextnodegettype-method"></a><span data-ttu-id="1c24e-103">Metodo IContextNode:: GetType</span><span class="sxs-lookup"><span data-stu-id="1c24e-103">IContextNode::GetType method</span></span>

<span data-ttu-id="1c24e-104">Recupera il tipo dell'oggetto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="1c24e-104">Retrieves the type of the [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c24e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1c24e-105">Syntax</span></span>


```C++
HRESULT GetType(
  [out] GUID *pContextNodeType
);
```



## <a name="parameters"></a><span data-ttu-id="1c24e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1c24e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c24e-107">*pContextNodeType* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="1c24e-107">*pContextNodeType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1c24e-108">Tipo dell'oggetto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="1c24e-108">The type of the [**IContextNode**](icontextnode.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c24e-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1c24e-109">Return value</span></span>

<span data-ttu-id="1c24e-110">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="1c24e-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="1c24e-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="1c24e-111">Remarks</span></span>

<span data-ttu-id="1c24e-112">I tipi di nodi sono descritti nelle costanti dei [tipi di nodo di contesto](context-node-types.md) .</span><span class="sxs-lookup"><span data-stu-id="1c24e-112">Types of nodes are described in the [Context Node Types](context-node-types.md) constants.</span></span>

## <a name="examples"></a><span data-ttu-id="1c24e-113">Esempio</span><span class="sxs-lookup"><span data-stu-id="1c24e-113">Examples</span></span>

<span data-ttu-id="1c24e-114">Nell'esempio seguente viene illustrato un metodo helper che recupera le informazioni su un nodo specificato, il relativo parametro *pContextNode* .</span><span class="sxs-lookup"><span data-stu-id="1c24e-114">The following example shows a helper method that retrieves information about a specified node, its *pContextNode* parameter.</span></span> <span data-ttu-id="1c24e-115">Questo metodo helper restituisce informazioni dai metodi seguenti.</span><span class="sxs-lookup"><span data-stu-id="1c24e-115">This helper method returns information from the following methods.</span></span>

-   [<span data-ttu-id="1c24e-116">**IContextNode:: GetId**</span><span class="sxs-lookup"><span data-stu-id="1c24e-116">**IContextNode::GetId**</span></span>](icontextnode-getid.md)
-   <span data-ttu-id="1c24e-117">**IContextNode:: GetType**</span><span class="sxs-lookup"><span data-stu-id="1c24e-117">**IContextNode::GetType**</span></span>
-   [<span data-ttu-id="1c24e-118">**IContextNode:: GetLocation**</span><span class="sxs-lookup"><span data-stu-id="1c24e-118">**IContextNode::GetLocation**</span></span>](icontextnode-getlocation.md)
-   [<span data-ttu-id="1c24e-119">**IContextNode:: GetParentNode**</span><span class="sxs-lookup"><span data-stu-id="1c24e-119">**IContextNode::GetParentNode**</span></span>](icontextnode-getparentnode.md)


```C++
// Helper method for collecting information about a context node.
HRESULT CMyClass::GetNodeInformation(
    IContextNode *pContextNode,
    GUID *pNodeIdentifier,
    GUID *pContextNodeType,
    IAnalysisRegion **ppAnalysisRegion,
    IContextNode **ppParentNode,
    IContextNodes **ppSubNodes)
{
    // Get the identifier of the context node.
    HRESULT hr = pContextNode->GetId(pNodeIdentifier);

    if (FAILED(hr))
    {
        return hr;
    }

    // Get the type identifier for the context node.
    hr = pContextNode->GetType(pContextNodeType);

    if (FAILED(hr))
    {
        return hr;
    }

    // Get the location of the context node.
    hr = pContextNode->GetLocation(ppAnalysisRegion);

    if (FAILED(hr))
    {
        return hr;
    }

    // Get the parent node of the context node.
    hr = pContextNode->GetParentNode(ppParentNode);

    if (FAILED(hr))
    {
        if ((*ppAnalysisRegion) != NULL)
        {
            (*ppAnalysisRegion)->Release();
            (*ppAnalysisRegion) = NULL;
        }
        return hr;
    }

    // Get the subnodes of the context node.
    hr = pContextNode->GetSubNodes(ppSubNodes);

    if (FAILED(hr))
    {
        if (*ppAnalysisRegion)
        {
            (*ppAnalysisRegion)->Release();
            (*ppAnalysisRegion) = NULL;
        }
        if (*ppParentNode)
        {
            (*ppParentNode)->Release();
            (*ppParentNode) = NULL;
        }
        return hr;
    }

    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="1c24e-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1c24e-120">Requirements</span></span>



| <span data-ttu-id="1c24e-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c24e-121">Requirement</span></span> | <span data-ttu-id="1c24e-122">Valore</span><span class="sxs-lookup"><span data-stu-id="1c24e-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c24e-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1c24e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="1c24e-124">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="1c24e-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="1c24e-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1c24e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="1c24e-126">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="1c24e-126">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="1c24e-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1c24e-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c24e-128"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="1c24e-128"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="1c24e-129">DLL</span><span class="sxs-lookup"><span data-stu-id="1c24e-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1c24e-130"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c24e-130"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="1c24e-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1c24e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c24e-132">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="1c24e-132">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="1c24e-133">Tipi di nodo di contesto</span><span class="sxs-lookup"><span data-stu-id="1c24e-133">Context Node Types</span></span>](context-node-types.md)
</dt> <dt>

[<span data-ttu-id="1c24e-134">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="1c24e-134">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




