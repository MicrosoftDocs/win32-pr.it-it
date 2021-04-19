---
description: "Usa la funzione ResumeThread di Microsoft Win32 per continuare l'operazione del thread di lavoro dopo una chiamata precedente alla funzione membro CMsgThread:: SuspendThread."
ms.assetid: 5c94a079-5c74-4024-8fb0-71c7ef9c7e73
title: Metodo CMsgThread. ResumeThread (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.ResumeThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3e0a20bb60f4a10a06ef50f58c449496cae8050d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333318"
---
# <a name="cmsgthreadresumethread-method"></a><span data-ttu-id="4652f-103">CMsgThread. ResumeThread, metodo</span><span class="sxs-lookup"><span data-stu-id="4652f-103">CMsgThread.ResumeThread method</span></span>

<span data-ttu-id="4652f-104">Usa la funzione **ResumeThread** di Microsoft Win32 per continuare l'operazione del thread di lavoro dopo una chiamata precedente alla funzione membro [**CMsgThread:: SuspendThread**](cmsgthread-suspendthread.md) .</span><span class="sxs-lookup"><span data-stu-id="4652f-104">Uses the Microsoft Win32 **ResumeThread** function to continue the operation of the worker thread after a previous call to the [**CMsgThread::SuspendThread**](cmsgthread-suspendthread.md) member function.</span></span>

## <a name="syntax"></a><span data-ttu-id="4652f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4652f-105">Syntax</span></span>


```C++
DWORD ResumeThread();
```



## <a name="parameters"></a><span data-ttu-id="4652f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4652f-106">Parameters</span></span>

<span data-ttu-id="4652f-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="4652f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4652f-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4652f-108">Return value</span></span>

<span data-ttu-id="4652f-109">Se la funzione membro ha esito positivo, il valore restituito è il conteggio di sospensione precedente del thread.</span><span class="sxs-lookup"><span data-stu-id="4652f-109">If the member function succeeds, the return value is the previous suspend count of the thread.</span></span> <span data-ttu-id="4652f-110">Se la funzione membro ha esito negativo, il valore restituito è 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="4652f-110">If the member function fails, the return value is 0xFFFFFFFF.</span></span> <span data-ttu-id="4652f-111">Per ottenere informazioni estese sull'errore, chiamare la funzione **GetLastError** di Microsoft Win32.</span><span class="sxs-lookup"><span data-stu-id="4652f-111">To obtain extended error information, call the Microsoft Win32 **GetLastError** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="4652f-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4652f-112">Requirements</span></span>



| <span data-ttu-id="4652f-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="4652f-113">Requirement</span></span> | <span data-ttu-id="4652f-114">Valore</span><span class="sxs-lookup"><span data-stu-id="4652f-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4652f-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4652f-115">Header</span></span><br/>  | <dl> <span data-ttu-id="4652f-116"><dt>Msgthrd. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4652f-116"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4652f-117">Libreria</span><span class="sxs-lookup"><span data-stu-id="4652f-117">Library</span></span><br/> | <dl> <span data-ttu-id="4652f-118"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="4652f-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4652f-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4652f-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4652f-120">**Classe CMsgThread**</span><span class="sxs-lookup"><span data-stu-id="4652f-120">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 




