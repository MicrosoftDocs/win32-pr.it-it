---
title: Messaggio MM_JOY1MOVE (mmsystem. h)
description: Il \_ messaggio mm JOY1MOVE notifica alla finestra che ha acquisito il joystick JOYSTICKID1 che la posizione del joystick è cambiata.
ms.assetid: 317ac0b2-f873-413d-b071-47d840229643
keywords:
- MM_JOY1MOVE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MM_JOY1MOVE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a78753bd55f6682b3ac3f1514356d93cb455d162
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301077"
---
# <a name="mm_joy1move-message"></a><span data-ttu-id="91d92-104">\_Messaggio JOY1MOVE mm</span><span class="sxs-lookup"><span data-stu-id="91d92-104">MM\_JOY1MOVE message</span></span>

<span data-ttu-id="91d92-105">Il messaggio **mm \_ JOY1MOVE** notifica alla finestra che ha acquisito il joystick JOYSTICKID1 che la posizione del joystick è cambiata.</span><span class="sxs-lookup"><span data-stu-id="91d92-105">The **MM\_JOY1MOVE** message notifies the window that has captured joystick JOYSTICKID1 that the joystick position has changed.</span></span>


```C++
MM_JOY1MOVE 
fwButtons = wParam; 
xPos = LOWORD(lParam); 
yPos = HIWORD(lParam); 
```



## <a name="parameters"></a><span data-ttu-id="91d92-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="91d92-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91d92-107"><span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*fwButtons*</span><span class="sxs-lookup"><span data-stu-id="91d92-107"><span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*fwButtons*</span></span>
</dt> <dd>

<span data-ttu-id="91d92-108">Identifica i pulsanti che vengono premuti.</span><span class="sxs-lookup"><span data-stu-id="91d92-108">Identifies the buttons that are pressed.</span></span> <span data-ttu-id="91d92-109">Può essere uno o più dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="91d92-109">It can be one or more of the following values:</span></span>



| <span data-ttu-id="91d92-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="91d92-110">Requirement</span></span> | <span data-ttu-id="91d92-111">Valore</span><span class="sxs-lookup"><span data-stu-id="91d92-111">Value</span></span> |
|--------------|------------------------------------|
| <span data-ttu-id="91d92-112">GIOIA \_ Button1</span><span class="sxs-lookup"><span data-stu-id="91d92-112">JOY\_BUTTON1</span></span> | <span data-ttu-id="91d92-113">Viene premuto il primo pulsante del joystick.</span><span class="sxs-lookup"><span data-stu-id="91d92-113">First joystick button is pressed.</span></span>  |
| <span data-ttu-id="91d92-114">GIOIA \_ Button2</span><span class="sxs-lookup"><span data-stu-id="91d92-114">JOY\_BUTTON2</span></span> | <span data-ttu-id="91d92-115">Viene premuto il secondo pulsante del joystick.</span><span class="sxs-lookup"><span data-stu-id="91d92-115">Second joystick button is pressed.</span></span> |
| <span data-ttu-id="91d92-116">GIOIA \_ Button3</span><span class="sxs-lookup"><span data-stu-id="91d92-116">JOY\_BUTTON3</span></span> | <span data-ttu-id="91d92-117">Viene premuto il terzo pulsante del joystick.</span><span class="sxs-lookup"><span data-stu-id="91d92-117">Third joystick button is pressed.</span></span>  |
| <span data-ttu-id="91d92-118">GIOIA \_ BUTTON4</span><span class="sxs-lookup"><span data-stu-id="91d92-118">JOY\_BUTTON4</span></span> | <span data-ttu-id="91d92-119">Viene premuto il quarto pulsante del joystick.</span><span class="sxs-lookup"><span data-stu-id="91d92-119">Fourth joystick button is pressed.</span></span> |



 

</dd> <dt>

<span data-ttu-id="91d92-120"><span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*</span><span class="sxs-lookup"><span data-stu-id="91d92-120"><span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*</span></span>
</dt> <dd>

<span data-ttu-id="91d92-121">Coordinate x del joystick rispetto all'angolo superiore sinistro dell'area client.</span><span class="sxs-lookup"><span data-stu-id="91d92-121">The x-coordinates of the joystick relative to the upper left corner of the client area.</span></span>

</dd> <dt>

<span data-ttu-id="91d92-122"><span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*yPos*</span><span class="sxs-lookup"><span data-stu-id="91d92-122"><span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*yPos*</span></span>
</dt> <dd>

<span data-ttu-id="91d92-123">Coordinata y del joystick rispetto all'angolo superiore sinistro dell'area client.</span><span class="sxs-lookup"><span data-stu-id="91d92-123">The y-coordinate of the joystick relative to the upper left corner of the client area.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="91d92-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="91d92-124">Requirements</span></span>



| <span data-ttu-id="91d92-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="91d92-125">Requirement</span></span> | <span data-ttu-id="91d92-126">Valore</span><span class="sxs-lookup"><span data-stu-id="91d92-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91d92-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="91d92-127">Minimum supported client</span></span><br/> | <span data-ttu-id="91d92-128">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="91d92-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="91d92-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="91d92-129">Minimum supported server</span></span><br/> | <span data-ttu-id="91d92-130">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="91d92-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="91d92-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="91d92-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="91d92-132"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="91d92-132"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91d92-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="91d92-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91d92-134">Joystick</span><span class="sxs-lookup"><span data-stu-id="91d92-134">Joysticks</span></span>](joysticks.md)
</dt> <dt>

[<span data-ttu-id="91d92-135">Messaggi di joystick multimediali</span><span class="sxs-lookup"><span data-stu-id="91d92-135">Multimedia Joystick Messages</span></span>](multimedia-joystick-messages.md)
</dt> </dl>

 

 





