---
title: Tipi di dati di input MIDI
description: Tipi di dati di input MIDI
ms.assetid: c67f149e-60b8-4f9e-8e3c-a88cd579d29f
keywords:
- Instrument Digital Interface (MIDI), tipi di dati di input
- MIDI (Instrument Digital Interface), tipi di dati di input
- registrazione di audio MIDI, tipi di dati di input
- Tipi di dati di input MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f3cb45c321cdac95c09274f25293f4635d5a715638367c8f9e06cf5c45777af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119525221"
---
# <a name="midi-input-data-types"></a>Tipi di dati di input MIDI

Windows definisce i tipi di dati seguenti per le funzioni di input MIDI.



| Valore                            | Significato                                                                                                                                                                                     |
|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **HMIDIIN**                      | Handle di un dispositivo di input MIDI.                                                                                                                                                              |
| [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr)       | Intestazione per un buffer del flusso o un blocco di dati esclusivi di sistema MIDI. Per le applicazioni di input, questa struttura registra solo i dati esclusivi del sistema (il flusso non è supportato per l'input MIDI). |
| [**MIDIINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-midiincaps) | Struttura usata per ottenere informazioni sulle funzionalità di un dispositivo di input MIDI.                                                                                                                    |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registrazione di audio MIDI](recording-midi-audio.md)
</dt> </dl>

 

 