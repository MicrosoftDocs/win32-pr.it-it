---
description: Il metodo GetImageSize recupera le informazioni sulle dimensioni dell'immagine video.
ms.assetid: a6d7f949-c6a9-49e9-b10a-f6f5bd73dc00
title: Metodo CBaseControlVideo. GetImageSize (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetImageSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ed7795e3998bc101e907bce87c9981e86f51fcb6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333800"
---
# <a name="cbasecontrolvideogetimagesize-method"></a><span data-ttu-id="7f111-103">CBaseControlVideo. GetImageSize, metodo</span><span class="sxs-lookup"><span data-stu-id="7f111-103">CBaseControlVideo.GetImageSize method</span></span>

<span data-ttu-id="7f111-104">Il `GetImageSize` metodo recupera le informazioni sulle dimensioni dell'immagine video.</span><span class="sxs-lookup"><span data-stu-id="7f111-104">The `GetImageSize` method retrieves video image size information.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f111-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7f111-105">Syntax</span></span>


```C++
HRESULT GetImageSize(
   VIDEOINFOHEADER *pVideoInfo,
   long            *pBufferSize,
   RECT            *pSourceRect
);
```



## <a name="parameters"></a><span data-ttu-id="7f111-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7f111-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f111-107">*pVideoInfo*</span><span class="sxs-lookup"><span data-stu-id="7f111-107">*pVideoInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="7f111-108">Puntatore a una struttura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) da compilare.</span><span class="sxs-lookup"><span data-stu-id="7f111-108">Pointer to a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure to be filled in.</span></span>

</dd> <dt>

<span data-ttu-id="7f111-109">*pBufferSize*</span><span class="sxs-lookup"><span data-stu-id="7f111-109">*pBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="7f111-110">Puntatore alla dimensione del buffer video.</span><span class="sxs-lookup"><span data-stu-id="7f111-110">Pointer to the size of the video buffer.</span></span>

</dd> <dt>

<span data-ttu-id="7f111-111">*pSourceRect*</span><span class="sxs-lookup"><span data-stu-id="7f111-111">*pSourceRect*</span></span> 
</dt> <dd>

<span data-ttu-id="7f111-112">Puntatore alle dimensioni del rettangolo del video di origine.</span><span class="sxs-lookup"><span data-stu-id="7f111-112">Pointer to the rectangle dimensions of the source video.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f111-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7f111-113">Return value</span></span>

<span data-ttu-id="7f111-114">Restituisce un valore **HRESULT** che dipende dall'implementazione di. può essere uno dei valori seguenti oppure altri valori non sono elencati.</span><span class="sxs-lookup"><span data-stu-id="7f111-114">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="7f111-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="7f111-115">Return code</span></span>                                                                                  | <span data-ttu-id="7f111-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7f111-116">Description</span></span>                                                               |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7f111-117"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="7f111-117"><dt>**E\_FAIL**</dt></span></span> </dl>       | <span data-ttu-id="7f111-118">Esito negativo.</span><span class="sxs-lookup"><span data-stu-id="7f111-118">Failure.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="7f111-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="7f111-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="7f111-120">Argomento non valido.</span><span class="sxs-lookup"><span data-stu-id="7f111-120">Invalid argument.</span></span> <span data-ttu-id="7f111-121">Il formato dei dati non è compatibile.</span><span class="sxs-lookup"><span data-stu-id="7f111-121">The data format is not compatible.</span></span><br/>           |
| <dl> <span data-ttu-id="7f111-122"><dt>**E \_ imprevisto**</dt></span><span class="sxs-lookup"><span data-stu-id="7f111-122"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="7f111-123">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="7f111-123">Unexpected error occurred.</span></span> <span data-ttu-id="7f111-124">Uno o più argomenti sono **null**.</span><span class="sxs-lookup"><span data-stu-id="7f111-124">One or more arguments are **NULL**.</span></span><br/> |
| <dl> <span data-ttu-id="7f111-125"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="7f111-125"><dt>**NOERROR**</dt></span></span> </dl>       | <span data-ttu-id="7f111-126">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="7f111-126">Success.</span></span><br/>                                                       |



 

## <a name="remarks"></a><span data-ttu-id="7f111-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="7f111-127">Remarks</span></span>

<span data-ttu-id="7f111-128">Questa funzione membro è una funzione helper usata per la creazione di rendering di immagini di memoria per immagini DIB.</span><span class="sxs-lookup"><span data-stu-id="7f111-128">This member function is a helper function used for creating memory image renderings of DIB images.</span></span> <span data-ttu-id="7f111-129">Viene chiamato dall'implementazione della classe di base di [**CBaseControlVideo:: GetCurrentImage**](cbasecontrolvideo-getcurrentimage.md) quando un parametro _pVideoImage_ **null** viene passato a tale funzione membro.</span><span class="sxs-lookup"><span data-stu-id="7f111-129">It is called from the base class implementation of [**CBaseControlVideo::GetCurrentImage**](cbasecontrolvideo-getcurrentimage.md) when a **NULL**_pVideoImage_ parameter is passed to that member function.</span></span> <span data-ttu-id="7f111-130">Di conseguenza, questa funzione membro costruisce e restituisce una struttura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) , usando le informazioni in *pBufferSize* e *pSourceRect*.</span><span class="sxs-lookup"><span data-stu-id="7f111-130">As a result, this member function constructs and returns a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure, using the information in *pBufferSize* and *pSourceRect*.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f111-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7f111-131">Requirements</span></span>



| <span data-ttu-id="7f111-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f111-132">Requirement</span></span> | <span data-ttu-id="7f111-133">Valore</span><span class="sxs-lookup"><span data-stu-id="7f111-133">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f111-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7f111-134">Header</span></span><br/>  | <dl> <span data-ttu-id="7f111-135"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7f111-135"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7f111-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="7f111-136">Library</span></span><br/> | <dl> <span data-ttu-id="7f111-137"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="7f111-137"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f111-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7f111-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f111-139">**Classe CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="7f111-139">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




