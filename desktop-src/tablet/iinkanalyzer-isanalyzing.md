---
description: Recupera un valore che indica se IInkAnalyzer esegue l'analisi dell'input penna.
ms.assetid: 3f3f6f29-0c90-47e1-938c-f1ce6ed8df47
title: 'Metodo IInkAnalyzer:: overanalyzing (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.IsAnalyzing
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 94275d157b2936b7ad0ae16d4d70b62475f19af9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526490"
---
# <a name="iinkanalyzerisanalyzing-method"></a><span data-ttu-id="88366-103">Metodo IInkAnalyzer:: overanalyzing</span><span class="sxs-lookup"><span data-stu-id="88366-103">IInkAnalyzer::IsAnalyzing method</span></span>

<span data-ttu-id="88366-104">Recupera un valore che indica se [**IInkAnalyzer**](iinkanalyzer.md) esegue l'analisi dell'input penna.</span><span class="sxs-lookup"><span data-stu-id="88366-104">Retrieves a value indicating whether the [**IInkAnalyzer**](iinkanalyzer.md) is performing ink analysis.</span></span>

## <a name="syntax"></a><span data-ttu-id="88366-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="88366-105">Syntax</span></span>


```C++
HRESULT IsAnalyzing(
  [out] VARIANT_BOOL *pbAnalyzing
);
```



## <a name="parameters"></a><span data-ttu-id="88366-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="88366-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88366-107">*pbAnalyzing* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="88366-107">*pbAnalyzing* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="88366-108">**Variante \_ TRUE** se [**IInkAnalyzer**](iinkanalyzer.md) esegue l'analisi dell'input penna; in caso contrario, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="88366-108">**VARIANT\_TRUE** if the [**IInkAnalyzer**](iinkanalyzer.md) is performing ink analysis; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88366-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="88366-109">Return value</span></span>

<span data-ttu-id="88366-110">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="88366-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="88366-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="88366-111">Remarks</span></span>

<span data-ttu-id="88366-112">Questa proprietà è una **variante \_ true** se [**IInkAnalyzer**](iinkanalyzer.md) esegue l'analisi sincrona o asincrona.</span><span class="sxs-lookup"><span data-stu-id="88366-112">This property is **VARIANT\_TRUE** if the [**IInkAnalyzer**](iinkanalyzer.md) is performing synchronous or asynchronous analysis.</span></span>

## <a name="examples"></a><span data-ttu-id="88366-113">Esempio</span><span class="sxs-lookup"><span data-stu-id="88366-113">Examples</span></span>

<span data-ttu-id="88366-114">Nell'esempio seguente viene illustrato un metodo che esamina l'albero dei risultati [**IContextNode**](icontextnode.md) dell'analizzatore di input penna.</span><span class="sxs-lookup"><span data-stu-id="88366-114">The following example shows a method that walks the ink analyzer's [**IContextNode**](icontextnode.md) results tree.</span></span> <span data-ttu-id="88366-115">Se l'analizzatore di input penna non sta attualmente eseguendo l'analisi dell'input penna, il metodo esegue le operazioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="88366-115">If the ink analyzer is not currently performing ink analysis, the method does the following.</span></span>

-   <span data-ttu-id="88366-116">Ottiene la stringa di riconoscimento superiore.</span><span class="sxs-lookup"><span data-stu-id="88366-116">Gets the top recognition string.</span></span>
-   <span data-ttu-id="88366-117">Ottiene il nodo radice dell'analizzatore di input penna.</span><span class="sxs-lookup"><span data-stu-id="88366-117">Gets the ink analyzer's root node.</span></span>
-   <span data-ttu-id="88366-118">Chiama un metodo helper, `ExploreContextNode` , per esaminare il nodo radice e i relativi nodi figlio.</span><span class="sxs-lookup"><span data-stu-id="88366-118">Calls a helper method, `ExploreContextNode`, to examine the root node and its child nodes.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="88366-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="88366-119">Requirements</span></span>



| <span data-ttu-id="88366-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="88366-120">Requirement</span></span> | <span data-ttu-id="88366-121">Valore</span><span class="sxs-lookup"><span data-stu-id="88366-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88366-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="88366-122">Minimum supported client</span></span><br/> | <span data-ttu-id="88366-123">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="88366-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="88366-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="88366-124">Minimum supported server</span></span><br/> | <span data-ttu-id="88366-125">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="88366-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="88366-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="88366-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="88366-127"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="88366-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="88366-128">DLL</span><span class="sxs-lookup"><span data-stu-id="88366-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="88366-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="88366-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="88366-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="88366-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88366-131">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="88366-131">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="88366-132">**Metodo IInkAnalyzer:: Analyze**</span><span class="sxs-lookup"><span data-stu-id="88366-132">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="88366-133">**Metodo IInkAnalyzer:: BackgroundAnalyze**</span><span class="sxs-lookup"><span data-stu-id="88366-133">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="88366-134">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="88366-134">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




