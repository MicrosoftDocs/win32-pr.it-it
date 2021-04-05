---
description: Recupera la stringa di risultato migliore dell'operazione di riconoscimento per l'intero albero del nodo di contesto in IInkAnalyzer.
ms.assetid: 4aa57f41-3122-47a9-a60d-4a229e23f63c
title: 'Metodo IInkAnalyzer:: GetRecognizedString (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetRecognizedString
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 67afe9909fcabb8df880706b2b077ea602ccade6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751807"
---
# <a name="iinkanalyzergetrecognizedstring-method"></a><span data-ttu-id="46cdf-103">Metodo IInkAnalyzer:: GetRecognizedString</span><span class="sxs-lookup"><span data-stu-id="46cdf-103">IInkAnalyzer::GetRecognizedString method</span></span>

<span data-ttu-id="46cdf-104">Recupera la stringa di risultato migliore dell'operazione di riconoscimento per l'intero albero del nodo di contesto in [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="46cdf-104">Retrieves the best-result string of the recognition operation for the entire context node tree in the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="46cdf-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="46cdf-105">Syntax</span></span>


```C++
HRESULT GetRecognizedString(
  [out] BSTR *pbstrRecognizedString
);
```



## <a name="parameters"></a><span data-ttu-id="46cdf-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="46cdf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46cdf-107">*pbstrRecognizedString* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="46cdf-107">*pbstrRecognizedString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="46cdf-108">Stringa di risultato migliore dell'operazione di riconoscimento per l'intero albero del nodo di contesto in [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="46cdf-108">The best-result string of the recognition operation for the entire context node tree in the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46cdf-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="46cdf-109">Return value</span></span>

<span data-ttu-id="46cdf-110">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="46cdf-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="46cdf-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="46cdf-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="46cdf-112">Per evitare una perdita di memoria, chiamare [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) per *pbstrRecognizedString* quando non è più necessario usare la stringa.</span><span class="sxs-lookup"><span data-stu-id="46cdf-112">To avoid a memory leak, call [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) for *pbstrRecognizedString* when you no longer need to use the string.</span></span>

 

<span data-ttu-id="46cdf-113">Questo metodo restituisce lo stesso valore dei dati della proprietà del nodo radice per la stringa riconosciuta.</span><span class="sxs-lookup"><span data-stu-id="46cdf-113">This method returns the same value as the root node's property data for the recognized string.</span></span> <span data-ttu-id="46cdf-114">(Vedere il [**Metodo IInkAnalyzer:: GetRootNode**](iinkanalyzer-getrootnode.md), [**IContextNode:: GetPropertyData**](icontextnode-getpropertydata.md)e le [proprietà del nodo di contesto](context-node-properties.md)).</span><span class="sxs-lookup"><span data-stu-id="46cdf-114">(See [**IInkAnalyzer::GetRootNode Method**](iinkanalyzer-getrootnode.md), [**IContextNode::GetPropertyData**](icontextnode-getpropertydata.md), and [Context Node Properties](context-node-properties.md).)</span></span>

## <a name="examples"></a><span data-ttu-id="46cdf-115">Esempio</span><span class="sxs-lookup"><span data-stu-id="46cdf-115">Examples</span></span>

<span data-ttu-id="46cdf-116">Nell'esempio seguente viene illustrato un metodo che esamina l'albero dei risultati [**IContextNode**](icontextnode.md) dell'analizzatore di input penna.</span><span class="sxs-lookup"><span data-stu-id="46cdf-116">The following example shows a method that walks the ink analyzer's [**IContextNode**](icontextnode.md) results tree.</span></span> <span data-ttu-id="46cdf-117">Se il IInkAnlyzer non sta attualmente eseguendo l'analisi dell'input penna, il metodo esegue le operazioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="46cdf-117">If the IInkAnlyzer is not currently performing ink analysis, the method does the following.</span></span>

-   <span data-ttu-id="46cdf-118">Ottiene la stringa di riconoscimento superiore.</span><span class="sxs-lookup"><span data-stu-id="46cdf-118">Gets the top recognition string.</span></span>
-   <span data-ttu-id="46cdf-119">Ottiene il nodo radice dell'analizzatore di input penna.</span><span class="sxs-lookup"><span data-stu-id="46cdf-119">Gets the ink analyzer's root node.</span></span>
-   <span data-ttu-id="46cdf-120">Chiama un metodo helper, `ExploreContextNode` , per esaminare il nodo radice e i relativi nodi figlio.</span><span class="sxs-lookup"><span data-stu-id="46cdf-120">Calls a helper method, `ExploreContextNode`, to examine the root node and its child nodes.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="46cdf-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="46cdf-121">Requirements</span></span>



| <span data-ttu-id="46cdf-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="46cdf-122">Requirement</span></span> | <span data-ttu-id="46cdf-123">Valore</span><span class="sxs-lookup"><span data-stu-id="46cdf-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46cdf-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="46cdf-124">Minimum supported client</span></span><br/> | <span data-ttu-id="46cdf-125">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="46cdf-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="46cdf-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="46cdf-126">Minimum supported server</span></span><br/> | <span data-ttu-id="46cdf-127">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="46cdf-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="46cdf-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="46cdf-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="46cdf-129"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="46cdf-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="46cdf-130">DLL</span><span class="sxs-lookup"><span data-stu-id="46cdf-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46cdf-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="46cdf-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="46cdf-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="46cdf-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46cdf-133">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="46cdf-133">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="46cdf-134">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="46cdf-134">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

