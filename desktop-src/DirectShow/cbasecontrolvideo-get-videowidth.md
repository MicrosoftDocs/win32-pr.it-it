---
description: Il \_ metodo Get VideoWidth recupera la larghezza del video nativo.
ms.assetid: dfd897f0-f580-44c0-9445-ba61ae267187
title: Metodo CBaseControlVideo.get_VideoWidth (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_VideoWidth
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: faeeed7ea8af58103e74d9b8c3690523c893282f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333805"
---
# <a name="cbasecontrolvideoget_videowidth-method"></a><span data-ttu-id="2fb52-103">Metodo CBaseControlVideo. Get \_ VideoWidth</span><span class="sxs-lookup"><span data-stu-id="2fb52-103">CBaseControlVideo.get\_VideoWidth method</span></span>

<span data-ttu-id="2fb52-104">Il `get_VideoWidth` metodo recupera la larghezza del video nativo.</span><span class="sxs-lookup"><span data-stu-id="2fb52-104">The `get_VideoWidth` method retrieves the width of the native video.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fb52-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2fb52-105">Syntax</span></span>


```C++
HRESULT get_VideoWidth(
   long *pVideoWidth
);
```



## <a name="parameters"></a><span data-ttu-id="2fb52-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2fb52-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2fb52-107">*pVideoWidth*</span><span class="sxs-lookup"><span data-stu-id="2fb52-107">*pVideoWidth*</span></span> 
</dt> <dd>

<span data-ttu-id="2fb52-108">Puntatore alla larghezza del video nativo, in pixel.</span><span class="sxs-lookup"><span data-stu-id="2fb52-108">Pointer to the width of the native video, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2fb52-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2fb52-109">Return value</span></span>

<span data-ttu-id="2fb52-110">Restituisce NOERROR se ha esito positivo o E \_ OutOfMemory se la memoria disponibile non è sufficiente.</span><span class="sxs-lookup"><span data-stu-id="2fb52-110">Returns NOERROR if successful or E\_OUTOFMEMORY if there is not enough memory available.</span></span>

## <a name="remarks"></a><span data-ttu-id="2fb52-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="2fb52-111">Remarks</span></span>

<span data-ttu-id="2fb52-112">Questa funzione membro implementa il metodo [**IBasicVideo:: Get \_ VideoWidth**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_videowidth) .</span><span class="sxs-lookup"><span data-stu-id="2fb52-112">This member function implements the [**IBasicVideo::get\_VideoWidth**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_videowidth) method.</span></span> <span data-ttu-id="2fb52-113">Chiama il CBaseControlVideo virtuale pure [**:: GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) per recuperare la struttura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) dalla classe derivata.</span><span class="sxs-lookup"><span data-stu-id="2fb52-113">It calls the pure virtual [**CBaseControlVideo::GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) to retrieve the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure from the derived class.</span></span>

## <a name="requirements"></a><span data-ttu-id="2fb52-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2fb52-114">Requirements</span></span>



| <span data-ttu-id="2fb52-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="2fb52-115">Requirement</span></span> | <span data-ttu-id="2fb52-116">Valore</span><span class="sxs-lookup"><span data-stu-id="2fb52-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2fb52-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2fb52-117">Header</span></span><br/>  | <dl> <span data-ttu-id="2fb52-118"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2fb52-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2fb52-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="2fb52-119">Library</span></span><br/> | <dl> <span data-ttu-id="2fb52-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="2fb52-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2fb52-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2fb52-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fb52-122">**Classe CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="2fb52-122">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




