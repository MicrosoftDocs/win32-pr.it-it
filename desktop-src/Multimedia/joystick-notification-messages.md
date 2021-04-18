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
# <a name="joystick-notification-messages"></a>Messaggi di notifica del joystick

I messaggi del joystick notificano all'applicazione che un joystick è stato modificato o che uno dei pulsanti è stato modificato. I messaggi che iniziano con MM \_ JOY1 vengono inviati alla funzione se l'applicazione richiede input dal joystick usando l'identificatore JOYSTICKID1 e i \_ messaggi mm JOY2 vengono inviati se l'applicazione richiede input dal joystick usando l'identificatore JOYSTICKID2.

I messaggi nella tabella seguente identificano lo stato dei pulsanti del joystick:



| Message                                         | Descrizione                                                     |
|-------------------------------------------------|-----------------------------------------------------------------|
| [**\_JOY1BUTTONDOWN mm**](mm-joy1buttondown.md) | È stato premuto un pulsante sul joystick JOYSTICKID1.              |
| [**\_JOY1BUTTONUP mm**](mm-joy1buttonup.md)     | È stato rilasciato un pulsante sul joystick JOYSTICKID1.             |
| [**\_JOY1MOVE mm**](mm-joy1move.md)             | La posizione del JOYSTICKID1 del joystick è cambiata nella direzione x o y. |
| [**\_JOY1ZMOVE mm**](mm-joy1zmove.md)           | La posizione del JOYSTICKID1 del joystick è cambiata nella direzione z.       |
| [**\_JOY2BUTTONDOWN mm**](mm-joy2buttondown.md) | È stato premuto un pulsante sul joystick JOYSTICKID2.              |
| [**\_JOY2BUTTONUP mm**](mm-joy2buttonup.md)     | È stato rilasciato un pulsante sul joystick JOYSTICKID2.             |
| [**\_JOY2MOVE mm**](mm-joy2move.md)             | La posizione del JOYSTICKID2 del joystick è cambiata nella direzione x o y  |
| [**\_JOY2ZMOVE mm**](mm-joy2zmove.md)           | La posizione del JOYSTICKID2 del joystick è cambiata nella direzione z.       |



 

Tutti i messaggi segnalano i pulsanti inesistenti come rilasciati.

 

 




