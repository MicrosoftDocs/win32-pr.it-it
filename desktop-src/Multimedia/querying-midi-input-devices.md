---
title: Esecuzione di query su dispositivi di input MIDI
description: Esecuzione di query su dispositivi di input MIDI
ms.assetid: 2da88418-f9cf-49da-b17f-8a26d357b5ab
keywords:
- Instrument Digital Interface (MIDI), dispositivi di input
- MIDI (Instrument Digital Interface), dispositivi di input
- registrazione di audio MIDI, dispositivi di input
- Dispositivi di input MIDI
- Instrument Digital Interface (MIDI), esecuzione di query sui dispositivi di input
- MIDI (Instrument Digital Interface), esecuzione di query sui dispositivi di input
- registrazione di audio MIDI, esecuzione di query su dispositivi di input
- esecuzione di query su dispositivi di input MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81340f767c1ef3acf3105f78d2cef000f7548361b387e6887ecc4136437dbe6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118371933"
---
# <a name="querying-midi-input-devices"></a>Esecuzione di query su dispositivi di input MIDI

Prima di registrare l'audio MIDI, è necessario usare la funzione [**midiInGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-midiingetdevcaps) per determinare le funzionalità del dispositivo di input MIDI presente nel sistema. Questa funzione accetta un indirizzo di una struttura [**MIDIINCAPS,**](/windows/win32/api/mmeapi/ns-mmeapi-midiincaps) che contiene informazioni sulle funzionalità del dispositivo specificato. Queste informazioni includono gli identificatori del produttore e del prodotto, il nome del prodotto per il dispositivo e il numero di versione del driver di dispositivo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registrazione di audio MIDI](recording-midi-audio.md)
</dt> </dl>

 

 