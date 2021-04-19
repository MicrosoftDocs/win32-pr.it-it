---
description: Il metodo OnStopStreaming viene chiamato quando il filtro interrompe il flusso.
ms.assetid: d882fec8-09e1-4d36-a09c-44568e743da3
title: Metodo CBaseRenderer. OnStopStreaming (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnStopStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 417a18ca53240dce0e4ed6d40f551c45c24b0f1c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333349"
---
# <a name="cbaserendereronstopstreaming-method"></a><span data-ttu-id="2713c-103">CBaseRenderer. OnStopStreaming, metodo</span><span class="sxs-lookup"><span data-stu-id="2713c-103">CBaseRenderer.OnStopStreaming method</span></span>

<span data-ttu-id="2713c-104">Il `OnStopStreaming` metodo viene chiamato quando il filtro interrompe il flusso.</span><span class="sxs-lookup"><span data-stu-id="2713c-104">The `OnStopStreaming` method is called when the filter stops streaming.</span></span>

## <a name="syntax"></a><span data-ttu-id="2713c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2713c-105">Syntax</span></span>


```C++
virtual HRESULT OnStopStreaming();
```



## <a name="parameters"></a><span data-ttu-id="2713c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2713c-106">Parameters</span></span>

<span data-ttu-id="2713c-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="2713c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2713c-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2713c-108">Return value</span></span>

<span data-ttu-id="2713c-109">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2713c-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="2713c-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="2713c-110">Remarks</span></span>

<span data-ttu-id="2713c-111">Il metodo [**CBaseRenderer:: StopStreaming**](cbaserenderer-stopstreaming.md) chiama questo metodo.</span><span class="sxs-lookup"><span data-stu-id="2713c-111">The [**CBaseRenderer::StopStreaming**](cbaserenderer-stopstreaming.md) method calls this method.</span></span> <span data-ttu-id="2713c-112">Non esegue alcuna operazione nella classe di base, ma la classe derivata può eseguirne l'override.</span><span class="sxs-lookup"><span data-stu-id="2713c-112">It does nothing in the base class, but the derived class can override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="2713c-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2713c-113">Requirements</span></span>



| <span data-ttu-id="2713c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="2713c-114">Requirement</span></span> | <span data-ttu-id="2713c-115">Valore</span><span class="sxs-lookup"><span data-stu-id="2713c-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2713c-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2713c-116">Header</span></span><br/>  | <dl> <span data-ttu-id="2713c-117"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2713c-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2713c-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="2713c-118">Library</span></span><br/> | <dl> <span data-ttu-id="2713c-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="2713c-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2713c-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2713c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2713c-121">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="2713c-121">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




