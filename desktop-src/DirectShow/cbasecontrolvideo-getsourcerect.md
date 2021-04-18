---
description: Il metodo GetSourceRect Recupera il rettangolo di origine. Si tratta di un metodo interno.
ms.assetid: 51028b79-6aab-4abc-8ee8-2965bda9d191
title: Metodo CBaseControlVideo. GetSourceRect (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e57a5beda7b147e952ecbb26c96df5f7e372e6d7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327127"
---
# <a name="cbasecontrolvideogetsourcerect-method"></a><span data-ttu-id="f4345-104">CBaseControlVideo. GetSourceRect, metodo</span><span class="sxs-lookup"><span data-stu-id="f4345-104">CBaseControlVideo.GetSourceRect method</span></span>

<span data-ttu-id="f4345-105">Il `GetSourceRect` metodo recupera il rettangolo di origine.</span><span class="sxs-lookup"><span data-stu-id="f4345-105">The `GetSourceRect` method retrieves the source rectangle.</span></span> <span data-ttu-id="f4345-106">Si tratta di un metodo interno.</span><span class="sxs-lookup"><span data-stu-id="f4345-106">This is an internal method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4345-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f4345-107">Syntax</span></span>


```C++
virtual HRESULT GetSourceRect(
   RECT *pSourceRect
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="f4345-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="f4345-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4345-109">*pSourceRect*</span><span class="sxs-lookup"><span data-stu-id="f4345-109">*pSourceRect*</span></span> 
</dt> <dd>

<span data-ttu-id="f4345-110">Puntatore al rettangolo di origine recuperato.</span><span class="sxs-lookup"><span data-stu-id="f4345-110">Pointer to the retrieved source rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4345-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f4345-111">Return value</span></span>

<span data-ttu-id="f4345-112">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f4345-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4345-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="f4345-113">Remarks</span></span>

<span data-ttu-id="f4345-114">Questa funzione membro deve essere sottoposta a override nella classe derivata per restituire il rettangolo di origine utilizzato dal renderer video.</span><span class="sxs-lookup"><span data-stu-id="f4345-114">This member function must be overridden in the derived class to return the source rectangle held by the video renderer.</span></span> <span data-ttu-id="f4345-115">Viene chiamato dalle funzioni membro [**CBaseControlVideo**](cbasecontrolvideo.md) seguenti.</span><span class="sxs-lookup"><span data-stu-id="f4345-115">It is called from the following [**CBaseControlVideo**](cbasecontrolvideo.md) member functions.</span></span>

-   [<span data-ttu-id="f4345-116">**CBaseControlVideo::GetSourcePosition**</span><span class="sxs-lookup"><span data-stu-id="f4345-116">**CBaseControlVideo::GetSourcePosition**</span></span>](cbasecontrolvideo-getsourceposition.md)
-   [<span data-ttu-id="f4345-117">**CBaseControlVideo::p UT \_ SourceLeft**</span><span class="sxs-lookup"><span data-stu-id="f4345-117">**CBaseControlVideo::put\_SourceLeft**</span></span>](cbasecontrolvideo-put-sourceleft.md)
-   [<span data-ttu-id="f4345-118">**CBaseControlVideo:: Get \_ SourceLeft**</span><span class="sxs-lookup"><span data-stu-id="f4345-118">**CBaseControlVideo::get\_SourceLeft**</span></span>](cbasecontrolvideo-get-sourceleft.md)
-   [<span data-ttu-id="f4345-119">**CBaseControlVideo::p UT \_ SourceWidth**</span><span class="sxs-lookup"><span data-stu-id="f4345-119">**CBaseControlVideo::put\_SourceWidth**</span></span>](cbasecontrolvideo-put-sourcewidth.md)
-   [<span data-ttu-id="f4345-120">**CBaseControlVideo:: Get \_ SourceWidth**</span><span class="sxs-lookup"><span data-stu-id="f4345-120">**CBaseControlVideo::get\_SourceWidth**</span></span>](cbasecontrolvideo-get-sourcewidth.md)
-   [<span data-ttu-id="f4345-121">**CBaseControlVideo::p UT \_ SourceTop**</span><span class="sxs-lookup"><span data-stu-id="f4345-121">**CBaseControlVideo::put\_SourceTop**</span></span>](cbasecontrolvideo-put-sourcetop.md)
-   [<span data-ttu-id="f4345-122">**CBaseControlVideo:: Get \_ SourceTop**</span><span class="sxs-lookup"><span data-stu-id="f4345-122">**CBaseControlVideo::get\_SourceTop**</span></span>](cbasecontrolvideo-get-sourcetop.md)
-   [<span data-ttu-id="f4345-123">**CBaseControlVideo::p UT \_ SourceHeight**</span><span class="sxs-lookup"><span data-stu-id="f4345-123">**CBaseControlVideo::put\_SourceHeight**</span></span>](cbasecontrolvideo-put-sourceheight.md)
-   [<span data-ttu-id="f4345-124">**CBaseControlVideo:: Get \_ SourceHeight**</span><span class="sxs-lookup"><span data-stu-id="f4345-124">**CBaseControlVideo::get\_SourceHeight**</span></span>](cbasecontrolvideo-get-sourceheight.md)

<span data-ttu-id="f4345-125">Nell'esempio seguente viene illustrata un'implementazione di questa funzione in una classe derivata.</span><span class="sxs-lookup"><span data-stu-id="f4345-125">The following example demonstrates an implementation of this function in a derived class.</span></span>


```C++
// Return the current source rectangle
HRESULT CVideoText::GetSourceRect(RECT *pSourceRect)
{
    ASSERT(pSourceRect);
    m_pRenderer->m_DrawImage.GetSourceRect(pSourceRect);
    return NOERROR;
}
```



<span data-ttu-id="f4345-126">In questo esempio, CVideoText è una classe derivata da [**CBaseControlVideo**](cbasecontrolvideo.md), m \_ pRenderer include un oggetto di una classe derivata da [**CBaseVideoRenderer**](cbasevideorenderer.md)e il \_ membro dati DrawImage m, definito nella classe derivata, include un oggetto [**CDrawImage**](cdrawimage.md) .</span><span class="sxs-lookup"><span data-stu-id="f4345-126">In this example, CVideoText is a class derived from [**CBaseControlVideo**](cbasecontrolvideo.md), m\_pRenderer holds an object of a class derived from [**CBaseVideoRenderer**](cbasevideorenderer.md), and the m\_DrawImage data member, defined in the derived class, holds a [**CDrawImage**](cdrawimage.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4345-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f4345-127">Requirements</span></span>



| <span data-ttu-id="f4345-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4345-128">Requirement</span></span> | <span data-ttu-id="f4345-129">Valore</span><span class="sxs-lookup"><span data-stu-id="f4345-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4345-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f4345-130">Header</span></span><br/>  | <dl> <span data-ttu-id="f4345-131"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f4345-131"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f4345-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="f4345-132">Library</span></span><br/> | <dl> <span data-ttu-id="f4345-133"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f4345-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4345-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f4345-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4345-135">**Classe CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="f4345-135">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




