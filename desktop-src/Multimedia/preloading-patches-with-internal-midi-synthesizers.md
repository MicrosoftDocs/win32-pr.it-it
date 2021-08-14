---
title: Precaricamento di patch con sintetizzatori MIDI interni
description: Precaricamento di patch con sintetizzatori MIDI interni
ms.assetid: c200aa91-ab91-48e8-b3b5-8e7f36e511be
keywords:
- Instrument Digital Interface (MIDI), sintetizzatori interni
- MIDI (Instrument Digital Interface), sintetizzatori interni
- riproduzione di file MIDI, sintetizzatori interni
- sintetizzatori MIDI interni
- Instrument Digital Interface (MIDI), precaricamento delle patch
- MIDI (Instrument Digital Interface), precaricamento delle patch
- riproduzione di file MIDI, precaricamento di patch
- precaricamento di patch MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de389e058c015c38d05fb8ff2a960ca3ef75a662faa6a1ce519c26afe14f09b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118372498"
---
# <a name="preloading-patches-with-internal-midi-synthesizers"></a>Precaricamento di patch con sintetizzatori MIDI interni

Alcuni dispositivi di sintesi MIDI interni non possono mantenere caricate contemporaneamente tutte le patch. Questi dispositivi devono precaricare i dati delle patch.

Windows fornisce le funzioni seguenti per richiedere che un sintetizzatore precarica e memorizza nella cache le patch specificate.



| Valore                                                      | Significato                                                                                                     |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**midiOutCachePatches**](/windows/win32/api/mmeapi/nf-mmeapi-midioutcachepatches)         | Richiede che un dispositivo di sintetizzatore MIDI interno precarica e melodic patch specificate nella cache.              |
| [**midiOutCacheDrumPatches**](/windows/win32/api/mmeapi/nf-mmeapi-midioutcachedrumpatches) | Richiede che un dispositivo di sintetizzatore MIDI interno precarica e memorizza nella cache patch patch basate su chiave specifiche. |



 

Per informazioni su come determinare se un determinato dispositivo supporta il precaricamento delle patch, vedere [Esecuzione di query su dispositivi di output MIDI.](querying-midi-output-devices.md)

 

 