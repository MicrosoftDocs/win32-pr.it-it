---
description: 'Il metodo EnumMediaTypes enumera i tipi di supporto preferiti del PIN. Questo metodo implementa il metodo IPin:: EnumMediaTypes.'
ms.assetid: 0c28b4b0-a45f-400f-a6d7-7668458f9642
title: Metodo CTransInPlaceInputPin. EnumMediaTypes (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.EnumMediaTypes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ffa634fa695eb0007b49fc1c36c730c7fbde361b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326201"
---
# <a name="ctransinplaceinputpinenummediatypes-method"></a><span data-ttu-id="5899a-104">CTransInPlaceInputPin. EnumMediaTypes, metodo</span><span class="sxs-lookup"><span data-stu-id="5899a-104">CTransInPlaceInputPin.EnumMediaTypes method</span></span>

<span data-ttu-id="5899a-105">Il `EnumMediaTypes` metodo enumera i tipi di supporto preferiti del PIN.</span><span class="sxs-lookup"><span data-stu-id="5899a-105">The `EnumMediaTypes` method enumerates the pin's preferred media types.</span></span> <span data-ttu-id="5899a-106">Questo metodo implementa il metodo [**Ipin:: EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) .</span><span class="sxs-lookup"><span data-stu-id="5899a-106">This method implements the [**IPin::EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5899a-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5899a-107">Syntax</span></span>


```C++
HRESULT EnumMediaTypes(
   IEnumMediaTypes **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="5899a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="5899a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5899a-109">*ppEnum*</span><span class="sxs-lookup"><span data-stu-id="5899a-109">*ppEnum*</span></span> 
</dt> <dd>

<span data-ttu-id="5899a-110">Riceve un puntatore all'interfaccia [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) .</span><span class="sxs-lookup"><span data-stu-id="5899a-110">Receives a pointer to the [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5899a-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5899a-111">Return value</span></span>

<span data-ttu-id="5899a-112">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5899a-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="5899a-113">I valori possibili includono quelli mostrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="5899a-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="5899a-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="5899a-114">Return code</span></span>                                                                                           | <span data-ttu-id="5899a-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5899a-115">Description</span></span>                                 |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="5899a-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5899a-116"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="5899a-117">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="5899a-117">Success.</span></span><br/>                         |
| <dl> <span data-ttu-id="5899a-118"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="5899a-118"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>         | <span data-ttu-id="5899a-119">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="5899a-119">Insufficient memory.</span></span><br/>             |
| <dl> <span data-ttu-id="5899a-120"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="5899a-120"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="5899a-121">Puntatore **null** .</span><span class="sxs-lookup"><span data-stu-id="5899a-121">**NULL** pointer.</span></span><br/>                |
| <dl> <span data-ttu-id="5899a-122"><dt>**VFW \_ E \_ non \_ connesso**</dt></span><span class="sxs-lookup"><span data-stu-id="5899a-122"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="5899a-123">Il pin di output non è connesso.</span><span class="sxs-lookup"><span data-stu-id="5899a-123">The output pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5899a-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="5899a-124">Remarks</span></span>

<span data-ttu-id="5899a-125">Questo metodo restituisce l'interfaccia **IEnumMediaTypes** dal pin di input downstream.</span><span class="sxs-lookup"><span data-stu-id="5899a-125">This method returns the **IEnumMediaTypes** interface from downstream input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="5899a-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5899a-126">Requirements</span></span>



| <span data-ttu-id="5899a-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="5899a-127">Requirement</span></span> | <span data-ttu-id="5899a-128">Valore</span><span class="sxs-lookup"><span data-stu-id="5899a-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5899a-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5899a-129">Header</span></span><br/>  | <dl> <span data-ttu-id="5899a-130"><dt>Transip. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5899a-130"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5899a-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="5899a-131">Library</span></span><br/> | <dl> <span data-ttu-id="5899a-132"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="5899a-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5899a-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5899a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5899a-134">**Classe CTransInPlaceInputPin**</span><span class="sxs-lookup"><span data-stu-id="5899a-134">**CTransInPlaceInputPin Class**</span></span>](ctransinplaceinputpin.md)
</dt> </dl>

 

 




