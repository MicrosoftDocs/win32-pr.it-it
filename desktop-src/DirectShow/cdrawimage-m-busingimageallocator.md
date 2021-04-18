---
description: La \_ variabile membro bUsingImageAllocator m indica se l'allocatore per la connessione pin è un oggetto CImageAllocator. Se il valore è TRUE, l'allocatore è un oggetto CImageAllocator (o deriva da tale classe).
ms.assetid: 8eddcab6-77b9-4c8f-be74-33e91661430d
title: 'Membro CDrawImage:: m_bUsingImageAllocator (Winutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bUsingImageAllocator
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e08d1e8217f42c6855759cefeef40e56949156fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330682"
---
# <a name="cdrawimagem_busingimageallocator-member"></a><span data-ttu-id="811ee-104">Membro bUsingImageAllocator di CDrawImage:: m \_</span><span class="sxs-lookup"><span data-stu-id="811ee-104">CDrawImage::m\_bUsingImageAllocator member</span></span>

<span data-ttu-id="811ee-105">La `m_bUsingImageAllocator` variabile membro indica se l'allocatore per la connessione pin è un oggetto **CImageAllocator** .</span><span class="sxs-lookup"><span data-stu-id="811ee-105">The `m_bUsingImageAllocator` member variable indicates whether the allocator for the pin connection is a **CImageAllocator** object.</span></span> <span data-ttu-id="811ee-106">Se il valore è **true**, l'allocatore è un oggetto **CImageAllocator** (o deriva da tale classe).</span><span class="sxs-lookup"><span data-stu-id="811ee-106">If the value is **TRUE**, the allocator is a **CImageAllocator** object (or is derived from that class).</span></span>

## <a name="syntax"></a><span data-ttu-id="811ee-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="811ee-107">Syntax</span></span>


```C++
BOOL m_bUsingImageAllocator;
```



## <a name="remarks"></a><span data-ttu-id="811ee-108">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="811ee-108">Remarks</span></span>

<span data-ttu-id="811ee-109">Quando il valore è **true**, l'oggetto **CDrawImage** può utilizzare le funzioni **GDI BitBlt** e **StretchBlt** per eseguire il rendering dell'immagine, anziché le funzioni più lente **SetDIBitsToDevice** e **StretchDIBits** .</span><span class="sxs-lookup"><span data-stu-id="811ee-109">When the value is **TRUE**, the **CDrawImage** object can use the GDI **BitBlt** and **StretchBlt** functions to render the image, rather than the slower **SetDIBitsToDevice** and **StretchDIBits** functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="811ee-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="811ee-110">Requirements</span></span>



| <span data-ttu-id="811ee-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="811ee-111">Requirement</span></span> | <span data-ttu-id="811ee-112">Valore</span><span class="sxs-lookup"><span data-stu-id="811ee-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="811ee-113">Intestazione</span><span class="sxs-lookup"><span data-stu-id="811ee-113">Header</span></span><br/>  | <dl> <span data-ttu-id="811ee-114"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="811ee-114"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="811ee-115">Libreria</span><span class="sxs-lookup"><span data-stu-id="811ee-115">Library</span></span><br/> | <dl> <span data-ttu-id="811ee-116"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="811ee-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="811ee-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="811ee-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="811ee-118">**Classe CDrawImage**</span><span class="sxs-lookup"><span data-stu-id="811ee-118">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> <dt>

[<span data-ttu-id="811ee-119">**CDrawImage::NotifyAllocator**</span><span class="sxs-lookup"><span data-stu-id="811ee-119">**CDrawImage::NotifyAllocator**</span></span>](cdrawimage-notifyallocator.md)
</dt> <dt>

[<span data-ttu-id="811ee-120">**CDrawImage::UsingImageAllocator**</span><span class="sxs-lookup"><span data-stu-id="811ee-120">**CDrawImage::UsingImageAllocator**</span></span>](cdrawimage-usingimageallocator.md)
</dt> </dl>

 

 




