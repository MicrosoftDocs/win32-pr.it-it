---
description: Recupera l'identificatore del thread.
ms.assetid: c2b25342-841a-46cb-862c-01761fc60363
title: Metodo CMsgThread. GetThreadID (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.GetThreadID
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0819810b9b7589fc5272c0e79f87fc2f34325f5e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328831"
---
# <a name="cmsgthreadgetthreadid-method"></a><span data-ttu-id="66c04-103">CMsgThread. GetThreadID, metodo</span><span class="sxs-lookup"><span data-stu-id="66c04-103">CMsgThread.GetThreadID method</span></span>

<span data-ttu-id="66c04-104">Recupera l'identificatore del thread.</span><span class="sxs-lookup"><span data-stu-id="66c04-104">Retrieves the thread's identifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="66c04-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="66c04-105">Syntax</span></span>


```C++
DWORD GetThreadID();
```



## <a name="parameters"></a><span data-ttu-id="66c04-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="66c04-106">Parameters</span></span>

<span data-ttu-id="66c04-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="66c04-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="66c04-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="66c04-108">Return value</span></span>

<span data-ttu-id="66c04-109">Restituisce il membro dati privato **m \_ ThreadID** .</span><span class="sxs-lookup"><span data-stu-id="66c04-109">Returns the **m\_ThreadId** private data member.</span></span>

## <a name="remarks"></a><span data-ttu-id="66c04-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="66c04-110">Remarks</span></span>

<span data-ttu-id="66c04-111">Questa funzione restituisce l'identificatore Microsoft Win32 per il thread di lavoro.</span><span class="sxs-lookup"><span data-stu-id="66c04-111">This function returns the Microsoft Win32 identifier for the worker thread.</span></span> <span data-ttu-id="66c04-112">Questa funzione membro può essere chiamata nel thread di lavoro o in un thread client.</span><span class="sxs-lookup"><span data-stu-id="66c04-112">You can call this member function on either the worker thread or a client thread.</span></span>

## <a name="requirements"></a><span data-ttu-id="66c04-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="66c04-113">Requirements</span></span>



| <span data-ttu-id="66c04-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="66c04-114">Requirement</span></span> | <span data-ttu-id="66c04-115">Valore</span><span class="sxs-lookup"><span data-stu-id="66c04-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66c04-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="66c04-116">Header</span></span><br/>  | <dl> <span data-ttu-id="66c04-117"><dt>Msgthrd. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="66c04-117"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="66c04-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="66c04-118">Library</span></span><br/> | <dl> <span data-ttu-id="66c04-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="66c04-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66c04-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="66c04-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66c04-121">**Classe CMsgThread**</span><span class="sxs-lookup"><span data-stu-id="66c04-121">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 




