---
description: 'Metodo CTransInPlaceFilter.GetPin: il metodo GetPin recupera un pin.'
ms.assetid: d8e4973b-2af4-4141-ab2e-ea2159cd51be
title: Metodo CTransInPlaceFilter.GetPin (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.GetPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1075f2a14c58b085b73f2e4283458286c118a7ae
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084769"
---
# <a name="ctransinplacefiltergetpin-method"></a><span data-ttu-id="a0fae-103">Metodo CTransInPlaceFilter.GetPin</span><span class="sxs-lookup"><span data-stu-id="a0fae-103">CTransInPlaceFilter.GetPin method</span></span>

<span data-ttu-id="a0fae-104">Il `GetPin` metodo recupera un segnaposto.</span><span class="sxs-lookup"><span data-stu-id="a0fae-104">The `GetPin` method retrieves a pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0fae-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a0fae-105">Syntax</span></span>


```C++
virtual CBasePin* GetPin(
   int n
);
```



## <a name="parameters"></a><span data-ttu-id="a0fae-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a0fae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0fae-107">*n*</span><span class="sxs-lookup"><span data-stu-id="a0fae-107">*n*</span></span> 
</dt> <dd>

<span data-ttu-id="a0fae-108">Numero del pin specificato, indicizzato da zero.</span><span class="sxs-lookup"><span data-stu-id="a0fae-108">Number of the specified pin, indexed from zero.</span></span> <span data-ttu-id="a0fae-109">In questo filtro, pin 0 è il pin di input e pin 1 è il pin di output.</span><span class="sxs-lookup"><span data-stu-id="a0fae-109">On this filter, pin 0 is the input pin, and pin 1 is the output pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0fae-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a0fae-110">Return value</span></span>

<span data-ttu-id="a0fae-111">Restituisce un puntatore [**all'oggetto CBasePin**](cbasepin.md) che implementa il pin oppure **NULL se** il metodo ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="a0fae-111">Returns a pointer to the [**CBasePin**](cbasepin.md) object that implements the pin, or **NULL** if the method fails.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0fae-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="a0fae-112">Remarks</span></span>

<span data-ttu-id="a0fae-113">Questo metodo esegue l'override [**del metodo CTransformFilter::GetPin.**](ctransformfilter-getpin.md)</span><span class="sxs-lookup"><span data-stu-id="a0fae-113">This method overrides the [**CTransformFilter::GetPin**](ctransformfilter-getpin.md) method.</span></span> <span data-ttu-id="a0fae-114">La prima volta che viene chiamato il metodo , vengono creati entrambi i segnaposto.</span><span class="sxs-lookup"><span data-stu-id="a0fae-114">The first time the method is called, it creates both pins.</span></span>

<span data-ttu-id="a0fae-115">Questo metodo non incrementa il conteggio dei riferimenti sul segnaposto restituito, quindi il pin restituito non ha un conteggio dei riferimenti in sospeso.</span><span class="sxs-lookup"><span data-stu-id="a0fae-115">This method does not increment the reference count on the returned pin, so the returned pin does not have an outstanding reference count.</span></span> <span data-ttu-id="a0fae-116">Se il chiamante deve mantenere un riferimento sul pin, deve chiamare il metodo **IUnknown::AddRef** sul pin.</span><span class="sxs-lookup"><span data-stu-id="a0fae-116">If the caller needs to keep a reference on the pin, it should call the **IUnknown::AddRef** method on the pin.</span></span>

<span data-ttu-id="a0fae-117">Se il filtro usa i pin [**CTransInPlaceInputPin**](ctransinplaceinputpin.md) e [**CTransInPlaceOutputPin**](ctransinplaceoutputpin.md) predefiniti, probabilmente non è necessario eseguire l'override di questo metodo.</span><span class="sxs-lookup"><span data-stu-id="a0fae-117">If the filter uses the default [**CTransInPlaceInputPin**](ctransinplaceinputpin.md) and [**CTransInPlaceOutputPin**](ctransinplaceoutputpin.md) pins, you probably do not need to override this method.</span></span> <span data-ttu-id="a0fae-118">Se il filtro usa segnaposto che estendono tali classi, tuttavia, è necessario eseguire l'override di questo metodo per creare segnaposti di quel tipo.</span><span class="sxs-lookup"><span data-stu-id="a0fae-118">If the filter uses pins that extend those classes, however, you must override this method to create pins of that type.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0fae-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a0fae-119">Requirements</span></span>



| <span data-ttu-id="a0fae-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0fae-120">Requirement</span></span> | <span data-ttu-id="a0fae-121">Valore</span><span class="sxs-lookup"><span data-stu-id="a0fae-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0fae-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a0fae-122">Header</span></span><br/>  | <dl> <span data-ttu-id="a0fae-123"><dt>Transip.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="a0fae-123"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a0fae-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="a0fae-124">Library</span></span><br/> | <dl> <span data-ttu-id="a0fae-125"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="a0fae-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0fae-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a0fae-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0fae-127">**Classe CTransInPlaceFilter**</span><span class="sxs-lookup"><span data-stu-id="a0fae-127">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




