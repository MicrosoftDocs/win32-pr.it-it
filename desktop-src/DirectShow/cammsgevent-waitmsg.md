---
description: Il metodo WaitMsg attende che l'evento venga segnalato, durante l'invio dei messaggi inviati.
ms.assetid: 5cab98ca-f9f3-4c7c-9ce2-8e16109d8fbb
title: Metodo CAMMsgEvent. WaitMsg (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMMsgEvent.WaitMsg
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9622e962f130a082a5c1206367f4850cebb6ce02
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326946"
---
# <a name="cammsgeventwaitmsg-method"></a><span data-ttu-id="1cc5d-103">CAMMsgEvent. WaitMsg, metodo</span><span class="sxs-lookup"><span data-stu-id="1cc5d-103">CAMMsgEvent.WaitMsg method</span></span>

<span data-ttu-id="1cc5d-104">Il `WaitMsg` metodo attende che l'evento venga segnalato, durante l'invio dei messaggi inviati.</span><span class="sxs-lookup"><span data-stu-id="1cc5d-104">The `WaitMsg` method waits for the event to be signaled, while dispatching sent messages.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cc5d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1cc5d-105">Syntax</span></span>


```C++
BOOL WaitMsg(
   DWORD dwTimeOut = INFINITE
);
```



## <a name="parameters"></a><span data-ttu-id="1cc5d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1cc5d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1cc5d-107">*dwTimeOut*</span><span class="sxs-lookup"><span data-stu-id="1cc5d-107">*dwTimeOut*</span></span> 
</dt> <dd>

<span data-ttu-id="1cc5d-108">Valore di timeout facoltativo, in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="1cc5d-108">Optional time-out value, in milliseconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1cc5d-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1cc5d-109">Return value</span></span>

<span data-ttu-id="1cc5d-110">Restituisce **true** se l'evento viene segnalato oppure **false** se si è verificato il timeout.</span><span class="sxs-lookup"><span data-stu-id="1cc5d-110">Returns **TRUE** if the event is signaled, or **FALSE** if the time-out occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="1cc5d-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="1cc5d-111">Remarks</span></span>

<span data-ttu-id="1cc5d-112">Questo metodo chiama la funzione PeekMessage per elaborare i messaggi.</span><span class="sxs-lookup"><span data-stu-id="1cc5d-112">This method calls the PeekMessage function to process messages.</span></span> <span data-ttu-id="1cc5d-113">Chiamare questo metodo invece di [**CAMEvent:: wait**](camevent-wait.md) se il thread deve elaborare i messaggi in attesa di un evento.</span><span class="sxs-lookup"><span data-stu-id="1cc5d-113">Call this method instead of [**CAMEvent::Wait**](camevent-wait.md) if your thread needs to process messages while waiting for an event.</span></span> <span data-ttu-id="1cc5d-114">Se il thread non elabora i messaggi e un altro thread invia un messaggio, potrebbe verificarsi un deadlock.</span><span class="sxs-lookup"><span data-stu-id="1cc5d-114">If the thread does not process messages and another thread sends a message, deadlock could occur.</span></span>

<span data-ttu-id="1cc5d-115">Si supponga, ad esempio, di creare un thread e di bloccarlo fino a quando il thread non viene inizializzato.</span><span class="sxs-lookup"><span data-stu-id="1cc5d-115">For example, suppose you create a thread and then block until the thread initializes.</span></span> <span data-ttu-id="1cc5d-116">Se il thread invia un messaggio alla finestra chiamando la funzione SendMessage, verrà generato un deadlock.</span><span class="sxs-lookup"><span data-stu-id="1cc5d-116">If the thread sends a message to your window by calling the SendMessage function, it will result in a deadlock.</span></span> <span data-ttu-id="1cc5d-117">Questo perché SendMessage non restituisce un risultato fino a quando il messaggio non è stato elaborato.</span><span class="sxs-lookup"><span data-stu-id="1cc5d-117">This is because SendMessage does not return until the message has been processed.</span></span> <span data-ttu-id="1cc5d-118">La chiamata a WaitMsg consente la restituzione della chiamata SendMessage, impedendo il deadlock.</span><span class="sxs-lookup"><span data-stu-id="1cc5d-118">Calling WaitMsg allows the SendMessage call to return, preventing the deadlock.</span></span>

## <a name="requirements"></a><span data-ttu-id="1cc5d-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1cc5d-119">Requirements</span></span>



| <span data-ttu-id="1cc5d-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="1cc5d-120">Requirement</span></span> | <span data-ttu-id="1cc5d-121">Valore</span><span class="sxs-lookup"><span data-stu-id="1cc5d-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1cc5d-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1cc5d-122">Header</span></span><br/>  | <dl> <span data-ttu-id="1cc5d-123"><dt>Wxutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1cc5d-123"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="1cc5d-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="1cc5d-124">Library</span></span><br/> | <dl> <span data-ttu-id="1cc5d-125"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="1cc5d-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1cc5d-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1cc5d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cc5d-127">**Classe CAMMsgEvent**</span><span class="sxs-lookup"><span data-stu-id="1cc5d-127">**CAMMsgEvent Class**</span></span>](cammsgevent.md)
</dt> </dl>

 

 




