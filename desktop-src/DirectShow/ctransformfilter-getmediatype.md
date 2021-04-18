---
description: Il metodo GetMediaType recupera un tipo di supporto preferito per il pin di output.
ms.assetid: 9a1b123b-aa8a-4bf0-a926-466ded24e506
title: Metodo CTransformFilter. GetMediaType (Transfrm. h)
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
ms.openlocfilehash: ba751e291a1ffa8e030be7e77cfd456956718baa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331312"
---
# <a name="ctransformfiltergetmediatype-method"></a><span data-ttu-id="d47b5-103">CTransformFilter. GetMediaType, metodo</span><span class="sxs-lookup"><span data-stu-id="d47b5-103">CTransformFilter.GetMediaType method</span></span>

<span data-ttu-id="d47b5-104">Il `GetMediaType` metodo recupera un tipo di supporto preferito per il pin di output.</span><span class="sxs-lookup"><span data-stu-id="d47b5-104">The `GetMediaType` method retrieves a preferred media type for the output pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="d47b5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d47b5-105">Syntax</span></span>


```C++
virtual HRESULT GetMediaType(
   int        iPosition,
   CMediaType *pMediaType
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="d47b5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d47b5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d47b5-107">*iPosition*</span><span class="sxs-lookup"><span data-stu-id="d47b5-107">*iPosition*</span></span> 
</dt> <dd>

<span data-ttu-id="d47b5-108">Valore di indice in base zero.</span><span class="sxs-lookup"><span data-stu-id="d47b5-108">Zero-based index value.</span></span>

</dd> <dt>

<span data-ttu-id="d47b5-109">*pMediaType*</span><span class="sxs-lookup"><span data-stu-id="d47b5-109">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="d47b5-110">Puntatore a un oggetto [**CMediaType**](cmediatype.md) che riceve il tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="d47b5-110">Pointer to a [**CMediaType**](cmediatype.md) object that receives the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d47b5-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d47b5-111">Return value</span></span>

<span data-ttu-id="d47b5-112">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d47b5-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="d47b5-113">I valori possibili includono quelli mostrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="d47b5-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="d47b5-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="d47b5-114">Return code</span></span>                                                                                            | <span data-ttu-id="d47b5-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d47b5-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="d47b5-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d47b5-116"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="d47b5-117">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="d47b5-117">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="d47b5-118"><dt>**\_non ci \_ sono \_ altri \_ elementi di VFW**</dt></span><span class="sxs-lookup"><span data-stu-id="d47b5-118"><dt>**VFW\_S\_NO\_MORE\_ITEMS**</dt></span></span> </dl> | <span data-ttu-id="d47b5-119">Indice non compreso nell'intervallo.</span><span class="sxs-lookup"><span data-stu-id="d47b5-119">Index out of range.</span></span><br/>   |
| <dl> <span data-ttu-id="d47b5-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="d47b5-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>           | <span data-ttu-id="d47b5-121">Indice minore di zero.</span><span class="sxs-lookup"><span data-stu-id="d47b5-121">Index less than zero.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d47b5-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="d47b5-122">Remarks</span></span>

<span data-ttu-id="d47b5-123">Il metodo [**CTransformOutputPin:: GetMediaType**](ctransformoutputpin-getmediatype.md) del PIN di output chiama questo metodo.</span><span class="sxs-lookup"><span data-stu-id="d47b5-123">The output pin's [**CTransformOutputPin::GetMediaType**](ctransformoutputpin-getmediatype.md) method calls this method.</span></span> <span data-ttu-id="d47b5-124">La classe derivata deve implementare questo metodo.</span><span class="sxs-lookup"><span data-stu-id="d47b5-124">The derived class must implement this method.</span></span> <span data-ttu-id="d47b5-125">Per ulteriori informazioni, vedere [**CBasePin:: GetMediaType**](cbasepin-getmediatype.md).</span><span class="sxs-lookup"><span data-stu-id="d47b5-125">For more information, see [**CBasePin::GetMediaType**](cbasepin-getmediatype.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d47b5-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d47b5-126">Requirements</span></span>



| <span data-ttu-id="d47b5-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="d47b5-127">Requirement</span></span> | <span data-ttu-id="d47b5-128">Valore</span><span class="sxs-lookup"><span data-stu-id="d47b5-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d47b5-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d47b5-129">Header</span></span><br/>  | <dl> <span data-ttu-id="d47b5-130"><dt>Transfrm. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d47b5-130"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d47b5-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="d47b5-131">Library</span></span><br/> | <dl> <span data-ttu-id="d47b5-132"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d47b5-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d47b5-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d47b5-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d47b5-134">**Classe CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="d47b5-134">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




