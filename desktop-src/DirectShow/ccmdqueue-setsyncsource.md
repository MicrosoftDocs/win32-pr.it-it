---
description: Il metodo SetSyncSource imposta l'orologio usato per la temporizzazione.
ms.assetid: 646d4d24-f9b7-438a-b842-58e90eb6a945
title: Metodo CCmdQueue. SetSyncSource (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.SetSyncSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 995df3afa5185d8f50278899ac6a5d67dc6d230e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324185"
---
# <a name="ccmdqueuesetsyncsource-method"></a><span data-ttu-id="1ebe6-103">CCmdQueue. SetSyncSource, metodo</span><span class="sxs-lookup"><span data-stu-id="1ebe6-103">CCmdQueue.SetSyncSource method</span></span>

<span data-ttu-id="1ebe6-104">Il `SetSyncSource` metodo imposta l'orologio usato per la temporizzazione.</span><span class="sxs-lookup"><span data-stu-id="1ebe6-104">The `SetSyncSource` method sets the clock used for timing.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ebe6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1ebe6-105">Syntax</span></span>


```C++
virtual HRESULT SetSyncSource(
   IReferenceClock *pIrc
);
```



## <a name="parameters"></a><span data-ttu-id="1ebe6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1ebe6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ebe6-107">*pIrc*</span><span class="sxs-lookup"><span data-stu-id="1ebe6-107">*pIrc*</span></span> 
</dt> <dd>

<span data-ttu-id="1ebe6-108">Puntatore all'interfaccia [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) .</span><span class="sxs-lookup"><span data-stu-id="1ebe6-108">Pointer to the [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ebe6-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1ebe6-109">Return value</span></span>

<span data-ttu-id="1ebe6-110">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1ebe6-110">Returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ebe6-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1ebe6-111">Requirements</span></span>



| <span data-ttu-id="1ebe6-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ebe6-112">Requirement</span></span> | <span data-ttu-id="1ebe6-113">Valore</span><span class="sxs-lookup"><span data-stu-id="1ebe6-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ebe6-114">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1ebe6-114">Header</span></span><br/>  | <dl> <span data-ttu-id="1ebe6-115"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1ebe6-115"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1ebe6-116">Libreria</span><span class="sxs-lookup"><span data-stu-id="1ebe6-116">Library</span></span><br/> | <dl> <span data-ttu-id="1ebe6-117"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="1ebe6-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ebe6-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1ebe6-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ebe6-119">**Classe CCmdQueue**</span><span class="sxs-lookup"><span data-stu-id="1ebe6-119">**CCmdQueue Class**</span></span>](ccmdqueue.md)
</dt> </dl>

 

 




