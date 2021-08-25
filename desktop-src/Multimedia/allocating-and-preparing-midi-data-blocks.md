---
title: Allocazione e preparazione di blocchi di dati MIDI
description: Allocazione e preparazione di blocchi di dati MIDI
ms.assetid: b3a70441-e8f9-4886-bf22-426ebd74d045
keywords:
- Instrument Digital Interface (MIDI), allocazione di blocchi di dati
- MIDI (Instrument Digital Interface), allocazione di blocchi di dati
- servizi MIDI, allocazione di blocchi di dati
- allocazione di blocchi di dati MIDI
- Instrument Digital Interface (MIDI), preparazione dei blocchi di dati
- MIDI (Instrument Digital Interface), preparazione dei blocchi di dati
- servizi MIDI, preparazione di blocchi di dati
- preparazione di blocchi di dati MIDI
- Instrument Digital Interface (MIDI), blocchi di dati
- MIDI (Instrument Digital Interface), blocchi di dati
- servizi MIDI, blocchi di dati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 137556c1344e6f2e8db8557d45a70c5981fa7bab99e7452cc1f756b4a8ee159b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119808491"
---
# <a name="allocating-and-preparing-midi-data-blocks"></a>Allocazione e preparazione di blocchi di dati MIDI

Le [**funzioni midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg), [**midiInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer)e [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) richiedono che le applicazioni allocano blocchi di dati da passare ai driver di dispositivo a scopo di riproduzione o registrazione. Ognuna di queste funzioni usa una [**struttura MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) per descrivere il blocco di dati.

Prima di usare una di queste funzioni per passare un blocco di dati a un driver di dispositivo, è necessario allocare memoria per il buffer e la struttura di intestazione che descrive il blocco di dati.

Windows fornisce le funzioni seguenti per la preparazione e la pulizia dei blocchi di dati MIDI.



| Valore                                                    | Significato                                                |
|----------------------------------------------------------|--------------------------------------------------------|
| [**midiInPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midiinprepareheader)       | Prepara un blocco di dati di input MIDI.                      |
| [**midiInUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midiinunprepareheader)   | Pulisce la preparazione di un blocco di dati di input MIDI.  |
| [**midiOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutprepareheader)     | Prepara un blocco di dati di output MIDI.                     |
| [**midiOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutunprepareheader) | Pulisce la preparazione di un blocco di dati di output MIDI. |



 

Prima di passare un blocco di dati MIDI a un driver di dispositivo, è necessario preparare il buffer passandolo alla funzione [**midiInPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midiinprepareheader) o [**midiOutPrepareHeader.**](/windows/win32/api/mmeapi/nf-mmeapi-midioutprepareheader) Quando il driver di dispositivo termina con il buffer e lo restituisce, è necessario pulire questa preparazione passando il buffer alla funzione [**midiInUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midiinunprepareheader) o [**midiOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutunprepareheader) prima che sia possibile liberare memoria allocata.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Servizi MIDI](midi-services.md)
</dt> </dl>

 

 