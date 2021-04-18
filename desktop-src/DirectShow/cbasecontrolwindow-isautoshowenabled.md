---
description: Il metodo IsAutoShowEnabled recupera informazioni sull'eventuale visualizzazione automatica della finestra video quando il filtro di rendering viene sospeso o eseguito.
ms.assetid: 769e3023-a515-4b80-a979-2e4fa9612e65
title: Metodo CBaseControlWindow. IsAutoShowEnabled (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.IsAutoShowEnabled
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2c4b4a894593cb3be26a1034098cd2a0cdacf926
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329264"
---
# <a name="cbasecontrolwindowisautoshowenabled-method"></a><span data-ttu-id="08aca-103">CBaseControlWindow. IsAutoShowEnabled, metodo</span><span class="sxs-lookup"><span data-stu-id="08aca-103">CBaseControlWindow.IsAutoShowEnabled method</span></span>

<span data-ttu-id="08aca-104">Il `IsAutoShowEnabled` metodo recupera informazioni sull'eventuale visualizzazione automatica della finestra video quando il filtro di rendering viene sospeso o eseguito.</span><span class="sxs-lookup"><span data-stu-id="08aca-104">The `IsAutoShowEnabled` method retrieves information about whether the video window automatically appears when the rendering filter pauses or runs.</span></span>

## <a name="syntax"></a><span data-ttu-id="08aca-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="08aca-105">Syntax</span></span>


```C++
BOOL IsAutoShowEnabled();
```



## <a name="parameters"></a><span data-ttu-id="08aca-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="08aca-106">Parameters</span></span>

<span data-ttu-id="08aca-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="08aca-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="08aca-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="08aca-108">Return value</span></span>

<span data-ttu-id="08aca-109">Restituisce **true** se il **membro \_ bAutoShow m** è impostato su 1 o su **false** se è impostato su 0.</span><span class="sxs-lookup"><span data-stu-id="08aca-109">Returns **TRUE** if the **m\_bAutoShow** member is set to  1 or **FALSE** if it is set to 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="08aca-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="08aca-110">Remarks</span></span>

<span data-ttu-id="08aca-111">Se il **membro \_ bAutoShow m** è impostato su 1 in una finestra video nascosta, la finestra diventa visibile quando il filtro viene sospeso o eseguito.</span><span class="sxs-lookup"><span data-stu-id="08aca-111">If the **m\_bAutoShow** member is set to  1 on a video window that is hidden, the window becomes visible when the filter pauses or runs.</span></span> <span data-ttu-id="08aca-112">Se questo membro è impostato su 0, la finestra viene visualizzata solo se si usa la funzione membro [**CBaseControlWindow::p UT \_ Visible**](cbasecontrolwindow-put-visible.md) o [**CBaseControlWindow::p UT \_ WindowState**](cbasecontrolwindow-put-windowstate.md) con i parametri appropriati.</span><span class="sxs-lookup"><span data-stu-id="08aca-112">If this member is set to 0, the window will appear only if you use the [**CBaseControlWindow::put\_Visible**](cbasecontrolwindow-put-visible.md) or [**CBaseControlWindow::put\_WindowState**](cbasecontrolwindow-put-windowstate.md) member function with the appropriate parameters.</span></span>

<span data-ttu-id="08aca-113">Questa funzione membro recupera l'impostazione del membro **\_ bAutoShow di m** e ha lo stesso risultato dell'utilizzo del metodo [**IVideoWindow:: Get \_ AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-get_autoshow) .</span><span class="sxs-lookup"><span data-stu-id="08aca-113">This member function retrieves the **m\_bAutoShow** member setting and has the same result as using the [**IVideoWindow::get\_AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-get_autoshow) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="08aca-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="08aca-114">Requirements</span></span>



| <span data-ttu-id="08aca-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="08aca-115">Requirement</span></span> | <span data-ttu-id="08aca-116">Valore</span><span class="sxs-lookup"><span data-stu-id="08aca-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08aca-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="08aca-117">Header</span></span><br/>  | <dl> <span data-ttu-id="08aca-118"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="08aca-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="08aca-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="08aca-119">Library</span></span><br/> | <dl> <span data-ttu-id="08aca-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="08aca-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08aca-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="08aca-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08aca-122">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="08aca-122">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




