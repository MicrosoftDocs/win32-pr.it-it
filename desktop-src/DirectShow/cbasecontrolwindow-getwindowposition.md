---
description: Il metodo GetWindowPosition recupera le coordinate correnti per la finestra.
ms.assetid: a2f46a87-b2cd-450f-8d2b-0f8695432fda
title: Metodo CBaseControlWindow. GetWindowPosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.GetWindowPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: af2b1bdb8b2c839644e8c0629e3e272c123d3c21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328085"
---
# <a name="cbasecontrolwindowgetwindowposition-method"></a><span data-ttu-id="32f62-103">CBaseControlWindow. GetWindowPosition, metodo</span><span class="sxs-lookup"><span data-stu-id="32f62-103">CBaseControlWindow.GetWindowPosition method</span></span>

<span data-ttu-id="32f62-104">Il `GetWindowPosition` metodo recupera le coordinate correnti per la finestra.</span><span class="sxs-lookup"><span data-stu-id="32f62-104">The `GetWindowPosition` method retrieves the current coordinates for the window.</span></span>

## <a name="syntax"></a><span data-ttu-id="32f62-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="32f62-105">Syntax</span></span>


```C++
HRESULT GetWindowPosition(
   long *pLeft,
   long *pTop,
   long *pWidth,
   long *pHeight
);
```



## <a name="parameters"></a><span data-ttu-id="32f62-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="32f62-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32f62-107">*pLeft*</span><span class="sxs-lookup"><span data-stu-id="32f62-107">*pLeft*</span></span> 
</dt> <dd>

<span data-ttu-id="32f62-108">Puntatore alla coordinata sinistra, espressa in coordinate dello schermo.</span><span class="sxs-lookup"><span data-stu-id="32f62-108">Pointer to the left coordinate, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="32f62-109">*pTop*</span><span class="sxs-lookup"><span data-stu-id="32f62-109">*pTop*</span></span> 
</dt> <dd>

<span data-ttu-id="32f62-110">Puntatore alla coordinata superiore, espressa in coordinate dello schermo.</span><span class="sxs-lookup"><span data-stu-id="32f62-110">Pointer to the top coordinate, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="32f62-111">*pWidth*</span><span class="sxs-lookup"><span data-stu-id="32f62-111">*pWidth*</span></span> 
</dt> <dd>

<span data-ttu-id="32f62-112">Puntatore alla larghezza della finestra, in coordinate dello schermo.</span><span class="sxs-lookup"><span data-stu-id="32f62-112">Pointer to the window width, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="32f62-113">*pHeight*</span><span class="sxs-lookup"><span data-stu-id="32f62-113">*pHeight*</span></span> 
</dt> <dd>

<span data-ttu-id="32f62-114">Puntatore all'altezza della finestra, in coordinate dello schermo.</span><span class="sxs-lookup"><span data-stu-id="32f62-114">Pointer to the window height, in screen coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32f62-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="32f62-115">Return value</span></span>

<span data-ttu-id="32f62-116">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="32f62-116">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="32f62-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="32f62-117">Requirements</span></span>



| <span data-ttu-id="32f62-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="32f62-118">Requirement</span></span> | <span data-ttu-id="32f62-119">Valore</span><span class="sxs-lookup"><span data-stu-id="32f62-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32f62-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="32f62-120">Header</span></span><br/>  | <dl> <span data-ttu-id="32f62-121"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="32f62-121"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="32f62-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="32f62-122">Library</span></span><br/> | <dl> <span data-ttu-id="32f62-123"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="32f62-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32f62-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="32f62-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32f62-125">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="32f62-125">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




