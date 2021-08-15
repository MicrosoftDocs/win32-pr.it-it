---
title: Esecuzione di query su dispositivi MIDI
description: Esecuzione di query su dispositivi MIDI
ms.assetid: 0c9882a7-b5cb-41d1-a52e-003112225035
keywords:
- Instrument Digital Interface (MIDI), esecuzione di query sui dispositivi
- MIDI (Instrument Digital Interface), esecuzione di query sui dispositivi
- servizi MIDI, esecuzione di query sui dispositivi
- esecuzione di query su dispositivi MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3546971a17a5a8002f0e6d4205ceee5ca796babeb2b27df911cfca5a5911371c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118372316"
---
# <a name="querying-midi-devices"></a>Esecuzione di query su dispositivi MIDI

Prima di riprodurre o registrare i dati MIDI, è necessario determinare le funzionalità dell'hardware MIDI presente nel sistema. La funzionalità MIDI può variare da un computer multimediale a quello successivo. Le applicazioni non devono fare ipotesi sull'hardware presente in un determinato sistema.

Windows fornisce le funzioni seguenti per determinare il numero di dispositivi MIDI disponibili per l'input o l'output in un determinato sistema.



| Valore                                          | Significato                                                            |
|------------------------------------------------|--------------------------------------------------------------------|
| [**midiInGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-midiingetnumdevs)   | Recupera il numero di dispositivi di input MIDI presenti nel sistema.  |
| [**midiOutGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetnumdevs) | Recupera il numero di dispositivi di output MIDI presenti nel sistema. |



 

Analogamente ad altri dispositivi audio, i dispositivi MIDI sono identificati da un identificatore di dispositivo, che viene determinato in modo implicito dal numero di dispositivi presenti in un determinato sistema. Gli identificatori dei dispositivi vanno da zero al numero di dispositivi presenti, meno uno. Ad esempio, se in un sistema sono presenti due dispositivi di output MIDI, gli identificatori di dispositivo validi sono 0 e 1.

Dopo aver determinato il numero di dispositivi di input o output MIDI presenti in un sistema, è possibile ottenere informazioni sulle funzionalità di ogni dispositivo. Windows fornisce le funzioni seguenti per determinare le funzionalità dei dispositivi audio.



| Valore                                          | Significato                                                                                                                                   |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [**midiInGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-midiingetdevcaps)   | Recupera le funzionalità di un dispositivo di input MIDI specificato e inserisce queste informazioni nella [**struttura MIDIINCAPS.**](/windows/win32/api/mmeapi/ns-mmeapi-midiincaps)    |
| [**midiOutGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetdevcaps) | Recupera le funzionalità di un determinato dispositivo di output MIDI e inserisce queste informazioni nella [**struttura MIDIOUTCAPS.**](/windows/win32/api/mmeapi/ns-mmeapi-midioutcaps) |



 

Ognuna di queste funzioni ha un parametro che specifica l'indirizzo di una struttura che la funzione riempie con informazioni sulle funzionalità di un dispositivo specificato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Servizi MIDI](midi-services.md)
</dt> </dl>

 

 