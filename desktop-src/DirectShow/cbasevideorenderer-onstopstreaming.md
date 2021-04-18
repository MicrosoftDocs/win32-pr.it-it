---
description: Il metodo OnStopStreaming viene chiamato alla fine del flusso per correggere gli orari del report della pagina delle proprietà.
ms.assetid: 92174edb-2f6c-4bad-91c5-769aaebcc495
title: Metodo CBaseVideoRenderer. OnStopStreaming (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnStopStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 08cf23fd2e1a7e854625d8a369d15290591386fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325364"
---
# <a name="cbasevideorendereronstopstreaming-method"></a><span data-ttu-id="7a28e-103">CBaseVideoRenderer. OnStopStreaming, metodo</span><span class="sxs-lookup"><span data-stu-id="7a28e-103">CBaseVideoRenderer.OnStopStreaming method</span></span>

<span data-ttu-id="7a28e-104">Il `OnStopStreaming` metodo viene chiamato alla fine del flusso per correggere gli orari del report della pagina delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="7a28e-104">The `OnStopStreaming` method is called at the end of streaming to fix times for the property page report.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a28e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7a28e-105">Syntax</span></span>


```C++
HRESULT OnStopStreaming();
```



## <a name="parameters"></a><span data-ttu-id="7a28e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7a28e-106">Parameters</span></span>

<span data-ttu-id="7a28e-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="7a28e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7a28e-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7a28e-108">Return value</span></span>

<span data-ttu-id="7a28e-109">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7a28e-109">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a28e-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="7a28e-110">Remarks</span></span>

<span data-ttu-id="7a28e-111">Questa funzione membro viene chiamata due volte, una volta in pausa e di nuovo quando il flusso viene effettivamente arrestato.</span><span class="sxs-lookup"><span data-stu-id="7a28e-111">This member function is called twice, once when pausing and again when the stream is actually stopped.</span></span>

<span data-ttu-id="7a28e-112">Questa funzione membro esegue l'override di [**CBaseRenderer:: OnStopStreaming**](cbaserenderer-onstopstreaming.md).</span><span class="sxs-lookup"><span data-stu-id="7a28e-112">This member function overrides [**CBaseRenderer::OnStopStreaming**](cbaserenderer-onstopstreaming.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7a28e-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7a28e-113">Requirements</span></span>



| <span data-ttu-id="7a28e-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a28e-114">Requirement</span></span> | <span data-ttu-id="7a28e-115">Valore</span><span class="sxs-lookup"><span data-stu-id="7a28e-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a28e-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7a28e-116">Header</span></span><br/>  | <dl> <span data-ttu-id="7a28e-117"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7a28e-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7a28e-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="7a28e-118">Library</span></span><br/> | <dl> <span data-ttu-id="7a28e-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="7a28e-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a28e-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7a28e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a28e-121">**Classe CBaseVideoRenderer**</span><span class="sxs-lookup"><span data-stu-id="7a28e-121">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




