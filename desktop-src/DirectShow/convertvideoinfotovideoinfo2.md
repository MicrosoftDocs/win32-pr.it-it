---
description: La funzione ConvertVideoInfoToVideoInfo2 converte un tipo di supporto che usa VIDEOINFOHEADER in uno che usa VIDEOINFOHEADER2.
ms.assetid: d938bfc0-a5ae-475b-b183-56ff39b4bae1
title: Funzione ConvertVideoInfoToVideoInfo2 (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConvertVideoInfoToVideoInfo2
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 54611c83c30ad65a806a077dc51c933a9f881636
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324003"
---
# <a name="convertvideoinfotovideoinfo2-function"></a><span data-ttu-id="b1134-103">ConvertVideoInfoToVideoInfo2 (funzione)</span><span class="sxs-lookup"><span data-stu-id="b1134-103">ConvertVideoInfoToVideoInfo2 function</span></span>

<span data-ttu-id="b1134-104">La `ConvertVideoInfoToVideoInfo2` funzione converte un tipo di supporto che usa [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) in uno che usa [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2).</span><span class="sxs-lookup"><span data-stu-id="b1134-104">The `ConvertVideoInfoToVideoInfo2` function converts a media type that uses [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) to one that uses [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2).</span></span>

## <a name="syntax"></a><span data-ttu-id="b1134-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b1134-105">Syntax</span></span>


```C++
HRESULT STDAPI ConvertVideoInfoToVideoInfo2(
   AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="b1134-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b1134-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1134-107">*PMT*</span><span class="sxs-lookup"><span data-stu-id="b1134-107">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="b1134-108">Puntatore alla struttura [**del \_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) da convertire.</span><span class="sxs-lookup"><span data-stu-id="b1134-108">Pointer to the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure to convert.</span></span> <span data-ttu-id="b1134-109">Il formato del tipo di formato della struttura deve essere \_ videoinfo.</span><span class="sxs-lookup"><span data-stu-id="b1134-109">The structure must have format type FORMAT\_VideoInfo.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1134-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b1134-110">Return value</span></span>

<span data-ttu-id="b1134-111">Restituisce S \_ OK o e \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="b1134-111">Returns S\_OK or E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1134-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="b1134-112">Remarks</span></span>

<span data-ttu-id="b1134-113">Questa funzione alloca una nuova struttura **VIDEOINFOHEADER2** , ne copia i membri della struttura **VIDEOINFOHEADER** e sostituisce la struttura precedente con la nuova struttura nel blocco di formato del tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="b1134-113">This function allocates a new **VIDEOINFOHEADER2** structure, copies the members of the **VIDEOINFOHEADER** structure into it, and replaces the old structure with the new structure in the format block of the media type.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1134-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b1134-114">Requirements</span></span>



| <span data-ttu-id="b1134-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1134-115">Requirement</span></span> | <span data-ttu-id="b1134-116">Valore</span><span class="sxs-lookup"><span data-stu-id="b1134-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1134-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b1134-117">Header</span></span><br/>  | <dl> <span data-ttu-id="b1134-118"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b1134-118"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b1134-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="b1134-119">Library</span></span><br/> | <dl> <span data-ttu-id="b1134-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b1134-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1134-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b1134-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1134-122">Funzioni video e immagine</span><span class="sxs-lookup"><span data-stu-id="b1134-122">Video and Image Functions</span></span>](video-and-image-functions.md)
</dt> </dl>

 

 




