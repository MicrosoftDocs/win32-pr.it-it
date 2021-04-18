---
description: Il metodo OnWaitEnd viene chiamato al termine di un tempo di attesa.
ms.assetid: 283627bb-599c-4711-abc4-b5f92dfd29a5
title: Metodo CBaseVideoRenderer. OnWaitEnd (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnWaitEnd
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 36377565556a759c9268ef1bf31ff7774933ccc2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325365"
---
# <a name="cbasevideorendereronwaitend-method"></a><span data-ttu-id="91332-103">CBaseVideoRenderer. OnWaitEnd, metodo</span><span class="sxs-lookup"><span data-stu-id="91332-103">CBaseVideoRenderer.OnWaitEnd method</span></span>

<span data-ttu-id="91332-104">Il metodo OnWaitEnd viene chiamato al termine di un tempo di attesa.</span><span class="sxs-lookup"><span data-stu-id="91332-104">The OnWaitEnd method is called when a wait time ends.</span></span>

## <a name="syntax"></a><span data-ttu-id="91332-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="91332-105">Syntax</span></span>


```C++
void OnWaitEnd();
```



## <a name="parameters"></a><span data-ttu-id="91332-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="91332-106">Parameters</span></span>

<span data-ttu-id="91332-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="91332-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="91332-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="91332-108">Return value</span></span>

<span data-ttu-id="91332-109">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="91332-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="91332-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="91332-110">Remarks</span></span>

<span data-ttu-id="91332-111">Questa funzione membro esegue solo la registrazione delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="91332-111">This member function does only performance logging.</span></span> <span data-ttu-id="91332-112">Viene chiamato quando il thread viene risvegliato dall'attesa nella finestra o quando l'esempio successivo è dovuto al rendering.</span><span class="sxs-lookup"><span data-stu-id="91332-112">It is called when the thread is awoken from waiting in the window, or when the next sample is due to be rendered.</span></span> <span data-ttu-id="91332-113">Potrebbe essere usato per raccogliere informazioni che controllano la sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="91332-113">It could eventually be used to gather information that controls synchronization.</span></span>

## <a name="requirements"></a><span data-ttu-id="91332-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="91332-114">Requirements</span></span>



| <span data-ttu-id="91332-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="91332-115">Requirement</span></span> | <span data-ttu-id="91332-116">Valore</span><span class="sxs-lookup"><span data-stu-id="91332-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91332-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="91332-117">Header</span></span><br/>  | <dl> <span data-ttu-id="91332-118"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="91332-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="91332-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="91332-119">Library</span></span><br/> | <dl> <span data-ttu-id="91332-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="91332-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91332-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="91332-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91332-122">**Classe CBaseVideoRenderer**</span><span class="sxs-lookup"><span data-stu-id="91332-122">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




