---
description: Il metodo Run passa alla modalità di esecuzione in modo che sia possibile eseguire i comandi rinviati dall'ora del flusso.
ms.assetid: c529ae84-c9b7-46f1-a1e4-716fc9e9df13
title: Metodo CCmdQueue. Run (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 424914e53a12ff0f43e8b7e2a3345c28d84437d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324472"
---
# <a name="ccmdqueuerun-method"></a><span data-ttu-id="ec32d-103">Metodo CCmdQueue. Run</span><span class="sxs-lookup"><span data-stu-id="ec32d-103">CCmdQueue.Run method</span></span>

<span data-ttu-id="ec32d-104">Il `Run` metodo passa alla modalità di esecuzione in modo che sia possibile eseguire i comandi rinviati dall'ora del flusso.</span><span class="sxs-lookup"><span data-stu-id="ec32d-104">The `Run` method switches to running mode so that commands that are deferred by the stream time can be run.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec32d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ec32d-105">Syntax</span></span>


```C++
virtual HRESULT Run(
   REFERENCE_TIME tStreamTimeOffset
);
```



## <a name="parameters"></a><span data-ttu-id="ec32d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ec32d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec32d-107">*tStreamTimeOffset*</span><span class="sxs-lookup"><span data-stu-id="ec32d-107">*tStreamTimeOffset*</span></span> 
</dt> <dd>

<span data-ttu-id="ec32d-108">Tempo di offset.</span><span class="sxs-lookup"><span data-stu-id="ec32d-108">Offset time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec32d-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ec32d-109">Return value</span></span>

<span data-ttu-id="ec32d-110">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ec32d-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec32d-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="ec32d-111">Remarks</span></span>

<span data-ttu-id="ec32d-112">In modalità di esecuzione, è noto il mapping del flusso di tempo per presentazione.</span><span class="sxs-lookup"><span data-stu-id="ec32d-112">During running mode, stream-time-to-presentation-time mapping is known.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec32d-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ec32d-113">Requirements</span></span>



| <span data-ttu-id="ec32d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec32d-114">Requirement</span></span> | <span data-ttu-id="ec32d-115">Valore</span><span class="sxs-lookup"><span data-stu-id="ec32d-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec32d-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ec32d-116">Header</span></span><br/>  | <dl> <span data-ttu-id="ec32d-117"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ec32d-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ec32d-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="ec32d-118">Library</span></span><br/> | <dl> <span data-ttu-id="ec32d-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ec32d-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec32d-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ec32d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec32d-121">**Classe CCmdQueue**</span><span class="sxs-lookup"><span data-stu-id="ec32d-121">**CCmdQueue Class**</span></span>](ccmdqueue.md)
</dt> </dl>

 

 




