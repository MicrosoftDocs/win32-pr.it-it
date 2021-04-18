---
description: Il metodo GetRestorePosition recupera la posizione in cui la finestra verrà ripristinata quando non è ingrandita o ridotta a icona.
ms.assetid: 5f129be3-c4d8-4583-bbc8-870e0bcafd80
title: Metodo CBaseControlWindow. GetRestorePosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.GetRestorePosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f922a97f69f4dae03d4e61a54bd99c52d69a984a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328086"
---
# <a name="cbasecontrolwindowgetrestoreposition-method"></a><span data-ttu-id="d0dfa-103">CBaseControlWindow. GetRestorePosition, metodo</span><span class="sxs-lookup"><span data-stu-id="d0dfa-103">CBaseControlWindow.GetRestorePosition method</span></span>

<span data-ttu-id="d0dfa-104">Il `GetRestorePosition` metodo recupera la posizione in cui la finestra verrà ripristinata quando non è ingrandita o ridotta a icona.</span><span class="sxs-lookup"><span data-stu-id="d0dfa-104">The `GetRestorePosition` method retrieves the position to which the window will be restored when it is not maximized or minimized.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0dfa-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d0dfa-105">Syntax</span></span>


```C++
HRESULT GetRestorePosition(
   long *pLeft,
   long *pTop,
   long *pWidth,
   long *pHeight
);
```



## <a name="parameters"></a><span data-ttu-id="d0dfa-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d0dfa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0dfa-107">*pLeft*</span><span class="sxs-lookup"><span data-stu-id="d0dfa-107">*pLeft*</span></span> 
</dt> <dd>

<span data-ttu-id="d0dfa-108">Puntatore al valore per la coordinata più a sinistra.</span><span class="sxs-lookup"><span data-stu-id="d0dfa-108">Pointer to the value for leftmost coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="d0dfa-109">*pTop*</span><span class="sxs-lookup"><span data-stu-id="d0dfa-109">*pTop*</span></span> 
</dt> <dd>

<span data-ttu-id="d0dfa-110">Puntatore al valore per la parte superiore della finestra.</span><span class="sxs-lookup"><span data-stu-id="d0dfa-110">Pointer to the value for top of the window.</span></span>

</dd> <dt>

<span data-ttu-id="d0dfa-111">*pWidth*</span><span class="sxs-lookup"><span data-stu-id="d0dfa-111">*pWidth*</span></span> 
</dt> <dd>

<span data-ttu-id="d0dfa-112">Puntatore al valore per la larghezza della finestra.</span><span class="sxs-lookup"><span data-stu-id="d0dfa-112">Pointer to the value for width of the window.</span></span>

</dd> <dt>

<span data-ttu-id="d0dfa-113">*pHeight*</span><span class="sxs-lookup"><span data-stu-id="d0dfa-113">*pHeight*</span></span> 
</dt> <dd>

<span data-ttu-id="d0dfa-114">Puntatore al valore per l'altezza della finestra.</span><span class="sxs-lookup"><span data-stu-id="d0dfa-114">Pointer to the value for height of window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0dfa-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d0dfa-115">Return value</span></span>

<span data-ttu-id="d0dfa-116">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d0dfa-116">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0dfa-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="d0dfa-117">Remarks</span></span>

<span data-ttu-id="d0dfa-118">Equivale ai valori restituiti dalla funzione [**CBaseControlWindow:: GetWindowPosition**](cbasecontrolwindow-getwindowposition.md) quando la finestra non è né ingrandita né ridotta a icona.</span><span class="sxs-lookup"><span data-stu-id="d0dfa-118">This is the same as the values returned by the [**CBaseControlWindow::GetWindowPosition**](cbasecontrolwindow-getwindowposition.md) function when the window is neither maximized nor minimized.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0dfa-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d0dfa-119">Requirements</span></span>



| <span data-ttu-id="d0dfa-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0dfa-120">Requirement</span></span> | <span data-ttu-id="d0dfa-121">Valore</span><span class="sxs-lookup"><span data-stu-id="d0dfa-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0dfa-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d0dfa-122">Header</span></span><br/>  | <dl> <span data-ttu-id="d0dfa-123"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d0dfa-123"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d0dfa-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="d0dfa-124">Library</span></span><br/> | <dl> <span data-ttu-id="d0dfa-125"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d0dfa-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0dfa-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d0dfa-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0dfa-127">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="d0dfa-127">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




