---
description: Recupera la posizione e le dimensioni dell'oggetto IContextNode.
ms.assetid: 40787a9b-1017-4209-aec8-09b7332bfa8a
title: 'Metodo IContextNode:: GetLocation (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetLocation
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 13366442399961eaba7a411b1b3c87171f0879b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307437"
---
# <a name="icontextnodegetlocation-method"></a><span data-ttu-id="f0bbe-103">Metodo IContextNode:: GetLocation</span><span class="sxs-lookup"><span data-stu-id="f0bbe-103">IContextNode::GetLocation method</span></span>

<span data-ttu-id="f0bbe-104">Recupera la posizione e le dimensioni dell'oggetto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="f0bbe-104">Retrieves the position and size of the [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0bbe-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f0bbe-105">Syntax</span></span>


```C++
HRESULT GetLocation(
  [out] IAnalysisRegion **ppIAnalysisRegion
);
```



## <a name="parameters"></a><span data-ttu-id="f0bbe-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f0bbe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0bbe-107">*ppIAnalysisRegion* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f0bbe-107">*ppIAnalysisRegion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0bbe-108">Puntatore alla posizione e alle dimensioni dell'oggetto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="f0bbe-108">A pointer to the position and size of the [**IContextNode**](icontextnode.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0bbe-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f0bbe-109">Return value</span></span>

<span data-ttu-id="f0bbe-110">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="f0bbe-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f0bbe-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="f0bbe-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="f0bbe-112">Per evitare una perdita di memoria, chiamare [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su \* *ppIAnalysisRegion* quando non è più necessario usare l'area di analisi.</span><span class="sxs-lookup"><span data-stu-id="f0bbe-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppIAnalysisRegion* when you no longer need to use the analysis region.</span></span>

 

<span data-ttu-id="f0bbe-113">Il percorso di un nodo del contenitore viene determinato individuando l'Unione di tutte le posizioni foglia.</span><span class="sxs-lookup"><span data-stu-id="f0bbe-113">The location for a container node is determined by finding the union of all the leaf's locations.</span></span> <span data-ttu-id="f0bbe-114">La posizione di un nodo foglia dell'input penna è determinata dalla ricerca dell'Unione del rettangolo di delimitazione dei tratti associati.</span><span class="sxs-lookup"><span data-stu-id="f0bbe-114">The location for an ink leaf node is determined by finding the union of the bounding box of the associated strokes.</span></span> <span data-ttu-id="f0bbe-115">Il percorso di un nodo foglia non input penna viene impostato al momento della creazione del nodo e può essere aggiornato con [**IContextNode:: selocation**](icontextnode-setlocation.md).</span><span class="sxs-lookup"><span data-stu-id="f0bbe-115">The location for a non-ink leaf node is set when the node is created and can be updated using [**IContextNode::SetLocation**](icontextnode-setlocation.md).</span></span>

## <a name="examples"></a><span data-ttu-id="f0bbe-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="f0bbe-116">Examples</span></span>

<span data-ttu-id="f0bbe-117">Nell'esempio seguente viene illustrato un metodo helper che recupera le informazioni su un nodo specificato, il relativo parametro *pContextNode* .</span><span class="sxs-lookup"><span data-stu-id="f0bbe-117">The following example shows a helper method that retrieves information about a specified node, its *pContextNode* parameter.</span></span> <span data-ttu-id="f0bbe-118">Questo metodo helper restituisce informazioni dai metodi seguenti.</span><span class="sxs-lookup"><span data-stu-id="f0bbe-118">This helper method returns information from the following methods.</span></span>

-   [<span data-ttu-id="f0bbe-119">**IContextNode:: GetId**</span><span class="sxs-lookup"><span data-stu-id="f0bbe-119">**IContextNode::GetId**</span></span>](icontextnode-getid.md)
-   [<span data-ttu-id="f0bbe-120">**IContextNode:: GetType**</span><span class="sxs-lookup"><span data-stu-id="f0bbe-120">**IContextNode::GetType**</span></span>](icontextnode-gettype.md)
-   <span data-ttu-id="f0bbe-121">**IContextNode:: GetLocation**</span><span class="sxs-lookup"><span data-stu-id="f0bbe-121">**IContextNode::GetLocation**</span></span>
-   [<span data-ttu-id="f0bbe-122">**IContextNode:: GetParentNode**</span><span class="sxs-lookup"><span data-stu-id="f0bbe-122">**IContextNode::GetParentNode**</span></span>](icontextnode-getparentnode.md)


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



## <a name="requirements"></a><span data-ttu-id="f0bbe-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f0bbe-123">Requirements</span></span>



| <span data-ttu-id="f0bbe-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0bbe-124">Requirement</span></span> | <span data-ttu-id="f0bbe-125">Valore</span><span class="sxs-lookup"><span data-stu-id="f0bbe-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0bbe-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f0bbe-126">Minimum supported client</span></span><br/> | <span data-ttu-id="f0bbe-127">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="f0bbe-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f0bbe-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f0bbe-128">Minimum supported server</span></span><br/> | <span data-ttu-id="f0bbe-129">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="f0bbe-129">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="f0bbe-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f0bbe-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0bbe-131"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="f0bbe-131"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="f0bbe-132">DLL</span><span class="sxs-lookup"><span data-stu-id="f0bbe-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f0bbe-133"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f0bbe-133"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="f0bbe-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f0bbe-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0bbe-135">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="f0bbe-135">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="f0bbe-136">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="f0bbe-136">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="f0bbe-137">**IContextNode:: selocation**</span><span class="sxs-lookup"><span data-stu-id="f0bbe-137">**IContextNode::SetLocation**</span></span>](icontextnode-setlocation.md)
</dt> <dt>

[<span data-ttu-id="f0bbe-138">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="f0bbe-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

