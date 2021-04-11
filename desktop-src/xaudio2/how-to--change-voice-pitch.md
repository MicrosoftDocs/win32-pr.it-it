---
description: In questo argomento viene illustrato come aumentare o ridurre il pitch dei dati audio modificando la velocità di riproduzione usando la funzione SetFrequencyRatio in una voce di origine.
ms.assetid: 93408116-1c1f-307f-7e1f-090f2663ff0b
title: 'Procedura: modificare il pitch vocale'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7143dda30eae48bd8ed966c4170da2884d2633ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129771"
---
# <a name="how-to-change-voice-pitch"></a>Procedura: modificare il pitch vocale

In questo argomento viene illustrato come aumentare o ridurre il pitch dei dati audio modificando la velocità di riproduzione usando la funzione [**SetFrequencyRatio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) in una voce di origine.

## <a name="to-change-the-pitch-of-a-source-voice"></a>Per modificare il passo di una voce di origine

1.  Determinare il rapporto di frequenza desiderato per la [**voce di origine**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice).

    Per altre informazioni sul calcolo del rapporto di frequenza, vedere [controllo volume e pitch XAudio2](xaudio2-volume-and-pitch-control.md) .

    ```
    float frequencyRatio = sourceRate / targetRate;
    ```

    

2.  Utilizzare la funzione [**SetFrequencyRatio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) per impostare il rapporto di frequenza della voce di origine.

    ```
    pSourceVoice->SetFrequencyRatio(frequencyRatio);
    ```

    

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida alla programmazione di XAudio2](programming-guide.md)
</dt> <dt>

[Procedura: Creare un grafico di elaborazione audio di base](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[Controllo volume e pitch XAudio2](volume-and-pitch-control.md)
</dt> </dl>

 

 
