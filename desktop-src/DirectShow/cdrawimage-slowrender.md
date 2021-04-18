---
description: Il metodo SlowRender disegna l'immagine video usando le funzioni SetDIBitsToDevice o StretchDIBits.
ms.assetid: e1d8b189-b588-48eb-988a-3e5dedb38dbd
title: Metodo CDrawImage. SlowRender (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.SlowRender
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b736bf6c44d4ada6e0a28408c449c9f8b2f1e1cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327205"
---
# <a name="cdrawimageslowrender-method"></a><span data-ttu-id="b47ed-103">CDrawImage. SlowRender, metodo</span><span class="sxs-lookup"><span data-stu-id="b47ed-103">CDrawImage.SlowRender method</span></span>

<span data-ttu-id="b47ed-104">Il `SlowRender` metodo disegna l'immagine video usando le funzioni **SetDIBitsToDevice** o **StretchDIBits** .</span><span class="sxs-lookup"><span data-stu-id="b47ed-104">The `SlowRender` method draws the video image using the **SetDIBitsToDevice** or **StretchDIBits** functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="b47ed-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b47ed-105">Syntax</span></span>


```C++
void SlowRender(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="b47ed-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b47ed-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b47ed-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="b47ed-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="b47ed-108">Puntatore all'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) dell'esempio che contiene l'immagine.</span><span class="sxs-lookup"><span data-stu-id="b47ed-108">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the sample that contains the image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b47ed-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b47ed-109">Return value</span></span>

<span data-ttu-id="b47ed-110">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="b47ed-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b47ed-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="b47ed-111">Remarks</span></span>

<span data-ttu-id="b47ed-112">Se [**CDrawImage:: UsingImageAllocator**](cdrawimage-usingimageallocator.md) restituisce **false**, il metodo [**CDrawImage::D rawImage**](cdrawimage-drawimage.md) USA `SlowRender` per creare l'immagine del video.</span><span class="sxs-lookup"><span data-stu-id="b47ed-112">If [**CDrawImage::UsingImageAllocator**](cdrawimage-usingimageallocator.md) returns **FALSE**, the [**CDrawImage::DrawImage**](cdrawimage-drawimage.md) method uses `SlowRender` to draw the video image.</span></span> <span data-ttu-id="b47ed-113">In caso contrario, DrawImage usa il metodo **FastRender** .</span><span class="sxs-lookup"><span data-stu-id="b47ed-113">Otherwise, DrawImage uses the **FastRender** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="b47ed-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b47ed-114">Requirements</span></span>



| <span data-ttu-id="b47ed-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b47ed-115">Requirement</span></span> | <span data-ttu-id="b47ed-116">Valore</span><span class="sxs-lookup"><span data-stu-id="b47ed-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b47ed-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b47ed-117">Header</span></span><br/>  | <dl> <span data-ttu-id="b47ed-118"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b47ed-118"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b47ed-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="b47ed-119">Library</span></span><br/> | <dl> <span data-ttu-id="b47ed-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b47ed-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b47ed-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b47ed-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b47ed-122">**Classe CDrawImage**</span><span class="sxs-lookup"><span data-stu-id="b47ed-122">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> <dt>

[<span data-ttu-id="b47ed-123">**CDrawImage::FastRender**</span><span class="sxs-lookup"><span data-stu-id="b47ed-123">**CDrawImage::FastRender**</span></span>](cdrawimage-fastrender.md)
</dt> </dl>

 

 




