---
description: Il metodo UninitialiseWindow rilascia le risorse della finestra.
ms.assetid: 8c5bb0c1-1d92-4025-bbbd-1e57ddde4456
title: Metodo CBaseWindow. UninitialiseWindow (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.UninitialiseWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ceeadd0ec7a61422f0127c957125caa9a01dcefb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333325"
---
# <a name="cbasewindowuninitialisewindow-method"></a><span data-ttu-id="c5181-103">CBaseWindow. UninitialiseWindow, metodo</span><span class="sxs-lookup"><span data-stu-id="c5181-103">CBaseWindow.UninitialiseWindow method</span></span>

<span data-ttu-id="c5181-104">Il `UninitialiseWindow` metodo rilascia le risorse della finestra.</span><span class="sxs-lookup"><span data-stu-id="c5181-104">The `UninitialiseWindow` method releases the window's resources.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5181-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c5181-105">Syntax</span></span>


```C++
virtual HRESULT UninitialiseWindow();
```



## <a name="parameters"></a><span data-ttu-id="c5181-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c5181-106">Parameters</span></span>

<span data-ttu-id="c5181-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="c5181-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c5181-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c5181-108">Return value</span></span>

<span data-ttu-id="c5181-109">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c5181-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5181-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="c5181-110">Remarks</span></span>

<span data-ttu-id="c5181-111">Questo metodo libera le risorse acquisite dal metodo [**CBaseWindow:: InitialiseWindow**](cbasewindow-initialisewindow.md) .</span><span class="sxs-lookup"><span data-stu-id="c5181-111">This method frees resources that were acquired by the [**CBaseWindow::InitialiseWindow**](cbasewindow-initialisewindow.md) method.</span></span> <span data-ttu-id="c5181-112">Il metodo [**CBaseWindow::D onewithwindow**](cbasewindow-donewithwindow.md) chiama questo metodo.</span><span class="sxs-lookup"><span data-stu-id="c5181-112">The [**CBaseWindow::DoneWithWindow**](cbasewindow-donewithwindow.md) method calls this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5181-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c5181-113">Requirements</span></span>



| <span data-ttu-id="c5181-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5181-114">Requirement</span></span> | <span data-ttu-id="c5181-115">Valore</span><span class="sxs-lookup"><span data-stu-id="c5181-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5181-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c5181-116">Header</span></span><br/>  | <dl> <span data-ttu-id="c5181-117"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c5181-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c5181-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="c5181-118">Library</span></span><br/> | <dl> <span data-ttu-id="c5181-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="c5181-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5181-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c5181-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5181-121">**Classe CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="c5181-121">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




