---
description: Modalità di funzionamento di VMR
ms.assetid: 98244af1-5934-4d1c-b9c3-7a414b065fe7
title: Modalità di funzionamento di VMR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88e7a1fa378ff781a712f71c877c32991cf19683a81daa10ff9b2fbbea40e7c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049371"
---
# <a name="vmr-modes-of-operation"></a>Modalità di funzionamento di VMR

L'architettura dei componenti della macchina virtuale consente alle applicazioni di configurarla in vari modi, a seconda della modalità di esecuzione del rendering. La tabella seguente illustra le tre modalità di presentazione e le due modalità di combinazione e i componenti presenti per ogni configurazione.



| Mode       | Flusso singolo                                                                     | Più Flussi (modalità di combinazione)                                                                                             |
|------------|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| Finestra   | Unità di sincronizzazione Allocator-presenterCore<br/> Gestione finestre<br/> | MixerCompositor\*<br/> Allocator-presenter<br/> Unità di sincronizzazione principale<br/> Gestione finestre<br/> |
| Windowless | Unità di sincronizzazione Allocator-presenterCore<br/>                           | MixerCompositor\*<br/> Allocator-presenter<br/> Unità di sincronizzazione principale<br/>                           |
| Senza rendering | Allocator-presenter (fornito dall'applicazione)Unità di sincronizzazione principale<br/> | MixerCompositor\*<br/> Allocator-presenter (fornito dall'applicazione)<br/> Unità di sincronizzazione principale<br/> |



 

\* Indica che l'applicazione ha la possibilità di fornire un componente personalizzato o di usare il componente predefinito.

In tutte le configurazioni, il punto principale da ricordare quando si creano grafici di filtro con la macchina virtuale è che è necessario configurare la macchina virtuale prima di connetterla.

Per tutte le configurazioni, i pin non possono essere aggiunti o rimossi dinamicamente dopo che la macchina virtuale è connessa al filtro upstream, ma possono essere connessi e disconnessi. Se l'applicazione non è certi del numero di pin necessari, deve configurare il vmr per il numero massimo che potrebbe essere necessario. La presenza di pin di input inutilizzati nel filtro non riduce le prestazioni di rendering. A differenza della versione precedente Mixer overlay, la macchina virtuale non dispone di un pin di output perché non richiede un filtro separato per la gestione delle finestre.

Le sezioni seguenti descrivono come configurare la macchina virtuale per una determinata modalità:

-   [Modalità finestra vmr (compatibilità)](vmr-windowed--compatibility--mode.md)
-   [Modalità senza finestra vmr](vmr-windowless-mode.md)
-   [VMR con più Flussi (modalità di combinazione)](vmr-with-multiple-streams--mixing-mode.md)
-   [Modalità di combinazione YUV](yuv-mixing-mode.md)
-   [Posizionamento e spostamento di rettangoli video nello spazio di composizione](positioning-and-moving-video-rectangles-in-composition-space.md)
-   [Modalità di riproduzione senza rendering vmr (allocatore-presentatori personalizzati)](vmr-renderless-playback-mode--custom-allocator-presenters.md)
-   [Modalità esclusiva DirectDraw](directdraw-exclusive-mode.md)

 

 




