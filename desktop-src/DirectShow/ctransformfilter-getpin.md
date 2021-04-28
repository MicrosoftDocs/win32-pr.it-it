---
description: 'Metodo CTransformFilter.GetPin: il metodo GetPin recupera un pin.'
ms.assetid: 5d278ef0-e5ce-439e-93b1-fec988c55854
title: Metodo CTransformFilter.GetPin (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.GetPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8e76cafce2ca5a9881b87d9248c144dc584971c0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085079"
---
# <a name="ctransformfiltergetpin-method"></a><span data-ttu-id="eccf2-103">Metodo CTransformFilter.GetPin</span><span class="sxs-lookup"><span data-stu-id="eccf2-103">CTransformFilter.GetPin method</span></span>

<span data-ttu-id="eccf2-104">Il `GetPin` metodo recupera un pin.</span><span class="sxs-lookup"><span data-stu-id="eccf2-104">The `GetPin` method retrieves a pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="eccf2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="eccf2-105">Syntax</span></span>


```C++
virtual CBasePin* GetPin(
   int n
);
```



## <a name="parameters"></a><span data-ttu-id="eccf2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="eccf2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eccf2-107">*n*</span><span class="sxs-lookup"><span data-stu-id="eccf2-107">*n*</span></span> 
</dt> <dd>

<span data-ttu-id="eccf2-108">Numero del pin specificato, indicizzato da zero.</span><span class="sxs-lookup"><span data-stu-id="eccf2-108">Number of the specified pin, indexed from zero.</span></span> <span data-ttu-id="eccf2-109">In questo filtro, pin 0 è il pin di input e pin 1 è il pin di output.</span><span class="sxs-lookup"><span data-stu-id="eccf2-109">On this filter, pin 0 is the input pin, and pin 1 is the output pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eccf2-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="eccf2-110">Return value</span></span>

<span data-ttu-id="eccf2-111">Restituisce un puntatore [**all'oggetto CBasePin**](cbasepin.md) che implementa il pin oppure **NULL** se il metodo ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="eccf2-111">Returns a pointer to the [**CBasePin**](cbasepin.md) object that implements the pin, or **NULL** if the method fails.</span></span>

## <a name="remarks"></a><span data-ttu-id="eccf2-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="eccf2-112">Remarks</span></span>

<span data-ttu-id="eccf2-113">Questo metodo implementa il metodo [**CBaseFilter::GetPin**](cbasefilter-getpin.md) virtuale puro.</span><span class="sxs-lookup"><span data-stu-id="eccf2-113">This method implements the pure virtual [**CBaseFilter::GetPin**](cbasefilter-getpin.md) method.</span></span> <span data-ttu-id="eccf2-114">La prima volta che viene chiamato il metodo , vengono creati entrambi i pin.</span><span class="sxs-lookup"><span data-stu-id="eccf2-114">The first time the method is called, it creates both pins.</span></span>

<span data-ttu-id="eccf2-115">Questo metodo non incrementa il conteggio dei riferimenti sul pin restituito, quindi il pin restituito non ha un conteggio dei riferimenti in sospeso.</span><span class="sxs-lookup"><span data-stu-id="eccf2-115">This method does not increment the reference count on the returned pin, so the returned pin does not have an outstanding reference count.</span></span> <span data-ttu-id="eccf2-116">Se il chiamante deve mantenere un riferimento sul pin, deve chiamare il metodo **IUnknown::AddRef** sul pin.</span><span class="sxs-lookup"><span data-stu-id="eccf2-116">If the caller needs to keep a reference on the pin, it should call the **IUnknown::AddRef** method on the pin.</span></span>

<span data-ttu-id="eccf2-117">Se il filtro usa i pin [**CTransformInputPin**](ctransforminputpin.md) e [**CTransformOutputPin**](ctransformoutputpin.md) predefiniti, probabilmente non è necessario eseguire l'override di questo metodo.</span><span class="sxs-lookup"><span data-stu-id="eccf2-117">If the filter uses the default [**CTransformInputPin**](ctransforminputpin.md) and [**CTransformOutputPin**](ctransformoutputpin.md) pins, you probably do not need to override this method.</span></span> <span data-ttu-id="eccf2-118">Se il filtro usa pin che estendono tali classi, tuttavia, è necessario eseguire l'override di questo metodo per creare pin di quel tipo.</span><span class="sxs-lookup"><span data-stu-id="eccf2-118">If the filter uses pins that extend those classes, however, you must override this method to create pins of that type.</span></span>

## <a name="requirements"></a><span data-ttu-id="eccf2-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eccf2-119">Requirements</span></span>



| <span data-ttu-id="eccf2-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="eccf2-120">Requirement</span></span> | <span data-ttu-id="eccf2-121">Valore</span><span class="sxs-lookup"><span data-stu-id="eccf2-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eccf2-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="eccf2-122">Header</span></span><br/>  | <dl> <span data-ttu-id="eccf2-123"><dt>Transfrm.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="eccf2-123"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="eccf2-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="eccf2-124">Library</span></span><br/> | <dl> <span data-ttu-id="eccf2-125"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="eccf2-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eccf2-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="eccf2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eccf2-127">**Classe CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="eccf2-127">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




