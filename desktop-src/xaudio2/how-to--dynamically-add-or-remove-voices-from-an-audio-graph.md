---
description: È possibile modificare i grafici audio in qualsiasi momento per aggiungere o rimuovere voci o interi sottografici.
ms.assetid: b2f9ec6a-4b5b-e618-759b-d7dbc0d97ac4
title: 'Procedura: Aggiungere o rimuovere dinamicamente voci da un grafico audio'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdb26150b5614ec53e4cc4de5af74e9a14ee2a94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129767"
---
# <a name="how-to-dynamically-add-or-remove-voices-from-an-audio-graph"></a>Procedura: Aggiungere o rimuovere dinamicamente voci da un grafico audio

È possibile modificare i grafici audio in qualsiasi momento per aggiungere o rimuovere voci o interi sottografici. Questo argomento illustra come aggiungere o rimuovere submix Voices da un grafo creato seguendo i passaggi in [procedura: creare un grafico di elaborazione audio di base](how-to--build-a-basic-audio-processing-graph.md). Una singola voce può inviare l'output a diverse voci o a una lungo catena di voci. La rimozione o l'aggiunta di una singola voce può avere un effetto grande su un grafico audio.

## <a name="to-dynamically-change-an-audio-graph"></a>Per modificare dinamicamente un grafico audio

L'aggiunta e la rimozione di voci da un grafo audio è molto simile all'aggiunta o alla rimozione di nodi da un grafico o un elenco collegato a un solo collegamento.

-   Per aggiungere una voce o un sottografico a un grafico audio

    Impostare l'output di una voce nel grafico, ovvero la voce padre, sulla voce da aggiungere tramite la funzione [**SetOutputVoices**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputvoices) . Impostare l'output della nuova voce sull'elemento figlio originale della voce padre.

    ```
    XAUDIO2_SEND_DESCRIPTOR send = {0, pNewVoice};
    XAUDIO2_VOICE_SENDS sendlist = {1, &send};
    pParentVoice->SetOutputVoices(&sendlist);
    send.pOutputVoice = pChildVoice;
    pNewVoice->SetOutputVoices(&sendlist);
    ```

    

-   Per rimuovere una voce o un sottografico da un grafico audio

    Impostare la voce di output dell'elemento padre della voce da rimuovere al figlio della voce da rimuovere. Se la voce da rimuovere si trova alla fine del grafico, è necessario modificare la voce padre in modo che punti alla voce Master.

    ```
    XAUDIO2_SEND_DESCRIPTOR send = {0, pChildVoice};
    XAUDIO2_VOICE_SENDS sendlist = {1, &send};
    pParentVoice->SetOutputVoices(&sendlist);
    ```

    

Si noti che per chiarezza ogni elemento padre ha solo un elemento figlio in questi esempi. Se un nodo padre ha più elementi figlio, il relativo oggetto Send includerà una matrice di voci anziché un puntatore a una sola voce.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Grafici audio](audio-graphs.md)
</dt> <dt>

[Guida alla programmazione di XAudio2](programming-guide.md)
</dt> <dt>

[Procedura: Creare un grafico di elaborazione audio di base](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[Procedura: Usare voci di missaggio secondario](how-to--use-submix-voices.md)
</dt> <dt>

[Procedura: Creare una catena di effetti](how-to--create-an-effect-chain.md)
</dt> </dl>

 

 
