---
description: Il metodo CheckRequest controlla se è presente una richiesta, senza blocco.
ms.assetid: 46d0840e-a304-41e3-9016-9f35e404cd30
title: Metodo CAMThread. CheckRequest (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.CheckRequest
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5a004e0f5303cf6702c03e78c292a6a2d832a489
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328273"
---
# <a name="camthreadcheckrequest-method"></a><span data-ttu-id="cd137-103">CAMThread. CheckRequest, metodo</span><span class="sxs-lookup"><span data-stu-id="cd137-103">CAMThread.CheckRequest method</span></span>

<span data-ttu-id="cd137-104">Il `CheckRequest` metodo verifica se è presente una richiesta, senza blocco.</span><span class="sxs-lookup"><span data-stu-id="cd137-104">The `CheckRequest` method checks if there is a request, without blocking.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd137-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cd137-105">Syntax</span></span>


```C++
BOOL CheckRequest(
   DWORD *pParam
);
```



## <a name="parameters"></a><span data-ttu-id="cd137-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="cd137-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd137-107">*pParam*</span><span class="sxs-lookup"><span data-stu-id="cd137-107">*pParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cd137-108">Puntatore a una variabile che riceve il valore passato nell'ultima chiamata al metodo [**CAMThread:: CallWorker**](camthread-callworker.md) .</span><span class="sxs-lookup"><span data-stu-id="cd137-108">Pointer to a variable that receives the value passed in the last call to the [**CAMThread::CallWorker**](camthread-callworker.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd137-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cd137-109">Return value</span></span>

<span data-ttu-id="cd137-110">Restituisce **true** se è presente una richiesta in sospeso; in caso contrario, **false** .</span><span class="sxs-lookup"><span data-stu-id="cd137-110">Returns **TRUE** if there is a pending request, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd137-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="cd137-111">Remarks</span></span>

<span data-ttu-id="cd137-112">Questo metodo è una versione non di blocco del metodo [**CAMThread:: GetRequest**](camthread-getrequest.md) .</span><span class="sxs-lookup"><span data-stu-id="cd137-112">This method is a non-blocking version of the [**CAMThread::GetRequest**](camthread-getrequest.md) method.</span></span>

<span data-ttu-id="cd137-113">Se un altro thread è in attesa di una chiamata a CallWorker, questo metodo recupera il parametro request e restituisce **true**.</span><span class="sxs-lookup"><span data-stu-id="cd137-113">If another thread is waiting on a call to CallWorker, this method retrieves the request parameter and returns **TRUE**.</span></span> <span data-ttu-id="cd137-114">In caso contrario, restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="cd137-114">Otherwise, it returns **FALSE**.</span></span> <span data-ttu-id="cd137-115">Se il metodo restituisce **true**, chiamare il metodo [**CAMThread:: Reply**](camthread-reply.md) per rilasciare il thread richiedente.</span><span class="sxs-lookup"><span data-stu-id="cd137-115">If the method returns **TRUE**, call the [**CAMThread::Reply**](camthread-reply.md) method to release the requesting thread.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd137-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cd137-116">Requirements</span></span>



| <span data-ttu-id="cd137-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd137-117">Requirement</span></span> | <span data-ttu-id="cd137-118">Valore</span><span class="sxs-lookup"><span data-stu-id="cd137-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd137-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cd137-119">Header</span></span><br/>  | <dl> <span data-ttu-id="cd137-120"><dt>Wxutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cd137-120"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="cd137-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="cd137-121">Library</span></span><br/> | <dl> <span data-ttu-id="cd137-122"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="cd137-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd137-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cd137-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd137-124">**Classe CAMThread**</span><span class="sxs-lookup"><span data-stu-id="cd137-124">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




