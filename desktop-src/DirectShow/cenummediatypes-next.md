---
description: 'Il metodo successivo recupera un numero specificato di tipi di supporti. Questo metodo implementa il metodo IEnumMediaTypes:: Next.'
ms.assetid: d59dea48-e36c-4ee6-9935-5a47e8a12a9e
title: Metodo CEnumMediaTypes. Next (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumMediaTypes.Next
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6b5eaa75a52f88539438cec58f024919577518e2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329852"
---
# <a name="cenummediatypesnext-method"></a><span data-ttu-id="78d3f-104">Metodo CEnumMediaTypes. Next</span><span class="sxs-lookup"><span data-stu-id="78d3f-104">CEnumMediaTypes.Next method</span></span>

<span data-ttu-id="78d3f-105">Il `Next` metodo recupera un numero specificato di tipi di supporti.</span><span class="sxs-lookup"><span data-stu-id="78d3f-105">The `Next` method retrieves a specified number of media types.</span></span> <span data-ttu-id="78d3f-106">Questo metodo implementa il metodo [**IEnumMediaTypes:: Next**](/windows/desktop/api/Strmif/nf-strmif-ienummediatypes-next) .</span><span class="sxs-lookup"><span data-stu-id="78d3f-106">This method implements the [**IEnumMediaTypes::Next**](/windows/desktop/api/Strmif/nf-strmif-ienummediatypes-next) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="78d3f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="78d3f-107">Syntax</span></span>


```C++
HRESULT Next(
   ULONG         cMediaTypes,
   AM_MEDIA_TYPE **ppMediaTypes,
   ULONG         *pcFetched
);
```



## <a name="parameters"></a><span data-ttu-id="78d3f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="78d3f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78d3f-109">*cMediaTypes*</span><span class="sxs-lookup"><span data-stu-id="78d3f-109">*cMediaTypes*</span></span> 
</dt> <dd>

<span data-ttu-id="78d3f-110">Numero di tipi di supporto da recuperare.</span><span class="sxs-lookup"><span data-stu-id="78d3f-110">Number of media types to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="78d3f-111">*ppMediaTypes*</span><span class="sxs-lookup"><span data-stu-id="78d3f-111">*ppMediaTypes*</span></span> 
</dt> <dd>

<span data-ttu-id="78d3f-112">Matrice di puntatori alle strutture di [**\_ \_ tipo multimediale am**](/windows/win32/api/strmif/ns-strmif-am_media_type) , di dimensioni *cPins*.</span><span class="sxs-lookup"><span data-stu-id="78d3f-112">Array of pointers to [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structures, of size *cPins*.</span></span>

</dd> <dt>

<span data-ttu-id="78d3f-113">*pcFetched*</span><span class="sxs-lookup"><span data-stu-id="78d3f-113">*pcFetched*</span></span> 
</dt> <dd>

<span data-ttu-id="78d3f-114">Puntatore a una variabile che riceve il numero di tipi di supporti restituiti dal metodo.</span><span class="sxs-lookup"><span data-stu-id="78d3f-114">Pointer to a variable that receives the number of media types the method returned.</span></span> <span data-ttu-id="78d3f-115">Può essere **null** se *cMediaTypes* è 1.</span><span class="sxs-lookup"><span data-stu-id="78d3f-115">Can be **NULL** if *cMediaTypes* is 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78d3f-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="78d3f-116">Return value</span></span>

<span data-ttu-id="78d3f-117">Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="78d3f-117">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="78d3f-118">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="78d3f-118">Return code</span></span>                                                                                                | <span data-ttu-id="78d3f-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="78d3f-119">Description</span></span>                                                                         |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="78d3f-120"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="78d3f-120"><dt>**S\_FALSE**</dt></span></span> </dl>                    | <span data-ttu-id="78d3f-121">Non è stato possibile recuperare tutti i tipi di supporto richiesti.</span><span class="sxs-lookup"><span data-stu-id="78d3f-121">Did not retrieve as many media types as requested.</span></span><br/>                       |
| <dl> <span data-ttu-id="78d3f-122"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="78d3f-122"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="78d3f-123">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="78d3f-123">Success.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="78d3f-124"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="78d3f-124"><dt>**E\_INVALIDARG**</dt></span></span> </dl>               | <span data-ttu-id="78d3f-125">Argomento non valido.</span><span class="sxs-lookup"><span data-stu-id="78d3f-125">Invalid argument.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="78d3f-126"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="78d3f-126"><dt>**E\_POINTER**</dt></span></span> </dl>                  | <span data-ttu-id="78d3f-127">Argomento puntatore **null** .</span><span class="sxs-lookup"><span data-stu-id="78d3f-127">**NULL** pointer argument.</span></span><br/>                                               |
| <dl> <span data-ttu-id="78d3f-128"><dt>**non \_ \_ \_ \_ sincronizzato con VFW E enum \_**</dt></span><span class="sxs-lookup"><span data-stu-id="78d3f-128"><dt>**VFW\_E\_ENUM\_OUT\_OF\_SYNC**</dt></span></span> </dl> | <span data-ttu-id="78d3f-129">Lo stato del PIN è stato modificato ed è ora incoerente con l'enumeratore.</span><span class="sxs-lookup"><span data-stu-id="78d3f-129">The pin's state has changed and is now inconsistent with the enumerator.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="78d3f-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="78d3f-130">Remarks</span></span>

<span data-ttu-id="78d3f-131">Se il metodo ha esito positivo, la matrice specificata da *ppMediaTypes* contiene i puntatori alle \_ strutture del tipo di supporto am \_ .</span><span class="sxs-lookup"><span data-stu-id="78d3f-131">If the method succeeds, the array specified by *ppMediaTypes* contains pointers to AM\_MEDIA\_TYPE structures.</span></span> <span data-ttu-id="78d3f-132">Il numero di strutture è uguale a *\* pcFetched*.</span><span class="sxs-lookup"><span data-stu-id="78d3f-132">The number of structures is equal to *\*pcFetched*.</span></span> <span data-ttu-id="78d3f-133">Liberare ogni tipo di supporto chiamando la funzione [**DeleteMediaType**](deletemediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="78d3f-133">Free each media type by calling the [**DeleteMediaType**](deletemediatype.md) function.</span></span>

<span data-ttu-id="78d3f-134">Questo metodo chiama il metodo [**CBasePin:: GetMediaType**](cbasepin-getmediatype.md) del PIN per recuperare i tipi di supporto.</span><span class="sxs-lookup"><span data-stu-id="78d3f-134">This method calls the pin's [**CBasePin::GetMediaType**](cbasepin-getmediatype.md) method to retrieve the media types.</span></span>

## <a name="requirements"></a><span data-ttu-id="78d3f-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="78d3f-135">Requirements</span></span>



| <span data-ttu-id="78d3f-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="78d3f-136">Requirement</span></span> | <span data-ttu-id="78d3f-137">Valore</span><span class="sxs-lookup"><span data-stu-id="78d3f-137">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78d3f-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="78d3f-138">Header</span></span><br/>  | <dl> <span data-ttu-id="78d3f-139"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="78d3f-139"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="78d3f-140">Libreria</span><span class="sxs-lookup"><span data-stu-id="78d3f-140">Library</span></span><br/> | <dl> <span data-ttu-id="78d3f-141"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="78d3f-141"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78d3f-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="78d3f-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78d3f-143">**Classe CEnumMediaTypes**</span><span class="sxs-lookup"><span data-stu-id="78d3f-143">**CEnumMediaTypes Class**</span></span>](cenummediatypes.md)
</dt> </dl>

 

 




