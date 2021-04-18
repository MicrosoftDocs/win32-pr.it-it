---
description: Il metodo OnThreadDestroy viene chiamato quando il thread di streaming sta per uscire.
ms.assetid: a484b6d2-bce6-4a42-9176-2a6ce374e28b
title: Metodo CSourceStream. OnThreadDestroy (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.OnThreadDestroy
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3e7377ce11955d7121a33311d390464e042b98f5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330038"
---
# <a name="csourcestreamonthreaddestroy-method"></a><span data-ttu-id="19e77-103">CSourceStream. OnThreadDestroy, metodo</span><span class="sxs-lookup"><span data-stu-id="19e77-103">CSourceStream.OnThreadDestroy method</span></span>

<span data-ttu-id="19e77-104">Il `OnThreadDestroy` metodo viene chiamato quando il thread di streaming sta per uscire.</span><span class="sxs-lookup"><span data-stu-id="19e77-104">The `OnThreadDestroy` method is called when the streaming thread is about to exit.</span></span>

## <a name="syntax"></a><span data-ttu-id="19e77-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="19e77-105">Syntax</span></span>


```C++
virtual HRESULT OnThreadDestroy();
```



## <a name="parameters"></a><span data-ttu-id="19e77-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="19e77-106">Parameters</span></span>

<span data-ttu-id="19e77-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="19e77-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="19e77-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="19e77-108">Return value</span></span>

<span data-ttu-id="19e77-109">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="19e77-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="19e77-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="19e77-110">Remarks</span></span>

<span data-ttu-id="19e77-111">La routine thread, [**CSourceStream:: ThreadProc**](csourcestream-threadproc.md), chiama questo metodo prima di uscire.</span><span class="sxs-lookup"><span data-stu-id="19e77-111">The thread procedure, [**CSourceStream::ThreadProc**](csourcestream-threadproc.md), calls this method before it exits.</span></span> <span data-ttu-id="19e77-112">Il metodo non esegue alcuna operazione nella classe di base. è disponibile per la classe derivata di cui eseguire l'override.</span><span class="sxs-lookup"><span data-stu-id="19e77-112">The method does nothing in the base class; it is available for the derived class to override.</span></span> <span data-ttu-id="19e77-113">Se la classe derivata restituisce un codice di errore, il thread viene chiuso con un errore.</span><span class="sxs-lookup"><span data-stu-id="19e77-113">If the derived class returns an error code, the thread exits with an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="19e77-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="19e77-114">Requirements</span></span>



| <span data-ttu-id="19e77-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="19e77-115">Requirement</span></span> | <span data-ttu-id="19e77-116">Valore</span><span class="sxs-lookup"><span data-stu-id="19e77-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19e77-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="19e77-117">Header</span></span><br/>  | <dl> <span data-ttu-id="19e77-118"><dt>Source. h (Includi Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="19e77-118"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="19e77-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="19e77-119">Library</span></span><br/> | <dl> <span data-ttu-id="19e77-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="19e77-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19e77-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="19e77-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19e77-122">**Classe CSourceStream**</span><span class="sxs-lookup"><span data-stu-id="19e77-122">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




