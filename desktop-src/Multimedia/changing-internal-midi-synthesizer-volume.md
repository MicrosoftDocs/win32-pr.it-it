---
title: Modifica del volume interno del sintetizzatore MIDI
description: Modifica del volume interno del sintetizzatore MIDI
ms.assetid: 75ab7ff5-f394-4a79-8dcc-f4eef434a36e
keywords:
- MidI (Musical Instrument Digital Interface), sintetizzatori interni
- MIDI (Musical Instrument Digital Interface), sintetizzatori interni
- riproduzione di file MIDI, sintetizzatori interni
- sintetizzatori MIDI interni
- MIDI (Musical Instrument Digital Interface), modifica del volume
- MIDI (Musical Instrument Digital Interface), modifica del volume
- riproduzione di file MIDI, modifica del volume
- modifica del volume MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 646c7e17a7e8c0a6902e26dd8bbfdf8eb89c39297fdacdf062749d8c47a3d487
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119808211"
---
# <a name="changing-internal-midi-synthesizer-volume"></a>Modifica del volume interno del sintetizzatore MIDI

Windows fornisce le funzioni seguenti per recuperare e impostare il livello di volume dei dispositivi di sintetizzatori MIDI interni:



| Valore                                        | Significato                                                                       |
|----------------------------------------------|-------------------------------------------------------------------------------|
| [**midiOutGetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetvolume) | Recupera il livello di volume del dispositivo sintetizzatore MIDI interno specificato. |
| [**midiOutSetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-midioutsetvolume) | Imposta il livello di volume del dispositivo sintetizzatore MIDI interno specificato.      |



 

Non tutti i dispositivi di output MIDI supportano le modifiche al volume. Alcuni dispositivi possono supportare singole modifiche del volume nei canali sinistro e destro. Per informazioni su come determinare se un determinato dispositivo supporta le modifiche del volume, vedere [Esecuzione di query sui dispositivi di output MIDI.](querying-midi-output-devices.md)

A meno che l'applicazione non sia progettata per essere un'applicazione master per il controllo del volume (fornisce all'utente il controllo del volume per tutti i dispositivi audio in un sistema), è necessario aprire un dispositivo audio prima di modificarne il volume. È anche necessario controllare il livello del volume prima di modificarlo e ripristinare il livello del volume al livello precedente appena possibile.

Volume specificato come valore doubleword. I 16 bit superiori specificano il volume relativo del canale destro e i 16 bit inferiori specificano il volume relativo del canale sinistro.

Per i dispositivi che non supportano singole modifiche del volume nei canali sinistro e destro, i 16 bit inferiori specificano il livello del volume e i 16 bit superiori vengono ignorati. I valori per il livello di volume variano da 0x0 (silenzio) a 0xFFFF (volume massimo) e vengono interpretati logaritmicamente. L'aumento del volume percepito è lo stesso quando si aumenta il livello di volume da 0x5000 a 0x6000 come da 0x4000 a 0x5000.

 

 