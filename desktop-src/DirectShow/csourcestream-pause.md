---
description: Il metodo pause segnala al thread di streaming che diventa attivo.
ms.assetid: c97da113-c5a7-422d-9215-70b556e0b8ca
title: Metodo CSourceStream. pause (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Pause
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b6f7cd3b38144edebd98ca655b32bf6092f44269
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330663"
---
# <a name="csourcestreampause-method"></a><span data-ttu-id="cc928-103">CSourceStream. pause (metodo)</span><span class="sxs-lookup"><span data-stu-id="cc928-103">CSourceStream.Pause method</span></span>

<span data-ttu-id="cc928-104">Il `Pause` metodo segnala al thread di streaming di essere attivo.</span><span class="sxs-lookup"><span data-stu-id="cc928-104">The `Pause` method signals the streaming thread to become active.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc928-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cc928-105">Syntax</span></span>


```C++
HRESULT Pause();
```



## <a name="parameters"></a><span data-ttu-id="cc928-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="cc928-106">Parameters</span></span>

<span data-ttu-id="cc928-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="cc928-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cc928-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cc928-108">Return value</span></span>

<span data-ttu-id="cc928-109">Restituisce S \_ OK o e \_ imprevisto.</span><span class="sxs-lookup"><span data-stu-id="cc928-109">Returns S\_OK or E\_UNEXPECTED.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc928-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="cc928-110">Remarks</span></span>

<span data-ttu-id="cc928-111">Il metodo [**CSourceStream:: Active**](csourcestream-active.md) chiama questo metodo.</span><span class="sxs-lookup"><span data-stu-id="cc928-111">The [**CSourceStream::Active**](csourcestream-active.md) method calls this method.</span></span> <span data-ttu-id="cc928-112">Quando il metodo [**CSourceStream:: ThreadProc**](csourcestream-threadproc.md) riceve la richiesta, chiama il metodo [**CSourceStream::D obufferprocessingloop**](csourcestream-dobufferprocessingloop.md) .</span><span class="sxs-lookup"><span data-stu-id="cc928-112">When the [**CSourceStream::ThreadProc**](csourcestream-threadproc.md) method receives this request, it calls the [**CSourceStream::DoBufferProcessingLoop**](csourcestream-dobufferprocessingloop.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc928-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cc928-113">Requirements</span></span>



| <span data-ttu-id="cc928-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc928-114">Requirement</span></span> | <span data-ttu-id="cc928-115">Valore</span><span class="sxs-lookup"><span data-stu-id="cc928-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc928-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cc928-116">Header</span></span><br/>  | <dl> <span data-ttu-id="cc928-117"><dt>Source. h (Includi Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cc928-117"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="cc928-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="cc928-118">Library</span></span><br/> | <dl> <span data-ttu-id="cc928-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="cc928-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc928-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cc928-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc928-121">**Classe CSourceStream**</span><span class="sxs-lookup"><span data-stu-id="cc928-121">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




