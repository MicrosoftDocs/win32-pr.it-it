---
description: Il metodo AsynchronousBlockOutputPin blocca il PIN. Il metodo può restituire prima del blocco del PIN.
ms.assetid: 14cdc973-f0d3-4d1b-8491-67c1421f630b
title: Metodo CDynamicOutputPin. AsynchronousBlockOutputPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.AsynchronousBlockOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 67232bf1081f9c9ea088968cb6c5d02667b00eeb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333464"
---
# <a name="cdynamicoutputpinasynchronousblockoutputpin-method"></a><span data-ttu-id="f0176-104">CDynamicOutputPin. AsynchronousBlockOutputPin, metodo</span><span class="sxs-lookup"><span data-stu-id="f0176-104">CDynamicOutputPin.AsynchronousBlockOutputPin method</span></span>

<span data-ttu-id="f0176-105">Il `AsynchronousBlockOutputPin` metodo blocca il PIN.</span><span class="sxs-lookup"><span data-stu-id="f0176-105">The `AsynchronousBlockOutputPin` method blocks the pin.</span></span> <span data-ttu-id="f0176-106">Il metodo può restituire prima del blocco del PIN.</span><span class="sxs-lookup"><span data-stu-id="f0176-106">The method might return before the pin is blocked.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0176-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f0176-107">Syntax</span></span>


```C++
HRESULT AsynchronousBlockOutputPin(
   HANDLE hNotifyCallerPinBlockedEvent
);
```



## <a name="parameters"></a><span data-ttu-id="f0176-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="f0176-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0176-109">*hNotifyCallerPinBlockedEvent*</span><span class="sxs-lookup"><span data-stu-id="f0176-109">*hNotifyCallerPinBlockedEvent*</span></span> 
</dt> <dd>

<span data-ttu-id="f0176-110">Handle per un evento.</span><span class="sxs-lookup"><span data-stu-id="f0176-110">Handle to an event.</span></span> <span data-ttu-id="f0176-111">L'evento viene segnalato quando il pin di output è bloccato o se il chiamante Annulla l'operazione di blocco.</span><span class="sxs-lookup"><span data-stu-id="f0176-111">The event is signaled when the output pin is blocked, or if the caller cancels the block operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0176-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f0176-112">Return value</span></span>

<span data-ttu-id="f0176-113">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f0176-113">Returns an **HRESULT** value.</span></span> <span data-ttu-id="f0176-114">I valori possibili includono quelli mostrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="f0176-114">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="f0176-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="f0176-115">Return code</span></span>                                                                                                                    | <span data-ttu-id="f0176-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f0176-116">Description</span></span>                                              |
|--------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="f0176-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f0176-117"><dt>**S\_OK**</dt></span></span> </dl>                                           | <span data-ttu-id="f0176-118">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="f0176-118">Success.</span></span><br/>                                      |
| <dl> <span data-ttu-id="f0176-119"><dt>**\_pin VFW \_ E \_ già \_ bloccato**</dt></span><span class="sxs-lookup"><span data-stu-id="f0176-119"><dt>**VFW\_E\_PIN\_ALREADY\_BLOCKED**</dt></span></span> </dl>                   | <span data-ttu-id="f0176-120">Il PIN è già bloccato in un altro thread.</span><span class="sxs-lookup"><span data-stu-id="f0176-120">Pin is already blocked on another thread.</span></span><br/>     |
| <dl> <span data-ttu-id="f0176-121"><dt>**\_pin VFW \_ E \_ già \_ bloccato \_ in \_ questo \_ thread**</dt></span><span class="sxs-lookup"><span data-stu-id="f0176-121"><dt>**VFW\_E\_PIN\_ALREADY\_BLOCKED\_ON\_THIS\_THREAD**</dt></span></span> </dl> | <span data-ttu-id="f0176-122">Il PIN è già bloccato nel thread chiamante.</span><span class="sxs-lookup"><span data-stu-id="f0176-122">Pin is already blocked on the calling thread.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f0176-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="f0176-123">Remarks</span></span>

<span data-ttu-id="f0176-124">Non chiamare questo metodo dal thread di streaming.</span><span class="sxs-lookup"><span data-stu-id="f0176-124">Do not call this method from the streaming thread.</span></span>

<span data-ttu-id="f0176-125">Se nessun thread di streaming usa il PIN, questo metodo blocca immediatamente il PIN.</span><span class="sxs-lookup"><span data-stu-id="f0176-125">If no streaming thread is using the pin, this method immediately blocks the pin.</span></span> <span data-ttu-id="f0176-126">In caso contrario, lo stato del PIN viene impostato su "Pending" e viene restituito.</span><span class="sxs-lookup"><span data-stu-id="f0176-126">Otherwise, it sets the pin status to "pending" and returns.</span></span> <span data-ttu-id="f0176-127">Al termine dell'operazione di streaming, il thread di streaming chiama il metodo [**CDynamicOutputPin:: StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) , che blocca il PIN e segnala l'evento **hNotifyCallerPinBlockedEvent** .</span><span class="sxs-lookup"><span data-stu-id="f0176-127">When the streaming operation completes, the streaming thread calls the [**CDynamicOutputPin::StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) method, which blocks the pin and signals the **hNotifyCallerPinBlockedEvent** event.</span></span> <span data-ttu-id="f0176-128">Per annullare un blocco in sospeso, chiamare il metodo [**CDynamicOutputPin:: UnblockOutputPin**](cdynamicoutputpin-unblockoutputpin.md) .</span><span class="sxs-lookup"><span data-stu-id="f0176-128">To cancel a pending block, call the [**CDynamicOutputPin::UnblockOutputPin**](cdynamicoutputpin-unblockoutputpin.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0176-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f0176-129">Requirements</span></span>



| <span data-ttu-id="f0176-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0176-130">Requirement</span></span> | <span data-ttu-id="f0176-131">Valore</span><span class="sxs-lookup"><span data-stu-id="f0176-131">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0176-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f0176-132">Header</span></span><br/>  | <dl> <span data-ttu-id="f0176-133"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f0176-133"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f0176-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="f0176-134">Library</span></span><br/> | <dl> <span data-ttu-id="f0176-135"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f0176-135"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0176-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f0176-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0176-137">**Classe CDynamicOutputPin**</span><span class="sxs-lookup"><span data-stu-id="f0176-137">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




