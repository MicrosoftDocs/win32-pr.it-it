---
description: Il metodo IsDefaultSourceRect determina se il renderer usa il rettangolo di origine predefinito (puro virtuale).
ms.assetid: 08c7a365-585c-47e6-9c26-6aa1fa3625e7
title: Metodo CBaseControlVideo. IsDefaultSourceRect (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.IsDefaultSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 390ae779eaa7d640d23b40a7e6f6579e158bf6ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332080"
---
# <a name="cbasecontrolvideoisdefaultsourcerect-method"></a><span data-ttu-id="654f2-103">CBaseControlVideo. IsDefaultSourceRect, metodo</span><span class="sxs-lookup"><span data-stu-id="654f2-103">CBaseControlVideo.IsDefaultSourceRect method</span></span>

<span data-ttu-id="654f2-104">Il `IsDefaultSourceRect` metodo determina se il renderer usa il rettangolo di origine predefinito (puro virtuale).</span><span class="sxs-lookup"><span data-stu-id="654f2-104">The `IsDefaultSourceRect` method determines if the renderer is using the default source rectangle (pure virtual).</span></span>

## <a name="syntax"></a><span data-ttu-id="654f2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="654f2-105">Syntax</span></span>


```C++
virtual HRESULT IsDefaultSourceRect() = 0;
```



## <a name="parameters"></a><span data-ttu-id="654f2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="654f2-106">Parameters</span></span>

<span data-ttu-id="654f2-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="654f2-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="654f2-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="654f2-108">Return value</span></span>

<span data-ttu-id="654f2-109">Restituisce \_ OK se il renderer utilizza l'origine predefinita; in caso contrario, restituisce \_ false.</span><span class="sxs-lookup"><span data-stu-id="654f2-109">Returns S\_OK if the renderer is using the default source; otherwise, returns S\_FALSE.</span></span>

## <a name="remarks"></a><span data-ttu-id="654f2-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="654f2-110">Remarks</span></span>

<span data-ttu-id="654f2-111">Questa funzione membro deve essere implementata nella classe derivata.</span><span class="sxs-lookup"><span data-stu-id="654f2-111">This member function must be implemented in the derived class.</span></span> <span data-ttu-id="654f2-112">Viene chiamato dalla funzione membro [**CBaseControlVideo:: IsUsingDefaultSource**](cbasecontrolvideo-isusingdefaultsource.md) .</span><span class="sxs-lookup"><span data-stu-id="654f2-112">It is called by the [**CBaseControlVideo::IsUsingDefaultSource**](cbasecontrolvideo-isusingdefaultsource.md) member function.</span></span>

<span data-ttu-id="654f2-113">Nell'esempio seguente viene illustrata un'implementazione di questa funzione in una classe derivata.</span><span class="sxs-lookup"><span data-stu-id="654f2-113">The following example demonstrates an implementation of this function in a derived class.</span></span>


```C++
// Return S_OK if using the default source; otherwise, S_FALSE.
HRESULT CVideoText::IsDefaultSourceRect()
{
    RECT SourceRect;

    VIDEOINFO *pVideoInfo = (VIDEOINFO *) m_pRenderer->m_mtIn.Format();
    BITMAPINFOHEADER *pHeader = HEADER(pVideoInfo);
    m_pRenderer->m_DrawImage.GetSourceRect(&SourceRect);

    // Check the coordinates that match the video dimensions.

    if (SourceRect.left != 0 || SourceRect.top != 0 ||
            SourceRect.right != pHeader->biWidth ||
                SourceRect.bottom != pHeader->biHeight) {
                    return S_FALSE;
    }
    return S_OK;
}
```



<span data-ttu-id="654f2-114">In questo esempio, CVideoText è una classe derivata da [**CBaseControlVideo**](cbasecontrolvideo.md), m \_ pRenderer include un oggetto di una classe derivata da [**CBaseVideoRenderer**](cbasevideorenderer.md)e il \_ membro dati DrawImage m, definito nella classe derivata, include un oggetto [**CDrawImage**](cdrawimage.md) .</span><span class="sxs-lookup"><span data-stu-id="654f2-114">In this example, CVideoText is a class derived from [**CBaseControlVideo**](cbasecontrolvideo.md), m\_pRenderer holds an object of a class derived from [**CBaseVideoRenderer**](cbasevideorenderer.md), and the m\_DrawImage data member, defined in the derived class, holds a [**CDrawImage**](cdrawimage.md) object.</span></span> <span data-ttu-id="654f2-115">Il \_ membro dati mtIn m, definito anche nella classe derivata, include un oggetto [**CMediaType**](cmediatype.md) con il tipo di supporto del PIN di input.</span><span class="sxs-lookup"><span data-stu-id="654f2-115">The m\_mtIn data member, also defined in the derived class, holds a [**CMediaType**](cmediatype.md) object with the media type of the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="654f2-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="654f2-116">Requirements</span></span>



| <span data-ttu-id="654f2-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="654f2-117">Requirement</span></span> | <span data-ttu-id="654f2-118">Valore</span><span class="sxs-lookup"><span data-stu-id="654f2-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="654f2-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="654f2-119">Header</span></span><br/>  | <dl> <span data-ttu-id="654f2-120"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="654f2-120"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="654f2-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="654f2-121">Library</span></span><br/> | <dl> <span data-ttu-id="654f2-122"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="654f2-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="654f2-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="654f2-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="654f2-124">**Classe CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="654f2-124">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




