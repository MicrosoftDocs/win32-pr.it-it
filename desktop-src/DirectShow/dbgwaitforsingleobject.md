---
description: Attende che un oggetto venga segnalato.
ms.assetid: 5fbcccd9-9db7-4834-852a-86f28218e92e
title: Funzione DbgWaitForSingleObject (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgWaitForSingleObject
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 99d0058a60b5cf5b362adb80855a788d9a597af6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333268"
---
# <a name="dbgwaitforsingleobject-function"></a><span data-ttu-id="c593b-103">DbgWaitForSingleObject (funzione)</span><span class="sxs-lookup"><span data-stu-id="c593b-103">DbgWaitForSingleObject function</span></span>

<span data-ttu-id="c593b-104">Attende che un oggetto venga segnalato.</span><span class="sxs-lookup"><span data-stu-id="c593b-104">Waits for an object to become signaled.</span></span>

<span data-ttu-id="c593b-105">In una build di debug questa funzione attiva un'asserzione se l'intervallo di timeout scade prima che l'oggetto venga segnalato.</span><span class="sxs-lookup"><span data-stu-id="c593b-105">In a debug build, this function triggers an assert if the time-out interval expires before the object is signaled.</span></span> <span data-ttu-id="c593b-106">Per impostare l'intervallo di timeout, chiamare la funzione [**DbgSetWaitTimeout**](dbgsetwaittimeout.md) .</span><span class="sxs-lookup"><span data-stu-id="c593b-106">To set the time-out interval, call the [**DbgSetWaitTimeout**](dbgsetwaittimeout.md) function.</span></span>

<span data-ttu-id="c593b-107">In una build finale questa funzione equivale alla funzione **WaitForSingleObject** con un intervallo di timeout infinito.</span><span class="sxs-lookup"><span data-stu-id="c593b-107">In a retail build, this function is equivalent to the **WaitForSingleObject** function with a time-out interval of INFINITE.</span></span>

## <a name="syntax"></a><span data-ttu-id="c593b-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c593b-108">Syntax</span></span>


```C++
DWORD DbgWaitForSingleObject(
   HANDLE h
);
```



## <a name="parameters"></a><span data-ttu-id="c593b-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="c593b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c593b-110">*h*</span><span class="sxs-lookup"><span data-stu-id="c593b-110">*h*</span></span> 
</dt> <dd>

<span data-ttu-id="c593b-111">Handle per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="c593b-111">Handle to the object.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c593b-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c593b-112">Requirements</span></span>



| <span data-ttu-id="c593b-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="c593b-113">Requirement</span></span> | <span data-ttu-id="c593b-114">Valore</span><span class="sxs-lookup"><span data-stu-id="c593b-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c593b-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c593b-115">Header</span></span><br/>  | <dl> <span data-ttu-id="c593b-116"><dt>Wxdebug. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c593b-116"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c593b-117">Libreria</span><span class="sxs-lookup"><span data-stu-id="c593b-117">Library</span></span><br/> | <dl> <span data-ttu-id="c593b-118"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="c593b-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c593b-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c593b-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c593b-120">Funzioni di debug di attesa</span><span class="sxs-lookup"><span data-stu-id="c593b-120">Wait Debugging Functions</span></span>](wait-debugging-functions.md)
</dt> </dl>

 

 




