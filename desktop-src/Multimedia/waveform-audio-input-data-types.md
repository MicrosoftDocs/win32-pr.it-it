---
title: Waveform-Audio tipi di dati di input
description: Waveform-Audio tipi di dati di input
ms.assetid: dfedcb93-edfb-4a25-8445-95d4aee55734
keywords:
- audio waveform, tipi di dati di input
- interfaccia waveform-audio,tipi di dati di input
- registrazione di audio waveform, tipi di dati di input
- Handle HWAVEIN
- Struttura WAVEFORMATEX
- Struttura WAVEHDR
- Struttura WAVEINCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6e131e55c404fe658a0c8f60a8f816ff231f9eb9492bcf8641a4e38781bfa78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119892091"
---
# <a name="waveform-audio-input-data-types"></a>Waveform-Audio tipi di dati di input

I tipi di dati seguenti sono definiti per le funzioni di input waveform-audio.



| Tipo                                 | Descrizione                                                                                                                                                     |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **HWAVEIN**                          | Handle di un dispositivo di input open waveform-audio.                                                                                                                  |
| [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) | Struttura che specifica i formati di dati supportati da un particolare dispositivo di input waveform-audio. Questa struttura viene usata anche per i dispositivi di output waveform-audio. |
| [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr)           | Struttura utilizzata come intestazione per un blocco di dati di input waveform-audio. Questa struttura viene usata anche per i dispositivi di output waveform-audio.                             |
| [**WAVEINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveincaps)     | Struttura usata per ottenere informazioni sulle funzionalità di un particolare dispositivo di input waveform-audio.                                                                   |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registrazione dell'audio waveform](recording-waveform-audio.md)
</dt> </dl>

 

 