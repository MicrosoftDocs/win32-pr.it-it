---
description: Il requisito minimo per consentire a XAudio2 di riprodurre dati audio è un grafico di elaborazione audio, creato da una singola voce di master e da un'unica voce di origine.
ms.assetid: 40f79959-23c9-4513-363b-2f2fc85e4c0a
title: 'Procedura: Creare un grafico di elaborazione audio di base'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43a11601514e3bcad5536ed1a8599178bcc52aa0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314416"
---
# <a name="how-to-build-a-basic-audio-processing-graph"></a><span data-ttu-id="e4560-103">Procedura: Creare un grafico di elaborazione audio di base</span><span class="sxs-lookup"><span data-stu-id="e4560-103">How to: Build a Basic Audio Processing Graph</span></span>

<span data-ttu-id="e4560-104">Il requisito minimo per consentire a XAudio2 di riprodurre dati audio è un grafico di elaborazione audio, creato da una singola voce di master e da un'unica voce di origine.</span><span class="sxs-lookup"><span data-stu-id="e4560-104">The minimum requirement for enabling XAudio2 to play audio data is an audio processing graph, which is constructed from a single mastering voice and a single source voice.</span></span>

## <a name="to-build-a-basic-audio-processing-graph"></a><span data-ttu-id="e4560-105">Per creare un grafico di elaborazione audio di base</span><span class="sxs-lookup"><span data-stu-id="e4560-105">To build a basic audio processing graph</span></span>

1.  <span data-ttu-id="e4560-106">Inizializzare il motore XAudio2 seguendo i passaggi descritti in [procedura: inizializzare XAudio2](how-to--initialize-xaudio2.md).</span><span class="sxs-lookup"><span data-stu-id="e4560-106">Initialize the XAudio2 engine by following the steps described in [How to: Initialize XAudio2](how-to--initialize-xaudio2.md).</span></span>
2.  <span data-ttu-id="e4560-107">Popolare una struttura del [**\_ buffer**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) **WAVEFORMATEX** e XAUDIO2 attenendosi alla procedura descritta in [procedura: caricare file di dati audio in XAUDIO2](how-to--load-audio-data-files-in-xaudio2.md).</span><span class="sxs-lookup"><span data-stu-id="e4560-107">Populate a **WAVEFORMATEX** and [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) structure by following the steps described in [How to: Load Audio Data Files in XAudio2](how-to--load-audio-data-files-in-xaudio2.md).</span></span>
3.  <span data-ttu-id="e4560-108">Creare una voce di origine usando la funzione [**CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) .</span><span class="sxs-lookup"><span data-stu-id="e4560-108">Create a source voice using the [**CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) function.</span></span>

    <span data-ttu-id="e4560-109">Quando si specifica NULL per l'argomento pSendList di [**CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice), l'output della voce di origine passa alla voce mastering creata nel passaggio 1.</span><span class="sxs-lookup"><span data-stu-id="e4560-109">When you specify NULL for the pSendList argument of [**CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice), the source voice's output goes to the mastering voice created in step 1.</span></span>

    ```
    IXAudio2SourceVoice* pSourceVoice;
    if( FAILED(hr = pXAudio2->CreateSourceVoice( &pSourceVoice, (WAVEFORMATEX*)&wfx,
                  0, XAUDIO2_DEFAULT_FREQ_RATIO, NULL, NULL, NULL ) ) ) return hr;
    ```

    

    <span data-ttu-id="e4560-110">Al termine di questo passaggio, è disponibile un semplice grafico audio costituito dalla voce di origine, dalla voce Master e dal dispositivo audio.</span><span class="sxs-lookup"><span data-stu-id="e4560-110">After you finish this step, there is a simple audio graph consisting of the source voice, the mastering voice, and the audio device.</span></span> <span data-ttu-id="e4560-111">I passaggi rimanenti di questo argomento illustrano come avviare il flusso di dati audio attraverso il grafo.</span><span class="sxs-lookup"><span data-stu-id="e4560-111">The remaining steps in this how-to topic show you how to start audio data flowing through the graph.</span></span>

    <span data-ttu-id="e4560-112">Un semplice grafico audio</span><span class="sxs-lookup"><span data-stu-id="e4560-112">A simple audio graph</span></span>

    ![un semplice grafico audio.](images/xaudio2-audio-graph.png)

4.  <span data-ttu-id="e4560-114">Usare la funzione [**SubmitSourceBuffer**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-submitsourcebuffer) per inviare un [**\_ buffer XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) alla voce di origine.</span><span class="sxs-lookup"><span data-stu-id="e4560-114">Use the function [**SubmitSourceBuffer**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-submitsourcebuffer) to submit an [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) to the source voice.</span></span>

    ```
    if( FAILED(hr = pSourceVoice->SubmitSourceBuffer( &buffer ) ) )
        return hr;
    ```

    

5.  <span data-ttu-id="e4560-115">Usare la funzione [**Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) per avviare la voce di origine.</span><span class="sxs-lookup"><span data-stu-id="e4560-115">Use the [**Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) function to start the source voice.</span></span>

    ```
    if ( FAILED(hr = pSourceVoice->Start( 0, XAUDIO2_COMMIT_NOW ) ) )
        return hr;
    ```

    

## <a name="related-topics"></a><span data-ttu-id="e4560-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e4560-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4560-117">Grafici audio</span><span class="sxs-lookup"><span data-stu-id="e4560-117">Audio Graphs</span></span>](audio-graphs.md)
</dt> <dt>

[<span data-ttu-id="e4560-118">Guida alla programmazione di XAudio2</span><span class="sxs-lookup"><span data-stu-id="e4560-118">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> </dl>

 

 
