---
description: "Il metodo FindPin Recupera il pin con l'identificatore specificato. Questo metodo implementa il metodo IBaseFilter:: FindPin."
ms.assetid: 152e4ff3-2809-4c57-b9c8-f51fc50b3703
title: Metodo CBaseFilter. FindPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.FindPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 98b49c547ec59a74185f7f719da660220de8480f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330413"
---
# <a name="cbasefilterfindpin-method"></a><span data-ttu-id="d7622-104">CBaseFilter. FindPin, metodo</span><span class="sxs-lookup"><span data-stu-id="d7622-104">CBaseFilter.FindPin method</span></span>

<span data-ttu-id="d7622-105">Il `FindPin` metodo recupera il pin con l'identificatore specificato.</span><span class="sxs-lookup"><span data-stu-id="d7622-105">The `FindPin` method retrieves the pin with the specified identifier.</span></span> <span data-ttu-id="d7622-106">Questo metodo implementa il metodo [**IBaseFilter:: FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin) .</span><span class="sxs-lookup"><span data-stu-id="d7622-106">This method implements the [**IBaseFilter::FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7622-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d7622-107">Syntax</span></span>


```C++
HRESULT FindPin(
   LPCWSTR Id,
   IPin    **ppPin
);
```



## <a name="parameters"></a><span data-ttu-id="d7622-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d7622-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7622-109">*Id*</span><span class="sxs-lookup"><span data-stu-id="d7622-109">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="d7622-110">Puntatore a una stringa Unicode costante a terminazione null che identifica il PIN.</span><span class="sxs-lookup"><span data-stu-id="d7622-110">Pointer to a constant, null-terminated Unicode string that identifies the pin.</span></span>

</dd> <dt>

<span data-ttu-id="d7622-111">*ppPin*</span><span class="sxs-lookup"><span data-stu-id="d7622-111">*ppPin*</span></span> 
</dt> <dd>

<span data-ttu-id="d7622-112">Indirizzo di una variabile che riceve un puntatore all'interfaccia [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del PIN.</span><span class="sxs-lookup"><span data-stu-id="d7622-112">Address of a variable that receives a pointer to the pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7622-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d7622-113">Return value</span></span>

<span data-ttu-id="d7622-114">Restituisce uno dei seguenti valori **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d7622-114">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="d7622-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="d7622-115">Return code</span></span>                                                                                       | <span data-ttu-id="d7622-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d7622-116">Description</span></span>                               |
|---------------------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="d7622-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d7622-117"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="d7622-118">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="d7622-118">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="d7622-119"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="d7622-119"><dt>**E\_POINTER**</dt></span></span> </dl>         | <span data-ttu-id="d7622-120">Argomento puntatore **null** .</span><span class="sxs-lookup"><span data-stu-id="d7622-120">**NULL** pointer argument.</span></span><br/>     |
| <dl> <span data-ttu-id="d7622-121"><dt>**VFW \_ E \_ non \_ trovato**</dt></span><span class="sxs-lookup"><span data-stu-id="d7622-121"><dt>**VFW\_E\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="d7622-122">Impossibile trovare un pin corrispondente.</span><span class="sxs-lookup"><span data-stu-id="d7622-122">Could not find a matching pin.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d7622-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="d7622-123">Remarks</span></span>

<span data-ttu-id="d7622-124">Questo metodo chiama il metodo [**CBasePin:: Name**](cbasepin-name.md) per confrontare il nome di ogni pin con la stringa specificata dal parametro *ID* .</span><span class="sxs-lookup"><span data-stu-id="d7622-124">This method calls the [**CBasePin::Name**](cbasepin-name.md) method to compare each pin's name against the string specified by the *Id* parameter.</span></span>

<span data-ttu-id="d7622-125">Se il metodo ha esito positivo, l'interfaccia **Ipin** ha un conteggio dei riferimenti in attesa.</span><span class="sxs-lookup"><span data-stu-id="d7622-125">If the method succeeds, the **IPin** interface has an outstanding reference count.</span></span> <span data-ttu-id="d7622-126">Assicurarsi di rilasciarlo al termine dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="d7622-126">Be sure to release it when you are done.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7622-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d7622-127">Requirements</span></span>



| <span data-ttu-id="d7622-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7622-128">Requirement</span></span> | <span data-ttu-id="d7622-129">Valore</span><span class="sxs-lookup"><span data-stu-id="d7622-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7622-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d7622-130">Header</span></span><br/>  | <dl> <span data-ttu-id="d7622-131"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d7622-131"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d7622-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="d7622-132">Library</span></span><br/> | <dl> <span data-ttu-id="d7622-133"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d7622-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7622-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d7622-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7622-135">**Classe CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="d7622-135">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




