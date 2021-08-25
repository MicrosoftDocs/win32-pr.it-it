---
description: Questo argomento illustra come aumentare o ridurre il tono dei dati audio modificandone la velocità di riproduzione usando la funzione SetFrequencyRatio su una voce di origine.
ms.assetid: 93408116-1c1f-307f-7e1f-090f2663ff0b
title: 'Procedura: Modificare il tono della voce'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc44fe757c563e3556f760ead594bb619da9f62fb2c3eafc774e15d7b9e5bc85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926471"
---
# <a name="how-to-change-voice-pitch"></a>Procedura: Modificare il tono della voce

Questo argomento illustra come aumentare o ridurre il tono dei dati audio modificandone la velocità di riproduzione usando la [**funzione SetFrequencyRatio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) su una voce di origine.

## <a name="to-change-the-pitch-of-a-source-voice"></a>Per modificare il tono di una voce di origine

1.  Determinare il rapporto di frequenza desiderato per la [**voce di origine**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice).

    Per altre informazioni sul calcolo del rapporto di frequenza, vedere [XAudio2 Volume and Pitch Control (Controllo](xaudio2-volume-and-pitch-control.md) del volume e del passo di XAudio2).

    ```
    float frequencyRatio = sourceRate / targetRate;
    ```

    

2.  Usare la [**funzione SetFrequencyRatio per**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) impostare il rapporto di frequenza della voce di origine.

    ```
    pSourceVoice->SetFrequencyRatio(frequencyRatio);
    ```

    

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida alla programmazione di XAudio2](programming-guide.md)
</dt> <dt>

[Procedura: Creare un grafico di elaborazione audio di base](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[Controllo del volume e del passo XAudio2](volume-and-pitch-control.md)
</dt> </dl>

 

 
