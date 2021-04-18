---
description: Il metodo GetTargetRect Recupera il rettangolo di destinazione corrente.
ms.assetid: b6542b06-af36-4666-b6fa-d9fa3c6c7044
title: Metodo CDrawImage. GetTargetRect (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.GetTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 547dd12117cec95ad1cb0159667a8dd72a95a6e5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327208"
---
# <a name="cdrawimagegettargetrect-method"></a><span data-ttu-id="b6882-103">CDrawImage. GetTargetRect, metodo</span><span class="sxs-lookup"><span data-stu-id="b6882-103">CDrawImage.GetTargetRect method</span></span>

<span data-ttu-id="b6882-104">Il `GetTargetRect` metodo recupera il rettangolo di destinazione corrente.</span><span class="sxs-lookup"><span data-stu-id="b6882-104">The `GetTargetRect` method retrieves the current destination rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6882-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b6882-105">Syntax</span></span>


```C++
void GetTargetRect(
   RECT *pTargetRect
);
```



## <a name="parameters"></a><span data-ttu-id="b6882-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b6882-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6882-107">*pTargetRect*</span><span class="sxs-lookup"><span data-stu-id="b6882-107">*pTargetRect*</span></span> 
</dt> <dd>

<span data-ttu-id="b6882-108">Puntatore a una struttura **Rect** che riceve il rettangolo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="b6882-108">Pointer to a **RECT** structure that receives the target rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6882-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b6882-109">Return value</span></span>

<span data-ttu-id="b6882-110">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="b6882-110">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6882-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b6882-111">Requirements</span></span>



| <span data-ttu-id="b6882-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6882-112">Requirement</span></span> | <span data-ttu-id="b6882-113">Valore</span><span class="sxs-lookup"><span data-stu-id="b6882-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6882-114">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b6882-114">Header</span></span><br/>  | <dl> <span data-ttu-id="b6882-115"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b6882-115"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b6882-116">Libreria</span><span class="sxs-lookup"><span data-stu-id="b6882-116">Library</span></span><br/> | <dl> <span data-ttu-id="b6882-117"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b6882-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6882-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b6882-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6882-119">**Classe CDrawImage**</span><span class="sxs-lookup"><span data-stu-id="b6882-119">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 




