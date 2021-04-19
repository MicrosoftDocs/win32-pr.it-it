---
description: Il metodo OnSize gestisce \_ i messaggi di dimensioni WM.
ms.assetid: 21d867a4-4321-478a-9beb-5d3053569369
title: Metodo CBaseWindow. OnSize (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.OnSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c9020510030d3b3d4b30e066adfe67367618fb3d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325760"
---
# <a name="cbasewindowonsize-method"></a><span data-ttu-id="d4276-103">Metodo CBaseWindow. OnSize</span><span class="sxs-lookup"><span data-stu-id="d4276-103">CBaseWindow.OnSize method</span></span>

<span data-ttu-id="d4276-104">Il `OnSize` metodo gestisce \_ i messaggi di dimensioni WM.</span><span class="sxs-lookup"><span data-stu-id="d4276-104">The `OnSize` method handles WM\_SIZE messages.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4276-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d4276-105">Syntax</span></span>


```C++
virtual BOOL OnSize(
   LONG Width,
   LONG Height
);
```



## <a name="parameters"></a><span data-ttu-id="d4276-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d4276-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4276-107">*Larghezza*</span><span class="sxs-lookup"><span data-stu-id="d4276-107">*Width*</span></span> 
</dt> <dd>

<span data-ttu-id="d4276-108">Larghezza dell'area client in pixel.</span><span class="sxs-lookup"><span data-stu-id="d4276-108">Width of the client area, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="d4276-109">*Altezza*</span><span class="sxs-lookup"><span data-stu-id="d4276-109">*Height*</span></span> 
</dt> <dd>

<span data-ttu-id="d4276-110">Altezza dell'area client in pixel.</span><span class="sxs-lookup"><span data-stu-id="d4276-110">Height of the client area, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4276-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d4276-111">Return value</span></span>

<span data-ttu-id="d4276-112">Restituisce **true**.</span><span class="sxs-lookup"><span data-stu-id="d4276-112">Returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d4276-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="d4276-113">Remarks</span></span>

<span data-ttu-id="d4276-114">Questo metodo archivia la nuova larghezza e altezza.</span><span class="sxs-lookup"><span data-stu-id="d4276-114">This method stores the new width and height.</span></span> <span data-ttu-id="d4276-115">Per recuperare questi valori, chiamare i metodi [**CBaseWindow:: GetWindowHeight**](cbasewindow-getwindowheight.md) e [**CBaseWindow:: GetWindowWidth**](cbasewindow-getwindowwidth.md) .</span><span class="sxs-lookup"><span data-stu-id="d4276-115">To retrieve these values, call the [**CBaseWindow::GetWindowHeight**](cbasewindow-getwindowheight.md) and [**CBaseWindow::GetWindowWidth**](cbasewindow-getwindowwidth.md) methods.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4276-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d4276-116">Requirements</span></span>



| <span data-ttu-id="d4276-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4276-117">Requirement</span></span> | <span data-ttu-id="d4276-118">Valore</span><span class="sxs-lookup"><span data-stu-id="d4276-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4276-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d4276-119">Header</span></span><br/>  | <dl> <span data-ttu-id="d4276-120"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d4276-120"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d4276-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="d4276-121">Library</span></span><br/> | <dl> <span data-ttu-id="d4276-122"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d4276-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4276-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d4276-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4276-124">**Classe CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="d4276-124">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




