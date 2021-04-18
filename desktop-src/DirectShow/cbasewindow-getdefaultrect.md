---
description: Il metodo GetDefaultRect recupera le dimensioni predefinite dell'area client.
ms.assetid: 9eb9e3a4-0d45-4aa3-a496-1b0bd92d4989
title: Metodo CBaseWindow. GetDefaultRect (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.GetDefaultRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1d7ec9612eab45e21262f8344daf7a52a6a888b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327944"
---
# <a name="cbasewindowgetdefaultrect-method"></a><span data-ttu-id="e224b-103">CBaseWindow. GetDefaultRect, metodo</span><span class="sxs-lookup"><span data-stu-id="e224b-103">CBaseWindow.GetDefaultRect method</span></span>

<span data-ttu-id="e224b-104">Il `GetDefaultRect` metodo recupera le dimensioni predefinite dell'area client.</span><span class="sxs-lookup"><span data-stu-id="e224b-104">The `GetDefaultRect` method retrieves the default size of the client area.</span></span>

## <a name="syntax"></a><span data-ttu-id="e224b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e224b-105">Syntax</span></span>


```C++
virtual RECT GetDefaultRect();
```



## <a name="parameters"></a><span data-ttu-id="e224b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e224b-106">Parameters</span></span>

<span data-ttu-id="e224b-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="e224b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e224b-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e224b-108">Return value</span></span>

<span data-ttu-id="e224b-109">Restituisce il rettangolo predefinito.</span><span class="sxs-lookup"><span data-stu-id="e224b-109">Returns the default rectangle.</span></span>

## <a name="remarks"></a><span data-ttu-id="e224b-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="e224b-110">Remarks</span></span>

<span data-ttu-id="e224b-111">Quando la finestra viene attivata, l'oggetto chiama questo metodo per determinare la dimensione che deve rendere l'area client della finestra.</span><span class="sxs-lookup"><span data-stu-id="e224b-111">When the window is activated, the object calls this method to determine how large it should make the window's client area.</span></span> <span data-ttu-id="e224b-112">Nella classe di base, questo metodo restituisce un rettangolo la cui altezza e larghezza sono le costanti definite DEFHEIGHT e DEFWIDTH.</span><span class="sxs-lookup"><span data-stu-id="e224b-112">In the base class, this method returns a rectangle whose height and width are the defined constants DEFHEIGHT and DEFWIDTH.</span></span> <span data-ttu-id="e224b-113">Una classe derivata deve eseguire l'override di questo metodo.</span><span class="sxs-lookup"><span data-stu-id="e224b-113">A derived class should override this method.</span></span> <span data-ttu-id="e224b-114">Per un renderer video, la classe derivata restituirà in genere le dimensioni dell'immagine video nativa.</span><span class="sxs-lookup"><span data-stu-id="e224b-114">For a video renderer, the derived class will typically return the size of the native video image.</span></span>

## <a name="requirements"></a><span data-ttu-id="e224b-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e224b-115">Requirements</span></span>



| <span data-ttu-id="e224b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e224b-116">Requirement</span></span> | <span data-ttu-id="e224b-117">Valore</span><span class="sxs-lookup"><span data-stu-id="e224b-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e224b-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e224b-118">Header</span></span><br/>  | <dl> <span data-ttu-id="e224b-119"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e224b-119"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e224b-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="e224b-120">Library</span></span><br/> | <dl> <span data-ttu-id="e224b-121"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="e224b-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e224b-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e224b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e224b-123">**Classe CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="e224b-123">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




