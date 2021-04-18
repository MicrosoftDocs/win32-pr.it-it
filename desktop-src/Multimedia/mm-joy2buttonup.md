---
title: Messaggio MM_JOY2BUTTONUP (mmsystem. h)
description: Il \_ messaggio mm JOY2BUTTONUP notifica alla finestra che ha acquisito il joystick JOYSTICKID2 che un pulsante è stato rilasciato.
ms.assetid: da024466-7cd3-42ec-90a7-1468eb42841e
keywords:
- MM_JOY2BUTTONUP messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MM_JOY2BUTTONUP
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7a4f2d23739fc72a6898e2b53fc3e1c330687f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302774"
---
# <a name="mm_joy2buttonup-message"></a><span data-ttu-id="22434-104">\_Messaggio JOY2BUTTONUP mm</span><span class="sxs-lookup"><span data-stu-id="22434-104">MM\_JOY2BUTTONUP message</span></span>

<span data-ttu-id="22434-105">Il messaggio **mm \_ JOY2BUTTONUP** notifica alla finestra che ha acquisito il joystick JOYSTICKID2 che un pulsante è stato rilasciato.</span><span class="sxs-lookup"><span data-stu-id="22434-105">The **MM\_JOY2BUTTONUP** message notifies the window that has captured joystick JOYSTICKID2 that a button has been released.</span></span>


```C++
MM_JOY2BUTTONUP 
fwButton = wParam; 
xPos = LOWORD(lParam); 
yPos = HIWORD(lParam); 
```



## <a name="parameters"></a><span data-ttu-id="22434-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="22434-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22434-107">**fwButtons**</span><span class="sxs-lookup"><span data-stu-id="22434-107">**fwButtons**</span></span> 
</dt> <dd>

<span data-ttu-id="22434-108">Identifica il pulsante che ha modificato lo stato e i pulsanti premuti.</span><span class="sxs-lookup"><span data-stu-id="22434-108">Identifies the button that has changed state and the buttons that are pressed.</span></span> <span data-ttu-id="22434-109">I possibili valori sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="22434-109">It can be one of the following:</span></span>



| <span data-ttu-id="22434-110">Valore</span><span class="sxs-lookup"><span data-stu-id="22434-110">Value</span></span>                                                                                                                                                            | <span data-ttu-id="22434-111">Significato</span><span class="sxs-lookup"><span data-stu-id="22434-111">Meaning</span></span>                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span id="JOY_BUTTON1CHG"></span><span id="joy_button1chg"></span><dl> <span data-ttu-id="22434-112"><dt>**GIOIA \_ BUTTON1CHG**</dt></span><span class="sxs-lookup"><span data-stu-id="22434-112"><dt>**JOY\_BUTTON1CHG**</dt></span></span> </dl> | <span data-ttu-id="22434-113">Il primo pulsante del joystick è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="22434-113">First joystick button has changed state.</span></span><br/>  |
| <span id="JOY_BUTTON2CHG"></span><span id="joy_button2chg"></span><dl> <span data-ttu-id="22434-114"><dt>**GIOIA \_ BUTTON2CHG**</dt></span><span class="sxs-lookup"><span data-stu-id="22434-114"><dt>**JOY\_BUTTON2CHG**</dt></span></span> </dl> | <span data-ttu-id="22434-115">Il secondo pulsante del joystick è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="22434-115">Second joystick button has changed state.</span></span><br/> |
| <span id="JOY_BUTTON3CHG"></span><span id="joy_button3chg"></span><dl> <span data-ttu-id="22434-116"><dt>**GIOIA \_ BUTTON3CHG**</dt></span><span class="sxs-lookup"><span data-stu-id="22434-116"><dt>**JOY\_BUTTON3CHG**</dt></span></span> </dl> | <span data-ttu-id="22434-117">Il terzo pulsante del joystick è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="22434-117">Third joystick button has changed state.</span></span><br/>  |
| <span id="JOY_BUTTON4CHG"></span><span id="joy_button4chg"></span><dl> <span data-ttu-id="22434-118"><dt>**GIOIA \_ BUTTON4CHG**</dt></span><span class="sxs-lookup"><span data-stu-id="22434-118"><dt>**JOY\_BUTTON4CHG**</dt></span></span> </dl> | <span data-ttu-id="22434-119">Il quarto pulsante del joystick è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="22434-119">Fourth joystick button has changed state.</span></span><br/> |



 

<span data-ttu-id="22434-120">e uno o più degli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="22434-120">and one or more of the following:</span></span>



| <span data-ttu-id="22434-121">Valore</span><span class="sxs-lookup"><span data-stu-id="22434-121">Value</span></span>                                                                                                                                                   | <span data-ttu-id="22434-122">Significato</span><span class="sxs-lookup"><span data-stu-id="22434-122">Meaning</span></span>                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="JOY_BUTTON1"></span><span id="joy_button1"></span><dl> <span data-ttu-id="22434-123"><dt>**GIOIA \_ Button1**</dt></span><span class="sxs-lookup"><span data-stu-id="22434-123"><dt>**JOY\_BUTTON1**</dt></span></span> </dl> | <span data-ttu-id="22434-124">Viene premuto il primo pulsante del joystick.</span><span class="sxs-lookup"><span data-stu-id="22434-124">First joystick button is pressed.</span></span><br/>  |
| <span id="JOY_BUTTON2"></span><span id="joy_button2"></span><dl> <span data-ttu-id="22434-125"><dt>**GIOIA \_ Button2**</dt></span><span class="sxs-lookup"><span data-stu-id="22434-125"><dt>**JOY\_BUTTON2**</dt></span></span> </dl> | <span data-ttu-id="22434-126">Viene premuto il secondo pulsante del joystick.</span><span class="sxs-lookup"><span data-stu-id="22434-126">Second joystick button is pressed.</span></span><br/> |
| <span id="JOY_BUTTON3"></span><span id="joy_button3"></span><dl> <span data-ttu-id="22434-127"><dt>**GIOIA \_ Button3**</dt></span><span class="sxs-lookup"><span data-stu-id="22434-127"><dt>**JOY\_BUTTON3**</dt></span></span> </dl> | <span data-ttu-id="22434-128">Viene premuto il terzo pulsante del joystick.</span><span class="sxs-lookup"><span data-stu-id="22434-128">Third joystick button is pressed.</span></span><br/>  |
| <span id="JOY_BUTTON4"></span><span id="joy_button4"></span><dl> <span data-ttu-id="22434-129"><dt>**GIOIA \_ BUTTON4**</dt></span><span class="sxs-lookup"><span data-stu-id="22434-129"><dt>**JOY\_BUTTON4**</dt></span></span> </dl> | <span data-ttu-id="22434-130">Viene premuto il quarto pulsante del joystick.</span><span class="sxs-lookup"><span data-stu-id="22434-130">Fourth joystick button is pressed.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="22434-131">**xPos**</span><span class="sxs-lookup"><span data-stu-id="22434-131">**xPos**</span></span> 
</dt> <dd>

<span data-ttu-id="22434-132">Coordinate x del joystick rispetto all'angolo superiore sinistro dell'area client.</span><span class="sxs-lookup"><span data-stu-id="22434-132">The x-coordinates of the joystick relative to the upper left corner of the client area.</span></span>

</dd> <dt>

<span data-ttu-id="22434-133">**yPos**</span><span class="sxs-lookup"><span data-stu-id="22434-133">**yPos**</span></span> 
</dt> <dd>

<span data-ttu-id="22434-134">Coordinata y del joystick rispetto all'angolo superiore sinistro dell'area client.</span><span class="sxs-lookup"><span data-stu-id="22434-134">The y-coordinate of the joystick relative to the upper left corner of the client area.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="22434-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="22434-135">Requirements</span></span>



| <span data-ttu-id="22434-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="22434-136">Requirement</span></span> | <span data-ttu-id="22434-137">Valore</span><span class="sxs-lookup"><span data-stu-id="22434-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22434-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="22434-138">Minimum supported client</span></span><br/> | <span data-ttu-id="22434-139">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="22434-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="22434-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="22434-140">Minimum supported server</span></span><br/> | <span data-ttu-id="22434-141">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="22434-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="22434-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="22434-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="22434-143"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="22434-143"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22434-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="22434-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22434-145">Joystick</span><span class="sxs-lookup"><span data-stu-id="22434-145">Joysticks</span></span>](joysticks.md)
</dt> <dt>

[<span data-ttu-id="22434-146">Messaggi di joystick multimediali</span><span class="sxs-lookup"><span data-stu-id="22434-146">Multimedia Joystick Messages</span></span>](multimedia-joystick-messages.md)
</dt> </dl>

 

 





