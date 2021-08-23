---
title: Event-Based notifiche
description: Event-Based notifiche
ms.assetid: bd483865-f983-416a-9b72-475fe9679cd1
keywords:
- rossetti, notifiche
- rossetti, messaggi
- joystick, notifiche basate su eventi
- rossetti, soglia di spostamento
- notifiche di joystick basate su eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b50e973434d5f5706c92a22f76846ada150bfc7caf3f5ba88c3f385f7eaf84e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119526181"
---
# <a name="event-based-notifications"></a>Event-Based notifiche

È possibile chiedere al sistema di inviare messaggi di joystick a un'applicazione ogni volta che la posizione di un asse del joystick cambia di un valore maggiore della soglia di *spostamento* del dispositivo. La soglia di spostamento è la distanza in cui il joystick deve essere spostato prima che un messaggio di modifica della posizione del joystick venga inviato a una finestra che ha acquisito il dispositivo. Per altre informazioni, vedere [**MM \_ JOY1MOVE**](mm-joy1move.md), [**MM \_ JOY1ZMOVE**](mm-joy1zmove.md), [**MM \_ JOY2MOVE**](mm-joy2move.md)o [**MM \_ JOY2ZMOVE**](mm-joy2zmove.md).

La soglia è inizialmente zero. È possibile impostare la soglia di spostamento usando la [**funzione joySetThreshold.**](/windows/win32/api/joystickapi/nf-joystickapi-joysetthreshold) È possibile recuperare la frequenza minima di polling del joystick usando la [**funzione joyGetDevCaps.**](/windows/win32/api/joystickapi/nf-joystickapi-joygetdevcaps)

 

 