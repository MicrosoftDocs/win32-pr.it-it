---
description: 'Il metodo EnumMediaTypes enumera i tipi di supporto preferiti del PIN. Questo metodo implementa il metodo IPin:: EnumMediaTypes.'
ms.assetid: 0360f9fc-6876-4a54-8de1-bf289e0e10ae
title: Metodo CBasePin. EnumMediaTypes (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.EnumMediaTypes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 54aaddbbcde26791b6c55665bfbbb7ff62048238
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328848"
---
# <a name="cbasepinenummediatypes-method"></a><span data-ttu-id="f0513-104">CBasePin. EnumMediaTypes, metodo</span><span class="sxs-lookup"><span data-stu-id="f0513-104">CBasePin.EnumMediaTypes method</span></span>

<span data-ttu-id="f0513-105">Il `EnumMediaTypes` metodo enumera i tipi di supporto preferiti del PIN.</span><span class="sxs-lookup"><span data-stu-id="f0513-105">The `EnumMediaTypes` method enumerates the pin's preferred media types.</span></span> <span data-ttu-id="f0513-106">Questo metodo implementa il metodo [**Ipin:: EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) .</span><span class="sxs-lookup"><span data-stu-id="f0513-106">This method implements the [**IPin::EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0513-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f0513-107">Syntax</span></span>


```C++
HRESULT EnumMediaTypes(
   IEnumMediaTypes **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="f0513-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="f0513-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0513-109">*ppEnum*</span><span class="sxs-lookup"><span data-stu-id="f0513-109">*ppEnum*</span></span> 
</dt> <dd>

<span data-ttu-id="f0513-110">Indirizzo di una variabile che riceve un puntatore all'interfaccia [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) .</span><span class="sxs-lookup"><span data-stu-id="f0513-110">Address of a variable that receives a pointer to the [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0513-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f0513-111">Return value</span></span>

<span data-ttu-id="f0513-112">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f0513-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="f0513-113">I valori possibili includono quelli nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="f0513-113">Possible values include those in the following table.</span></span>



| <span data-ttu-id="f0513-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="f0513-114">Return code</span></span>                                                                                   | <span data-ttu-id="f0513-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f0513-115">Description</span></span>                           |
|-----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="f0513-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f0513-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="f0513-117">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="f0513-117">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="f0513-118"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="f0513-118"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="f0513-119">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="f0513-119">Insufficient memory.</span></span><br/>       |
| <dl> <span data-ttu-id="f0513-120"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="f0513-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="f0513-121">Argomento puntatore **null** .</span><span class="sxs-lookup"><span data-stu-id="f0513-121">**NULL** pointer argument.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f0513-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="f0513-122">Remarks</span></span>

<span data-ttu-id="f0513-123">I pin di input non sono necessari per enumerare i tipi preferiti.</span><span class="sxs-lookup"><span data-stu-id="f0513-123">Input pins are not required to enumerate any preferred types.</span></span> <span data-ttu-id="f0513-124">I pin di output devono enumerare almeno un tipo preferito.</span><span class="sxs-lookup"><span data-stu-id="f0513-124">Output pins must enumerate at least one preferred type.</span></span> <span data-ttu-id="f0513-125">In caso contrario, entrambi i pin potrebbero non avere un tipo preferito, rendendo impossibile la connessione.</span><span class="sxs-lookup"><span data-stu-id="f0513-125">Otherwise, both pins could lack a preferred type, making a connection impossible.</span></span>

<span data-ttu-id="f0513-126">L'interfaccia **IEnumMediaTypes** funziona come un enumeratore COM standard.</span><span class="sxs-lookup"><span data-stu-id="f0513-126">The **IEnumMediaTypes** interface works like a standard COM enumerator.</span></span> <span data-ttu-id="f0513-127">Per altre informazioni, vedere [enumerazione di oggetti in un grafico a filtro](enumerating-objects-in-a-filter-graph.md).</span><span class="sxs-lookup"><span data-stu-id="f0513-127">For more information, see [Enumerating Objects in a Filter Graph](enumerating-objects-in-a-filter-graph.md).</span></span> <span data-ttu-id="f0513-128">Se il metodo ha esito positivo, l'interfaccia **IEnumMediaTypes** ha un conteggio dei riferimenti in attesa.</span><span class="sxs-lookup"><span data-stu-id="f0513-128">If the method succeeds, the **IEnumMediaTypes** interface has an outstanding reference count.</span></span> <span data-ttu-id="f0513-129">Assicurarsi di rilasciarlo al termine dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="f0513-129">Be sure to release it when you are done.</span></span>

<span data-ttu-id="f0513-130">La classe base [**CEnumMediaTypes**](cenummediatypes.md) implementa **IEnumMediaTypes**.</span><span class="sxs-lookup"><span data-stu-id="f0513-130">The [**CEnumMediaTypes**](cenummediatypes.md) base class implements **IEnumMediaTypes**.</span></span> <span data-ttu-id="f0513-131">Chiama il metodo [**CBasePin:: GetMediaType**](cbasepin-getmediatype.md) del PIN per enumerare i tipi di supporto.</span><span class="sxs-lookup"><span data-stu-id="f0513-131">It calls the pin's [**CBasePin::GetMediaType**](cbasepin-getmediatype.md) method to enumerate the media types.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0513-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f0513-132">Requirements</span></span>



| <span data-ttu-id="f0513-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0513-133">Requirement</span></span> | <span data-ttu-id="f0513-134">Valore</span><span class="sxs-lookup"><span data-stu-id="f0513-134">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0513-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f0513-135">Header</span></span><br/>  | <dl> <span data-ttu-id="f0513-136"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f0513-136"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f0513-137">Libreria</span><span class="sxs-lookup"><span data-stu-id="f0513-137">Library</span></span><br/> | <dl> <span data-ttu-id="f0513-138"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f0513-138"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0513-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f0513-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0513-140">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="f0513-140">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




