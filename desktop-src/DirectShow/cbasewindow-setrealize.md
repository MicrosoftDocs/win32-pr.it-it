---
description: Il metodo sealize specifica se la finestra realizza le tavolozze.
ms.assetid: ab4a6069-c11f-4126-93bf-6de5277970a1
title: Metodo CBaseWindow. sealize (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.SetRealize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 587e54cdbbbf57ddb4cf52e2d5dfb916acaee22d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333326"
---
# <a name="cbasewindowsetrealize-method"></a><span data-ttu-id="306f3-103">Metodo CBaseWindow. sealize</span><span class="sxs-lookup"><span data-stu-id="306f3-103">CBaseWindow.SetRealize method</span></span>

<span data-ttu-id="306f3-104">Il `SetRealize` metodo specifica se la finestra realizza le tavolozze.</span><span class="sxs-lookup"><span data-stu-id="306f3-104">The `SetRealize` method specifies whether the window realizes palettes.</span></span>

## <a name="syntax"></a><span data-ttu-id="306f3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="306f3-105">Syntax</span></span>


```C++
void SetRealize(
   BOOL bRealize
);
```



## <a name="parameters"></a><span data-ttu-id="306f3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="306f3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="306f3-107">*bRealize*</span><span class="sxs-lookup"><span data-stu-id="306f3-107">*bRealize*</span></span> 
</dt> <dd>

<span data-ttu-id="306f3-108">Valore booleano che specifica se realizzare le tavolozze.</span><span class="sxs-lookup"><span data-stu-id="306f3-108">Boolean value that specifies whether to realize palettes.</span></span> <span data-ttu-id="306f3-109">Se **true**, il metodo [**CBaseWindow:: sepalette**](cbasewindow-setpalette.md) realizza le tavolozze.</span><span class="sxs-lookup"><span data-stu-id="306f3-109">If **TRUE**, the [**CBaseWindow::SetPalette**](cbasewindow-setpalette.md) method realizes palettes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="306f3-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="306f3-110">Return value</span></span>

<span data-ttu-id="306f3-111">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="306f3-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="306f3-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="306f3-112">Remarks</span></span>

<span data-ttu-id="306f3-113">Per impostazione predefinita, il metodo **sepalette** realizza la tavolozza specificata.</span><span class="sxs-lookup"><span data-stu-id="306f3-113">By default, the **SetPalette** method realizes the specified palette.</span></span> <span data-ttu-id="306f3-114">Chiamare questo metodo per modificare il comportamento predefinito, in modo che le tavolozze vengano selezionate ma non realizzate.</span><span class="sxs-lookup"><span data-stu-id="306f3-114">Call this method to change the default behavior, so that palettes are selected but not realized.</span></span> <span data-ttu-id="306f3-115">Questo metodo imposta la variabile membro [**CBaseWindow:: m \_ bNoRealize**](cbasewindow-m-bnorealize.md) .</span><span class="sxs-lookup"><span data-stu-id="306f3-115">This method sets the [**CBaseWindow::m\_bNoRealize**](cbasewindow-m-bnorealize.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="306f3-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="306f3-116">Requirements</span></span>



| <span data-ttu-id="306f3-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="306f3-117">Requirement</span></span> | <span data-ttu-id="306f3-118">Valore</span><span class="sxs-lookup"><span data-stu-id="306f3-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="306f3-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="306f3-119">Header</span></span><br/>  | <dl> <span data-ttu-id="306f3-120"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="306f3-120"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="306f3-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="306f3-121">Library</span></span><br/> | <dl> <span data-ttu-id="306f3-122"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="306f3-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="306f3-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="306f3-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="306f3-124">**Classe CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="306f3-124">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




