---
title: Tipi di dispositivi
description: Tipi di dispositivi
ms.assetid: 6556fa6a-5906-4afb-ab7d-ef41a0e22d13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e27ed77debb663a1d90e03512832ca83e6e276d3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712967"
---
# <a name="device-types"></a>Tipi di dispositivi

MCI riconosce un set di base di *tipi di dispositivi*. Un tipo di dispositivo è un set di driver MCI che condividono un set di comandi comune e vengono usati per controllare dispositivi multimediali o file di dati simili. Molti comandi MCI, ad esempio [**Open**](open.md) ([**MCI \_ Open**](mci-open.md)), richiedono di specificare un tipo di dispositivo.

Nella tabella seguente sono elencati i tipi di dispositivi definiti. L'implementazione corrente di MCI include i set di comandi per un subset di questi dispositivi.



| Tipo di dispositivo      | Costante                      | Descrizione                                      |
|------------------|-------------------------------|--------------------------------------------------|
| **cdaudio**      | \_ \_ audio CD DEVTYPE \_ MCI       | Lettore audio CD                                  |
| **dat**          | DEVTYPE di MCI \_ \_             | Lettore nastro digitale audio                        |
| **digitalvideo** | \_ \_ video digitale MCI \_ DEVTYPE  | Video digitale in una finestra (non basato su GDI)        |
| **altri**        | \_altri DEVTYPE \_ MCI           | Dispositivo MCI non definito                             |
| **sovrapposizione**      | \_ \_ sovrimpressione DEVTYPE MCI         | Dispositivo overlay (video analogico in una finestra)        |
| **scanner**      | \_scanner DEVTYPE \_ MCI         | Scanner immagini                                    |
| **sequencer**    | \_ \_ sequencer DEVTYPE MCI       | Sequencer MIDI                                   |
| **VCR**          | \_VCR DEVTYPE \_ MCI             | Registratore di cassette video o lettore                |
| **videodisco**    | \_videodisco DEVTYPE \_ MCI       | Videodisco Player                                 |
| **WaveAudio**    | \_audio della \_ waveform \_ DEVTYPE MCI | Dispositivo audio che riproduce file di forma d'onda digitalizzati |



 

In questo documento i nomi dei tipi di dispositivo sono in grassetto. I nomi dei tipi di dispositivo vengono usati con l'interfaccia della stringa di comando. Le costanti di tipo dispositivo vengono usate con l'interfaccia del messaggio di comando.

 

 




