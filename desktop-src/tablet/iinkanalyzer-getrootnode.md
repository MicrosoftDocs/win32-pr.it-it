---
description: Ottiene il IContextNode radice dell'albero del contesto dell'oggetto IInkAnalyzer.
ms.assetid: 6c073952-7962-4f38-89ae-f543e64e904f
title: 'Metodo IInkAnalyzer:: GetRootNode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetRootNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 280c1907558372d247f25a0f760990d7c3c53a07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307383"
---
# <a name="iinkanalyzergetrootnode-method"></a><span data-ttu-id="992a9-103">Metodo IInkAnalyzer:: GetRootNode</span><span class="sxs-lookup"><span data-stu-id="992a9-103">IInkAnalyzer::GetRootNode method</span></span>

<span data-ttu-id="992a9-104">Ottiene il [**IContextNode**](icontextnode.md) radice dell'albero del contesto dell'oggetto [**IInkAnalyzer**](iinkanalyzer.md) .</span><span class="sxs-lookup"><span data-stu-id="992a9-104">Gets the root [**IContextNode**](icontextnode.md) of the [**IInkAnalyzer**](iinkanalyzer.md) object's context tree.</span></span>

## <a name="syntax"></a><span data-ttu-id="992a9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="992a9-105">Syntax</span></span>


```C++
HRESULT GetRootNode(
  [out] IContextNode **ppRootNode
);
```



## <a name="parameters"></a><span data-ttu-id="992a9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="992a9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="992a9-107">*ppRootNode* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="992a9-107">*ppRootNode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="992a9-108">[**IContextNode**](icontextnode.md) radice dell'albero del contesto dell'oggetto [**IInkAnalyzer**](iinkanalyzer.md) .</span><span class="sxs-lookup"><span data-stu-id="992a9-108">The root [**IContextNode**](icontextnode.md) of the [**IInkAnalyzer**](iinkanalyzer.md) object's context tree.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="992a9-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="992a9-109">Return value</span></span>

<span data-ttu-id="992a9-110">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="992a9-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="992a9-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="992a9-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="992a9-112">Per evitare una perdita di memoria, chiamare [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su *ppRootNode* quando non è più necessario usare il nodo radice.</span><span class="sxs-lookup"><span data-stu-id="992a9-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppRootNode* when you no longer need to use the root node.</span></span>

 

<span data-ttu-id="992a9-113">[**IInkAnalyzer**](iinkanalyzer.md) gestisce un albero di oggetti [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="992a9-113">The [**IInkAnalyzer**](iinkanalyzer.md) maintains a tree of [**IContextNode**](icontextnode.md) objects.</span></span> <span data-ttu-id="992a9-114">Questi oggetti contengono sia l'input per l'analisi che i risultati dell'analisi.</span><span class="sxs-lookup"><span data-stu-id="992a9-114">These objects contain both input for analysis and the results of analysis.</span></span> <span data-ttu-id="992a9-115">Quando i tratti vengono inizialmente aggiunti a **IInkAnalyzer**, **IInkAnalyzer** li assegna a un **IContextNode** di tipo UnclassifiedInk (vedere i tipi di [nodo](context-node-types.md) [**IContextNode:: GetType**](icontextnode-gettype.md) e context).</span><span class="sxs-lookup"><span data-stu-id="992a9-115">When strokes are initially added to the **IInkAnalyzer**, the **IInkAnalyzer** assigns them to a **IContextNode** of type UnclassifiedInk (See [**IContextNode::GetType**](icontextnode-gettype.md) and [Context Node Types](context-node-types.md)).</span></span> <span data-ttu-id="992a9-116">Una volta analizzati i tratti, **IInkAnalyzer** li assegna agli oggetti **IContextNode** appropriati nell'albero.</span><span class="sxs-lookup"><span data-stu-id="992a9-116">After the strokes are analyzed, the **IInkAnalyzer** assigns them to appropriate **IContextNode** objects in the tree.</span></span> <span data-ttu-id="992a9-117">Per altre informazioni sull'uso di **IInkAnalyzer** per analizzare l'input penna, vedere [Cenni preliminari sull'analisi dell'input penna](ink-analysis-overview.md).</span><span class="sxs-lookup"><span data-stu-id="992a9-117">For more information about using the **IInkAnalyzer** to analyze ink, see [Ink Analysis Overview](ink-analysis-overview.md).</span></span>

## <a name="examples"></a><span data-ttu-id="992a9-118">Esempio</span><span class="sxs-lookup"><span data-stu-id="992a9-118">Examples</span></span>

<span data-ttu-id="992a9-119">Nell'esempio seguente viene illustrato un metodo che esamina l'albero dei risultati [**IContextNode**](icontextnode.md) dell'analizzatore di input penna.</span><span class="sxs-lookup"><span data-stu-id="992a9-119">The following example shows a method that walks the ink analyzer's [**IContextNode**](icontextnode.md) results tree.</span></span> <span data-ttu-id="992a9-120">Se il IInkAnlyzer non sta attualmente eseguendo l'analisi dell'input penna, il metodo esegue le operazioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="992a9-120">If the IInkAnlyzer is not currently performing ink analysis, the method does the following.</span></span>

-   <span data-ttu-id="992a9-121">Ottiene la stringa di riconoscimento superiore.</span><span class="sxs-lookup"><span data-stu-id="992a9-121">Gets the top recognition string.</span></span>
-   <span data-ttu-id="992a9-122">Ottiene il nodo radice dell'analizzatore di input penna.</span><span class="sxs-lookup"><span data-stu-id="992a9-122">Gets the ink analyzer's root node.</span></span>
-   <span data-ttu-id="992a9-123">Chiama un metodo helper, `ExploreContextNode` , per esaminare il nodo radice e i relativi nodi figlio.</span><span class="sxs-lookup"><span data-stu-id="992a9-123">Calls a helper method, `ExploreContextNode`, to examine the root node and its child nodes.</span></span>


```C++
// Helper method that explores the current analysis results of an ink analyzer.
HRESULT CMyClass::ExploreAnalysisResults(
    IInkAnalyzer *pInkAnalyzer)
{
    // Check that the ink analyzer is not currently analyzing ink.
    VARIANT_BOOL bIsAnalyzing;
    HRESULT hr = pInkAnalyzer->IsAnalyzing(&bIsAnalyzing);

    if (SUCCEEDED(hr))
    {
        if (bIsAnalyzing)
        {
            return E_PENDING;
        }

        // Get the ink analyzer's best-result string.
        BSTR recognizedString = NULL;
        hr = pInkAnalyzer->GetRecognizedString(&recognizedString);

        if (SUCCEEDED(hr))
        {
            // Insert code that records the ink analyzer's best-result string here.

            // Get the ink analyzer's root node.
            IContextNode *pRootNode = NULL;
            hr = pInkAnalyzer->GetRootNode(&pRootNode);

            if (SUCCEEDED(hr))
            {
                // Call a helper method that recursively explores context
                // nodes and their subnodes.
                hr = this->ExploreContextNode(pRootNode);
            }

            // Release this reference to the root node.
            if (pRootNode != NULL)
            {
                pRootNode->Release();
                pRootNode = NULL;
            }
        }

        // Free the system resources for the recognized string.
        SysFreeString(recognizedString);
    }

    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="992a9-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="992a9-124">Requirements</span></span>



| <span data-ttu-id="992a9-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="992a9-125">Requirement</span></span> | <span data-ttu-id="992a9-126">Valore</span><span class="sxs-lookup"><span data-stu-id="992a9-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="992a9-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="992a9-127">Minimum supported client</span></span><br/> | <span data-ttu-id="992a9-128">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="992a9-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="992a9-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="992a9-129">Minimum supported server</span></span><br/> | <span data-ttu-id="992a9-130">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="992a9-130">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="992a9-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="992a9-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="992a9-132"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="992a9-132"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="992a9-133">DLL</span><span class="sxs-lookup"><span data-stu-id="992a9-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="992a9-134"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="992a9-134"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="992a9-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="992a9-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="992a9-136">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="992a9-136">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="992a9-137">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="992a9-137">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="992a9-138">Tipi di nodo di contesto</span><span class="sxs-lookup"><span data-stu-id="992a9-138">Context Node Types</span></span>](context-node-types.md)
</dt> <dt>

[<span data-ttu-id="992a9-139">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="992a9-139">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

