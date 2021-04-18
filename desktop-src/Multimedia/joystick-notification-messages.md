---
title: Messaggi di notifica del joystick
description: Messaggi di notifica del joystick
ms.assetid: 9e8ccc1b-85a9-44bf-b561-6ad4c10cddd1
keywords:
- joystick, notifiche
- joystick, messaggi
- joystick, posizione
- joystick, pulsanti
- Messaggi di MM_JOY1
- Messaggi di MM_JOY2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 698f999dab49ea6684e9184f6ed5c46286518b97
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297995"
---
# <a name="joystick-notification-messages"></a><span data-ttu-id="afe28-109">Messaggi di notifica del joystick</span><span class="sxs-lookup"><span data-stu-id="afe28-109">Joystick Notification Messages</span></span>

<span data-ttu-id="afe28-110">I messaggi del joystick notificano all'applicazione che un joystick è stato modificato o che uno dei pulsanti è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="afe28-110">Joystick messages notify your application that a joystick has changed position or that one of its buttons has changed states.</span></span> <span data-ttu-id="afe28-111">I messaggi che iniziano con MM \_ JOY1 vengono inviati alla funzione se l'applicazione richiede input dal joystick usando l'identificatore JOYSTICKID1 e i \_ messaggi mm JOY2 vengono inviati se l'applicazione richiede input dal joystick usando l'identificatore JOYSTICKID2.</span><span class="sxs-lookup"><span data-stu-id="afe28-111">Messages beginning with MM\_JOY1 are sent to the function if your application requests input from the joystick using the identifier JOYSTICKID1, and MM\_JOY2 messages are sent if your application requests input from the joystick using the identifier JOYSTICKID2.</span></span>

<span data-ttu-id="afe28-112">I messaggi nella tabella seguente identificano lo stato dei pulsanti del joystick:</span><span class="sxs-lookup"><span data-stu-id="afe28-112">The messages in the following table identify the status of the joystick buttons:</span></span>



| <span data-ttu-id="afe28-113">Message</span><span class="sxs-lookup"><span data-stu-id="afe28-113">Message</span></span>                                         | <span data-ttu-id="afe28-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="afe28-114">Description</span></span>                                                     |
|-------------------------------------------------|-----------------------------------------------------------------|
| [<span data-ttu-id="afe28-115">**\_JOY1BUTTONDOWN mm**</span><span class="sxs-lookup"><span data-stu-id="afe28-115">**MM\_JOY1BUTTONDOWN**</span></span>](mm-joy1buttondown.md) | <span data-ttu-id="afe28-116">È stato premuto un pulsante sul joystick JOYSTICKID1.</span><span class="sxs-lookup"><span data-stu-id="afe28-116">A button on joystick JOYSTICKID1 has been pressed.</span></span>              |
| [<span data-ttu-id="afe28-117">**\_JOY1BUTTONUP mm**</span><span class="sxs-lookup"><span data-stu-id="afe28-117">**MM\_JOY1BUTTONUP**</span></span>](mm-joy1buttonup.md)     | <span data-ttu-id="afe28-118">È stato rilasciato un pulsante sul joystick JOYSTICKID1.</span><span class="sxs-lookup"><span data-stu-id="afe28-118">A button on joystick JOYSTICKID1 has been released.</span></span>             |
| [<span data-ttu-id="afe28-119">**\_JOY1MOVE mm**</span><span class="sxs-lookup"><span data-stu-id="afe28-119">**MM\_JOY1MOVE**</span></span>](mm-joy1move.md)             | <span data-ttu-id="afe28-120">La posizione del JOYSTICKID1 del joystick è cambiata nella direzione x o y.</span><span class="sxs-lookup"><span data-stu-id="afe28-120">Joystick JOYSTICKID1 changed position in the x- or y-direction.</span></span> |
| [<span data-ttu-id="afe28-121">**\_JOY1ZMOVE mm**</span><span class="sxs-lookup"><span data-stu-id="afe28-121">**MM\_JOY1ZMOVE**</span></span>](mm-joy1zmove.md)           | <span data-ttu-id="afe28-122">La posizione del JOYSTICKID1 del joystick è cambiata nella direzione z.</span><span class="sxs-lookup"><span data-stu-id="afe28-122">Joystick JOYSTICKID1 changed position in the z-direction.</span></span>       |
| [<span data-ttu-id="afe28-123">**\_JOY2BUTTONDOWN mm**</span><span class="sxs-lookup"><span data-stu-id="afe28-123">**MM\_JOY2BUTTONDOWN**</span></span>](mm-joy2buttondown.md) | <span data-ttu-id="afe28-124">È stato premuto un pulsante sul joystick JOYSTICKID2.</span><span class="sxs-lookup"><span data-stu-id="afe28-124">A button on joystick JOYSTICKID2 has been pressed.</span></span>              |
| [<span data-ttu-id="afe28-125">**\_JOY2BUTTONUP mm**</span><span class="sxs-lookup"><span data-stu-id="afe28-125">**MM\_JOY2BUTTONUP**</span></span>](mm-joy2buttonup.md)     | <span data-ttu-id="afe28-126">È stato rilasciato un pulsante sul joystick JOYSTICKID2.</span><span class="sxs-lookup"><span data-stu-id="afe28-126">A button on joystick JOYSTICKID2 has been released.</span></span>             |
| [<span data-ttu-id="afe28-127">**\_JOY2MOVE mm**</span><span class="sxs-lookup"><span data-stu-id="afe28-127">**MM\_JOY2MOVE**</span></span>](mm-joy2move.md)             | <span data-ttu-id="afe28-128">La posizione del JOYSTICKID2 del joystick è cambiata nella direzione x o y</span><span class="sxs-lookup"><span data-stu-id="afe28-128">Joystick JOYSTICKID2 changed position in the x- or y-direction</span></span>  |
| [<span data-ttu-id="afe28-129">**\_JOY2ZMOVE mm**</span><span class="sxs-lookup"><span data-stu-id="afe28-129">**MM\_JOY2ZMOVE**</span></span>](mm-joy2zmove.md)           | <span data-ttu-id="afe28-130">La posizione del JOYSTICKID2 del joystick è cambiata nella direzione z.</span><span class="sxs-lookup"><span data-stu-id="afe28-130">Joystick JOYSTICKID2 changed position in the z-direction.</span></span>       |



 

<span data-ttu-id="afe28-131">Tutti i messaggi segnalano i pulsanti inesistenti come rilasciati.</span><span class="sxs-lookup"><span data-stu-id="afe28-131">All messages report nonexistent buttons as released.</span></span>

 

 




