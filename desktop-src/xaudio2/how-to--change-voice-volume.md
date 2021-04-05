---
description: In questo argomento viene illustrato come è possibile modificare il volume di una voce a livello generale, a ogni canale di output o tra ogni canale di una voce e un'altra voce nel relativo oggetto Send.
ms.assetid: 40004128-4abb-4bcd-fe76-91276be8abec
title: 'Procedura: modificare il volume vocale'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a307c5585e56fb6dc4dbdc40386c6844607498ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757694"
---
# <a name="how-to-change-voice-volume"></a>Procedura: modificare il volume vocale

In questo argomento viene illustrato come è possibile modificare il volume di una voce a livello generale, a ogni canale di output o tra ogni canale di una voce e un'altra voce nel relativo oggetto [**Send**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends).

## <a name="to-set-an-overall-volume-level-for-the-voices-input"></a>Per impostare un livello di volume complessivo per l'input della voce

-   Utilizzare la funzione [**sevolume**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume) .

    ```
    pSourceVoice->SetVolume(1.0);
    ```

    

## <a name="to-set-the-volume-of-the-voices-output-channels"></a>Per impostare il volume dei canali di output della voce

1.  Creare una matrice di numeri a virgola mobile contenenti i volumi desiderati di tutti i canali di output nella voce.

    La matrice avrà una voce per ogni canale nella voce.

    ```
    float SourceVoiceChannelVolumes[1] = {1.0};
    ```

    

2.  Utilizzare la funzione [**SetChannelVolumes**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setchannelvolumes) per impostare il volume dei canali di output.

    ```
    hr = pSourceVoice->SetChannelVolumes(1,SourceVoiceChannelVolumes);
    ```

    

## <a name="to-set-the-volume-of-connections"></a>Per impostare il volume delle connessioni

Impostare il volume di connessione tra la voce e una voce nel relativo oggetto [**Send**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends).

1.  Creare una matrice di numeri a virgola mobile che definisce una matrice di output se la voce Invia a un'altra voce.

    > [!Note]  
    > La matrice deve contenere un numero di voci uguale ai canali vocali di origine × canali vocali di destinazione. In questo esempio, il mapping viene da una voce con un canale a una voce con due canali.

     

    ```
    float outputMatrix[2] = {1.0f,0.05f};
    ```

    

2.  Utilizzare la funzione [**SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) per impostare la matrice di output.

    ```
    pSourceVoice->SetOutputMatrix(pSubmixVoice,1,2,outputMatrix);
    ```

    

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida alla programmazione di XAudio2](programming-guide.md)
</dt> <dt>

[Procedura: Creare un grafico di elaborazione audio di base](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[Controllo volume e pitch XAudio2](volume-and-pitch-control.md)
</dt> </dl>

 

 
