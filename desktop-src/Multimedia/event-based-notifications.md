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
# <a name="event-based-notifications"></a>Notifiche Event-Based

È possibile richiedere al sistema di inviare i messaggi del joystick a un'applicazione ogni volta che la posizione di un asse del joystick viene modificata in base a un valore maggiore della *soglia di spostamento* del dispositivo. La soglia di spostamento corrisponde alla distanza con cui è necessario spostare il joystick prima che un messaggio di modifica della posizione del joystick venga inviato a una finestra che ha acquisito il dispositivo. Per altre informazioni, vedere [**mm \_ JOY1MOVE**](mm-joy1move.md), [**mm \_ JOY1ZMOVE**](mm-joy1zmove.md), [**mm \_ JOY2MOVE**](mm-joy2move.md)o [**mm \_ JOY2ZMOVE**](mm-joy2zmove.md).

La soglia è inizialmente zero. È possibile impostare la soglia di spostamento usando la funzione [**joySetThreshold**](/windows/win32/api/joystickapi/nf-joystickapi-joysetthreshold) . È possibile recuperare la frequenza di polling minima del joystick usando la funzione [**joyGetDevCaps**](/windows/win32/api/joystickapi/nf-joystickapi-joygetdevcaps) .

 

 