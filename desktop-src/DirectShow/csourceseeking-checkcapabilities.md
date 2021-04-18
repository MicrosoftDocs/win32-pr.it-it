---
description: 'Il metodo CheckCapabilities esegue una query se il flusso ha specificato funzionalità di ricerca. Questo metodo implementa il metodo IMediaSeeking:: CheckCapabilities.'
ms.assetid: 5d37e179-9e04-44e1-acbc-dfd2682830c0
title: Metodo CSourceSeeking. CheckCapabilities (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.CheckCapabilities
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2f537973ac6c8f084ea42ba915a6293e581debef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325738"
---
# <a name="csourceseekingcheckcapabilities-method"></a><span data-ttu-id="beb4a-104">CSourceSeeking. CheckCapabilities, metodo</span><span class="sxs-lookup"><span data-stu-id="beb4a-104">CSourceSeeking.CheckCapabilities method</span></span>

<span data-ttu-id="beb4a-105">Il `CheckCapabilities` metodo esegue una query se il flusso ha specificato funzionalità di ricerca.</span><span class="sxs-lookup"><span data-stu-id="beb4a-105">The `CheckCapabilities` method queries whether the stream has specified seeking capabilities.</span></span> <span data-ttu-id="beb4a-106">Questo metodo implementa il metodo [**IMediaSeeking:: CheckCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) .</span><span class="sxs-lookup"><span data-stu-id="beb4a-106">This method implements the [**IMediaSeeking::CheckCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="beb4a-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="beb4a-107">Syntax</span></span>


```C++
HRESULT CheckCapabilities(
   DWORD *pCapabilities
);
```



## <a name="parameters"></a><span data-ttu-id="beb4a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="beb4a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="beb4a-109">*pCapabilities*</span><span class="sxs-lookup"><span data-stu-id="beb4a-109">*pCapabilities*</span></span> 
</dt> <dd>

<span data-ttu-id="beb4a-110">Puntatore a una combinazione bit per bit di uno o più attributi per la [**\_ ricerca di \_ \_ funzionalità**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) .</span><span class="sxs-lookup"><span data-stu-id="beb4a-110">Pointer to a bitwise combination of one or more [**AM\_SEEKING\_SEEKING\_CAPABILITIES**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) attributes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="beb4a-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="beb4a-111">Return value</span></span>

<span data-ttu-id="beb4a-112">Restituisce uno dei valori **HRESULT** elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="beb4a-112">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="beb4a-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="beb4a-113">Return code</span></span>                                                                               | <span data-ttu-id="beb4a-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="beb4a-114">Description</span></span>                                                            |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="beb4a-115"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="beb4a-115"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="beb4a-116">Non tutte le funzionalità di *pCapabilities* sono presenti.</span><span class="sxs-lookup"><span data-stu-id="beb4a-116">Not all of the capabilities in *pCapabilities* are present.</span></span><br/> |
| <dl> <span data-ttu-id="beb4a-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="beb4a-117"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="beb4a-118">Sono presenti tutte le funzionalità di *pCapabilities* .</span><span class="sxs-lookup"><span data-stu-id="beb4a-118">All capabilities in *pCapabilities* are present.</span></span><br/>            |
| <dl> <span data-ttu-id="beb4a-119"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="beb4a-119"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="beb4a-120">Argomento puntatore **null** .</span><span class="sxs-lookup"><span data-stu-id="beb4a-120">**NULL** pointer argument.</span></span><br/>                                  |



 

## <a name="remarks"></a><span data-ttu-id="beb4a-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="beb4a-121">Remarks</span></span>

<span data-ttu-id="beb4a-122">Come implementato, questo metodo controlla il valore di *\* pCapabilities* sulla variabile membro [**CSourceSeeking:: m \_ dwSeekingCaps**](csourceseeking-m-dwseekingcaps.md) .</span><span class="sxs-lookup"><span data-stu-id="beb4a-122">As implemented, this method checks the value of *\*pCapabilities* against the [**CSourceSeeking::m\_dwSeekingCaps**](csourceseeking-m-dwseekingcaps.md) member variable.</span></span> <span data-ttu-id="beb4a-123">Tuttavia, non imposta *\* pCapabilities* uguale a **m \_ dwSeekingCaps**, come descritto per il metodo [**IMediaSeeking:: CheckCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) .</span><span class="sxs-lookup"><span data-stu-id="beb4a-123">However, it does not set *\*pCapabilities* equal to **m\_dwSeekingCaps**, as described for the [**IMediaSeeking::CheckCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) method.</span></span> <span data-ttu-id="beb4a-124">Inoltre, nel caso in cui non sia disponibile alcuna funzionalità specificata, il metodo non restituisce E ha \_ esito negativo.</span><span class="sxs-lookup"><span data-stu-id="beb4a-124">Also, in the case where none of the specified capabilities are available, the method does not return E\_FAIL.</span></span> <span data-ttu-id="beb4a-125">Un'implementazione più completa è la seguente:</span><span class="sxs-lookup"><span data-stu-id="beb4a-125">A more complete implementation would be as follows:</span></span>


```C++
STDMETHODIMP CheckCapabilities(DWORD *pCapabilities)
{
    CheckPointer(pCapabilities, E_POINTER)
;
    DWORD dwCaps;
    HRESULT hr = GetCapabilities(&dwCaps);
    if (SUCCEEDED(hr))
    {
        dwCaps &= *pCapabilities;
        if (dwCaps)
        {
            hr =  (dwCaps == *pCapabilities ? S_OK : S_FALSE );
        }
        else 
        {
            hr = E_FAIL;
        }
        *pCapabilities = dwCaps;
    }
    else 
    {
        *pCapabilities = 0;
    }
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="beb4a-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="beb4a-126">Requirements</span></span>



| <span data-ttu-id="beb4a-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="beb4a-127">Requirement</span></span> | <span data-ttu-id="beb4a-128">Valore</span><span class="sxs-lookup"><span data-stu-id="beb4a-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="beb4a-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="beb4a-129">Header</span></span><br/>  | <dl> <span data-ttu-id="beb4a-130"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="beb4a-130"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="beb4a-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="beb4a-131">Library</span></span><br/> | <dl> <span data-ttu-id="beb4a-132"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="beb4a-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="beb4a-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="beb4a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="beb4a-134">**Classe CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="beb4a-134">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




