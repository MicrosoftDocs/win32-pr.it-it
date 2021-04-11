---
description: Rappresenta un avviso o un errore che si verifica durante un'operazione di analisi dell'input penna.
ms.assetid: a9b0564b-8a49-44bc-9dbc-60a2fd5b60f2
title: Interfaccia IAnalysisWarning (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisWarning
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 79e865ac909d6f9ee1862926ffab06f538661d6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129515"
---
# <a name="ianalysiswarning-interface"></a><span data-ttu-id="9b07e-103">Interfaccia IAnalysisWarning</span><span class="sxs-lookup"><span data-stu-id="9b07e-103">IAnalysisWarning interface</span></span>

<span data-ttu-id="9b07e-104">Rappresenta un avviso o un errore che si verifica durante un'operazione di analisi dell'input penna.</span><span class="sxs-lookup"><span data-stu-id="9b07e-104">Represents a warning or error that occurs during an ink analysis operation.</span></span>

## <a name="members"></a><span data-ttu-id="9b07e-105">Membri</span><span class="sxs-lookup"><span data-stu-id="9b07e-105">Members</span></span>

<span data-ttu-id="9b07e-106">L'interfaccia **IAnalysisWarning** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="9b07e-106">The **IAnalysisWarning** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="9b07e-107">**IAnalysisWarning** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="9b07e-107">**IAnalysisWarning** also has these types of members:</span></span>

-   [<span data-ttu-id="9b07e-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="9b07e-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="9b07e-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="9b07e-109">Methods</span></span>

<span data-ttu-id="9b07e-110">L'interfaccia **IAnalysisWarning** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="9b07e-110">The **IAnalysisWarning** interface has these methods.</span></span>



| <span data-ttu-id="9b07e-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="9b07e-111">Method</span></span>                                                            | <span data-ttu-id="9b07e-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9b07e-112">Description</span></span>                                                                                                                            |
|:------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9b07e-113">**GetBackgroundError**</span><span class="sxs-lookup"><span data-stu-id="9b07e-113">**GetBackgroundError**</span></span>](ianalysiswarning-getbackgrounderror.md) | <span data-ttu-id="9b07e-114">Recupera il codice di errore per l'operazione di analisi dell'input penna in background se si è verificato un errore.</span><span class="sxs-lookup"><span data-stu-id="9b07e-114">Retrieves the error code for the background ink analysis operation if an error occurred.</span></span><br/>                                    |
| [<span data-ttu-id="9b07e-115">**GetHint**</span><span class="sxs-lookup"><span data-stu-id="9b07e-115">**GetHint**</span></span>](ianalysiswarning-gethint.md)                       | <span data-ttu-id="9b07e-116">Recupera l'hint di analisi che ha generato l'avviso</span><span class="sxs-lookup"><span data-stu-id="9b07e-116">Retrieves the analysis hint that caused this warning</span></span><br/>                                                                        |
| [<span data-ttu-id="9b07e-117">**GetNodeIds**</span><span class="sxs-lookup"><span data-stu-id="9b07e-117">**GetNodeIds**</span></span>](ianalysiswarning-getnodeids.md)                 | <span data-ttu-id="9b07e-118">Recupera gli identificatori di qualsiasi nodo di contesto pertinente associato a questo avviso.</span><span class="sxs-lookup"><span data-stu-id="9b07e-118">Retrieves the identifiers of any relevant context nodes that are associated with this warning.</span></span><br/>                              |
| [<span data-ttu-id="9b07e-119">**GetWarningCode**</span><span class="sxs-lookup"><span data-stu-id="9b07e-119">**GetWarningCode**</span></span>](ianalysiswarning-getwarningcode.md)         | <span data-ttu-id="9b07e-120">Recupera il tipo di avviso che si è verificato utilizzando l'enumerazione [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) .</span><span class="sxs-lookup"><span data-stu-id="9b07e-120">Retrieves the type of warning that occurred by using the [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) enumeration.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9b07e-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="9b07e-121">Remarks</span></span>

<span data-ttu-id="9b07e-122">I tipi di avvisi che possono verificarsi sono descritti dall'enumerazione [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) .</span><span class="sxs-lookup"><span data-stu-id="9b07e-122">The types of warnings that can occur are described by the [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) enumeration.</span></span> <span data-ttu-id="9b07e-123">Spesso gli avvisi si verificano quando si tenta di usare una funzionalità non supportata dal [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) usato da [**IInkAnalyzer**](iinkanalyzer.md) .</span><span class="sxs-lookup"><span data-stu-id="9b07e-123">Often warnings occur when you try to use a feature that is not supported by the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) that the [**IInkAnalyzer**](iinkanalyzer.md) is using.</span></span>

<span data-ttu-id="9b07e-124">Alcuni avvisi indicano che il [**IInkAnalyzer**](iinkanalyzer.md) non ha completato l'operazione di analisi.</span><span class="sxs-lookup"><span data-stu-id="9b07e-124">Some warnings indicate that the [**IInkAnalyzer**](iinkanalyzer.md) did not complete the analysis operation.</span></span> <span data-ttu-id="9b07e-125">Per ulteriori informazioni, vedere [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode).</span><span class="sxs-lookup"><span data-stu-id="9b07e-125">For more information, see [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode).</span></span>

## <a name="examples"></a><span data-ttu-id="9b07e-126">Esempio</span><span class="sxs-lookup"><span data-stu-id="9b07e-126">Examples</span></span>

<span data-ttu-id="9b07e-127">Nell'esempio seguente viene illustrata una struttura di un gestore eventi per l'evento [**\_ IAnalysisEvents:: results**](-ianalysisevents-results.md) .</span><span class="sxs-lookup"><span data-stu-id="9b07e-127">The following example shows an outline of an event handler for the [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) event.</span></span> <span data-ttu-id="9b07e-128">Il gestore verifica [**IAnalysisStatus:: con esito positivo**](ianalysisstatus-issuccessful.md).</span><span class="sxs-lookup"><span data-stu-id="9b07e-128">The handler checks [**IAnalysisStatus::IsSuccessful**](ianalysisstatus-issuccessful.md).</span></span> <span data-ttu-id="9b07e-129">Se l'operazione di analisi genera avvisi, il gestore scorre la raccolta di oggetti **IAnalysisWarning** .</span><span class="sxs-lookup"><span data-stu-id="9b07e-129">If the analysis operation generates warnings, the handler iterates through the collection of **IAnalysisWarning** objects.</span></span>


```C++
// _IAnalysisEvents::Results event handler.
STDMETHODIMP CMyClass::Results(
    IInkAnalyzer *pInkAnalyzer,
    IAnalysisStatus *pAnalysisStatus)
{
    // Check the status of the analysis operation.
    VARIANT_BOOL bResult = VARIANT_FALSE;
    HRESULT hr = pAnalysisStatus->IsSuccessful(&bResult);

    if( SUCCEEDED(hr) )
    {
        if( bResult )
        {
            // Insert code that handles a successful result.
        }
        else
        {
            // Get the analysis warnings.
            IAnalysisWarnings* pAnalysisWarnings = NULL;
            hr = pAnalysisStatus->GetWarnings(&pAnalysisWarnings);
            if (SUCCEEDED(hr))
            {
                // Iterate through the warning collection.
                ULONG warningCount = 0;
                hr = pAnalysisWarnings->GetCount(&warningCount);
                if (SUCCEEDED(hr))
                {
                    IAnalysisWarning *pAnalysisWarning = NULL;
                    AnalysisWarningCode analysisWarningCode;
                    for (ULONG index=0; index<warningCount; index++)
                    {
                        // Get an analysis warning.
                        hr = pAnalysisWarnings->GetAnalysisWarning(
                            index, &pAnalysisWarning);

                        if (SUCCEEDED(hr))
                        {
                            // Get the warning code for the warning.
                            hr = pAnalysisWarning->GetWarningCode(
                                &analysisWarningCode);

                            if (SUCCEEDED(hr))
                            {
                                // Insert code that handles each
                                // analysis warning.
                            }
                        }

                        // Release this reference to the analysis warning.
                        if (pAnalysisWarning != NULL)
                        {
                            pAnalysisWarning->Release();
                            pAnalysisWarning = NULL;
                        }

                        if (FAILED(hr))
                        {
                            break;
                        }
                    }
                }
            }

            // Release this reference to the analysis warnings collection.
            if (pAnalysisWarnings != NULL)
            {
                pAnalysisWarnings->Release();
                pAnalysisWarnings = NULL;
            }
        }
    }
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="9b07e-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9b07e-130">Requirements</span></span>



| <span data-ttu-id="9b07e-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b07e-131">Requirement</span></span> | <span data-ttu-id="9b07e-132">Valore</span><span class="sxs-lookup"><span data-stu-id="9b07e-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b07e-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9b07e-133">Minimum supported client</span></span><br/> | <span data-ttu-id="9b07e-134">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="9b07e-134">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="9b07e-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9b07e-135">Minimum supported server</span></span><br/> | <span data-ttu-id="9b07e-136">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="9b07e-136">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="9b07e-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9b07e-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b07e-138"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="9b07e-138"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="9b07e-139">DLL</span><span class="sxs-lookup"><span data-stu-id="9b07e-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9b07e-140"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9b07e-140"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="9b07e-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9b07e-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b07e-142">**IAnalysisWarnings**</span><span class="sxs-lookup"><span data-stu-id="9b07e-142">**IAnalysisWarnings**</span></span>](ianalysiswarnings.md)
</dt> <dt>

[<span data-ttu-id="9b07e-143">**AnalysisWarningCode**</span><span class="sxs-lookup"><span data-stu-id="9b07e-143">**AnalysisWarningCode**</span></span>](analysiswarningcode.md)
</dt> <dt>

[<span data-ttu-id="9b07e-144">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="9b07e-144">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

