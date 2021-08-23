---
title: Apertura e chiusura di driver di dispositivo
description: Apertura e chiusura di driver di dispositivo
ms.assetid: 441bc0ec-41c9-4595-92f9-4c2304b10f16
keywords:
- Instrument Digital Interface (MIDI), apertura di dispositivi
- MIDI (Instrument Digital Interface), apertura di dispositivi
- servizi MIDI, apertura di dispositivi
- apertura di dispositivi MIDI
- Instrument Digital Interface (MIDI), dispositivi di chiusura
- MIDI (Instrument Digital Interface), dispositivi di chiusura
- servizi MIDI, chiusura di dispositivi
- chiusura di dispositivi MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e935ab3d0d420e735bed6e01d08c80962e134338ea9e88eaa4899e0e81cb71f3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119806291"
---
# <a name="opening-and-closing-device-drivers"></a>Apertura e chiusura di driver di dispositivo

È necessario aprire un dispositivo MIDI prima di usarlo e chiudere il dispositivo non appena lo si termina di usarlo. Windows fornisce le funzioni seguenti per aprire e chiudere diversi tipi di dispositivi MIDI.



| Valore                                | Significato                                            |
|--------------------------------------|----------------------------------------------------|
| [**midiInClose**](/windows/win32/api/mmeapi/nf-mmeapi-midiinclose)   | Chiude un dispositivo di input MIDI specificato.              |
| [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen)     | Apre un dispositivo di input MIDI specificato per la registrazione. |
| [**midiOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-midioutclose) | Chiude un dispositivo di output MIDI specificato.             |
| [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen)   | Apre un dispositivo di output MIDI per la riproduzione.           |



 

Ogni funzione che apre un dispositivo MIDI accetta come parametri un identificatore di dispositivo, un indirizzo di una posizione di memoria e alcuni parametri univoci per i dispositivi MIDI. La posizione della memoria viene riempita con un handle di dispositivo, che viene usato per identificare il dispositivo audio aperto nelle chiamate ad altre funzioni audio.

Molte funzioni MIDI possono accettare un handle di dispositivo o un identificatore di dispositivo. Sebbene sia possibile usare un handle di dispositivo ovunque si usi un identificatore di dispositivo, non è sempre possibile usare un identificatore di dispositivo quando viene chiamato un handle.

> [!Note]  
> I dispositivi MIDI non sono necessariamente condivisione, quindi un particolare dispositivo potrebbe non essere disponibile quando un utente lo richiede. In questo caso, l'applicazione deve inviare una notifica all'utente e consentire all'utente di provare ad aprire nuovamente il dispositivo.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Servizi MIDI](midi-services.md)
</dt> </dl>

 

 