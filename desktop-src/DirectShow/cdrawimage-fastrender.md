---
description: Il metodo FastRender disegna l'immagine video usando le funzioni BitBlt o StretchBlt.
ms.assetid: 8bbc96ce-393f-46fb-bf90-61d3ce0ef0d6
title: Metodo CDrawImage. FastRender (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.FastRender
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 823583beed6696d40803ccc098410dac053b8948
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327210"
---
# <a name="cdrawimagefastrender-method"></a><span data-ttu-id="43dc1-103">CDrawImage. FastRender, metodo</span><span class="sxs-lookup"><span data-stu-id="43dc1-103">CDrawImage.FastRender method</span></span>

<span data-ttu-id="43dc1-104">Il `FastRender` metodo disegna l'immagine video usando le funzioni **BitBlt** o **StretchBlt** .</span><span class="sxs-lookup"><span data-stu-id="43dc1-104">The `FastRender` method draws the video image using the **BitBlt** or **StretchBlt** functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="43dc1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="43dc1-105">Syntax</span></span>


```C++
void FastRender(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="43dc1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="43dc1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43dc1-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="43dc1-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="43dc1-108">Puntatore all'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) dell'esempio che contiene l'immagine.</span><span class="sxs-lookup"><span data-stu-id="43dc1-108">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the sample that contains the image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43dc1-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="43dc1-109">Return value</span></span>

<span data-ttu-id="43dc1-110">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="43dc1-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="43dc1-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="43dc1-111">Remarks</span></span>

<span data-ttu-id="43dc1-112">Il metodo [**CDrawImage::D rawImage**](cdrawimage-drawimage.md) chiama questo metodo, ma solo se l'allocatore per la connessione è un oggetto [**CImageAllocator**](cimageallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="43dc1-112">The [**CDrawImage::DrawImage**](cdrawimage-drawimage.md) method calls this method, but only if the allocator for the connection is a [**CImageAllocator**](cimageallocator.md) object.</span></span> <span data-ttu-id="43dc1-113">In tal caso, l'esempio multimediale è sicuramente un oggetto [**CImageSample**](cimagesample.md) .</span><span class="sxs-lookup"><span data-stu-id="43dc1-113">In that case, the media sample is guaranteed to be a [**CImageSample**](cimagesample.md) object.</span></span> <span data-ttu-id="43dc1-114">L'oggetto **CImageSample** usa la funzione **CreateDIBSection** per allocare la memoria condivisa per la bitmap, che consente di creare l'immagine usando **BitBlt** o **StretchBlt**.</span><span class="sxs-lookup"><span data-stu-id="43dc1-114">The **CImageSample** object uses the **CreateDIBSection** function to allocate shared memory for the bitmap, which makes it possible to draw the image using either **BitBlt** or **StretchBlt**.</span></span>

<span data-ttu-id="43dc1-115">Questo metodo chiama **BitBlt** se i rettangoli di origine e destinazione corrispondono esattamente o **StretchBlt** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="43dc1-115">This method calls **BitBlt** if the source and targer rectangles exactly match, or **StretchBlt** otherwise.</span></span>

<span data-ttu-id="43dc1-116">Se il filtro non è il proprietario dell'allocatore, il metodo **DrawImage** USA [**CDrawImage:: SlowRender**](cdrawimage-slowrender.md) per creare l'immagine.</span><span class="sxs-lookup"><span data-stu-id="43dc1-116">If the filter does not own the allocator, the **DrawImage** method uses [**CDrawImage::SlowRender**](cdrawimage-slowrender.md) to draw the image.</span></span>

## <a name="requirements"></a><span data-ttu-id="43dc1-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="43dc1-117">Requirements</span></span>



| <span data-ttu-id="43dc1-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="43dc1-118">Requirement</span></span> | <span data-ttu-id="43dc1-119">Valore</span><span class="sxs-lookup"><span data-stu-id="43dc1-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43dc1-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="43dc1-120">Header</span></span><br/>  | <dl> <span data-ttu-id="43dc1-121"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="43dc1-121"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="43dc1-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="43dc1-122">Library</span></span><br/> | <dl> <span data-ttu-id="43dc1-123"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="43dc1-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43dc1-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="43dc1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43dc1-125">**Classe CDrawImage**</span><span class="sxs-lookup"><span data-stu-id="43dc1-125">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 




