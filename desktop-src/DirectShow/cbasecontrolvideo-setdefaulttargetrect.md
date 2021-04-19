---
description: Il metodo SetDefaultTargetRect imposta il rettangolo del video di destinazione predefinito (Virtual pure). Si tratta di una funzione membro interna che viene chiamata quando viene reimpostato il rettangolo di origine.
ms.assetid: bb7e32b2-f02c-465f-a8cb-6172d9724790
title: Metodo CBaseControlVideo. SetDefaultTargetRect (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetDefaultTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 54b31268935cb296543b3992bf67b7a2193c1a92
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328561"
---
# <a name="cbasecontrolvideosetdefaulttargetrect-method"></a><span data-ttu-id="e766c-104">CBaseControlVideo. SetDefaultTargetRect, metodo</span><span class="sxs-lookup"><span data-stu-id="e766c-104">CBaseControlVideo.SetDefaultTargetRect method</span></span>

<span data-ttu-id="e766c-105">Il `SetDefaultTargetRect` metodo imposta il rettangolo del video di destinazione predefinito (virtuale puro).</span><span class="sxs-lookup"><span data-stu-id="e766c-105">The `SetDefaultTargetRect` method sets the default target video rectangle (pure virtual).</span></span> <span data-ttu-id="e766c-106">Si tratta di una funzione membro interna che viene chiamata quando viene reimpostato il rettangolo di origine.</span><span class="sxs-lookup"><span data-stu-id="e766c-106">This is an internal member function that gets called when the source rectangle is reset.</span></span>

## <a name="syntax"></a><span data-ttu-id="e766c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e766c-107">Syntax</span></span>


```C++
virtual HRESULT SetDefaultTargetRect() = 0;
```



## <a name="parameters"></a><span data-ttu-id="e766c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e766c-108">Parameters</span></span>

<span data-ttu-id="e766c-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="e766c-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e766c-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e766c-110">Return value</span></span>

<span data-ttu-id="e766c-111">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e766c-111">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e766c-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="e766c-112">Remarks</span></span>

<span data-ttu-id="e766c-113">Le classi derivate devono eseguire l'override di questo per reimpostare il rettangolo video di destinazione</span><span class="sxs-lookup"><span data-stu-id="e766c-113">Derived classes should override this to reset the destination video rectangle.</span></span> <span data-ttu-id="e766c-114">Viene chiamato dalla funzione membro [**CBaseControlVideo:: SetDefaultDestinationPosition**](cbasecontrolvideo-setdefaultdestinationposition.md) .</span><span class="sxs-lookup"><span data-stu-id="e766c-114">It is called from the [**CBaseControlVideo::SetDefaultDestinationPosition**](cbasecontrolvideo-setdefaultdestinationposition.md) member function.</span></span>

<span data-ttu-id="e766c-115">Nell'esempio seguente viene illustrata un'implementazione di questa funzione in una classe derivata.</span><span class="sxs-lookup"><span data-stu-id="e766c-115">The following example demonstrates an implementation of this function in a derived class.</span></span>


```C++
// This is called when you reset the default target rectangle.
HRESULT CVideoText::SetDefaultTargetRect()
{
    VIDEOINFO *pVideoInfo = (VIDEOINFO *) m_pRenderer->m_mtIn.Format();
    BITMAPINFOHEADER *pHeader = HEADER(pVideoInfo);
    RECT TargetRect = {0,0,m_Size.cx,m_Size.cy};
    m_pRenderer->m_DrawImage.SetTargetRect(&TargetRect);
    return NOERROR;
}
```



<span data-ttu-id="e766c-116">In questo esempio, CVideoText è una classe derivata da [**CBaseControlVideo**](cbasecontrolvideo.md), m \_ pRenderer include un oggetto di una classe derivata da [**CBaseVideoRenderer**](cbasevideorenderer.md)e il \_ membro dati DrawImage m, definito nella classe derivata, include un oggetto [**CDrawImage**](cdrawimage.md) .</span><span class="sxs-lookup"><span data-stu-id="e766c-116">In this example, CVideoText is a class derived from [**CBaseControlVideo**](cbasecontrolvideo.md), m\_pRenderer holds an object of a class derived from [**CBaseVideoRenderer**](cbasevideorenderer.md), and the m\_DrawImage data member, defined in the derived class, holds a [**CDrawImage**](cdrawimage.md) object.</span></span> <span data-ttu-id="e766c-117">Il \_ membro dati mtIn m, definito anche nella classe derivata, include un oggetto [**CMediaType**](cmediatype.md) con il tipo di supporto del PIN di input.</span><span class="sxs-lookup"><span data-stu-id="e766c-117">The m\_mtIn data member, also defined in the derived class, holds a [**CMediaType**](cmediatype.md) object with the media type of the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="e766c-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e766c-118">Requirements</span></span>



| <span data-ttu-id="e766c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e766c-119">Requirement</span></span> | <span data-ttu-id="e766c-120">Valore</span><span class="sxs-lookup"><span data-stu-id="e766c-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e766c-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e766c-121">Header</span></span><br/>  | <dl> <span data-ttu-id="e766c-122"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e766c-122"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e766c-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="e766c-123">Library</span></span><br/> | <dl> <span data-ttu-id="e766c-124"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="e766c-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e766c-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e766c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e766c-126">**Classe CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="e766c-126">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




