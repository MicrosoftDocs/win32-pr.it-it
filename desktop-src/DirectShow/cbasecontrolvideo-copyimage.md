---
description: Crea una copia di memoria di un'immagine.
ms.assetid: 83a980bc-1298-439f-8dfc-49534591977f
title: Metodo CBaseControlVideo. CopyImage (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.CopyImage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 23ada87e77d3c3441f489abed2e7af86a2a556ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327580"
---
# <a name="cbasecontrolvideocopyimage-method"></a><span data-ttu-id="a9ee1-103">CBaseControlVideo. CopyImage, metodo</span><span class="sxs-lookup"><span data-stu-id="a9ee1-103">CBaseControlVideo.CopyImage method</span></span>

<span data-ttu-id="a9ee1-104">Crea una copia di memoria di un'immagine.</span><span class="sxs-lookup"><span data-stu-id="a9ee1-104">Creates a memory copy of an image.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9ee1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a9ee1-105">Syntax</span></span>


```C++
HRESULT CopyImage(
   IMediaSample    *pMediaSample,
   VIDEOINFOHEADER *pVideoInfo,
   LONG            *pBufferSize,
   BYTE            *pVideoImage,
   RECT            *pSourceRect
);
```



## <a name="parameters"></a><span data-ttu-id="a9ee1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a9ee1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9ee1-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="a9ee1-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="a9ee1-108">Puntatore all'esempio che contiene l'immagine del video.</span><span class="sxs-lookup"><span data-stu-id="a9ee1-108">Pointer to the sample containing the video image.</span></span>

</dd> <dt>

<span data-ttu-id="a9ee1-109">*pVideoInfo*</span><span class="sxs-lookup"><span data-stu-id="a9ee1-109">*pVideoInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="a9ee1-110">Puntatore al formato che rappresenta l'immagine del video.</span><span class="sxs-lookup"><span data-stu-id="a9ee1-110">Pointer to the format representing the video image.</span></span>

</dd> <dt>

<span data-ttu-id="a9ee1-111">*pBufferSize*</span><span class="sxs-lookup"><span data-stu-id="a9ee1-111">*pBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="a9ee1-112">Puntatore alla dimensione del buffer di output.</span><span class="sxs-lookup"><span data-stu-id="a9ee1-112">Pointer to the size of the output buffer.</span></span>

</dd> <dt>

<span data-ttu-id="a9ee1-113">*pVideoImage*</span><span class="sxs-lookup"><span data-stu-id="a9ee1-113">*pVideoImage*</span></span> 
</dt> <dd>

<span data-ttu-id="a9ee1-114">Puntatore al buffer di output.</span><span class="sxs-lookup"><span data-stu-id="a9ee1-114">Pointer to the output buffer.</span></span>

</dd> <dt>

<span data-ttu-id="a9ee1-115">*pSourceRect*</span><span class="sxs-lookup"><span data-stu-id="a9ee1-115">*pSourceRect*</span></span> 
</dt> <dd>

<span data-ttu-id="a9ee1-116">Puntatore al rettangolo del video di origine.</span><span class="sxs-lookup"><span data-stu-id="a9ee1-116">Pointer to the source video rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9ee1-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a9ee1-117">Return value</span></span>

<span data-ttu-id="a9ee1-118">Se il parametro *pVideoImage* è **null**, il parametro *pBufferSize* viene compilato con il numero di byte che il buffer di output richiede per archiviare l'immagine.</span><span class="sxs-lookup"><span data-stu-id="a9ee1-118">If the *pVideoImage* parameter is **NULL**, the *pBufferSize* parameter is filled in with the number of bytes the output buffer requires to store the image.</span></span> <span data-ttu-id="a9ee1-119">Se il buffer passato è troppo piccolo o la funzione membro non riesce ad allocare memoria sufficiente, la funzione membro restituisce E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="a9ee1-119">If the buffer passed in is too small or the member function fails to allocate sufficient memory, the member function returns E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9ee1-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="a9ee1-120">Remarks</span></span>

<span data-ttu-id="a9ee1-121">La funzione membro recupera l'immagine dall'esempio e la copia nel buffer di output.</span><span class="sxs-lookup"><span data-stu-id="a9ee1-121">The member function retrieves the image from the sample and copies it into the output buffer.</span></span> <span data-ttu-id="a9ee1-122">La sezione del video copiato nel buffer di output riflette il rettangolo di origine impostato tramite l'interfaccia [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) (anche se non riflette il rettangolo di destinazione).</span><span class="sxs-lookup"><span data-stu-id="a9ee1-122">The section of video copied into the output buffer reflects the source rectangle that is set through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface (although it does not reflect the destination rectangle).</span></span>

## <a name="requirements"></a><span data-ttu-id="a9ee1-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a9ee1-123">Requirements</span></span>



| <span data-ttu-id="a9ee1-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9ee1-124">Requirement</span></span> | <span data-ttu-id="a9ee1-125">Valore</span><span class="sxs-lookup"><span data-stu-id="a9ee1-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9ee1-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a9ee1-126">Header</span></span><br/>  | <dl> <span data-ttu-id="a9ee1-127"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a9ee1-127"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a9ee1-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="a9ee1-128">Library</span></span><br/> | <dl> <span data-ttu-id="a9ee1-129"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="a9ee1-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9ee1-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a9ee1-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9ee1-131">**Classe CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="a9ee1-131">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




