---
description: Attende la segnalazione di qualsiasi (o tutti) degli oggetti specificati.
ms.assetid: e60c98b6-a4d2-40de-8297-727404e3c387
title: Funzione DbgWaitForMultipleObjects (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgWaitForMultipleObjects
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0e555afb4e6a82500876f11e6d1275e7de027f7e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333271"
---
# <a name="dbgwaitformultipleobjects-function"></a><span data-ttu-id="86991-103">DbgWaitForMultipleObjects (funzione)</span><span class="sxs-lookup"><span data-stu-id="86991-103">DbgWaitForMultipleObjects function</span></span>

<span data-ttu-id="86991-104">Attende la segnalazione di qualsiasi (o tutti) degli oggetti specificati.</span><span class="sxs-lookup"><span data-stu-id="86991-104">Waits for any (or all) of the specified objects to be signaled.</span></span>

<span data-ttu-id="86991-105">In una build di debug questa funzione attiva un'asserzione se l'intervallo di timeout scade prima che gli oggetti vengano segnalati.</span><span class="sxs-lookup"><span data-stu-id="86991-105">In a debug build, this function triggers an assert if the time-out interval expires before the objects are signaled.</span></span> <span data-ttu-id="86991-106">Per impostare l'intervallo di timeout, chiamare la funzione [**DbgSetWaitTimeout**](dbgsetwaittimeout.md) .</span><span class="sxs-lookup"><span data-stu-id="86991-106">To set the time-out interval, call the [**DbgSetWaitTimeout**](dbgsetwaittimeout.md) function.</span></span>

<span data-ttu-id="86991-107">In una build finale questa funzione equivale alla funzione **WaitForMultipleObjects** con un intervallo di timeout infinito.</span><span class="sxs-lookup"><span data-stu-id="86991-107">In a retail build, this function is equivalent to the **WaitForMultipleObjects** function with a time-out interval of INFINITE.</span></span>

## <a name="syntax"></a><span data-ttu-id="86991-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="86991-108">Syntax</span></span>


```C++
DWORD DbgWaitForMultipleObjects(
   DWORD         nCount,
   CONST HANDLE  *lpHandles,
   BOOL          bWaitAll
);
```



## <a name="parameters"></a><span data-ttu-id="86991-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="86991-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86991-110">*nCount*</span><span class="sxs-lookup"><span data-stu-id="86991-110">*nCount*</span></span> 
</dt> <dd>

<span data-ttu-id="86991-111">Numero di oggetti.</span><span class="sxs-lookup"><span data-stu-id="86991-111">Number of objects.</span></span>

</dd> <dt>

<span data-ttu-id="86991-112">*lpHandles*</span><span class="sxs-lookup"><span data-stu-id="86991-112">*lpHandles*</span></span> 
</dt> <dd>

<span data-ttu-id="86991-113">Matrice di handle per gli oggetti di dimensioni *nCount*.</span><span class="sxs-lookup"><span data-stu-id="86991-113">Array of handles to objects, of size *nCount*.</span></span>

</dd> <dt>

<span data-ttu-id="86991-114">*bWaitAll*</span><span class="sxs-lookup"><span data-stu-id="86991-114">*bWaitAll*</span></span> 
</dt> <dd>

<span data-ttu-id="86991-115">Valore booleano che specifica se attendere tutti gli oggetti.</span><span class="sxs-lookup"><span data-stu-id="86991-115">Boolean value that specifies whether to wait for all of the objects.</span></span> <span data-ttu-id="86991-116">Se **true**, la funzione attende che tutti gli oggetti vengano segnalati.</span><span class="sxs-lookup"><span data-stu-id="86991-116">If **TRUE**, the function waits for all of the objects to be signaled.</span></span> <span data-ttu-id="86991-117">In caso contrario, attende che venga segnalato almeno un oggetto.</span><span class="sxs-lookup"><span data-stu-id="86991-117">Otherwise, it waits for at least one object to be signaled.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="86991-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="86991-118">Requirements</span></span>



| <span data-ttu-id="86991-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="86991-119">Requirement</span></span> | <span data-ttu-id="86991-120">Valore</span><span class="sxs-lookup"><span data-stu-id="86991-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86991-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="86991-121">Header</span></span><br/>  | <dl> <span data-ttu-id="86991-122"><dt>Wxdebug. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="86991-122"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="86991-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="86991-123">Library</span></span><br/> | <dl> <span data-ttu-id="86991-124"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="86991-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86991-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="86991-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86991-126">Funzioni di debug di attesa</span><span class="sxs-lookup"><span data-stu-id="86991-126">Wait Debugging Functions</span></span>](wait-debugging-functions.md)
</dt> </dl>

 

 




