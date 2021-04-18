---
description: Il \_ metodo Get BitErrorRate recupera una frequenza degli errori di bit approssimativa per il video.
ms.assetid: 4078611c-6e09-47c8-8e1c-f33bc6ddca79
title: Metodo CBaseControlVideo.get_BitErrorRate (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_BitErrorRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9ae15a882f6dcd8840519f9067223dde3e925f6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327578"
---
# <a name="cbasecontrolvideoget_biterrorrate-method"></a><span data-ttu-id="1576d-103">Metodo CBaseControlVideo. Get \_ BitErrorRate</span><span class="sxs-lookup"><span data-stu-id="1576d-103">CBaseControlVideo.get\_BitErrorRate method</span></span>

<span data-ttu-id="1576d-104">Il `get_BitErrorRate` metodo recupera una frequenza degli errori di bit approssimativa per il video.</span><span class="sxs-lookup"><span data-stu-id="1576d-104">The `get_BitErrorRate` method retrieves an approximate bit error rate for the video.</span></span>

## <a name="syntax"></a><span data-ttu-id="1576d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1576d-105">Syntax</span></span>


```C++
HRESULT get_BitErrorRate(
   long *pBitErrorRate
);
```



## <a name="parameters"></a><span data-ttu-id="1576d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1576d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1576d-107">*pBitErrorRate*</span><span class="sxs-lookup"><span data-stu-id="1576d-107">*pBitErrorRate*</span></span> 
</dt> <dd>

<span data-ttu-id="1576d-108">Puntatore alla frequenza degli errori di bit (un errore per approssimativamente questo numero di bit).</span><span class="sxs-lookup"><span data-stu-id="1576d-108">Pointer to the bit error rate (one error for approximately this many bits).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1576d-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1576d-109">Return value</span></span>

<span data-ttu-id="1576d-110">Restituisce NOERROR se ha esito positivo o E \_ OutOfMemory se la memoria disponibile non è sufficiente.</span><span class="sxs-lookup"><span data-stu-id="1576d-110">Returns NOERROR if successful or E\_OUTOFMEMORY if there is not enough memory available.</span></span>

## <a name="remarks"></a><span data-ttu-id="1576d-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="1576d-111">Remarks</span></span>

<span data-ttu-id="1576d-112">Questa funzione membro implementa il metodo [**IBasicVideo:: Get \_ BitErrorRate**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_biterrorrate) .</span><span class="sxs-lookup"><span data-stu-id="1576d-112">This member function implements the [**IBasicVideo::get\_BitErrorRate**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_biterrorrate) method.</span></span> <span data-ttu-id="1576d-113">Chiama il metodo [**CBaseControlVideo:: GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) virtuale pure per recuperare la struttura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) dalla classe derivata.</span><span class="sxs-lookup"><span data-stu-id="1576d-113">It calls the pure virtual [**CBaseControlVideo::GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) method to retrieve the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure from the derived class.</span></span>

## <a name="requirements"></a><span data-ttu-id="1576d-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1576d-114">Requirements</span></span>



| <span data-ttu-id="1576d-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="1576d-115">Requirement</span></span> | <span data-ttu-id="1576d-116">Valore</span><span class="sxs-lookup"><span data-stu-id="1576d-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1576d-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1576d-117">Header</span></span><br/>  | <dl> <span data-ttu-id="1576d-118"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1576d-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1576d-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="1576d-119">Library</span></span><br/> | <dl> <span data-ttu-id="1576d-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="1576d-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1576d-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1576d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1576d-122">**Classe CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="1576d-122">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




