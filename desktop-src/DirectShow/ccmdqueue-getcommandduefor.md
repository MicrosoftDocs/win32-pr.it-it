---
description: Il metodo GetCommandDueFor recupera un comando posticipato pianificato a un'ora specificata.
ms.assetid: f8a2f9ae-f359-4429-aca5-021b6fe2aa93
title: Metodo CCmdQueue. GetCommandDueFor (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.GetCommandDueFor
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 48a01436a68a5b98d08880c1516bbf4576d10be2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324483"
---
# <a name="ccmdqueuegetcommandduefor-method"></a><span data-ttu-id="df087-103">CCmdQueue. GetCommandDueFor, metodo</span><span class="sxs-lookup"><span data-stu-id="df087-103">CCmdQueue.GetCommandDueFor method</span></span>

<span data-ttu-id="df087-104">Il `GetCommandDueFor` metodo recupera un comando posticipato pianificato a un'ora specificata.</span><span class="sxs-lookup"><span data-stu-id="df087-104">The `GetCommandDueFor` method retrieves a deferred command that is scheduled at a specified time.</span></span>

## <a name="syntax"></a><span data-ttu-id="df087-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="df087-105">Syntax</span></span>


```C++
virtual HRESULT GetCommandDueFor(
   REFERENCE_TIME   tStream,
   CDeferredCommand **ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="df087-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="df087-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df087-107">*tStream*</span><span class="sxs-lookup"><span data-stu-id="df087-107">*tStream*</span></span> 
</dt> <dd>

<span data-ttu-id="df087-108">Ora pianificata per il comando.</span><span class="sxs-lookup"><span data-stu-id="df087-108">Time for which the command is scheduled.</span></span>

</dd> <dt>

<span data-ttu-id="df087-109">*ppCmd*</span><span class="sxs-lookup"><span data-stu-id="df087-109">*ppCmd*</span></span> 
</dt> <dd>

<span data-ttu-id="df087-110">Indirizzo di un puntatore al comando posticipato da eseguire al momento specificato nel parametro *tStream* .</span><span class="sxs-lookup"><span data-stu-id="df087-110">Address of a pointer to the deferred command to be carried out at the time specified in the *tStream* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df087-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="df087-111">Return value</span></span>

<span data-ttu-id="df087-112">Restituisce VFW \_ E \_ non \_ trovato se nessun comando è dovuto; in caso contrario, restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="df087-112">Returns VFW\_E\_NOT\_FOUND if no commands are due; otherwise, returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="df087-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="df087-113">Remarks</span></span>

<span data-ttu-id="df087-114">Questa funzione membro accetta un flusso di tempo e restituisce il comando posticipato pianificato in quel momento.</span><span class="sxs-lookup"><span data-stu-id="df087-114">This member function takes a stream time and returns the deferred command scheduled at that time.</span></span> <span data-ttu-id="df087-115">L'offset del tempo effettivo del flusso viene calcolato quando viene eseguita la coda dei comandi.</span><span class="sxs-lookup"><span data-stu-id="df087-115">The actual stream-time offset is calculated when the command queue is run.</span></span> <span data-ttu-id="df087-116">I comandi rimangono accodati fino all'esecuzione o annullati.</span><span class="sxs-lookup"><span data-stu-id="df087-116">Commands remain queued until run or canceled.</span></span> <span data-ttu-id="df087-117">Questa funzione membro non verrà bloccata.</span><span class="sxs-lookup"><span data-stu-id="df087-117">This member function will not block.</span></span>

## <a name="requirements"></a><span data-ttu-id="df087-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="df087-118">Requirements</span></span>



| <span data-ttu-id="df087-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="df087-119">Requirement</span></span> | <span data-ttu-id="df087-120">Valore</span><span class="sxs-lookup"><span data-stu-id="df087-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df087-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="df087-121">Header</span></span><br/>  | <dl> <span data-ttu-id="df087-122"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="df087-122"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="df087-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="df087-123">Library</span></span><br/> | <dl> <span data-ttu-id="df087-124"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="df087-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df087-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="df087-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df087-126">**Classe CCmdQueue**</span><span class="sxs-lookup"><span data-stu-id="df087-126">**CCmdQueue Class**</span></span>](ccmdqueue.md)
</dt> </dl>

 

 




