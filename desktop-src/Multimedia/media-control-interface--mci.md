---
title: Interfaccia di controllo multimediale (MCI)
description: Interfaccia di controllo multimediale (MCI)
ms.assetid: e22f23b5-0fa6-4957-bbbf-b1b3a4c8bd31
keywords:
- Windows multimediali, Media Control Interface (MCI)
- multimedia,Media Control Interface (MCI)
- audio multimediale, Media Control Interface (MCI)
- audio, Media Control Interface (MCI)
- MIDI (Musical Instrument Digital Interface), Media Control Interface (MCI)
- MIDI (Musical Instrument Digital Interface), Media Control Interface (MCI)
- Media Control Interface (MCI), Musical Instrument Digital Interface (MIDI)
- MCI (Media Control Interface),Musical Instrument Digital Interface (MIDI)
- Media Control Interface (MCI), sequencer MIDI
- MCI (Media Control Interface), sequencer MIDI
- Sequencer MIDI MCI, informazioni su
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4c8d21588754d0f66dbed97c74bbaabe4c005335059dace2997012691a24c8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119782981"
---
# <a name="media-control-interface-mci"></a>Interfaccia di controllo multimediale (MCI)

Il sequencer MIDI MCI è il componente di sistema MCI che riproduce i file MIDI. Le applicazioni possono riprodurre facilmente i file MIDI usando MCI, ma MCI impone le restrizioni seguenti alle funzionalità MIDI:

-   MCI supporta solo l'output MIDI.
-   MCI non consente la sincronizzazione di chiusura tra eventi MIDI e altri eventi in tempo reale (ad esempio video).

Se è necessaria una sincronizzazione MIDI accurata, è necessario usare i buffer di flusso o i servizi MIDI. Se sono necessarie funzionalità di input MIDI, è necessario usare i servizi MIDI.

Il sequencer MIDI MCI riproduce i file MIDI standard e i file MIDI RIFF (Resource Interchange File Format), noti come file RMID. I file MIDI standard sono conformi alla [specifica MIDI Files 1.0](creating-midi-files.md) standard. Poiché i file RMID sono file MIDI standard con un'intestazione RIFF, le informazioni sui file MIDI standard si applicano anche ai file RMID. Per altre informazioni sui file RIFF, vedere [Resource Interchange File Format Services](resource-interchange-file-format-services.md).

Anche se attualmente sono disponibili tre tipi di file MIDI standard, il sequencer MCI ne riproduce solo due: i file MIDI Format 0 e Format 1.

Per altre informazioni sul controllo dei dispositivi multimediali (inclusi i sequencer) tramite i comandi [MCI,](mci.md)vedere MCI .

 

 




