---
description: Il metodo SetSourceRect imposta il rettangolo del video di origine corrente (virtuale puro). Si tratta di una funzione membro interna che viene chiamata quando il rettangolo di origine viene modificato.
ms.assetid: 13bb594b-b154-40a2-ad00-f1e86781074d
title: Metodo CBaseControlVideo. SetSourceRect (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0e3be6cc3819e1452fd196d4906377204a6e90bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332354"
---
# <a name="cbasecontrolvideosetsourcerect-method"></a><span data-ttu-id="f95e7-104">CBaseControlVideo. SetSourceRect, metodo</span><span class="sxs-lookup"><span data-stu-id="f95e7-104">CBaseControlVideo.SetSourceRect method</span></span>

<span data-ttu-id="f95e7-105">Il `SetSourceRect` metodo imposta il rettangolo del video di origine corrente (virtuale puro).</span><span class="sxs-lookup"><span data-stu-id="f95e7-105">The `SetSourceRect` method sets the current source video rectangle (pure virtual).</span></span> <span data-ttu-id="f95e7-106">Si tratta di una funzione membro interna che viene chiamata quando il rettangolo di origine viene modificato.</span><span class="sxs-lookup"><span data-stu-id="f95e7-106">This is an internal member function that gets called when the source rectangle changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="f95e7-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f95e7-107">Syntax</span></span>


```C++
virtual HRESULT SetSourceRect(
   RECT *pSourceRect
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="f95e7-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="f95e7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f95e7-109">*pSourceRect*</span><span class="sxs-lookup"><span data-stu-id="f95e7-109">*pSourceRect*</span></span> 
</dt> <dd>

<span data-ttu-id="f95e7-110">Puntatore al rettangolo di origine.</span><span class="sxs-lookup"><span data-stu-id="f95e7-110">Pointer to the source rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f95e7-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f95e7-111">Return value</span></span>

<span data-ttu-id="f95e7-112">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f95e7-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f95e7-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="f95e7-113">Remarks</span></span>

<span data-ttu-id="f95e7-114">Le classi derivate devono eseguire l'override di questa funzione membro per capire quando viene modificato il rettangolo di origine.</span><span class="sxs-lookup"><span data-stu-id="f95e7-114">Derived classes should override this member function to know when the source rectangle changes.</span></span> <span data-ttu-id="f95e7-115">Viene chiamato dalle funzioni membro seguenti.</span><span class="sxs-lookup"><span data-stu-id="f95e7-115">It is called from the following member functions.</span></span>

-   [<span data-ttu-id="f95e7-116">**CBaseControlVideo::SetSourcePosition**</span><span class="sxs-lookup"><span data-stu-id="f95e7-116">**CBaseControlVideo::SetSourcePosition**</span></span>](cbasecontrolvideo-setsourceposition.md)
-   [<span data-ttu-id="f95e7-117">**CBaseControlVideo::p UT \_ SourceLeft**</span><span class="sxs-lookup"><span data-stu-id="f95e7-117">**CBaseControlVideo::put\_SourceLeft**</span></span>](cbasecontrolvideo-put-sourceleft.md)
-   [<span data-ttu-id="f95e7-118">**CBaseControlVideo::p UT \_ SourceWidth**</span><span class="sxs-lookup"><span data-stu-id="f95e7-118">**CBaseControlVideo::put\_SourceWidth**</span></span>](cbasecontrolvideo-put-sourcewidth.md)
-   [<span data-ttu-id="f95e7-119">**CBaseControlVideo::p UT \_ SourceTop**</span><span class="sxs-lookup"><span data-stu-id="f95e7-119">**CBaseControlVideo::put\_SourceTop**</span></span>](cbasecontrolvideo-put-sourcetop.md)
-   [<span data-ttu-id="f95e7-120">**CBaseControlVideo::p UT \_ SourceHeight**</span><span class="sxs-lookup"><span data-stu-id="f95e7-120">**CBaseControlVideo::put\_SourceHeight**</span></span>](cbasecontrolvideo-put-sourceheight.md)

<span data-ttu-id="f95e7-121">Nell'esempio seguente viene illustrata un'implementazione di questa funzione in una classe derivata.</span><span class="sxs-lookup"><span data-stu-id="f95e7-121">The following example demonstrates an implementation of this function in a derived class.</span></span>


```C++
HRESULT CVideoText::SetSourceRect(RECT *pSourceRect)
{
    m_pRenderer->m_DrawImage.SetSourceRect(pSourceRect);
    return NOERROR;
}
```



<span data-ttu-id="f95e7-122">In questo esempio, CVideoText è una classe derivata da [**CBaseControlVideo**](cbasecontrolvideo.md), m \_ pRenderer include un oggetto di una classe derivata da [**CBaseVideoRenderer**](cbasevideorenderer.md)e il \_ membro dati DrawImage m, definito nella classe derivata, include un oggetto [**CDrawImage**](cdrawimage.md) .</span><span class="sxs-lookup"><span data-stu-id="f95e7-122">In this example, CVideoText is a class derived from [**CBaseControlVideo**](cbasecontrolvideo.md), m\_pRenderer holds an object of a class derived from [**CBaseVideoRenderer**](cbasevideorenderer.md), and the m\_DrawImage data member, defined in the derived class, holds a [**CDrawImage**](cdrawimage.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="f95e7-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f95e7-123">Requirements</span></span>



| <span data-ttu-id="f95e7-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="f95e7-124">Requirement</span></span> | <span data-ttu-id="f95e7-125">Valore</span><span class="sxs-lookup"><span data-stu-id="f95e7-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f95e7-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f95e7-126">Header</span></span><br/>  | <dl> <span data-ttu-id="f95e7-127"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f95e7-127"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f95e7-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="f95e7-128">Library</span></span><br/> | <dl> <span data-ttu-id="f95e7-129"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f95e7-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f95e7-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f95e7-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f95e7-131">**Classe CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="f95e7-131">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




