---
description: Il metodo Lock blocca l'oggetto sezione critica.
ms.assetid: b08be5ec-3f02-4ed8-8791-20e4d2a0c55f
title: Metodo CCritSec. Lock (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCritSec.Lock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 19599e9cd3c3b8fa913bd07d22fe743aaaa1382f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333732"
---
# <a name="ccritseclock-method"></a><span data-ttu-id="28ee6-103">Metodo CCritSec. Lock</span><span class="sxs-lookup"><span data-stu-id="28ee6-103">CCritSec.Lock method</span></span>

<span data-ttu-id="28ee6-104">Il metodo **Lock** blocca l'oggetto sezione critica.</span><span class="sxs-lookup"><span data-stu-id="28ee6-104">The **Lock** method locks the critical section object.</span></span>

## <a name="syntax"></a><span data-ttu-id="28ee6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="28ee6-105">Syntax</span></span>


```C++
void Lock();
```



## <a name="parameters"></a><span data-ttu-id="28ee6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="28ee6-106">Parameters</span></span>

<span data-ttu-id="28ee6-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="28ee6-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="28ee6-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="28ee6-108">Return value</span></span>

<span data-ttu-id="28ee6-109">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="28ee6-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="28ee6-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="28ee6-110">Remarks</span></span>

<span data-ttu-id="28ee6-111">Questo metodo chiama la funzione [**EnterCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-entercriticalsection) .</span><span class="sxs-lookup"><span data-stu-id="28ee6-111">This method calls the [**EnterCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-entercriticalsection) function.</span></span>

<span data-ttu-id="28ee6-112">Chiamare la funzione membro [**CCritSec:: Unlock**](ccritsec-unlock.md) per sbloccare la sezione critica.</span><span class="sxs-lookup"><span data-stu-id="28ee6-112">Call the [**CCritSec::Unlock**](ccritsec-unlock.md) member function to unlock the critical section.</span></span> <span data-ttu-id="28ee6-113">È possibile eseguire più chiamate al metodo **Lock** sullo stesso thread. Assicurarsi di chiamare **Unlock** un numero di volte corrispondente.</span><span class="sxs-lookup"><span data-stu-id="28ee6-113">You can make multiple calls to the **Lock** method on the same thread; be sure to call **Unlock** a corresponding number of times.</span></span>

<span data-ttu-id="28ee6-114">Se l'oggetto è già bloccato da un altro thread, il metodo **CCritSec:: Lock** si blocca fino a quando l'oggetto non viene rilasciato o fino a quando non si verifica un'eccezione di deadlock possibile.</span><span class="sxs-lookup"><span data-stu-id="28ee6-114">If the object is already locked by another thread, the **CCritSec::Lock** method blocks until the object is released, or until a possible-deadlock exception occurs.</span></span>

## <a name="requirements"></a><span data-ttu-id="28ee6-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="28ee6-115">Requirements</span></span>



| <span data-ttu-id="28ee6-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="28ee6-116">Requirement</span></span> | <span data-ttu-id="28ee6-117">Valore</span><span class="sxs-lookup"><span data-stu-id="28ee6-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28ee6-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="28ee6-118">Header</span></span><br/>  | <dl> <span data-ttu-id="28ee6-119"><dt>Wxutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="28ee6-119"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="28ee6-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="28ee6-120">Library</span></span><br/> | <dl> <span data-ttu-id="28ee6-121"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="28ee6-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28ee6-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="28ee6-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28ee6-123">**Classe CCritSec**</span><span class="sxs-lookup"><span data-stu-id="28ee6-123">**CCritSec Class**</span></span>](ccritsec.md)
</dt> </dl>

 

