---
description: Il metodo di Accodamento determina se l'oggetto utilizza un thread di lavoro per recapitare esempi.
ms.assetid: 8d26661f-6cd7-42ea-bc4b-8746d22a7ca0
title: Metodo COutputQueue. unqueued (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.IsQueued
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 47093acedb3a28d633ea2c8b0bbdbba3c1493de7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325756"
---
# <a name="coutputqueueisqueued-method"></a><span data-ttu-id="16c2e-103">Metodo COutputQueue. unqueued</span><span class="sxs-lookup"><span data-stu-id="16c2e-103">COutputQueue.IsQueued method</span></span>

<span data-ttu-id="16c2e-104">Il `IsQueued` metodo determina se l'oggetto utilizza un thread di lavoro per recapitare esempi.</span><span class="sxs-lookup"><span data-stu-id="16c2e-104">The `IsQueued` method determines whether the object is using a worker thread to deliver samples.</span></span>

## <a name="syntax"></a><span data-ttu-id="16c2e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="16c2e-105">Syntax</span></span>


```C++
BOOL IsQueued();
```



## <a name="parameters"></a><span data-ttu-id="16c2e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="16c2e-106">Parameters</span></span>

<span data-ttu-id="16c2e-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="16c2e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="16c2e-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="16c2e-108">Return value</span></span>

<span data-ttu-id="16c2e-109">Restituisce **true** se l'oggetto utilizza un thread di lavoro; in caso contrario, **false** .</span><span class="sxs-lookup"><span data-stu-id="16c2e-109">Returns **TRUE** if the object is using a worker thread, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="16c2e-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="16c2e-110">Requirements</span></span>



| <span data-ttu-id="16c2e-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="16c2e-111">Requirement</span></span> | <span data-ttu-id="16c2e-112">Valore</span><span class="sxs-lookup"><span data-stu-id="16c2e-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16c2e-113">Intestazione</span><span class="sxs-lookup"><span data-stu-id="16c2e-113">Header</span></span><br/>  | <dl> <span data-ttu-id="16c2e-114"><dt>Outputq. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="16c2e-114"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="16c2e-115">Libreria</span><span class="sxs-lookup"><span data-stu-id="16c2e-115">Library</span></span><br/> | <dl> <span data-ttu-id="16c2e-116"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="16c2e-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16c2e-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="16c2e-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16c2e-118">**Classe COutputQueue**</span><span class="sxs-lookup"><span data-stu-id="16c2e-118">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




