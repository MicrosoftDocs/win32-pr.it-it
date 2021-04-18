---
description: Il metodo Wait si blocca fino a quando l'evento non viene segnalato o fino a quando non si verifica un timeout.
ms.assetid: bcc13723-a59b-4e8a-bfc8-eadb6facf116
title: Metodo CAMEvent. Wait (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMEvent.Wait
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0ab5bc2aabf77fb73739528e99cda7961ae87e9d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331332"
---
# <a name="cameventwait-method"></a><span data-ttu-id="689c0-103">Metodo CAMEvent. Wait</span><span class="sxs-lookup"><span data-stu-id="689c0-103">CAMEvent.Wait method</span></span>

<span data-ttu-id="689c0-104">Il `Wait` metodo si blocca fino a quando l'evento non viene segnalato o fino a quando non si verifica un timeout.</span><span class="sxs-lookup"><span data-stu-id="689c0-104">The `Wait` method blocks until the event is signaled, or until a time-out occurs.</span></span>

## <a name="syntax"></a><span data-ttu-id="689c0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="689c0-105">Syntax</span></span>


```C++
BOOL Wait(
   DWORD dwTimeout = INFINITE
);
```



## <a name="parameters"></a><span data-ttu-id="689c0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="689c0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="689c0-107">*dwTimeout*</span><span class="sxs-lookup"><span data-stu-id="689c0-107">*dwTimeout*</span></span> 
</dt> <dd>

<span data-ttu-id="689c0-108">Valore di timeout facoltativo, rappresentato in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="689c0-108">Optional time-out value, represented in milliseconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="689c0-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="689c0-109">Return value</span></span>

<span data-ttu-id="689c0-110">Restituisce **true** se l'evento viene segnalato.</span><span class="sxs-lookup"><span data-stu-id="689c0-110">Returns **TRUE** if the event is signaled.</span></span> <span data-ttu-id="689c0-111">In caso contrario, restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="689c0-111">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="689c0-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="689c0-112">Remarks</span></span>

<span data-ttu-id="689c0-113">Per gli eventi di reimpostazione automatica, l'evento viene reimpostato su uno stato non segnalato quando il metodo restituisce un risultato.</span><span class="sxs-lookup"><span data-stu-id="689c0-113">For auto-reset events, the event is reset to a nonsignaled state when this method returns.</span></span>

## <a name="requirements"></a><span data-ttu-id="689c0-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="689c0-114">Requirements</span></span>



| <span data-ttu-id="689c0-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="689c0-115">Requirement</span></span> | <span data-ttu-id="689c0-116">Valore</span><span class="sxs-lookup"><span data-stu-id="689c0-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="689c0-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="689c0-117">Header</span></span><br/>  | <dl> <span data-ttu-id="689c0-118"><dt>Wxutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="689c0-118"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="689c0-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="689c0-119">Library</span></span><br/> | <dl> <span data-ttu-id="689c0-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="689c0-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="689c0-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="689c0-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="689c0-122">**Classe CAMEvent**</span><span class="sxs-lookup"><span data-stu-id="689c0-122">**CAMEvent Class**</span></span>](camevent.md)
</dt> </dl>

 

 




