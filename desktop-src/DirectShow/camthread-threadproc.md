---
description: Il metodo ThreadProc è la routine thread.
ms.assetid: 2d991f15-afea-4843-bc68-aeb5ca69d28b
title: Metodo CAMThread. ThreadProc (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.ThreadProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7081a7f7e1cd84a6bf8d482aa7dddf7a48b39f0a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330543"
---
# <a name="camthreadthreadproc-method"></a><span data-ttu-id="1e956-103">CAMThread. ThreadProc, metodo</span><span class="sxs-lookup"><span data-stu-id="1e956-103">CAMThread.ThreadProc method</span></span>

<span data-ttu-id="1e956-104">Il `ThreadProc` metodo è la routine del thread.</span><span class="sxs-lookup"><span data-stu-id="1e956-104">The `ThreadProc` method is the thread procedure.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e956-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1e956-105">Syntax</span></span>


```C++
virtual DWORD ThreadProc() = 0;
```



## <a name="parameters"></a><span data-ttu-id="1e956-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1e956-106">Parameters</span></span>

<span data-ttu-id="1e956-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="1e956-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1e956-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1e956-108">Return value</span></span>

<span data-ttu-id="1e956-109">Restituisce un valore **DWORD** il cui significato è definito dalla classe derivata.</span><span class="sxs-lookup"><span data-stu-id="1e956-109">Returns a **DWORD** value whose meaning is defined by the derived class.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e956-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="1e956-110">Remarks</span></span>

<span data-ttu-id="1e956-111">Si tratta di un metodo virtuale puro.</span><span class="sxs-lookup"><span data-stu-id="1e956-111">This is a pure virtual method.</span></span> <span data-ttu-id="1e956-112">Implementare questo metodo nella classe derivata per fornire una routine del thread.</span><span class="sxs-lookup"><span data-stu-id="1e956-112">Implement this method in your derived class to supply a thread procedure.</span></span> <span data-ttu-id="1e956-113">Quando il metodo [**CAMThread:: create**](camthread-create.md) crea un thread, fornisce l'indirizzo del metodo [**CAMThread:: InitialThreadProc**](camthread-initialthreadproc.md) , che a sua volta chiama il metodo ThreadProc.</span><span class="sxs-lookup"><span data-stu-id="1e956-113">When the [**CAMThread::Create**](camthread-create.md) method creates a thread, it gives the address of the [**CAMThread::InitialThreadProc**](camthread-initialthreadproc.md) method, which in turn calls your ThreadProc method.</span></span>

<span data-ttu-id="1e956-114">In genere, il metodo ThreadProc entrerà in un ciclo che recupera le richieste (chiamando i metodi [**CAMThread:: GetRequest**](camthread-getrequest.md) o [**CAMThread:: CheckRequest**](camthread-checkrequest.md) ) ed elabora i dati.</span><span class="sxs-lookup"><span data-stu-id="1e956-114">Typically, your ThreadProc method will enter a loop that retrieves requests (by calling the [**CAMThread::GetRequest**](camthread-getrequest.md) or [**CAMThread::CheckRequest**](camthread-checkrequest.md) methods) and processes data.</span></span>

<span data-ttu-id="1e956-115">Quando questo metodo viene restituito, il thread viene chiuso.</span><span class="sxs-lookup"><span data-stu-id="1e956-115">When this method returns, the thread exits.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e956-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1e956-116">Requirements</span></span>



| <span data-ttu-id="1e956-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e956-117">Requirement</span></span> | <span data-ttu-id="1e956-118">Valore</span><span class="sxs-lookup"><span data-stu-id="1e956-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e956-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1e956-119">Header</span></span><br/>  | <dl> <span data-ttu-id="1e956-120"><dt>Wxutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1e956-120"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="1e956-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="1e956-121">Library</span></span><br/> | <dl> <span data-ttu-id="1e956-122"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="1e956-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e956-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1e956-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e956-124">**Classe CAMThread**</span><span class="sxs-lookup"><span data-stu-id="1e956-124">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




