---
title: Time-Based notifiche
description: Time-Based notifiche
ms.assetid: cf7bc0d4-f3bd-4416-b85f-0ff51a0efbbc
keywords:
- stick, notifiche
- sticks, messages
- stick, notifiche basate sul tempo
- notifiche basate sul tempo a levetta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80052d5e728a7a5b00e6177a36c30f470fe80daeafbe39a12aa4c9a883766534
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688251"
---
# <a name="time-based-notifications"></a>Time-Based notifiche

È possibile notificare al sistema operativo di inviare messaggi a un'applicazione a intervalli di tempo regolari impostando il parametro *fChanged* di [**heartbeatSetCapture**](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture) su **FALSE** e specificando la lunghezza dell'intervallo tra i messaggi successivi. A tale scopo, assegnare *al parametro uPeriod* un valore compreso tra le frequenze di polling minima e massima per ilstick. È possibile determinare questo intervallo usando la [**funzionemineGetDevCaps,**](/windows/win32/api/joystickapi/nf-joystickapi-joygetdevcaps) che riempie i membri **wPeriodMin** e **wPeriodMax** nella [**strutturaMINECAPS.**](/windows/win32/api/joystickapi/ns-joystickapi-joycaps) Se il *valore uPeriod* non è compreso nell'intervallo di frequenze di polling valide per il levetta, il driver del levetta usa la frequenza di polling minima o massima, a seconda del valore *di uPeriod.*

> [!Note]  
> Windows configura un evento timer con ogni chiamata a **timerSetCapture.**

 

 

 