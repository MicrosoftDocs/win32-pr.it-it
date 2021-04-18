---
description: "Il metodo FindPin ottiene il pin con l'identificatore specificato. Questo metodo implementa il metodo IBaseFilter:: FindPin."
ms.assetid: 56ee3e0d-9e3f-4d25-846b-50119b55a122
title: Metodo CTransformFilter. FindPin (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.FindPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1631651932d5adbc49fb59d44291dccea55fd41f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328337"
---
# <a name="ctransformfilterfindpin-method"></a><span data-ttu-id="c45dc-104">CTransformFilter. FindPin, metodo</span><span class="sxs-lookup"><span data-stu-id="c45dc-104">CTransformFilter.FindPin method</span></span>

<span data-ttu-id="c45dc-105">Il metodo **FindPin** ottiene il pin con l'identificatore specificato.</span><span class="sxs-lookup"><span data-stu-id="c45dc-105">The **FindPin** method gets the pin with the specified identifier.</span></span> <span data-ttu-id="c45dc-106">Questo metodo implementa il metodo [**IBaseFilter:: FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin) .</span><span class="sxs-lookup"><span data-stu-id="c45dc-106">This method implements the [**IBaseFilter::FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c45dc-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c45dc-107">Syntax</span></span>


```C++
HRESULT FindPin(
   LPCWSTR Id,
   IPin    **ppPin
);
```



## <a name="parameters"></a><span data-ttu-id="c45dc-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="c45dc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c45dc-109">*Id*</span><span class="sxs-lookup"><span data-stu-id="c45dc-109">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="c45dc-110">Stringa di caratteri wide che contiene l'identificatore del PIN.</span><span class="sxs-lookup"><span data-stu-id="c45dc-110">Wide-character string that contains the pin identifier.</span></span>

</dd> <dt>

<span data-ttu-id="c45dc-111">*ppPin*</span><span class="sxs-lookup"><span data-stu-id="c45dc-111">*ppPin*</span></span> 
</dt> <dd>

<span data-ttu-id="c45dc-112">Riceve un puntatore all'interfaccia [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del PIN.</span><span class="sxs-lookup"><span data-stu-id="c45dc-112">Receives a pointer to the pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span> <span data-ttu-id="c45dc-113">Se il metodo ha esito negativo, `*ppPin` viene impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="c45dc-113">If the method fails, `*ppPin` is set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c45dc-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c45dc-114">Return value</span></span>

<span data-ttu-id="c45dc-115">Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="c45dc-115">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="c45dc-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="c45dc-116">Return code</span></span>                                                                                       | <span data-ttu-id="c45dc-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c45dc-117">Description</span></span>                                           |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <span data-ttu-id="c45dc-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c45dc-118"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="c45dc-119">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="c45dc-119">Success.</span></span><br/>                                   |
| <dl> <span data-ttu-id="c45dc-120"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="c45dc-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>     | <span data-ttu-id="c45dc-121">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="c45dc-121">Insufficient memory.</span></span><br/>                       |
| <dl> <span data-ttu-id="c45dc-122"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="c45dc-122"><dt>**E\_POINTER**</dt></span></span> </dl>         | <span data-ttu-id="c45dc-123">Argomento puntatore **null** .</span><span class="sxs-lookup"><span data-stu-id="c45dc-123">**NULL** pointer argument.</span></span><br/>                 |
| <dl> <span data-ttu-id="c45dc-124"><dt>**VFW \_ E \_ non \_ trovato**</dt></span><span class="sxs-lookup"><span data-stu-id="c45dc-124"><dt>**VFW\_E\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="c45dc-125">Non è stato possibile trovare un pin con questo identificatore.</span><span class="sxs-lookup"><span data-stu-id="c45dc-125">Could not find a pin with this identifier.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c45dc-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="c45dc-126">Remarks</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c45dc-127">L'implementazione di questo metodo non chiama [**Ipin:: QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) per trovare la corrispondenza con l'identificatore del PIN.</span><span class="sxs-lookup"><span data-stu-id="c45dc-127">The implementation of this method does not call [**IPin::QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) to match the pin identifier.</span></span> <span data-ttu-id="c45dc-128">Al contrario, il metodo presuppone che il pin di input sia denominato "in" e che il pin di output sia denominato "out".</span><span class="sxs-lookup"><span data-stu-id="c45dc-128">Instead, the method assumes that the input pin is named "In", and the output pin is named "Out".</span></span> <span data-ttu-id="c45dc-129">Se si usa un set di identificatori di PIN diverso, eseguire l'override di questo metodo.</span><span class="sxs-lookup"><span data-stu-id="c45dc-129">If you use a different set of pin identifiers, override this method.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c45dc-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c45dc-130">Requirements</span></span>



| <span data-ttu-id="c45dc-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="c45dc-131">Requirement</span></span> | <span data-ttu-id="c45dc-132">Valore</span><span class="sxs-lookup"><span data-stu-id="c45dc-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c45dc-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c45dc-133">Header</span></span><br/>  | <dl> <span data-ttu-id="c45dc-134"><dt>Transfrm. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c45dc-134"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c45dc-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="c45dc-135">Library</span></span><br/> | <dl> <span data-ttu-id="c45dc-136"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="c45dc-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c45dc-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c45dc-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c45dc-138">**Classe CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="c45dc-138">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




