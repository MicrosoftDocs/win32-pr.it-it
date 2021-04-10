---
title: Messaggio MM_JOY1BUTTONUP (mmsystem. h)
description: Il \_ messaggio mm JOY1BUTTONUP notifica alla finestra che ha acquisito il joystick JOYSTICKID1 che un pulsante è stato rilasciato.
ms.assetid: 37f0f87a-4805-4cec-9c0c-9d6b36a3ff0d
keywords:
- MM_JOY1BUTTONUP messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MM_JOY1BUTTONUP
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 007a5d954b9b879f87c5e8ffe2d0774d0d1d85a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121667"
---
# <a name="mm_joy1buttonup-message"></a><span data-ttu-id="aa60e-104">\_Messaggio JOY1BUTTONUP mm</span><span class="sxs-lookup"><span data-stu-id="aa60e-104">MM\_JOY1BUTTONUP message</span></span>

<span data-ttu-id="aa60e-105">Il messaggio **mm \_ JOY1BUTTONUP** notifica alla finestra che ha acquisito il joystick JOYSTICKID1 che un pulsante è stato rilasciato.</span><span class="sxs-lookup"><span data-stu-id="aa60e-105">The **MM\_JOY1BUTTONUP** message notifies the window that has captured joystick JOYSTICKID1 that a button has been released.</span></span>


```C++
MM_JOY1BUTTONUP 
fwButtons = wParam; 
xPos = LOWORD(lParam); 
yPos = HIWORD(lParam); 
```



## <a name="parameters"></a><span data-ttu-id="aa60e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="aa60e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa60e-107"><span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*fwButtons*</span><span class="sxs-lookup"><span data-stu-id="aa60e-107"><span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*fwButtons*</span></span>
</dt> <dd>

<span data-ttu-id="aa60e-108">Identifica il pulsante che ha modificato lo stato e i pulsanti premuti.</span><span class="sxs-lookup"><span data-stu-id="aa60e-108">Identifies the button that has changed state and the buttons that are pressed.</span></span> <span data-ttu-id="aa60e-109">I possibili valori sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="aa60e-109">It can be one of the following:</span></span>



| <span data-ttu-id="aa60e-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa60e-110">Requirement</span></span> | <span data-ttu-id="aa60e-111">Valore</span><span class="sxs-lookup"><span data-stu-id="aa60e-111">Value</span></span> |
|-----------------|-------------------------------------------|
| <span data-ttu-id="aa60e-112">GIOIA \_ BUTTON1CHG</span><span class="sxs-lookup"><span data-stu-id="aa60e-112">JOY\_BUTTON1CHG</span></span> | <span data-ttu-id="aa60e-113">Il primo pulsante del joystick è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="aa60e-113">First joystick button has changed state.</span></span>  |
| <span data-ttu-id="aa60e-114">GIOIA \_ BUTTON2CHG</span><span class="sxs-lookup"><span data-stu-id="aa60e-114">JOY\_BUTTON2CHG</span></span> | <span data-ttu-id="aa60e-115">Il secondo pulsante del joystick è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="aa60e-115">Second joystick button has changed state.</span></span> |
| <span data-ttu-id="aa60e-116">GIOIA \_ BUTTON3CHG</span><span class="sxs-lookup"><span data-stu-id="aa60e-116">JOY\_BUTTON3CHG</span></span> | <span data-ttu-id="aa60e-117">Il terzo pulsante del joystick è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="aa60e-117">Third joystick button has changed state.</span></span>  |
| <span data-ttu-id="aa60e-118">GIOIA \_ BUTTON4CHG</span><span class="sxs-lookup"><span data-stu-id="aa60e-118">JOY\_BUTTON4CHG</span></span> | <span data-ttu-id="aa60e-119">Il quarto pulsante del joystick è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="aa60e-119">Fourth joystick button has changed state.</span></span> |



 

<span data-ttu-id="aa60e-120">e uno o più degli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="aa60e-120">and one or more of the following:</span></span>



| <span data-ttu-id="aa60e-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa60e-121">Requirement</span></span> | <span data-ttu-id="aa60e-122">Valore</span><span class="sxs-lookup"><span data-stu-id="aa60e-122">Value</span></span> |
|--------------|------------------------------------|
| <span data-ttu-id="aa60e-123">GIOIA \_ Button1</span><span class="sxs-lookup"><span data-stu-id="aa60e-123">JOY\_BUTTON1</span></span> | <span data-ttu-id="aa60e-124">Viene premuto il primo pulsante del joystick.</span><span class="sxs-lookup"><span data-stu-id="aa60e-124">First joystick button is pressed.</span></span>  |
| <span data-ttu-id="aa60e-125">GIOIA \_ Button2</span><span class="sxs-lookup"><span data-stu-id="aa60e-125">JOY\_BUTTON2</span></span> | <span data-ttu-id="aa60e-126">Viene premuto il secondo pulsante del joystick.</span><span class="sxs-lookup"><span data-stu-id="aa60e-126">Second joystick button is pressed.</span></span> |
| <span data-ttu-id="aa60e-127">GIOIA \_ Button3</span><span class="sxs-lookup"><span data-stu-id="aa60e-127">JOY\_BUTTON3</span></span> | <span data-ttu-id="aa60e-128">Viene premuto il terzo pulsante del joystick.</span><span class="sxs-lookup"><span data-stu-id="aa60e-128">Third joystick button is pressed.</span></span>  |
| <span data-ttu-id="aa60e-129">GIOIA \_ BUTTON4</span><span class="sxs-lookup"><span data-stu-id="aa60e-129">JOY\_BUTTON4</span></span> | <span data-ttu-id="aa60e-130">Viene premuto il quarto pulsante del joystick.</span><span class="sxs-lookup"><span data-stu-id="aa60e-130">Fourth joystick button is pressed.</span></span> |



 

</dd> <dt>

<span data-ttu-id="aa60e-131"><span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*</span><span class="sxs-lookup"><span data-stu-id="aa60e-131"><span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*</span></span>
</dt> <dd>

<span data-ttu-id="aa60e-132">Coordinate x del joystick rispetto all'angolo superiore sinistro dell'area client.</span><span class="sxs-lookup"><span data-stu-id="aa60e-132">The x-coordinates of the joystick relative to the upper left corner of the client area.</span></span>

</dd> <dt>

<span data-ttu-id="aa60e-133"><span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*yPos*</span><span class="sxs-lookup"><span data-stu-id="aa60e-133"><span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*yPos*</span></span>
</dt> <dd>

<span data-ttu-id="aa60e-134">Coordinata y del joystick rispetto all'angolo superiore sinistro dell'area client.</span><span class="sxs-lookup"><span data-stu-id="aa60e-134">The y-coordinate of the joystick relative to the upper left corner of the client area.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="aa60e-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aa60e-135">Requirements</span></span>



| <span data-ttu-id="aa60e-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa60e-136">Requirement</span></span> | <span data-ttu-id="aa60e-137">Valore</span><span class="sxs-lookup"><span data-stu-id="aa60e-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa60e-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aa60e-138">Minimum supported client</span></span><br/> | <span data-ttu-id="aa60e-139">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="aa60e-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="aa60e-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aa60e-140">Minimum supported server</span></span><br/> | <span data-ttu-id="aa60e-141">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="aa60e-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="aa60e-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="aa60e-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa60e-143"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="aa60e-143"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa60e-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aa60e-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa60e-145">Joystick</span><span class="sxs-lookup"><span data-stu-id="aa60e-145">Joysticks</span></span>](joysticks.md)
</dt> <dt>

[<span data-ttu-id="aa60e-146">Messaggi di joystick multimediali</span><span class="sxs-lookup"><span data-stu-id="aa60e-146">Multimedia Joystick Messages</span></span>](multimedia-joystick-messages.md)
</dt> </dl>

 

 





