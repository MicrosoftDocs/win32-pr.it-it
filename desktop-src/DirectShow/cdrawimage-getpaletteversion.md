---
description: Il metodo GetPaletteVersion recupera la versione della tavolozza corrente.
ms.assetid: 9f97a810-04a4-4ea3-8918-416e9cd8e5e4
title: Metodo CDrawImage. GetPaletteVersion (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.GetPaletteVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c86f1a0dad8d33913a52962dfe2ec09b7b8244db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332644"
---
# <a name="cdrawimagegetpaletteversion-method"></a><span data-ttu-id="dcf27-103">CDrawImage. GetPaletteVersion, metodo</span><span class="sxs-lookup"><span data-stu-id="dcf27-103">CDrawImage.GetPaletteVersion method</span></span>

<span data-ttu-id="dcf27-104">Il `GetPaletteVersion` metodo recupera la versione della tavolozza corrente.</span><span class="sxs-lookup"><span data-stu-id="dcf27-104">The `GetPaletteVersion` method retrieves the current palette version.</span></span>

## <a name="syntax"></a><span data-ttu-id="dcf27-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dcf27-105">Syntax</span></span>


```C++
LONG GetPaletteVersion();
```



## <a name="parameters"></a><span data-ttu-id="dcf27-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="dcf27-106">Parameters</span></span>

<span data-ttu-id="dcf27-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="dcf27-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="dcf27-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dcf27-108">Return value</span></span>

<span data-ttu-id="dcf27-109">Restituisce il valore della variabile **membro \_ PaletteVersion m** .</span><span class="sxs-lookup"><span data-stu-id="dcf27-109">Returns the value of the **m\_PaletteVersion** member variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="dcf27-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="dcf27-110">Remarks</span></span>

<span data-ttu-id="dcf27-111">Il valore restituito da questo metodo si applica solo quando l'allocatore è un oggetto [**CImageAllocator**](cimageallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="dcf27-111">The value returned by this method applies only when the allocator is a [**CImageAllocator**](cimageallocator.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="dcf27-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dcf27-112">Requirements</span></span>



| <span data-ttu-id="dcf27-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="dcf27-113">Requirement</span></span> | <span data-ttu-id="dcf27-114">Valore</span><span class="sxs-lookup"><span data-stu-id="dcf27-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dcf27-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dcf27-115">Header</span></span><br/>  | <dl> <span data-ttu-id="dcf27-116"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dcf27-116"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="dcf27-117">Libreria</span><span class="sxs-lookup"><span data-stu-id="dcf27-117">Library</span></span><br/> | <dl> <span data-ttu-id="dcf27-118"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="dcf27-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dcf27-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dcf27-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcf27-120">**Classe CDrawImage**</span><span class="sxs-lookup"><span data-stu-id="dcf27-120">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> <dt>

[<span data-ttu-id="dcf27-121">**CDrawImage::IncrementPaletteVersion**</span><span class="sxs-lookup"><span data-stu-id="dcf27-121">**CDrawImage::IncrementPaletteVersion**</span></span>](cdrawimage-incrementpaletteversion.md)
</dt> <dt>

[<span data-ttu-id="dcf27-122">**CDrawImage::ResetPaletteVersion**</span><span class="sxs-lookup"><span data-stu-id="dcf27-122">**CDrawImage::ResetPaletteVersion**</span></span>](cdrawimage-resetpaletteversion.md)
</dt> </dl>

 

 




