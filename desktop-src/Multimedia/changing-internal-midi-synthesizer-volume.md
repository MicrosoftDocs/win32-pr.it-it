---
title: Modifica del volume del sintetizzatore MIDI interno
description: Modifica del volume del sintetizzatore MIDI interno
ms.assetid: 75ab7ff5-f394-4a79-8dcc-f4eef434a36e
keywords:
- MIDI (Musical Instrument Digital Interface), sintetizzatori interni
- MIDI (Musical Instrument Digital Interface), sintetizzatori interni
- riproduzione di file MIDI, sintetizzatori interni
- Sintetizzatori MIDI interni
- MIDI (Musical Instrument Digital Interface), modifica del volume
- MIDI (Musical Instrument Digital Interface), modifica del volume
- riproduzione di file MIDI, modifica del volume
- modifica del volume MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2369b13483ce6fa45d82ee177282a0de5e86538e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103963053"
---
# <a name="changing-internal-midi-synthesizer-volume"></a>Modifica del volume del sintetizzatore MIDI interno

Windows fornisce le funzioni seguenti per recuperare e impostare il livello di volume dei dispositivi del sintetizzatore MIDI interno:



| Valore                                        | Significato                                                                       |
|----------------------------------------------|-------------------------------------------------------------------------------|
| [**midiOutGetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetvolume) | Recupera il livello del volume del dispositivo del sintetizzatore MIDI interno specificato. |
| [**midiOutSetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-midioutsetvolume) | Imposta il livello del volume del dispositivo del sintetizzatore MIDI interno specificato.      |



 

Non tutti i dispositivi di output MIDI supportano le modifiche del volume. Alcuni dispositivi sono in grado di supportare singole modifiche dei volumi nei canali sinistro e destro. Per informazioni su come determinare se un dispositivo specifico supporta le modifiche del volume, vedere [esecuzione di query sui dispositivi di output MIDI](querying-midi-output-devices.md).

A meno che l'applicazione non sia progettata come applicazione di controllo del volume principale (fornisce all'utente il controllo del volume per tutti i dispositivi audio in un sistema), è necessario aprire un dispositivo audio prima di modificare il volume. È inoltre consigliabile controllare il livello del volume prima di modificarlo e ripristinare il livello del volume precedente il prima possibile.

Il volume viene specificato come valore parola doppia. I 16 bit superiori specificano il volume relativo del canale destro e i 16 bit inferiori specificano il volume relativo del canale sinistro.

Per i dispositivi che non supportano modifiche dei singoli volumi nei canali sinistro e destro, i 16 bit inferiori specificano il livello di volume e i 16 bit superiori vengono ignorati. I valori per il livello del volume variano da 0x0 (silenzioso) a 0xFFFF (volume massimo) e vengono interpretati come logaritmicamente. L'aumento del volume percepito è lo stesso quando si aumenta il livello di volume da 0x5000 a 0x6000, come da 0x4000 a 0x5000.

 

 