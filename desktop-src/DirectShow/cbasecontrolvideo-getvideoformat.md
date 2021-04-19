---
description: Il metodo GetVideoFormat recupera un esempio video che rappresenta il formato video corrente.
ms.assetid: f7457c5b-037c-4a63-963e-0fc6086609a4
title: Metodo CBaseControlVideo. GetVideoFormat (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetVideoFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d84b64818a02a60073fc21411e4a99bde07a6e00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332085"
---
# <a name="cbasecontrolvideogetvideoformat-method"></a><span data-ttu-id="1a5d6-103">CBaseControlVideo. GetVideoFormat, metodo</span><span class="sxs-lookup"><span data-stu-id="1a5d6-103">CBaseControlVideo.GetVideoFormat method</span></span>

<span data-ttu-id="1a5d6-104">Il `GetVideoFormat` metodo recupera un esempio video che rappresenta il formato video corrente.</span><span class="sxs-lookup"><span data-stu-id="1a5d6-104">The `GetVideoFormat` method retrieves a video sample that represents the current video format.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a5d6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1a5d6-105">Syntax</span></span>


```C++
virtual VIDEOINFOHEADER* GetVideoFormat() = 0;
```



## <a name="parameters"></a><span data-ttu-id="1a5d6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1a5d6-106">Parameters</span></span>

<span data-ttu-id="1a5d6-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="1a5d6-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1a5d6-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1a5d6-108">Return value</span></span>

<span data-ttu-id="1a5d6-109">Restituisce un puntatore a una struttura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) che contiene il formato video corrente.</span><span class="sxs-lookup"><span data-stu-id="1a5d6-109">Returns a pointer to a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure that contains the current video format.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a5d6-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="1a5d6-110">Remarks</span></span>

<span data-ttu-id="1a5d6-111">Per restituire e controllare determinate informazioni tramite [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo), è necessario che l'oggetto conosca il formato video corrente.</span><span class="sxs-lookup"><span data-stu-id="1a5d6-111">To return and check certain information through [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo), the object must know the current video format.</span></span> <span data-ttu-id="1a5d6-112">Ottiene queste informazioni chiamando il metodo virtuale pure che le classi derivate devono eseguire l'override.</span><span class="sxs-lookup"><span data-stu-id="1a5d6-112">It gets this information by calling this pure virtual method that derived classes must override.</span></span> <span data-ttu-id="1a5d6-113">Questa funzione membro viene chiamata dalle funzioni membro [**CBaseControlVideo**](cbasecontrolvideo.md) seguenti.</span><span class="sxs-lookup"><span data-stu-id="1a5d6-113">This member function is called by the following [**CBaseControlVideo**](cbasecontrolvideo.md) member functions.</span></span>

-   [<span data-ttu-id="1a5d6-114">**CBaseControlVideo::OnVideoSizeChange**</span><span class="sxs-lookup"><span data-stu-id="1a5d6-114">**CBaseControlVideo::OnVideoSizeChange**</span></span>](cbasecontrolvideo-onvideosizechange.md)
-   [<span data-ttu-id="1a5d6-115">**CBaseControlVideo:: Get \_ AvgTimePerFrame**</span><span class="sxs-lookup"><span data-stu-id="1a5d6-115">**CBaseControlVideo::get\_AvgTimePerFrame**</span></span>](cbasecontrolvideo-get-avgtimeperframe.md)
-   [<span data-ttu-id="1a5d6-116">**CBaseControlVideo:: Get \_ bitrate**</span><span class="sxs-lookup"><span data-stu-id="1a5d6-116">**CBaseControlVideo::get\_BitRate**</span></span>](cbasecontrolvideo-get-bitrate.md)
-   [<span data-ttu-id="1a5d6-117">**CBaseControlVideo:: Get \_ BitErrorRate**</span><span class="sxs-lookup"><span data-stu-id="1a5d6-117">**CBaseControlVideo::get\_BitErrorRate**</span></span>](cbasecontrolvideo-get-biterrorrate.md)
-   [<span data-ttu-id="1a5d6-118">**CBaseControlVideo:: Get \_ VideoWidth**</span><span class="sxs-lookup"><span data-stu-id="1a5d6-118">**CBaseControlVideo::get\_VideoWidth**</span></span>](cbasecontrolvideo-get-videowidth.md)
-   [<span data-ttu-id="1a5d6-119">**CBaseControlVideo:: Get \_ VideoHeight**</span><span class="sxs-lookup"><span data-stu-id="1a5d6-119">**CBaseControlVideo::get\_VideoHeight**</span></span>](cbasecontrolvideo-get-videoheight.md)
-   [<span data-ttu-id="1a5d6-120">**CBaseControlVideo::GetVideoPaletteEntries**</span><span class="sxs-lookup"><span data-stu-id="1a5d6-120">**CBaseControlVideo::GetVideoPaletteEntries**</span></span>](cbasecontrolvideo-getvideopaletteentries.md)
-   [<span data-ttu-id="1a5d6-121">**CBaseControlVideo::GetVideoSize**</span><span class="sxs-lookup"><span data-stu-id="1a5d6-121">**CBaseControlVideo::GetVideoSize**</span></span>](cbasecontrolvideo-getvideosize.md)

## <a name="requirements"></a><span data-ttu-id="1a5d6-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1a5d6-122">Requirements</span></span>



| <span data-ttu-id="1a5d6-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a5d6-123">Requirement</span></span> | <span data-ttu-id="1a5d6-124">Valore</span><span class="sxs-lookup"><span data-stu-id="1a5d6-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a5d6-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1a5d6-125">Header</span></span><br/>  | <dl> <span data-ttu-id="1a5d6-126"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1a5d6-126"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1a5d6-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="1a5d6-127">Library</span></span><br/> | <dl> <span data-ttu-id="1a5d6-128"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="1a5d6-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a5d6-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1a5d6-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a5d6-130">**Classe CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="1a5d6-130">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




