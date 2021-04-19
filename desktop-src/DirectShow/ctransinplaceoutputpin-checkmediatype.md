---
description: Il metodo CheckMediaType determina se il pin accetta un tipo di supporto specifico.
ms.assetid: be720021-ef7b-4281-a9f4-93abbdafc75d
title: Metodo CTransInPlaceOutputPin. CheckMediaType (Transip. h)
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
ms.openlocfilehash: b0a422851bc7e09075076decc39d57b85d1052ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326184"
---
# <a name="ctransinplaceoutputpincheckmediatype-method"></a><span data-ttu-id="06195-103">CTransInPlaceOutputPin. CheckMediaType, metodo</span><span class="sxs-lookup"><span data-stu-id="06195-103">CTransInPlaceOutputPin.CheckMediaType method</span></span>

<span data-ttu-id="06195-104">Il `CheckMediaType` metodo determina se il pin accetta un tipo di supporto specifico.</span><span class="sxs-lookup"><span data-stu-id="06195-104">The `CheckMediaType` method determines if the pin accepts a specific media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="06195-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="06195-105">Syntax</span></span>


```C++
HRESULT CheckMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="06195-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="06195-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06195-107">*PMT*</span><span class="sxs-lookup"><span data-stu-id="06195-107">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="06195-108">Puntatore a un oggetto [**CMediaType**](cmediatype.md) che contiene il tipo di supporto proposto.</span><span class="sxs-lookup"><span data-stu-id="06195-108">Pointer to a [**CMediaType**](cmediatype.md) object that contains the proposed media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06195-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="06195-109">Return value</span></span>

<span data-ttu-id="06195-110">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="06195-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="06195-111">I valori possibili includono quelli mostrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="06195-111">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="06195-112">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="06195-112">Return code</span></span>                                                                                                | <span data-ttu-id="06195-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="06195-113">Description</span></span>                         |
|------------------------------------------------------------------------------------------------------------|-------------------------------------|
| <dl> <span data-ttu-id="06195-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="06195-114"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="06195-115">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="06195-115">Success.</span></span><br/>                 |
| <dl> <span data-ttu-id="06195-116"><dt>**\_tipo VFW \_ E \_ non \_ accettato**</dt></span><span class="sxs-lookup"><span data-stu-id="06195-116"><dt>**VFW\_E\_TYPE\_NOT\_ACCEPTED**</dt></span></span> </dl> | <span data-ttu-id="06195-117">Tipo di supporto non accettato.</span><span class="sxs-lookup"><span data-stu-id="06195-117">Media type not accepted.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="06195-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="06195-118">Remarks</span></span>

<span data-ttu-id="06195-119">Questo metodo esegue l'override del metodo [**CTransformOutputPin:: CheckMediaType**](ctransformoutputpin-checkmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="06195-119">This method overrides the [**CTransformOutputPin::CheckMediaType**](ctransformoutputpin-checkmediatype.md) method.</span></span>

<span data-ttu-id="06195-120">Se il filtro è già in streaming e usa due allocatori, questo metodo rifiuterà eventuali modifiche al formato.</span><span class="sxs-lookup"><span data-stu-id="06195-120">If the filter is already streaming and is using two allocators, this method rejects any format changes.</span></span> <span data-ttu-id="06195-121">In caso contrario, questo metodo chiama il metodo [**CTransformFilter:: CheckInputType**](ctransformfilter-checkinputtype.md) del filtro per verificare il tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="06195-121">Otherwise, this method calls the filter's [**CTransformFilter::CheckInputType**](ctransformfilter-checkinputtype.md) method to check the media type.</span></span> <span data-ttu-id="06195-122">Se il pin di input è connesso, viene chiamato anche il metodo [**Ipin:: QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) sul pin di output upstream.</span><span class="sxs-lookup"><span data-stu-id="06195-122">If the input pin is connected, it also calls the [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) method on the upstream output pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="06195-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="06195-123">Requirements</span></span>



| <span data-ttu-id="06195-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="06195-124">Requirement</span></span> | <span data-ttu-id="06195-125">Valore</span><span class="sxs-lookup"><span data-stu-id="06195-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06195-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="06195-126">Header</span></span><br/>  | <dl> <span data-ttu-id="06195-127"><dt>Transip. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="06195-127"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="06195-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="06195-128">Library</span></span><br/> | <dl> <span data-ttu-id="06195-129"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="06195-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06195-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="06195-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06195-131">**Classe CTransInPlaceOutputPin**</span><span class="sxs-lookup"><span data-stu-id="06195-131">**CTransInPlaceOutputPin Class**</span></span>](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




