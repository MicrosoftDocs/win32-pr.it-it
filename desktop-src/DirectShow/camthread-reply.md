---
description: Il metodo Reply risponde a una richiesta.
ms.assetid: 90e91b99-6a1c-46a2-b83d-eba483f1832a
title: Metodo CAMThread. Reply (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.Reply
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5e86e0bc0155e527aa11c26531ae5608e6828362
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332358"
---
# <a name="camthreadreply-method"></a><span data-ttu-id="065d6-103">Metodo CAMThread. Reply</span><span class="sxs-lookup"><span data-stu-id="065d6-103">CAMThread.Reply method</span></span>

<span data-ttu-id="065d6-104">Il `Reply` metodo risponde a una richiesta.</span><span class="sxs-lookup"><span data-stu-id="065d6-104">The `Reply` method replies to a request.</span></span>

## <a name="syntax"></a><span data-ttu-id="065d6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="065d6-105">Syntax</span></span>


```C++
void Reply(
   DWORD dw
);
```



## <a name="parameters"></a><span data-ttu-id="065d6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="065d6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="065d6-107">*dw*</span><span class="sxs-lookup"><span data-stu-id="065d6-107">*dw*</span></span> 
</dt> <dd>

<span data-ttu-id="065d6-108">Valore da restituire nel metodo [**CAMThread:: CallWorker**](camthread-callworker.md) .</span><span class="sxs-lookup"><span data-stu-id="065d6-108">Value to return in the [**CAMThread::CallWorker**](camthread-callworker.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="065d6-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="065d6-109">Return value</span></span>

<span data-ttu-id="065d6-110">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="065d6-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="065d6-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="065d6-111">Remarks</span></span>

<span data-ttu-id="065d6-112">Il metodo CallWorker si blocca fino a quando non viene chiamato questo metodo.</span><span class="sxs-lookup"><span data-stu-id="065d6-112">The CallWorker method blocks until this method is called.</span></span> <span data-ttu-id="065d6-113">Il parametro *DW* fornisce il valore restituito per CallWorker.</span><span class="sxs-lookup"><span data-stu-id="065d6-113">The *dw* parameter supplies the return value for CallWorker.</span></span> <span data-ttu-id="065d6-114">Chiamare questo metodo nella routine del thread dopo aver recuperato una richiesta, per rilasciare il thread richiedente.</span><span class="sxs-lookup"><span data-stu-id="065d6-114">Call this method in your thread procedure after you retrieve a request, to release the requesting thread.</span></span>

## <a name="requirements"></a><span data-ttu-id="065d6-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="065d6-115">Requirements</span></span>



| <span data-ttu-id="065d6-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="065d6-116">Requirement</span></span> | <span data-ttu-id="065d6-117">Valore</span><span class="sxs-lookup"><span data-stu-id="065d6-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="065d6-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="065d6-118">Header</span></span><br/>  | <dl> <span data-ttu-id="065d6-119"><dt>Wxutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="065d6-119"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="065d6-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="065d6-120">Library</span></span><br/> | <dl> <span data-ttu-id="065d6-121"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="065d6-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="065d6-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="065d6-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="065d6-123">**Classe CAMThread**</span><span class="sxs-lookup"><span data-stu-id="065d6-123">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




