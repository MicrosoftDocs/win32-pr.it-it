---
title: Allocazione e preparazione di blocchi di dati MIDI
description: Allocazione e preparazione di blocchi di dati MIDI
ms.assetid: b3a70441-e8f9-4886-bf22-426ebd74d045
keywords:
- MIDI (Musical Instrument Digital Interface), allocazione di blocchi di dati
- MIDI (Musical Instrument Digital Interface), allocazione di blocchi di dati
- Servizi MIDI, allocazione di blocchi di dati
- allocazione di blocchi di dati MIDI
- MIDI (Musical Instrument Digital Interface), preparazione dei blocchi di dati
- MIDI (Musical Instrument Digital Interface), preparazione dei blocchi di dati
- Servizi MIDI, preparazione dei blocchi di dati
- preparazione dei blocchi di dati MIDI
- MIDI (Musical Instrument Digital Interface), blocchi di dati
- MIDI (Musical Instrument Digital Interface), blocchi di dati
- Servizi MIDI, blocchi di dati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48b23a72dfd46035a3d23743faa7228e5fe85aaf
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299764"
---
# <a name="allocating-and-preparing-midi-data-blocks"></a>Allocazione e preparazione di blocchi di dati MIDI

Le funzioni [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg), [**midiInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer)e [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) richiedono che le applicazioni allochino i blocchi di dati da passare ai driver di dispositivo ai fini della riproduzione o della registrazione. Ognuna di queste funzioni utilizza una struttura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) per descrivere il relativo blocco di dati.

Prima di usare una di queste funzioni per passare un blocco di dati a un driver di dispositivo, è necessario allocare memoria per il buffer e la struttura dell'intestazione che descrive il blocco di dati.

Windows fornisce le funzioni seguenti per la preparazione e la pulizia dei blocchi di dati MIDI.



| Valore                                                    | Significato                                                |
|----------------------------------------------------------|--------------------------------------------------------|
| [**midiInPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midiinprepareheader)       | Prepara un blocco di dati di input MIDI.                      |
| [**midiInUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midiinunprepareheader)   | Pulisce la preparazione di un blocco di dati di input MIDI.  |
| [**midiOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutprepareheader)     | Prepara un blocco di dati di output MIDI.                     |
| [**midiOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutunprepareheader) | Pulisce la preparazione di un blocco di dati di output MIDI. |



 

Prima di passare un blocco di dati MIDI a un driver di dispositivo, è necessario preparare il buffer passandolo alla funzione [**midiInPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midiinprepareheader) o [**midiOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutprepareheader) . Quando il driver di dispositivo è terminato con il buffer e lo restituisce, è necessario pulire la preparazione passando il buffer alla funzione [**midiInUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midiinunprepareheader) o [**midiOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutunprepareheader) prima di poter liberare la memoria allocata.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Servizi MIDI](midi-services.md)
</dt> </dl>

 

 