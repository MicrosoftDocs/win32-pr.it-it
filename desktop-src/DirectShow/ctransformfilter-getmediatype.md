---
description: 'Metodo CTransformFilter.GetMediaType: il metodo GetMediaType recupera un tipo di supporto preferito per il pin di output.'
ms.assetid: 9a1b123b-aa8a-4bf0-a926-466ded24e506
title: Metodo CTransformFilter.GetMediaType (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6415b8e3d8ae4e292b7e2592b123120927081ea8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095119"
---
# <a name="ctransformfiltergetmediatype-method"></a><span data-ttu-id="fc48b-103">Metodo CTransformFilter.GetMediaType</span><span class="sxs-lookup"><span data-stu-id="fc48b-103">CTransformFilter.GetMediaType method</span></span>

<span data-ttu-id="fc48b-104">Il `GetMediaType` metodo recupera un tipo di supporto preferito per il pin di output.</span><span class="sxs-lookup"><span data-stu-id="fc48b-104">The `GetMediaType` method retrieves a preferred media type for the output pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc48b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fc48b-105">Syntax</span></span>


```C++
virtual HRESULT GetMediaType(
   int        iPosition,
   CMediaType *pMediaType
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="fc48b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="fc48b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc48b-107">*iPosition*</span><span class="sxs-lookup"><span data-stu-id="fc48b-107">*iPosition*</span></span> 
</dt> <dd>

<span data-ttu-id="fc48b-108">Valore di indice in base zero.</span><span class="sxs-lookup"><span data-stu-id="fc48b-108">Zero-based index value.</span></span>

</dd> <dt>

<span data-ttu-id="fc48b-109">*pMediaType*</span><span class="sxs-lookup"><span data-stu-id="fc48b-109">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="fc48b-110">Puntatore a un [**oggetto CMediaType**](cmediatype.md) che riceve il tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="fc48b-110">Pointer to a [**CMediaType**](cmediatype.md) object that receives the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc48b-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fc48b-111">Return value</span></span>

<span data-ttu-id="fc48b-112">Restituisce un **valore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="fc48b-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="fc48b-113">I valori possibili includono quelli illustrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="fc48b-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="fc48b-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="fc48b-114">Return code</span></span>                                                                                            | <span data-ttu-id="fc48b-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fc48b-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="fc48b-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="fc48b-116"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="fc48b-117">Operazione completata.</span><span class="sxs-lookup"><span data-stu-id="fc48b-117">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="fc48b-118"><dt>**VFW \_ S \_ NO \_ MORE \_ ITEMS**</dt></span><span class="sxs-lookup"><span data-stu-id="fc48b-118"><dt>**VFW\_S\_NO\_MORE\_ITEMS**</dt></span></span> </dl> | <span data-ttu-id="fc48b-119">Indice non compreso nell'intervallo.</span><span class="sxs-lookup"><span data-stu-id="fc48b-119">Index out of range.</span></span><br/>   |
| <dl> <span data-ttu-id="fc48b-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="fc48b-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>           | <span data-ttu-id="fc48b-121">Indice minore di zero.</span><span class="sxs-lookup"><span data-stu-id="fc48b-121">Index less than zero.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="fc48b-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="fc48b-122">Remarks</span></span>

<span data-ttu-id="fc48b-123">Il metodo [**CTransformOutputPin::GetMediaType**](ctransformoutputpin-getmediatype.md) del pin di output chiama questo metodo.</span><span class="sxs-lookup"><span data-stu-id="fc48b-123">The output pin's [**CTransformOutputPin::GetMediaType**](ctransformoutputpin-getmediatype.md) method calls this method.</span></span> <span data-ttu-id="fc48b-124">La classe derivata deve implementare questo metodo.</span><span class="sxs-lookup"><span data-stu-id="fc48b-124">The derived class must implement this method.</span></span> <span data-ttu-id="fc48b-125">Per altre informazioni, vedere [**CBasePin::GetMediaType**](cbasepin-getmediatype.md).</span><span class="sxs-lookup"><span data-stu-id="fc48b-125">For more information, see [**CBasePin::GetMediaType**](cbasepin-getmediatype.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fc48b-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fc48b-126">Requirements</span></span>



| <span data-ttu-id="fc48b-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc48b-127">Requirement</span></span> | <span data-ttu-id="fc48b-128">Valore</span><span class="sxs-lookup"><span data-stu-id="fc48b-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc48b-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fc48b-129">Header</span></span><br/>  | <dl> <span data-ttu-id="fc48b-130"><dt>Transfrm.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="fc48b-130"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="fc48b-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="fc48b-131">Library</span></span><br/> | <dl> <span data-ttu-id="fc48b-132"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="fc48b-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc48b-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fc48b-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc48b-134">**Classe CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="fc48b-134">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




