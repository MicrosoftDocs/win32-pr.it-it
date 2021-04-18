---
description: Il metodo NotifyThread notifica al thread che la coda contiene dati.
ms.assetid: d91cde3f-2876-4fb4-a124-f1460bba2cc9
title: Metodo COutputQueue. NotifyThread (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.NotifyThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7bb5f965bac15e99140955e8ee2519feaadfef85
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324684"
---
# <a name="coutputqueuenotifythread-method"></a><span data-ttu-id="73efb-103">COutputQueue. NotifyThread, metodo</span><span class="sxs-lookup"><span data-stu-id="73efb-103">COutputQueue.NotifyThread method</span></span>

<span data-ttu-id="73efb-104">Il `NotifyThread` metodo notifica al thread che la coda contiene dati.</span><span class="sxs-lookup"><span data-stu-id="73efb-104">The `NotifyThread` method notifies the thread that the queue contains data.</span></span>

## <a name="syntax"></a><span data-ttu-id="73efb-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="73efb-105">Syntax</span></span>


```C++
void NotifyThread();
```



## <a name="parameters"></a><span data-ttu-id="73efb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="73efb-106">Parameters</span></span>

<span data-ttu-id="73efb-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="73efb-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="73efb-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="73efb-108">Return value</span></span>

<span data-ttu-id="73efb-109">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="73efb-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="73efb-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="73efb-110">Remarks</span></span>

<span data-ttu-id="73efb-111">Prima di chiamare questo metodo, mantenere la sezione critica.</span><span class="sxs-lookup"><span data-stu-id="73efb-111">Hold the critical section before calling this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="73efb-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="73efb-112">Requirements</span></span>



| <span data-ttu-id="73efb-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="73efb-113">Requirement</span></span> | <span data-ttu-id="73efb-114">Valore</span><span class="sxs-lookup"><span data-stu-id="73efb-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73efb-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="73efb-115">Header</span></span><br/>  | <dl> <span data-ttu-id="73efb-116"><dt>Outputq. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="73efb-116"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="73efb-117">Libreria</span><span class="sxs-lookup"><span data-stu-id="73efb-117">Library</span></span><br/> | <dl> <span data-ttu-id="73efb-118"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="73efb-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73efb-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="73efb-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73efb-120">**Classe COutputQueue**</span><span class="sxs-lookup"><span data-stu-id="73efb-120">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




