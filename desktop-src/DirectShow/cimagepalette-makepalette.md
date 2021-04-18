---
description: Il metodo MakePalette crea una tavolozza logica dalla tabella dei colori in formato video.
ms.assetid: f158e529-d683-4210-818d-21a834fc7683
title: Metodo CImagePalette. MakePalette (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.MakePalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 20c4484b2666b25b5d713ede450a9a5a99f93348
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325064"
---
# <a name="cimagepalettemakepalette-method"></a><span data-ttu-id="8fcf2-103">CImagePalette. MakePalette, metodo</span><span class="sxs-lookup"><span data-stu-id="8fcf2-103">CImagePalette.MakePalette method</span></span>

<span data-ttu-id="8fcf2-104">Il `MakePalette` metodo crea una tavolozza logica dalla tabella dei colori in un formato video.</span><span class="sxs-lookup"><span data-stu-id="8fcf2-104">The `MakePalette` method creates a logical palette from the color table in a video format.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fcf2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8fcf2-105">Syntax</span></span>


```C++
HPALETTE MakePalette(
   const VIDEOINFOHEADER *pVideoInfo,
         LPSTR           szDevice
);
```



## <a name="parameters"></a><span data-ttu-id="8fcf2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8fcf2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8fcf2-107">*pVideoInfo*</span><span class="sxs-lookup"><span data-stu-id="8fcf2-107">*pVideoInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="8fcf2-108">Puntatore a una struttura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) contenente la tabella dei colori.</span><span class="sxs-lookup"><span data-stu-id="8fcf2-108">Pointer to a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure that contains the color table.</span></span>

</dd> <dt>

<span data-ttu-id="8fcf2-109">*szDevice*</span><span class="sxs-lookup"><span data-stu-id="8fcf2-109">*szDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="8fcf2-110">Puntatore a una stringa che contiene il nome del dispositivo di visualizzazione, come restituito dalla funzione **ENUMDISPLAYDEVICES** GDI.</span><span class="sxs-lookup"><span data-stu-id="8fcf2-110">Pointer to a string that contains the name of the display device, as returned by the GDI **EnumDisplayDevices** function.</span></span> <span data-ttu-id="8fcf2-111">Per usare il dispositivo di visualizzazione principale, impostare questo parametro su **null**.</span><span class="sxs-lookup"><span data-stu-id="8fcf2-111">To use the main display device, set this parameter to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8fcf2-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8fcf2-112">Return value</span></span>

<span data-ttu-id="8fcf2-113">Se ha esito positivo, restituisce un handle per la tavolozza.</span><span class="sxs-lookup"><span data-stu-id="8fcf2-113">If successful, returns a handle to the palette.</span></span> <span data-ttu-id="8fcf2-114">In caso contrario, restituisce **null**.</span><span class="sxs-lookup"><span data-stu-id="8fcf2-114">Otherwise, returns **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="8fcf2-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8fcf2-115">Requirements</span></span>



| <span data-ttu-id="8fcf2-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="8fcf2-116">Requirement</span></span> | <span data-ttu-id="8fcf2-117">Valore</span><span class="sxs-lookup"><span data-stu-id="8fcf2-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8fcf2-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8fcf2-118">Header</span></span><br/>  | <dl> <span data-ttu-id="8fcf2-119"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8fcf2-119"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8fcf2-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="8fcf2-120">Library</span></span><br/> | <dl> <span data-ttu-id="8fcf2-121"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="8fcf2-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8fcf2-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8fcf2-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fcf2-123">**Classe CImagePalette**</span><span class="sxs-lookup"><span data-stu-id="8fcf2-123">**CImagePalette Class**</span></span>](cimagepalette.md)
</dt> </dl>

 

 




