---
description: È possibile modificare i grafici audio in qualsiasi momento per aggiungere o rimuovere voci o interi sottografi.
ms.assetid: b2f9ec6a-4b5b-e618-759b-d7dbc0d97ac4
title: 'Procedura: Aggiungere o rimuovere dinamicamente voci da un grafico audio'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1a49cfc88e89884b63484b7bd58f7f5d96020cd21f8d1147794b840f00258fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082935"
---
# <a name="how-to-dynamically-add-or-remove-voices-from-an-audio-graph"></a>Procedura: Aggiungere o rimuovere dinamicamente voci da un grafico audio

È possibile modificare i grafici audio in qualsiasi momento per aggiungere o rimuovere voci o interi sottografi. Questo argomento illustra come aggiungere o rimuovere voci submix da un grafo creato seguendo la procedura descritta in [Procedura: Compilare](how-to--build-a-basic-audio-processing-graph.md)un'elaborazione audio di base Graph . Una singola voce può inviare l'output a più voci o a una lunga catena di voci. La rimozione o l'aggiunta di una singola voce può avere un effetto di grandi dimensioni su un grafico audio.

## <a name="to-dynamically-change-an-audio-graph"></a>Per modificare dinamicamente un grafico audio

L'aggiunta e la rimozione di voci da un grafo audio è molto simile all'aggiunta o alla rimozione di nodi da un singolo elenco o grafico collegato.

-   Per aggiungere una voce o un sottogramma a un grafico audio

    Impostare l'output di una voce nel grafico, la voce padre, sulla voce da aggiungere usando la [**funzione SetOutputVoices.**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputvoices) Impostare l'output della nuova voce sul figlio originale della voce padre.

    ```
    XAUDIO2_SEND_DESCRIPTOR send = {0, pNewVoice};
    XAUDIO2_VOICE_SENDS sendlist = {1, &send};
    pParentVoice->SetOutputVoices(&sendlist);
    send.pOutputVoice = pChildVoice;
    pNewVoice->SetOutputVoices(&sendlist);
    ```

    

-   Per rimuovere una voce o un sottogramma da un grafico audio

    Impostare la voce di output dell'elemento padre della voce da rimuovere sul figlio della voce da rimuovere. Se la voce rimossa si trova alla fine del grafico, la voce padre deve essere modificata in modo che punti alla voce master.

    ```
    XAUDIO2_SEND_DESCRIPTOR send = {0, pChildVoice};
    XAUDIO2_VOICE_SENDS sendlist = {1, &send};
    pParentVoice->SetOutputVoices(&sendlist);
    ```

    

Si noti che per maggiore chiarezza ogni padre ha un solo elemento figlio in questi esempi. Se un nodo padre ha più elementi figlio, il relativo elenco di invio conterrà una matrice di voci anziché un puntatore a una sola voce.

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

 

 
