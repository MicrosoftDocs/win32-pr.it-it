---
description: Il metodo ShouldDrawSampleNow determina se il video deve essere disegnato senza impostare un collegamento di notifica del timer con il clock.
ms.assetid: 2cbefc66-0d99-4559-b210-3163cd413dbf
title: Metodo CBaseVideoRenderer. ShouldDrawSampleNow (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.ShouldDrawSampleNow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8c96b7453eb6009121fd6782030f7988663f5e8f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325346"
---
# <a name="cbasevideorenderershoulddrawsamplenow-method"></a><span data-ttu-id="71464-103">CBaseVideoRenderer. ShouldDrawSampleNow, metodo</span><span class="sxs-lookup"><span data-stu-id="71464-103">CBaseVideoRenderer.ShouldDrawSampleNow method</span></span>

<span data-ttu-id="71464-104">Il `ShouldDrawSampleNow` metodo determina se il video deve essere disegnato senza impostare un collegamento di notifica del timer con il clock.</span><span class="sxs-lookup"><span data-stu-id="71464-104">The `ShouldDrawSampleNow` method determines if the video should be drawn without setting a timer advise link with the clock.</span></span>

## <a name="syntax"></a><span data-ttu-id="71464-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="71464-105">Syntax</span></span>


```C++
virtual HRESULT ShouldDrawSampleNow(
   IMediaSample   *pMediaSample,
   REFERENCE_TIME *ptrStart,
   REFERENCE_TIME *ptrEnd
);
```



## <a name="parameters"></a><span data-ttu-id="71464-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="71464-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71464-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="71464-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="71464-108">Puntatore all'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) per l'esempio.</span><span class="sxs-lookup"><span data-stu-id="71464-108">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface for the sample.</span></span>

</dd> <dt>

<span data-ttu-id="71464-109">*ptrStart*</span><span class="sxs-lookup"><span data-stu-id="71464-109">*ptrStart*</span></span> 
</dt> <dd>

<span data-ttu-id="71464-110">Puntatore al momento in cui iniziare il rendering.</span><span class="sxs-lookup"><span data-stu-id="71464-110">Pointer to the time to begin rendering.</span></span>

</dd> <dt>

<span data-ttu-id="71464-111">*ptrEnd*</span><span class="sxs-lookup"><span data-stu-id="71464-111">*ptrEnd*</span></span> 
</dt> <dd>

<span data-ttu-id="71464-112">Puntatore al tempo necessario per arrestare il rendering.</span><span class="sxs-lookup"><span data-stu-id="71464-112">Pointer to the time to stop rendering.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71464-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="71464-113">Return value</span></span>

<span data-ttu-id="71464-114">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="71464-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="71464-115">Restituisce \_ OK per indicare un valore di estrazione in una sola volta senza attendere, S \_ false per indicare il valore di *ptrStart* per ora, oppure un errore per indicare che non è possibile creare l'esempio, ovvero ignorarlo per risparmiare tempo.</span><span class="sxs-lookup"><span data-stu-id="71464-115">Returns S\_OK to mean draw at once without waiting, S\_FALSE to mean draw at time *ptrStart*, or an error to mean do not draw the sample; that is, skip it to save time.</span></span>

## <a name="remarks"></a><span data-ttu-id="71464-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="71464-116">Remarks</span></span>

<span data-ttu-id="71464-117">Questa funzione membro esegue l'override di [**CBaseRenderer:: ShouldDrawSampleNow**](cbaserenderer-shoulddrawsamplenow.md).</span><span class="sxs-lookup"><span data-stu-id="71464-117">This member function overrides [**CBaseRenderer::ShouldDrawSampleNow**](cbaserenderer-shoulddrawsamplenow.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="71464-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="71464-118">Requirements</span></span>



| <span data-ttu-id="71464-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="71464-119">Requirement</span></span> | <span data-ttu-id="71464-120">Valore</span><span class="sxs-lookup"><span data-stu-id="71464-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71464-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="71464-121">Header</span></span><br/>  | <dl> <span data-ttu-id="71464-122"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="71464-122"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="71464-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="71464-123">Library</span></span><br/> | <dl> <span data-ttu-id="71464-124"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="71464-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71464-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="71464-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71464-126">**Classe CBaseVideoRenderer**</span><span class="sxs-lookup"><span data-stu-id="71464-126">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




