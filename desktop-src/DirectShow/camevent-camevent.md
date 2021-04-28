---
description: 'Costruttore CAMEvent.CAMEvent : metodo del costruttore.'
ms.assetid: 35c9ac07-8756-42b1-beeb-5f0e79466742
title: Costruttore CAMEvent.CAMEvent (Wxutil.h)
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
ms.openlocfilehash: cdd37ba72d9467c16d46b2aec3ec40c206466eaf
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096532"
---
# <a name="cameventcamevent-constructor"></a><span data-ttu-id="51826-103">Costruttore CAMEvent.CAMEvent</span><span class="sxs-lookup"><span data-stu-id="51826-103">CAMEvent.CAMEvent constructor</span></span>

<span data-ttu-id="51826-104">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="51826-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="51826-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="51826-105">Syntax</span></span>


```C++
CAMEvent(
   BOOL    fManualReset,
   HRESULT *phr
);
```



## <a name="parameters"></a><span data-ttu-id="51826-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="51826-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51826-107">*fManualReset*</span><span class="sxs-lookup"><span data-stu-id="51826-107">*fManualReset*</span></span> 
</dt> <dd>

<span data-ttu-id="51826-108">Valore booleano che specifica se l'oggetto è un evento di reimpostazione manuale o un evento di reimpostazione automatica.</span><span class="sxs-lookup"><span data-stu-id="51826-108">Boolean value that specifies whether the object is a manual-reset event or an auto-reset event.</span></span> <span data-ttu-id="51826-109">Se **TRUE,** l'oggetto è un evento di reimpostazione manuale.</span><span class="sxs-lookup"><span data-stu-id="51826-109">If **TRUE**, the object is a manual-reset event.</span></span> <span data-ttu-id="51826-110">In caso contrario, si tratta di un evento di reimpostazione automatica.</span><span class="sxs-lookup"><span data-stu-id="51826-110">Otherwise, it is an auto-reset event.</span></span>

</dd> <dt>

<span data-ttu-id="51826-111">*Phr*</span><span class="sxs-lookup"><span data-stu-id="51826-111">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="51826-112">Puntatore a un **valore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="51826-112">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="51826-113">Se il costruttore ha esito negativo, questo parametro riceve un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="51826-113">If the constructor fails, this parameter receives an error code.</span></span> <span data-ttu-id="51826-114">In questo caso, l'oggetto non è in uno stato valido.</span><span class="sxs-lookup"><span data-stu-id="51826-114">If this occurs, the object is not in a valid state.</span></span>

<span data-ttu-id="51826-115">Per compatibilità con le versioni precedenti di strmbase.lib, il valore predefinito di questo parametro è **NULL.**</span><span class="sxs-lookup"><span data-stu-id="51826-115">For backward compatibility with earlier versions of strmbase.lib, this parameter defaults to **NULL**.</span></span> <span data-ttu-id="51826-116">È tuttavia preferibile passare un valore non **NULL,** in modo che il chiamante possa controllare lo stato dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="51826-116">However, passing a non-**NULL** value is preferred, so that the caller can check the status of the object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="51826-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="51826-117">Remarks</span></span>

<span data-ttu-id="51826-118">L'evento inizia in uno stato non firmato.</span><span class="sxs-lookup"><span data-stu-id="51826-118">The event begins in a nonsignaled state.</span></span>

<span data-ttu-id="51826-119">Con un evento di reimpostazione automatica, il [**metodo CAMEvent::Wait**](camevent-wait.md) reimposta l'evento su nonsignaled quando il metodo viene restituito.</span><span class="sxs-lookup"><span data-stu-id="51826-119">With an auto-reset event, the [**CAMEvent::Wait**](camevent-wait.md) method resets the event to nonsignaled when the method returns.</span></span> <span data-ttu-id="51826-120">Con un evento di reimpostazione manuale, l'evento rimane segnalato fino a quando non si chiama il [**metodo CAMEvent::Reset.**](camevent-reset.md)</span><span class="sxs-lookup"><span data-stu-id="51826-120">With a manual-reset event, the event remains signaled until you call the [**CAMEvent::Reset**](camevent-reset.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="51826-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="51826-121">Requirements</span></span>



| <span data-ttu-id="51826-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="51826-122">Requirement</span></span> | <span data-ttu-id="51826-123">Valore</span><span class="sxs-lookup"><span data-stu-id="51826-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51826-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="51826-124">Header</span></span><br/>  | <dl> <span data-ttu-id="51826-125"><dt>Wxutil.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="51826-125"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="51826-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="51826-126">Library</span></span><br/> | <dl> <span data-ttu-id="51826-127"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="51826-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51826-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="51826-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51826-129">**Classe CAMEvent**</span><span class="sxs-lookup"><span data-stu-id="51826-129">**CAMEvent Class**</span></span>](camevent.md)
</dt> </dl>

 

 




