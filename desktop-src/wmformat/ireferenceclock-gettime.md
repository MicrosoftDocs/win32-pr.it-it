---
title: Metodo getTime IReferenceClock
description: Il metodo getTime recupera l'ora di riferimento corrente.
ms.assetid: 9bf5050a-ae09-4a72-a3f2-3df8339d99b9
keywords:
- Metodo getTime per Windows Media Format
- Metodo getTime, formato Windows Media, interfaccia IReferenceClock
- Interfaccia IReferenceClock-formato Windows Media, metodo getTime
topic_type:
- apiref
api_name:
- IReferenceClock.GetTime
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c679ce0adbbc6cc7ddc014c12f1b0ace4be6b4b0
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104398046"
---
# <a name="ireferenceclockgettime-method"></a><span data-ttu-id="f4a62-106">Metodo IReferenceClock:: getTime</span><span class="sxs-lookup"><span data-stu-id="f4a62-106">IReferenceClock::GetTime method</span></span>

<span data-ttu-id="f4a62-107">Il metodo **getTime** recupera l'ora di riferimento corrente.</span><span class="sxs-lookup"><span data-stu-id="f4a62-107">The **GetTime** method retrieves the current reference time.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4a62-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f4a62-108">Syntax</span></span>


```C++
HRESULT GetTime(
  [out] REFERENCE_TIME *pTime
);
```



## <a name="parameters"></a><span data-ttu-id="f4a62-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="f4a62-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4a62-110">*pTime* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f4a62-110">*pTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f4a62-111">Puntatore a una variabile che riceve l'ora corrente, in unità di 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="f4a62-111">Pointer to a variable that receives the current time, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4a62-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f4a62-112">Return value</span></span>

<span data-ttu-id="f4a62-113">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="f4a62-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="f4a62-114">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="f4a62-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="f4a62-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="f4a62-115">Return code</span></span>                                                                               | <span data-ttu-id="f4a62-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f4a62-116">Description</span></span>                                   |
|-------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="f4a62-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f4a62-117"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="f4a62-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="f4a62-118">The method succeeded.</span></span><br/>              |
| <dl> <span data-ttu-id="f4a62-119"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="f4a62-119"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="f4a62-120">Il parametro *pTime* è **null**.</span><span class="sxs-lookup"><span data-stu-id="f4a62-120">The *pTime* parameter is **NULL**.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="f4a62-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f4a62-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4a62-122">**Interfaccia IReferenceClock**</span><span class="sxs-lookup"><span data-stu-id="f4a62-122">**IReferenceClock Interface**</span></span>](ireferenceclock.md)
</dt> </dl>

 

 





