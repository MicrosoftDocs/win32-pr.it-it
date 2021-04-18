---
description: Il metodo GetPin recupera un PIN.
ms.assetid: d8e4973b-2af4-4141-ab2e-ea2159cd51be
title: Metodo CTransInPlaceFilter. GetPin (Transip. h)
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
ms.openlocfilehash: ae93b663af5427bc61367ae03a3abd6790b8634a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331121"
---
# <a name="ctransinplacefiltergetpin-method"></a><span data-ttu-id="bb076-103">CTransInPlaceFilter. GetPin, metodo</span><span class="sxs-lookup"><span data-stu-id="bb076-103">CTransInPlaceFilter.GetPin method</span></span>

<span data-ttu-id="bb076-104">Il `GetPin` metodo recupera un PIN.</span><span class="sxs-lookup"><span data-stu-id="bb076-104">The `GetPin` method retrieves a pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb076-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bb076-105">Syntax</span></span>


```C++
virtual CBasePin* GetPin(
   int n
);
```



## <a name="parameters"></a><span data-ttu-id="bb076-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="bb076-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb076-107">*n*</span><span class="sxs-lookup"><span data-stu-id="bb076-107">*n*</span></span> 
</dt> <dd>

<span data-ttu-id="bb076-108">Numero del PIN specificato, indicizzato da zero.</span><span class="sxs-lookup"><span data-stu-id="bb076-108">Number of the specified pin, indexed from zero.</span></span> <span data-ttu-id="bb076-109">In questo filtro, pin 0 è il pin di input e pin 1 è il pin di output.</span><span class="sxs-lookup"><span data-stu-id="bb076-109">On this filter, pin 0 is the input pin, and pin 1 is the output pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb076-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bb076-110">Return value</span></span>

<span data-ttu-id="bb076-111">Restituisce un puntatore all'oggetto [**CBasePin**](cbasepin.md) che implementa il PIN oppure **null** se il metodo ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="bb076-111">Returns a pointer to the [**CBasePin**](cbasepin.md) object that implements the pin, or **NULL** if the method fails.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb076-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="bb076-112">Remarks</span></span>

<span data-ttu-id="bb076-113">Questo metodo esegue l'override del metodo [**CTransformFilter:: GetPin**](ctransformfilter-getpin.md) .</span><span class="sxs-lookup"><span data-stu-id="bb076-113">This method overrides the [**CTransformFilter::GetPin**](ctransformfilter-getpin.md) method.</span></span> <span data-ttu-id="bb076-114">La prima volta che viene chiamato il metodo, vengono creati entrambi i pin.</span><span class="sxs-lookup"><span data-stu-id="bb076-114">The first time the method is called, it creates both pins.</span></span>

<span data-ttu-id="bb076-115">Questo metodo non incrementa il conteggio dei riferimenti sul pin restituito, quindi il pin restituito non dispone di un conteggio dei riferimenti in attesa.</span><span class="sxs-lookup"><span data-stu-id="bb076-115">This method does not increment the reference count on the returned pin, so the returned pin does not have an outstanding reference count.</span></span> <span data-ttu-id="bb076-116">Se il chiamante deve mantenere un riferimento al pin, deve chiamare il metodo **IUnknown:: AddRef** sul pin.</span><span class="sxs-lookup"><span data-stu-id="bb076-116">If the caller needs to keep a reference on the pin, it should call the **IUnknown::AddRef** method on the pin.</span></span>

<span data-ttu-id="bb076-117">Se il filtro usa i pin predefiniti [**CTransInPlaceInputPin**](ctransinplaceinputpin.md) e [**CTransInPlaceOutputPin**](ctransinplaceoutputpin.md) , probabilmente non è necessario eseguire l'override di questo metodo.</span><span class="sxs-lookup"><span data-stu-id="bb076-117">If the filter uses the default [**CTransInPlaceInputPin**](ctransinplaceinputpin.md) and [**CTransInPlaceOutputPin**](ctransinplaceoutputpin.md) pins, you probably do not need to override this method.</span></span> <span data-ttu-id="bb076-118">Se il filtro usa pin che estendono tali classi, tuttavia, è necessario eseguire l'override di questo metodo per creare pin di quel tipo.</span><span class="sxs-lookup"><span data-stu-id="bb076-118">If the filter uses pins that extend those classes, however, you must override this method to create pins of that type.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb076-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bb076-119">Requirements</span></span>



| <span data-ttu-id="bb076-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb076-120">Requirement</span></span> | <span data-ttu-id="bb076-121">Valore</span><span class="sxs-lookup"><span data-stu-id="bb076-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb076-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bb076-122">Header</span></span><br/>  | <dl> <span data-ttu-id="bb076-123"><dt>Transip. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bb076-123"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="bb076-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="bb076-124">Library</span></span><br/> | <dl> <span data-ttu-id="bb076-125"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="bb076-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb076-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bb076-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb076-127">**Classe CTransInPlaceFilter**</span><span class="sxs-lookup"><span data-stu-id="bb076-127">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




