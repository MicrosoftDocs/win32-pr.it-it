---
description: Il metodo PossiblyEatMessage trasmette i messaggi della tastiera e del mouse alla finestra di svuotamento del messaggio.
ms.assetid: 8e344c5d-2f94-454f-89b7-45c539b6e833
title: Metodo CBaseControlWindow. PossiblyEatMessage (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.PossiblyEatMessage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9bfadcfbbd6833d8f3e9b65bd39d0cdbef4a006e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327226"
---
# <a name="cbasecontrolwindowpossiblyeatmessage-method"></a><span data-ttu-id="efec6-103">CBaseControlWindow. PossiblyEatMessage, metodo</span><span class="sxs-lookup"><span data-stu-id="efec6-103">CBaseControlWindow.PossiblyEatMessage method</span></span>

<span data-ttu-id="efec6-104">Il `PossiblyEatMessage` metodo trasmette i messaggi della tastiera e del mouse alla finestra di svuotamento del messaggio.</span><span class="sxs-lookup"><span data-stu-id="efec6-104">The `PossiblyEatMessage` method forwards keyboard and mouse messages to the message-drain window.</span></span>

## <a name="syntax"></a><span data-ttu-id="efec6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="efec6-105">Syntax</span></span>


```C++
BOOL PossiblyEatMessage(
   UINT   uMsg,
   WPARAM wParam,
   LPARAM lParam
);
```



## <a name="parameters"></a><span data-ttu-id="efec6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="efec6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="efec6-107">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="efec6-107">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="efec6-108">Messaggio finestra.</span><span class="sxs-lookup"><span data-stu-id="efec6-108">Window message.</span></span>

</dd> <dt>

<span data-ttu-id="efec6-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="efec6-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="efec6-110">Primo parametro del messaggio.</span><span class="sxs-lookup"><span data-stu-id="efec6-110">First message parameter.</span></span>

</dd> <dt>

<span data-ttu-id="efec6-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="efec6-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="efec6-112">Secondo parametro del messaggio.</span><span class="sxs-lookup"><span data-stu-id="efec6-112">Second message parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="efec6-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="efec6-113">Return value</span></span>

<span data-ttu-id="efec6-114">Restituisce **true** se il messaggio è stato inviato alla finestra; in caso contrario, **false** .</span><span class="sxs-lookup"><span data-stu-id="efec6-114">Returns **TRUE** if the message was forwarded to the window, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="efec6-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="efec6-115">Remarks</span></span>

<span data-ttu-id="efec6-116">La finestra di svuotamento dei messaggi è una finestra progettata per ricevere determinati messaggi di mouse e tastiera.</span><span class="sxs-lookup"><span data-stu-id="efec6-116">The message-drain window is a window designated to receive certain mouse and keyboard messages.</span></span> <span data-ttu-id="efec6-117">Inizialmente la finestra è **null**; può essere impostata chiamando [**CBaseControlWindow::p UT \_ MessageDrain**](cbasecontrolwindow-put-messagedrain.md).</span><span class="sxs-lookup"><span data-stu-id="efec6-117">Initially the window is **NULL**; it can be set by calling [**CBaseControlWindow::put\_MessageDrain**](cbasecontrolwindow-put-messagedrain.md).</span></span>

<span data-ttu-id="efec6-118">Se la finestra di svuotamento dei messaggi è non **null**, `PossiblyEatMessage` inserisce i messaggi seguenti in tale finestra:</span><span class="sxs-lookup"><span data-stu-id="efec6-118">If the message-drain window is non-**NULL**, `PossiblyEatMessage` posts the following messages to that window:</span></span>

-   <span data-ttu-id="efec6-119">\_carattere WM</span><span class="sxs-lookup"><span data-stu-id="efec6-119">WM\_CHAR</span></span>
-   <span data-ttu-id="efec6-120">\_DEADCHAR WM</span><span class="sxs-lookup"><span data-stu-id="efec6-120">WM\_DEADCHAR</span></span>
-   <span data-ttu-id="efec6-121">KeyDown di WM \_</span><span class="sxs-lookup"><span data-stu-id="efec6-121">WM\_KEYDOWN</span></span>
-   <span data-ttu-id="efec6-122">KEYUP di WM \_</span><span class="sxs-lookup"><span data-stu-id="efec6-122">WM\_KEYUP</span></span>
-   <span data-ttu-id="efec6-123">\_LBUTTONDBLCLK WM</span><span class="sxs-lookup"><span data-stu-id="efec6-123">WM\_LBUTTONDBLCLK</span></span>
-   <span data-ttu-id="efec6-124">\_LBUTTONDOWN WM</span><span class="sxs-lookup"><span data-stu-id="efec6-124">WM\_LBUTTONDOWN</span></span>
-   <span data-ttu-id="efec6-125">\_LBUTTONUP WM</span><span class="sxs-lookup"><span data-stu-id="efec6-125">WM\_LBUTTONUP</span></span>
-   <span data-ttu-id="efec6-126">\_MBUTTONDBLCLK WM</span><span class="sxs-lookup"><span data-stu-id="efec6-126">WM\_MBUTTONDBLCLK</span></span>
-   <span data-ttu-id="efec6-127">\_MBUTTONDOWN WM</span><span class="sxs-lookup"><span data-stu-id="efec6-127">WM\_MBUTTONDOWN</span></span>
-   <span data-ttu-id="efec6-128">\_MBUTTONUP WM</span><span class="sxs-lookup"><span data-stu-id="efec6-128">WM\_MBUTTONUP</span></span>
-   <span data-ttu-id="efec6-129">\_MOUSEACTIVATE WM</span><span class="sxs-lookup"><span data-stu-id="efec6-129">WM\_MOUSEACTIVATE</span></span>
-   <span data-ttu-id="efec6-130">MOUSEMOVE di WM \_</span><span class="sxs-lookup"><span data-stu-id="efec6-130">WM\_MOUSEMOVE</span></span>
-   <span data-ttu-id="efec6-131">\_NCLBUTTONDBLCLK WM</span><span class="sxs-lookup"><span data-stu-id="efec6-131">WM\_NCLBUTTONDBLCLK</span></span>
-   <span data-ttu-id="efec6-132">\_NCLBUTTONDOWN WM</span><span class="sxs-lookup"><span data-stu-id="efec6-132">WM\_NCLBUTTONDOWN</span></span>
-   <span data-ttu-id="efec6-133">\_NCLBUTTONUP WM</span><span class="sxs-lookup"><span data-stu-id="efec6-133">WM\_NCLBUTTONUP</span></span>
-   <span data-ttu-id="efec6-134">\_NCMBUTTONDBLCLK WM</span><span class="sxs-lookup"><span data-stu-id="efec6-134">WM\_NCMBUTTONDBLCLK</span></span>
-   <span data-ttu-id="efec6-135">\_NCMBUTTONDOWN WM</span><span class="sxs-lookup"><span data-stu-id="efec6-135">WM\_NCMBUTTONDOWN</span></span>
-   <span data-ttu-id="efec6-136">\_NCMBUTTONUP WM</span><span class="sxs-lookup"><span data-stu-id="efec6-136">WM\_NCMBUTTONUP</span></span>
-   <span data-ttu-id="efec6-137">\_NCMOUSEMOVE WM</span><span class="sxs-lookup"><span data-stu-id="efec6-137">WM\_NCMOUSEMOVE</span></span>
-   <span data-ttu-id="efec6-138">\_NCRBUTTONDBLCLK WM</span><span class="sxs-lookup"><span data-stu-id="efec6-138">WM\_NCRBUTTONDBLCLK</span></span>
-   <span data-ttu-id="efec6-139">\_NCRBUTTONDOWN WM</span><span class="sxs-lookup"><span data-stu-id="efec6-139">WM\_NCRBUTTONDOWN</span></span>
-   <span data-ttu-id="efec6-140">\_NCRBUTTONUP WM</span><span class="sxs-lookup"><span data-stu-id="efec6-140">WM\_NCRBUTTONUP</span></span>
-   <span data-ttu-id="efec6-141">\_RBUTTONDBLCLK WM</span><span class="sxs-lookup"><span data-stu-id="efec6-141">WM\_RBUTTONDBLCLK</span></span>
-   <span data-ttu-id="efec6-142">\_RBUTTONDOWN WM</span><span class="sxs-lookup"><span data-stu-id="efec6-142">WM\_RBUTTONDOWN</span></span>
-   <span data-ttu-id="efec6-143">\_RBUTTONUP WM</span><span class="sxs-lookup"><span data-stu-id="efec6-143">WM\_RBUTTONUP</span></span>
-   <span data-ttu-id="efec6-144">\_SYSCHAR WM</span><span class="sxs-lookup"><span data-stu-id="efec6-144">WM\_SYSCHAR</span></span>
-   <span data-ttu-id="efec6-145">\_SYSDEADCHAR WM</span><span class="sxs-lookup"><span data-stu-id="efec6-145">WM\_SYSDEADCHAR</span></span>
-   <span data-ttu-id="efec6-146">\_SYSKEYDOWN WM</span><span class="sxs-lookup"><span data-stu-id="efec6-146">WM\_SYSKEYDOWN</span></span>
-   <span data-ttu-id="efec6-147">\_SYSKEYUP WM</span><span class="sxs-lookup"><span data-stu-id="efec6-147">WM\_SYSKEYUP</span></span>

<span data-ttu-id="efec6-148">Ignora gli altri messaggi.</span><span class="sxs-lookup"><span data-stu-id="efec6-148">It ignores other messages.</span></span> <span data-ttu-id="efec6-149">Se la finestra di svuotamento dei messaggi è **null**, il metodo ignorerà tutti i messaggi della finestra.</span><span class="sxs-lookup"><span data-stu-id="efec6-149">If the message-drain window is **NULL**, the method ignores all window messages.</span></span> <span data-ttu-id="efec6-150">Il metodo restituisce **true** se inserisce il messaggio o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="efec6-150">The method returns **TRUE** if it posts the message, or **FALSE** otherwise.</span></span> <span data-ttu-id="efec6-151">La classe **CBaseWindow** chiama questo metodo quando riceve un messaggio di finestra.</span><span class="sxs-lookup"><span data-stu-id="efec6-151">The **CBaseWindow** class calls this method when it receives a window message.</span></span>

## <a name="requirements"></a><span data-ttu-id="efec6-152">Requisiti</span><span class="sxs-lookup"><span data-stu-id="efec6-152">Requirements</span></span>



| <span data-ttu-id="efec6-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="efec6-153">Requirement</span></span> | <span data-ttu-id="efec6-154">Valore</span><span class="sxs-lookup"><span data-stu-id="efec6-154">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="efec6-155">Intestazione</span><span class="sxs-lookup"><span data-stu-id="efec6-155">Header</span></span><br/>  | <dl> <span data-ttu-id="efec6-156"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="efec6-156"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="efec6-157">Libreria</span><span class="sxs-lookup"><span data-stu-id="efec6-157">Library</span></span><br/> | <dl> <span data-ttu-id="efec6-158"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="efec6-158"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="efec6-159">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="efec6-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efec6-160">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="efec6-160">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




