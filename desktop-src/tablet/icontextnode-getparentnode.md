---
description: Recupera il nodo padre di questo IContextNode nell'albero del nodo di contesto.
ms.assetid: 782fd973-f8f3-4902-b8e0-cc5e70a66d28
title: 'Metodo IContextNode:: GetParentNode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetParentNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 50bba716486910802e91cbe6d3f003d172f1cb29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526527"
---
# <a name="icontextnodegetparentnode-method"></a><span data-ttu-id="ccf41-103">Metodo IContextNode:: GetParentNode</span><span class="sxs-lookup"><span data-stu-id="ccf41-103">IContextNode::GetParentNode method</span></span>

<span data-ttu-id="ccf41-104">Recupera il nodo padre di questo [**IContextNode**](icontextnode.md) nell'albero del nodo di contesto.</span><span class="sxs-lookup"><span data-stu-id="ccf41-104">Retrieves the parent node of this [**IContextNode**](icontextnode.md) in the context node tree.</span></span>

## <a name="syntax"></a><span data-ttu-id="ccf41-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ccf41-105">Syntax</span></span>


```C++
HRESULT GetParentNode(
  [out] IContextNode **ppParentContextNode
);
```



## <a name="parameters"></a><span data-ttu-id="ccf41-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ccf41-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ccf41-107">*ppParentContextNode* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ccf41-107">*ppParentContextNode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ccf41-108">Puntatore al nodo padre di questo oggetto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="ccf41-108">A pointer to the parent node of this [**IContextNode**](icontextnode.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ccf41-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ccf41-109">Return value</span></span>

<span data-ttu-id="ccf41-110">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="ccf41-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ccf41-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="ccf41-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="ccf41-112">Per evitare una perdita di memoria, chiamare [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su \* *ppParentContextNode* quando non è più necessario usare il nodo di contesto padre.</span><span class="sxs-lookup"><span data-stu-id="ccf41-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppParentContextNode* when you no longer need to use the parent context node.</span></span>

 

<span data-ttu-id="ccf41-113">Se si tratta del nodo radice, il parametro *ppParentContextNode* è impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="ccf41-113">If this is the root node, the *ppParentContextNode* parameter is set to **NULL**.</span></span>

## <a name="examples"></a><span data-ttu-id="ccf41-114">Esempio</span><span class="sxs-lookup"><span data-stu-id="ccf41-114">Examples</span></span>

<span data-ttu-id="ccf41-115">Nell'esempio seguente viene illustrato un metodo helper che recupera le informazioni su un nodo specificato, il relativo parametro *pContextNode* .</span><span class="sxs-lookup"><span data-stu-id="ccf41-115">The following example shows a helper method that retrieves information about a specified node, its *pContextNode* parameter.</span></span> <span data-ttu-id="ccf41-116">Questo metodo helper restituisce informazioni dai metodi seguenti.</span><span class="sxs-lookup"><span data-stu-id="ccf41-116">This helper method returns information from the following methods.</span></span>

-   [<span data-ttu-id="ccf41-117">**IContextNode:: GetId**</span><span class="sxs-lookup"><span data-stu-id="ccf41-117">**IContextNode::GetId**</span></span>](icontextnode-getid.md)
-   [<span data-ttu-id="ccf41-118">**IContextNode:: GetType**</span><span class="sxs-lookup"><span data-stu-id="ccf41-118">**IContextNode::GetType**</span></span>](icontextnode-gettype.md)
-   [<span data-ttu-id="ccf41-119">**IContextNode:: GetLocation**</span><span class="sxs-lookup"><span data-stu-id="ccf41-119">**IContextNode::GetLocation**</span></span>](icontextnode-getlocation.md)
-   <span data-ttu-id="ccf41-120">**IContextNode:: GetParentNode**</span><span class="sxs-lookup"><span data-stu-id="ccf41-120">**IContextNode::GetParentNode**</span></span>


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



## <a name="requirements"></a><span data-ttu-id="ccf41-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ccf41-121">Requirements</span></span>



| <span data-ttu-id="ccf41-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="ccf41-122">Requirement</span></span> | <span data-ttu-id="ccf41-123">Valore</span><span class="sxs-lookup"><span data-stu-id="ccf41-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ccf41-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ccf41-124">Minimum supported client</span></span><br/> | <span data-ttu-id="ccf41-125">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="ccf41-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ccf41-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ccf41-126">Minimum supported server</span></span><br/> | <span data-ttu-id="ccf41-127">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="ccf41-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="ccf41-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ccf41-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="ccf41-129"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="ccf41-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="ccf41-130">DLL</span><span class="sxs-lookup"><span data-stu-id="ccf41-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ccf41-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ccf41-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="ccf41-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ccf41-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccf41-133">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="ccf41-133">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="ccf41-134">**IContextNode::GetSubNodes**</span><span class="sxs-lookup"><span data-stu-id="ccf41-134">**IContextNode::GetSubNodes**</span></span>](icontextnode-getsubnodes.md)
</dt> <dt>

[<span data-ttu-id="ccf41-135">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="ccf41-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

