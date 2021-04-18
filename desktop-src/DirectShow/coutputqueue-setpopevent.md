---
description: Il metodo SetPopEvent specifica un evento che viene segnalato ogni volta che l'oggetto rimuove un campione dalla coda.
ms.assetid: 147a09b9-14d3-4739-843a-1bfb19d2d052
title: Metodo COutputQueue. SetPopEvent (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.SetPopEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 764abf76265fce66c5798923ca1fa522edd682af
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324670"
---
# <a name="coutputqueuesetpopevent-method"></a><span data-ttu-id="7dce4-103">COutputQueue. SetPopEvent, metodo</span><span class="sxs-lookup"><span data-stu-id="7dce4-103">COutputQueue.SetPopEvent method</span></span>

<span data-ttu-id="7dce4-104">Il `SetPopEvent` metodo specifica un evento che viene segnalato ogni volta che l'oggetto rimuove un campione dalla coda.</span><span class="sxs-lookup"><span data-stu-id="7dce4-104">The `SetPopEvent` method specifies an event that is signaled whenever the object removes a sample from the queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="7dce4-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7dce4-105">Syntax</span></span>


```C++
void SetPopEvent(
   HANDLE hEvent
);
```



## <a name="parameters"></a><span data-ttu-id="7dce4-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7dce4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7dce4-107">*hEvent*</span><span class="sxs-lookup"><span data-stu-id="7dce4-107">*hEvent*</span></span> 
</dt> <dd>

<span data-ttu-id="7dce4-108">Handle per un evento creato dal chiamante.</span><span class="sxs-lookup"><span data-stu-id="7dce4-108">Handle to an event created by the caller.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7dce4-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7dce4-109">Return value</span></span>

<span data-ttu-id="7dce4-110">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="7dce4-110">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="7dce4-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7dce4-111">Requirements</span></span>



| <span data-ttu-id="7dce4-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="7dce4-112">Requirement</span></span> | <span data-ttu-id="7dce4-113">Valore</span><span class="sxs-lookup"><span data-stu-id="7dce4-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7dce4-114">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7dce4-114">Header</span></span><br/>  | <dl> <span data-ttu-id="7dce4-115"><dt>Outputq. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7dce4-115"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7dce4-116">Libreria</span><span class="sxs-lookup"><span data-stu-id="7dce4-116">Library</span></span><br/> | <dl> <span data-ttu-id="7dce4-117"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="7dce4-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7dce4-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7dce4-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7dce4-119">**Classe COutputQueue**</span><span class="sxs-lookup"><span data-stu-id="7dce4-119">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




