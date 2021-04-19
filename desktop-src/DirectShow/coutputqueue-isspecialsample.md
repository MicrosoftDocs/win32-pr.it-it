---
description: Il metodo IsSpecialSample determina se i dati in coda sono un messaggio di controllo.
ms.assetid: 33d9c7a2-3046-45a5-a9f5-8f33a03bbcdd
title: Metodo COutputQueue. IsSpecialSample (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.IsSpecialSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cc57847d6a977c740bbf50bae220a89b0ed6fab1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325753"
---
# <a name="coutputqueueisspecialsample-method"></a><span data-ttu-id="5b287-103">COutputQueue. IsSpecialSample, metodo</span><span class="sxs-lookup"><span data-stu-id="5b287-103">COutputQueue.IsSpecialSample method</span></span>

<span data-ttu-id="5b287-104">Il `IsSpecialSample` metodo determina se i dati in coda sono un messaggio di controllo.</span><span class="sxs-lookup"><span data-stu-id="5b287-104">The `IsSpecialSample` method determines whether queued data is a control message.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b287-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5b287-105">Syntax</span></span>


```C++
BOOL IsSpecialSample(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="5b287-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5b287-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b287-107">*pSample*</span><span class="sxs-lookup"><span data-stu-id="5b287-107">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="5b287-108">Puntatore a un elemento della coda.</span><span class="sxs-lookup"><span data-stu-id="5b287-108">Pointer to an item in the queue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b287-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5b287-109">Return value</span></span>

<span data-ttu-id="5b287-110">Restituisce **true** se *pSample* è un messaggio di controllo. in caso contrario, **false** .</span><span class="sxs-lookup"><span data-stu-id="5b287-110">Returns **TRUE** if *pSample* is a control message, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b287-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="5b287-111">Remarks</span></span>

<span data-ttu-id="5b287-112">Il metodo [**COutputQueue:: QueueSample**](coutputqueue-queuesample.md) può ricevere i messaggi di controllo oltre agli esempi di supporti.</span><span class="sxs-lookup"><span data-stu-id="5b287-112">The [**COutputQueue::QueueSample**](coutputqueue-queuesample.md) method can receive control messages in addition to media samples.</span></span> <span data-ttu-id="5b287-113">Un messaggio di controllo è una costante definita (di cui viene eseguito il cast a un \_ tipo Long PTR) che indica al thread di eseguire un'azione.</span><span class="sxs-lookup"><span data-stu-id="5b287-113">A control message is a defined constant (cast to a LONG\_PTR type) that instructs the thread to perform an action.</span></span> <span data-ttu-id="5b287-114">I messaggi di controllo non contengono dati multimediali.</span><span class="sxs-lookup"><span data-stu-id="5b287-114">Control messages do not contain media data.</span></span> <span data-ttu-id="5b287-115">Per ulteriori informazioni, vedere **COutputQueue:: QueueSample**.</span><span class="sxs-lookup"><span data-stu-id="5b287-115">For more information, see **COutputQueue::QueueSample**.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b287-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5b287-116">Requirements</span></span>



| <span data-ttu-id="5b287-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b287-117">Requirement</span></span> | <span data-ttu-id="5b287-118">Valore</span><span class="sxs-lookup"><span data-stu-id="5b287-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b287-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5b287-119">Header</span></span><br/>  | <dl> <span data-ttu-id="5b287-120"><dt>Outputq. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5b287-120"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5b287-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="5b287-121">Library</span></span><br/> | <dl> <span data-ttu-id="5b287-122"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="5b287-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b287-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5b287-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b287-124">**Classe COutputQueue**</span><span class="sxs-lookup"><span data-stu-id="5b287-124">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




