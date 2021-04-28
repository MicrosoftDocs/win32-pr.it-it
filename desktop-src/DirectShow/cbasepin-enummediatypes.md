---
description: 'Metodo CBasePin.EnumMediaTypes: il metodo EnumMediaTypes enumera i tipi di supporti preferiti del pin. Questo metodo implementa il metodo IPin::EnumMediaTypes.'
ms.assetid: 0360f9fc-6876-4a54-8de1-bf289e0e10ae
title: Metodo CBasePin.EnumMediaTypes (Amfilter.h)
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
ms.openlocfilehash: c68fe1ab83724149dcd2fb58a60e9c6950d887ca
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099389"
---
# <a name="cbasepinenummediatypes-method"></a><span data-ttu-id="0a0ac-104">Metodo CBasePin.EnumMediaTypes</span><span class="sxs-lookup"><span data-stu-id="0a0ac-104">CBasePin.EnumMediaTypes method</span></span>

<span data-ttu-id="0a0ac-105">Il `EnumMediaTypes` metodo enumera i tipi di supporti preferiti del pin.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-105">The `EnumMediaTypes` method enumerates the pin's preferred media types.</span></span> <span data-ttu-id="0a0ac-106">Questo metodo implementa il [**metodo IPin::EnumMediaTypes.**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes)</span><span class="sxs-lookup"><span data-stu-id="0a0ac-106">This method implements the [**IPin::EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a0ac-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0a0ac-107">Syntax</span></span>


```C++
HRESULT EnumMediaTypes(
   IEnumMediaTypes **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="0a0ac-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="0a0ac-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a0ac-109">*ppEnum*</span><span class="sxs-lookup"><span data-stu-id="0a0ac-109">*ppEnum*</span></span> 
</dt> <dd>

<span data-ttu-id="0a0ac-110">Indirizzo di una variabile che riceve un puntatore [**all'interfaccia IEnumMediaTypes.**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes)</span><span class="sxs-lookup"><span data-stu-id="0a0ac-110">Address of a variable that receives a pointer to the [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a0ac-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0a0ac-111">Return value</span></span>

<span data-ttu-id="0a0ac-112">Restituisce un **valore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="0a0ac-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="0a0ac-113">I valori possibili sono quelli riportati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-113">Possible values include those in the following table.</span></span>



| <span data-ttu-id="0a0ac-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="0a0ac-114">Return code</span></span>                                                                                   | <span data-ttu-id="0a0ac-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0a0ac-115">Description</span></span>                           |
|-----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="0a0ac-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0a0ac-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="0a0ac-117">Operazione completata.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-117">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="0a0ac-118"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="0a0ac-118"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="0a0ac-119">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-119">Insufficient memory.</span></span><br/>       |
| <dl> <span data-ttu-id="0a0ac-120"><dt>**PUNTATORE \_ E**</dt></span><span class="sxs-lookup"><span data-stu-id="0a0ac-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="0a0ac-121">Argomento del puntatore **NULL.**</span><span class="sxs-lookup"><span data-stu-id="0a0ac-121">**NULL** pointer argument.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0a0ac-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="0a0ac-122">Remarks</span></span>

<span data-ttu-id="0a0ac-123">I pin di input non sono necessari per enumerare i tipi preferiti.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-123">Input pins are not required to enumerate any preferred types.</span></span> <span data-ttu-id="0a0ac-124">I pin di output devono enumerare almeno un tipo preferito.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-124">Output pins must enumerate at least one preferred type.</span></span> <span data-ttu-id="0a0ac-125">In caso contrario, entrambi i pin potrebbero non avere un tipo preferito, rendendo impossibile una connessione.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-125">Otherwise, both pins could lack a preferred type, making a connection impossible.</span></span>

<span data-ttu-id="0a0ac-126">**L'interfaccia IEnumMediaTypes** funziona come un enumeratore COM standard.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-126">The **IEnumMediaTypes** interface works like a standard COM enumerator.</span></span> <span data-ttu-id="0a0ac-127">Per altre informazioni, vedere [Enumerazione di oggetti in un grafo di filtro.](enumerating-objects-in-a-filter-graph.md)</span><span class="sxs-lookup"><span data-stu-id="0a0ac-127">For more information, see [Enumerating Objects in a Filter Graph](enumerating-objects-in-a-filter-graph.md).</span></span> <span data-ttu-id="0a0ac-128">Se il metodo ha esito positivo, **l'interfaccia IEnumMediaTypes** ha un conteggio dei riferimenti in sospeso.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-128">If the method succeeds, the **IEnumMediaTypes** interface has an outstanding reference count.</span></span> <span data-ttu-id="0a0ac-129">Al termine, assicurarsi di rilasciarlo.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-129">Be sure to release it when you are done.</span></span>

<span data-ttu-id="0a0ac-130">La classe di base [**CEnumMediaTypes**](cenummediatypes.md) implementa **IEnumMediaTypes**.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-130">The [**CEnumMediaTypes**](cenummediatypes.md) base class implements **IEnumMediaTypes**.</span></span> <span data-ttu-id="0a0ac-131">Chiama il metodo [**CBasePin::GetMediaType**](cbasepin-getmediatype.md) del pin per enumerare i tipi di supporti.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-131">It calls the pin's [**CBasePin::GetMediaType**](cbasepin-getmediatype.md) method to enumerate the media types.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a0ac-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0a0ac-132">Requirements</span></span>



| <span data-ttu-id="0a0ac-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a0ac-133">Requirement</span></span> | <span data-ttu-id="0a0ac-134">Valore</span><span class="sxs-lookup"><span data-stu-id="0a0ac-134">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a0ac-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0a0ac-135">Header</span></span><br/>  | <dl> <span data-ttu-id="0a0ac-136"><dt>Amfilter.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="0a0ac-136"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="0a0ac-137">Libreria</span><span class="sxs-lookup"><span data-stu-id="0a0ac-137">Library</span></span><br/> | <dl> <span data-ttu-id="0a0ac-138"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="0a0ac-138"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a0ac-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0a0ac-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a0ac-140">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="0a0ac-140">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




