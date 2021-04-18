---
description: Contiene una raccolta di oggetti che implementano l'interfaccia IAnalysisWarning e che sono il risultato di un'operazione di analisi dell'input penna.
ms.assetid: 2118c18b-d316-4e91-8652-62969115e8b5
title: Interfaccia IAnalysisWarnings (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisWarnings
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 938d406ea90d86cc05ac84b69304b7a85e0e54fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307449"
---
# <a name="ianalysiswarnings-interface"></a><span data-ttu-id="ccfbe-103">Interfaccia IAnalysisWarnings</span><span class="sxs-lookup"><span data-stu-id="ccfbe-103">IAnalysisWarnings interface</span></span>

<span data-ttu-id="ccfbe-104">Contiene una raccolta di oggetti che implementano l'interfaccia [**IAnalysisWarning**](ianalysiswarning.md) e che sono il risultato di un'operazione di analisi dell'input penna.</span><span class="sxs-lookup"><span data-stu-id="ccfbe-104">Contains a collection of objects that implement the [**IAnalysisWarning**](ianalysiswarning.md) interface and that are the result of an ink analysis operation.</span></span>

## <a name="members"></a><span data-ttu-id="ccfbe-105">Membri</span><span class="sxs-lookup"><span data-stu-id="ccfbe-105">Members</span></span>

<span data-ttu-id="ccfbe-106">L'interfaccia **IAnalysisWarnings** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="ccfbe-106">The **IAnalysisWarnings** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="ccfbe-107">**IAnalysisWarnings** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="ccfbe-107">**IAnalysisWarnings** also has these types of members:</span></span>

-   [<span data-ttu-id="ccfbe-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="ccfbe-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ccfbe-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="ccfbe-109">Methods</span></span>

<span data-ttu-id="ccfbe-110">L'interfaccia **IAnalysisWarnings** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="ccfbe-110">The **IAnalysisWarnings** interface has these methods.</span></span>



| <span data-ttu-id="ccfbe-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="ccfbe-111">Method</span></span>                                                             | <span data-ttu-id="ccfbe-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ccfbe-112">Description</span></span>                                                                                                                                |
|:-------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ccfbe-113">**GetAnalysisWarning**</span><span class="sxs-lookup"><span data-stu-id="ccfbe-113">**GetAnalysisWarning**</span></span>](ianalysiswarnings-getanalysiswarning.md) | <span data-ttu-id="ccfbe-114">Recupera l'oggetto [**IAnalysisWarning**](ianalysiswarning.md) in corrispondenza dell'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="ccfbe-114">Retrieves the [**IAnalysisWarning**](ianalysiswarning.md) object at the specified index.</span></span><br/>                                       |
| [<span data-ttu-id="ccfbe-115">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="ccfbe-115">**GetCount**</span></span>](ianalysiswarnings-getcount.md)                     | <span data-ttu-id="ccfbe-116">Recupera il numero di oggetti [**IAnalysisWarning**](ianalysiswarning.md) contenuti nella raccolta **IAnalysisWarnings** .</span><span class="sxs-lookup"><span data-stu-id="ccfbe-116">Retrieves the number of [**IAnalysisWarning**](ianalysiswarning.md) objects contained in the **IAnalysisWarnings** collection.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="ccfbe-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="ccfbe-117">Examples</span></span>

<span data-ttu-id="ccfbe-118">Nell'esempio seguente viene illustrata una struttura di un gestore eventi per l'evento [**\_ IAnalysisEvents:: results**](-ianalysisevents-results.md) .</span><span class="sxs-lookup"><span data-stu-id="ccfbe-118">The following example shows an outline of an event handler for the [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) event.</span></span> <span data-ttu-id="ccfbe-119">Il gestore verifica [**IAnalysisStatus:: con esito positivo**](ianalysisstatus-issuccessful.md).</span><span class="sxs-lookup"><span data-stu-id="ccfbe-119">The handler checks [**IAnalysisStatus::IsSuccessful**](ianalysisstatus-issuccessful.md).</span></span> <span data-ttu-id="ccfbe-120">Se l'operazione di analisi ha generato avvisi, il gestore scorre la raccolta di oggetti [**IAnalysisWarning**](ianalysiswarning.md) .</span><span class="sxs-lookup"><span data-stu-id="ccfbe-120">If the analysis operation generated warnings, the handler iterates through the collection of [**IAnalysisWarning**](ianalysiswarning.md) objects.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="ccfbe-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ccfbe-121">Requirements</span></span>



| <span data-ttu-id="ccfbe-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="ccfbe-122">Requirement</span></span> | <span data-ttu-id="ccfbe-123">Valore</span><span class="sxs-lookup"><span data-stu-id="ccfbe-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ccfbe-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ccfbe-124">Minimum supported client</span></span><br/> | <span data-ttu-id="ccfbe-125">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="ccfbe-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ccfbe-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ccfbe-126">Minimum supported server</span></span><br/> | <span data-ttu-id="ccfbe-127">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="ccfbe-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="ccfbe-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ccfbe-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="ccfbe-129"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="ccfbe-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="ccfbe-130">DLL</span><span class="sxs-lookup"><span data-stu-id="ccfbe-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ccfbe-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ccfbe-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="ccfbe-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ccfbe-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccfbe-133">**IAnalysisStatus**</span><span class="sxs-lookup"><span data-stu-id="ccfbe-133">**IAnalysisStatus**</span></span>](ianalysisstatus.md)
</dt> <dt>

[<span data-ttu-id="ccfbe-134">**IAnalysisWarning**</span><span class="sxs-lookup"><span data-stu-id="ccfbe-134">**IAnalysisWarning**</span></span>](ianalysiswarning.md)
</dt> <dt>

[<span data-ttu-id="ccfbe-135">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="ccfbe-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

