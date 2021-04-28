---
description: "Metodo CSource.FindPin: il metodo FindPin recupera il pin con l'identificatore specificato. Questo metodo implementa il metodo IBaseFilter::FindPin."
ms.assetid: ad593dbf-ca56-4409-ac6e-1b88908c8cee
title: Metodo CSource.FindPin (Source.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.FindPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: daa1e2404e7c6fbf1d879d71374298103bdc621f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098859"
---
# <a name="csourcefindpin-method"></a><span data-ttu-id="8f9a1-104">Metodo CSource.FindPin</span><span class="sxs-lookup"><span data-stu-id="8f9a1-104">CSource.FindPin method</span></span>

<span data-ttu-id="8f9a1-105">Il `FindPin` metodo recupera il pin con l'identificatore specificato.</span><span class="sxs-lookup"><span data-stu-id="8f9a1-105">The `FindPin` method retrieves the pin with the specified identifier.</span></span> <span data-ttu-id="8f9a1-106">Questo metodo implementa il [**metodo IBaseFilter::FindPin.**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin)</span><span class="sxs-lookup"><span data-stu-id="8f9a1-106">This method implements the [**IBaseFilter::FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f9a1-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8f9a1-107">Syntax</span></span>


```C++
HRESULT FindPin(
   LPCWSTR Id,
   IPin    **ppPin
);
```



## <a name="parameters"></a><span data-ttu-id="8f9a1-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="8f9a1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f9a1-109">*Id*</span><span class="sxs-lookup"><span data-stu-id="8f9a1-109">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="8f9a1-110">Puntatore a una stringa con terminazione Null che identifica il pin.</span><span class="sxs-lookup"><span data-stu-id="8f9a1-110">Pointer to a null-terminated string that identifies the pin.</span></span>

</dd> <dt>

<span data-ttu-id="8f9a1-111">*ppPin*</span><span class="sxs-lookup"><span data-stu-id="8f9a1-111">*ppPin*</span></span> 
</dt> <dd>

<span data-ttu-id="8f9a1-112">Riceve un puntatore all'interfaccia [**IPin del**](/windows/desktop/api/Strmif/nn-strmif-ipin) pin.</span><span class="sxs-lookup"><span data-stu-id="8f9a1-112">Receives a pointer to the pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span> <span data-ttu-id="8f9a1-113">Se il metodo ha esito negativo, \* *ppPin* è impostato su **NULL**</span><span class="sxs-lookup"><span data-stu-id="8f9a1-113">If the method fails, \**ppPin* is set to **NULL**</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f9a1-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8f9a1-114">Return value</span></span>

<span data-ttu-id="8f9a1-115">Restituisce uno dei **valori HRESULT** illustrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="8f9a1-115">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="8f9a1-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="8f9a1-116">Return code</span></span>                                                                                       | <span data-ttu-id="8f9a1-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8f9a1-117">Description</span></span>                                           |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <span data-ttu-id="8f9a1-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8f9a1-118"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="8f9a1-119">Operazione completata.</span><span class="sxs-lookup"><span data-stu-id="8f9a1-119">Success.</span></span><br/>                                   |
| <dl> <span data-ttu-id="8f9a1-120"><dt>**PUNTATORE E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8f9a1-120"><dt>**E\_POINTER**</dt></span></span> </dl>         | <span data-ttu-id="8f9a1-121">Argomento del puntatore **NULL.**</span><span class="sxs-lookup"><span data-stu-id="8f9a1-121">**NULL** pointer argument.</span></span><br/>                 |
| <dl> <span data-ttu-id="8f9a1-122"><dt>**VFW \_ E \_ NON \_ TROVATO**</dt></span><span class="sxs-lookup"><span data-stu-id="8f9a1-122"><dt>**VFW\_E\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="8f9a1-123">Impossibile trovare un pin con questo identificatore.</span><span class="sxs-lookup"><span data-stu-id="8f9a1-123">Could not find a pin with this identifier.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8f9a1-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="8f9a1-124">Remarks</span></span>

<span data-ttu-id="8f9a1-125">Il primo segnaposto è sempre denominato "1". il secondo pin è denominato "2"; e così via.</span><span class="sxs-lookup"><span data-stu-id="8f9a1-125">The first pin is always named "1"; the second pin is named "2"; and so forth.</span></span> <span data-ttu-id="8f9a1-126">Per altre informazioni, vedere [**CSourceStream::QueryId**](csourcestream-queryid.md).</span><span class="sxs-lookup"><span data-stu-id="8f9a1-126">For more information, see [**CSourceStream::QueryId**](csourcestream-queryid.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8f9a1-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8f9a1-127">Requirements</span></span>



| <span data-ttu-id="8f9a1-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f9a1-128">Requirement</span></span> | <span data-ttu-id="8f9a1-129">Valore</span><span class="sxs-lookup"><span data-stu-id="8f9a1-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f9a1-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8f9a1-130">Header</span></span><br/>  | <dl> <span data-ttu-id="8f9a1-131"><dt>Source.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="8f9a1-131"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="8f9a1-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="8f9a1-132">Library</span></span><br/> | <dl> <span data-ttu-id="8f9a1-133"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="8f9a1-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f9a1-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8f9a1-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f9a1-135">**Classe CSource**</span><span class="sxs-lookup"><span data-stu-id="8f9a1-135">**CSource Class**</span></span>](csource.md)
</dt> </dl>

 

 




