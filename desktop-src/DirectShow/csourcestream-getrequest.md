---
description: Il metodo GetRequest attende la richiesta del thread successivo.
ms.assetid: 2938374b-174f-4276-98a2-20a084bd9bbd
title: Metodo CSourceStream. GetRequest (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.GetRequest
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3f45e6f6cf269f7aca6741d8e1c150c7054b07f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330048"
---
# <a name="csourcestreamgetrequest-method"></a><span data-ttu-id="ddfb5-103">Metodo CSourceStream. GetRequest</span><span class="sxs-lookup"><span data-stu-id="ddfb5-103">CSourceStream.GetRequest method</span></span>

<span data-ttu-id="ddfb5-104">Il `GetRequest` metodo attende la richiesta del thread successivo.</span><span class="sxs-lookup"><span data-stu-id="ddfb5-104">The `GetRequest` method waits for the next thread request.</span></span>

## <a name="syntax"></a><span data-ttu-id="ddfb5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ddfb5-105">Syntax</span></span>


```C++
Command GetRequest();
```



## <a name="parameters"></a><span data-ttu-id="ddfb5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ddfb5-106">Parameters</span></span>

<span data-ttu-id="ddfb5-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="ddfb5-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ddfb5-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ddfb5-108">Return value</span></span>

<span data-ttu-id="ddfb5-109">Restituisce la richiesta successiva del thread.</span><span class="sxs-lookup"><span data-stu-id="ddfb5-109">Returns the next thread request.</span></span>

## <a name="remarks"></a><span data-ttu-id="ddfb5-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="ddfb5-110">Remarks</span></span>

<span data-ttu-id="ddfb5-111">Questo metodo esegue l'override del metodo [**CAMThread:: GetRequest**](camthread-getrequest.md) .</span><span class="sxs-lookup"><span data-stu-id="ddfb5-111">This method overrides the [**CAMThread::GetRequest**](camthread-getrequest.md) method.</span></span> <span data-ttu-id="ddfb5-112">Viene eseguito il cast del valore restituito al tipo enumerato seguente:</span><span class="sxs-lookup"><span data-stu-id="ddfb5-112">The return value is cast to the following enumerated type:</span></span>


```C++
enum Command {CMD_INIT, CMD_PAUSE, CMD_RUN, CMD_STOP, CMD_EXIT};
```



## <a name="requirements"></a><span data-ttu-id="ddfb5-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ddfb5-113">Requirements</span></span>



| <span data-ttu-id="ddfb5-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ddfb5-114">Requirement</span></span> | <span data-ttu-id="ddfb5-115">Valore</span><span class="sxs-lookup"><span data-stu-id="ddfb5-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ddfb5-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ddfb5-116">Header</span></span><br/>  | <dl> <span data-ttu-id="ddfb5-117"><dt>Source. h (Includi Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ddfb5-117"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="ddfb5-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="ddfb5-118">Library</span></span><br/> | <dl> <span data-ttu-id="ddfb5-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ddfb5-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ddfb5-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ddfb5-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddfb5-121">**Classe CSourceStream**</span><span class="sxs-lookup"><span data-stu-id="ddfb5-121">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




