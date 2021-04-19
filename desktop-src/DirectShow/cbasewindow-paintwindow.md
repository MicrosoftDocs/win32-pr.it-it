---
description: Il metodo PaintWindow fa sì che la finestra venga ridisegnata.
ms.assetid: dce3d782-00e5-4176-9365-378d59d48ebc
title: Metodo CBaseWindow. PaintWindow (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.PaintWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3b0932422f85cb31d587485976dfacbaa51e2bf7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332589"
---
# <a name="cbasewindowpaintwindow-method"></a><span data-ttu-id="d4dd1-103">CBaseWindow. PaintWindow, metodo</span><span class="sxs-lookup"><span data-stu-id="d4dd1-103">CBaseWindow.PaintWindow method</span></span>

<span data-ttu-id="d4dd1-104">Il `PaintWindow` metodo fa sì che la finestra venga ridisegnata.</span><span class="sxs-lookup"><span data-stu-id="d4dd1-104">The `PaintWindow` method causes the window to be repainted.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4dd1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d4dd1-105">Syntax</span></span>


```C++
void PaintWindow(
   BOOL bErase
);
```



## <a name="parameters"></a><span data-ttu-id="d4dd1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d4dd1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4dd1-107">*bErase*</span><span class="sxs-lookup"><span data-stu-id="d4dd1-107">*bErase*</span></span> 
</dt> <dd>

<span data-ttu-id="d4dd1-108">Valore booleano che specifica se lo sfondo è stato cancellato.</span><span class="sxs-lookup"><span data-stu-id="d4dd1-108">Boolean value that specifies whether the background is erased.</span></span> <span data-ttu-id="d4dd1-109">Se il valore è **true**, lo sfondo viene cancellato.</span><span class="sxs-lookup"><span data-stu-id="d4dd1-109">If the value is **TRUE**, the background is erased.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4dd1-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d4dd1-110">Return value</span></span>

<span data-ttu-id="d4dd1-111">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="d4dd1-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d4dd1-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="d4dd1-112">Remarks</span></span>

<span data-ttu-id="d4dd1-113">Questo metodo genera un \_ messaggio di disegno WM invalidando l'intera area client della finestra.</span><span class="sxs-lookup"><span data-stu-id="d4dd1-113">This method generates a WM\_PAINT message by invalidating the window's entire client area.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4dd1-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d4dd1-114">Requirements</span></span>



| <span data-ttu-id="d4dd1-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4dd1-115">Requirement</span></span> | <span data-ttu-id="d4dd1-116">Valore</span><span class="sxs-lookup"><span data-stu-id="d4dd1-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4dd1-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d4dd1-117">Header</span></span><br/>  | <dl> <span data-ttu-id="d4dd1-118"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d4dd1-118"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d4dd1-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="d4dd1-119">Library</span></span><br/> | <dl> <span data-ttu-id="d4dd1-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d4dd1-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4dd1-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d4dd1-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4dd1-122">**Classe CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="d4dd1-122">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




