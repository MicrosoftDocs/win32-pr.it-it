---
description: Il metodo OnThreadCreate viene chiamato quando viene inizializzato il thread di streaming.
ms.assetid: eeaa0d12-3185-4c97-b481-fc420cfc0897
title: Metodo CSourceStream. OnThreadCreate (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.OnThreadCreate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a5ae3c210ca81eafa1951fc51301eaf50491357f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330041"
---
# <a name="csourcestreamonthreadcreate-method"></a><span data-ttu-id="77938-103">CSourceStream. OnThreadCreate, metodo</span><span class="sxs-lookup"><span data-stu-id="77938-103">CSourceStream.OnThreadCreate method</span></span>

<span data-ttu-id="77938-104">Il `OnThreadCreate` metodo viene chiamato quando viene inizializzato il thread di streaming.</span><span class="sxs-lookup"><span data-stu-id="77938-104">The `OnThreadCreate` method is called when the streaming thread is initialized.</span></span>

## <a name="syntax"></a><span data-ttu-id="77938-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="77938-105">Syntax</span></span>


```C++
virtual HRESULT OnThreadCreate();
```



## <a name="parameters"></a><span data-ttu-id="77938-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="77938-106">Parameters</span></span>

<span data-ttu-id="77938-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="77938-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="77938-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="77938-108">Return value</span></span>

<span data-ttu-id="77938-109">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="77938-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="77938-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="77938-110">Remarks</span></span>

<span data-ttu-id="77938-111">La routine thread, [**CSourceStream:: ThreadProc**](csourcestream-threadproc.md), chiama questo metodo quando riceve prima una richiesta [**CSourceStream:: init**](csourcestream-init.md) .</span><span class="sxs-lookup"><span data-stu-id="77938-111">The thread procedure, [**CSourceStream::ThreadProc**](csourcestream-threadproc.md), calls this method when it first receives a [**CSourceStream::Init**](csourcestream-init.md) request.</span></span> <span data-ttu-id="77938-112">Il metodo non esegue alcuna operazione nella classe di base.</span><span class="sxs-lookup"><span data-stu-id="77938-112">The method does nothing in the base class.</span></span> <span data-ttu-id="77938-113">La classe derivata può eseguire l'override di questo metodo per eseguire le inizializzazioni dei thread.</span><span class="sxs-lookup"><span data-stu-id="77938-113">The derived class can override this method to perform thread initializations.</span></span> <span data-ttu-id="77938-114">Se la classe derivata restituisce un codice di errore, il thread viene chiuso con un errore.</span><span class="sxs-lookup"><span data-stu-id="77938-114">If the derived class returns an error code, the thread exits with an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="77938-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="77938-115">Requirements</span></span>



| <span data-ttu-id="77938-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="77938-116">Requirement</span></span> | <span data-ttu-id="77938-117">Valore</span><span class="sxs-lookup"><span data-stu-id="77938-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77938-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="77938-118">Header</span></span><br/>  | <dl> <span data-ttu-id="77938-119"><dt>Source. h (Includi Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="77938-119"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="77938-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="77938-120">Library</span></span><br/> | <dl> <span data-ttu-id="77938-121"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="77938-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77938-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="77938-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77938-123">**Classe CSourceStream**</span><span class="sxs-lookup"><span data-stu-id="77938-123">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




