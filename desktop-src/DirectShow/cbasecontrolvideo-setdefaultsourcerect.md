---
description: Il metodo SetDefaultSourceRect imposta il rettangolo del video di origine predefinito (puro virtuale). In una funzione membro interna che viene chiamata quando viene reimpostato il rettangolo di origine.
ms.assetid: d0dae0a9-8763-485e-b9d3-80076a3f2f35
title: Metodo CBaseControlVideo. SetDefaultSourceRect (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetDefaultSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 82fe2001a42ca75fff4f3172c8ce05da18881d73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329871"
---
# <a name="cbasecontrolvideosetdefaultsourcerect-method"></a><span data-ttu-id="f5f3b-104">CBaseControlVideo. SetDefaultSourceRect, metodo</span><span class="sxs-lookup"><span data-stu-id="f5f3b-104">CBaseControlVideo.SetDefaultSourceRect method</span></span>

<span data-ttu-id="f5f3b-105">Il `SetDefaultSourceRect` metodo imposta il rettangolo del video di origine predefinito (puro virtuale).</span><span class="sxs-lookup"><span data-stu-id="f5f3b-105">The `SetDefaultSourceRect` method sets the default source video rectangle (pure virtual).</span></span> <span data-ttu-id="f5f3b-106">In una funzione membro interna che viene chiamata quando viene reimpostato il rettangolo di origine.</span><span class="sxs-lookup"><span data-stu-id="f5f3b-106">This in an internal member function that gets called when the source rectangle is reset.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5f3b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f5f3b-107">Syntax</span></span>


```C++
virtual HRESULT SetDefaultSourceRect() = 0;
```



## <a name="parameters"></a><span data-ttu-id="f5f3b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="f5f3b-108">Parameters</span></span>

<span data-ttu-id="f5f3b-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="f5f3b-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f5f3b-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f5f3b-110">Return value</span></span>

<span data-ttu-id="f5f3b-111">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f5f3b-111">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5f3b-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="f5f3b-112">Remarks</span></span>

<span data-ttu-id="f5f3b-113">Le classi derivate devono eseguire l'override di questo per ripristinare il rettangolo di origine.</span><span class="sxs-lookup"><span data-stu-id="f5f3b-113">Derived classes should override this to reset the source rectangle.</span></span> <span data-ttu-id="f5f3b-114">Viene chiamato da [**CBaseControlVideo:: SetDefaultSourcePosition**](cbasecontrolvideo-setdefaultsourceposition.md).</span><span class="sxs-lookup"><span data-stu-id="f5f3b-114">It is called from [**CBaseControlVideo::SetDefaultSourcePosition**](cbasecontrolvideo-setdefaultsourceposition.md).</span></span>

<span data-ttu-id="f5f3b-115">Nell'esempio seguente viene illustrata un'implementazione di questa funzione in una classe derivata.</span><span class="sxs-lookup"><span data-stu-id="f5f3b-115">The following example demonstrates an implementation of this function in a derived class.</span></span>


```C++
// This is called when you reset the default source rectangle.
HRESULT CVideoText::SetDefaultSourceRect()
{
    VIDEOINFO *pVideoInfo = (VIDEOINFO *) m_pRenderer->m_mtIn.Format();
    BITMAPINFOHEADER *pHeader = HEADER(pVideoInfo);
    RECT SourceRect = {0,0,pHeader->biWidth,pHeader->biHeight};
    m_pRenderer->m_DrawImage.SetSourceRect(&SourceRect);
    return NOERROR;
}
```



<span data-ttu-id="f5f3b-116">In questo esempio, CVideoText è una classe derivata da [**CBaseControlVideo**](cbasecontrolvideo.md), m \_ pRenderer include un oggetto di una classe derivata da [**CBaseVideoRenderer**](cbasevideorenderer.md)e il \_ membro dati DrawImage m, definito nella classe derivata, include un oggetto [**CDrawImage**](cdrawimage.md) .</span><span class="sxs-lookup"><span data-stu-id="f5f3b-116">In this example, CVideoText is a class derived from [**CBaseControlVideo**](cbasecontrolvideo.md), m\_pRenderer holds an object of a class derived from [**CBaseVideoRenderer**](cbasevideorenderer.md), and the m\_DrawImage data member, defined in the derived class, holds a [**CDrawImage**](cdrawimage.md) object.</span></span> <span data-ttu-id="f5f3b-117">Il \_ membro dati mtIn m, definito anche nella classe derivata, include un oggetto [**CMediaType**](cmediatype.md) con tipo di supporto del PIN di input.</span><span class="sxs-lookup"><span data-stu-id="f5f3b-117">The m\_mtIn data member, also defined in the derived class, holds a [**CMediaType**](cmediatype.md) object with media type of the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5f3b-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f5f3b-118">Requirements</span></span>



| <span data-ttu-id="f5f3b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5f3b-119">Requirement</span></span> | <span data-ttu-id="f5f3b-120">Valore</span><span class="sxs-lookup"><span data-stu-id="f5f3b-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5f3b-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f5f3b-121">Header</span></span><br/>  | <dl> <span data-ttu-id="f5f3b-122"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f5f3b-122"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f5f3b-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="f5f3b-123">Library</span></span><br/> | <dl> <span data-ttu-id="f5f3b-124"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f5f3b-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5f3b-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f5f3b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5f3b-126">**Classe CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="f5f3b-126">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




