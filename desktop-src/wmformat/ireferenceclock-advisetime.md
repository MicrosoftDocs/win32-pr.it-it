---
title: Metodo IReferenceClock AdviseTime
description: Il metodo AdviseTime richiede una notifica asincrona che è trascorso un periodo di tempo.
ms.assetid: 8f3f8713-b53c-4110-ac7a-724bbc49368e
keywords:
- Metodo AdviseTime Windows Media Format
- Metodo AdviseTime Windows Media Format, interfaccia IReferenceClock
- Interfaccia IReferenceClock-formato Windows Media, metodo AdviseTime
topic_type:
- apiref
api_name:
- IReferenceClock.AdviseTime
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3fa91338b4bff8f925f00e7159a36089e0de0aa8
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299129"
---
# <a name="ireferenceclockadvisetime-method"></a><span data-ttu-id="36eb2-106">Metodo IReferenceClock:: AdviseTime</span><span class="sxs-lookup"><span data-stu-id="36eb2-106">IReferenceClock::AdviseTime method</span></span>

<span data-ttu-id="36eb2-107">Il metodo **AdviseTime** richiede una notifica asincrona che è trascorso un periodo di tempo.</span><span class="sxs-lookup"><span data-stu-id="36eb2-107">The **AdviseTime** method requests an asynchronous notification that a time has elapsed.</span></span>

## <a name="syntax"></a><span data-ttu-id="36eb2-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="36eb2-108">Syntax</span></span>


```C++
HRESULT AdviseTime(
  [in]  REFERENCE_TIME rtBaseTime,
  [in]  REFERENCE_TIME rtStreamTime,
  [in]  HEVENT         hEvent,
  [out] DWORD          *pdwAdviseCookie
);
```



## <a name="parameters"></a><span data-ttu-id="36eb2-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="36eb2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36eb2-110">*rtBaseTime* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="36eb2-110">*rtBaseTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36eb2-111">Tempo di riferimento di base, in unità 100-nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="36eb2-111">Base reference time, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="36eb2-112">*rtStreamTime* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="36eb2-112">*rtStreamTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36eb2-113">Tempo di offset del flusso, in unità di 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="36eb2-113">Stream offset time, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="36eb2-114">*hEvent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="36eb2-114">*hEvent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36eb2-115">Handle per un evento, creato dal chiamante.</span><span class="sxs-lookup"><span data-stu-id="36eb2-115">Handle to an event, created by the caller.</span></span> <span data-ttu-id="36eb2-116">Questo evento verrà segnalato al termine dell'intervallo di tempo specificato.</span><span class="sxs-lookup"><span data-stu-id="36eb2-116">This event will be signaled when the time specified elapses.</span></span>

</dd> <dt>

<span data-ttu-id="36eb2-117">*pdwAdviseCookie* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="36eb2-117">*pdwAdviseCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="36eb2-118">Puntatore a una variabile che riceve un identificatore per la richiesta.</span><span class="sxs-lookup"><span data-stu-id="36eb2-118">Pointer to a variable that receives an identifier for the request.</span></span> <span data-ttu-id="36eb2-119">Viene usato per identificare la chiamata a **AdviseTime** in futuro, ad esempio, per annullare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="36eb2-119">This is used to identify this call to **AdviseTime** in the future for example, to cancel the request.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36eb2-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="36eb2-120">Return value</span></span>

<span data-ttu-id="36eb2-121">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="36eb2-121">The method returns an **HRESULT**.</span></span> <span data-ttu-id="36eb2-122">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="36eb2-122">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="36eb2-123">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="36eb2-123">Return code</span></span>                                                                               | <span data-ttu-id="36eb2-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="36eb2-124">Description</span></span>                                             |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <dl> <span data-ttu-id="36eb2-125"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="36eb2-125"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="36eb2-126">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="36eb2-126">The method succeeded.</span></span><br/>                        |
| <dl> <span data-ttu-id="36eb2-127"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="36eb2-127"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="36eb2-128">Il parametro *pdwAdviseCookie* è **null**.</span><span class="sxs-lookup"><span data-stu-id="36eb2-128">The *pdwAdviseCookie* parameter is **NULL**.</span></span><br/> |
| <dl> <span data-ttu-id="36eb2-129"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="36eb2-129"><dt>**E\_FAIL**</dt></span></span> </dl>    | <span data-ttu-id="36eb2-130">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="36eb2-130">Unspecified failure.</span></span><br/>                         |



 

## <a name="see-also"></a><span data-ttu-id="36eb2-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="36eb2-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36eb2-132">**Interfaccia IReferenceClock**</span><span class="sxs-lookup"><span data-stu-id="36eb2-132">**IReferenceClock Interface**</span></span>](ireferenceclock.md)
</dt> </dl>

 

 





