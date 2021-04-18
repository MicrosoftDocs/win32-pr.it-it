---
description: 'Il metodo InitialThreadProc chiama il metodo COutputQueue:: ThreadProc quando viene creato il thread.'
ms.assetid: 6093f0c3-ec58-418d-bb8c-618163c43ac7
title: Metodo COutputQueue.InitialThreadProc (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.InitialThreadProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dfc7b8660d838b6ad31dd298c509b6282ab61810
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331460"
---
# <a name="coutputqueueinitialthreadproc-method"></a><span data-ttu-id="56db7-103">Metodo tialThreadProc COutputQueue.Ini</span><span class="sxs-lookup"><span data-stu-id="56db7-103">COutputQueue.InitialThreadProc method</span></span>

<span data-ttu-id="56db7-104">Il `InitialThreadProc` metodo chiama il metodo [**COutputQueue:: ThreadProc**](coutputqueue-threadproc.md) quando viene creato il thread.</span><span class="sxs-lookup"><span data-stu-id="56db7-104">The `InitialThreadProc` method calls the [**COutputQueue::ThreadProc**](coutputqueue-threadproc.md) method when the thread is created.</span></span>

## <a name="syntax"></a><span data-ttu-id="56db7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="56db7-105">Syntax</span></span>


```C++
static DWORD WINAPI InitialThreadProc(
   LPVOID pv
);
```



## <a name="parameters"></a><span data-ttu-id="56db7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="56db7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56db7-107">*PV*</span><span class="sxs-lookup"><span data-stu-id="56db7-107">*pv*</span></span> 
</dt> <dd>

<span data-ttu-id="56db7-108">`this` puntatore.</span><span class="sxs-lookup"><span data-stu-id="56db7-108">`this` pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56db7-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="56db7-109">Return value</span></span>

<span data-ttu-id="56db7-110">Restituisce il valore restituito dal metodo [**COutputQueue:: ThreadProc**](coutputqueue-threadproc.md) .</span><span class="sxs-lookup"><span data-stu-id="56db7-110">Returns the value returned by the [**COutputQueue::ThreadProc**](coutputqueue-threadproc.md) method.</span></span>

## <a name="remarks"></a><span data-ttu-id="56db7-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="56db7-111">Remarks</span></span>

<span data-ttu-id="56db7-112">Questo metodo è la procedura del thread per il thread di lavoro dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="56db7-112">This method is the thread procedure for the object's worker thread.</span></span> <span data-ttu-id="56db7-113">Il puntatore dell'oggetto `this` è il parametro thread.</span><span class="sxs-lookup"><span data-stu-id="56db7-113">The object's `this` pointer is the thread parameter.</span></span> <span data-ttu-id="56db7-114">Il metodo consente di dereferenziare questo oggetto per chiamare **ThreadProc**.</span><span class="sxs-lookup"><span data-stu-id="56db7-114">The method dereferences this to call **ThreadProc**.</span></span>

## <a name="requirements"></a><span data-ttu-id="56db7-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="56db7-115">Requirements</span></span>



| <span data-ttu-id="56db7-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="56db7-116">Requirement</span></span> | <span data-ttu-id="56db7-117">Valore</span><span class="sxs-lookup"><span data-stu-id="56db7-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56db7-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="56db7-118">Header</span></span><br/>  | <dl> <span data-ttu-id="56db7-119"><dt>Outputq. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="56db7-119"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="56db7-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="56db7-120">Library</span></span><br/> | <dl> <span data-ttu-id="56db7-121"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="56db7-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56db7-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="56db7-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56db7-123">**Classe COutputQueue**</span><span class="sxs-lookup"><span data-stu-id="56db7-123">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




