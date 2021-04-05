---
title: Tipi di dati di input Waveform-Audio
description: Tipi di dati di input Waveform-Audio
ms.assetid: dfedcb93-edfb-4a25-8445-95d4aee55734
keywords:
- audio Waveform, tipi di dati di input
- waveform-interfaccia audio, tipi di dati di input
- registrazione audio della forma d'onda, tipi di dati di input
- Handle HWAVEIN
- Struttura WAVEFORMATEX
- Struttura WAVEHDR
- Struttura WAVEINCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39a8d37869224fe2ce677e2b8b952030ca6e021f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046675"
---
# <a name="waveform-audio-input-data-types"></a>Tipi di dati di input Waveform-Audio

I tipi di dati seguenti sono definiti per le funzioni di input audio e di forma d'onda.



| Tipo                                 | Descrizione                                                                                                                                                     |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **HWAVEIN**                          | Handle di un dispositivo di input audio e di forma d'onda aperto.                                                                                                                  |
| [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) | Struttura che specifica i formati di dati supportati da un dispositivo di input audio e di forma d'onda particolare. Questa struttura viene usata anche per i dispositivi di output dell'audio e della forma d'onda. |
| [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr)           | Struttura utilizzata come intestazione per un blocco di dati di input audio e di forma d'onda. Questa struttura viene usata anche per i dispositivi di output dell'audio e della forma d'onda.                             |
| [**WAVEINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveincaps)     | Struttura usata per richiedere informazioni sulle funzionalità di un dispositivo di input audio e di forma d'onda particolare.                                                                   |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registrazione dell'audio della forma d'onda](recording-waveform-audio.md)
</dt> </dl>

 

 