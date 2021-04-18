---
description: Evento segnalato quando il pin si blocca correttamente oppure l'utente annulla un blocco in sospeso.
ms.assetid: 699bb7f7-e4f7-47c3-bbb1-0bc6556651ae
title: 'Membro CDynamicOutputPin:: m_hNotifyCallerPinBlockedEvent (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_hNotifyCallerPinBlockedEvent
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3e28aa890e15602376b9500243a89e8f0e3d3bb6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325193"
---
# <a name="cdynamicoutputpinm_hnotifycallerpinblockedevent-member"></a><span data-ttu-id="4c23f-103">Membro hNotifyCallerPinBlockedEvent di CDynamicOutputPin:: m \_</span><span class="sxs-lookup"><span data-stu-id="4c23f-103">CDynamicOutputPin::m\_hNotifyCallerPinBlockedEvent member</span></span>

<span data-ttu-id="4c23f-104">Evento segnalato quando il pin si blocca correttamente oppure l'utente annulla un blocco in sospeso.</span><span class="sxs-lookup"><span data-stu-id="4c23f-104">Event that is signaled when the pin successfully blocks, or the user cancels a pending block.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c23f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4c23f-105">Syntax</span></span>


```C++
HANDLE m_hNotifyCallerPinBlockedEvent;
```



## <a name="remarks"></a><span data-ttu-id="4c23f-106">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="4c23f-106">Remarks</span></span>

<span data-ttu-id="4c23f-107">Prima di accedere a questa variabile, conservare la sezione [**CDynamicOutputPin:: m \_ BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) critical.</span><span class="sxs-lookup"><span data-stu-id="4c23f-107">Before accessing this variable, hold the [**CDynamicOutputPin::m\_BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) critical section.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c23f-108">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4c23f-108">Requirements</span></span>



| <span data-ttu-id="4c23f-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c23f-109">Requirement</span></span> | <span data-ttu-id="4c23f-110">Valore</span><span class="sxs-lookup"><span data-stu-id="4c23f-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c23f-111">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4c23f-111">Header</span></span><br/>  | <dl> <span data-ttu-id="4c23f-112"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4c23f-112"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="4c23f-113">Libreria</span><span class="sxs-lookup"><span data-stu-id="4c23f-113">Library</span></span><br/> | <dl> <span data-ttu-id="4c23f-114"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="4c23f-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c23f-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4c23f-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c23f-116">**Classe CDynamicOutputPin**</span><span class="sxs-lookup"><span data-stu-id="4c23f-116">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




