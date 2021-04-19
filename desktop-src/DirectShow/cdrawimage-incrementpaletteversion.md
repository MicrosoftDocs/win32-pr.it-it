---
description: Il metodo IncrementPaletteVersion incrementa la versione della tavolozza. Chiamare questo metodo se il tipo di supporto viene modificato in un nuovo formato pallettizzati.
ms.assetid: 1ce77f97-d225-45f5-a259-1dcca1272d15
title: Metodo CDrawImage. IncrementPaletteVersion (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.IncrementPaletteVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 21b4220ec98c5b083913e92f5749866f629a4854
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331929"
---
# <a name="cdrawimageincrementpaletteversion-method"></a><span data-ttu-id="a4bfd-104">CDrawImage. IncrementPaletteVersion, metodo</span><span class="sxs-lookup"><span data-stu-id="a4bfd-104">CDrawImage.IncrementPaletteVersion method</span></span>

<span data-ttu-id="a4bfd-105">Il `IncrementPaletteVersion` metodo incrementa la versione della tavolozza.</span><span class="sxs-lookup"><span data-stu-id="a4bfd-105">The `IncrementPaletteVersion` method increments the palette version.</span></span> <span data-ttu-id="a4bfd-106">Chiamare questo metodo se il tipo di supporto viene modificato in un nuovo formato pallettizzati.</span><span class="sxs-lookup"><span data-stu-id="a4bfd-106">Call this method if the media type changes to a new palettized format.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4bfd-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a4bfd-107">Syntax</span></span>


```C++
void IncrementPaletteVersion();
```



## <a name="parameters"></a><span data-ttu-id="a4bfd-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a4bfd-108">Parameters</span></span>

<span data-ttu-id="a4bfd-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="a4bfd-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a4bfd-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a4bfd-110">Return value</span></span>

<span data-ttu-id="a4bfd-111">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="a4bfd-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4bfd-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="a4bfd-112">Remarks</span></span>

<span data-ttu-id="a4bfd-113">Questo metodo incrementa il valore della variabile membro **\_ PaletteVersion m** .</span><span class="sxs-lookup"><span data-stu-id="a4bfd-113">This method increments the value of the **m\_PaletteVersion** member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4bfd-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a4bfd-114">Requirements</span></span>



| <span data-ttu-id="a4bfd-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4bfd-115">Requirement</span></span> | <span data-ttu-id="a4bfd-116">Valore</span><span class="sxs-lookup"><span data-stu-id="a4bfd-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4bfd-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a4bfd-117">Header</span></span><br/>  | <dl> <span data-ttu-id="a4bfd-118"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a4bfd-118"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a4bfd-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="a4bfd-119">Library</span></span><br/> | <dl> <span data-ttu-id="a4bfd-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="a4bfd-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4bfd-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a4bfd-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4bfd-122">**Classe CDrawImage**</span><span class="sxs-lookup"><span data-stu-id="a4bfd-122">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> <dt>

[<span data-ttu-id="a4bfd-123">**CDrawImage::GetPaletteVersion**</span><span class="sxs-lookup"><span data-stu-id="a4bfd-123">**CDrawImage::GetPaletteVersion**</span></span>](cdrawimage-getpaletteversion.md)
</dt> <dt>

[<span data-ttu-id="a4bfd-124">**CDrawImage::ResetPaletteVersion**</span><span class="sxs-lookup"><span data-stu-id="a4bfd-124">**CDrawImage::ResetPaletteVersion**</span></span>](cdrawimage-resetpaletteversion.md)
</dt> </dl>

 

 




