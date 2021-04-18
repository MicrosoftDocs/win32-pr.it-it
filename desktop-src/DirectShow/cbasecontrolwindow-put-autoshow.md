---
description: Il \_ metodo Put Autoshow imposta il flag di stato di visualizzazione.
ms.assetid: 857472b8-845b-46d3-8593-3fba9a9c8cdc
title: Metodo CBaseControlWindow.put_AutoShow (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_AutoShow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: eda5c0c4055979537c5cc471053715e29a348f1a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327225"
---
# <a name="cbasecontrolwindowput_autoshow-method"></a><span data-ttu-id="d4f87-103">CBaseControlWindow. put \_ AutoShow (metodo)</span><span class="sxs-lookup"><span data-stu-id="d4f87-103">CBaseControlWindow.put\_AutoShow method</span></span>

<span data-ttu-id="d4f87-104">Il `put_AutoShow` metodo imposta il flag di stato di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="d4f87-104">The `put_AutoShow` method sets the AutoShow state flag.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4f87-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d4f87-105">Syntax</span></span>


```C++
HRESULT put_AutoShow(
   long AutoShow
);
```



## <a name="parameters"></a><span data-ttu-id="d4f87-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d4f87-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4f87-107">*AutoShow*</span><span class="sxs-lookup"><span data-stu-id="d4f87-107">*AutoShow*</span></span> 
</dt> <dd>

<span data-ttu-id="d4f87-108">Flag booleano di automazione (0 è disattivato, 1 è on).</span><span class="sxs-lookup"><span data-stu-id="d4f87-108">Automation Boolean flag (0 is off,  1 is on).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4f87-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d4f87-109">Return value</span></span>

<span data-ttu-id="d4f87-110">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d4f87-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d4f87-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="d4f87-111">Remarks</span></span>

<span data-ttu-id="d4f87-112">Questa proprietà semplifica l'accesso alla visualizzazione delle finestre per le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="d4f87-112">This property simplifies window display access for applications.</span></span> <span data-ttu-id="d4f87-113">Se questa impostazione è impostata su 1 (on), la finestra, che in genere è nascosta dopo la connessione del filtro, verrà visualizzata automaticamente quando il filtro viene sospeso o eseguito.</span><span class="sxs-lookup"><span data-stu-id="d4f87-113">If this is set to  1 (on), the window, which is typically hidden after the filter is connected, will be displayed automatically when the filter pauses or runs.</span></span> <span data-ttu-id="d4f87-114">Tuttavia, la finestra non deve essere nascosta quando il filtro si arresta.</span><span class="sxs-lookup"><span data-stu-id="d4f87-114">The window should not be hidden when the filter stops, however.</span></span> <span data-ttu-id="d4f87-115">Se è impostato su 0 (disattivato), la finestra viene resa visibile solo quando l'applicazione chiama [**CBaseControlWindow::p UT \_ Visible**](cbasecontrolwindow-put-visible.md) o [**CBaseControlWindow::p UT \_ WindowState**](cbasecontrolwindow-put-windowstate.md) con i parametri appropriati.</span><span class="sxs-lookup"><span data-stu-id="d4f87-115">If this is set to 0 (off), the window is made visible only when the application calls [**CBaseControlWindow::put\_Visible**](cbasecontrolwindow-put-visible.md) or [**CBaseControlWindow::put\_WindowState**](cbasecontrolwindow-put-windowstate.md) with the appropriate parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4f87-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d4f87-116">Requirements</span></span>



| <span data-ttu-id="d4f87-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4f87-117">Requirement</span></span> | <span data-ttu-id="d4f87-118">Valore</span><span class="sxs-lookup"><span data-stu-id="d4f87-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4f87-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d4f87-119">Header</span></span><br/>  | <dl> <span data-ttu-id="d4f87-120"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d4f87-120"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d4f87-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="d4f87-121">Library</span></span><br/> | <dl> <span data-ttu-id="d4f87-122"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d4f87-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4f87-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d4f87-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4f87-124">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="d4f87-124">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




