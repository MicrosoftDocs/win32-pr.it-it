---
title: Esecuzione di query sui dispositivi di output MIDI
description: Esecuzione di query sui dispositivi di output MIDI
ms.assetid: c6a33a4e-c61a-4e06-805e-5128a97f5199
keywords:
- Instrument Digital Interface (MIDI), dispositivi di output
- MIDI (Instrument Digital Interface), dispositivi di output
- riproduzione di file MIDI, dispositivi di output
- Dispositivi di output MIDI
- Instrument Digital Interface (MIDI), esecuzione di query sui dispositivi di output
- MIDI (Instrument Digital Interface), esecuzione di query sui dispositivi di output
- riproduzione di file MIDI, esecuzione di query su dispositivi di output
- esecuzione di query su dispositivi di output MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b493c0b3554a9a60cfc349d13a5404ec4d2b27915933c14b387df29a582406e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118371913"
---
# <a name="querying-midi-output-devices"></a>Esecuzione di query sui dispositivi di output MIDI

Prima di riprodurre un file MIDI, è necessario usare la funzione [**midiOutGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetdevcaps) per determinare le funzionalità del dispositivo di output MIDI presente nel sistema. Questa funzione accetta un indirizzo di una struttura [**MIDIOUTCAPS,**](/windows/win32/api/mmeapi/ns-mmeapi-midioutcaps) che contiene informazioni sulle funzionalità del dispositivo specificato. Queste informazioni includono gli identificatori del produttore e del prodotto, un nome di prodotto per il dispositivo e il numero di versione del driver di dispositivo (specificato rispettivamente nei membri **wMid**, **wPid**, **szPname** e **vDriverVersion** ).

I dispositivi di output MIDI possono essere sintetizzatori interni o porte di output MIDI esterne. Il **membro wTechnology** della **struttura MIDIOUTCAPS** specifica la tecnologia del dispositivo.

Se il dispositivo è un sintetizzatore interno, sono disponibili informazioni aggiuntive sul dispositivo nei membri **wVoices,** **wNotes** e **wChannelMask.** Il **membro wVoices** specifica il numero di voci supportate dal dispositivo. Ogni voce può avere un suono o un timbro diverso. Le voci sono organizzate in canali MIDI. Il **membro wNotes** specifica la *polifonosi* del dispositivo, ovvero il numero massimo di note che possono essere riprodotte contemporaneamente. Il **membro wChannelMask** è una rappresentazione di bit dei canali MIDI a cui risponde il dispositivo. Ad esempio, se il dispositivo risponde ai primi otto canali MIDI, **wChannelMask** viene 0x00FF. Se il dispositivo è una porta di output esterna, **wVoices** e **wNotes** non sono usati e **wChannelMask** è impostato su 0xFFFF.

Il **membro dwSupport** della struttura **MIDIOUTCAPS** indica se il driver di dispositivo supporta le modifiche al volume, la memorizzazione nella cache delle patch e lo streaming. Le modifiche al volume sono supportate solo dai dispositivi di sintesi interni. Le porte di output MIDI esterne non supportano le modifiche al volume. Per informazioni sulla modifica del volume, vedere Modifica del volume interno del sintetizzatore [MIDI.](changing-internal-midi-synthesizer-volume.md)

 

 