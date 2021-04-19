---
description: Il metodo CheckMediaType determina se il pin accetta un tipo di supporto specifico.
ms.assetid: 2d5f784a-8970-487d-94ef-d96d04f8eb2e
title: Metodo CTransInPlaceInputPin. CheckMediaType (Transip. h)
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
ms.openlocfilehash: 22f271759bc0ade6b820aed2039bbc16a2cf4a31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326203"
---
# <a name="ctransinplaceinputpincheckmediatype-method"></a><span data-ttu-id="1ed78-103">CTransInPlaceInputPin. CheckMediaType, metodo</span><span class="sxs-lookup"><span data-stu-id="1ed78-103">CTransInPlaceInputPin.CheckMediaType method</span></span>

<span data-ttu-id="1ed78-104">Il `CheckMediaType` metodo determina se il pin accetta un tipo di supporto specifico.</span><span class="sxs-lookup"><span data-stu-id="1ed78-104">The `CheckMediaType` method determines if the pin accepts a specific media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ed78-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1ed78-105">Syntax</span></span>


```C++
HRESULT CheckMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="1ed78-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1ed78-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ed78-107">*PMT*</span><span class="sxs-lookup"><span data-stu-id="1ed78-107">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="1ed78-108">Puntatore a un oggetto [**CMediaType**](cmediatype.md) che contiene il tipo di supporto proposto.</span><span class="sxs-lookup"><span data-stu-id="1ed78-108">Pointer to a [**CMediaType**](cmediatype.md) object that contains the proposed media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ed78-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1ed78-109">Return value</span></span>

<span data-ttu-id="1ed78-110">Restituisce \_ OK se il tipo di supporto proposto è accettabile.</span><span class="sxs-lookup"><span data-stu-id="1ed78-110">Returns S\_OK if the proposed media type is acceptable.</span></span> <span data-ttu-id="1ed78-111">In caso contrario, restituisce \_ false o un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="1ed78-111">Otherwise, returns S\_FALSE or an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ed78-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="1ed78-112">Remarks</span></span>

<span data-ttu-id="1ed78-113">Questo metodo esegue l'override del metodo [**CTransformInputPin:: CheckMediaType**](ctransforminputpin-checkmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="1ed78-113">This method overrides the [**CTransformInputPin::CheckMediaType**](ctransforminputpin-checkmediatype.md) method.</span></span> <span data-ttu-id="1ed78-114">Chiama il metodo [**CTransformFilter:: CheckInputType**](ctransformfilter-checkinputtype.md) del filtro per verificare il tipo di input.</span><span class="sxs-lookup"><span data-stu-id="1ed78-114">It calls the filter's [**CTransformFilter::CheckInputType**](ctransformfilter-checkinputtype.md) method to check the input type.</span></span> <span data-ttu-id="1ed78-115">Se il pin di output è connesso, questo metodo chiama anche il metodo [**Ipin:: QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) sul pin di input downstream.</span><span class="sxs-lookup"><span data-stu-id="1ed78-115">If the output pin is connected, this method also calls the [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) method on the downstream input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ed78-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1ed78-116">Requirements</span></span>



| <span data-ttu-id="1ed78-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ed78-117">Requirement</span></span> | <span data-ttu-id="1ed78-118">Valore</span><span class="sxs-lookup"><span data-stu-id="1ed78-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ed78-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1ed78-119">Header</span></span><br/>  | <dl> <span data-ttu-id="1ed78-120"><dt>Transip. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1ed78-120"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1ed78-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="1ed78-121">Library</span></span><br/> | <dl> <span data-ttu-id="1ed78-122"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="1ed78-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ed78-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1ed78-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ed78-124">**Classe CTransInPlaceInputPin**</span><span class="sxs-lookup"><span data-stu-id="1ed78-124">**CTransInPlaceInputPin Class**</span></span>](ctransinplaceinputpin.md)
</dt> </dl>

 

 




