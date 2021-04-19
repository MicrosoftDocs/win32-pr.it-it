---
description: Il metodo StartStreaming avvia il flusso quando il filtro passa a uno stato di esecuzione.
ms.assetid: 198e9c1b-be69-4ba6-aa67-9f24ed080ab6
title: Metodo CBaseRenderer. StartStreaming (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.StartStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7bf1fcb1cbfb651221296054493688b2d9f33bd3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332997"
---
# <a name="cbaserendererstartstreaming-method"></a><span data-ttu-id="d175f-103">CBaseRenderer. StartStreaming, metodo</span><span class="sxs-lookup"><span data-stu-id="d175f-103">CBaseRenderer.StartStreaming method</span></span>

<span data-ttu-id="d175f-104">Il `StartStreaming` metodo avvia lo streaming quando il filtro passa a uno stato di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="d175f-104">The `StartStreaming` method initiates streaming when the filter switches to a running state.</span></span>

## <a name="syntax"></a><span data-ttu-id="d175f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d175f-105">Syntax</span></span>


```C++
virtual HRESULT StartStreaming();
```



## <a name="parameters"></a><span data-ttu-id="d175f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d175f-106">Parameters</span></span>

<span data-ttu-id="d175f-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="d175f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d175f-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d175f-108">Return value</span></span>

<span data-ttu-id="d175f-109">Restituisce S \_ OK o un altro valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d175f-109">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d175f-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="d175f-110">Remarks</span></span>

<span data-ttu-id="d175f-111">Se il filtro include un esempio, pianifica l'esempio per il rendering.</span><span class="sxs-lookup"><span data-stu-id="d175f-111">If the filter has a sample, it schedules the sample for rendering.</span></span> <span data-ttu-id="d175f-112">In caso contrario, se è presente una notifica di fine del flusso in sospeso, il filtro Invia un evento [**EC \_ complete**](ec-complete.md) al gestore del grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="d175f-112">Otherwise, if there is a pending end-of-stream notification, the filter sends an [**EC\_COMPLETE**](ec-complete.md) event to the filter graph manager.</span></span>

<span data-ttu-id="d175f-113">Questo metodo chiama il metodo [**CBaseRenderer:: OnStartStreaming**](cbaserenderer-onstartstreaming.md) .</span><span class="sxs-lookup"><span data-stu-id="d175f-113">This method calls the [**CBaseRenderer::OnStartStreaming**](cbaserenderer-onstartstreaming.md) method.</span></span> <span data-ttu-id="d175f-114">Questo metodo non esegue alcuna operazione nella classe di base, ma la classe derivata può eseguirne l'override.</span><span class="sxs-lookup"><span data-stu-id="d175f-114">That method does nothing in the base class, but the derived class can override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="d175f-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d175f-115">Requirements</span></span>



| <span data-ttu-id="d175f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d175f-116">Requirement</span></span> | <span data-ttu-id="d175f-117">Valore</span><span class="sxs-lookup"><span data-stu-id="d175f-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d175f-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d175f-118">Header</span></span><br/>  | <dl> <span data-ttu-id="d175f-119"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d175f-119"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d175f-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="d175f-120">Library</span></span><br/> | <dl> <span data-ttu-id="d175f-121"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d175f-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d175f-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d175f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d175f-123">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="d175f-123">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




