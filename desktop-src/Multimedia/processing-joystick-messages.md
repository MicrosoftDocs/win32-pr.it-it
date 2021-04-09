---
title: Elaborazione dei messaggi del joystick
description: Elaborazione dei messaggi del joystick
ms.assetid: d21a9d49-1fc0-4899-9083-87c3cf4e0e62
keywords:
- joystick, messaggi
- Messaggio MM_JOY1MOVE
- Messaggio MM_JOY1BUTTONDOWN
- Messaggio MM_JOY1BUTTONUP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f2337d392c0104dcb49839b19c5fb615481ee2a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044516"
---
# <a name="processing-joystick-messages"></a>Elaborazione dei messaggi del joystick

Nell'esempio seguente viene illustrato il modo in cui un'applicazione può rispondere ai movimenti e alle modifiche del joystick negli Stati dei pulsanti. Quando il joystick cambia posizione, l'applicazione sposta il cursore e, se è premuto uno dei pulsanti, disegna un punto elenco sul desktop. Quando viene premuto un pulsante del joystick, l'applicazione disegna un foro sul desktop e riproduce un suono continuamente fino a quando non viene rilasciato un pulsante. I messaggi da controllare sono [**mm \_ JOY1MOVE**](mm-joy1move.md), [**mm \_ JOY1BUTTONDOWN**](mm-joy1buttondown.md)e [**mm \_ JOY1BUTTONUP**](mm-joy1buttonup.md).


```C++
case MM_JOY1MOVE :                     // changed position 
    if((UINT) wParam & (JOY_BUTTON1 | JOY_BUTTON2)) 
        DrawFire(hWnd); 
    DrawSight(lParam);                 // calculates new cursor position 
    break; 
case MM_JOY1BUTTONDOWN :               // button is down 
    if((UINT) wParam & JOY_BUTTON1) 
    { 
        PlaySound(lpButton1, SND_LOOP | SND_ASYNC | SND_MEMORY); 
        DrawFire(hWnd); 
    } 
    else if((UINT) wParam & JOY_BUTTON2) 
    { 
        PlaySound(lpButton2, SND_ASYNC | SND_MEMORY |  SND_LOOP); 
        DrawFire(hWnd); 
    } 
    break; 
case MM_JOY1BUTTONUP :                 // button is up 
    sndPlaySound(NULL, 0);             // stops the sound 
    break; 

```



 

 




