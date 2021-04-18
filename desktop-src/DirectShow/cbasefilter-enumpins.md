---
description: 'Il metodo EnumPins enumera i pin in questo filtro. Questo metodo implementa il metodo IBaseFilter:: EnumPins.'
ms.assetid: c1015ed3-658f-4f96-a1fb-e04b81a9ddb5
title: Metodo CBaseFilter. EnumPins (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.EnumPins
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 66a0f88a9749ba1dabb982e2f275da8a4be2a422
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330415"
---
# <a name="cbasefilterenumpins-method"></a><span data-ttu-id="a9244-104">CBaseFilter. EnumPins, metodo</span><span class="sxs-lookup"><span data-stu-id="a9244-104">CBaseFilter.EnumPins method</span></span>

<span data-ttu-id="a9244-105">Il `EnumPins` metodo enumera i pin in questo filtro.</span><span class="sxs-lookup"><span data-stu-id="a9244-105">The `EnumPins` method enumerates the pins on this filter.</span></span> <span data-ttu-id="a9244-106">Questo metodo implementa il metodo [**IBaseFilter:: EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) .</span><span class="sxs-lookup"><span data-stu-id="a9244-106">This method implements the [**IBaseFilter::EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9244-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a9244-107">Syntax</span></span>


```C++
HRESULT EnumPins(
   IEnumPins **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="a9244-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a9244-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9244-109">*ppEnum*</span><span class="sxs-lookup"><span data-stu-id="a9244-109">*ppEnum*</span></span> 
</dt> <dd>

<span data-ttu-id="a9244-110">Indirizzo di una variabile che riceve un puntatore all'interfaccia [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) .</span><span class="sxs-lookup"><span data-stu-id="a9244-110">Address of a variable that receives a pointer to the [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9244-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a9244-111">Return value</span></span>

<span data-ttu-id="a9244-112">Restituisce uno dei seguenti valori **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a9244-112">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="a9244-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="a9244-113">Return code</span></span>                                                                                   | <span data-ttu-id="a9244-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a9244-114">Description</span></span>                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="a9244-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a9244-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="a9244-116">Operazione riuscita</span><span class="sxs-lookup"><span data-stu-id="a9244-116">Success</span></span><br/>                   |
| <dl> <span data-ttu-id="a9244-117"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="a9244-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="a9244-118">Memoria insufficiente</span><span class="sxs-lookup"><span data-stu-id="a9244-118">Insufficient memory</span></span><br/>       |
| <dl> <span data-ttu-id="a9244-119"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="a9244-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="a9244-120">Argomento puntatore **null**</span><span class="sxs-lookup"><span data-stu-id="a9244-120">**NULL** pointer argument</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a9244-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="a9244-121">Remarks</span></span>

<span data-ttu-id="a9244-122">Questo metodo crea un'istanza della classe di base [**CEnumPins**](cenumpins.md) e restituisce un puntatore a tale oggetto, di tipo **IEnumPins**.</span><span class="sxs-lookup"><span data-stu-id="a9244-122">This method creates an instance of the [**CEnumPins**](cenumpins.md) base class, and returns a pointer to that object, of type **IEnumPins**.</span></span> <span data-ttu-id="a9244-123">La classe **CEnumPins** chiama il metodo [**CBaseFilter:: GetPin**](cbasefilter-getpin.md) del filtro per enumerare i pin sul filtro.</span><span class="sxs-lookup"><span data-stu-id="a9244-123">The **CEnumPins** class calls the filter's [**CBaseFilter::GetPin**](cbasefilter-getpin.md) method to enumerate the pins on the filter.</span></span>

<span data-ttu-id="a9244-124">Se questo metodo ha esito positivo, l'interfaccia **IEnumPins** ha un conteggio dei riferimenti in attesa.</span><span class="sxs-lookup"><span data-stu-id="a9244-124">If this method succeeds, the **IEnumPins** interface has an outstanding reference count.</span></span> <span data-ttu-id="a9244-125">Il chiamante deve rilasciare l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="a9244-125">The caller must release the interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9244-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a9244-126">Requirements</span></span>



| <span data-ttu-id="a9244-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9244-127">Requirement</span></span> | <span data-ttu-id="a9244-128">Valore</span><span class="sxs-lookup"><span data-stu-id="a9244-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9244-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a9244-129">Header</span></span><br/>  | <dl> <span data-ttu-id="a9244-130"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a9244-130"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a9244-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="a9244-131">Library</span></span><br/> | <dl> <span data-ttu-id="a9244-132"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="a9244-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9244-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a9244-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9244-134">**Classe CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="a9244-134">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




