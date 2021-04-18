---
description: Il metodo check Controlla se l'evento è impostato, senza bloccarsi.
ms.assetid: b8e55798-fd8e-4442-bc35-08887d8a3129
title: Metodo CAMEvent. check (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMEvent.Check
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1a112d1b9484acb4d7e9cc2992b8dee629f40e23
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324423"
---
# <a name="cameventcheck-method"></a><span data-ttu-id="9f457-103">Metodo CAMEvent. check</span><span class="sxs-lookup"><span data-stu-id="9f457-103">CAMEvent.Check method</span></span>

<span data-ttu-id="9f457-104">Il `Check` metodo controlla se l'evento è impostato, senza bloccarsi.</span><span class="sxs-lookup"><span data-stu-id="9f457-104">The `Check` method checks whether the event is set, without blocking.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f457-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9f457-105">Syntax</span></span>


```C++
BOOL Check();
```



## <a name="parameters"></a><span data-ttu-id="9f457-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9f457-106">Parameters</span></span>

<span data-ttu-id="9f457-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="9f457-107">This method has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f457-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="9f457-108">Remarks</span></span>

<span data-ttu-id="9f457-109">Restituisce **true** se l'evento è impostato o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="9f457-109">Returns **TRUE** if the event is set, or **FALSE** otherwise.</span></span> <span data-ttu-id="9f457-110">Questo metodo chiama il metodo [**CAMEvent:: wait**](camevent-wait.md) con un timeout di zero.</span><span class="sxs-lookup"><span data-stu-id="9f457-110">This method calls the [**CAMEvent::Wait**](camevent-wait.md) method with a time-out of zero.</span></span> <span data-ttu-id="9f457-111">Se l'oggetto è un evento di reimpostazione automatica, questo metodo reimposta l'evento.</span><span class="sxs-lookup"><span data-stu-id="9f457-111">If the object is an auto-reset event, this method resets the event.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f457-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9f457-112">Requirements</span></span>



| <span data-ttu-id="9f457-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f457-113">Requirement</span></span> | <span data-ttu-id="9f457-114">Valore</span><span class="sxs-lookup"><span data-stu-id="9f457-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f457-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9f457-115">Header</span></span><br/>  | <dl> <span data-ttu-id="9f457-116"><dt>Wxutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9f457-116"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="9f457-117">Libreria</span><span class="sxs-lookup"><span data-stu-id="9f457-117">Library</span></span><br/> | <dl> <span data-ttu-id="9f457-118"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="9f457-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f457-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9f457-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f457-120">**Classe CAMEvent**</span><span class="sxs-lookup"><span data-stu-id="9f457-120">**CAMEvent Class**</span></span>](camevent.md)
</dt> </dl>

 

 




