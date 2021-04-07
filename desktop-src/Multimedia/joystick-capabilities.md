---
title: Funzionalità del joystick
description: Funzionalità del joystick
ms.assetid: 910c7f1d-e20a-4a03-b512-9a7f8cb1e559
keywords:
- input multimediale, joystick
- joystick, spostamento a due assi
- joystick, spostamento a tre assi
- joystick, pulsanti
- joystick, intervalli di movimento
- joystick, frequenze di polling
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b317d5a0c8deb48b49224fd051ecb7ce5a0bbced
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726719"
---
# <a name="joystick-capabilities"></a>Funzionalità del joystick

I joystick possono supportare un movimento di due o tre assi e un massimo di quattro pulsanti. I joystick supportano anche *intervalli diversi di frequenze di movimento e di* *polling*. L'intervallo di movimento è la distanza in base alla quale un handle di joystick può spostarsi dalla posizione di riposo alla posizione più lontana dalla posizione di riposo. La frequenza di polling è l'intervallo di tempo tra le query del joystick.

I driver del joystick possono supportare uno o due joystick. È possibile determinare il numero di joystick supportati da un driver del joystick usando la funzione [**joyGetNumDevs**](/windows/win32/api/joystickapi/nf-joystickapi-joygetnumdevs) . Questa funzione restituisce un Unsigned Integer che contiene il numero di joystick supportati o zero se non è disponibile alcun supporto per il joystick. Il valore restituito non indica il numero di joystick collegati al sistema.

È possibile determinare se un joystick è collegato al sistema tramite la funzione [**joyGetPos**](/windows/win32/api/joystickapi/nf-joystickapi-joygetpos) . Questa funzione restituisce JOYERR \_ NOERROR se il dispositivo specificato è collegato. In caso contrario, restituisce JOYERR \_ scollegato.

Ogni joystick dispone di diverse funzionalità disponibili per l'applicazione. È possibile recuperare le funzionalità di un joystick usando la funzione [**joyGetDevCaps**](/windows/win32/api/joystickapi/nf-joystickapi-joygetdevcaps) . Questa funzione riempie una struttura [**JOYCAPS**](/windows/win32/api/joystickapi/ns-joystickapi-joycaps) con funzionalità di joystick quali i valori minimo e massimo per il sistema di coordinate, il numero di pulsanti sul joystick e le frequenze di polling minime e massime.

 

 