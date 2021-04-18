---
description: Modalità di funzionamento VMR
ms.assetid: 98244af1-5934-4d1c-b9c3-7a414b065fe7
title: Modalità di funzionamento VMR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43427c4119bb912d2bc2cf92b1c740b1d22e1bf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308951"
---
# <a name="vmr-modes-of-operation"></a>Modalità di funzionamento VMR

L'architettura dei componenti di VMR consente alle applicazioni di configurarlo in vari modi, a seconda del modo in cui deve essere eseguito il rendering. La tabella seguente illustra le tre modalità di presentazione e le due modalità di combinazione e i componenti presenti per ogni configurazione.



| Modalità       | Flusso singolo                                                                     | Più flussi (modalità di combinazione)                                                                                             |
|------------|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| Finestra   | Allocatore-unità di sincronizzazione presenterCore<br/> Gestione finestre<br/> | MixerCompositor\*<br/> Allocatore-Presenter<br/> Unità di sincronizzazione principale<br/> Gestione finestre<br/> |
| Windowless | Allocatore-unità di sincronizzazione presenterCore<br/>                           | MixerCompositor\*<br/> Allocatore-Presenter<br/> Unità di sincronizzazione principale<br/>                           |
| Renderless | Allocator-Presenter (fornito dall'applicazione) unità di sincronizzazione principale<br/> | MixerCompositor\*<br/> Allocatore-Presenter (fornito dall'applicazione)<br/> Unità di sincronizzazione principale<br/> |



 

\* Indica che l'applicazione dispone dell'opzione per fornire un componente personalizzato o utilizzare il componente predefinito.

In tutte le configurazioni, il punto principale da ricordare quando si creano i grafici di filtro con VMR è che è necessario configurare il VMR prima di connetterlo.

Per tutte le configurazioni, i pin non possono essere aggiunti o rimossi in modo dinamico dopo la connessione di VMR al filtro upstream, ma possono essere connessi e disconnessi. Se l'applicazione non è sicura di quanti pin saranno necessari, è necessario configurare il VMR per il numero massimo che potrebbe essere necessario. La presenza di pin di input non utilizzati sul filtro non comporta un peggioramento delle prestazioni di rendering. A differenza del vecchio mixer sovrapposto, VMR non ha un pin di output perché non richiede un filtro separato per la gestione della finestra.

Le sezioni seguenti descrivono come configurare VMR per una determinata modalità:

-   [Modalità a finestra (compatibilità) VMR](vmr-windowed--compatibility--mode.md)
-   [Modalità senza finestra VMR](vmr-windowless-mode.md)
-   [VMR con più flussi (modalità di combinazione)](vmr-with-multiple-streams--mixing-mode.md)
-   [Modalità di combinazione YUV](yuv-mixing-mode.md)
-   [Posizionamento e trasferimento di rettangoli video nello spazio di composizione](positioning-and-moving-video-rectangles-in-composition-space.md)
-   [Modalità di riproduzione con rendering VMR (allocatore personalizzato-Presenter)](vmr-renderless-playback-mode--custom-allocator-presenters.md)
-   [Modalità esclusiva di DirectDraw](directdraw-exclusive-mode.md)

 

 




