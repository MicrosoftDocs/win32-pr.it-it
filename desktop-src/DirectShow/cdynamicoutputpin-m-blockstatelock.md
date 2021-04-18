---
description: Sezione critica che protegge lo stato di blocco.
ms.assetid: 6d20cf4c-2c27-41e6-8d01-6cb5e3876a38
title: 'Membro CDynamicOutputPin:: m_BlockStateLock (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_BlockStateLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 56d9175342218e8b82698fe9b89d15937d6913e1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327931"
---
# <a name="cdynamicoutputpinm_blockstatelock-member"></a><span data-ttu-id="98151-103">Membro BlockStateLock di CDynamicOutputPin:: m \_</span><span class="sxs-lookup"><span data-stu-id="98151-103">CDynamicOutputPin::m\_BlockStateLock member</span></span>

<span data-ttu-id="98151-104">Sezione critica che protegge lo stato di blocco.</span><span class="sxs-lookup"><span data-stu-id="98151-104">Critical section that protects the blocking state.</span></span>

## <a name="syntax"></a><span data-ttu-id="98151-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="98151-105">Syntax</span></span>


```C++
CCritSec m_BlockStateLock;
```



## <a name="remarks"></a><span data-ttu-id="98151-106">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="98151-106">Remarks</span></span>

<span data-ttu-id="98151-107">Prima di usare una delle seguenti variabili membro, mantenere questa sezione critica:</span><span class="sxs-lookup"><span data-stu-id="98151-107">Hold this critical section before using any of the following member variables:</span></span>

-   [<span data-ttu-id="98151-108">**CDynamicOutputPin:: m \_ BlockState**</span><span class="sxs-lookup"><span data-stu-id="98151-108">**CDynamicOutputPin::m\_BlockState**</span></span>](cdynamicoutputpin-m-blockstate.md)
-   [<span data-ttu-id="98151-109">**CDynamicOutputPin:: m \_ dwBlockCallerThreadID**</span><span class="sxs-lookup"><span data-stu-id="98151-109">**CDynamicOutputPin::m\_dwBlockCallerThreadID**</span></span>](cdynamicoutputpin-m-dwblockcallerthreadid.md)
-   [<span data-ttu-id="98151-110">**CDynamicOutputPin:: m \_ dwNumOutstandingOutputPinUsers**</span><span class="sxs-lookup"><span data-stu-id="98151-110">**CDynamicOutputPin::m\_dwNumOutstandingOutputPinUsers**</span></span>](cdynamicoutputpin-m-dwnumoutstandingoutputpinusers.md)
-   [<span data-ttu-id="98151-111">**CDynamicOutputPin:: m \_ hNotifyCallerPinBlockedEvent**</span><span class="sxs-lookup"><span data-stu-id="98151-111">**CDynamicOutputPin::m\_hNotifyCallerPinBlockedEvent**</span></span>](cdynamicoutputpin-m-hnotifycallerpinblockedevent.md)

## <a name="requirements"></a><span data-ttu-id="98151-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="98151-112">Requirements</span></span>



| <span data-ttu-id="98151-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="98151-113">Requirement</span></span> | <span data-ttu-id="98151-114">Valore</span><span class="sxs-lookup"><span data-stu-id="98151-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98151-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="98151-115">Header</span></span><br/>  | <dl> <span data-ttu-id="98151-116"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="98151-116"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="98151-117">Libreria</span><span class="sxs-lookup"><span data-stu-id="98151-117">Library</span></span><br/> | <dl> <span data-ttu-id="98151-118"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="98151-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98151-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="98151-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98151-120">**Classe CDynamicOutputPin**</span><span class="sxs-lookup"><span data-stu-id="98151-120">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




