---
description: Il \_ metodo Get VideoHeight recupera l'altezza del video nativo.
ms.assetid: f33ba789-f9c6-47f1-879b-241bfdc72010
title: Metodo CBaseControlVideo.get_VideoHeight (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_VideoHeight
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4e738636cecd8031962ae31ebf54ac258d868013
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327556"
---
# <a name="cbasecontrolvideoget_videoheight-method"></a><span data-ttu-id="4984c-103">Metodo CBaseControlVideo. Get \_ VideoHeight</span><span class="sxs-lookup"><span data-stu-id="4984c-103">CBaseControlVideo.get\_VideoHeight method</span></span>

<span data-ttu-id="4984c-104">Il `get_VideoHeight` metodo recupera l'altezza del video nativo.</span><span class="sxs-lookup"><span data-stu-id="4984c-104">The `get_VideoHeight` method retrieves the height of the native video.</span></span>

## <a name="syntax"></a><span data-ttu-id="4984c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4984c-105">Syntax</span></span>


```C++
HRESULT get_VideoHeight(
   long *pVideoHeight
);
```



## <a name="parameters"></a><span data-ttu-id="4984c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4984c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4984c-107">*pVideoHeight*</span><span class="sxs-lookup"><span data-stu-id="4984c-107">*pVideoHeight*</span></span> 
</dt> <dd>

<span data-ttu-id="4984c-108">Puntatore all'altezza, in pixel, del video nativo.</span><span class="sxs-lookup"><span data-stu-id="4984c-108">Pointer to the height of the native video, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4984c-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4984c-109">Return value</span></span>

<span data-ttu-id="4984c-110">Restituisce NOERROR se ha esito positivo o E \_ OutOfMemory se la memoria disponibile non è sufficiente.</span><span class="sxs-lookup"><span data-stu-id="4984c-110">Returns NOERROR if successful or E\_OUTOFMEMORY if there is not enough memory available.</span></span>

## <a name="remarks"></a><span data-ttu-id="4984c-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="4984c-111">Remarks</span></span>

<span data-ttu-id="4984c-112">Questa funzione membro implementa il metodo [**IBasicVideo:: Get \_ VideoHeight**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_videoheight) .</span><span class="sxs-lookup"><span data-stu-id="4984c-112">This member function implements the [**IBasicVideo::get\_VideoHeight**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_videoheight) method.</span></span> <span data-ttu-id="4984c-113">Chiama il CBaseControlVideo virtuale pure [**:: GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) per recuperare la struttura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) dalla classe derivata.</span><span class="sxs-lookup"><span data-stu-id="4984c-113">It calls the pure virtual [**CBaseControlVideo::GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) to retrieve the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure from the derived class.</span></span>

## <a name="requirements"></a><span data-ttu-id="4984c-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4984c-114">Requirements</span></span>



| <span data-ttu-id="4984c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="4984c-115">Requirement</span></span> | <span data-ttu-id="4984c-116">Valore</span><span class="sxs-lookup"><span data-stu-id="4984c-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4984c-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4984c-117">Header</span></span><br/>  | <dl> <span data-ttu-id="4984c-118"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4984c-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4984c-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="4984c-119">Library</span></span><br/> | <dl> <span data-ttu-id="4984c-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="4984c-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4984c-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4984c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4984c-122">**Classe CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="4984c-122">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




