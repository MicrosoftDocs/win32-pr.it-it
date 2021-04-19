---
description: Il metodo ResetPaletteVersion Reimposta la versione della tavolozza. Chiamare questo metodo se il pin del filtro proprietario si riconnette.
ms.assetid: c9e5588c-5501-4356-bdec-a339d33f9eb5
title: Metodo CDrawImage. ResetPaletteVersion (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.ResetPaletteVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a94cd04de428a29308ead8fa33ccfe1792e021a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326825"
---
# <a name="cdrawimageresetpaletteversion-method"></a><span data-ttu-id="2561c-104">CDrawImage. ResetPaletteVersion, metodo</span><span class="sxs-lookup"><span data-stu-id="2561c-104">CDrawImage.ResetPaletteVersion method</span></span>

<span data-ttu-id="2561c-105">Il `ResetPaletteVersion` metodo reimposta la versione della tavolozza.</span><span class="sxs-lookup"><span data-stu-id="2561c-105">The `ResetPaletteVersion` method resets the palette version.</span></span> <span data-ttu-id="2561c-106">Chiamare questo metodo se il pin del filtro proprietario si riconnette.</span><span class="sxs-lookup"><span data-stu-id="2561c-106">Call this method if the owning filter's pin reconnects.</span></span>

## <a name="syntax"></a><span data-ttu-id="2561c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2561c-107">Syntax</span></span>


```C++
void ResetPaletteVersion();
```



## <a name="parameters"></a><span data-ttu-id="2561c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="2561c-108">Parameters</span></span>

<span data-ttu-id="2561c-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="2561c-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2561c-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2561c-110">Return value</span></span>

<span data-ttu-id="2561c-111">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="2561c-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2561c-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="2561c-112">Remarks</span></span>

<span data-ttu-id="2561c-113">Questo metodo imposta il valore di **m \_ PaletteVersion** su una costante predefinita, una **\_ versione della tavolozza**.</span><span class="sxs-lookup"><span data-stu-id="2561c-113">This method sets the value of **m\_PaletteVersion** to a predefined constant, **PALETTE\_VERSION**.</span></span>

## <a name="requirements"></a><span data-ttu-id="2561c-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2561c-114">Requirements</span></span>



| <span data-ttu-id="2561c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="2561c-115">Requirement</span></span> | <span data-ttu-id="2561c-116">Valore</span><span class="sxs-lookup"><span data-stu-id="2561c-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2561c-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2561c-117">Header</span></span><br/>  | <dl> <span data-ttu-id="2561c-118"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2561c-118"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2561c-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="2561c-119">Library</span></span><br/> | <dl> <span data-ttu-id="2561c-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="2561c-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2561c-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2561c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2561c-122">**Classe CDrawImage**</span><span class="sxs-lookup"><span data-stu-id="2561c-122">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> <dt>

[<span data-ttu-id="2561c-123">**CDrawImage::GetPaletteVersion**</span><span class="sxs-lookup"><span data-stu-id="2561c-123">**CDrawImage::GetPaletteVersion**</span></span>](cdrawimage-getpaletteversion.md)
</dt> <dt>

[<span data-ttu-id="2561c-124">**CDrawImage::IncrementPaletteVersion**</span><span class="sxs-lookup"><span data-stu-id="2561c-124">**CDrawImage::IncrementPaletteVersion**</span></span>](cdrawimage-incrementpaletteversion.md)
</dt> </dl>

 

 




