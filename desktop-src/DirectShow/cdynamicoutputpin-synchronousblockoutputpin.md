---
description: Il metodo SynchronousBlockOutputPin blocca il PIN. non restituisce alcun risultato finché il PIN non viene bloccato.
ms.assetid: 10fdb788-bc72-4eda-b60b-af83f954d689
title: Metodo CDynamicOutputPin. SynchronousBlockOutputPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.SynchronousBlockOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7fff1a0a1f093b97d07c74d7916ef2a7511d0e16
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333079"
---
# <a name="cdynamicoutputpinsynchronousblockoutputpin-method"></a><span data-ttu-id="0aab5-103">CDynamicOutputPin. SynchronousBlockOutputPin, metodo</span><span class="sxs-lookup"><span data-stu-id="0aab5-103">CDynamicOutputPin.SynchronousBlockOutputPin method</span></span>

<span data-ttu-id="0aab5-104">Il `SynchronousBlockOutputPin` metodo blocca il PIN. non restituisce alcun risultato finché il PIN non viene bloccato.</span><span class="sxs-lookup"><span data-stu-id="0aab5-104">The `SynchronousBlockOutputPin` method blocks the pin; does not return until the pin is blocked.</span></span>

## <a name="syntax"></a><span data-ttu-id="0aab5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0aab5-105">Syntax</span></span>


```C++
HRESULT SynchronousBlockOutputPin();
```



## <a name="parameters"></a><span data-ttu-id="0aab5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0aab5-106">Parameters</span></span>

<span data-ttu-id="0aab5-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="0aab5-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0aab5-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0aab5-108">Return value</span></span>

<span data-ttu-id="0aab5-109">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0aab5-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="0aab5-110">I valori possibili includono quelli mostrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="0aab5-110">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="0aab5-111">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="0aab5-111">Return code</span></span>                                                                                                                    | <span data-ttu-id="0aab5-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0aab5-112">Description</span></span>                                              |
|--------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="0aab5-113"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0aab5-113"><dt>**S\_OK**</dt></span></span> </dl>                                           | <span data-ttu-id="0aab5-114">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="0aab5-114">Success.</span></span><br/>                                      |
| <dl> <span data-ttu-id="0aab5-115"><dt>**\_pin VFW \_ E \_ già \_ bloccato**</dt></span><span class="sxs-lookup"><span data-stu-id="0aab5-115"><dt>**VFW\_E\_PIN\_ALREADY\_BLOCKED**</dt></span></span> </dl>                   | <span data-ttu-id="0aab5-116">Il PIN è già bloccato in un altro thread.</span><span class="sxs-lookup"><span data-stu-id="0aab5-116">Pin is already blocked on another thread.</span></span><br/>     |
| <dl> <span data-ttu-id="0aab5-117"><dt>**\_pin VFW \_ E \_ già \_ bloccato \_ in \_ questo \_ thread**</dt></span><span class="sxs-lookup"><span data-stu-id="0aab5-117"><dt>**VFW\_E\_PIN\_ALREADY\_BLOCKED\_ON\_THIS\_THREAD**</dt></span></span> </dl> | <span data-ttu-id="0aab5-118">Il PIN è già bloccato nel thread chiamante.</span><span class="sxs-lookup"><span data-stu-id="0aab5-118">Pin is already blocked on the calling thread.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0aab5-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="0aab5-119">Remarks</span></span>

<span data-ttu-id="0aab5-120">Non chiamare questo metodo dal thread di streaming.</span><span class="sxs-lookup"><span data-stu-id="0aab5-120">Do not call this method from the streaming thread.</span></span>

## <a name="requirements"></a><span data-ttu-id="0aab5-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0aab5-121">Requirements</span></span>



| <span data-ttu-id="0aab5-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="0aab5-122">Requirement</span></span> | <span data-ttu-id="0aab5-123">Valore</span><span class="sxs-lookup"><span data-stu-id="0aab5-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0aab5-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0aab5-124">Header</span></span><br/>  | <dl> <span data-ttu-id="0aab5-125"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0aab5-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="0aab5-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="0aab5-126">Library</span></span><br/> | <dl> <span data-ttu-id="0aab5-127"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="0aab5-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0aab5-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0aab5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0aab5-129">**Classe CDynamicOutputPin**</span><span class="sxs-lookup"><span data-stu-id="0aab5-129">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




