---
description: Il metodo SetTargetRect imposta il rettangolo di destinazione corrente (virtuale puro). Si tratta di una funzione membro interna che viene chiamata quando il rettangolo di destinazione viene modificato.
ms.assetid: 9e48989d-5995-4f9d-82b2-01229473c3e8
title: Metodo CBaseControlVideo. SetTargetRect (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3868e7d8df93940829fb96c7152a55048a5cae82
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332353"
---
# <a name="cbasecontrolvideosettargetrect-method"></a><span data-ttu-id="36e93-104">CBaseControlVideo. SetTargetRect, metodo</span><span class="sxs-lookup"><span data-stu-id="36e93-104">CBaseControlVideo.SetTargetRect method</span></span>

<span data-ttu-id="36e93-105">Il `SetTargetRect` metodo imposta il rettangolo di destinazione corrente (virtuale puro).</span><span class="sxs-lookup"><span data-stu-id="36e93-105">The `SetTargetRect` method sets the current target rectangle (pure virtual).</span></span> <span data-ttu-id="36e93-106">Si tratta di una funzione membro interna che viene chiamata quando il rettangolo di destinazione viene modificato.</span><span class="sxs-lookup"><span data-stu-id="36e93-106">This is an internal member function that gets called when the destination rectangle changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="36e93-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="36e93-107">Syntax</span></span>


```C++
virtual HRESULT SetTargetRect(
   RECT *pTargetRect
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="36e93-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="36e93-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36e93-109">*pTargetRect*</span><span class="sxs-lookup"><span data-stu-id="36e93-109">*pTargetRect*</span></span> 
</dt> <dd>

<span data-ttu-id="36e93-110">Puntatore al rettangolo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="36e93-110">Pointer to the destination rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36e93-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="36e93-111">Return value</span></span>

<span data-ttu-id="36e93-112">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="36e93-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="36e93-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="36e93-113">Remarks</span></span>

<span data-ttu-id="36e93-114">Le classi derivate devono eseguire l'override di questo per stabilire quando cambia il rettangolo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="36e93-114">Derived classes should override this to know when the destination rectangle changes.</span></span> <span data-ttu-id="36e93-115">Viene chiamato dalle funzioni membro seguenti.</span><span class="sxs-lookup"><span data-stu-id="36e93-115">It is called from the following member functions.</span></span>

-   [<span data-ttu-id="36e93-116">**CBaseControlVideo::SetDestinationPosition**</span><span class="sxs-lookup"><span data-stu-id="36e93-116">**CBaseControlVideo::SetDestinationPosition**</span></span>](cbasecontrolvideo-setdestinationposition.md)
-   [<span data-ttu-id="36e93-117">**CBaseControlVideo::p UT \_ DestinationLeft**</span><span class="sxs-lookup"><span data-stu-id="36e93-117">**CBaseControlVideo::put\_DestinationLeft**</span></span>](cbasecontrolvideo-put-destinationleft.md)
-   [<span data-ttu-id="36e93-118">**CBaseControlVideo::p UT \_ DestinationWidth**</span><span class="sxs-lookup"><span data-stu-id="36e93-118">**CBaseControlVideo::put\_DestinationWidth**</span></span>](cbasecontrolvideo-put-destinationwidth.md)
-   [<span data-ttu-id="36e93-119">**CBaseControlVideo::p UT \_ DestinationTop**</span><span class="sxs-lookup"><span data-stu-id="36e93-119">**CBaseControlVideo::put\_DestinationTop**</span></span>](cbasecontrolvideo-put-destinationtop.md)
-   [<span data-ttu-id="36e93-120">**CBaseControlVideo::p UT \_ DestinationHeight**</span><span class="sxs-lookup"><span data-stu-id="36e93-120">**CBaseControlVideo::put\_DestinationHeight**</span></span>](cbasecontrolvideo-put-destinationheight.md)

<span data-ttu-id="36e93-121">Nell'esempio seguente viene illustrata un'implementazione di questa funzione in una classe derivata.</span><span class="sxs-lookup"><span data-stu-id="36e93-121">The following example demonstrates an implementation of this function in a derived class.</span></span>


```C++
HRESULT CVideoText::SetTargetRect(RECT *pTargetRect)
{
    m_pRenderer->m_DrawImage.SetTargetRect(pTargetRect);
    return NOERROR;
}
```



<span data-ttu-id="36e93-122">In questo esempio, CVideoText è una classe derivata da [**CBaseControlVideo**](cbasecontrolvideo.md), m \_ pRenderer include un oggetto di una classe derivata da [**CBaseVideoRenderer**](cbasevideorenderer.md)e il \_ membro dati DrawImage m, definito nella classe derivata, include un oggetto [**CDrawImage**](cdrawimage.md) .</span><span class="sxs-lookup"><span data-stu-id="36e93-122">In this example, CVideoText is a class derived from [**CBaseControlVideo**](cbasecontrolvideo.md), m\_pRenderer holds an object of a class derived from [**CBaseVideoRenderer**](cbasevideorenderer.md), and the m\_DrawImage data member, defined in the derived class, holds a [**CDrawImage**](cdrawimage.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="36e93-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="36e93-123">Requirements</span></span>



| <span data-ttu-id="36e93-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="36e93-124">Requirement</span></span> | <span data-ttu-id="36e93-125">Valore</span><span class="sxs-lookup"><span data-stu-id="36e93-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36e93-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="36e93-126">Header</span></span><br/>  | <dl> <span data-ttu-id="36e93-127"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="36e93-127"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="36e93-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="36e93-128">Library</span></span><br/> | <dl> <span data-ttu-id="36e93-129"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="36e93-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36e93-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="36e93-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36e93-131">**Classe CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="36e93-131">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




