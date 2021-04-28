---
description: 'Metodo CBaseInputPin.NotifyAllocator: il metodo NotifyAllocator specifica un allocatore per la connessione. Questo metodo implementa il metodo IMemInputPin::NotifyAllocator.'
ms.assetid: 16167bd5-2d33-4329-87ec-6a6c578e0060
title: Metodo CBaseInputPin.NotifyAllocator (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.NotifyAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c63e448d0cf2d287a441a4983f6a2e06bd9b8151
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099716"
---
# <a name="cbaseinputpinnotifyallocator-method"></a><span data-ttu-id="2c19b-104">Metodo CBaseInputPin.NotifyAllocator</span><span class="sxs-lookup"><span data-stu-id="2c19b-104">CBaseInputPin.NotifyAllocator method</span></span>

<span data-ttu-id="2c19b-105">Il `NotifyAllocator` metodo specifica un allocatore per la connessione.</span><span class="sxs-lookup"><span data-stu-id="2c19b-105">The `NotifyAllocator` method specifies an allocator for the connection.</span></span> <span data-ttu-id="2c19b-106">Questo metodo implementa il [**metodo IMemInputPin::NotifyAllocator.**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator)</span><span class="sxs-lookup"><span data-stu-id="2c19b-106">This method implements the [**IMemInputPin::NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c19b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2c19b-107">Syntax</span></span>


```C++
HRESULT NotifyAllocator(
   IMemAllocator *pAllocator,
   BOOL          bReadOnly
);
```



## <a name="parameters"></a><span data-ttu-id="2c19b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="2c19b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c19b-109">*pAllocator*</span><span class="sxs-lookup"><span data-stu-id="2c19b-109">*pAllocator*</span></span> 
</dt> <dd>

<span data-ttu-id="2c19b-110">Puntatore all'interfaccia [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) dell'allocatore.</span><span class="sxs-lookup"><span data-stu-id="2c19b-110">Pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

</dd> <dt>

<span data-ttu-id="2c19b-111">*bReadOnly*</span><span class="sxs-lookup"><span data-stu-id="2c19b-111">*bReadOnly*</span></span> 
</dt> <dd>

<span data-ttu-id="2c19b-112">Flag che specifica se gli esempi di questo allocatore sono di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="2c19b-112">Flag that specifies whether samples from this allocator are read-only.</span></span> <span data-ttu-id="2c19b-113">Se **TRUE,** gli esempi sono di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="2c19b-113">If **TRUE**, samples are read-only.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c19b-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2c19b-114">Return value</span></span>

<span data-ttu-id="2c19b-115">Restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2c19b-115">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c19b-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="2c19b-116">Remarks</span></span>

<span data-ttu-id="2c19b-117">Durante la connessione del pin, il pin di output sceglie un allocatore e chiama questo metodo per inviare una notifica al pin di input.</span><span class="sxs-lookup"><span data-stu-id="2c19b-117">During the pin connection, the output pin chooses an allocator and calls this method to notify the input pin.</span></span> <span data-ttu-id="2c19b-118">Il pin di output può usare l'allocatore proposto dal pin di input nel metodo [**IMemInputPin::GetAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) oppure può fornire il proprio allocatore.</span><span class="sxs-lookup"><span data-stu-id="2c19b-118">The output pin can use the allocator that the input pin proposed in the [**IMemInputPin::GetAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) method, or it can provide its own allocator.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c19b-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2c19b-119">Requirements</span></span>



| <span data-ttu-id="2c19b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c19b-120">Requirement</span></span> | <span data-ttu-id="2c19b-121">Valore</span><span class="sxs-lookup"><span data-stu-id="2c19b-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c19b-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2c19b-122">Header</span></span><br/>  | <dl> <span data-ttu-id="2c19b-123"><dt>Amfilter.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="2c19b-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="2c19b-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="2c19b-124">Library</span></span><br/> | <dl> <span data-ttu-id="2c19b-125"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="2c19b-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c19b-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2c19b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c19b-127">**Classe CBaseInputPin**</span><span class="sxs-lookup"><span data-stu-id="2c19b-127">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




