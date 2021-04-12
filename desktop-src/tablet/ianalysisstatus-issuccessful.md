---
description: Recupera un riepilogo booleano dei risultati dell'operazione di analisi.
ms.assetid: 9bc690f4-fb5f-449e-bde0-bd2277c4573b
title: 'Metodo IAnalysisStatus:: isvalidful (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisStatus.IsSuccessful
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: daf7ec801773d855f0ed85a795bc492ef673a74e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343736"
---
# <a name="ianalysisstatusissuccessful-method"></a><span data-ttu-id="859cd-103">Metodo IAnalysisStatus:: con esito positivo</span><span class="sxs-lookup"><span data-stu-id="859cd-103">IAnalysisStatus::IsSuccessful method</span></span>

<span data-ttu-id="859cd-104">Recupera un riepilogo booleano dei risultati dell'operazione di analisi.</span><span class="sxs-lookup"><span data-stu-id="859cd-104">Retrieves a Boolean summary of the results of the analysis operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="859cd-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="859cd-105">Syntax</span></span>


```C++
HRESULT IsSuccessful(
  [out] VARIANT_BOOL *pfSuccessful
);
```



## <a name="parameters"></a><span data-ttu-id="859cd-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="859cd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="859cd-107">*pfSuccessful* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="859cd-107">*pfSuccessful* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="859cd-108">**Variante \_ TRUE** se l'operazione di analisi è stata completata senza avvisi oppure **Variant \_ false** se si è verificato almeno un avviso.</span><span class="sxs-lookup"><span data-stu-id="859cd-108">**VARIANT\_TRUE** if the analysis operation completed without any warnings, or **VARIANT\_FALSE** if at least one warning occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="859cd-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="859cd-109">Return value</span></span>

<span data-ttu-id="859cd-110">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="859cd-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="examples"></a><span data-ttu-id="859cd-111">Esempio</span><span class="sxs-lookup"><span data-stu-id="859cd-111">Examples</span></span>

<span data-ttu-id="859cd-112">Nell'esempio seguente viene illustrata una struttura di un gestore eventi per l'evento [**\_ IAnalysisEvents:: results**](-ianalysisevents-results.md) .</span><span class="sxs-lookup"><span data-stu-id="859cd-112">The following example shows an outline of an event handler for the [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) event.</span></span> <span data-ttu-id="859cd-113">Il gestore verifica **IAnalysisStatus:: con esito positivo**.</span><span class="sxs-lookup"><span data-stu-id="859cd-113">The handler checks **IAnalysisStatus::IsSuccessful**.</span></span> <span data-ttu-id="859cd-114">Se l'operazione di analisi genera avvisi, il gestore scorre la raccolta di oggetti [**IAnalysisWarning**](ianalysiswarning.md) .</span><span class="sxs-lookup"><span data-stu-id="859cd-114">If the analysis operation generates warnings, the handler iterates through the collection of [**IAnalysisWarning**](ianalysiswarning.md) objects.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="859cd-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="859cd-115">Requirements</span></span>



| <span data-ttu-id="859cd-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="859cd-116">Requirement</span></span> | <span data-ttu-id="859cd-117">Valore</span><span class="sxs-lookup"><span data-stu-id="859cd-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="859cd-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="859cd-118">Minimum supported client</span></span><br/> | <span data-ttu-id="859cd-119">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="859cd-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="859cd-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="859cd-120">Minimum supported server</span></span><br/> | <span data-ttu-id="859cd-121">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="859cd-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="859cd-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="859cd-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="859cd-123"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="859cd-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="859cd-124">DLL</span><span class="sxs-lookup"><span data-stu-id="859cd-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="859cd-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="859cd-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="859cd-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="859cd-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="859cd-127">**IAnalysisStatus**</span><span class="sxs-lookup"><span data-stu-id="859cd-127">**IAnalysisStatus**</span></span>](ianalysisstatus.md)
</dt> <dt>

[<span data-ttu-id="859cd-128">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="859cd-128">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




