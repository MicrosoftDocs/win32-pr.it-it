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
# <a name="how-to-change-voice-pitch"></a><span data-ttu-id="31ed1-103">Procedura: modificare il pitch vocale</span><span class="sxs-lookup"><span data-stu-id="31ed1-103">How to: Change Voice Pitch</span></span>

<span data-ttu-id="31ed1-104">In questo argomento viene illustrato come aumentare o ridurre il pitch dei dati audio modificando la velocità di riproduzione usando la funzione [**SetFrequencyRatio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) in una voce di origine.</span><span class="sxs-lookup"><span data-stu-id="31ed1-104">This topic shows you how you can raise or lower the pitch of audio data by changing its rate of playback using the [**SetFrequencyRatio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) function on a source voice.</span></span>

## <a name="to-change-the-pitch-of-a-source-voice"></a><span data-ttu-id="31ed1-105">Per modificare il passo di una voce di origine</span><span class="sxs-lookup"><span data-stu-id="31ed1-105">To change the pitch of a source voice</span></span>

1.  <span data-ttu-id="31ed1-106">Determinare il rapporto di frequenza desiderato per la [**voce di origine**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice).</span><span class="sxs-lookup"><span data-stu-id="31ed1-106">Determine the desired frequency ratio for the [**source voice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice).</span></span>

    <span data-ttu-id="31ed1-107">Per altre informazioni sul calcolo del rapporto di frequenza, vedere [controllo volume e pitch XAudio2](xaudio2-volume-and-pitch-control.md) .</span><span class="sxs-lookup"><span data-stu-id="31ed1-107">See [XAudio2 Volume and Pitch Control](xaudio2-volume-and-pitch-control.md) for more information about calculating the frequency ratio.</span></span>

    ```
    float frequencyRatio = sourceRate / targetRate;
    ```

    

2.  <span data-ttu-id="31ed1-108">Utilizzare la funzione [**SetFrequencyRatio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) per impostare il rapporto di frequenza della voce di origine.</span><span class="sxs-lookup"><span data-stu-id="31ed1-108">Use the [**SetFrequencyRatio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) function to set the frequency ratio of the source voice.</span></span>

    ```
    pSourceVoice->SetFrequencyRatio(frequencyRatio);
    ```

    

## <a name="related-topics"></a><span data-ttu-id="31ed1-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="31ed1-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="31ed1-110">Guida alla programmazione di XAudio2</span><span class="sxs-lookup"><span data-stu-id="31ed1-110">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="31ed1-111">Procedura: Creare un grafico di elaborazione audio di base</span><span class="sxs-lookup"><span data-stu-id="31ed1-111">How to: Build a Basic Audio Processing Graph</span></span>](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[<span data-ttu-id="31ed1-112">Controllo volume e pitch XAudio2</span><span class="sxs-lookup"><span data-stu-id="31ed1-112">XAudio2 Volume and Pitch Control</span></span>](volume-and-pitch-control.md)
</dt> </dl>

 

 
