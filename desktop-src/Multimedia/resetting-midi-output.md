---
title: Reimpostazione dell'output MIDI
description: Reimpostazione dell'output MIDI
ms.assetid: 281a7cfa-f274-4c7a-b63a-c0573b9f1169
keywords:
- MidI (Musical Instrument Digital Interface), reimpostazione dei dispositivi di output
- MIDI (Musical Instrument Digital Interface), reimpostazione dei dispositivi di output
- riproduzione di file MIDI, reimpostazione dei dispositivi di output
- reimpostazione dei dispositivi di output
- MidI (Musical Instrument Digital Interface), dispositivi di output
- MIDI (Musical Instrument Digital Interface), dispositivi di output
- riproduzione di file MIDI, dispositivi di output
- Dispositivi di output MIDI
- EOX (fine esclusiva)
- end-of-exclusive (EOX)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46c0073d9fc016e21e401e4cb2e7c28b4fd1aa5e3180801975df4e334243b953
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119689261"
---
# <a name="resetting-midi-output"></a>Reimpostazione dell'output MIDI

La [**funzione midiOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-midioutreset) disattiva tutte le note in tutti i canali MIDI per un dispositivo MIDI specificato. Quindi, la funzione contrassegna tutti i buffer esclusivi di sistema in sospeso come completata e li restituisce all'applicazione. Questa funzione può essere utile in un'applicazione che usa l'output MIDI per fornire all'utente la possibilità di reimpostare l'output MIDI.

> [!Note]  
> La terminazione di un messaggio esclusivo di sistema senza inviare un byte EOX (fine esclusivo) può causare problemi per il dispositivo ricevente. La **funzione midiOutReset** non invia un byte EOX quando termina un messaggio esclusivo di sistema, perché le applicazioni sono responsabili di questa operazione.

 

 

 