---
title: Gestione degli errori con le funzioni MIDI
description: Gestione degli errori con le funzioni MIDI
ms.assetid: 7ea5db5e-34d7-4506-8157-c24adf5bcdda
keywords:
- MIDI (Musical Instrument Digital Interface), errori
- MIDI (Musical Instrument Digital Interface), errori
- Servizi MIDI, errori
- Errori MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9689fe30b9c4f598cfc9bea892ff3d4fe15d3a9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299812"
---
# <a name="handling-errors-with-midi-functions"></a>Gestione degli errori con le funzioni MIDI

Le funzioni audio MIDI restituiscono un codice di errore diverso da zero. Per gli errori associati a MIDI, le funzioni [**midiInGetErrorText**](/windows/win32/api/mmeapi/nf-mmeapi-midiingeterrortext) e [**midiOutGetErrorText**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgeterrortext) recuperano le descrizioni testuali per i codici di errore. L'applicazione deve comunque esaminare il valore di errore stesso per determinare il modo in cui procedere, ma può utilizzare le descrizioni degli errori nelle finestre di dialogo per informare gli utenti delle condizioni di errore.

Le uniche funzioni MIDI che non restituiscono codici di errore sono le funzioni [**midiInGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-midiingetnumdevs) e [**midiOutGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetnumdevs) . Queste funzioni restituiscono un valore pari a zero se non sono presenti dispositivi in un sistema o se vengono rilevati errori dalla funzione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Servizi MIDI](midi-services.md)
</dt> </dl>

 

 