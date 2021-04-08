---
title: Apertura e chiusura di driver di dispositivo
description: Apertura e chiusura di driver di dispositivo
ms.assetid: 441bc0ec-41c9-4595-92f9-4c2304b10f16
keywords:
- MIDI (Musical Instrument Digital Interface), apertura di dispositivi
- MIDI (Musical Instrument Digital Interface), apertura di dispositivi
- Servizi MIDI, apertura di dispositivi
- apertura di dispositivi MIDI
- MIDI (Musical Instrument Digital Interface), chiusura di dispositivi
- MIDI (Musical Instrument Digital Interface), chiusura di dispositivi
- Servizi MIDI, chiusura di dispositivi
- chiusura di dispositivi MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53d7035455baa067b81af7da980a4ae043500c7b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725079"
---
# <a name="opening-and-closing-device-drivers"></a>Apertura e chiusura di driver di dispositivo

È necessario aprire un dispositivo MIDI prima di usarlo ed è necessario chiudere il dispositivo non appena si termina di usarlo. Windows fornisce le funzioni seguenti per aprire e chiudere tipi diversi di dispositivi MIDI.



| Valore                                | Significato                                            |
|--------------------------------------|----------------------------------------------------|
| [**midiInClose**](/windows/win32/api/mmeapi/nf-mmeapi-midiinclose)   | Chiude un dispositivo di input MIDI specificato.              |
| [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen)     | Apre un dispositivo di input MIDI specificato per la registrazione. |
| [**midiOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-midioutclose) | Chiude un dispositivo di output MIDI specificato.             |
| [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen)   | Apre un dispositivo di output MIDI per la riproduzione.           |



 

Ogni funzione che apre un dispositivo MIDI accetta come parametri un identificatore di dispositivo, un indirizzo di una posizione di memoria e alcuni parametri univoci per i dispositivi MIDI. La posizione di memoria viene riempita con un handle di dispositivo, che viene usato per identificare il dispositivo audio aperto nelle chiamate ad altre funzioni audio.

Molte funzioni MIDI possono accettare un handle di dispositivo o un identificatore di dispositivo. Sebbene sia possibile usare un handle di dispositivo ovunque venga usato un identificatore di dispositivo, non è sempre possibile usare un identificatore di dispositivo quando viene chiamato un handle per.

> [!Note]  
> I dispositivi MIDI non sono necessariamente condivisibili, pertanto è possibile che un determinato dispositivo non sia disponibile quando richiesto da un utente. In questo caso, l'applicazione deve notificare all'utente e consentire all'utente di provare ad aprire nuovamente il dispositivo.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Servizi MIDI](midi-services.md)
</dt> </dl>

 

 