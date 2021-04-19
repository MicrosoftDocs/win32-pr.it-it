---
description: La funzione WaitDispatchingMessages attende che un oggetto venga segnalato, durante l'invio dei messaggi della finestra.
ms.assetid: d15f6736-d141-47a3-b767-fbf774982fb4
title: Funzione WaitDispatchingMessages (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WaitDispatchingMessages
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9e509a081243f28293dc2d8abf8311f69eaf9a44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326776"
---
# <a name="waitdispatchingmessages-function"></a><span data-ttu-id="111d6-103">WaitDispatchingMessages (funzione)</span><span class="sxs-lookup"><span data-stu-id="111d6-103">WaitDispatchingMessages function</span></span>

<span data-ttu-id="111d6-104">La `WaitDispatchingMessages` funzione attende la segnalazione di un oggetto, durante l'invio dei messaggi della finestra.</span><span class="sxs-lookup"><span data-stu-id="111d6-104">The `WaitDispatchingMessages` function waits for an object to be signaled, while dispatching window messages.</span></span>

## <a name="syntax"></a><span data-ttu-id="111d6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="111d6-105">Syntax</span></span>


```C++
DWORD WINAPI WaitDispatchingMessages(
   HANDLE hObject,
   DWORD  dwWait,
   HWND   hwnd = NULL,
   UINT   uMsg = 0,
   HANDLE hEvent = NULL
);
```



## <a name="parameters"></a><span data-ttu-id="111d6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="111d6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="111d6-107">*hObject*</span><span class="sxs-lookup"><span data-stu-id="111d6-107">*hObject*</span></span> 
</dt> <dd>

<span data-ttu-id="111d6-108">Handle dell'oggetto da attendere.</span><span class="sxs-lookup"><span data-stu-id="111d6-108">Handle of the object to wait for.</span></span>

</dd> <dt>

<span data-ttu-id="111d6-109">*dwWait*</span><span class="sxs-lookup"><span data-stu-id="111d6-109">*dwWait*</span></span> 
</dt> <dd>

<span data-ttu-id="111d6-110">Intervallo di timeout, in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="111d6-110">Time-out interval, in milliseconds.</span></span>

</dd> <dt>

<span data-ttu-id="111d6-111">*HWND*</span><span class="sxs-lookup"><span data-stu-id="111d6-111">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="111d6-112">Handle facoltativo per una finestra.</span><span class="sxs-lookup"><span data-stu-id="111d6-112">Optional handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="111d6-113">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="111d6-113">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="111d6-114">Messaggio finestra facoltativo che specifica un messaggio da inviare.</span><span class="sxs-lookup"><span data-stu-id="111d6-114">Optional window message, specifying a message to dispatch.</span></span>

</dd> <dt>

<span data-ttu-id="111d6-115">*hEvent*</span><span class="sxs-lookup"><span data-stu-id="111d6-115">*hEvent*</span></span> 
</dt> <dd>

<span data-ttu-id="111d6-116">Handle facoltativo per un evento da attendere.</span><span class="sxs-lookup"><span data-stu-id="111d6-116">Optional handle to an event to wait for.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="111d6-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="111d6-117">Return value</span></span>

<span data-ttu-id="111d6-118">Restituisce il valore dalla funzione **WaitForMultipleObjects** .</span><span class="sxs-lookup"><span data-stu-id="111d6-118">Returns the value from the **WaitForMultipleObjects** function.</span></span>

## <a name="remarks"></a><span data-ttu-id="111d6-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="111d6-119">Remarks</span></span>

<span data-ttu-id="111d6-120">Se un oggetto è proprietario di una finestra, deve inviare messaggi della finestra durante l'attesa.</span><span class="sxs-lookup"><span data-stu-id="111d6-120">If an object owns a window, it should dispatch window messages while waiting.</span></span> <span data-ttu-id="111d6-121">Questa funzione consente all'oggetto di attendere un evento, un semaforo o un altro oggetto di esclusione reciproca durante l'invio dei messaggi.</span><span class="sxs-lookup"><span data-stu-id="111d6-121">This function enables the object to wait for an event, semaphore, or other mutual exclusion object while dispatching messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="111d6-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="111d6-122">Requirements</span></span>



| <span data-ttu-id="111d6-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="111d6-123">Requirement</span></span> | <span data-ttu-id="111d6-124">Valore</span><span class="sxs-lookup"><span data-stu-id="111d6-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="111d6-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="111d6-125">Header</span></span><br/>  | <dl> <span data-ttu-id="111d6-126"><dt>Wxutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="111d6-126"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="111d6-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="111d6-127">Library</span></span><br/> | <dl> <span data-ttu-id="111d6-128"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="111d6-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="111d6-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="111d6-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="111d6-130">Funzioni helper varie</span><span class="sxs-lookup"><span data-stu-id="111d6-130">Miscellaneous Helper Functions</span></span>](miscellaneous-helper-functions.md)
</dt> </dl>

 

 




