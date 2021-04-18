---
description: "Il metodo getallocator recupera l'allocatore di memoria proposto da questo pin. Questo metodo implementa il metodo IMemInputPin:: getallocator."
ms.assetid: 07bc77f8-a877-4403-b424-20bda715a818
title: Metodo CBaseInputPin. getallocator (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.GetAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 098738fc63ba1834b1eefb4b2518e3309db35c43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326065"
---
# <a name="cbaseinputpingetallocator-method"></a><span data-ttu-id="06cec-104">Metodo CBaseInputPin. getallocator</span><span class="sxs-lookup"><span data-stu-id="06cec-104">CBaseInputPin.GetAllocator method</span></span>

<span data-ttu-id="06cec-105">Il `GetAllocator` metodo recupera l'allocatore di memoria proposto da questo pin.</span><span class="sxs-lookup"><span data-stu-id="06cec-105">The `GetAllocator` method retrieves the memory allocator proposed by this pin.</span></span> <span data-ttu-id="06cec-106">Questo metodo implementa il metodo [**IMemInputPin:: Getallocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) .</span><span class="sxs-lookup"><span data-stu-id="06cec-106">This method implements the [**IMemInputPin::GetAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="06cec-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="06cec-107">Syntax</span></span>


```C++
HRESULT GetAllocator(
   IMemAllocator **ppAllocator
);
```



## <a name="parameters"></a><span data-ttu-id="06cec-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="06cec-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06cec-109">*ppAllocator*</span><span class="sxs-lookup"><span data-stu-id="06cec-109">*ppAllocator*</span></span> 
</dt> <dd>

<span data-ttu-id="06cec-110">Indirizzo di una variabile che riceve un puntatore all'interfaccia [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) dell'allocatore.</span><span class="sxs-lookup"><span data-stu-id="06cec-110">Address of a variable that receives a pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06cec-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="06cec-111">Return value</span></span>

<span data-ttu-id="06cec-112">Restituisce \_ OK se ha esito positivo o un codice di errore della funzione **CoCreateInstance** .</span><span class="sxs-lookup"><span data-stu-id="06cec-112">Returns S\_OK if successful, or an error code from the **CoCreateInstance** function.</span></span>

## <a name="remarks"></a><span data-ttu-id="06cec-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="06cec-113">Remarks</span></span>

<span data-ttu-id="06cec-114">Questo metodo crea un oggetto [**CMemAllocator**](cmemallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="06cec-114">This method creates a [**CMemAllocator**](cmemallocator.md) object.</span></span> <span data-ttu-id="06cec-115">Eseguire l'override di questo metodo se il filtro usa un allocatore da un pin downstream o un allocatore personalizzato.</span><span class="sxs-lookup"><span data-stu-id="06cec-115">Override this method if your filter uses an allocator from a downstream pin, or a custom allocator.</span></span>

<span data-ttu-id="06cec-116">Se il metodo ha esito positivo, l'interfaccia **IMemAllocator** ha un conteggio dei riferimenti in attesa.</span><span class="sxs-lookup"><span data-stu-id="06cec-116">If the method succeeds, the **IMemAllocator** interface has an outstanding reference count.</span></span> <span data-ttu-id="06cec-117">Assicurarsi di rilasciarlo al termine dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="06cec-117">Be sure to release it when you are done.</span></span>

## <a name="requirements"></a><span data-ttu-id="06cec-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="06cec-118">Requirements</span></span>



| <span data-ttu-id="06cec-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="06cec-119">Requirement</span></span> | <span data-ttu-id="06cec-120">Valore</span><span class="sxs-lookup"><span data-stu-id="06cec-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06cec-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="06cec-121">Header</span></span><br/>  | <dl> <span data-ttu-id="06cec-122"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="06cec-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="06cec-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="06cec-123">Library</span></span><br/> | <dl> <span data-ttu-id="06cec-124"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="06cec-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06cec-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="06cec-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06cec-126">**Classe CBaseInputPin**</span><span class="sxs-lookup"><span data-stu-id="06cec-126">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




