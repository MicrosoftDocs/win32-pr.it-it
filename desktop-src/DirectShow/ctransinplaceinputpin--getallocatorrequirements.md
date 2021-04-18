---
description: "Il metodo GetAllocatorRequirements recupera le proprietà dell'allocatore richieste dal pin. Questo metodo implementa il metodo IMemInputPin:: GetAllocatorRequirements."
ms.assetid: 1355facc-f863-44b2-9284-8f06f62d39a2
title: Metodo CTransInPlaceInputPin. GetAllocatorRequirements (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.GetAllocatorRequirements
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dfa176cd5da0317821996593e19bb90396e82224
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330835"
---
# <a name="ctransinplaceinputpingetallocatorrequirements-method"></a><span data-ttu-id="021b5-104">CTransInPlaceInputPin. GetAllocatorRequirements, metodo</span><span class="sxs-lookup"><span data-stu-id="021b5-104">CTransInPlaceInputPin.GetAllocatorRequirements method</span></span>

<span data-ttu-id="021b5-105">Il `GetAllocatorRequirements` metodo recupera le proprietà dell'allocatore richieste dal pin.</span><span class="sxs-lookup"><span data-stu-id="021b5-105">The `GetAllocatorRequirements` method retrieves the allocator properties requested by the pin.</span></span> <span data-ttu-id="021b5-106">Questo metodo implementa il metodo [**IMemInputPin:: GetAllocatorRequirements**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements) .</span><span class="sxs-lookup"><span data-stu-id="021b5-106">This method implements the [**IMemInputPin::GetAllocatorRequirements**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="021b5-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="021b5-107">Syntax</span></span>


```C++
HRESULT GetAllocatorRequirements(
   ALLOCATOR_PROPERTIES *pProps
);
```



## <a name="parameters"></a><span data-ttu-id="021b5-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="021b5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="021b5-109">*pProps*</span><span class="sxs-lookup"><span data-stu-id="021b5-109">*pProps*</span></span> 
</dt> <dd>

<span data-ttu-id="021b5-110">Puntatore a una struttura di [**\_ proprietà dell'allocatore**](/windows/win32/api/strmif/ns-strmif-allocator_properties) , compilata con i requisiti.</span><span class="sxs-lookup"><span data-stu-id="021b5-110">Pointer to an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure, which is filled in with the requirements.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="021b5-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="021b5-111">Return value</span></span>

<span data-ttu-id="021b5-112">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="021b5-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="021b5-113">I valori possibili includono quelli mostrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="021b5-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="021b5-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="021b5-114">Return code</span></span>                                                                               | <span data-ttu-id="021b5-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="021b5-115">Description</span></span>                                                                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="021b5-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="021b5-116"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="021b5-117">Operazione riuscita</span><span class="sxs-lookup"><span data-stu-id="021b5-117">Success</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="021b5-118"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="021b5-118"><dt>**E\_NOTIMPL**</dt></span></span> </dl> | <span data-ttu-id="021b5-119">Il pin di output non è connesso oppure il pin di input downstream non supporta il metodo.</span><span class="sxs-lookup"><span data-stu-id="021b5-119">The output pin is not connected, or the downstream input pin does not support the method.</span></span><br/> |
| <dl> <span data-ttu-id="021b5-120"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="021b5-120"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="021b5-121">Argomento puntatore **null**</span><span class="sxs-lookup"><span data-stu-id="021b5-121">**NULL** pointer argument</span></span><br/>                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="021b5-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="021b5-122">Remarks</span></span>

<span data-ttu-id="021b5-123">Se il pin di output è connesso, questo metodo passa la chiamata al pin di input downstream.</span><span class="sxs-lookup"><span data-stu-id="021b5-123">If the output pin is connected, this method passes the call to the downstream input pin.</span></span> <span data-ttu-id="021b5-124">In caso contrario, restituisce E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="021b5-124">Otherwise, it returns E\_NOTIMPL.</span></span>

## <a name="requirements"></a><span data-ttu-id="021b5-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="021b5-125">Requirements</span></span>



| <span data-ttu-id="021b5-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="021b5-126">Requirement</span></span> | <span data-ttu-id="021b5-127">Valore</span><span class="sxs-lookup"><span data-stu-id="021b5-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="021b5-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="021b5-128">Header</span></span><br/>  | <dl> <span data-ttu-id="021b5-129"><dt>Transip. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="021b5-129"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="021b5-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="021b5-130">Library</span></span><br/> | <dl> <span data-ttu-id="021b5-131"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="021b5-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="021b5-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="021b5-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="021b5-133">**Classe CTransInPlaceInputPin**</span><span class="sxs-lookup"><span data-stu-id="021b5-133">**CTransInPlaceInputPin Class**</span></span>](ctransinplaceinputpin.md)
</dt> </dl>

 

 




