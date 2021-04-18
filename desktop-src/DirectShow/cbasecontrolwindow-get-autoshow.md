---
description: Il \_ metodo Get Autoshow Recupera il flag di stato di Autoshow corrente.
ms.assetid: b27651d1-3ac5-4a52-9549-b63bacda5dc8
title: Metodo CBaseControlWindow.get_AutoShow (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_AutoShow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f45679b9d036f1c5386cd2c1d18a31fa3d6bd64f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325388"
---
# <a name="cbasecontrolwindowget_autoshow-method"></a><span data-ttu-id="993b0-103">CBaseControlWindow. Get \_ AutoShow (metodo)</span><span class="sxs-lookup"><span data-stu-id="993b0-103">CBaseControlWindow.get\_AutoShow method</span></span>

<span data-ttu-id="993b0-104">Il `get_AutoShow` metodo recupera il flag di stato di Autoshow corrente.</span><span class="sxs-lookup"><span data-stu-id="993b0-104">The `get_AutoShow` method retrieves the current AutoShow state flag.</span></span>

## <a name="syntax"></a><span data-ttu-id="993b0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="993b0-105">Syntax</span></span>


```C++
HRESULT get_AutoShow(
   long *AutoShow
);
```



## <a name="parameters"></a><span data-ttu-id="993b0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="993b0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="993b0-107">*AutoShow*</span><span class="sxs-lookup"><span data-stu-id="993b0-107">*AutoShow*</span></span> 
</dt> <dd>

<span data-ttu-id="993b0-108">Puntatore a un flag booleano di automazione (0 è disattivato, 1 è on).</span><span class="sxs-lookup"><span data-stu-id="993b0-108">Pointer to an Automation Boolean flag (0 is off,  1 is on).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="993b0-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="993b0-109">Return value</span></span>

<span data-ttu-id="993b0-110">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="993b0-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="993b0-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="993b0-111">Remarks</span></span>

<span data-ttu-id="993b0-112">Questa funzione membro implementa il metodo [**IVideoWindow:: Get \_ AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-get_autoshow) .</span><span class="sxs-lookup"><span data-stu-id="993b0-112">This member function implements the [**IVideoWindow::get\_AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-get_autoshow) method.</span></span> <span data-ttu-id="993b0-113">Questa proprietà semplifica l'accesso alla visualizzazione delle finestre per le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="993b0-113">This property simplifies window display access for applications.</span></span> <span data-ttu-id="993b0-114">Se questa impostazione è impostata su 1 (on), la finestra, che in genere viene nascosta dopo la connessione del filtro, verrà visualizzata automaticamente quando il filtro viene sospeso o eseguito.</span><span class="sxs-lookup"><span data-stu-id="993b0-114">If this is set to  1 (on), the window, which is typically hidden after connection of the filter, will be displayed automatically when the filter pauses or runs.</span></span> <span data-ttu-id="993b0-115">Tuttavia, la finestra non deve essere nascosta quando il filtro si arresta.</span><span class="sxs-lookup"><span data-stu-id="993b0-115">The window should not be hidden when the filter stops, however.</span></span> <span data-ttu-id="993b0-116">Se questo parametro è impostato su 0 (disattivato), la finestra viene resa visibile solo quando l'applicazione chiama [**CBaseControlWindow::p UT \_ Visible**](cbasecontrolwindow-put-visible.md) o [**CBaseControlWindow::p UT \_ WindowState**](cbasecontrolwindow-put-windowstate.md) con i parametri appropriati.</span><span class="sxs-lookup"><span data-stu-id="993b0-116">If this parameter is set to 0 (off), the window is made visible only when the application calls [**CBaseControlWindow::put\_Visible**](cbasecontrolwindow-put-visible.md) or [**CBaseControlWindow::put\_WindowState**](cbasecontrolwindow-put-windowstate.md) with the appropriate parameters.</span></span>

<span data-ttu-id="993b0-117">Questa funzione membro deve essere chiamata da oggetti esterni tramite l'interfaccia [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) e pertanto blocca la sezione critica per la sincronizzazione con il filtro associato.</span><span class="sxs-lookup"><span data-stu-id="993b0-117">This member function is meant to be called by external objects through the [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) interface, and therefore locks the critical section to synchronize with the associated filter.</span></span> <span data-ttu-id="993b0-118">Chiamare la funzione membro [**CBaseControlWindow:: IsAutoShowEnabled**](cbasecontrolwindow-isautoshowenabled.md) per recuperare questa proprietà se non si chiama da un oggetto esterno.</span><span class="sxs-lookup"><span data-stu-id="993b0-118">Call the [**CBaseControlWindow::IsAutoShowEnabled**](cbasecontrolwindow-isautoshowenabled.md) member function to retrieve this property if you are not calling from an external object.</span></span>

## <a name="requirements"></a><span data-ttu-id="993b0-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="993b0-119">Requirements</span></span>



| <span data-ttu-id="993b0-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="993b0-120">Requirement</span></span> | <span data-ttu-id="993b0-121">Valore</span><span class="sxs-lookup"><span data-stu-id="993b0-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="993b0-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="993b0-122">Header</span></span><br/>  | <dl> <span data-ttu-id="993b0-123"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="993b0-123"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="993b0-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="993b0-124">Library</span></span><br/> | <dl> <span data-ttu-id="993b0-125"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="993b0-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="993b0-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="993b0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="993b0-127">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="993b0-127">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




