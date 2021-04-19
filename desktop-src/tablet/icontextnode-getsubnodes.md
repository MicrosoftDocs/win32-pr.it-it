---
description: Ottiene i nodi figlio diretti dell'oggetto IContextNode.
ms.assetid: 50ce2fa4-031e-42e9-8e47-c0d3c2d2b4df
title: 'Metodo IContextNode:: GetSubNodes (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetSubNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 5c0526ca4a5b4db355c1f895a44ebbf634cb8bc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307429"
---
# <a name="icontextnodegetsubnodes-method"></a><span data-ttu-id="067b1-103">Metodo IContextNode:: GetSubNodes</span><span class="sxs-lookup"><span data-stu-id="067b1-103">IContextNode::GetSubNodes method</span></span>

<span data-ttu-id="067b1-104">Ottiene i nodi figlio diretti dell'oggetto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="067b1-104">Gets the direct child nodes of the [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="067b1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="067b1-105">Syntax</span></span>


```C++
HRESULT GetSubNodes(
  [out] IContextNodes **ppSubContextNodes
);
```



## <a name="parameters"></a><span data-ttu-id="067b1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="067b1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="067b1-107">*ppSubContextNodes* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="067b1-107">*ppSubContextNodes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="067b1-108">Raccolta di oggetti [**IContextNode**](icontextnode.md) che sono nodi figlio diretti di questo **IContextNode**.</span><span class="sxs-lookup"><span data-stu-id="067b1-108">A collection of the [**IContextNode**](icontextnode.md) objects that are direct child nodes of this **IContextNode**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="067b1-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="067b1-109">Return value</span></span>

<span data-ttu-id="067b1-110">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="067b1-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="067b1-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="067b1-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="067b1-112">Per evitare una perdita di memoria, chiamare [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su \* *ppSubContextNodes* quando non è più necessario usare la raccolta di sottonodi.</span><span class="sxs-lookup"><span data-stu-id="067b1-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppSubContextNodes* when you no longer need to use the collection of subnodes.</span></span>

 

<span data-ttu-id="067b1-113">Vengono restituiti solo i nodi figlio diretti, non tutti i nodi discendenti.</span><span class="sxs-lookup"><span data-stu-id="067b1-113">This returns only the direct child nodes, not all of the descendant nodes.</span></span>

## <a name="examples"></a><span data-ttu-id="067b1-114">Esempio</span><span class="sxs-lookup"><span data-stu-id="067b1-114">Examples</span></span>

<span data-ttu-id="067b1-115">Questo esempio illustra un metodo, `ExploreContextNode` , che esamina un [**IContextNode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="067b1-115">This example shows a method, `ExploreContextNode`, that examines an [**IContextNode**](icontextnode.md).</span></span> <span data-ttu-id="067b1-116">Il metodo esegue le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="067b1-116">The method does the following:</span></span>

-   <span data-ttu-id="067b1-117">Ottiene il tipo del nodo di contesto.</span><span class="sxs-lookup"><span data-stu-id="067b1-117">Gets the context node's type.</span></span>
-   <span data-ttu-id="067b1-118">Esamina le proprietà specifiche del tipo di nodo chiamando un metodo di supporto, se il nodo di contesto è un input penna non classificato, un hint di analisi o un nodo di riconoscimento personalizzato.</span><span class="sxs-lookup"><span data-stu-id="067b1-118">Examines specific properties of the node type by calling a helper method, if the context node is an unclassified ink, analysis hint, or custom recognizer node.</span></span>
-   <span data-ttu-id="067b1-119">Esamina ogni sottonodo chiamando se nel nodo sono presenti sottonodi.</span><span class="sxs-lookup"><span data-stu-id="067b1-119">Examines each subnode by calling itself, if the node has subnodes.</span></span>
-   <span data-ttu-id="067b1-120">Esamina i dati del tratto per il nodo chiamando un metodo di supporto, se il nodo è un nodo foglia dell'input penna.</span><span class="sxs-lookup"><span data-stu-id="067b1-120">Examines the stroke data for the node by calling a helper method, if the node is an ink leaf node.</span></span>


```C++
HRESULT CMyClass::ExploreContextNode(
    IContextNode *pContextNode)
{
    // Check for certain types of context nodes.
    GUID ContextNodeType;
    HRESULT hr = pContextNode->GetType(&ContextNodeType);

    if (SUCCEEDED(hr))
    {
        if (IsEqualGUID(GUID_CNT_UNCLASSIFIEDINK, ContextNodeType))
        {
            // Call a helper method that explores unclassified ink nodes.
            hr = this->ExploreUnclassifiedInkNode(pContextNode);
        }
        else if (IsEqualGUID(GUID_CNT_ANALYSISHINT, ContextNodeType))
        {
            // Call a helper method that explores analysis hint nodes.
            hr = this->ExploreAnalysisHintNode(pContextNode);
        }
        else if (IsEqualGUID(GUID_CNT_CUSTOMRECOGNIZER, ContextNodeType))
        {
            // Call a helper method that explores custom recognizer nodes.
            hr = this->ExploreCustomRecognizerNode(pContextNode);
        }

        if (SUCCEEDED(hr))
        {
            // Check if this node is a branch or a leaf node.
            IContextNodes *pSubNodes = NULL;
            hr = pContextNode->GetSubNodes(&pSubNodes);

            if (SUCCEEDED(hr))
            {
                ULONG ulSubNodeCount;
                hr = pSubNodes->GetCount(&ulSubNodeCount);

                if (SUCCEEDED(hr))
                {
                    if (ulSubNodeCount > 0)
                    {
                        // This node has child nodes; explore each child node.
                        IContextNode *pSubNode = NULL;
                        for (ULONG index=0; index<ulSubNodeCount; index++)
                        {
                            hr = pSubNodes->GetContextNode(index, &pSubNode);

                            if (SUCCEEDED(hr))
                            {
                                // Recursive call to explore the child node of this
                                // context node.
                                hr = this->ExploreContextNode(pSubNode);
                            }

                            // Release this reference to the child context node.
                            if (pSubNode != NULL)
                            {
                                pSubNode->Release();
                                pSubNode = NULL;
                            }

                            if (FAILED(hr))
                            {
                                break;
                            }
                        }
                    }
                    else
                    {
                        // This is a leaf node. Check if it contains stroke data.
                        ULONG ulStrokeCount;
                        hr = pContextNode->GetStrokeCount(&ulStrokeCount);

                        if (SUCCEEDED(hr))
                        {
                            if (ulStrokeCount > 0)
                            {
                                // This node is an ink leaf node; call helper
                                // method that explores available stroke data.
                                hr = this->ExploreNodeStrokeData(pContextNode);
                            }
                        }
                    }
                }
            }

            // Release this reference to the subnodes collection.
            if (pSubNodes != NULL)
            {
                pSubNodes->Release();
                pSubNodes = NULL;
            }
        }
    }

    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="067b1-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="067b1-121">Requirements</span></span>



| <span data-ttu-id="067b1-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="067b1-122">Requirement</span></span> | <span data-ttu-id="067b1-123">Valore</span><span class="sxs-lookup"><span data-stu-id="067b1-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="067b1-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="067b1-124">Minimum supported client</span></span><br/> | <span data-ttu-id="067b1-125">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="067b1-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="067b1-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="067b1-126">Minimum supported server</span></span><br/> | <span data-ttu-id="067b1-127">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="067b1-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="067b1-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="067b1-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="067b1-129"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="067b1-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="067b1-130">DLL</span><span class="sxs-lookup"><span data-stu-id="067b1-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="067b1-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="067b1-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="067b1-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="067b1-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="067b1-133">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="067b1-133">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="067b1-134">**IContextNode:: GetParentNode**</span><span class="sxs-lookup"><span data-stu-id="067b1-134">**IContextNode::GetParentNode**</span></span>](icontextnode-getparentnode.md)
</dt> <dt>

[<span data-ttu-id="067b1-135">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="067b1-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

