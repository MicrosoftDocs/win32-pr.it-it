---
title: Funzionalità di Joystick
description: Funzionalità di Joystick
ms.assetid: 910c7f1d-e20a-4a03-b512-9a7f8cb1e559
keywords:
- input multimediale, rossetti
- joystick, spostamento a due assi
- joystick, movimento a tre assi
- tasti di scelta, pulsanti
- joystick, intervalli di movimento
- joystick, frequenze di polling
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 311109468485a8174d9567516e747ef786019cc105c378ee91b55fa2f123c5cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118140449"
---
# <a name="joystick-capabilities"></a>Funzionalità di Joystick

I tasti di scelta possono supportare lo spostamento a due o tre assi e fino a quattro pulsanti. I joystick supportano anche diversi *intervalli di frequenze di* *movimento e polling.* L'intervallo di movimento è la distanza che una maniglia del joystick può spostare dalla posizione di riposo alla posizione più lontana dalla posizione di riposo. La frequenza di polling è l'intervallo di tempo tra le query del joystick.

I driver di joystick possono supportare uno o due rossetti. È possibile determinare il numero di joystick supportati da un driver di joystick usando la [**funzione joyGetNumDevs.**](/windows/win32/api/joystickapi/nf-joystickapi-joygetnumdevs) Questa funzione restituisce un intero senza segno che contiene il numero di tasti supportati oppure zero se non è disponibile alcun supporto per il joystick. Il valore restituito non indica il numero di joystick collegati al sistema.

È possibile determinare se un joystick è collegato al sistema usando la [**funzione joyGetPos.**](/windows/win32/api/joystickapi/nf-joystickapi-joygetpos) Questa funzione restituisce JOYERR \_ NOERROR se il dispositivo specificato è collegato. In caso contrario, restituisce JOYERR \_ UNPLUGGED.

Ogni joystick ha diverse funzionalità disponibili per l'applicazione. È possibile recuperare le funzionalità di un joystick usando la [**funzione joyGetDevCaps.**](/windows/win32/api/joystickapi/nf-joystickapi-joygetdevcaps) Questa funzione riempie una struttura [**JOYCAPS**](/windows/win32/api/joystickapi/ns-joystickapi-joycaps) con funzionalità quali i valori minimo e massimo per il sistema di coordinate, il numero di pulsanti sul joystick e le frequenze di polling minimo e massimo.

 

 