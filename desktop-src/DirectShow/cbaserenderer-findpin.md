---
description: Il metodo FindPin Recupera il pin con l'identificatore specificato.
ms.assetid: d07a298f-ddb0-44eb-85ca-81735875cdf3
title: Metodo CBaseRenderer. FindPin (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.FindPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d6e6789a91f34d95933ae7869e1588eeb14b6006
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329383"
---
# <a name="cbaserendererfindpin-method"></a><span data-ttu-id="f32f2-103">CBaseRenderer. FindPin, metodo</span><span class="sxs-lookup"><span data-stu-id="f32f2-103">CBaseRenderer.FindPin method</span></span>

<span data-ttu-id="f32f2-104">Il `FindPin` metodo recupera il pin con l'identificatore specificato.</span><span class="sxs-lookup"><span data-stu-id="f32f2-104">The `FindPin` method retrieves the pin with the specified identifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="f32f2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f32f2-105">Syntax</span></span>


```C++
HRESULT FindPin(
   LPCWSTR Id,
   IPin    **ppPin
);
```



## <a name="parameters"></a><span data-ttu-id="f32f2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f32f2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f32f2-107">*Id*</span><span class="sxs-lookup"><span data-stu-id="f32f2-107">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="f32f2-108">Puntatore a una stringa di caratteri wide a terminazione null che identifica il PIN.</span><span class="sxs-lookup"><span data-stu-id="f32f2-108">Pointer to a constant, null-terminated wide-character string that identifies the pin.</span></span> <span data-ttu-id="f32f2-109">Deve essere L "in".</span><span class="sxs-lookup"><span data-stu-id="f32f2-109">Must be L"In".</span></span>

</dd> <dt>

<span data-ttu-id="f32f2-110">*ppPin*</span><span class="sxs-lookup"><span data-stu-id="f32f2-110">*ppPin*</span></span> 
</dt> <dd>

<span data-ttu-id="f32f2-111">Indirizzo di una variabile che riceve un puntatore all'interfaccia [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del PIN.</span><span class="sxs-lookup"><span data-stu-id="f32f2-111">Address of a variable that receives a pointer to the pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span> <span data-ttu-id="f32f2-112">Se il metodo ha esito negativo, *\* ppPin* è impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="f32f2-112">If the method fails, *\*ppPin* is set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f32f2-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f32f2-113">Return value</span></span>

<span data-ttu-id="f32f2-114">Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="f32f2-114">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="f32f2-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="f32f2-115">Return code</span></span>                                                                                       | <span data-ttu-id="f32f2-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f32f2-116">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="f32f2-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f32f2-117"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="f32f2-118">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="f32f2-118">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="f32f2-119"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="f32f2-119"><dt>**E\_POINTER**</dt></span></span> </dl>         | <span data-ttu-id="f32f2-120">Argomento puntatore **null** .</span><span class="sxs-lookup"><span data-stu-id="f32f2-120">**NULL** pointer argument.</span></span><br/> |
| <dl> <span data-ttu-id="f32f2-121"><dt>**VFW \_ E \_ non \_ trovato**</dt></span><span class="sxs-lookup"><span data-stu-id="f32f2-121"><dt>**VFW\_E\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="f32f2-122">Non trovato.</span><span class="sxs-lookup"><span data-stu-id="f32f2-122">Not found.</span></span><br/>                 |



 

## <a name="remarks"></a><span data-ttu-id="f32f2-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="f32f2-123">Remarks</span></span>

<span data-ttu-id="f32f2-124">Questo metodo esegue l'override del metodo [**CBaseFilter:: FindPin**](cbasefilter-findpin.md) .</span><span class="sxs-lookup"><span data-stu-id="f32f2-124">This method overrides the [**CBaseFilter::FindPin**](cbasefilter-findpin.md) method.</span></span> <span data-ttu-id="f32f2-125">Il solo pin del filtro (il pin di input) è denominato "in".</span><span class="sxs-lookup"><span data-stu-id="f32f2-125">The filter's only pin (the input pin) is named "In".</span></span>

## <a name="requirements"></a><span data-ttu-id="f32f2-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f32f2-126">Requirements</span></span>



| <span data-ttu-id="f32f2-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="f32f2-127">Requirement</span></span> | <span data-ttu-id="f32f2-128">Valore</span><span class="sxs-lookup"><span data-stu-id="f32f2-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f32f2-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f32f2-129">Header</span></span><br/>  | <dl> <span data-ttu-id="f32f2-130"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f32f2-130"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f32f2-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="f32f2-131">Library</span></span><br/> | <dl> <span data-ttu-id="f32f2-132"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f32f2-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f32f2-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f32f2-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f32f2-134">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="f32f2-134">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




