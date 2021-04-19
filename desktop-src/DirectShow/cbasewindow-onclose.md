---
description: Il metodo OnClose gestisce \_ i messaggi di chiusura WM.
ms.assetid: e562add4-752e-4665-a75e-a5526fb7f045
title: Metodo CBaseWindow. OnClose (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.OnClose
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 189b08c116f66ff864ffe308befb990973c6ce43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325766"
---
# <a name="cbasewindowonclose-method"></a><span data-ttu-id="d38fc-103">Metodo CBaseWindow. OnClose</span><span class="sxs-lookup"><span data-stu-id="d38fc-103">CBaseWindow.OnClose method</span></span>

<span data-ttu-id="d38fc-104">Il `OnClose` metodo gestisce \_ i messaggi di chiusura WM.</span><span class="sxs-lookup"><span data-stu-id="d38fc-104">The `OnClose` method handles WM\_CLOSE messages.</span></span>

## <a name="syntax"></a><span data-ttu-id="d38fc-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d38fc-105">Syntax</span></span>


```C++
virtual BOOL OnClose();
```



## <a name="parameters"></a><span data-ttu-id="d38fc-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d38fc-106">Parameters</span></span>

<span data-ttu-id="d38fc-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="d38fc-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d38fc-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d38fc-108">Return value</span></span>

<span data-ttu-id="d38fc-109">Restituisce **true**.</span><span class="sxs-lookup"><span data-stu-id="d38fc-109">Returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d38fc-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="d38fc-110">Remarks</span></span>

<span data-ttu-id="d38fc-111">Nella classe di base, questo metodo nasconde semplicemente la finestra.</span><span class="sxs-lookup"><span data-stu-id="d38fc-111">In the base class, this method simply hides the window.</span></span> <span data-ttu-id="d38fc-112">In genere, una classe derivata eseguirà l'override di questo metodo in modo che invii anche un evento [**EC \_ USERABORT**](ec-userabort.md) .</span><span class="sxs-lookup"><span data-stu-id="d38fc-112">Typically, a derived class will override this method so that it sends an [**EC\_USERABORT**](ec-userabort.md) event as well.</span></span> <span data-ttu-id="d38fc-113">Non eseguire l'override del metodo per eliminare definitivamente la finestra.</span><span class="sxs-lookup"><span data-stu-id="d38fc-113">Do not override the method to destroy the window.</span></span> <span data-ttu-id="d38fc-114">Al contrario, chiamare il metodo [**CBaseWindow::D onewithwindow**](cbasewindow-donewithwindow.md) quando il filtro proprietario viene eliminato definitivamente.</span><span class="sxs-lookup"><span data-stu-id="d38fc-114">Instead, call the [**CBaseWindow::DoneWithWindow**](cbasewindow-donewithwindow.md) method when the owning filter is destroyed.</span></span>

## <a name="requirements"></a><span data-ttu-id="d38fc-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d38fc-115">Requirements</span></span>



| <span data-ttu-id="d38fc-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d38fc-116">Requirement</span></span> | <span data-ttu-id="d38fc-117">Valore</span><span class="sxs-lookup"><span data-stu-id="d38fc-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d38fc-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d38fc-118">Header</span></span><br/>  | <dl> <span data-ttu-id="d38fc-119"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d38fc-119"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d38fc-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="d38fc-120">Library</span></span><br/> | <dl> <span data-ttu-id="d38fc-121"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d38fc-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d38fc-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d38fc-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d38fc-123">**Classe CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="d38fc-123">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




