---
description: Il metodo DecideAllocator seleziona un allocatore di memoria.
ms.assetid: cdc15b0e-ea1b-43aa-9267-95fa9db56ed5
title: Metodo CBaseOutputPin. DecideAllocator (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.DecideAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4e587562341118b904803302f0fd7249ebf8e507
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329546"
---
# <a name="cbaseoutputpindecideallocator-method"></a><span data-ttu-id="25fc0-103">CBaseOutputPin. DecideAllocator, metodo</span><span class="sxs-lookup"><span data-stu-id="25fc0-103">CBaseOutputPin.DecideAllocator method</span></span>

<span data-ttu-id="25fc0-104">Il `DecideAllocator` metodo seleziona un allocatore di memoria.</span><span class="sxs-lookup"><span data-stu-id="25fc0-104">The `DecideAllocator` method selects a memory allocator.</span></span>

## <a name="syntax"></a><span data-ttu-id="25fc0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="25fc0-105">Syntax</span></span>


```C++
virtual HRESULT DecideAllocator(
   IMemInputPin  *pPin,
   IMemAllocator **pAlloc
);
```



## <a name="parameters"></a><span data-ttu-id="25fc0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="25fc0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25fc0-107">*pPin*</span><span class="sxs-lookup"><span data-stu-id="25fc0-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="25fc0-108">Puntatore all'interfaccia [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) del PIN di input.</span><span class="sxs-lookup"><span data-stu-id="25fc0-108">Pointer to the input pin's [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface.</span></span>

</dd> <dt>

<span data-ttu-id="25fc0-109">*pAlloc*</span><span class="sxs-lookup"><span data-stu-id="25fc0-109">*pAlloc*</span></span> 
</dt> <dd>

<span data-ttu-id="25fc0-110">Indirizzo di una variabile che riceve un puntatore all'interfaccia [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) dell'allocatore.</span><span class="sxs-lookup"><span data-stu-id="25fc0-110">Address of a variable that receives a pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25fc0-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="25fc0-111">Return value</span></span>

<span data-ttu-id="25fc0-112">Restituisce \_ OK se ha esito positivo o un valore **HRESULT** che indica la ragione dell'errore.</span><span class="sxs-lookup"><span data-stu-id="25fc0-112">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="25fc0-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="25fc0-113">Remarks</span></span>

<span data-ttu-id="25fc0-114">Questo metodo viene chiamato alla fine del processo di connessione del PIN.</span><span class="sxs-lookup"><span data-stu-id="25fc0-114">This method is called at the end of the pin connection process.</span></span> <span data-ttu-id="25fc0-115">Esegue i passaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="25fc0-115">It performs the following steps:</span></span>

1.  <span data-ttu-id="25fc0-116">Chiama il metodo [**IMemInputPin:: GetAllocatorRequirements**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements) per recuperare i requisiti del buffer del PIN di input, se presenti.</span><span class="sxs-lookup"><span data-stu-id="25fc0-116">Calls the [**IMemInputPin::GetAllocatorRequirements**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements) method to retrieve the input pin's buffer requirements, if any.</span></span>
2.  <span data-ttu-id="25fc0-117">Chiama il metodo [**IMemInputPin:: Getallocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) per richiedere un allocatore dal pin di input.</span><span class="sxs-lookup"><span data-stu-id="25fc0-117">Calls the [**IMemInputPin::GetAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) method to request an allocator from the input pin.</span></span> <span data-ttu-id="25fc0-118">Se il pin di input non fornisce un allocatore, il pin di output ne crea uno chiamando il metodo della classe [**CBaseOutputPin:: InitAllocator**](cbaseoutputpin-initallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="25fc0-118">If the input pin does not provide an allocator, the output pin creates one by calling the [**CBaseOutputPin::InitAllocator**](cbaseoutputpin-initallocator.md) class method.</span></span>
3.  <span data-ttu-id="25fc0-119">Chiama il metodo della classe [**CBaseOutputPin::D ecidebuffersize**](cbaseoutputpin-decidebuffersize.md) , che imposta le proprietà dell'allocatore.</span><span class="sxs-lookup"><span data-stu-id="25fc0-119">Calls the [**CBaseOutputPin::DecideBufferSize**](cbaseoutputpin-decidebuffersize.md) class method, which sets the allocator properties.</span></span> <span data-ttu-id="25fc0-120">Si tratta di un metodo virtuale puro. la classe derivata deve implementarla.</span><span class="sxs-lookup"><span data-stu-id="25fc0-120">This is a pure virtual method; the derived class must implement it.</span></span>
4.  <span data-ttu-id="25fc0-121">Chiama il metodo [**IMemInputPin:: NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) , che invia una notifica al pin di input dell'allocatore usato.</span><span class="sxs-lookup"><span data-stu-id="25fc0-121">Calls the [**IMemInputPin::NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) method, which notifies the input pin of the allocator being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="25fc0-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="25fc0-122">Requirements</span></span>



| <span data-ttu-id="25fc0-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="25fc0-123">Requirement</span></span> | <span data-ttu-id="25fc0-124">Valore</span><span class="sxs-lookup"><span data-stu-id="25fc0-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25fc0-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="25fc0-125">Header</span></span><br/>  | <dl> <span data-ttu-id="25fc0-126"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="25fc0-126"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="25fc0-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="25fc0-127">Library</span></span><br/> | <dl> <span data-ttu-id="25fc0-128"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="25fc0-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25fc0-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="25fc0-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25fc0-130">**Classe CBaseOutputPin**</span><span class="sxs-lookup"><span data-stu-id="25fc0-130">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




