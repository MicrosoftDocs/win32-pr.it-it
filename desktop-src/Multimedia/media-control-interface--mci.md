---
title: Interfaccia di controllo multimediale (MCI)
description: Interfaccia di controllo multimediale (MCI)
ms.assetid: e22f23b5-0fa6-4957-bbbf-b1b3a4c8bd31
keywords:
- Multimedia di Windows, interfaccia di controllo multimediale (MCI)
- Multimedia, interfaccia di controllo multimediale (MCI)
- audio multimediale, MCI (Media Control Interface)
- audio, interfaccia di controllo multimediale (MCI)
- MIDI (Musical Instrument Digital Interface), MCI (Media Control Interface)
- MIDI (strumento musicale digitale), MCI (Media Control Interface)
- Interfaccia di controllo multimediale (MCI), Musical Instrument Digital Interface (MIDI)
- MCI (Media Control Interface), Musical Instrument Digital Interface (MIDI)
- Interfaccia di controllo multimediale (MCI), MIDI sequencer
- MCI (Media Control Interface), MIDI sequencer
- MCI MIDI sequencer, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00aaf582f625c4411a2400ee381ec5c17d4d8ae7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044639"
---
# <a name="media-control-interface-mci"></a>Interfaccia di controllo multimediale (MCI)

MCI MIDI sequencer è il componente di sistema MCI che riproduce file MIDI. Le applicazioni possono riprodurre facilmente file MIDI usando MCI, ma MCI impone le seguenti restrizioni sulle funzionalità MIDI:

-   MCI supporta solo l'output MIDI.
-   MCI non consente la sincronizzazione di chiusura tra eventi MIDI e altri eventi in tempo reale, ad esempio video.

Se è necessaria una sincronizzazione MIDI accurata, è necessario usare i buffer di flusso o i servizi MIDI. Se sono necessarie funzionalità di input MIDI, è necessario usare i servizi MIDI.

MCI MIDI sequencer riproduce i file MIDI standard e i file MIDI del formato di file di scambio di risorse (RIFF), noti come file RMID. I file MIDI standard sono conformi alla specifica dei [file MIDI standard 1,0](creating-midi-files.md) . Poiché i file RMID sono file MIDI standard con un'intestazione RIFF, le informazioni sui file MIDI standard si applicano anche ai file RMID. Per altre informazioni sui file RIFF, vedere [Resource Interchange File Format Services](resource-interchange-file-format-services.md).

Sebbene esistano attualmente tre tipi di file MIDI standard, MCI sequencer ne riproduce solo due: formato 0 e formato 1 file MIDI.

Per ulteriori informazioni sul controllo dei dispositivi multimediali (inclusi i sequencer) utilizzando i comandi MCI, vedere [MCI](mci.md).

 

 




