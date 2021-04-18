---
description: Ottiene il numero di oggetti IAnalysisWarning contenuti nella raccolta IAnalysisWarnings.
ms.assetid: a0ad46d5-fb1b-40f6-bfc1-28ea1bf4eb44
title: 'Metodo IAnalysisWarnings:: GetCount (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisWarnings.GetCount
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: bc795d310f4bc532a39e2c1a2b4d2ba68f0401f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307451"
---
# <a name="ianalysiswarningsgetcount-method"></a><span data-ttu-id="d1e38-103">Metodo IAnalysisWarnings:: GetCount</span><span class="sxs-lookup"><span data-stu-id="d1e38-103">IAnalysisWarnings::GetCount method</span></span>

<span data-ttu-id="d1e38-104">Ottiene il numero di oggetti [**IAnalysisWarning**](ianalysiswarning.md) contenuti nella raccolta [**IAnalysisWarnings**](ianalysiswarnings.md) .</span><span class="sxs-lookup"><span data-stu-id="d1e38-104">Gets the number of [**IAnalysisWarning**](ianalysiswarning.md) objects contained in the [**IAnalysisWarnings**](ianalysiswarnings.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1e38-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d1e38-105">Syntax</span></span>


```C++
HRESULT GetCount(
  [out, retval] ULONG *pulCount
);
```



## <a name="parameters"></a><span data-ttu-id="d1e38-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d1e38-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1e38-107">*pulCount* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="d1e38-107">*pulCount* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="d1e38-108">Numero di oggetti [**IAnalysisWarning**](ianalysiswarning.md) contenuti nella raccolta [**IAnalysisWarnings**](ianalysiswarnings.md) .</span><span class="sxs-lookup"><span data-stu-id="d1e38-108">The number of [**IAnalysisWarning**](ianalysiswarning.md) objects contained in the [**IAnalysisWarnings**](ianalysiswarnings.md) collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1e38-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d1e38-109">Return value</span></span>

<span data-ttu-id="d1e38-110">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="d1e38-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="examples"></a><span data-ttu-id="d1e38-111">Esempio</span><span class="sxs-lookup"><span data-stu-id="d1e38-111">Examples</span></span>

<span data-ttu-id="d1e38-112">Nell'esempio seguente viene illustrata una struttura di un gestore eventi per l'evento [**\_ IAnalysisEvents:: results**](-ianalysisevents-results.md) .</span><span class="sxs-lookup"><span data-stu-id="d1e38-112">The following example shows an outline of an event handler for the [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) event.</span></span> <span data-ttu-id="d1e38-113">Il gestore verifica [**IAnalysisStatus:: con esito positivo**](ianalysisstatus-issuccessful.md).</span><span class="sxs-lookup"><span data-stu-id="d1e38-113">The handler checks [**IAnalysisStatus::IsSuccessful**](ianalysisstatus-issuccessful.md).</span></span> <span data-ttu-id="d1e38-114">Se l'operazione di analisi genera avvisi, il gestore scorre la raccolta di oggetti [**IAnalysisWarning**](ianalysiswarning.md) .</span><span class="sxs-lookup"><span data-stu-id="d1e38-114">If the analysis operation generates warnings, the handler iterates through the collection of [**IAnalysisWarning**](ianalysiswarning.md) objects.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="d1e38-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d1e38-115">Requirements</span></span>



| <span data-ttu-id="d1e38-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1e38-116">Requirement</span></span> | <span data-ttu-id="d1e38-117">Valore</span><span class="sxs-lookup"><span data-stu-id="d1e38-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1e38-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d1e38-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d1e38-119">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="d1e38-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d1e38-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d1e38-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d1e38-121">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="d1e38-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="d1e38-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d1e38-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1e38-123"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="d1e38-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="d1e38-124">DLL</span><span class="sxs-lookup"><span data-stu-id="d1e38-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1e38-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1e38-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="d1e38-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d1e38-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1e38-127">**IAnalysisWarnings**</span><span class="sxs-lookup"><span data-stu-id="d1e38-127">**IAnalysisWarnings**</span></span>](ianalysiswarnings.md)
</dt> <dt>

[<span data-ttu-id="d1e38-128">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="d1e38-128">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




