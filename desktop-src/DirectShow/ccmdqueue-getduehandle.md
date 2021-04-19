---
description: Il metodo GetDueHandle recupera l'handle dell'evento da segnalare.
ms.assetid: 495ea76d-8b94-48a9-8025-06ab18b66693
title: Metodo CCmdQueue. GetDueHandle (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.GetDueHandle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4cb7c8c965c72abe6343a8a75863e0e6969dc5c6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324477"
---
# <a name="ccmdqueuegetduehandle-method"></a><span data-ttu-id="46a47-103">CCmdQueue. GetDueHandle, metodo</span><span class="sxs-lookup"><span data-stu-id="46a47-103">CCmdQueue.GetDueHandle method</span></span>

<span data-ttu-id="46a47-104">Il `GetDueHandle` metodo recupera l'handle dell'evento da segnalare.</span><span class="sxs-lookup"><span data-stu-id="46a47-104">The `GetDueHandle` method retrieves the event handle to be signaled.</span></span>

## <a name="syntax"></a><span data-ttu-id="46a47-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="46a47-105">Syntax</span></span>


```C++
HANDLE GetDueHandle();
```



## <a name="parameters"></a><span data-ttu-id="46a47-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="46a47-106">Parameters</span></span>

<span data-ttu-id="46a47-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="46a47-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="46a47-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="46a47-108">Return value</span></span>

<span data-ttu-id="46a47-109">Restituisce l'handle dell'evento.</span><span class="sxs-lookup"><span data-stu-id="46a47-109">Returns the event handle.</span></span>

## <a name="remarks"></a><span data-ttu-id="46a47-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="46a47-110">Remarks</span></span>

<span data-ttu-id="46a47-111">Restituisce l'handle dell'evento ogni volta che sono presenti comandi posticipati che sono dovuti all'esecuzione (quando [**CCmdQueue:: GetDueCommand**](ccmdqueue-getduecommand.md) non verrà bloccato).</span><span class="sxs-lookup"><span data-stu-id="46a47-111">Return the event handle whenever there are deferred commands that are due for execution (when [**CCmdQueue::GetDueCommand**](ccmdqueue-getduecommand.md) will not block).</span></span>

## <a name="requirements"></a><span data-ttu-id="46a47-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="46a47-112">Requirements</span></span>



| <span data-ttu-id="46a47-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="46a47-113">Requirement</span></span> | <span data-ttu-id="46a47-114">Valore</span><span class="sxs-lookup"><span data-stu-id="46a47-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46a47-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="46a47-115">Header</span></span><br/>  | <dl> <span data-ttu-id="46a47-116"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="46a47-116"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="46a47-117">Libreria</span><span class="sxs-lookup"><span data-stu-id="46a47-117">Library</span></span><br/> | <dl> <span data-ttu-id="46a47-118"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="46a47-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46a47-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="46a47-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46a47-120">**Classe CCmdQueue**</span><span class="sxs-lookup"><span data-stu-id="46a47-120">**CCmdQueue Class**</span></span>](ccmdqueue.md)
</dt> </dl>

 

 




