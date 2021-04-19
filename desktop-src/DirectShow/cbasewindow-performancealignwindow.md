---
description: Il metodo PerformanceAlignWindow allinea la posizione della finestra ai limiti DWORD, per ottenere le prestazioni massime.
ms.assetid: e28950bc-2510-45b9-9c9c-c2a9dbc3dc02
title: Metodo CBaseWindow. PerformanceAlignWindow (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.PerformanceAlignWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e6e7a54372743d430cd904f47c79414d149cf033
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332587"
---
# <a name="cbasewindowperformancealignwindow-method"></a><span data-ttu-id="e3b9e-103">CBaseWindow. PerformanceAlignWindow, metodo</span><span class="sxs-lookup"><span data-stu-id="e3b9e-103">CBaseWindow.PerformanceAlignWindow method</span></span>

<span data-ttu-id="e3b9e-104">Il `PerformanceAlignWindow` Metodo allinea la posizione della finestra ai limiti **DWORD** , per ottenere le prestazioni massime.</span><span class="sxs-lookup"><span data-stu-id="e3b9e-104">The `PerformanceAlignWindow` method aligns the window position to **DWORD** boundaries, for maximum performance.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3b9e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e3b9e-105">Syntax</span></span>


```C++
HRESULT PerformanceAlignWindow();
```



## <a name="parameters"></a><span data-ttu-id="e3b9e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e3b9e-106">Parameters</span></span>

<span data-ttu-id="e3b9e-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="e3b9e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e3b9e-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e3b9e-108">Return value</span></span>

<span data-ttu-id="e3b9e-109">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e3b9e-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3b9e-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="e3b9e-110">Remarks</span></span>

<span data-ttu-id="e3b9e-111">Questo metodo allinea i bordi sinistro e superiore della finestra ai limiti DWORD, che possono migliorare le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="e3b9e-111">This method aligns the left and top edges of the window to DWORD boundaries, which can improve performance.</span></span> <span data-ttu-id="e3b9e-112">Se la finestra dispone di un elemento padre, il metodo restituisce \_ OK, ma esegue l'allineamento.</span><span class="sxs-lookup"><span data-stu-id="e3b9e-112">If the window has a parent, the method returns S\_OK but does perform the alignment.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3b9e-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e3b9e-113">Requirements</span></span>



| <span data-ttu-id="e3b9e-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3b9e-114">Requirement</span></span> | <span data-ttu-id="e3b9e-115">Valore</span><span class="sxs-lookup"><span data-stu-id="e3b9e-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3b9e-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e3b9e-116">Header</span></span><br/>  | <dl> <span data-ttu-id="e3b9e-117"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e3b9e-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e3b9e-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="e3b9e-118">Library</span></span><br/> | <dl> <span data-ttu-id="e3b9e-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="e3b9e-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3b9e-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e3b9e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3b9e-121">**Classe CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="e3b9e-121">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




