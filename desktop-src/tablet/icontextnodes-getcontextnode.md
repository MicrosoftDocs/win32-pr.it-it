---
description: Recupera l'oggetto IContextNode in corrispondenza dell'indice specificato all'interno di questa raccolta.
ms.assetid: 4b266512-9e58-43d2-8430-68310230fc27
title: 'Metodo IContextNodes:: getcontextnode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNodes.GetContextNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ec907fdcac5a1ed18cca54c79a876959868f2ecc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485100"
---
# <a name="icontextnodesgetcontextnode-method"></a><span data-ttu-id="546bf-103">Metodo IContextNodes:: getcontextnode</span><span class="sxs-lookup"><span data-stu-id="546bf-103">IContextNodes::GetContextNode method</span></span>

<span data-ttu-id="546bf-104">Recupera l'oggetto [**IContextNode**](icontextnode.md) in corrispondenza dell'indice specificato all'interno di questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="546bf-104">Retrieves the [**IContextNode**](icontextnode.md) object at the specified index within this collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="546bf-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="546bf-105">Syntax</span></span>


```C++
HRESULT GetContextNode(
  [in]  ULONG        ulIndex,
  [out] IContextNode **ppContextNode
);
```



## <a name="parameters"></a><span data-ttu-id="546bf-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="546bf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="546bf-107">*ulIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="546bf-107">*ulIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="546bf-108">Indice in base zero dell'oggetto [**IContextNode**](icontextnode.md) da ottenere.</span><span class="sxs-lookup"><span data-stu-id="546bf-108">The zero-based index of the [**IContextNode**](icontextnode.md) object to get.</span></span>

</dd> <dt>

<span data-ttu-id="546bf-109">*ppContextNode* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="546bf-109">*ppContextNode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="546bf-110">Puntatore a [**IContextNode**](icontextnode.md) a cui si fa riferimento in corrispondenza dell'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="546bf-110">Pointer to the [**IContextNode**](icontextnode.md) referenced at the specified index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="546bf-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="546bf-111">Return value</span></span>

<span data-ttu-id="546bf-112">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="546bf-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="546bf-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="546bf-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="546bf-114">Per evitare una perdita di memoria, chiamare [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su \* *ppContextNode* quando non è più necessario usare il nodo di contesto.</span><span class="sxs-lookup"><span data-stu-id="546bf-114">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppContextNode* when you no longer need to use the context node.</span></span>

 

## <a name="examples"></a><span data-ttu-id="546bf-115">Esempio</span><span class="sxs-lookup"><span data-stu-id="546bf-115">Examples</span></span>

<span data-ttu-id="546bf-116">Questo esempio illustra un metodo, `ExploreContextNode` , che esamina un [**IContextNode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="546bf-116">This example shows a method, `ExploreContextNode`, that examines an [**IContextNode**](icontextnode.md).</span></span> <span data-ttu-id="546bf-117">Il metodo esegue le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="546bf-117">The method does the following:</span></span>

-   <span data-ttu-id="546bf-118">Ottiene il tipo del nodo di contesto.</span><span class="sxs-lookup"><span data-stu-id="546bf-118">Gets the context node's type.</span></span>
-   <span data-ttu-id="546bf-119">Esamina le proprietà specifiche del tipo di nodo chiamando un metodo di supporto, se il nodo di contesto è un input penna non classificato, un hint di analisi o un nodo di riconoscimento personalizzato.</span><span class="sxs-lookup"><span data-stu-id="546bf-119">Examines specific properties of the node type by calling a helper method, if the context node is an unclassified ink, analysis hint, or custom recognizer node.</span></span>
-   <span data-ttu-id="546bf-120">Esamina ogni sottonodo chiamando se nel nodo sono presenti sottonodi.</span><span class="sxs-lookup"><span data-stu-id="546bf-120">Examines each subnode by calling itself, if the node has subnodes.</span></span>
-   <span data-ttu-id="546bf-121">Esamina i dati del tratto per il nodo chiamando un metodo di supporto, se il nodo è un nodo foglia dell'input penna.</span><span class="sxs-lookup"><span data-stu-id="546bf-121">Examines the stroke data for the node by calling a helper method, if the node is an ink leaf node.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="546bf-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="546bf-122">Requirements</span></span>



| <span data-ttu-id="546bf-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="546bf-123">Requirement</span></span> | <span data-ttu-id="546bf-124">Valore</span><span class="sxs-lookup"><span data-stu-id="546bf-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="546bf-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="546bf-125">Minimum supported client</span></span><br/> | <span data-ttu-id="546bf-126">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="546bf-126">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="546bf-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="546bf-127">Minimum supported server</span></span><br/> | <span data-ttu-id="546bf-128">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="546bf-128">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="546bf-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="546bf-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="546bf-130"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="546bf-130"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="546bf-131">DLL</span><span class="sxs-lookup"><span data-stu-id="546bf-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="546bf-132"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="546bf-132"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="546bf-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="546bf-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="546bf-134">**IContextNodes**</span><span class="sxs-lookup"><span data-stu-id="546bf-134">**IContextNodes**</span></span>](icontextnodes.md)
</dt> <dt>

[<span data-ttu-id="546bf-135">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="546bf-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

