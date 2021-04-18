---
description: Il \_ metodo Get bitrate recupera una velocità in bit approssimativa per il video.
ms.assetid: e12e4677-a038-479f-8b64-937ad521c4be
title: Metodo CBaseControlVideo.get_BitRate (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_BitRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 62f1feaed786b397801bbd17d2d2d41c0ccb813d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327571"
---
# <a name="cbasecontrolvideoget_bitrate-method"></a><span data-ttu-id="5aa6e-103">CBaseControlVideo. Get \_ bitrate (metodo)</span><span class="sxs-lookup"><span data-stu-id="5aa6e-103">CBaseControlVideo.get\_BitRate method</span></span>

<span data-ttu-id="5aa6e-104">Il `get_BitRate` metodo recupera una velocità in bit approssimativa per il video.</span><span class="sxs-lookup"><span data-stu-id="5aa6e-104">The `get_BitRate` method retrieves an approximate bit rate for the video.</span></span>

## <a name="syntax"></a><span data-ttu-id="5aa6e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5aa6e-105">Syntax</span></span>


```C++
HRESULT get_BitRate(
   long *pBitRate
);
```



## <a name="parameters"></a><span data-ttu-id="5aa6e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5aa6e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5aa6e-107">*pBitRate*</span><span class="sxs-lookup"><span data-stu-id="5aa6e-107">*pBitRate*</span></span> 
</dt> <dd>

<span data-ttu-id="5aa6e-108">Puntatore alla velocità in bit, in bit al secondo.</span><span class="sxs-lookup"><span data-stu-id="5aa6e-108">Pointer to the bit rate, in bits per second.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5aa6e-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5aa6e-109">Return value</span></span>

<span data-ttu-id="5aa6e-110">Restituisce NOERROR se ha esito positivo o E \_ OutOfMemory se non è disponibile memoria sufficiente.</span><span class="sxs-lookup"><span data-stu-id="5aa6e-110">Returns NOERROR if successful or E\_OUTOFMEMORY if not enough memory is available.</span></span>

## <a name="remarks"></a><span data-ttu-id="5aa6e-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="5aa6e-111">Remarks</span></span>

<span data-ttu-id="5aa6e-112">Questa funzione membro implementa il metodo [**IBasicVideo:: Get \_ bitrate**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_bitrate) .</span><span class="sxs-lookup"><span data-stu-id="5aa6e-112">This member function implements the [**IBasicVideo::get\_BitRate**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_bitrate) method.</span></span> <span data-ttu-id="5aa6e-113">Chiama il CBaseControlVideo virtuale pure [**:: GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) per recuperare la struttura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) dalla classe derivata.</span><span class="sxs-lookup"><span data-stu-id="5aa6e-113">It calls the pure virtual [**CBaseControlVideo::GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) to retrieve the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure from the derived class.</span></span>

## <a name="requirements"></a><span data-ttu-id="5aa6e-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5aa6e-114">Requirements</span></span>



| <span data-ttu-id="5aa6e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="5aa6e-115">Requirement</span></span> | <span data-ttu-id="5aa6e-116">Valore</span><span class="sxs-lookup"><span data-stu-id="5aa6e-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5aa6e-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5aa6e-117">Header</span></span><br/>  | <dl> <span data-ttu-id="5aa6e-118"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5aa6e-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5aa6e-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="5aa6e-119">Library</span></span><br/> | <dl> <span data-ttu-id="5aa6e-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="5aa6e-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5aa6e-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5aa6e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5aa6e-122">**Classe CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="5aa6e-122">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




