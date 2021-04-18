---
description: Il metodo ResetStreamingTimes Reimposta tutte le volte che controllano il flusso.
ms.assetid: 8a596760-a45a-4486-bb91-aab10bbf927f
title: Metodo CBaseVideoRenderer. ResetStreamingTimes (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.ResetStreamingTimes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d887ca9e246d5e3fb746c119b1ed6784201ec702
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325355"
---
# <a name="cbasevideorendererresetstreamingtimes-method"></a><span data-ttu-id="340c6-103">CBaseVideoRenderer. ResetStreamingTimes, metodo</span><span class="sxs-lookup"><span data-stu-id="340c6-103">CBaseVideoRenderer.ResetStreamingTimes method</span></span>

<span data-ttu-id="340c6-104">Il `ResetStreamingTimes` metodo reimposta tutte le volte che controllano il flusso.</span><span class="sxs-lookup"><span data-stu-id="340c6-104">The `ResetStreamingTimes` method resets all times that control the streaming.</span></span>

## <a name="syntax"></a><span data-ttu-id="340c6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="340c6-105">Syntax</span></span>


```C++
virtual HRESULT ResetStreamingTimes();
```



## <a name="parameters"></a><span data-ttu-id="340c6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="340c6-106">Parameters</span></span>

<span data-ttu-id="340c6-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="340c6-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="340c6-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="340c6-108">Return value</span></span>

<span data-ttu-id="340c6-109">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="340c6-109">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="340c6-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="340c6-110">Remarks</span></span>

<span data-ttu-id="340c6-111">Gli orari sono impostati in modo che i frame non vengano eliminati inizialmente e in modo che venga disegnato il primo frame.</span><span class="sxs-lookup"><span data-stu-id="340c6-111">The times are set so that frames will not be initially dropped and so that the first frame will be drawn.</span></span>

## <a name="requirements"></a><span data-ttu-id="340c6-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="340c6-112">Requirements</span></span>



| <span data-ttu-id="340c6-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="340c6-113">Requirement</span></span> | <span data-ttu-id="340c6-114">Valore</span><span class="sxs-lookup"><span data-stu-id="340c6-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="340c6-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="340c6-115">Header</span></span><br/>  | <dl> <span data-ttu-id="340c6-116"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="340c6-116"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="340c6-117">Libreria</span><span class="sxs-lookup"><span data-stu-id="340c6-117">Library</span></span><br/> | <dl> <span data-ttu-id="340c6-118"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="340c6-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="340c6-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="340c6-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="340c6-120">**Classe CBaseVideoRenderer**</span><span class="sxs-lookup"><span data-stu-id="340c6-120">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




