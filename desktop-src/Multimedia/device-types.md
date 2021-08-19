---
title: Tipi di dispositivo
description: Tipi di dispositivo
ms.assetid: 6556fa6a-5906-4afb-ab7d-ef41a0e22d13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 167eedddfc61960de35e979480c44b8f2efab5bf89738047446196b81a95a5b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119497161"
---
# <a name="device-types"></a>Tipi di dispositivo

McI riconosce un set di base di tipi *di dispositivo*. Un tipo di dispositivo è un set di driver MCI che condividono un set di comandi comune e vengono usati per controllare dispositivi multimediali o file di dati simili. Molti comandi MCI, ad esempio [**open**](open.md) [**(MCI \_ OPEN),**](mci-open.md)richiedono di specificare un tipo di dispositivo.

Nella tabella seguente sono elencati i tipi di dispositivo definiti. L'implementazione corrente di MCI include set di comandi per un subset di questi dispositivi.



| Tipo di dispositivo      | Costante                      | Descrizione                                      |
|------------------|-------------------------------|--------------------------------------------------|
| **cdaudio**      | MCI \_ DEVTYPE \_ CD \_ AUDIO       | Lettore audio CD                                  |
| **Dat**          | MCI \_ DEVTYPE \_ DAT             | Lettore nastro audio digitale                        |
| **digitalvideo** | VIDEO DIGITALE \_ MCI DEVTYPE \_ \_  | Video digitale in una finestra (non basato su GDI)        |
| **Altro**        | MCI \_ DEVTYPE \_ OTHER           | Dispositivo MCI non definito                             |
| **Sovrapposizione**      | \_SOVRIMPRESSIONE MCI DEVTYPE \_         | Dispositivo di sovrimpressione (video analogico in una finestra)        |
| **Scanner**      | MCI \_ DEVTYPE \_ SCANNER         | Scanner di immagini                                    |
| **sequencer**    | MCI \_ DEVTYPE \_ SEQUENCER       | Sequencer MIDI                                   |
| **Vcr**          | MCI \_ DEVTYPE \_ VCR             | Registratore o lettore videocassetta                |
| **videodisc**    | MCI \_ DEVTYPE \_ VIDEODISC       | Lettore Videodisc                                 |
| **Waveaudio**    | MCI \_ DEVTYPE \_ WAVEFORM \_ AUDIO | Dispositivo audio che riproduce file waveform digitalizzati |



 

In questo documento i nomi dei tipi di dispositivo sono in grassetto. I nomi dei tipi di dispositivo vengono usati con l'interfaccia della stringa di comando. Le costanti di tipo dispositivo vengono usate con l'interfaccia del messaggio di comando.

 

 




