---
description: Il metodo set segnala l'evento.
ms.assetid: dfcb1601-aa65-47f5-ae3c-f13fcd7b1398
title: Metodo CAMEvent. set (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMEvent.Set
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c9caeed17d42d121ae9263bf6c1fcd011ed573c7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331335"
---
# <a name="cameventset-method"></a><span data-ttu-id="c27ae-103">Metodo CAMEvent. set</span><span class="sxs-lookup"><span data-stu-id="c27ae-103">CAMEvent.Set method</span></span>

<span data-ttu-id="c27ae-104">Il `Set` metodo segnala l'evento.</span><span class="sxs-lookup"><span data-stu-id="c27ae-104">The `Set` method signals the event.</span></span>

## <a name="syntax"></a><span data-ttu-id="c27ae-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c27ae-105">Syntax</span></span>


```C++
void Set();
```



## <a name="parameters"></a><span data-ttu-id="c27ae-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c27ae-106">Parameters</span></span>

<span data-ttu-id="c27ae-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="c27ae-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c27ae-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c27ae-108">Return value</span></span>

<span data-ttu-id="c27ae-109">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="c27ae-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c27ae-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="c27ae-110">Remarks</span></span>

<span data-ttu-id="c27ae-111">Il comportamento varia a seconda che l'oggetto sia un evento di reimpostazione automatica o un evento di reimpostazione manuale:</span><span class="sxs-lookup"><span data-stu-id="c27ae-111">The behavior depends on whether the object is an auto-reset event or a manual-reset event:</span></span>

-   <span data-ttu-id="c27ae-112">**Reimpostazione automatica**: se un thread è in attesa di questo evento, viene rilasciato un thread e l'evento viene reimpostato.</span><span class="sxs-lookup"><span data-stu-id="c27ae-112">**Auto-reset**: If any threads are waiting on this event, one thread is released and the event is reset.</span></span> <span data-ttu-id="c27ae-113">Se nessun thread è in attesa di questo evento, l'evento rimane segnalato.</span><span class="sxs-lookup"><span data-stu-id="c27ae-113">If no threads are waiting on this event, the event remains signaled.</span></span>
-   <span data-ttu-id="c27ae-114">**Ripristino manuale**: tutti i thread in attesa di questo evento vengono rilasciati.</span><span class="sxs-lookup"><span data-stu-id="c27ae-114">**Manual-reset**: All the threads waiting on this event are released.</span></span> <span data-ttu-id="c27ae-115">L'evento rimane segnalato.</span><span class="sxs-lookup"><span data-stu-id="c27ae-115">The event remains signaled.</span></span>

## <a name="requirements"></a><span data-ttu-id="c27ae-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c27ae-116">Requirements</span></span>



| <span data-ttu-id="c27ae-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c27ae-117">Requirement</span></span> | <span data-ttu-id="c27ae-118">Valore</span><span class="sxs-lookup"><span data-stu-id="c27ae-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c27ae-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c27ae-119">Header</span></span><br/>  | <dl> <span data-ttu-id="c27ae-120"><dt>Wxutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c27ae-120"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="c27ae-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="c27ae-121">Library</span></span><br/> | <dl> <span data-ttu-id="c27ae-122"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="c27ae-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c27ae-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c27ae-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c27ae-124">**Classe CAMEvent**</span><span class="sxs-lookup"><span data-stu-id="c27ae-124">**CAMEvent Class**</span></span>](camevent.md)
</dt> </dl>

 

 




