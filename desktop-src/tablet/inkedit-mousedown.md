---
description: Si verifica quando l'utente preme un pulsante del mouse mentre il mouse si trova sul controllo InkEdit.
ms.assetid: 8985fee5-7b63-46ab-b229-046e2f0ee004
title: Evento InkEdit. MouseDown (inchiostrata. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78e684fe2d75e5eaaf2b0064e8c7c78cbfe281a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884941"
---
# <a name="inkeditmousedown-event"></a><span data-ttu-id="f9101-103">Evento InkEdit. MouseDown</span><span class="sxs-lookup"><span data-stu-id="f9101-103">InkEdit.MouseDown event</span></span>

<span data-ttu-id="f9101-104">Si verifica quando l'utente preme un pulsante del mouse mentre il mouse si trova sul controllo [InkEdit](inkedit-control-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="f9101-104">Occurs when the user presses a mouse button while the mouse is over the [InkEdit](inkedit-control-reference.md) control.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9101-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f9101-105">Syntax</span></span>


```C++
HRESULT MouseDown(
   short Button,
   short ShiftKey,
   long  xMouse,
   long  yMouse
);
```



## <a name="parameters"></a><span data-ttu-id="f9101-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f9101-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9101-107">*Button*</span><span class="sxs-lookup"><span data-stu-id="f9101-107">*Button*</span></span> 
</dt> <dd>

<span data-ttu-id="f9101-108">Membro dell'enumerazione [**MouseButton**](/windows/desktop/api/inked/ne-inked-mousebutton) che indica quali pulsanti del mouse sono stati premuti.</span><span class="sxs-lookup"><span data-stu-id="f9101-108">A member of the [**MouseButton**](/windows/desktop/api/inked/ne-inked-mousebutton) enumeration that indicates which mouse buttons were pressed.</span></span>



| <span data-ttu-id="f9101-109">Valore</span><span class="sxs-lookup"><span data-stu-id="f9101-109">Value</span></span>                                                                                                                                                            | <span data-ttu-id="f9101-110">Significato</span><span class="sxs-lookup"><span data-stu-id="f9101-110">Meaning</span></span>                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <span id="NO_BUTTON_"></span><span id="no_button_"></span><dl> <span data-ttu-id="f9101-111"><dt>**No \_ PULSANTE**</dt></span><span class="sxs-lookup"><span data-stu-id="f9101-111"><dt>**NO\_BUTTON** </dt></span></span> </dl>             | <span data-ttu-id="f9101-112">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="f9101-112">Default.</span></span> <span data-ttu-id="f9101-113">Non è stato premuto alcun pulsante del mouse.</span><span class="sxs-lookup"><span data-stu-id="f9101-113">No mouse button was pressed.</span></span> <br/> |
| <span id="LEFT_BUTTON_"></span><span id="left_button_"></span><dl> <span data-ttu-id="f9101-114"><dt>A **sinistra \_ PULSANTE**</dt></span><span class="sxs-lookup"><span data-stu-id="f9101-114"><dt>**LEFT\_BUTTON** </dt></span></span> </dl>       | <span data-ttu-id="f9101-115">È stato premuto il pulsante sinistro del mouse.</span><span class="sxs-lookup"><span data-stu-id="f9101-115">The left mouse button was pressed.</span></span> <br/>    |
| <span id="RIGHT_BUTTON_"></span><span id="right_button_"></span><dl> <span data-ttu-id="f9101-116"><dt>A **destra \_ PULSANTE**</dt></span><span class="sxs-lookup"><span data-stu-id="f9101-116"><dt>**RIGHT\_BUTTON** </dt></span></span> </dl>    | <span data-ttu-id="f9101-117">È stato premuto il pulsante destro del mouse.</span><span class="sxs-lookup"><span data-stu-id="f9101-117">The right mouse button was pressed.</span></span> <br/>   |
| <span id="MIDDLE_BUTTON_"></span><span id="middle_button_"></span><dl> <span data-ttu-id="f9101-118"><dt>Al **centro \_ PULSANTE**</dt></span><span class="sxs-lookup"><span data-stu-id="f9101-118"><dt>**MIDDLE\_BUTTON** </dt></span></span> </dl> | <span data-ttu-id="f9101-119">È stato premuto il pulsante centrale del mouse.</span><span class="sxs-lookup"><span data-stu-id="f9101-119">The middle mouse button was pressed.</span></span> <br/>  |



 

</dd> <dt>

<span data-ttu-id="f9101-120">*ShiftKey*</span><span class="sxs-lookup"><span data-stu-id="f9101-120">*ShiftKey*</span></span> 
</dt> <dd>

<span data-ttu-id="f9101-121">Membro dell'enumerazione [**InkShiftKeyModifierFlags**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags) che indica i tasti di modifica che vengono depressi al momento dell'evento.</span><span class="sxs-lookup"><span data-stu-id="f9101-121">A member of the [**InkShiftKeyModifierFlags**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags) enumeration that indicates which modifier keys are depressed at the time of the event.</span></span>



| <span data-ttu-id="f9101-122">Valore</span><span class="sxs-lookup"><span data-stu-id="f9101-122">Value</span></span>                                                                                                                                                                                     | <span data-ttu-id="f9101-123">Significato</span><span class="sxs-lookup"><span data-stu-id="f9101-123">Meaning</span></span>                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="IKM_Shift"></span><span id="ikm_shift"></span><span id="IKM_SHIFT"></span><dl> <span data-ttu-id="f9101-124"><dt>**IKM \_ Shift**</dt></span><span class="sxs-lookup"><span data-stu-id="f9101-124"><dt>**IKM\_Shift**</dt></span></span> </dl>             | <span data-ttu-id="f9101-125">Specifica che il tasto MAIUSC è stato utilizzato come modificatore.</span><span class="sxs-lookup"><span data-stu-id="f9101-125">Specifies that the SHIFT key was used as a modifier.</span></span> <br/> |
| <span id="IKM_Control_"></span><span id="ikm_control_"></span><span id="IKM_CONTROL_"></span><dl> <span data-ttu-id="f9101-126"><dt>**IKM \_ Controllo** di</dt></span><span class="sxs-lookup"><span data-stu-id="f9101-126"><dt>**IKM\_Control** </dt></span></span> </dl> | <span data-ttu-id="f9101-127">Specifica che il tasto CTRL è stato utilizzato come modificatore.</span><span class="sxs-lookup"><span data-stu-id="f9101-127">Specifies that the CTRL key was used as a modifier.</span></span> <br/>  |
| <span id="IKM_Alt_"></span><span id="ikm_alt_"></span><span id="IKM_ALT_"></span><dl> <span data-ttu-id="f9101-128"><dt>**IKM \_ Alt**</dt></span><span class="sxs-lookup"><span data-stu-id="f9101-128"><dt>**IKM\_Alt** </dt></span></span> </dl>                 | <span data-ttu-id="f9101-129">Specifica che il tasto ALT è stato utilizzato come modificatore.</span><span class="sxs-lookup"><span data-stu-id="f9101-129">Specifies that the ALT key was used as a modifier.</span></span> <br/>   |



 

</dd> <dt>

<span data-ttu-id="f9101-130">*xMouse*</span><span class="sxs-lookup"><span data-stu-id="f9101-130">*xMouse*</span></span> 
</dt> <dd>

<span data-ttu-id="f9101-131">Coordinata x corrente, in pixel, del puntatore del mouse.</span><span class="sxs-lookup"><span data-stu-id="f9101-131">The current x coordinate, in pixels, of the mouse pointer.</span></span>

</dd> <dt>

<span data-ttu-id="f9101-132">*yMouse*</span><span class="sxs-lookup"><span data-stu-id="f9101-132">*yMouse*</span></span> 
</dt> <dd>

<span data-ttu-id="f9101-133">Coordinata y corrente, in pixel, del puntatore del mouse.</span><span class="sxs-lookup"><span data-stu-id="f9101-133">The current y coordinate, in pixels, of the mouse pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9101-134">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f9101-134">Return value</span></span>

<span data-ttu-id="f9101-135">Se l'evento ha esito positivo, viene restituito **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="f9101-135">If this event succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f9101-136">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f9101-136">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9101-137">Commenti</span><span class="sxs-lookup"><span data-stu-id="f9101-137">Remarks</span></span>

<span data-ttu-id="f9101-138">Se viene premuto un pulsante del mouse mentre il puntatore è posizionato su un controllo [InkEdit](inkedit-control-reference.md) , il controllo acquisisce il mouse e riceve tutti gli eventi del mouse fino a includere l'ultimo evento [**MouseUp**](inkedit-mouseup.md) .</span><span class="sxs-lookup"><span data-stu-id="f9101-138">If a mouse button is pressed while the pointer is over an [InkEdit](inkedit-control-reference.md) control, that control captures the mouse and receives all mouse events up to and including the last [**MouseUp**](inkedit-mouseup.md) event.</span></span> <span data-ttu-id="f9101-139">Ciò implica che le coordinate del puntatore del mouse (x, y) restituite da un evento del mouse potrebbero non trovarsi sempre nell'area interna dell'oggetto che li riceve.</span><span class="sxs-lookup"><span data-stu-id="f9101-139">This implies that the (x, y) mouse-pointer coordinates returned by a mouse event may not always be in the internal area of the object that receives them.</span></span>

<span data-ttu-id="f9101-140">Se i pulsanti del mouse vengono premuti in successione, l'oggetto che acquisisce il mouse dopo la prima pressione riceve tutti gli eventi del mouse fino a quando non vengono rilasciati tutti i pulsanti.</span><span class="sxs-lookup"><span data-stu-id="f9101-140">If mouse buttons are pressed in succession, the object that captures the mouse after the first press receives all mouse events until all buttons are released.</span></span>

<span data-ttu-id="f9101-141">Questo metodo di evento è definito nell'interfaccia **\_ IInkEditEvents** .</span><span class="sxs-lookup"><span data-stu-id="f9101-141">This event method is defined in the **\_IInkEditEvents** interface.</span></span> <span data-ttu-id="f9101-142">L'interfaccia **\_ IInkEditEvents** implementa l'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificatore di DISPID \_ IeeMouseDown.</span><span class="sxs-lookup"><span data-stu-id="f9101-142">The **\_IInkEditEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IeeMouseDown.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9101-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f9101-143">Requirements</span></span>



| <span data-ttu-id="f9101-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9101-144">Requirement</span></span> | <span data-ttu-id="f9101-145">Valore</span><span class="sxs-lookup"><span data-stu-id="f9101-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9101-146">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f9101-146">Minimum supported client</span></span><br/> | <span data-ttu-id="f9101-147">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="f9101-147">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f9101-148">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f9101-148">Minimum supported server</span></span><br/> | <span data-ttu-id="f9101-149">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="f9101-149">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="f9101-150">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f9101-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9101-151"><dt>Inchiostrato. h (richiede anche il \_ . c)</dt></span><span class="sxs-lookup"><span data-stu-id="f9101-151"><dt>Inked.h (also requires inked\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="f9101-152">Libreria</span><span class="sxs-lookup"><span data-stu-id="f9101-152">Library</span></span><br/>                  | <dl> <span data-ttu-id="f9101-153"><dt>InkEd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9101-153"><dt>InkEd.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="f9101-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f9101-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9101-155">InkEdit</span><span class="sxs-lookup"><span data-stu-id="f9101-155">InkEdit</span></span>](inkedit-control-reference.md)
</dt> <dt>

[<span data-ttu-id="f9101-156">**Enumerazione InkMouseButton**</span><span class="sxs-lookup"><span data-stu-id="f9101-156">**InkMouseButton Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[<span data-ttu-id="f9101-157">**Enumerazione InkShiftKeyModifierFlags**</span><span class="sxs-lookup"><span data-stu-id="f9101-157">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> <dt>

<span data-ttu-id="f9101-158">[**\[Controllo InkEdit evento MouseMove\]**](inkedit-mousemove.md)</span><span class="sxs-lookup"><span data-stu-id="f9101-158">[**MouseMove Event \[InkEdit Control\]**](inkedit-mousemove.md)</span></span>
</dt> <dt>

<span data-ttu-id="f9101-159">[**\[Controllo InkEdit evento MouseUp\]**](inkedit-mouseup.md)</span><span class="sxs-lookup"><span data-stu-id="f9101-159">[**MouseUp Event \[InkEdit Control\]**](inkedit-mouseup.md)</span></span>
</dt> </dl>

 

