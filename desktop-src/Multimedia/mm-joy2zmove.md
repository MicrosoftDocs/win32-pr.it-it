---
title: Messaggio MM_JOY2ZMOVE (mmsystem. h)
description: Il \_ messaggio mm JOY2ZMOVE notifica alla finestra che ha acquisito il joystick JOYSTICKID2 che la posizione del joystick sull'asse z è cambiata.
ms.assetid: f09a1a11-8c97-4a03-a388-8bf9ab89a3db
keywords:
- MM_JOY2ZMOVE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MM_JOY2ZMOVE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d899a4a1c93304075cb166ba805367ceed6ddd3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302772"
---
# <a name="mm_joy2zmove-message"></a><span data-ttu-id="9889c-104">\_Messaggio JOY2ZMOVE mm</span><span class="sxs-lookup"><span data-stu-id="9889c-104">MM\_JOY2ZMOVE message</span></span>

<span data-ttu-id="9889c-105">Il messaggio **mm \_ JOY2ZMOVE** notifica alla finestra che ha acquisito il joystick JOYSTICKID2 che la posizione del joystick sull'asse z è cambiata.</span><span class="sxs-lookup"><span data-stu-id="9889c-105">The **MM\_JOY2ZMOVE** message notifies the window that has captured joystick JOYSTICKID2 that the joystick position on the z-axis has changed.</span></span>


```C++
MM_JOY2ZMOVE 
fwButtons = wParam; 
zPos = LOWORD(lParam); 
```



## <a name="parameters"></a><span data-ttu-id="9889c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9889c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9889c-107"><span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*fwButtons*</span><span class="sxs-lookup"><span data-stu-id="9889c-107"><span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*fwButtons*</span></span>
</dt> <dd>

<span data-ttu-id="9889c-108">Identifica i pulsanti che vengono premuti.</span><span class="sxs-lookup"><span data-stu-id="9889c-108">Identifies the buttons that are pressed.</span></span> <span data-ttu-id="9889c-109">Può essere uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="9889c-109">It can be one or more of the following values.</span></span>



| <span data-ttu-id="9889c-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="9889c-110">Requirement</span></span> | <span data-ttu-id="9889c-111">Valore</span><span class="sxs-lookup"><span data-stu-id="9889c-111">Value</span></span> |
|--------------|------------------------------------|
| <span data-ttu-id="9889c-112">GIOIA \_ Button1</span><span class="sxs-lookup"><span data-stu-id="9889c-112">JOY\_BUTTON1</span></span> | <span data-ttu-id="9889c-113">Viene premuto il primo pulsante del joystick.</span><span class="sxs-lookup"><span data-stu-id="9889c-113">First joystick button is pressed.</span></span>  |
| <span data-ttu-id="9889c-114">GIOIA \_ Button2</span><span class="sxs-lookup"><span data-stu-id="9889c-114">JOY\_BUTTON2</span></span> | <span data-ttu-id="9889c-115">Viene premuto il secondo pulsante del joystick.</span><span class="sxs-lookup"><span data-stu-id="9889c-115">Second joystick button is pressed.</span></span> |
| <span data-ttu-id="9889c-116">GIOIA \_ Button3</span><span class="sxs-lookup"><span data-stu-id="9889c-116">JOY\_BUTTON3</span></span> | <span data-ttu-id="9889c-117">Viene premuto il terzo pulsante del joystick.</span><span class="sxs-lookup"><span data-stu-id="9889c-117">Third joystick button is pressed.</span></span>  |
| <span data-ttu-id="9889c-118">GIOIA \_ BUTTON4</span><span class="sxs-lookup"><span data-stu-id="9889c-118">JOY\_BUTTON4</span></span> | <span data-ttu-id="9889c-119">Viene premuto il quarto pulsante del joystick.</span><span class="sxs-lookup"><span data-stu-id="9889c-119">Fourth joystick button is pressed.</span></span> |



 

</dd> <dt>

<span data-ttu-id="9889c-120"><span id="zPos"></span><span id="zpos"></span><span id="ZPOS"></span>*zPos*</span><span class="sxs-lookup"><span data-stu-id="9889c-120"><span id="zPos"></span><span id="zpos"></span><span id="ZPOS"></span>*zPos*</span></span>
</dt> <dd>

<span data-ttu-id="9889c-121">Coordinata z del joystick.</span><span class="sxs-lookup"><span data-stu-id="9889c-121">The z-coordinate of the joystick.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9889c-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9889c-122">Requirements</span></span>



| <span data-ttu-id="9889c-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="9889c-123">Requirement</span></span> | <span data-ttu-id="9889c-124">Valore</span><span class="sxs-lookup"><span data-stu-id="9889c-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9889c-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9889c-125">Minimum supported client</span></span><br/> | <span data-ttu-id="9889c-126">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9889c-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="9889c-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9889c-127">Minimum supported server</span></span><br/> | <span data-ttu-id="9889c-128">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9889c-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="9889c-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9889c-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="9889c-130"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9889c-130"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9889c-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9889c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9889c-132">Joystick</span><span class="sxs-lookup"><span data-stu-id="9889c-132">Joysticks</span></span>](joysticks.md)
</dt> <dt>

[<span data-ttu-id="9889c-133">Messaggi di joystick multimediali</span><span class="sxs-lookup"><span data-stu-id="9889c-133">Multimedia Joystick Messages</span></span>](multimedia-joystick-messages.md)
</dt> </dl>

 

 





