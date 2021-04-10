---
title: Notifiche Time-Based
description: Notifiche Time-Based
ms.assetid: cf7bc0d4-f3bd-4416-b85f-0ff51a0efbbc
keywords:
- joystick, notifiche
- joystick, messaggi
- joystick, notifiche basate sul tempo
- notifiche del joystick basate sul tempo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15dff2a6140bd993157f20e92488afce1b646e20
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103956354"
---
# <a name="time-based-notifications"></a><span data-ttu-id="fd0ca-107">Notifiche Time-Based</span><span class="sxs-lookup"><span data-stu-id="fd0ca-107">Time-Based Notifications</span></span>

<span data-ttu-id="fd0ca-108">È possibile notificare al sistema operativo di inviare i messaggi del joystick a un'applicazione a intervalli di tempo regolari impostando il parametro *fChanged* di [**joySetCapture**](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture) su **false** e specificando la lunghezza dell'intervallo tra i messaggi successivi.</span><span class="sxs-lookup"><span data-stu-id="fd0ca-108">You can notify the operating system to send joystick messages to an application at regular time intervals by setting the *fChanged* parameter of [**joySetCapture**](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture) to **FALSE** and by specifying the interval length between successive messages.</span></span> <span data-ttu-id="fd0ca-109">A tale scopo, assegnare il parametro *uPeriod* a un valore compreso tra le frequenze di polling minime e massime per il joystick.</span><span class="sxs-lookup"><span data-stu-id="fd0ca-109">To do this, assign the *uPeriod* parameter a value between the minimum and maximum polling frequencies for the joystick.</span></span> <span data-ttu-id="fd0ca-110">È possibile determinare questo intervallo usando la funzione [**joyGetDevCaps**](/windows/win32/api/joystickapi/nf-joystickapi-joygetdevcaps) , che compila i membri **wPeriodMin** e **wPeriodMax** nella struttura [**JOYCAPS**](/windows/win32/api/joystickapi/ns-joystickapi-joycaps) .</span><span class="sxs-lookup"><span data-stu-id="fd0ca-110">You can determine this range by using the [**joyGetDevCaps**](/windows/win32/api/joystickapi/nf-joystickapi-joygetdevcaps) function, which fills the **wPeriodMin** and **wPeriodMax** members in the [**JOYCAPS**](/windows/win32/api/joystickapi/ns-joystickapi-joycaps) structure.</span></span> <span data-ttu-id="fd0ca-111">Se il valore *uPeriod* non è compreso nell'intervallo di frequenze di polling valide per il joystick, il driver del joystick usa la frequenza di polling minima o massima, a seconda di quale sia il valore più vicino al valore di *uPeriod* .</span><span class="sxs-lookup"><span data-stu-id="fd0ca-111">If the *uPeriod* value is outside the range of valid polling frequencies for the joystick, the joystick driver uses the minimum or maximum polling frequency, whichever is closer to the *uPeriod* value.</span></span>

> [!Note]  
> <span data-ttu-id="fd0ca-112">Windows imposta un evento timer con ogni chiamata a **joySetCapture**.</span><span class="sxs-lookup"><span data-stu-id="fd0ca-112">Windows sets up a timer event with each call to **joySetCapture**.</span></span>

 

 

 