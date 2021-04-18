---
description: Il metodo IsDefaultTargetRect determina se il renderer usa il rettangolo di destinazione predefinito (Virtual pure).
ms.assetid: 60c09515-7a34-421c-b3e8-ce746a935583
title: Metodo CBaseControlVideo. IsDefaultTargetRect (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.IsDefaultTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e267cc65345d18800beccbc80ac7952c89d781d8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333797"
---
# <a name="cbasecontrolvideoisdefaulttargetrect-method"></a><span data-ttu-id="3ae59-103">CBaseControlVideo. IsDefaultTargetRect, metodo</span><span class="sxs-lookup"><span data-stu-id="3ae59-103">CBaseControlVideo.IsDefaultTargetRect method</span></span>

<span data-ttu-id="3ae59-104">Il `IsDefaultTargetRect` metodo determina se il renderer usa il rettangolo di destinazione predefinito (virtuale puro).</span><span class="sxs-lookup"><span data-stu-id="3ae59-104">The `IsDefaultTargetRect` method determines if the renderer is using the default target rectangle (pure virtual).</span></span>

## <a name="syntax"></a><span data-ttu-id="3ae59-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3ae59-105">Syntax</span></span>


```C++
virtual HRESULT IsDefaultTargetRect() = 0;
```



## <a name="parameters"></a><span data-ttu-id="3ae59-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3ae59-106">Parameters</span></span>

<span data-ttu-id="3ae59-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="3ae59-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3ae59-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3ae59-108">Return value</span></span>

<span data-ttu-id="3ae59-109">Restituisce \_ OK se il renderer utilizza la destinazione predefinita; in caso contrario, restituisce \_ false.</span><span class="sxs-lookup"><span data-stu-id="3ae59-109">Returns S\_OK if the renderer is using the default target; otherwise, returns S\_FALSE.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ae59-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="3ae59-110">Remarks</span></span>

<span data-ttu-id="3ae59-111">Questa funzione membro deve essere implementata nella classe derivata.</span><span class="sxs-lookup"><span data-stu-id="3ae59-111">This member function must be implemented in the derived class.</span></span> <span data-ttu-id="3ae59-112">Viene chiamato dalla funzione membro [**CBaseControlVideo:: IsUsingDefaultDestination**](cbasecontrolvideo-isusingdefaultdestination.md) .</span><span class="sxs-lookup"><span data-stu-id="3ae59-112">It is called by the [**CBaseControlVideo::IsUsingDefaultDestination**](cbasecontrolvideo-isusingdefaultdestination.md) member function.</span></span>

<span data-ttu-id="3ae59-113">Nell'esempio seguente viene illustrata un'implementazione di questa funzione in una classe derivata.</span><span class="sxs-lookup"><span data-stu-id="3ae59-113">The following example demonstrates an implementation of this function in a derived class.</span></span>


```C++
// Return S_OK if using the default target; otherwise, S_FALSE.
HRESULT CVideoText::IsDefaultTargetRect()
{
    RECT TargetRect;

    VIDEOINFO *pVideoInfo = (VIDEOINFO *) m_pRenderer->m_mtIn.Format();
    BITMAPINFOHEADER *pHeader = HEADER(pVideoInfo);
    m_pRenderer->m_DrawImage.GetTargetRect(&TargetRect);

    // Check the destination that matches the initial client area.

    if (TargetRect.left != 0 || TargetRect.top != 0 ||
            TargetRect.right != m_Size.cx ||
                TargetRect.bottom != m_Size.cy) {
                    return S_FALSE;
    }
    return S_OK;
}
```



<span data-ttu-id="3ae59-114">In questo esempio, CVideoText è una classe derivata da [**CBaseControlVideo**](cbasecontrolvideo.md), m \_ pRenderer include un oggetto di una classe derivata da [**CBaseVideoRenderer**](cbasevideorenderer.md)e il \_ membro dati DrawImage m, definito nella classe derivata, include un oggetto [**CDrawImage**](cdrawimage.md) .</span><span class="sxs-lookup"><span data-stu-id="3ae59-114">In this example, CVideoText is a class derived from [**CBaseControlVideo**](cbasecontrolvideo.md), m\_pRenderer holds an object of a class derived from [**CBaseVideoRenderer**](cbasevideorenderer.md), and the m\_DrawImage data member, defined in the derived class, holds a [**CDrawImage**](cdrawimage.md) object.</span></span> <span data-ttu-id="3ae59-115">Il \_ membro dati mtIn m, definito anche nella classe derivata, include un oggetto [**CMediaType**](cmediatype.md) con tipo di supporto del PIN di input.</span><span class="sxs-lookup"><span data-stu-id="3ae59-115">The m\_mtIn data member, also defined in the derived class, holds a [**CMediaType**](cmediatype.md) object with media type of the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ae59-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3ae59-116">Requirements</span></span>



| <span data-ttu-id="3ae59-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ae59-117">Requirement</span></span> | <span data-ttu-id="3ae59-118">Valore</span><span class="sxs-lookup"><span data-stu-id="3ae59-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ae59-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3ae59-119">Header</span></span><br/>  | <dl> <span data-ttu-id="3ae59-120"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3ae59-120"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3ae59-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="3ae59-121">Library</span></span><br/> | <dl> <span data-ttu-id="3ae59-122"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="3ae59-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ae59-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3ae59-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ae59-124">**Classe CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="3ae59-124">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




