---
description: Il \_ metodo Get AvgTimePerFrame Recupera il tempo medio per frame.
ms.assetid: bcfdb241-9ec1-49f4-b2b5-0869c27da953
title: Metodo CBaseControlVideo.get_AvgTimePerFrame (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_AvgTimePerFrame
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ae69140348be6e2fdfc120ee7fb40096d663f720
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327579"
---
# <a name="cbasecontrolvideoget_avgtimeperframe-method"></a><span data-ttu-id="bf487-103">Metodo CBaseControlVideo. Get \_ AvgTimePerFrame</span><span class="sxs-lookup"><span data-stu-id="bf487-103">CBaseControlVideo.get\_AvgTimePerFrame method</span></span>

<span data-ttu-id="bf487-104">Il `get_AvgTimePerFrame` metodo recupera il tempo medio per frame.</span><span class="sxs-lookup"><span data-stu-id="bf487-104">The `get_AvgTimePerFrame` method retrieves the average time per frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf487-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bf487-105">Syntax</span></span>


```C++
HRESULT get_AvgTimePerFrame(
   REFTIME *pAvgTimePerFrame
);
```



## <a name="parameters"></a><span data-ttu-id="bf487-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="bf487-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf487-107">*pAvgTimePerFrame*</span><span class="sxs-lookup"><span data-stu-id="bf487-107">*pAvgTimePerFrame*</span></span> 
</dt> <dd>

<span data-ttu-id="bf487-108">Puntatore al tempo medio per frame.</span><span class="sxs-lookup"><span data-stu-id="bf487-108">Pointer to the average time per frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf487-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bf487-109">Return value</span></span>

<span data-ttu-id="bf487-110">Restituisce NOERROR se ha esito positivo o E \_ OutOfMemory se la memoria disponibile non è sufficiente.</span><span class="sxs-lookup"><span data-stu-id="bf487-110">Returns NOERROR if successful or E\_OUTOFMEMORY if there is not enough memory available.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf487-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="bf487-111">Remarks</span></span>

<span data-ttu-id="bf487-112">Questa funzione membro implementa il metodo [**IBasicVideo:: Get \_ AvgTimePerFrame**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_avgtimeperframe) .</span><span class="sxs-lookup"><span data-stu-id="bf487-112">This member function implements the [**IBasicVideo::get\_AvgTimePerFrame**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_avgtimeperframe) method.</span></span> <span data-ttu-id="bf487-113">Chiama la funzione membro [**CBaseControlVideo:: GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) virtuale pure per recuperare la struttura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) dalla classe derivata.</span><span class="sxs-lookup"><span data-stu-id="bf487-113">It calls the pure virtual [**CBaseControlVideo::GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) member function to retrieve the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure from the derived class.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf487-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bf487-114">Requirements</span></span>



| <span data-ttu-id="bf487-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf487-115">Requirement</span></span> | <span data-ttu-id="bf487-116">Valore</span><span class="sxs-lookup"><span data-stu-id="bf487-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf487-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bf487-117">Header</span></span><br/>  | <dl> <span data-ttu-id="bf487-118"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bf487-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="bf487-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="bf487-119">Library</span></span><br/> | <dl> <span data-ttu-id="bf487-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="bf487-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf487-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bf487-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf487-122">**Classe CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="bf487-122">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




