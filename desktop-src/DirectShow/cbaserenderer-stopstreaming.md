---
description: Il metodo StopStreaming interrompe lo streaming quando il filtro si spegne dallo stato di esecuzione.
ms.assetid: 465dde15-adec-46da-b8c8-56743e0cbd29
title: Metodo CBaseRenderer. StopStreaming (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.StopStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dfd943de6a53383d7505fa9e884dcc152da6e5f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332991"
---
# <a name="cbaserendererstopstreaming-method"></a><span data-ttu-id="9a781-103">CBaseRenderer. StopStreaming, metodo</span><span class="sxs-lookup"><span data-stu-id="9a781-103">CBaseRenderer.StopStreaming method</span></span>

<span data-ttu-id="9a781-104">Il `StopStreaming` metodo interrompe lo streaming quando il filtro si spegne dallo stato di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="9a781-104">The `StopStreaming` method halts streaming when the filter switches out of the running state.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a781-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9a781-105">Syntax</span></span>


```C++
virtual HRESULT StopStreaming();
```



## <a name="parameters"></a><span data-ttu-id="9a781-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9a781-106">Parameters</span></span>

<span data-ttu-id="9a781-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="9a781-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9a781-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9a781-108">Return value</span></span>

<span data-ttu-id="9a781-109">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9a781-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a781-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="9a781-110">Remarks</span></span>

<span data-ttu-id="9a781-111">Questo metodo chiama il metodo [**CBaseRenderer:: OnStopStreaming**](cbaserenderer-onstopstreaming.md) .</span><span class="sxs-lookup"><span data-stu-id="9a781-111">This method calls the [**CBaseRenderer::OnStopStreaming**](cbaserenderer-onstopstreaming.md) method.</span></span> <span data-ttu-id="9a781-112">Questo metodo non esegue alcuna operazione nella classe di base, ma la classe derivata può eseguirne l'override.</span><span class="sxs-lookup"><span data-stu-id="9a781-112">That method does nothing in the base class, but the derived class can override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a781-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9a781-113">Requirements</span></span>



| <span data-ttu-id="9a781-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a781-114">Requirement</span></span> | <span data-ttu-id="9a781-115">Valore</span><span class="sxs-lookup"><span data-stu-id="9a781-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a781-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9a781-116">Header</span></span><br/>  | <dl> <span data-ttu-id="9a781-117"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9a781-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9a781-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="9a781-118">Library</span></span><br/> | <dl> <span data-ttu-id="9a781-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="9a781-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a781-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9a781-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a781-121">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="9a781-121">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




