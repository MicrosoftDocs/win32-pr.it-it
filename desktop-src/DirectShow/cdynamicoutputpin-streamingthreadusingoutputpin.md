---
description: Il metodo StreamingThreadUsingOutputPin determina se un thread sta eseguendo un'operazione di flusso sul pin.
ms.assetid: b6432a11-4e8b-4eb4-ad8e-aaff9398641b
title: Metodo CDynamicOutputPin. StreamingThreadUsingOutputPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.StreamingThreadUsingOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 797dcb94e227861642de2a05e6edf24f675bb4e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331646"
---
# <a name="cdynamicoutputpinstreamingthreadusingoutputpin-method"></a><span data-ttu-id="969cb-103">CDynamicOutputPin. StreamingThreadUsingOutputPin, metodo</span><span class="sxs-lookup"><span data-stu-id="969cb-103">CDynamicOutputPin.StreamingThreadUsingOutputPin method</span></span>

<span data-ttu-id="969cb-104">Il metodo StreamingThreadUsingOutputPin determina se un thread sta eseguendo un'operazione di flusso sul pin.</span><span class="sxs-lookup"><span data-stu-id="969cb-104">The StreamingThreadUsingOutputPin method determines whether any thread is performing a streaming operation on the pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="969cb-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="969cb-105">Syntax</span></span>


```C++
virtual bool StreamingThreadUsingOutputPin();
```



## <a name="parameters"></a><span data-ttu-id="969cb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="969cb-106">Parameters</span></span>

<span data-ttu-id="969cb-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="969cb-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="969cb-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="969cb-108">Return value</span></span>

<span data-ttu-id="969cb-109">Restituisce **true** se un thread sta eseguendo un'operazione di flusso sul pin.</span><span class="sxs-lookup"><span data-stu-id="969cb-109">Returns **TRUE** if a thread is performing a streaming operation on the pin.</span></span> <span data-ttu-id="969cb-110">In caso contrario, restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="969cb-110">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="969cb-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="969cb-111">Remarks</span></span>

<span data-ttu-id="969cb-112">Se i thread sono stati restituiti correttamente dal metodo [**CDynamicOutputPin:: StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) e non hanno eseguito una chiamata corrispondente al metodo [**CDynamicOutputPin:: StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) , questo metodo restituisce **true**.</span><span class="sxs-lookup"><span data-stu-id="969cb-112">If any threads have successfully returned from the [**CDynamicOutputPin::StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) method and have not made a corresponding call to the [**CDynamicOutputPin::StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) method, this method returns **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="969cb-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="969cb-113">Requirements</span></span>



| <span data-ttu-id="969cb-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="969cb-114">Requirement</span></span> | <span data-ttu-id="969cb-115">Valore</span><span class="sxs-lookup"><span data-stu-id="969cb-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="969cb-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="969cb-116">Header</span></span><br/>  | <dl> <span data-ttu-id="969cb-117"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="969cb-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="969cb-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="969cb-118">Library</span></span><br/> | <dl> <span data-ttu-id="969cb-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="969cb-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="969cb-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="969cb-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="969cb-121">**Classe CDynamicOutputPin**</span><span class="sxs-lookup"><span data-stu-id="969cb-121">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




