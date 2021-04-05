---
description: Recupera l'oggetto IAnalysisWarning in corrispondenza dell'indice specificato.
ms.assetid: 8f5d5642-73ec-496e-bad7-9f636fc00217
title: 'Metodo IAnalysisWarnings:: GetAnalysisWarning (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisWarnings.GetAnalysisWarning
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 88ed3686ecf3861a2b097ebfc005214ab0cdd1c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049525"
---
# <a name="ianalysiswarningsgetanalysiswarning-method"></a><span data-ttu-id="3927e-103">Metodo IAnalysisWarnings:: GetAnalysisWarning</span><span class="sxs-lookup"><span data-stu-id="3927e-103">IAnalysisWarnings::GetAnalysisWarning method</span></span>

<span data-ttu-id="3927e-104">Recupera l'oggetto [**IAnalysisWarning**](ianalysiswarning.md) in corrispondenza dell'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="3927e-104">Retrieves the [**IAnalysisWarning**](ianalysiswarning.md) object at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="3927e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3927e-105">Syntax</span></span>


```C++
HRESULT GetAnalysisWarning(
  [in]  ULONG            ulIndex,
  [out] IAnalysisWarning **ppWarning
);
```



## <a name="parameters"></a><span data-ttu-id="3927e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3927e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3927e-107">*ulIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3927e-107">*ulIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3927e-108">Indice in base zero dell'oggetto [**IAnalysisWarning**](ianalysiswarning.md) da ottenere.</span><span class="sxs-lookup"><span data-stu-id="3927e-108">The zero-based index of the [**IAnalysisWarning**](ianalysiswarning.md) object to get.</span></span>

</dd> <dt>

<span data-ttu-id="3927e-109">*ppWarning* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3927e-109">*ppWarning* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3927e-110">Puntatore all'oggetto [**IAnalysisWarning**](ianalysiswarning.md) in corrispondenza dell'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="3927e-110">A pointer to the [**IAnalysisWarning**](ianalysiswarning.md) object at the specified index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3927e-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3927e-111">Return value</span></span>

<span data-ttu-id="3927e-112">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="3927e-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3927e-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="3927e-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="3927e-114">Per evitare una perdita di memoria, chiamare [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su \* *ppWarning* quando non è più necessario usare l'avviso.</span><span class="sxs-lookup"><span data-stu-id="3927e-114">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppWarning* when you no longer need to use the warning.</span></span>

 

## <a name="examples"></a><span data-ttu-id="3927e-115">Esempio</span><span class="sxs-lookup"><span data-stu-id="3927e-115">Examples</span></span>

<span data-ttu-id="3927e-116">Nell'esempio seguente viene illustrata una struttura di un gestore eventi per l'evento [**\_ IAnalysisEvents:: results**](-ianalysisevents-results.md) .</span><span class="sxs-lookup"><span data-stu-id="3927e-116">The following example shows an outline of an event handler for the [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) event.</span></span> <span data-ttu-id="3927e-117">Il gestore verifica [**IAnalysisStatus:: con esito positivo**](ianalysisstatus-issuccessful.md).</span><span class="sxs-lookup"><span data-stu-id="3927e-117">The handler checks [**IAnalysisStatus::IsSuccessful**](ianalysisstatus-issuccessful.md).</span></span> <span data-ttu-id="3927e-118">Se l'operazione di analisi genera avvisi, il gestore scorre la raccolta di oggetti [**IAnalysisWarning**](ianalysiswarning.md) .</span><span class="sxs-lookup"><span data-stu-id="3927e-118">If the analysis operation generates warnings, the handler iterates through the collection of [**IAnalysisWarning**](ianalysiswarning.md) objects.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="3927e-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3927e-119">Requirements</span></span>



| <span data-ttu-id="3927e-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="3927e-120">Requirement</span></span> | <span data-ttu-id="3927e-121">Valore</span><span class="sxs-lookup"><span data-stu-id="3927e-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3927e-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3927e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3927e-123">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="3927e-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="3927e-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3927e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3927e-125">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="3927e-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="3927e-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3927e-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="3927e-127"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="3927e-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="3927e-128">DLL</span><span class="sxs-lookup"><span data-stu-id="3927e-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3927e-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3927e-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="3927e-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3927e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3927e-131">**IAnalysisWarnings**</span><span class="sxs-lookup"><span data-stu-id="3927e-131">**IAnalysisWarnings**</span></span>](ianalysiswarnings.md)
</dt> <dt>

[<span data-ttu-id="3927e-132">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="3927e-132">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

