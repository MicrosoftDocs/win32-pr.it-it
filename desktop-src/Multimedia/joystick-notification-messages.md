---
title: Messaggi di notifica del rossetto
description: Messaggi di notifica del rossetto
ms.assetid: 9e8ccc1b-85a9-44bf-b561-6ad4c10cddd1
keywords:
- rossetti, notifiche
- rossetti, messaggi
- rossetti, posizione
- tasti di scelta, pulsanti
- MM_JOY1 messaggi
- MM_JOY2 messaggi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27113adeb6f9fd4444f8fc30431df0eab686db667fa2674e81d7f5d4e568be64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118140341"
---
# <a name="joystick-notification-messages"></a>Messaggi di notifica del rossetto

I messaggi di joystick notificano all'applicazione che un joystick ha cambiato posizione o che uno dei relativi pulsanti ha modificato gli stati. I messaggi che iniziano con MM JOY1 vengono inviati alla funzione se l'applicazione richiede l'input dal joystick usando l'identificatore JOYSTICKID1 e i messaggi MM JOY2 vengono inviati se l'applicazione richiede l'input dal joystick usando l'identificatore \_ \_ JOYSTICKID2.

I messaggi nella tabella seguente identificano lo stato dei pulsanti del joystick:



| Message                                         | Descrizione                                                     |
|-------------------------------------------------|-----------------------------------------------------------------|
| [**MM \_ JOY1BUTTONDOWN**](mm-joy1buttondown.md) | È stato premuto un pulsante in joystick JOYSTICKID1.              |
| [**MM \_ JOY1BUTTONUP**](mm-joy1buttonup.md)     | È stato rilasciato un pulsante in joystick JOYSTICKID1.             |
| [**MM \_ JOY1MOVE**](mm-joy1move.md)             | Joystick JOYSTICKID1 ha modificato la posizione nella direzione x o y. |
| [**MM \_ JOY1ZMOVE**](mm-joy1zmove.md)           | Il joystick JOYSTICKID1 ha modificato la posizione nella direzione z.       |
| [**MM \_ JOY2BUTTONDOWN**](mm-joy2buttondown.md) | È stato premuto un pulsante in joystick JOYSTICKID2.              |
| [**MM \_ JOY2BUTTONUP**](mm-joy2buttonup.md)     | È stato rilasciato un pulsante in joystick JOYSTICKID2.             |
| [**MM \_ JOY2MOVE**](mm-joy2move.md)             | La posizione di Joystick JOYSTICKID2 è stata modificata nella direzione x o y  |
| [**MM \_ JOY2ZMOVE**](mm-joy2zmove.md)           | Joystick JOYSTICKID2 ha modificato la posizione nella direzione z.       |



 

Tutti i messaggi segnalano pulsanti inesistenti come rilasciati.

 

 




