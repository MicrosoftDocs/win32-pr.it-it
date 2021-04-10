---
description: Recupera l'identificatore per l'oggetto IContextNode.
ms.assetid: 7578bcc1-7c69-45fc-b3c2-7350ce4df99c
title: 'Metodo IContextNode:: GetId (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetId
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ef316111c7464bac0339a4888b887bc5cf20b93f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879362"
---
# <a name="icontextnodegetid-method"></a><span data-ttu-id="af92b-103">Metodo IContextNode:: GetId</span><span class="sxs-lookup"><span data-stu-id="af92b-103">IContextNode::GetId method</span></span>

<span data-ttu-id="af92b-104">Recupera l'identificatore per l'oggetto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="af92b-104">Retrieves the identifier for the [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="af92b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="af92b-105">Syntax</span></span>


```C++
HRESULT GetId(
  [out] GUID *pId
);
```



## <a name="parameters"></a><span data-ttu-id="af92b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="af92b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af92b-107">*PID* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="af92b-107">*pId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="af92b-108">Identificatore per l'oggetto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="af92b-108">The identifier for the [**IContextNode**](icontextnode.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af92b-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="af92b-109">Return value</span></span>

<span data-ttu-id="af92b-110">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="af92b-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="af92b-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="af92b-111">Remarks</span></span>

<span data-ttu-id="af92b-112">Ink Analyzer assegna un identificatore univoco a tutti i nodi di contesto creati.</span><span class="sxs-lookup"><span data-stu-id="af92b-112">The ink analyzer assigns a unique identifier to all context nodes it creates.</span></span> <span data-ttu-id="af92b-113">Durante l'analisi dell'input penna, Ink Analyzer può modificare l'identificatore per un nodo di contesto.</span><span class="sxs-lookup"><span data-stu-id="af92b-113">During ink analysis, the ink analyzer may change the identifier for a context node.</span></span> <span data-ttu-id="af92b-114">Ad esempio, Ink Analyzer può riclassificare un nodo di Word come due nodi di Word, quindi assegnare l'identificatore originale a uno e un nuovo identificatore all'altro.</span><span class="sxs-lookup"><span data-stu-id="af92b-114">For example, the ink analyzer may reclassify one word node as two word nodes and then assign the original identifier to one and a new identifier to the other.</span></span> <span data-ttu-id="af92b-115">In alternativa, è possibile che l'analizzatore di input penna riclassifichi due nodi di Word come un nodo di Word e assegnare uno degli identificatori originali al nuovo nodo di Word.</span><span class="sxs-lookup"><span data-stu-id="af92b-115">Or, the ink analyzer may reclassify two word nodes as one word node and assign one of the original identifiers to the new word node.</span></span>

## <a name="examples"></a><span data-ttu-id="af92b-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="af92b-116">Examples</span></span>

<span data-ttu-id="af92b-117">Nell'esempio seguente viene illustrato un metodo helper che recupera le informazioni su un nodo specificato, il relativo parametro *pContextNode* .</span><span class="sxs-lookup"><span data-stu-id="af92b-117">The following example shows a helper method that retrieves information about a specified node, its *pContextNode* parameter.</span></span> <span data-ttu-id="af92b-118">Questo metodo helper restituisce informazioni dai metodi seguenti.</span><span class="sxs-lookup"><span data-stu-id="af92b-118">This helper method returns information from the following methods.</span></span>

-   <span data-ttu-id="af92b-119">**IContextNode:: GetId**</span><span class="sxs-lookup"><span data-stu-id="af92b-119">**IContextNode::GetId**</span></span>
-   [<span data-ttu-id="af92b-120">**IContextNode:: GetType**</span><span class="sxs-lookup"><span data-stu-id="af92b-120">**IContextNode::GetType**</span></span>](icontextnode-gettype.md)
-   [<span data-ttu-id="af92b-121">**IContextNode:: GetLocation**</span><span class="sxs-lookup"><span data-stu-id="af92b-121">**IContextNode::GetLocation**</span></span>](icontextnode-getlocation.md)
-   [<span data-ttu-id="af92b-122">**IContextNode:: GetParentNode**</span><span class="sxs-lookup"><span data-stu-id="af92b-122">**IContextNode::GetParentNode**</span></span>](icontextnode-getparentnode.md)


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



## <a name="requirements"></a><span data-ttu-id="af92b-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="af92b-123">Requirements</span></span>



| <span data-ttu-id="af92b-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="af92b-124">Requirement</span></span> | <span data-ttu-id="af92b-125">Valore</span><span class="sxs-lookup"><span data-stu-id="af92b-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af92b-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="af92b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="af92b-127">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="af92b-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="af92b-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="af92b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="af92b-129">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="af92b-129">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="af92b-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="af92b-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="af92b-131"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="af92b-131"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="af92b-132">DLL</span><span class="sxs-lookup"><span data-stu-id="af92b-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="af92b-133"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="af92b-133"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="af92b-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="af92b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af92b-135">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="af92b-135">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="af92b-136">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="af92b-136">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




