---
description: Usa la funzione GetThreadPriority di Microsoft Win32 per recuperare la priorità del thread di lavoro corrente.
ms.assetid: a9db15cf-2c22-4c61-a817-20af5ade434b
title: Metodo CMsgThread. GetThreadPriority (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.GetThreadPriority
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3c9716b43ccc314ba487d982e0c1685960593f95
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325927"
---
# <a name="cmsgthreadgetthreadpriority-method"></a><span data-ttu-id="42bd5-103">CMsgThread. GetThreadPriority, metodo</span><span class="sxs-lookup"><span data-stu-id="42bd5-103">CMsgThread.GetThreadPriority method</span></span>

<span data-ttu-id="42bd5-104">Usa la funzione **GetThreadPriority** di Microsoft Win32 per recuperare la priorità del thread di lavoro corrente.</span><span class="sxs-lookup"><span data-stu-id="42bd5-104">Uses the Microsoft Win32 **GetThreadPriority** function to retrieve the priority of the current worker thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="42bd5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="42bd5-105">Syntax</span></span>


```C++
int GetThreadPriority();
```



## <a name="parameters"></a><span data-ttu-id="42bd5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="42bd5-106">Parameters</span></span>

<span data-ttu-id="42bd5-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="42bd5-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="42bd5-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="42bd5-108">Return value</span></span>

<span data-ttu-id="42bd5-109">Restituisce la priorità del thread come Integer.</span><span class="sxs-lookup"><span data-stu-id="42bd5-109">Returns the thread priority as an integer.</span></span>

## <a name="requirements"></a><span data-ttu-id="42bd5-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="42bd5-110">Requirements</span></span>



| <span data-ttu-id="42bd5-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="42bd5-111">Requirement</span></span> | <span data-ttu-id="42bd5-112">Valore</span><span class="sxs-lookup"><span data-stu-id="42bd5-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42bd5-113">Intestazione</span><span class="sxs-lookup"><span data-stu-id="42bd5-113">Header</span></span><br/>  | <dl> <span data-ttu-id="42bd5-114"><dt>Msgthrd. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="42bd5-114"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="42bd5-115">Libreria</span><span class="sxs-lookup"><span data-stu-id="42bd5-115">Library</span></span><br/> | <dl> <span data-ttu-id="42bd5-116"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="42bd5-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42bd5-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="42bd5-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42bd5-118">**Classe CMsgThread**</span><span class="sxs-lookup"><span data-stu-id="42bd5-118">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 




