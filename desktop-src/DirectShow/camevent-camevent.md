---
description: Metodo del costruttore.
ms.assetid: 35c9ac07-8756-42b1-beeb-5f0e79466742
title: Costruttore CAMEvent. CAMEvent (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMEvent.CAMEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a01d9d1f592675f58d19e81b800c966dddaca1c3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324429"
---
# <a name="cameventcamevent-constructor"></a><span data-ttu-id="ac985-103">Costruttore CAMEvent. CAMEvent</span><span class="sxs-lookup"><span data-stu-id="ac985-103">CAMEvent.CAMEvent constructor</span></span>

<span data-ttu-id="ac985-104">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="ac985-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac985-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ac985-105">Syntax</span></span>


```C++
CAMEvent(
   BOOL    fManualReset,
   HRESULT *phr
);
```



## <a name="parameters"></a><span data-ttu-id="ac985-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ac985-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac985-107">*fManualReset*</span><span class="sxs-lookup"><span data-stu-id="ac985-107">*fManualReset*</span></span> 
</dt> <dd>

<span data-ttu-id="ac985-108">Valore booleano che specifica se l'oggetto è un evento di reimpostazione manuale o un evento di reimpostazione automatica.</span><span class="sxs-lookup"><span data-stu-id="ac985-108">Boolean value that specifies whether the object is a manual-reset event or an auto-reset event.</span></span> <span data-ttu-id="ac985-109">Se **true**, l'oggetto è un evento di reimpostazione manuale.</span><span class="sxs-lookup"><span data-stu-id="ac985-109">If **TRUE**, the object is a manual-reset event.</span></span> <span data-ttu-id="ac985-110">In caso contrario, si tratta di un evento di reimpostazione automatica.</span><span class="sxs-lookup"><span data-stu-id="ac985-110">Otherwise, it is an auto-reset event.</span></span>

</dd> <dt>

<span data-ttu-id="ac985-111">*PHR*</span><span class="sxs-lookup"><span data-stu-id="ac985-111">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="ac985-112">Puntatore a un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ac985-112">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="ac985-113">Se il costruttore ha esito negativo, questo parametro riceve un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="ac985-113">If the constructor fails, this parameter receives an error code.</span></span> <span data-ttu-id="ac985-114">In tal caso, lo stato dell'oggetto non è valido.</span><span class="sxs-lookup"><span data-stu-id="ac985-114">If this occurs, the object is not in a valid state.</span></span>

<span data-ttu-id="ac985-115">Per la compatibilità con le versioni precedenti di strmbase. lib, il valore predefinito di questo parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="ac985-115">For backward compatibility with earlier versions of strmbase.lib, this parameter defaults to **NULL**.</span></span> <span data-ttu-id="ac985-116">Tuttavia, è preferibile passare un valore non **null** , in modo che il chiamante possa controllare lo stato dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ac985-116">However, passing a non-**NULL** value is preferred, so that the caller can check the status of the object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ac985-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="ac985-117">Remarks</span></span>

<span data-ttu-id="ac985-118">L'evento inizia con uno stato non segnalato.</span><span class="sxs-lookup"><span data-stu-id="ac985-118">The event begins in a nonsignaled state.</span></span>

<span data-ttu-id="ac985-119">Con un evento di reimpostazione automatica, il metodo [**CAMEvent:: wait**](camevent-wait.md) Reimposta l'evento su non segnalato quando il metodo restituisce un risultato.</span><span class="sxs-lookup"><span data-stu-id="ac985-119">With an auto-reset event, the [**CAMEvent::Wait**](camevent-wait.md) method resets the event to nonsignaled when the method returns.</span></span> <span data-ttu-id="ac985-120">Con un evento di reimpostazione manuale, l'evento rimane segnalato fino a quando non viene chiamato il metodo [**CAMEvent:: Reset**](camevent-reset.md) .</span><span class="sxs-lookup"><span data-stu-id="ac985-120">With a manual-reset event, the event remains signaled until you call the [**CAMEvent::Reset**](camevent-reset.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac985-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ac985-121">Requirements</span></span>



| <span data-ttu-id="ac985-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac985-122">Requirement</span></span> | <span data-ttu-id="ac985-123">Valore</span><span class="sxs-lookup"><span data-stu-id="ac985-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac985-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ac985-124">Header</span></span><br/>  | <dl> <span data-ttu-id="ac985-125"><dt>Wxutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ac985-125"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="ac985-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="ac985-126">Library</span></span><br/> | <dl> <span data-ttu-id="ac985-127"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ac985-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac985-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ac985-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac985-129">**Classe CAMEvent**</span><span class="sxs-lookup"><span data-stu-id="ac985-129">**CAMEvent Class**</span></span>](camevent.md)
</dt> </dl>

 

 




