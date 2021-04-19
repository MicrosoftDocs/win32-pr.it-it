---
description: Il metodo CountSetBits restituisce il numero di bit impostato su 1 in un campo di bit specificato.
ms.assetid: fc5701b8-88ff-4c23-9d26-854bb65cc55c
title: Metodo CImageDisplay. CountSetBits (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CountSetBits
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cb425b08b524b1d36b622bcfffcc9f311dccbbdf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333077"
---
# <a name="cimagedisplaycountsetbits-method"></a><span data-ttu-id="7c3e2-103">CImageDisplay. CountSetBits, metodo</span><span class="sxs-lookup"><span data-stu-id="7c3e2-103">CImageDisplay.CountSetBits method</span></span>

<span data-ttu-id="7c3e2-104">Il `CountSetBits` metodo restituisce il numero di bit impostato su 1 in un campo di bit specificato.</span><span class="sxs-lookup"><span data-stu-id="7c3e2-104">The `CountSetBits` method returns the number of bits set to 1 in a specified bit field.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c3e2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7c3e2-105">Syntax</span></span>


```C++
DWORD CountSetBits(
   const DWORD Field
);
```



## <a name="parameters"></a><span data-ttu-id="7c3e2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7c3e2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c3e2-107">*Campo*</span><span class="sxs-lookup"><span data-stu-id="7c3e2-107">*Field*</span></span> 
</dt> <dd>

<span data-ttu-id="7c3e2-108">Specifica un campo di bit come valore **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="7c3e2-108">Specifies a bit field as a **DWORD** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c3e2-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7c3e2-109">Return value</span></span>

<span data-ttu-id="7c3e2-110">Restituisce il numero di bit impostati su 1.</span><span class="sxs-lookup"><span data-stu-id="7c3e2-110">Returns the number of bits that are set to 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c3e2-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7c3e2-111">Requirements</span></span>



| <span data-ttu-id="7c3e2-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c3e2-112">Requirement</span></span> | <span data-ttu-id="7c3e2-113">Valore</span><span class="sxs-lookup"><span data-stu-id="7c3e2-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c3e2-114">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7c3e2-114">Header</span></span><br/>  | <dl> <span data-ttu-id="7c3e2-115"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7c3e2-115"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7c3e2-116">Libreria</span><span class="sxs-lookup"><span data-stu-id="7c3e2-116">Library</span></span><br/> | <dl> <span data-ttu-id="7c3e2-117"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="7c3e2-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c3e2-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7c3e2-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c3e2-119">**Classe CImageDisplay**</span><span class="sxs-lookup"><span data-stu-id="7c3e2-119">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 




