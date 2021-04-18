---
description: Il metodo GetTargetRect Recupera il rettangolo di destinazione. Si tratta di una funzione membro Helper interna.
ms.assetid: bf9d95c9-eee8-46b8-bdee-a7d16777ed83
title: Metodo CBaseControlVideo. GetTargetRect (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d59a12e134edf37c8ab0a63f46f77923b112605d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327843"
---
# <a name="cbasecontrolvideogettargetrect-method"></a><span data-ttu-id="eaf00-104">CBaseControlVideo. GetTargetRect, metodo</span><span class="sxs-lookup"><span data-stu-id="eaf00-104">CBaseControlVideo.GetTargetRect method</span></span>

<span data-ttu-id="eaf00-105">Il `GetTargetRect` metodo recupera il rettangolo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="eaf00-105">The `GetTargetRect` method retrieves the destination rectangle.</span></span> <span data-ttu-id="eaf00-106">Si tratta di una funzione membro Helper interna.</span><span class="sxs-lookup"><span data-stu-id="eaf00-106">This is an internal helper member function.</span></span>

## <a name="syntax"></a><span data-ttu-id="eaf00-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="eaf00-107">Syntax</span></span>


```C++
virtual HRESULT GetTargetRect(
   RECT *pTargetRect
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="eaf00-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="eaf00-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eaf00-109">*pTargetRect*</span><span class="sxs-lookup"><span data-stu-id="eaf00-109">*pTargetRect*</span></span> 
</dt> <dd>

<span data-ttu-id="eaf00-110">Puntatore al rettangolo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="eaf00-110">Pointer to the destination rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eaf00-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="eaf00-111">Return value</span></span>

<span data-ttu-id="eaf00-112">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="eaf00-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="eaf00-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="eaf00-113">Remarks</span></span>

<span data-ttu-id="eaf00-114">Questa funzione membro deve essere sottoposta a override nella classe derivata per restituire il rettangolo di destinazione utilizzato dal renderer video.</span><span class="sxs-lookup"><span data-stu-id="eaf00-114">This member function must be overridden in the derived class to return the target rectangle held by the video renderer.</span></span> <span data-ttu-id="eaf00-115">Viene chiamato dalle funzioni membro [**CBaseControlVideo**](cbasecontrolvideo.md) seguenti.</span><span class="sxs-lookup"><span data-stu-id="eaf00-115">It is called from the following [**CBaseControlVideo**](cbasecontrolvideo.md) member functions.</span></span>

-   [<span data-ttu-id="eaf00-116">**CBaseControlVideo::GetDestinationPosition**</span><span class="sxs-lookup"><span data-stu-id="eaf00-116">**CBaseControlVideo::GetDestinationPosition**</span></span>](cbasecontrolvideo-getdestinationposition.md)
-   [<span data-ttu-id="eaf00-117">**CBaseControlVideo::p UT \_ DestinationLeft**</span><span class="sxs-lookup"><span data-stu-id="eaf00-117">**CBaseControlVideo::put\_DestinationLeft**</span></span>](cbasecontrolvideo-put-destinationleft.md)
-   [<span data-ttu-id="eaf00-118">**CBaseControlVideo:: Get \_ DestinationLeft**</span><span class="sxs-lookup"><span data-stu-id="eaf00-118">**CBaseControlVideo::get\_DestinationLeft**</span></span>](cbasecontrolvideo-get-destinationleft.md)
-   [<span data-ttu-id="eaf00-119">**CBaseControlVideo::p UT \_ DestinationWidth**</span><span class="sxs-lookup"><span data-stu-id="eaf00-119">**CBaseControlVideo::put\_DestinationWidth**</span></span>](cbasecontrolvideo-put-destinationwidth.md)
-   [<span data-ttu-id="eaf00-120">**CBaseControlVideo:: Get \_ DestinationWidth**</span><span class="sxs-lookup"><span data-stu-id="eaf00-120">**CBaseControlVideo::get\_DestinationWidth**</span></span>](cbasecontrolvideo-get-destinationwidth.md)
-   [<span data-ttu-id="eaf00-121">**CBaseControlVideo::p UT \_ DestinationTop**</span><span class="sxs-lookup"><span data-stu-id="eaf00-121">**CBaseControlVideo::put\_DestinationTop**</span></span>](cbasecontrolvideo-put-destinationtop.md)
-   [<span data-ttu-id="eaf00-122">**CBaseControlVideo:: Get \_ DestinationTop**</span><span class="sxs-lookup"><span data-stu-id="eaf00-122">**CBaseControlVideo::get\_DestinationTop**</span></span>](cbasecontrolvideo-get-destinationtop.md)
-   [<span data-ttu-id="eaf00-123">**CBaseControlVideo::p UT \_ DestinationHeight**</span><span class="sxs-lookup"><span data-stu-id="eaf00-123">**CBaseControlVideo::put\_DestinationHeight**</span></span>](cbasecontrolvideo-put-destinationheight.md)
-   [<span data-ttu-id="eaf00-124">**CBaseControlVideo:: Get \_ DestinationHeight**</span><span class="sxs-lookup"><span data-stu-id="eaf00-124">**CBaseControlVideo::get\_DestinationHeight**</span></span>](cbasecontrolvideo-get-destinationheight.md)

<span data-ttu-id="eaf00-125">Nell'esempio seguente viene illustrata un'implementazione di questa funzione in una classe derivata.</span><span class="sxs-lookup"><span data-stu-id="eaf00-125">The following example demonstrates an implementation of this function in a derived class.</span></span>


```C++
// Return the current destination rectangle.
HRESULT CVideoText::GetTargetRect(RECT *pTargetRect)
{
    ASSERT(pTargetRect);
    m_pRenderer->m_DrawImage.GetTargetRect(pTargetRect);
    return NOERROR;
}
```



<span data-ttu-id="eaf00-126">In questo esempio, CVideoText è una classe derivata da [**CBaseControlVideo**](cbasecontrolvideo.md), m \_ pRenderer include un oggetto di una classe derivata da [**CBaseVideoRenderer**](cbasevideorenderer.md)e il \_ membro dati DrawImage m, definito nella classe derivata, include un oggetto [**CDrawImage**](cdrawimage.md) .</span><span class="sxs-lookup"><span data-stu-id="eaf00-126">In this example, CVideoText is a class derived from [**CBaseControlVideo**](cbasecontrolvideo.md), m\_pRenderer holds an object of a class derived from [**CBaseVideoRenderer**](cbasevideorenderer.md), and the m\_DrawImage data member, defined in the derived class, holds a [**CDrawImage**](cdrawimage.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="eaf00-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eaf00-127">Requirements</span></span>



| <span data-ttu-id="eaf00-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="eaf00-128">Requirement</span></span> | <span data-ttu-id="eaf00-129">Valore</span><span class="sxs-lookup"><span data-stu-id="eaf00-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eaf00-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="eaf00-130">Header</span></span><br/>  | <dl> <span data-ttu-id="eaf00-131"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="eaf00-131"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="eaf00-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="eaf00-132">Library</span></span><br/> | <dl> <span data-ttu-id="eaf00-133"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="eaf00-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eaf00-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="eaf00-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eaf00-135">**Classe CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="eaf00-135">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




