---
description: Il metodo OnReceiveFirstSample viene chiamato quando il filtro riceve un campione mentre è sospeso.
ms.assetid: 5bd481bf-a62d-4d3c-b875-b94298d12730
title: Metodo CBaseRenderer. OnReceiveFirstSample (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnReceiveFirstSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2368b0e2abda3bcdd08872d730f8b9902dad43ac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333351"
---
# <a name="cbaserendereronreceivefirstsample-method"></a><span data-ttu-id="d075f-103">CBaseRenderer. OnReceiveFirstSample, metodo</span><span class="sxs-lookup"><span data-stu-id="d075f-103">CBaseRenderer.OnReceiveFirstSample method</span></span>

<span data-ttu-id="d075f-104">Il `OnReceiveFirstSample` metodo viene chiamato quando il filtro riceve un campione mentre è sospeso.</span><span class="sxs-lookup"><span data-stu-id="d075f-104">The `OnReceiveFirstSample` method is called when the filter receives a sample while paused.</span></span>

## <a name="syntax"></a><span data-ttu-id="d075f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d075f-105">Syntax</span></span>


```C++
virtual void OnReceiveFirstSample(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="d075f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d075f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d075f-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="d075f-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="d075f-108">Puntatore all'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="d075f-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d075f-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d075f-109">Return value</span></span>

<span data-ttu-id="d075f-110">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="d075f-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d075f-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="d075f-111">Remarks</span></span>

<span data-ttu-id="d075f-112">Il metodo [**CBaseRenderer:: Receive**](cbaserenderer-receive.md) chiama questo metodo.</span><span class="sxs-lookup"><span data-stu-id="d075f-112">The [**CBaseRenderer::Receive**](cbaserenderer-receive.md) method calls this method.</span></span> <span data-ttu-id="d075f-113">Non esegue alcuna operazione nella classe di base, ma la classe derivata può eseguirne l'override.</span><span class="sxs-lookup"><span data-stu-id="d075f-113">It does nothing in the base class, but the derived class can override it.</span></span> <span data-ttu-id="d075f-114">Questo metodo è destinato principalmente ai renderer di video.</span><span class="sxs-lookup"><span data-stu-id="d075f-114">This method is intended primarily for video renderers.</span></span> <span data-ttu-id="d075f-115">Quando un renderer video viene sospeso, viene in genere visualizzato il primo campione come immagine ancora.</span><span class="sxs-lookup"><span data-stu-id="d075f-115">When a video renderer is paused, it typically displays the first sample as a still image.</span></span>

<span data-ttu-id="d075f-116">La ricerca del grafico mentre viene sospesa causa anche la chiamata del metodo.</span><span class="sxs-lookup"><span data-stu-id="d075f-116">Seeking the graph while paused also causes this method to be called.</span></span>

## <a name="requirements"></a><span data-ttu-id="d075f-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d075f-117">Requirements</span></span>



| <span data-ttu-id="d075f-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d075f-118">Requirement</span></span> | <span data-ttu-id="d075f-119">Valore</span><span class="sxs-lookup"><span data-stu-id="d075f-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d075f-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d075f-120">Header</span></span><br/>  | <dl> <span data-ttu-id="d075f-121"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d075f-121"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d075f-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="d075f-122">Library</span></span><br/> | <dl> <span data-ttu-id="d075f-123"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d075f-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d075f-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d075f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d075f-125">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="d075f-125">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




