---
description: 'Il metodo EnumMediaTypes enumera i tipi di supporto preferiti del PIN. Questo metodo implementa il metodo IPin:: EnumMediaTypes.'
ms.assetid: 942c6594-3053-484a-a0f7-286dcd3f7550
title: Metodo CTransInPlaceOutputPin. EnumMediaTypes (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin.EnumMediaTypes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4d214004412264272c64d0efaf20a5da7e1ca3cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326178"
---
# <a name="ctransinplaceoutputpinenummediatypes-method"></a><span data-ttu-id="cb266-104">CTransInPlaceOutputPin. EnumMediaTypes, metodo</span><span class="sxs-lookup"><span data-stu-id="cb266-104">CTransInPlaceOutputPin.EnumMediaTypes method</span></span>

<span data-ttu-id="cb266-105">Il `EnumMediaTypes` metodo enumera i tipi di supporto preferiti del PIN.</span><span class="sxs-lookup"><span data-stu-id="cb266-105">The `EnumMediaTypes` method enumerates the pin's preferred media types.</span></span> <span data-ttu-id="cb266-106">Questo metodo implementa il metodo [**Ipin:: EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) .</span><span class="sxs-lookup"><span data-stu-id="cb266-106">This method implements the [**IPin::EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb266-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cb266-107">Syntax</span></span>


```C++
HRESULT EnumMediaTypes(
   IEnumMediaTypes **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="cb266-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="cb266-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb266-109">*ppEnum*</span><span class="sxs-lookup"><span data-stu-id="cb266-109">*ppEnum*</span></span> 
</dt> <dd>

<span data-ttu-id="cb266-110">Riceve un puntatore all'interfaccia [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) .</span><span class="sxs-lookup"><span data-stu-id="cb266-110">Receives a pointer to the [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb266-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cb266-111">Return value</span></span>

<span data-ttu-id="cb266-112">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cb266-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="cb266-113">I valori possibili includono quelli mostrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="cb266-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="cb266-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="cb266-114">Return code</span></span>                                                                                           | <span data-ttu-id="cb266-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cb266-115">Description</span></span>                                         |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="cb266-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="cb266-116"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="cb266-117">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="cb266-117">Success.</span></span><br/>                                 |
| <dl> <span data-ttu-id="cb266-118"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="cb266-118"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>         | <span data-ttu-id="cb266-119">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="cb266-119">Insufficient memory.</span></span><br/>                     |
| <dl> <span data-ttu-id="cb266-120"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="cb266-120"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="cb266-121">Puntatore **null** .</span><span class="sxs-lookup"><span data-stu-id="cb266-121">**NULL** pointer.</span></span><br/>                        |
| <dl> <span data-ttu-id="cb266-122"><dt>**VFW \_ E \_ non \_ connesso**</dt></span><span class="sxs-lookup"><span data-stu-id="cb266-122"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="cb266-123">Il pin di input del filtro non è connesso.</span><span class="sxs-lookup"><span data-stu-id="cb266-123">The filter's input pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="cb266-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="cb266-124">Remarks</span></span>

<span data-ttu-id="cb266-125">Questo metodo restituisce l'interfaccia **IEnumMediaTypes** dal pin di output a Monte.</span><span class="sxs-lookup"><span data-stu-id="cb266-125">This method returns the **IEnumMediaTypes** interface from the upstream output pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb266-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cb266-126">Requirements</span></span>



| <span data-ttu-id="cb266-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb266-127">Requirement</span></span> | <span data-ttu-id="cb266-128">Valore</span><span class="sxs-lookup"><span data-stu-id="cb266-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb266-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cb266-129">Header</span></span><br/>  | <dl> <span data-ttu-id="cb266-130"><dt>Transip. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cb266-130"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="cb266-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="cb266-131">Library</span></span><br/> | <dl> <span data-ttu-id="cb266-132"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="cb266-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb266-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cb266-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb266-134">**Classe CTransInPlaceOutputPin**</span><span class="sxs-lookup"><span data-stu-id="cb266-134">**CTransInPlaceOutputPin Class**</span></span>](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




