---
description: 'Metodo CTransInPlaceOutputPin.CheckMediaType: il metodo CheckMediaType determina se il pin accetta un tipo di supporto specifico.'
ms.assetid: be720021-ef7b-4281-a9f4-93abbdafc75d
title: Metodo CTransInPlaceOutputPin.CheckMediaType (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 66cd29758e0b2d63db88db8b998cc79ec12efdd9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094719"
---
# <a name="ctransinplaceoutputpincheckmediatype-method"></a><span data-ttu-id="7ff5f-103">Metodo CTransInPlaceOutputPin.CheckMediaType</span><span class="sxs-lookup"><span data-stu-id="7ff5f-103">CTransInPlaceOutputPin.CheckMediaType method</span></span>

<span data-ttu-id="7ff5f-104">Il `CheckMediaType` metodo determina se il pin accetta un tipo di supporto specifico.</span><span class="sxs-lookup"><span data-stu-id="7ff5f-104">The `CheckMediaType` method determines if the pin accepts a specific media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ff5f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7ff5f-105">Syntax</span></span>


```C++
HRESULT CheckMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="7ff5f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7ff5f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ff5f-107">*Pmt*</span><span class="sxs-lookup"><span data-stu-id="7ff5f-107">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="7ff5f-108">Puntatore a un [**oggetto CMediaType**](cmediatype.md) che contiene il tipo di supporto proposto.</span><span class="sxs-lookup"><span data-stu-id="7ff5f-108">Pointer to a [**CMediaType**](cmediatype.md) object that contains the proposed media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ff5f-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7ff5f-109">Return value</span></span>

<span data-ttu-id="7ff5f-110">Restituisce un **valore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="7ff5f-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="7ff5f-111">I valori possibili includono quelli illustrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="7ff5f-111">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="7ff5f-112">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="7ff5f-112">Return code</span></span>                                                                                                | <span data-ttu-id="7ff5f-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7ff5f-113">Description</span></span>                         |
|------------------------------------------------------------------------------------------------------------|-------------------------------------|
| <dl> <span data-ttu-id="7ff5f-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7ff5f-114"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="7ff5f-115">Operazione completata.</span><span class="sxs-lookup"><span data-stu-id="7ff5f-115">Success.</span></span><br/>                 |
| <dl> <span data-ttu-id="7ff5f-116"><dt>**TIPO E VFW \_ \_ NON \_ \_ ACCETTATO**</dt></span><span class="sxs-lookup"><span data-stu-id="7ff5f-116"><dt>**VFW\_E\_TYPE\_NOT\_ACCEPTED**</dt></span></span> </dl> | <span data-ttu-id="7ff5f-117">Tipo di supporto non accettato.</span><span class="sxs-lookup"><span data-stu-id="7ff5f-117">Media type not accepted.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7ff5f-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="7ff5f-118">Remarks</span></span>

<span data-ttu-id="7ff5f-119">Questo metodo esegue l'override del metodo [**CTransformOutputPin::CheckMediaType.**](ctransformoutputpin-checkmediatype.md)</span><span class="sxs-lookup"><span data-stu-id="7ff5f-119">This method overrides the [**CTransformOutputPin::CheckMediaType**](ctransformoutputpin-checkmediatype.md) method.</span></span>

<span data-ttu-id="7ff5f-120">Se il filtro è già in streaming e usa due allocatori, questo metodo rifiuta le modifiche di formato.</span><span class="sxs-lookup"><span data-stu-id="7ff5f-120">If the filter is already streaming and is using two allocators, this method rejects any format changes.</span></span> <span data-ttu-id="7ff5f-121">In caso contrario, questo metodo chiama il metodo [**CTransformFilter::CheckInputType**](ctransformfilter-checkinputtype.md) del filtro per controllare il tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="7ff5f-121">Otherwise, this method calls the filter's [**CTransformFilter::CheckInputType**](ctransformfilter-checkinputtype.md) method to check the media type.</span></span> <span data-ttu-id="7ff5f-122">Se il pin di input è connesso, chiama anche il metodo [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) sul pin di output upstream.</span><span class="sxs-lookup"><span data-stu-id="7ff5f-122">If the input pin is connected, it also calls the [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) method on the upstream output pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ff5f-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7ff5f-123">Requirements</span></span>



| <span data-ttu-id="7ff5f-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ff5f-124">Requirement</span></span> | <span data-ttu-id="7ff5f-125">Valore</span><span class="sxs-lookup"><span data-stu-id="7ff5f-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ff5f-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7ff5f-126">Header</span></span><br/>  | <dl> <span data-ttu-id="7ff5f-127"><dt>Transip.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="7ff5f-127"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7ff5f-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="7ff5f-128">Library</span></span><br/> | <dl> <span data-ttu-id="7ff5f-129"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="7ff5f-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ff5f-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7ff5f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ff5f-131">**Classe CTransInPlaceOutputPin**</span><span class="sxs-lookup"><span data-stu-id="7ff5f-131">**CTransInPlaceOutputPin Class**</span></span>](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




