---
title: Time-Based notifiche
description: Time-Based notifiche
ms.assetid: cf7bc0d4-f3bd-4416-b85f-0ff51a0efbbc
keywords:
- rossetti, notifiche
- rossetti, messaggi
- joystick, notifiche basate sul tempo
- notifiche di joystick basate sul tempo
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

È possibile inviare messaggi di joystick al sistema operativo a un'applicazione a intervalli di tempo regolari impostando il parametro *fChanged* di [**joySetCapture**](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture) su **FALSE** e specificando la lunghezza dell'intervallo tra i messaggi successivi. A tale scopo, assegnare *al parametro uPeriod* un valore compreso tra le frequenze di polling minimo e massimo per il joystick. È possibile determinare questo intervallo usando la funzione [**joyGetDevCaps,**](/windows/win32/api/joystickapi/nf-joystickapi-joygetdevcaps) che riempie i membri **wPeriodMin** e **wPeriodMax** nella [**struttura JOYCAPS.**](/windows/win32/api/joystickapi/ns-joystickapi-joycaps) Se il *valore uPeriod* non è compreso nell'intervallo di frequenze di polling valide per il joystick, il driver del joystick usa la frequenza di polling minima o massima, a seconda del valore *uPeriod.*

> [!Note]  
> Windows un evento timer con ogni chiamata a **joySetCapture**.

 

 

 