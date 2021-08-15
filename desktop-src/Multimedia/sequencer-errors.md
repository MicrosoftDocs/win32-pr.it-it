---
title: Errori del sequencer
description: Errori del sequencer
ms.assetid: 07f2d6c5-8c23-4f3e-8b8a-4f659eda57f7
keywords:
- MCIERR return values,sequencer errors
- informazioni di riferimento multimediali, errori sequencer
- informazioni di riferimento per elementi multimediali, errori sequencer
- Media Control Interface (MCI), sequencer errors
- MCI (Media Control Interface), sequencer errors
- informazioni di riferimento per MCI, errori sequencer
- Riferimento MCI, errori sequencer
- Media Control Interface (MCI), errors
- MCI (Media Control Interface), errori
- riferimento per MCI, errori
- Riferimento MCI, errori
- Errori di sequencer
- Errori del sequencer MCI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bea7e5b38d5541041e8ec065c8cad31f9d31ed1bfa9f22562aba1bf1ff04039b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118371129"
---
# <a name="sequencer-errors"></a>Errori del sequencer

Per i sequencer MCI sono definiti i valori restituiti aggiuntivi seguenti:



| Valore                          | Significato                                                                                                                                                  |
|--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| MCIERR \_ SEQ \_ DIV \_ INCOMPATIBILE | I formati di ora del "puntatore del brano" e SMPTE sono singolari. Non è possibile usarli insieme.                                                              |
| MCIERR \_ SEQ \_ NOMIDIPRESENT     | Questo sistema non ha dispositivi MIDI installati. Usare l'opzione Driver dal Pannello di controllo per installare un driver MIDI.                                       |
| MCIERR \_ SEQ \_ PORT \_ INUSE       | La porta MIDI specificata è già in uso. Attendere che sia gratuito. quindi riprovare.                                                                       |
| MCIERR \_ SEQ \_ PORT \_ MAPNODEVICE | La configurazione corrente di MIDI Mapper si riferisce a un dispositivo MIDI non installato nel sistema. Usare MIDI Mapper dal Pannello di controllo per modificare la configurazione. |
| MCIERR \_ SEQ \_ PORT \_ MISCERROR   | Si è verificato un errore con la porta specificata.                                                                                                                   |
| PORTA MCIERR \_ SEQ \_ \_ INESISTENTE | Il dispositivo MIDI specificato non è installato nel sistema. Usare l'opzione Driver dal Pannello di controllo per installare un dispositivo MIDI.                        |
| MCIERR \_ SEQ \_ PORTUNSPECIFIED   | Nel sistema non è specificata una porta MIDI corrente.                                                                                                  |
| TIMER DI MCIERR \_ SEQ \_             | Tutti i timer multimediali vengono usati da altre applicazioni. Chiudere una di queste applicazioni; quindi riprovare.                                             |



 

 

 




