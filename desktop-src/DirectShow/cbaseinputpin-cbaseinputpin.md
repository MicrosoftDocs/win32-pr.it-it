---
description: Metodo del costruttore.
ms.assetid: a853813d-cdf6-4cb4-8288-62685a883b56
title: Costruttore CBaseInputPin. CBaseInputPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.CBaseInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 554c768f2cb99fda77aa87cfc916580b948da0ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331651"
---
# <a name="cbaseinputpincbaseinputpin-constructor"></a><span data-ttu-id="bb7d7-103">Costruttore CBaseInputPin. CBaseInputPin</span><span class="sxs-lookup"><span data-stu-id="bb7d7-103">CBaseInputPin.CBaseInputPin constructor</span></span>

<span data-ttu-id="bb7d7-104">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="bb7d7-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb7d7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bb7d7-105">Syntax</span></span>


```C++
CBaseInputPin(
   TCHAR       *pObjectName,
   CBaseFilter *pFilter,
   CCritSec    *pLock,
   HRESULT     *phr,
   LPCWSTR     pPinName
);
```



## <a name="parameters"></a><span data-ttu-id="bb7d7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="bb7d7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb7d7-107">*pObjectName*</span><span class="sxs-lookup"><span data-stu-id="bb7d7-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="bb7d7-108">Stringa contenente il nome di debug dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="bb7d7-108">String containing the debug name of the object.</span></span> <span data-ttu-id="bb7d7-109">Per ulteriori informazioni, vedere [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="bb7d7-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="bb7d7-110">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="bb7d7-110">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="bb7d7-111">Puntatore al filtro che ha creato questo pin.</span><span class="sxs-lookup"><span data-stu-id="bb7d7-111">Pointer to the filter that created this pin.</span></span>

</dd> <dt>

<span data-ttu-id="bb7d7-112">*pLock*</span><span class="sxs-lookup"><span data-stu-id="bb7d7-112">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="bb7d7-113">Puntatore a un blocco [**CCritSec**](ccritsec.md) , usato per serializzare le modifiche di stato.</span><span class="sxs-lookup"><span data-stu-id="bb7d7-113">Pointer to a [**CCritSec**](ccritsec.md) lock, used to serialize state changes.</span></span> <span data-ttu-id="bb7d7-114">Può trattarsi della stessa sezione critica del blocco filter, [**CBaseFilter:: m \_ pLock**](cbasefilter-m-plock.md).</span><span class="sxs-lookup"><span data-stu-id="bb7d7-114">This can be the same critical section as the filter lock, [**CBaseFilter::m\_pLock**](cbasefilter-m-plock.md).</span></span>

</dd> <dt>

<span data-ttu-id="bb7d7-115">*PHR*</span><span class="sxs-lookup"><span data-stu-id="bb7d7-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="bb7d7-116">Puntatore a una variabile che riceve un valore **HRESULT** che indica l'esito positivo o negativo del metodo.</span><span class="sxs-lookup"><span data-stu-id="bb7d7-116">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span>

</dd> <dt>

<span data-ttu-id="bb7d7-117">*pPinName*</span><span class="sxs-lookup"><span data-stu-id="bb7d7-117">*pPinName*</span></span> 
</dt> <dd>

<span data-ttu-id="bb7d7-118">Stringa di caratteri wide contenente il nome del PIN (usato anche come identificatore del pin).</span><span class="sxs-lookup"><span data-stu-id="bb7d7-118">Wide-character string containing the pin name (also used as the pin identifier).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bb7d7-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="bb7d7-119">Remarks</span></span>

<span data-ttu-id="bb7d7-120">Tutti i parametri vengono passati direttamente al costruttore [**CBasePin**](cbasepin-cbasepin.md) .</span><span class="sxs-lookup"><span data-stu-id="bb7d7-120">All of the parameters are passed directly to the [**CBasePin**](cbasepin-cbasepin.md) constructor.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb7d7-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bb7d7-121">Requirements</span></span>



| <span data-ttu-id="bb7d7-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb7d7-122">Requirement</span></span> | <span data-ttu-id="bb7d7-123">Valore</span><span class="sxs-lookup"><span data-stu-id="bb7d7-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb7d7-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bb7d7-124">Header</span></span><br/>  | <dl> <span data-ttu-id="bb7d7-125"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bb7d7-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="bb7d7-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="bb7d7-126">Library</span></span><br/> | <dl> <span data-ttu-id="bb7d7-127"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="bb7d7-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb7d7-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bb7d7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb7d7-129">**Classe CBaseInputPin**</span><span class="sxs-lookup"><span data-stu-id="bb7d7-129">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




