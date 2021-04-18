---
description: Il metodo ShouldSkipFrame determina se il filtro deve eliminare un campione specificato.
ms.assetid: 49f86f7d-28b1-443e-a238-692da96d60fb
title: Metodo CVideoTransformFilter. ShouldSkipFrame (Vtrans. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.ShouldSkipFrame
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7f845ac7ae52537bfadfb6c913537b32e4d44171
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325501"
---
# <a name="cvideotransformfiltershouldskipframe-method"></a><span data-ttu-id="d0685-103">CVideoTransformFilter. ShouldSkipFrame, metodo</span><span class="sxs-lookup"><span data-stu-id="d0685-103">CVideoTransformFilter.ShouldSkipFrame method</span></span>

<span data-ttu-id="d0685-104">Il `ShouldSkipFrame` metodo determina se il filtro deve eliminare un campione specificato.</span><span class="sxs-lookup"><span data-stu-id="d0685-104">The `ShouldSkipFrame` method determines whether the filter should drop a specified sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0685-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d0685-105">Syntax</span></span>


```C++
BOOL ShouldSkipFrame(
   IMediaSample *pIn
);
```



## <a name="parameters"></a><span data-ttu-id="d0685-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d0685-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0685-107">*pIn*</span><span class="sxs-lookup"><span data-stu-id="d0685-107">*pIn*</span></span> 
</dt> <dd>

<span data-ttu-id="d0685-108">Puntatore all'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="d0685-108">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0685-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d0685-109">Return value</span></span>

<span data-ttu-id="d0685-110">Restituisce **true** se il filtro deve eliminare questo esempio oppure **false** se il filtro deve elaborare l'esempio.</span><span class="sxs-lookup"><span data-stu-id="d0685-110">Returns **TRUE** if the filter should drop this sample, or **FALSE** if the filter should process this sample.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0685-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="d0685-111">Remarks</span></span>

<span data-ttu-id="d0685-112">Questo metodo restituisce **true** se vengono soddisfatte le condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="d0685-112">This method returns **TRUE** if the following conditions are met:</span></span>

-   <span data-ttu-id="d0685-113">Nell'esempio sono presenti timestamp.</span><span class="sxs-lookup"><span data-stu-id="d0685-113">The sample has time stamps.</span></span>
-   <span data-ttu-id="d0685-114">Il tempo di decodifica medio è almeno il 25% della durata del fotogramma.</span><span class="sxs-lookup"><span data-stu-id="d0685-114">The average decoding time is at least 25% of the frame duration.</span></span>
-   <span data-ttu-id="d0685-115">Il renderer è attualmente almeno un frame tardivo, come segnalato tramite messaggi di qualità.</span><span class="sxs-lookup"><span data-stu-id="d0685-115">The renderer is currently at least one frame late, as reported through quality messages.</span></span>
-   <span data-ttu-id="d0685-116">Se si ignora il fotogramma chiave successivo, il frame arriverà prima di più di un frame.</span><span class="sxs-lookup"><span data-stu-id="d0685-116">Skipping to the next key frame would not cause the frame to arrive more than one frame early.</span></span>

<span data-ttu-id="d0685-117">Ai fini di questo calcolo, il filtro registra le seguenti informazioni durante l'elaborazione dei dati:</span><span class="sxs-lookup"><span data-stu-id="d0685-117">For purposes of this calculation, the filter records the following information as it processes data:</span></span>

-   <span data-ttu-id="d0685-118">Tempo di decodifica medio negli ultimi 20 frame (**m \_ itrAvgDecode**)</span><span class="sxs-lookup"><span data-stu-id="d0685-118">The average decoding time over the past 20 frames (**m\_itrAvgDecode**)</span></span>
-   <span data-ttu-id="d0685-119">Il numero di frame dall'ultimo fotogramma chiave (**m \_ nFramesSinceKeyFrame**)</span><span class="sxs-lookup"><span data-stu-id="d0685-119">The number of frames since the last key frame (**m\_nFramesSinceKeyFrame**)</span></span>
-   <span data-ttu-id="d0685-120">Stima del numero di frame tra i fotogrammi chiave (**m \_ nKeyFramePeriod**)</span><span class="sxs-lookup"><span data-stu-id="d0685-120">An estimate of how many frames there are between key frames (**m\_nKeyFramePeriod**)</span></span>

<span data-ttu-id="d0685-121">Quando il filtro rilascia un frame, continua a rilasciare i frame fino a raggiungere il fotogramma chiave successivo.</span><span class="sxs-lookup"><span data-stu-id="d0685-121">Once the filter drops a frame, it continues to drop frames until it reaches the next key frame.</span></span> <span data-ttu-id="d0685-122">Se questo metodo restituisce **true**, invia anche un evento [**di \_ \_ modifica della qualità EC**](ec-quality-change.md) a Filter Graph Manager.</span><span class="sxs-lookup"><span data-stu-id="d0685-122">If this method returns **TRUE**, it also sends an [**EC\_QUALITY\_CHANGE**](ec-quality-change.md) event to the Filter Graph Manager.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0685-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d0685-123">Requirements</span></span>



| <span data-ttu-id="d0685-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0685-124">Requirement</span></span> | <span data-ttu-id="d0685-125">Valore</span><span class="sxs-lookup"><span data-stu-id="d0685-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0685-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d0685-126">Header</span></span><br/>  | <dl> <span data-ttu-id="d0685-127"><dt>Vtrans. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d0685-127"><dt>Vtrans.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="d0685-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="d0685-128">Library</span></span><br/> | <dl> <span data-ttu-id="d0685-129"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d0685-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0685-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d0685-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0685-131">**Classe CVideoTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="d0685-131">**CVideoTransformFilter Class**</span></span>](cvideotransformfilter.md)
</dt> </dl>

 

 




