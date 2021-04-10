---
title: Precaricamento di patch con sintetizzatori MIDI interni
description: Precaricamento di patch con sintetizzatori MIDI interni
ms.assetid: c200aa91-ab91-48e8-b3b5-8e7f36e511be
keywords:
- MIDI (Musical Instrument Digital Interface), sintetizzatori interni
- MIDI (Musical Instrument Digital Interface), sintetizzatori interni
- riproduzione di file MIDI, sintetizzatori interni
- Sintetizzatori MIDI interni
- MIDI (Musical Instrument Digital Interface), precaricamento di patch
- MIDI (Musical Instrument Digital Interface), precaricamento di patch
- riproduzione di file MIDI, precaricamento di patch
- precaricamento delle patch MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc54eccdaa0a0c9aa16f206e7e036f322b615d96
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103956407"
---
# <a name="preloading-patches-with-internal-midi-synthesizers"></a>Precaricamento di patch con sintetizzatori MIDI interni

Alcuni dispositivi del sintetizzatore MIDI interno non possono caricare contemporaneamente tutte le patch. Questi dispositivi devono precaricare i dati della patch.

Windows fornisce le funzioni seguenti per richiedere il precaricamento di un sintetizzatore e la memorizzazione nella cache delle patch specificate.



| Valore                                                      | Significato                                                                                                     |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**midiOutCachePatches**](/windows/win32/api/mmeapi/nf-mmeapi-midioutcachepatches)         | Richiede che un dispositivo del sintetizzatore MIDI interno precaricare e memorizzare nella cache le patch melodiche specificate.              |
| [**midiOutCacheDrumPatches**](/windows/win32/api/mmeapi/nf-mmeapi-midioutcachedrumpatches) | Richiede che un dispositivo del sintetizzatore MIDI interno precaricare e memorizzare nella cache le patch di percussione basate su chiavi specificate. |



 

Per informazioni su come determinare se un dispositivo specifico supporta il precaricamento delle patch, vedere [esecuzione di query sui dispositivi di output MIDI](querying-midi-output-devices.md).

 

 