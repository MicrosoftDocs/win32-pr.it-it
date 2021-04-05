---
title: Errori del sequencer
description: Errori del sequencer
ms.assetid: 07f2d6c5-8c23-4f3e-8b8a-4f659eda57f7
keywords:
- MCIERR valori restituiti, errori del sequencer
- riferimento multimediale, errori del sequencer
- informazioni di riferimento per gli errori di Sequencer e multimediali
- Media Control Interface (MCI), errori del sequencer
- MCI (interfaccia di controllo multimediale), errori del sequencer
- informazioni di riferimento per MCI, errori del sequencer
- Riferimento a MCI, errori del sequencer
- Interfaccia di controllo multimediale (MCI), errori
- MCI (interfaccia di controllo multimediale), errori
- informazioni di riferimento per MCI, errori
- Riferimento a MCI, errori
- errori del sequencer
- Errori del sequencer MCI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dd7d55d3b49be3d641f7396148d98766b224a58
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710441"
---
# <a name="sequencer-errors"></a>Errori del sequencer

Per i sequencer MCI sono definiti i seguenti valori restituiti aggiuntivi:



| Valore                          | Significato                                                                                                                                                  |
|--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| MCIERR \_ seq \_ div \_ incompatibile | I formati di ora del "puntatore del brano" e del SMPTE sono singolari. Non è possibile usarle insieme.                                                              |
| MCIERR \_ seq \_ NOMIDIPRESENT     | Nessun dispositivo MIDI installato nel sistema. Usare l'opzione drivers nel pannello di controllo per installare un driver MIDI.                                       |
| MCIERR \_ seq \_ porta \_ InUse       | La porta MIDI specificata è già in uso. Attendere fino a quando non è disponibile; quindi, riprovare.                                                                       |
| MCIERR \_ seq \_ porta \_ MAPNODEVICE | Il programma di installazione di MIDI Mapper corrente fa riferimento a un dispositivo MIDI non installato nel sistema. Usare il mapper MIDI dal pannello di controllo per modificare l'installazione. |
| MCIERR \_ seq \_ Port \_ uncerror   | Si è verificato un errore con la porta specificata.                                                                                                                   |
| MCIERR \_ seq \_ porta non \_ esistente | Il dispositivo MIDI specificato non è installato nel sistema. Usare l'opzione drivers nel pannello di controllo per installare un dispositivo MIDI.                        |
| MCIERR \_ seq \_ PORTUNSPECIFIED   | Per il sistema non è stata specificata una porta MIDI corrente.                                                                                                  |
| \_timer seq \_ MCIERR             | Tutti i timer multimediali vengono utilizzati da altre applicazioni. Uscire da una di queste applicazioni; quindi, riprovare.                                             |



 

 

 




