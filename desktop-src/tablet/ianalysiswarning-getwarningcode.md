---
description: Restituisce il tipo di avviso che si è verificato utilizzando l'enumerazione AnalysisWarningCode.
ms.assetid: ec67a5ac-a7a2-4805-b9b5-915ea956d228
title: 'Metodo IAnalysisWarning:: GetWarningCode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisWarning.GetWarningCode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 8e129b410de9e8ca9e3944b6a371fe0cac673fc5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307453"
---
# <a name="ianalysiswarninggetwarningcode-method"></a><span data-ttu-id="704b2-103">Metodo IAnalysisWarning:: GetWarningCode</span><span class="sxs-lookup"><span data-stu-id="704b2-103">IAnalysisWarning::GetWarningCode method</span></span>

<span data-ttu-id="704b2-104">Restituisce il tipo di avviso che si è verificato utilizzando l'enumerazione [**AnalysisWarningCode**](analysiswarningcode.md) .</span><span class="sxs-lookup"><span data-stu-id="704b2-104">Returns the type of warning that occurred by using the [**AnalysisWarningCode**](analysiswarningcode.md) enumeration.</span></span>

## <a name="syntax"></a><span data-ttu-id="704b2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="704b2-105">Syntax</span></span>


```C++
HRESULT GetWarningCode(
  [out] AnalysisWarningCode *pWarningCode
);
```



## <a name="parameters"></a><span data-ttu-id="704b2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="704b2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="704b2-107">*pWarningCode* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="704b2-107">*pWarningCode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="704b2-108">Tipo di avviso che si è verificato.</span><span class="sxs-lookup"><span data-stu-id="704b2-108">The type of warning that occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="704b2-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="704b2-109">Return value</span></span>

<span data-ttu-id="704b2-110">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="704b2-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="examples"></a><span data-ttu-id="704b2-111">Esempio</span><span class="sxs-lookup"><span data-stu-id="704b2-111">Examples</span></span>

<span data-ttu-id="704b2-112">Nell'esempio seguente viene illustrata una struttura di un gestore eventi per l'evento [**\_ IAnalysisEvents:: results**](-ianalysisevents-results.md) .</span><span class="sxs-lookup"><span data-stu-id="704b2-112">The following example shows an outline of an event handler for the [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) event.</span></span> <span data-ttu-id="704b2-113">Il gestore verifica [**IAnalysisStatus:: con esito positivo**](ianalysisstatus-issuccessful.md).</span><span class="sxs-lookup"><span data-stu-id="704b2-113">The handler checks [**IAnalysisStatus::IsSuccessful**](ianalysisstatus-issuccessful.md).</span></span> <span data-ttu-id="704b2-114">Se l'operazione di analisi ha generato avvisi, il gestore scorre la raccolta di oggetti [**IAnalysisWarning**](ianalysiswarning.md) .</span><span class="sxs-lookup"><span data-stu-id="704b2-114">If the analysis operation generated warnings, the handler iterates through the collection of [**IAnalysisWarning**](ianalysiswarning.md) objects.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="704b2-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="704b2-115">Requirements</span></span>



| <span data-ttu-id="704b2-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="704b2-116">Requirement</span></span> | <span data-ttu-id="704b2-117">Valore</span><span class="sxs-lookup"><span data-stu-id="704b2-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="704b2-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="704b2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="704b2-119">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="704b2-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="704b2-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="704b2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="704b2-121">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="704b2-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="704b2-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="704b2-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="704b2-123"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="704b2-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="704b2-124">DLL</span><span class="sxs-lookup"><span data-stu-id="704b2-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="704b2-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="704b2-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="704b2-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="704b2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="704b2-127">**IAnalysisWarning**</span><span class="sxs-lookup"><span data-stu-id="704b2-127">**IAnalysisWarning**</span></span>](ianalysiswarning.md)
</dt> <dt>

[<span data-ttu-id="704b2-128">**AnalysisWarningCode**</span><span class="sxs-lookup"><span data-stu-id="704b2-128">**AnalysisWarningCode**</span></span>](/windows/desktop/tablet/analysiswarningcode)
</dt> <dt>

[<span data-ttu-id="704b2-129">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="704b2-129">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

