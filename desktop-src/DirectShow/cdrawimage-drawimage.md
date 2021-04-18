---
description: Il metodo DrawImage Disegna un frame video nella finestra del video.
ms.assetid: 22e7f59c-90f7-4e0c-8993-eea1eaf58fba
title: Metodo CDrawImage. DrawImage (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.DrawImage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d219eb82ab2cf1929605eee4045c2f278022ad98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327212"
---
# <a name="cdrawimagedrawimage-method"></a><span data-ttu-id="be53a-103">Metodo CDrawImage. DrawImage</span><span class="sxs-lookup"><span data-stu-id="be53a-103">CDrawImage.DrawImage method</span></span>

<span data-ttu-id="be53a-104">Il `DrawImage` metodo disegna un frame video nella finestra del video.</span><span class="sxs-lookup"><span data-stu-id="be53a-104">The `DrawImage` method draws a video frame on the video window.</span></span>

## <a name="syntax"></a><span data-ttu-id="be53a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="be53a-105">Syntax</span></span>


```C++
BOOL DrawImage(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="be53a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="be53a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be53a-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="be53a-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="be53a-108">Puntatore all'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) dell'esempio che contiene l'immagine.</span><span class="sxs-lookup"><span data-stu-id="be53a-108">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the sample that contains the image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be53a-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="be53a-109">Return value</span></span>

<span data-ttu-id="be53a-110">Restituisce **true** se l'operazione è riuscita o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="be53a-110">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="be53a-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="be53a-111">Remarks</span></span>

<span data-ttu-id="be53a-112">Questo metodo delega a [**CDrawImage:: FastRender**](cdrawimage-fastrender.md) o [**CDrawImage:: SlowRender**](cdrawimage-slowrender.md), a seconda che il filtro appartenga all'allocatore che ha fornito l'esempio.</span><span class="sxs-lookup"><span data-stu-id="be53a-112">This method delegates to [**CDrawImage::FastRender**](cdrawimage-fastrender.md) or [**CDrawImage::SlowRender**](cdrawimage-slowrender.md), depending on whether the filter owns the allocator that provided the sample.</span></span> <span data-ttu-id="be53a-113">Se il filtro è proprietario dell'allocatore, l'esempio è sicuramente un oggetto [**CImageSample**](cimagesample.md) .</span><span class="sxs-lookup"><span data-stu-id="be53a-113">If the filter does own the allocator, the sample is guaranteed to be a [**CImageSample**](cimagesample.md) object.</span></span> <span data-ttu-id="be53a-114">In tal caso, nell'esempio viene utilizzata la memoria condivisa allocata da GDI e l'immagine può essere disegnata utilizzando **BitBlt** o **StretchBlt**.</span><span class="sxs-lookup"><span data-stu-id="be53a-114">In that case, the sample uses shared memory allocated by GDI, and the image can be drawn using either **BitBlt** or **StretchBlt**.</span></span> <span data-ttu-id="be53a-115">In caso contrario, le immagini devono essere disegnate usando le funzioni **SetDIBitsToDevice** o **StretchDIBits** più lente.</span><span class="sxs-lookup"><span data-stu-id="be53a-115">Otherwise, the images must be drawn using the slower **SetDIBitsToDevice** or **StretchDIBits** functions.</span></span>

<span data-ttu-id="be53a-116">Nelle compilazioni di debug questo metodo chiama **DisplaySampleTimes** per creare i timestamp dell'esempio sull'immagine video.</span><span class="sxs-lookup"><span data-stu-id="be53a-116">In debug builds, this method calls **DisplaySampleTimes** to draw the sample's time stamps over the video image.</span></span>

## <a name="requirements"></a><span data-ttu-id="be53a-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="be53a-117">Requirements</span></span>



| <span data-ttu-id="be53a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="be53a-118">Requirement</span></span> | <span data-ttu-id="be53a-119">Valore</span><span class="sxs-lookup"><span data-stu-id="be53a-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be53a-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="be53a-120">Header</span></span><br/>  | <dl> <span data-ttu-id="be53a-121"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="be53a-121"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="be53a-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="be53a-122">Library</span></span><br/> | <dl> <span data-ttu-id="be53a-123"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="be53a-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be53a-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="be53a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be53a-125">**Classe CDrawImage**</span><span class="sxs-lookup"><span data-stu-id="be53a-125">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> <dt>

[<span data-ttu-id="be53a-126">**CDrawImage::UsingImageAllocator**</span><span class="sxs-lookup"><span data-stu-id="be53a-126">**CDrawImage::UsingImageAllocator**</span></span>](cdrawimage-usingimageallocator.md)
</dt> </dl>

 

 




