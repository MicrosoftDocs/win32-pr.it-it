---
description: In questo argomento viene illustrato come è possibile impostare gruppi di voci per inviare l'output alla stessa voce submix. Ciò consente a una singola modifica a una voce di submix di influire su un intero gruppo di voci.
ms.assetid: 76c1c138-4846-9c4f-7875-446867436ee9
title: 'Procedura: Usare voci di missaggio secondario'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7152c3224d6528ac52651f2ca2f433631b347c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232294"
---
# <a name="how-to-use-submix-voices"></a><span data-ttu-id="52ecb-104">Procedura: Usare voci di missaggio secondario</span><span class="sxs-lookup"><span data-stu-id="52ecb-104">How to: Use Submix Voices</span></span>

<span data-ttu-id="52ecb-105">In questo argomento viene illustrato come è possibile impostare gruppi di voci per inviare l'output alla stessa voce submix.</span><span class="sxs-lookup"><span data-stu-id="52ecb-105">This topic shows you how you can set groups of voices to send their output to the same submix voice.</span></span> <span data-ttu-id="52ecb-106">Ciò consente a una singola modifica a una voce di submix di influire su un intero gruppo di voci.</span><span class="sxs-lookup"><span data-stu-id="52ecb-106">This enables a single change to a submix voice to affect a whole group of voices.</span></span>

1.  <span data-ttu-id="52ecb-107">Creare una [**voce submix**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice) a cui tutte le voci di effetto audio del gioco invieranno.</span><span class="sxs-lookup"><span data-stu-id="52ecb-107">Create a [**submix voice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice) to which all of the game's sound effect voices will send.</span></span>
    ```
    IXAudio2SubmixVoice * pSFXSubmixVoice;
    pXAudio2->CreateSubmixVoice(&pSFXSubmixVoice,1,44100,0,0,0,0);
    ```

    

2.  <span data-ttu-id="52ecb-108">Creare una struttura [**XAUDIO2 \_ Voice \_ Send**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends) che contiene un riferimento alla voce submix.</span><span class="sxs-lookup"><span data-stu-id="52ecb-108">Create an [**XAUDIO2\_VOICE\_SENDS**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends) structure that contains a reference to the submix voice.</span></span>
    ```
    XAUDIO2_SEND_DESCRIPTOR SFXSend = {0, pSFXSubmixVoice};
    XAUDIO2_VOICE_SENDS SFXSendList = {1, &SFXSend};
    ```

    

3.  <span data-ttu-id="52ecb-109">Passare la struttura [**XAUDIO2 \_ Voice \_ Send**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends) a nuove voci di origine man mano che vengono create.</span><span class="sxs-lookup"><span data-stu-id="52ecb-109">Pass the [**XAUDIO2\_VOICE\_SENDS**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends) structure to new source voices as they are created.</span></span>
    ```
    IXAudio2SourceVoice* pSFXSourceVoice;
    if( FAILED(hr = pXaudio2->CreateSourceVoice( &pSFXSourceVoice, (WAVEFORMATEX*)&wfx,
        0, XAUDIO2_DEFAULT_FREQ_RATIO, pCallback, pSFXSendList, NULL ) ) )
        return hr;
    ```

    

4.  <span data-ttu-id="52ecb-110">Applicare le modifiche a tutte le voci di effetto acustico modificando la voce submix.</span><span class="sxs-lookup"><span data-stu-id="52ecb-110">Apply changes to all sound effect voices by adjusting the submix voice.</span></span>

    <span data-ttu-id="52ecb-111">In questo esempio, la modifica del volume della voce submix con la funzione [**sevolume**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume) modifica in modo efficace il volume di tutte le voci che lo restituiscono.</span><span class="sxs-lookup"><span data-stu-id="52ecb-111">In this example, changing the volume of the submix voice with the [**SetVolume**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume) function effectively changes the volume of all voices that output to it.</span></span>

    ```
    pSFXSubmixVoice->SetVolume(0.1);
    ```

    

## <a name="related-topics"></a><span data-ttu-id="52ecb-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="52ecb-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52ecb-113">Voci</span><span class="sxs-lookup"><span data-stu-id="52ecb-113">Voices</span></span>](voices.md)
</dt> <dt>

[<span data-ttu-id="52ecb-114">Guida alla programmazione di XAudio2</span><span class="sxs-lookup"><span data-stu-id="52ecb-114">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="52ecb-115">Procedura: Creare un grafico di elaborazione audio di base</span><span class="sxs-lookup"><span data-stu-id="52ecb-115">How to: Build a Basic Audio Processing Graph</span></span>](how-to--build-a-basic-audio-processing-graph.md)
</dt> </dl>

 

 
