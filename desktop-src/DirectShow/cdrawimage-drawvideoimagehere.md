---
description: Il metodo DrawVideoImageHere disegna un'immagine da un campione multimediale a un contesto di dispositivo specificato.
ms.assetid: b11e1c6b-5a29-444f-a0a9-049cd9d49b13
title: Metodo CDrawImage. DrawVideoImageHere (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.DrawVideoImageHere
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 599dd82e282f2d14ac7e974363a62695e209c080
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327211"
---
# <a name="cdrawimagedrawvideoimagehere-method"></a><span data-ttu-id="88ef4-103">CDrawImage. DrawVideoImageHere, metodo</span><span class="sxs-lookup"><span data-stu-id="88ef4-103">CDrawImage.DrawVideoImageHere method</span></span>

<span data-ttu-id="88ef4-104">Il `DrawVideoImageHere` metodo disegna un'immagine da un campione multimediale a un contesto di dispositivo specificato.</span><span class="sxs-lookup"><span data-stu-id="88ef4-104">The `DrawVideoImageHere` method draws an image from a media sample to a specified device context.</span></span>

## <a name="syntax"></a><span data-ttu-id="88ef4-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="88ef4-105">Syntax</span></span>


```C++
BOOL DrawVideoImageHere(
   HDC          hdc,
   IMediaSample *pMediaSample,
   RECT         *lprcSrc,
   RECT         *lprcDst
);
```



## <a name="parameters"></a><span data-ttu-id="88ef4-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="88ef4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88ef4-107">*HDC*</span><span class="sxs-lookup"><span data-stu-id="88ef4-107">*hdc*</span></span> 
</dt> <dd>

<span data-ttu-id="88ef4-108">Handle per un contesto di dispositivo in cui si verificherà il disegno.</span><span class="sxs-lookup"><span data-stu-id="88ef4-108">Handle to a device context, where the drawing will occur.</span></span>

</dd> <dt>

<span data-ttu-id="88ef4-109">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="88ef4-109">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="88ef4-110">Puntatore all'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) dell'esempio che contiene l'immagine.</span><span class="sxs-lookup"><span data-stu-id="88ef4-110">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the sample that contains the image.</span></span>

</dd> <dt>

<span data-ttu-id="88ef4-111">*lprcSrc*</span><span class="sxs-lookup"><span data-stu-id="88ef4-111">*lprcSrc*</span></span> 
</dt> <dd>

<span data-ttu-id="88ef4-112">Puntatore a un rettangolo di origine da utilizzare per il disegno.</span><span class="sxs-lookup"><span data-stu-id="88ef4-112">Pointer to a source rectangle to use for drawing.</span></span> <span data-ttu-id="88ef4-113">Se **null**, viene utilizzato il rettangolo in [**CDrawImage:: m \_ sourceRect**](cdrawimage-m-sourcerect.md) .</span><span class="sxs-lookup"><span data-stu-id="88ef4-113">If **NULL**, the rectangle in [**CDrawImage::m\_SourceRect**](cdrawimage-m-sourcerect.md) is used.</span></span>

</dd> <dt>

<span data-ttu-id="88ef4-114">*lprcDst*</span><span class="sxs-lookup"><span data-stu-id="88ef4-114">*lprcDst*</span></span> 
</dt> <dd>

<span data-ttu-id="88ef4-115">Puntatore a un rettangolo di destinazione da utilizzare per il disegno.</span><span class="sxs-lookup"><span data-stu-id="88ef4-115">Pointer to a target rectangle to use for drawing.</span></span> <span data-ttu-id="88ef4-116">Se **null**, viene utilizzato il rettangolo in [**CDrawImage:: m \_ targetRect**](cdrawimage-m-targetrect.md) .</span><span class="sxs-lookup"><span data-stu-id="88ef4-116">If **NULL**, the rectangle in [**CDrawImage::m\_TargetRect**](cdrawimage-m-targetrect.md) is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88ef4-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="88ef4-117">Return value</span></span>

<span data-ttu-id="88ef4-118">Restituisce **true** se l'operazione ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="88ef4-118">Returns **TRUE** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="88ef4-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="88ef4-119">Requirements</span></span>



| <span data-ttu-id="88ef4-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="88ef4-120">Requirement</span></span> | <span data-ttu-id="88ef4-121">Valore</span><span class="sxs-lookup"><span data-stu-id="88ef4-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88ef4-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="88ef4-122">Header</span></span><br/>  | <dl> <span data-ttu-id="88ef4-123"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="88ef4-123"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="88ef4-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="88ef4-124">Library</span></span><br/> | <dl> <span data-ttu-id="88ef4-125"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="88ef4-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88ef4-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="88ef4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88ef4-127">**Classe CDrawImage**</span><span class="sxs-lookup"><span data-stu-id="88ef4-127">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 




