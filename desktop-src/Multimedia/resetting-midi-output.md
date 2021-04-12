---
title: Reimpostazione dell'output MIDI
description: Reimpostazione dell'output MIDI
ms.assetid: 281a7cfa-f274-4c7a-b63a-c0573b9f1169
keywords:
- MIDI (Musical Instrument Digital Interface), reimpostazione dei dispositivi di output
- MIDI (Musical Instrument Digital Interface), reimpostazione dei dispositivi di output
- riproduzione di file MIDI, reimpostazione dei dispositivi di output
- reimpostazione dei dispositivi di output
- MIDI (Musical Instrument Digital Interface), dispositivi di output
- MIDI (Musical Instrument Digital Interface), dispositivi di output
- riproduzione di file MIDI, dispositivi di output
- Dispositivi di output MIDI
- EOX (End-of-Exclusive)
- End-of-Exclusive (EOX)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15778fc8a1a48c34b69915aafb7e3139153b5882
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104336878"
---
# <a name="resetting-midi-output"></a>Reimpostazione dell'output MIDI

La funzione [**midiOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-midioutreset) disattiva tutte le note in tutti i canali MIDI per un dispositivo MIDI specificato. Quindi, la funzione contrassegna i buffer esclusivi del sistema in sospeso come completato e li restituisce all'applicazione. Questa funzione può essere utile in un'applicazione che usa l'output MIDI per fornire all'utente la possibilità di reimpostare l'output MIDI.

> [!Note]  
> La chiusura di un messaggio esclusivo del sistema senza inviare un byte EOX (End of Exclusive) può causare problemi per il dispositivo di destinazione. La funzione **midiOutReset** non invia un byte EOX quando termina un messaggio esclusivo del sistema, perché le applicazioni sono responsabili di questa operazione.

 

 

 