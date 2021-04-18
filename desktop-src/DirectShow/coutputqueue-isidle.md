---
description: Il metodo di inattività determina se l'oggetto è in attesa di dati.
ms.assetid: be1b5633-f9e9-497e-8b6f-5634eae91273
title: Metodo COutputQueue. IsValid (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.IsIdle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9bf8b42189e356659e74398eaa3eefeb5f771a8a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330667"
---
# <a name="coutputqueueisidle-method"></a><span data-ttu-id="92248-103">Metodo COutputQueue. IsValid</span><span class="sxs-lookup"><span data-stu-id="92248-103">COutputQueue.IsIdle method</span></span>

<span data-ttu-id="92248-104">Il `IsIdle` metodo determina se l'oggetto è in attesa di dati.</span><span class="sxs-lookup"><span data-stu-id="92248-104">The `IsIdle` method determines whether the object is waiting for data.</span></span>

## <a name="syntax"></a><span data-ttu-id="92248-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="92248-105">Syntax</span></span>


```C++
BOOL IsIdle();
```



## <a name="parameters"></a><span data-ttu-id="92248-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="92248-106">Parameters</span></span>

<span data-ttu-id="92248-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="92248-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="92248-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="92248-108">Return value</span></span>

<span data-ttu-id="92248-109">Restituisce **true** se il thread è in attesa e la matrice di esempio è vuota.</span><span class="sxs-lookup"><span data-stu-id="92248-109">Returns **TRUE** if the thread is waiting and the sample array is empty.</span></span> <span data-ttu-id="92248-110">In caso contrario, restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="92248-110">Otherwise, returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="92248-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="92248-111">Requirements</span></span>



| <span data-ttu-id="92248-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="92248-112">Requirement</span></span> | <span data-ttu-id="92248-113">Valore</span><span class="sxs-lookup"><span data-stu-id="92248-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92248-114">Intestazione</span><span class="sxs-lookup"><span data-stu-id="92248-114">Header</span></span><br/>  | <dl> <span data-ttu-id="92248-115"><dt>Outputq. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="92248-115"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="92248-116">Libreria</span><span class="sxs-lookup"><span data-stu-id="92248-116">Library</span></span><br/> | <dl> <span data-ttu-id="92248-117"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="92248-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92248-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="92248-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92248-119">**Classe COutputQueue**</span><span class="sxs-lookup"><span data-stu-id="92248-119">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




