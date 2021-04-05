---
title: Notifiche Event-Based
description: Notifiche Event-Based
ms.assetid: bd483865-f983-416a-9b72-475fe9679cd1
keywords:
- joystick, notifiche
- joystick, messaggi
- joystick, notifiche basate su eventi
- joystick, soglia di spostamento
- notifiche di joystick basate su eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1aa36809942593cdbe21b61af0d4f07f02b186a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725130"
---
# <a name="event-based-notifications"></a><span data-ttu-id="ebd0e-108">Notifiche Event-Based</span><span class="sxs-lookup"><span data-stu-id="ebd0e-108">Event-Based Notifications</span></span>

<span data-ttu-id="ebd0e-109">È possibile richiedere al sistema di inviare i messaggi del joystick a un'applicazione ogni volta che la posizione di un asse del joystick viene modificata in base a un valore maggiore della *soglia di spostamento* del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ebd0e-109">You can ask the system to send joystick messages to an application whenever the position of a joystick axis changes by a value greater than the *movement threshold* of the device.</span></span> <span data-ttu-id="ebd0e-110">La soglia di spostamento corrisponde alla distanza con cui è necessario spostare il joystick prima che un messaggio di modifica della posizione del joystick venga inviato a una finestra che ha acquisito il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ebd0e-110">The movement threshold is the distance the joystick must be moved before a joystick position change message is sent to a window that has captured the device.</span></span> <span data-ttu-id="ebd0e-111">Per altre informazioni, vedere [**mm \_ JOY1MOVE**](mm-joy1move.md), [**mm \_ JOY1ZMOVE**](mm-joy1zmove.md), [**mm \_ JOY2MOVE**](mm-joy2move.md)o [**mm \_ JOY2ZMOVE**](mm-joy2zmove.md).</span><span class="sxs-lookup"><span data-stu-id="ebd0e-111">For more information, see [**MM\_JOY1MOVE**](mm-joy1move.md), [**MM\_JOY1ZMOVE**](mm-joy1zmove.md), [**MM\_JOY2MOVE**](mm-joy2move.md), or [**MM\_JOY2ZMOVE**](mm-joy2zmove.md).</span></span>

<span data-ttu-id="ebd0e-112">La soglia è inizialmente zero.</span><span class="sxs-lookup"><span data-stu-id="ebd0e-112">The threshold is initially zero.</span></span> <span data-ttu-id="ebd0e-113">È possibile impostare la soglia di spostamento usando la funzione [**joySetThreshold**](/windows/win32/api/joystickapi/nf-joystickapi-joysetthreshold) .</span><span class="sxs-lookup"><span data-stu-id="ebd0e-113">You can set the movement threshold by using the [**joySetThreshold**](/windows/win32/api/joystickapi/nf-joystickapi-joysetthreshold) function.</span></span> <span data-ttu-id="ebd0e-114">È possibile recuperare la frequenza di polling minima del joystick usando la funzione [**joyGetDevCaps**](/windows/win32/api/joystickapi/nf-joystickapi-joygetdevcaps) .</span><span class="sxs-lookup"><span data-stu-id="ebd0e-114">You can retrieve the minimum polling frequency of the joystick by using the [**joyGetDevCaps**](/windows/win32/api/joystickapi/nf-joystickapi-joygetdevcaps) function.</span></span>

 

 