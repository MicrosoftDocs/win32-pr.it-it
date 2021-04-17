---
description: Ottiene il numero di tratti associati all'oggetto IContextNode.
ms.assetid: bb3c1cb3-dcf6-4465-b1bc-5c613e9747da
title: 'Metodo IContextNode:: GetStrokeCount (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetStrokeCount
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 2652168fa2846995aeb17ec23c194f908f22e5d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485108"
---
# <a name="icontextnodegetstrokecount-method"></a><span data-ttu-id="3c963-103">Metodo IContextNode:: GetStrokeCount</span><span class="sxs-lookup"><span data-stu-id="3c963-103">IContextNode::GetStrokeCount method</span></span>

<span data-ttu-id="3c963-104">Ottiene il numero di tratti associati all'oggetto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="3c963-104">Gets the number of strokes associated with the [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c963-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3c963-105">Syntax</span></span>


```C++
HRESULT GetStrokeCount(
  [out] ULONG *pulStrokeCount
);
```



## <a name="parameters"></a><span data-ttu-id="3c963-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3c963-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c963-107">*pulStrokeCount* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3c963-107">*pulStrokeCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3c963-108">Numero di tratti associati all'oggetto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="3c963-108">The number of strokes associated with the [**IContextNode**](icontextnode.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c963-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3c963-109">Return value</span></span>

<span data-ttu-id="3c963-110">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="3c963-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3c963-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="3c963-111">Remarks</span></span>

<span data-ttu-id="3c963-112">Solo i nodi di contesto foglia input penna hanno dati di tratto associati (vedere [**IContextNode:: GetType**](icontextnode-gettype.md)).</span><span class="sxs-lookup"><span data-stu-id="3c963-112">Only ink leaf context nodes have associated stroke data (see [**IContextNode::GetType**](icontextnode-gettype.md)).</span></span>

## <a name="examples"></a><span data-ttu-id="3c963-113">Esempio</span><span class="sxs-lookup"><span data-stu-id="3c963-113">Examples</span></span>

<span data-ttu-id="3c963-114">Questo esempio illustra un metodo, `ExploreContextNode` , che esamina un [**IContextNode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="3c963-114">This example shows a method, `ExploreContextNode`, that examines an [**IContextNode**](icontextnode.md).</span></span> <span data-ttu-id="3c963-115">Il metodo esegue le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="3c963-115">The method does the following:</span></span>

-   <span data-ttu-id="3c963-116">Ottiene il tipo del nodo di contesto.</span><span class="sxs-lookup"><span data-stu-id="3c963-116">Gets the context node's type.</span></span>
-   <span data-ttu-id="3c963-117">Esamina le proprietà specifiche del tipo di nodo chiamando un metodo di supporto, se il nodo di contesto è un input penna non classificato, un hint di analisi o un nodo di riconoscimento personalizzato.</span><span class="sxs-lookup"><span data-stu-id="3c963-117">Examines specific properties of the node type by calling a helper method, if the context node is an unclassified ink, analysis hint, or custom recognizer node.</span></span>
-   <span data-ttu-id="3c963-118">Esamina ogni sottonodo chiamando se nel nodo sono presenti sottonodi.</span><span class="sxs-lookup"><span data-stu-id="3c963-118">Examines each subnode by calling itself, if the node has subnodes.</span></span>
-   <span data-ttu-id="3c963-119">Esamina i dati del tratto per il nodo chiamando un metodo di supporto, se il nodo è un nodo foglia dell'input penna.</span><span class="sxs-lookup"><span data-stu-id="3c963-119">Examines the stroke data for the node by calling a helper method, if the node is an ink leaf node.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="3c963-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3c963-120">Requirements</span></span>



| <span data-ttu-id="3c963-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c963-121">Requirement</span></span> | <span data-ttu-id="3c963-122">Valore</span><span class="sxs-lookup"><span data-stu-id="3c963-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c963-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3c963-123">Minimum supported client</span></span><br/> | <span data-ttu-id="3c963-124">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="3c963-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="3c963-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3c963-125">Minimum supported server</span></span><br/> | <span data-ttu-id="3c963-126">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="3c963-126">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="3c963-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3c963-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c963-128"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="3c963-128"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="3c963-129">DLL</span><span class="sxs-lookup"><span data-stu-id="3c963-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c963-130"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c963-130"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="3c963-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3c963-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c963-132">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="3c963-132">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="3c963-133">**IContextNode:: GetStrokeIds**</span><span class="sxs-lookup"><span data-stu-id="3c963-133">**IContextNode::GetStrokeIds**</span></span>](icontextnode-getstrokeids.md)
</dt> <dt>

[<span data-ttu-id="3c963-134">**IContextNode::GetStrokeId**</span><span class="sxs-lookup"><span data-stu-id="3c963-134">**IContextNode::GetStrokeId**</span></span>](icontextnode-getstrokeid.md)
</dt> <dt>

[<span data-ttu-id="3c963-135">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="3c963-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




