---
description: 'Metodo CTransInPlaceInputPin.CheckMediaType: il metodo CheckMediaType determina se il pin accetta un tipo di supporto specifico.'
ms.assetid: 2d5f784a-8970-487d-94ef-d96d04f8eb2e
title: Metodo CTransInPlaceInputPin.CheckMediaType (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5de3cec87d740db42824b0d7abf1ee4bfc6aeecb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094799"
---
# <a name="ctransinplaceinputpincheckmediatype-method"></a><span data-ttu-id="46fc6-103">Metodo CTransInPlaceInputPin.CheckMediaType</span><span class="sxs-lookup"><span data-stu-id="46fc6-103">CTransInPlaceInputPin.CheckMediaType method</span></span>

<span data-ttu-id="46fc6-104">Il `CheckMediaType` metodo determina se il pin accetta un tipo di supporto specifico.</span><span class="sxs-lookup"><span data-stu-id="46fc6-104">The `CheckMediaType` method determines if the pin accepts a specific media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="46fc6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="46fc6-105">Syntax</span></span>


```C++
HRESULT CheckMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="46fc6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="46fc6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46fc6-107">*Pmt*</span><span class="sxs-lookup"><span data-stu-id="46fc6-107">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="46fc6-108">Puntatore a un [**oggetto CMediaType**](cmediatype.md) che contiene il tipo di supporto proposto.</span><span class="sxs-lookup"><span data-stu-id="46fc6-108">Pointer to a [**CMediaType**](cmediatype.md) object that contains the proposed media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46fc6-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="46fc6-109">Return value</span></span>

<span data-ttu-id="46fc6-110">Restituisce S \_ OK se il tipo di supporto proposto è accettabile.</span><span class="sxs-lookup"><span data-stu-id="46fc6-110">Returns S\_OK if the proposed media type is acceptable.</span></span> <span data-ttu-id="46fc6-111">In caso contrario, restituisce S \_ FALSE o un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="46fc6-111">Otherwise, returns S\_FALSE or an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="46fc6-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="46fc6-112">Remarks</span></span>

<span data-ttu-id="46fc6-113">Questo metodo esegue l'override [**del metodo CTransformInputPin::CheckMediaType.**](ctransforminputpin-checkmediatype.md)</span><span class="sxs-lookup"><span data-stu-id="46fc6-113">This method overrides the [**CTransformInputPin::CheckMediaType**](ctransforminputpin-checkmediatype.md) method.</span></span> <span data-ttu-id="46fc6-114">Chiama il metodo [**CTransformFilter::CheckInputType**](ctransformfilter-checkinputtype.md) del filtro per controllare il tipo di input.</span><span class="sxs-lookup"><span data-stu-id="46fc6-114">It calls the filter's [**CTransformFilter::CheckInputType**](ctransformfilter-checkinputtype.md) method to check the input type.</span></span> <span data-ttu-id="46fc6-115">Se il pin di output è connesso, questo metodo chiama anche il metodo [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) sul pin di input downstream.</span><span class="sxs-lookup"><span data-stu-id="46fc6-115">If the output pin is connected, this method also calls the [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) method on the downstream input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="46fc6-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="46fc6-116">Requirements</span></span>



| <span data-ttu-id="46fc6-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="46fc6-117">Requirement</span></span> | <span data-ttu-id="46fc6-118">Valore</span><span class="sxs-lookup"><span data-stu-id="46fc6-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46fc6-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="46fc6-119">Header</span></span><br/>  | <dl> <span data-ttu-id="46fc6-120"><dt>Transip.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="46fc6-120"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="46fc6-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="46fc6-121">Library</span></span><br/> | <dl> <span data-ttu-id="46fc6-122"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="46fc6-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46fc6-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="46fc6-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46fc6-124">**Classe CTransInPlaceInputPin**</span><span class="sxs-lookup"><span data-stu-id="46fc6-124">**CTransInPlaceInputPin Class**</span></span>](ctransinplaceinputpin.md)
</dt> </dl>

 

 




