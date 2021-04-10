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
# <a name="time-based-notifications"></a>Notifiche Time-Based

È possibile notificare al sistema operativo di inviare i messaggi del joystick a un'applicazione a intervalli di tempo regolari impostando il parametro *fChanged* di [**joySetCapture**](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture) su **false** e specificando la lunghezza dell'intervallo tra i messaggi successivi. A tale scopo, assegnare il parametro *uPeriod* a un valore compreso tra le frequenze di polling minime e massime per il joystick. È possibile determinare questo intervallo usando la funzione [**joyGetDevCaps**](/windows/win32/api/joystickapi/nf-joystickapi-joygetdevcaps) , che compila i membri **wPeriodMin** e **wPeriodMax** nella struttura [**JOYCAPS**](/windows/win32/api/joystickapi/ns-joystickapi-joycaps) . Se il valore *uPeriod* non è compreso nell'intervallo di frequenze di polling valide per il joystick, il driver del joystick usa la frequenza di polling minima o massima, a seconda di quale sia il valore più vicino al valore di *uPeriod* .

> [!Note]  
> Windows imposta un evento timer con ogni chiamata a **joySetCapture**.

 

 

 