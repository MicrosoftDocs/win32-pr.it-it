---
title: Tipi di dati di input MIDI
description: Tipi di dati di input MIDI
ms.assetid: c67f149e-60b8-4f9e-8e3c-a88cd579d29f
keywords:
- MIDI (Musical Instrument Digital Interface), tipi di dati di input
- MIDI (Musical Instrument Digital Interface), tipi di dati di input
- registrazione audio MIDI, tipi di dati di input
- Tipi di dati di input MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8f0738827cce4cfd8cb4a237dcd2031c2fe71a7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299750"
---
# <a name="midi-input-data-types"></a>Tipi di dati di input MIDI

Windows definisce i tipi di dati seguenti per le funzioni di input MIDI.



| Valore                            | Significato                                                                                                                                                                                     |
|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **HMIDIIN**                      | Handle di un dispositivo di input MIDI.                                                                                                                                                              |
| [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr)       | Intestazione per un buffer di flusso o un blocco di dati esclusivi del sistema MIDI. Per le applicazioni di input, questa struttura registra solo i dati esclusivi del sistema (il flusso non è supportato per l'input MIDI). |
| [**MIDIINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-midiincaps) | Struttura usata per richiedere informazioni sulle funzionalità di un dispositivo di input MIDI.                                                                                                                    |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registrazione audio MIDI](recording-midi-audio.md)
</dt> </dl>

 

 