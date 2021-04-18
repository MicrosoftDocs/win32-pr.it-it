---
description: Il metodo SetStretchMode calcola se l'immagine video deve essere allungata.
ms.assetid: ffdcaf9c-e157-4557-9193-8430c1c451bf
title: Metodo CDrawImage. SetStretchMode (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.SetStretchMode
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 33a4b3a6b104b9e2888776cc59183835f412fdcb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333720"
---
# <a name="cdrawimagesetstretchmode-method"></a><span data-ttu-id="fc525-103">CDrawImage. SetStretchMode, metodo</span><span class="sxs-lookup"><span data-stu-id="fc525-103">CDrawImage.SetStretchMode method</span></span>

<span data-ttu-id="fc525-104">Il `SetStretchMode` metodo calcola se l'immagine video deve essere allungata.</span><span class="sxs-lookup"><span data-stu-id="fc525-104">The `SetStretchMode` method calculates whether the video image must be stretched.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc525-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fc525-105">Syntax</span></span>


```C++
void SetStretchMode();
```



## <a name="parameters"></a><span data-ttu-id="fc525-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="fc525-106">Parameters</span></span>

<span data-ttu-id="fc525-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="fc525-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fc525-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fc525-108">Return value</span></span>

<span data-ttu-id="fc525-109">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="fc525-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc525-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="fc525-110">Remarks</span></span>

<span data-ttu-id="fc525-111">La classe **CDrawImage** chiama automaticamente questo metodo ogni volta che viene modificato il rettangolo di origine o di destinazione.</span><span class="sxs-lookup"><span data-stu-id="fc525-111">The **CDrawImage** class automatically calls this method whenever the source or target rectangle changes.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc525-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fc525-112">Requirements</span></span>



| <span data-ttu-id="fc525-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc525-113">Requirement</span></span> | <span data-ttu-id="fc525-114">Valore</span><span class="sxs-lookup"><span data-stu-id="fc525-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc525-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fc525-115">Header</span></span><br/>  | <dl> <span data-ttu-id="fc525-116"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fc525-116"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="fc525-117">Libreria</span><span class="sxs-lookup"><span data-stu-id="fc525-117">Library</span></span><br/> | <dl> <span data-ttu-id="fc525-118"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="fc525-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc525-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fc525-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc525-120">**Classe CDrawImage**</span><span class="sxs-lookup"><span data-stu-id="fc525-120">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 




