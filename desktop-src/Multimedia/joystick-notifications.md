---
title: Notifiche del joystick
description: Notifiche del joystick
ms.assetid: 523dfae3-bbd5-4955-96f3-1710e29d003f
keywords:
- joystick, notifiche
- joystick, messaggi
- joystick acquisiti
- joystick scollegati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2791f8da14107d50afe90d8efbdbfe79acba3093
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046704"
---
# <a name="joystick-notifications"></a>Notifiche del joystick

È possibile acquisire i messaggi Direct joystick da inviare a una funzione tramite la funzione [**joySetCapture**](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture) . Una sola applicazione alla volta può acquisire messaggi da un joystick, ma è possibile eseguire query sul joystick da un'altra applicazione usando la funzione [**joyGetPos**](/windows/win32/api/joystickapi/nf-joystickapi-joygetpos) o [**joyGetPosEx**](/windows/win32/api/joystickapi/nf-joystickapi-joygetposex) .

> [!Note]  
> Un messaggio di joystick può non riuscire a raggiungere l'applicazione che ha acquisito il joystick se una seconda applicazione usa **joyGetPos** o **joyGetPosEx** per eseguire una query sul joystick approssimativamente nello stesso momento in cui viene inviato il messaggio. In questo caso, la seconda applicazione potrebbe intercettare il messaggio.

 

Se si desidera acquisire messaggi da due joystick collegati al sistema, usare due volte [**joySetCapture**](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture) , una volta per ogni joystick. La finestra riceve messaggi distinti e distinti per ogni dispositivo.

È possibile rilasciare un joystick acquisito usando la funzione [**joyReleaseCapture**](/windows/win32/api/joystickapi/nf-joystickapi-joyreleasecapture) . Se un'applicazione non rilascia il joystick prima di terminare, il joystick viene rilasciato automaticamente poco dopo la distruzione della finestra di acquisizione.

Non è possibile acquisire un joystick scollegato. La funzione **joySetCapture** restituisce JOYERR \_ scollegata se il dispositivo specificato viene scollegato.

 

 