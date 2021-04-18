---
title: Messaggio MM_JOY2BUTTONDOWN (mmsystem. h)
description: Il \_ messaggio mm JOY2BUTTONDOWN notifica alla finestra che ha acquisito il joystick JOYSTICKID2 che è stato premuto un pulsante.
ms.assetid: b4cd48ea-91ad-48e9-b0ae-58d8ee124171
keywords:
- MM_JOY2BUTTONDOWN messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MM_JOY2BUTTONDOWN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f155fcdc21247e01fd5d730f3f7d4daaba705e65
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301076"
---
# <a name="mm_joy2buttondown-message"></a><span data-ttu-id="18a56-104">\_Messaggio JOY2BUTTONDOWN mm</span><span class="sxs-lookup"><span data-stu-id="18a56-104">MM\_JOY2BUTTONDOWN message</span></span>

<span data-ttu-id="18a56-105">Il messaggio **mm \_ JOY2BUTTONDOWN** notifica alla finestra che ha acquisito il joystick JOYSTICKID2 che è stato premuto un pulsante.</span><span class="sxs-lookup"><span data-stu-id="18a56-105">The **MM\_JOY2BUTTONDOWN** message notifies the window that has captured joystick JOYSTICKID2 that a button has been pressed.</span></span>


```C++
MM_JOY2BUTTONDOWN 
fwButtons = wParam; 
xPos = LOWORD(lParam); 
yPos = HIWORD(lParam); 
```



## <a name="parameters"></a><span data-ttu-id="18a56-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="18a56-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18a56-107"><span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*fwButtons*</span><span class="sxs-lookup"><span data-stu-id="18a56-107"><span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*fwButtons*</span></span>
</dt> <dd>

<span data-ttu-id="18a56-108">Identifica il pulsante che ha modificato lo stato e i pulsanti premuti.</span><span class="sxs-lookup"><span data-stu-id="18a56-108">Identifies the button that has changed state and the buttons that are pressed.</span></span> <span data-ttu-id="18a56-109">I possibili valori sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="18a56-109">It can be one of the following:</span></span>



| <span data-ttu-id="18a56-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="18a56-110">Requirement</span></span> | <span data-ttu-id="18a56-111">Valore</span><span class="sxs-lookup"><span data-stu-id="18a56-111">Value</span></span> |
|-----------------|-------------------------------------------|
| <span data-ttu-id="18a56-112">GIOIA \_ BUTTON1CHG</span><span class="sxs-lookup"><span data-stu-id="18a56-112">JOY\_BUTTON1CHG</span></span> | <span data-ttu-id="18a56-113">Il primo pulsante del joystick è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="18a56-113">First joystick button has changed state.</span></span>  |
| <span data-ttu-id="18a56-114">GIOIA \_ BUTTON2CHG</span><span class="sxs-lookup"><span data-stu-id="18a56-114">JOY\_BUTTON2CHG</span></span> | <span data-ttu-id="18a56-115">Il secondo pulsante del joystick è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="18a56-115">Second joystick button has changed state.</span></span> |
| <span data-ttu-id="18a56-116">GIOIA \_ BUTTON3CHG</span><span class="sxs-lookup"><span data-stu-id="18a56-116">JOY\_BUTTON3CHG</span></span> | <span data-ttu-id="18a56-117">Il terzo pulsante del joystick è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="18a56-117">Third joystick button has changed state.</span></span>  |
| <span data-ttu-id="18a56-118">GIOIA \_ BUTTON4CHG</span><span class="sxs-lookup"><span data-stu-id="18a56-118">JOY\_BUTTON4CHG</span></span> | <span data-ttu-id="18a56-119">Il quarto pulsante del joystick è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="18a56-119">Fourth joystick button has changed state.</span></span> |



 

<span data-ttu-id="18a56-120">e uno o più degli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="18a56-120">and one or more of the following:</span></span>



| <span data-ttu-id="18a56-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="18a56-121">Requirement</span></span> | <span data-ttu-id="18a56-122">Valore</span><span class="sxs-lookup"><span data-stu-id="18a56-122">Value</span></span> |
|--------------|------------------------------------|
| <span data-ttu-id="18a56-123">GIOIA \_ Button1</span><span class="sxs-lookup"><span data-stu-id="18a56-123">JOY\_BUTTON1</span></span> | <span data-ttu-id="18a56-124">Viene premuto il primo pulsante del joystick.</span><span class="sxs-lookup"><span data-stu-id="18a56-124">First joystick button is pressed.</span></span>  |
| <span data-ttu-id="18a56-125">GIOIA \_ Button2</span><span class="sxs-lookup"><span data-stu-id="18a56-125">JOY\_BUTTON2</span></span> | <span data-ttu-id="18a56-126">Viene premuto il secondo pulsante del joystick.</span><span class="sxs-lookup"><span data-stu-id="18a56-126">Second joystick button is pressed.</span></span> |
| <span data-ttu-id="18a56-127">GIOIA \_ Button3</span><span class="sxs-lookup"><span data-stu-id="18a56-127">JOY\_BUTTON3</span></span> | <span data-ttu-id="18a56-128">Viene premuto il terzo pulsante del joystick.</span><span class="sxs-lookup"><span data-stu-id="18a56-128">Third joystick button is pressed.</span></span>  |
| <span data-ttu-id="18a56-129">GIOIA \_ BUTTON4</span><span class="sxs-lookup"><span data-stu-id="18a56-129">JOY\_BUTTON4</span></span> | <span data-ttu-id="18a56-130">Viene premuto il quarto pulsante del joystick.</span><span class="sxs-lookup"><span data-stu-id="18a56-130">Fourth joystick button is pressed.</span></span> |



 

</dd> <dt>

<span data-ttu-id="18a56-131"><span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*</span><span class="sxs-lookup"><span data-stu-id="18a56-131"><span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*</span></span>
</dt> <dd>

<span data-ttu-id="18a56-132">Coordinate x del joystick rispetto all'angolo superiore sinistro dell'area client.</span><span class="sxs-lookup"><span data-stu-id="18a56-132">The x-coordinates of the joystick relative to the upper left corner of the client area.</span></span>

</dd> <dt>

<span data-ttu-id="18a56-133"><span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*yPos*</span><span class="sxs-lookup"><span data-stu-id="18a56-133"><span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*yPos*</span></span>
</dt> <dd>

<span data-ttu-id="18a56-134">Coordinata y del joystick rispetto all'angolo superiore sinistro dell'area client.</span><span class="sxs-lookup"><span data-stu-id="18a56-134">The y-coordinate of the joystick relative to the upper left corner of the client area.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="18a56-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="18a56-135">Requirements</span></span>



| <span data-ttu-id="18a56-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="18a56-136">Requirement</span></span> | <span data-ttu-id="18a56-137">Valore</span><span class="sxs-lookup"><span data-stu-id="18a56-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18a56-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="18a56-138">Minimum supported client</span></span><br/> | <span data-ttu-id="18a56-139">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="18a56-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="18a56-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="18a56-140">Minimum supported server</span></span><br/> | <span data-ttu-id="18a56-141">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="18a56-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="18a56-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="18a56-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="18a56-143"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="18a56-143"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18a56-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="18a56-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18a56-145">Joystick</span><span class="sxs-lookup"><span data-stu-id="18a56-145">Joysticks</span></span>](joysticks.md)
</dt> <dt>

[<span data-ttu-id="18a56-146">Messaggi di joystick multimediali</span><span class="sxs-lookup"><span data-stu-id="18a56-146">Multimedia Joystick Messages</span></span>](multimedia-joystick-messages.md)
</dt> </dl>

 

 





