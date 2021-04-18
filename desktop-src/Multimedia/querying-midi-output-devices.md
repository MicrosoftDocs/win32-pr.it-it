---
title: Esecuzione di query sui dispositivi di output MIDI
description: Esecuzione di query sui dispositivi di output MIDI
ms.assetid: c6a33a4e-c61a-4e06-805e-5128a97f5199
keywords:
- MIDI (Musical Instrument Digital Interface), dispositivi di output
- MIDI (Musical Instrument Digital Interface), dispositivi di output
- riproduzione di file MIDI, dispositivi di output
- Dispositivi di output MIDI
- MIDI (Musical Instrument Digital Interface), esecuzione di query sui dispositivi di output
- MIDI (Musical Instrument Digital Interface), esecuzione di query sui dispositivi di output
- riproduzione di file MIDI, esecuzione di query sui dispositivi di output
- esecuzione di query sui dispositivi di output MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 292fbacbb4acf182d566e8c98832dfb0f993ea2b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299710"
---
# <a name="querying-midi-output-devices"></a>Esecuzione di query sui dispositivi di output MIDI

Prima di riprodurre un file MIDI, è necessario usare la funzione [**midiOutGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetdevcaps) per determinare le funzionalità del dispositivo di output MIDI presente nel sistema. Questa funzione accetta un indirizzo di una struttura [**MIDIOUTCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-midioutcaps) , che compila con informazioni sulle funzionalità del dispositivo specificato. Queste informazioni includono gli identificatori del produttore e del prodotto, il nome del prodotto per il dispositivo e il numero di versione del driver di dispositivo, rispettivamente specificato nei membri **wMid**, **wPid**, **szPname** e **vDriverVersion** .

I dispositivi di output MIDI possono essere sintetizzatori interni o porte di output MIDI esterne. Il membro **wTechnology** della struttura **MIDIOUTCAPS** specifica la tecnologia del dispositivo.

Se il dispositivo è un sintetizzatore interno, sono disponibili informazioni aggiuntive sul dispositivo nei membri **wVoices**, **wNotes** e **wChannelMask** . Il membro **wVoices** specifica il numero di voci supportate dal dispositivo. Ogni voce può avere un suono o un timbro diverso. Le voci sono organizzate in canali MIDI. Il membro **wNotes** specifica la *polifonia* del dispositivo, ovvero il numero massimo di note che possono essere riprodotte simultaneamente. Il membro **wChannelMask** è una rappresentazione di bit dei canali MIDI a cui risponde il dispositivo. Ad esempio, se il dispositivo risponde ai primi otto canali MIDI, **wChannelMask** è 0x00FF. Se il dispositivo è una porta di output esterna, **wVoices** e **wNotes** sono inutilizzati e **wChannelMask** è impostato su 0xffff.

Il membro **dwSupport** della struttura **MIDIOUTCAPS** indica se il driver di dispositivo supporta le modifiche del volume, la memorizzazione nella cache delle patch e il flusso. Le modifiche del volume sono supportate solo dai dispositivi del sintetizzatore interno. Le porte di output MIDI esterne non supportano le modifiche del volume. Per informazioni sulla modifica del volume, vedere [modifica del volume del sintetizzatore MIDI interno](changing-internal-midi-synthesizer-volume.md).

 

 