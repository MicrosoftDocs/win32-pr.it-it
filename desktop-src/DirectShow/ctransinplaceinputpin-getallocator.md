---
description: "Il metodo getallocator recupera l'allocatore di memoria proposto da questo pin. Questo metodo implementa il metodo IMemInputPin:: getallocator."
ms.assetid: e9db4aa0-4f53-4ca4-babb-5e0215c7c284
title: Metodo CTransInPlaceInputPin. getallocator (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.GetAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7798640297539a8fa8f6349c799e61e7e22a453d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326198"
---
# <a name="ctransinplaceinputpingetallocator-method"></a><span data-ttu-id="d52f5-104">Metodo CTransInPlaceInputPin. getallocator</span><span class="sxs-lookup"><span data-stu-id="d52f5-104">CTransInPlaceInputPin.GetAllocator method</span></span>

<span data-ttu-id="d52f5-105">Il `GetAllocator` metodo recupera l'allocatore di memoria proposto da questo pin.</span><span class="sxs-lookup"><span data-stu-id="d52f5-105">The `GetAllocator` method retrieves the memory allocator proposed by this pin.</span></span> <span data-ttu-id="d52f5-106">Questo metodo implementa il metodo [**IMemInputPin:: Getallocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) .</span><span class="sxs-lookup"><span data-stu-id="d52f5-106">This method implements the [**IMemInputPin::GetAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d52f5-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d52f5-107">Syntax</span></span>


```C++
HRESULT GetAllocator(
   IMemAllocator **ppAllocator
);
```



## <a name="parameters"></a><span data-ttu-id="d52f5-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d52f5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d52f5-109">*ppAllocator*</span><span class="sxs-lookup"><span data-stu-id="d52f5-109">*ppAllocator*</span></span> 
</dt> <dd>

<span data-ttu-id="d52f5-110">Riceve un puntatore all'interfaccia [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) dell'allocatore.</span><span class="sxs-lookup"><span data-stu-id="d52f5-110">Receives a pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d52f5-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d52f5-111">Return value</span></span>

<span data-ttu-id="d52f5-112">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d52f5-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="d52f5-113">I valori possibili includono quelli mostrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="d52f5-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="d52f5-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="d52f5-114">Return code</span></span>                                                                                          | <span data-ttu-id="d52f5-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d52f5-115">Description</span></span>                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="d52f5-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d52f5-116"><dt>**S\_OK**</dt></span></span> </dl>                 | <span data-ttu-id="d52f5-117">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="d52f5-117">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="d52f5-118"><dt>**\_ \_ \_ allocatore E nessun allocatore**</dt></span><span class="sxs-lookup"><span data-stu-id="d52f5-118"><dt>**VFW\_E\_NO\_ALLOCATOR**</dt></span></span> </dl> | <span data-ttu-id="d52f5-119">Nessun allocatore disponibile.</span><span class="sxs-lookup"><span data-stu-id="d52f5-119">No allocator is available.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d52f5-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="d52f5-120">Remarks</span></span>

<span data-ttu-id="d52f5-121">Se il pin di output del filtro è connesso, questo metodo richiede un allocatore dal pin di input del filtro downstream.</span><span class="sxs-lookup"><span data-stu-id="d52f5-121">If the filter's output pin is connected, this method requests an allocator from the downstream filter's input pin.</span></span>

<span data-ttu-id="d52f5-122">Se il pin di output del filtro non è connesso, questo metodo crea un allocatore temporaneo.</span><span class="sxs-lookup"><span data-stu-id="d52f5-122">If the filter's output pin is not connected, this method creates a temporary allocator.</span></span> <span data-ttu-id="d52f5-123">Successivamente, quando il pin di output sarà connesso, il filtro riconnetterà il pin di input e rinegozierà l'allocatore.</span><span class="sxs-lookup"><span data-stu-id="d52f5-123">Later, when the output pin is connected, the filter will reconnect the input pin and renegotiate the allocator.</span></span>

## <a name="requirements"></a><span data-ttu-id="d52f5-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d52f5-124">Requirements</span></span>



| <span data-ttu-id="d52f5-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="d52f5-125">Requirement</span></span> | <span data-ttu-id="d52f5-126">Valore</span><span class="sxs-lookup"><span data-stu-id="d52f5-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d52f5-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d52f5-127">Header</span></span><br/>  | <dl> <span data-ttu-id="d52f5-128"><dt>Transip. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d52f5-128"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d52f5-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="d52f5-129">Library</span></span><br/> | <dl> <span data-ttu-id="d52f5-130"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d52f5-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d52f5-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d52f5-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d52f5-132">**Classe CTransInPlaceInputPin**</span><span class="sxs-lookup"><span data-stu-id="d52f5-132">**CTransInPlaceInputPin Class**</span></span>](ctransinplaceinputpin.md)
</dt> </dl>

 

 




