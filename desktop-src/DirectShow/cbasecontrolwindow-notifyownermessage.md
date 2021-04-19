---
description: Il metodo NotifyOwnerMessage passa i messaggi specifici alla finestra del video.
ms.assetid: 8b27281a-5b8a-46c3-aa66-390d4496f30e
title: Metodo CBaseControlWindow. NotifyOwnerMessage (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.NotifyOwnerMessage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9073d37987404849ba8aa3acbda9919df840b410
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333613"
---
# <a name="cbasecontrolwindownotifyownermessage-method"></a><span data-ttu-id="0ad29-103">CBaseControlWindow. NotifyOwnerMessage, metodo</span><span class="sxs-lookup"><span data-stu-id="0ad29-103">CBaseControlWindow.NotifyOwnerMessage method</span></span>

<span data-ttu-id="0ad29-104">Il `NotifyOwnerMessage` metodo passa i messaggi specifici alla finestra del video.</span><span class="sxs-lookup"><span data-stu-id="0ad29-104">The `NotifyOwnerMessage` method passes along specific messages to the video window.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ad29-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0ad29-105">Syntax</span></span>


```C++
HRESULT NotifyOwnerMessage(
   long     hwnd,
   long     uMsg,
   LONG_PTR wParam,
   LONG_PTR lParam
);
```



## <a name="parameters"></a><span data-ttu-id="0ad29-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0ad29-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ad29-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="0ad29-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="0ad29-108">Handle per la finestra del video.</span><span class="sxs-lookup"><span data-stu-id="0ad29-108">Handle to the video window.</span></span>

</dd> <dt>

<span data-ttu-id="0ad29-109">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="0ad29-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="0ad29-110">Dettagli del messaggio.</span><span class="sxs-lookup"><span data-stu-id="0ad29-110">Message details.</span></span>

</dd> <dt>

<span data-ttu-id="0ad29-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0ad29-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0ad29-112">Primo parametro del messaggio.</span><span class="sxs-lookup"><span data-stu-id="0ad29-112">First message parameter.</span></span>

</dd> <dt>

<span data-ttu-id="0ad29-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0ad29-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0ad29-114">Secondo parametro del messaggio.</span><span class="sxs-lookup"><span data-stu-id="0ad29-114">Second message parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ad29-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0ad29-115">Return value</span></span>

<span data-ttu-id="0ad29-116">Non restituisce alcun \_ errore.</span><span class="sxs-lookup"><span data-stu-id="0ad29-116">Returns NO\_ERROR.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ad29-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="0ad29-117">Remarks</span></span>

<span data-ttu-id="0ad29-118">Quando la finestra video è un elemento figlio di un'altra finestra, non riceve alcuni messaggi della finestra di primo livello.</span><span class="sxs-lookup"><span data-stu-id="0ad29-118">When the video window is a child of another window, it does not receive certain top-level window messages.</span></span> <span data-ttu-id="0ad29-119">Questi messaggi possono essere utili per un renderer, perché potrebbero influire sul comportamento.</span><span class="sxs-lookup"><span data-stu-id="0ad29-119">These messages can be valuable to a renderer, because they could affect its behavior.</span></span> <span data-ttu-id="0ad29-120">`NotifyOwnerMessage` passa uno dei messaggi seguenti alla finestra del video.</span><span class="sxs-lookup"><span data-stu-id="0ad29-120">`NotifyOwnerMessage` passes any of the following messages to the video window.</span></span>

-   <span data-ttu-id="0ad29-121">\_ACTIVATEAPP WM</span><span class="sxs-lookup"><span data-stu-id="0ad29-121">WM\_ACTIVATEAPP</span></span>
-   <span data-ttu-id="0ad29-122">\_DEVMODECHANGE WM</span><span class="sxs-lookup"><span data-stu-id="0ad29-122">WM\_DEVMODECHANGE</span></span>
-   <span data-ttu-id="0ad29-123">\_DISPLAYCHANGE WM</span><span class="sxs-lookup"><span data-stu-id="0ad29-123">WM\_DISPLAYCHANGE</span></span>
-   <span data-ttu-id="0ad29-124">\_PALETTECHANGED WM</span><span class="sxs-lookup"><span data-stu-id="0ad29-124">WM\_PALETTECHANGED</span></span>
-   <span data-ttu-id="0ad29-125">\_PALETTEISCHANGING WM</span><span class="sxs-lookup"><span data-stu-id="0ad29-125">WM\_PALETTEISCHANGING</span></span>
-   <span data-ttu-id="0ad29-126">\_QUERYNEWPALETTE WM</span><span class="sxs-lookup"><span data-stu-id="0ad29-126">WM\_QUERYNEWPALETTE</span></span>
-   <span data-ttu-id="0ad29-127">\_SYSCOLORCHANGE WM</span><span class="sxs-lookup"><span data-stu-id="0ad29-127">WM\_SYSCOLORCHANGE</span></span>

<span data-ttu-id="0ad29-128">È possibile richiedere che il server di distribuzione plug-in [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) (PID) renda una finestra diventata un elemento figlio di un'altra finestra.</span><span class="sxs-lookup"><span data-stu-id="0ad29-128">You can request that the [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) plug-in distributor (PID) make a window become a child of another window.</span></span> <span data-ttu-id="0ad29-129">Quando si verifica questo problema, il PID cercherà determinati messaggi che potrebbero essere inviati alla finestra proprietaria.</span><span class="sxs-lookup"><span data-stu-id="0ad29-129">When this occurs, the PID will look for certain messages that might be sent to the owning window.</span></span> <span data-ttu-id="0ad29-130">Il PID li inoltrerà quindi alla finestra di proprietà.</span><span class="sxs-lookup"><span data-stu-id="0ad29-130">The PID will then forward those messages to the owned window.</span></span> <span data-ttu-id="0ad29-131">L'elaborazione predefinita per i messaggi consiste nell'inviarli in modo sincrono alla routine di proprietà della finestra chiamando la funzione **SendMessage** Win32.</span><span class="sxs-lookup"><span data-stu-id="0ad29-131">The default processing for the messages is to send them to the owned window procedure synchronously by calling the Win32 **SendMessage** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ad29-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0ad29-132">Requirements</span></span>



| <span data-ttu-id="0ad29-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ad29-133">Requirement</span></span> | <span data-ttu-id="0ad29-134">Valore</span><span class="sxs-lookup"><span data-stu-id="0ad29-134">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ad29-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0ad29-135">Header</span></span><br/>  | <dl> <span data-ttu-id="0ad29-136"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0ad29-136"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0ad29-137">Libreria</span><span class="sxs-lookup"><span data-stu-id="0ad29-137">Library</span></span><br/> | <dl> <span data-ttu-id="0ad29-138"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="0ad29-138"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ad29-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0ad29-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ad29-140">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="0ad29-140">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




