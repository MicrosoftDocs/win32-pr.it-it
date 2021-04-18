---
description: "Il metodo FindPin Recupera il pin con l'identificatore specificato. Questo metodo implementa il metodo IBaseFilter:: FindPin."
ms.assetid: ad593dbf-ca56-4409-ac6e-1b88908c8cee
title: Metodo CSource. FindPin (source. h)
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
ms.openlocfilehash: 9fac8df1e53e4a129b42d1284a19392bc7b58aa2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324651"
---
# <a name="csourcefindpin-method"></a><span data-ttu-id="63c00-104">CSource. FindPin, metodo</span><span class="sxs-lookup"><span data-stu-id="63c00-104">CSource.FindPin method</span></span>

<span data-ttu-id="63c00-105">Il `FindPin` metodo recupera il pin con l'identificatore specificato.</span><span class="sxs-lookup"><span data-stu-id="63c00-105">The `FindPin` method retrieves the pin with the specified identifier.</span></span> <span data-ttu-id="63c00-106">Questo metodo implementa il metodo [**IBaseFilter:: FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin) .</span><span class="sxs-lookup"><span data-stu-id="63c00-106">This method implements the [**IBaseFilter::FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="63c00-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="63c00-107">Syntax</span></span>


```C++
HRESULT FindPin(
   LPCWSTR Id,
   IPin    **ppPin
);
```



## <a name="parameters"></a><span data-ttu-id="63c00-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="63c00-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63c00-109">*Id*</span><span class="sxs-lookup"><span data-stu-id="63c00-109">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="63c00-110">Puntatore a una stringa con terminazione null che identifica il PIN.</span><span class="sxs-lookup"><span data-stu-id="63c00-110">Pointer to a null-terminated string that identifies the pin.</span></span>

</dd> <dt>

<span data-ttu-id="63c00-111">*ppPin*</span><span class="sxs-lookup"><span data-stu-id="63c00-111">*ppPin*</span></span> 
</dt> <dd>

<span data-ttu-id="63c00-112">Riceve un puntatore all'interfaccia [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del PIN.</span><span class="sxs-lookup"><span data-stu-id="63c00-112">Receives a pointer to the pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span> <span data-ttu-id="63c00-113">Se il metodo ha esito negativo, \* *ppPin* è impostato su **null**</span><span class="sxs-lookup"><span data-stu-id="63c00-113">If the method fails, \**ppPin* is set to **NULL**</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63c00-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="63c00-114">Return value</span></span>

<span data-ttu-id="63c00-115">Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="63c00-115">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="63c00-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="63c00-116">Return code</span></span>                                                                                       | <span data-ttu-id="63c00-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="63c00-117">Description</span></span>                                           |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <span data-ttu-id="63c00-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="63c00-118"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="63c00-119">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="63c00-119">Success.</span></span><br/>                                   |
| <dl> <span data-ttu-id="63c00-120"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="63c00-120"><dt>**E\_POINTER**</dt></span></span> </dl>         | <span data-ttu-id="63c00-121">Argomento puntatore **null** .</span><span class="sxs-lookup"><span data-stu-id="63c00-121">**NULL** pointer argument.</span></span><br/>                 |
| <dl> <span data-ttu-id="63c00-122"><dt>**VFW \_ E \_ non \_ trovato**</dt></span><span class="sxs-lookup"><span data-stu-id="63c00-122"><dt>**VFW\_E\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="63c00-123">Non è stato possibile trovare un pin con questo identificatore.</span><span class="sxs-lookup"><span data-stu-id="63c00-123">Could not find a pin with this identifier.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="63c00-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="63c00-124">Remarks</span></span>

<span data-ttu-id="63c00-125">Il primo pin è sempre denominato "1"; il secondo pin è denominato "2"; e così via.</span><span class="sxs-lookup"><span data-stu-id="63c00-125">The first pin is always named "1"; the second pin is named "2"; and so forth.</span></span> <span data-ttu-id="63c00-126">Per ulteriori informazioni, vedere [**CSourceStream:: QueryId**](csourcestream-queryid.md).</span><span class="sxs-lookup"><span data-stu-id="63c00-126">For more information, see [**CSourceStream::QueryId**](csourcestream-queryid.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="63c00-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="63c00-127">Requirements</span></span>



| <span data-ttu-id="63c00-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="63c00-128">Requirement</span></span> | <span data-ttu-id="63c00-129">Valore</span><span class="sxs-lookup"><span data-stu-id="63c00-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63c00-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="63c00-130">Header</span></span><br/>  | <dl> <span data-ttu-id="63c00-131"><dt>Source. h (Includi Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="63c00-131"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="63c00-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="63c00-132">Library</span></span><br/> | <dl> <span data-ttu-id="63c00-133"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="63c00-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63c00-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="63c00-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63c00-135">**Classe CSource**</span><span class="sxs-lookup"><span data-stu-id="63c00-135">**CSource Class**</span></span>](csource.md)
</dt> </dl>

 

 




