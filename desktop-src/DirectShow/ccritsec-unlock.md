---
description: Il metodo Unlock Sblocca l'oggetto sezione critica.
ms.assetid: 61811e0e-df77-48e9-96d5-b7dff8c8db9b
title: Metodo CCritSec. Unlock (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCritSec.Unlock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ca84ce452d71d0d3111039d7a95d8f5dd3155058
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329860"
---
# <a name="ccritsecunlock-method"></a><span data-ttu-id="75f5d-103">Metodo CCritSec. Unlock</span><span class="sxs-lookup"><span data-stu-id="75f5d-103">CCritSec.Unlock method</span></span>

<span data-ttu-id="75f5d-104">Il metodo **Unlock Sblocca** l'oggetto sezione critica.</span><span class="sxs-lookup"><span data-stu-id="75f5d-104">The **Unlock** method unlocks the critical section object.</span></span>

## <a name="syntax"></a><span data-ttu-id="75f5d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="75f5d-105">Syntax</span></span>


```C++
void Unlock();
```



## <a name="parameters"></a><span data-ttu-id="75f5d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="75f5d-106">Parameters</span></span>

<span data-ttu-id="75f5d-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="75f5d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="75f5d-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="75f5d-108">Return value</span></span>

<span data-ttu-id="75f5d-109">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="75f5d-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="75f5d-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="75f5d-110">Remarks</span></span>

<span data-ttu-id="75f5d-111">Questo metodo chiama la funzione [**LeaveCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-leavecriticalsection) .</span><span class="sxs-lookup"><span data-stu-id="75f5d-111">This method calls the [**LeaveCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-leavecriticalsection) function.</span></span> <span data-ttu-id="75f5d-112">Chiamare questo metodo una volta per ogni chiamata al metodo [**CCritSec:: Lock**](ccritsec-lock.md) .</span><span class="sxs-lookup"><span data-stu-id="75f5d-112">Call this method once for each call to the [**CCritSec::Lock**](ccritsec-lock.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="75f5d-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="75f5d-113">Requirements</span></span>



| <span data-ttu-id="75f5d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="75f5d-114">Requirement</span></span> | <span data-ttu-id="75f5d-115">Valore</span><span class="sxs-lookup"><span data-stu-id="75f5d-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75f5d-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="75f5d-116">Header</span></span><br/>  | <dl> <span data-ttu-id="75f5d-117"><dt>Wxutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="75f5d-117"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="75f5d-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="75f5d-118">Library</span></span><br/> | <dl> <span data-ttu-id="75f5d-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="75f5d-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75f5d-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="75f5d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75f5d-121">**Classe CCritSec**</span><span class="sxs-lookup"><span data-stu-id="75f5d-121">**CCritSec Class**</span></span>](ccritsec.md)
</dt> </dl>

 

