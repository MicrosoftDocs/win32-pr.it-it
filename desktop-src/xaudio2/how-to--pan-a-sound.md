---
description: In questo argomento viene illustrato come è possibile impostare la matrice di output di una voce di origine mono che restituisce una voce master stereo per ottenere una panoramica tra gli altoparlanti sinistro e destro.
ms.assetid: d87db173-6de0-09eb-7767-df619c88acfd
title: 'Procedura: eseguire il panning di un suono'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4136d6e30cba1e6b0bc669fef5518d2a56f868f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883126"
---
# <a name="how-to-pan-a-sound"></a><span data-ttu-id="1fce1-103">Procedura: eseguire il panning di un suono</span><span class="sxs-lookup"><span data-stu-id="1fce1-103">How to: Pan a Sound</span></span>

<span data-ttu-id="1fce1-104">In questo argomento viene illustrato come è possibile impostare la matrice di output di una voce di origine mono che restituisce una voce master stereo per ottenere una panoramica tra gli altoparlanti sinistro e destro.</span><span class="sxs-lookup"><span data-stu-id="1fce1-104">This topic shows you how you can set the output matrix of a mono source voice that outputs to a stereo mastering voice in order to achieve panning between the left and right speakers.</span></span>

## <a name="to-setup-panning"></a><span data-ttu-id="1fce1-105">Per configurare la panoramica</span><span class="sxs-lookup"><span data-stu-id="1fce1-105">To setup panning</span></span>

1.  <span data-ttu-id="1fce1-106">Recuperare la configurazione dell'altoparlante utilizzando [**IXAudio2MasteringVoice:: GetChannelMask**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2masteringvoice-getchannelmask).</span><span class="sxs-lookup"><span data-stu-id="1fce1-106">Retrieve the speaker configuration using [**IXAudio2MasteringVoice::GetChannelMask**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2masteringvoice-getchannelmask).</span></span>

    ```
    DWORD dwChannelMask;       
    pMasteringVoice->GetChannelMask( &dwChannelMask );       
    ```

    

2.  <span data-ttu-id="1fce1-107">Creare una matrice che contenga la matrice di output.</span><span class="sxs-lookup"><span data-stu-id="1fce1-107">Create an array to hold the output matrix.</span></span> <span data-ttu-id="1fce1-108">La dimensione minima della matrice di output corrisponde al numero di canali nella voce di origine per il numero di canali nella voce di output.</span><span class="sxs-lookup"><span data-stu-id="1fce1-108">The minimum size of the output matrix is the number of channels in the source voice times the number of channels in the output voice.</span></span> <span data-ttu-id="1fce1-109">In questo caso, un array di otto elementi gestirà un output mono Voice in qualsiasi formato di output fino a 7,1 audio surround.</span><span class="sxs-lookup"><span data-stu-id="1fce1-109">In this case an eight element array will handle a mono voice outputting to any output format up to 7.1 surround sound.</span></span>

    ```
    float outputMatrix[ 8 ];
    for (int i=0; i<8; i++) outputMatrix[i] = 0;
    ```

    

3.  <span data-ttu-id="1fce1-110">Calcolare i livelli di trasmissione in base alla panoramica desiderata tra gli altoparlanti sinistro e destro.</span><span class="sxs-lookup"><span data-stu-id="1fce1-110">Calculate the send levels based on the desired panning between the left and right speakers.</span></span> <span data-ttu-id="1fce1-111">In questo esempio, i valori di Pan variano da-1 a 1 con-1 che indica tutto il suono a sinistra e 1 indica tutti i suoni nell'altoparlante destro.</span><span class="sxs-lookup"><span data-stu-id="1fce1-111">In this example, pan values will range from -1 to 1 with -1 indicating all sound to the left speaker and 1 indicating all sound to the right speaker.</span></span>

    ```
    // pan of -1.0 indicates all left speaker, 
    // 1.0 is all right speaker, 0.0 is split between left and right
    float left = 0.5f - pan / 2;
    float right = 0.5f + pan / 2; 
    ```

    

4.  <span data-ttu-id="1fce1-112">Impostare gli indici della matrice di output corrispondenti agli altoparlanti sinistro e destro con i valori calcolati nel passaggio precedente.</span><span class="sxs-lookup"><span data-stu-id="1fce1-112">Set the output matrix indices corresponding to the left and right speakers with the values calculated in the previous step.</span></span> <span data-ttu-id="1fce1-113">Gli altoparlanti sinistro e destro vengono determinati osservando la maschera di canale restituita da [**IXAudio2MasteringVoice:: GetChannelMask**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2masteringvoice-getchannelmask).</span><span class="sxs-lookup"><span data-stu-id="1fce1-113">The left and right speakers are determined by looking at the channel mask returned by [**IXAudio2MasteringVoice::GetChannelMask**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2masteringvoice-getchannelmask).</span></span> <span data-ttu-id="1fce1-114">Poiché i canali devono sempre essere codificati nell'ordine specificato nella pagina di riferimento [**WAVEFORMATEXTENSIBLE**](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-waveformatextensible) , è possibile determinare l'indice della matrice corrispondente a un singolo altoparlante.</span><span class="sxs-lookup"><span data-stu-id="1fce1-114">Since the channels must always be encoded in the order specified on the [**WAVEFORMATEXTENSIBLE**](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-waveformatextensible) reference page, it is possible to determine the array index corresponding to an individual speaker.</span></span>

    ```
    switch (dwChannelMask)
    {
    case SPEAKER_MONO:
        outputMatrix[0] = 1.0;
        break;
    case SPEAKER_STEREO:
    case SPEAKER_2POINT1:
    case SPEAKER_SURROUND:
        outputMatrix[0] = left;
        outputMatrix[1] = right;
        break;
    case SPEAKER_QUAD:
        outputMatrix[0] = outputMatrix[2] = left;
        outputMatrix[1] = outputMatrix[3] = right;
        break;
    case SPEAKER_4POINT1:
        outputMatrix[ 0 ] = outputMatrix[ 3 ] = left;
        outputMatrix[ 1 ] = outputMatrix[ 4 ] = right;
        break;
    case SPEAKER_5POINT1:
    case SPEAKER_7POINT1:
    case SPEAKER_5POINT1_SURROUND:
        outputMatrix[ 0 ] = outputMatrix[ 4 ] = left;
        outputMatrix[ 1 ] = outputMatrix[ 5 ] = right;
        break;
    case SPEAKER_7POINT1_SURROUND:
        outputMatrix[ 0 ] = outputMatrix[ 4 ] = outputMatrix[ 6 ] = left;
        outputMatrix[ 1 ] = outputMatrix[ 5 ] = outputMatrix[ 7 ] = right;
        break;
    }
    ```

    

5.  <span data-ttu-id="1fce1-115">Applicare la matrice di output alla voce di origine usando [**IXAudio2Voice:: SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix).</span><span class="sxs-lookup"><span data-stu-id="1fce1-115">Apply the output matrix to the originating voice by using [**IXAudio2Voice::SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix).</span></span> <span data-ttu-id="1fce1-116">La voce di origine sarà una voce di origine o un submix Voice invio a una voce submix o a una voce Master.</span><span class="sxs-lookup"><span data-stu-id="1fce1-116">The originating voice will be either a source voice or a submix voice sending to either a submix voice or a mastering voice.</span></span> <span data-ttu-id="1fce1-117">È possibile ottenere informazioni sulle voci di origine e di destinazione, ad esempio il numero di canali, usando [**IXAudio2Voice:: GetVoiceDetails**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-getvoicedetails).</span><span class="sxs-lookup"><span data-stu-id="1fce1-117">You can get info about the originating and destination voices, like their number of channels, by using [**IXAudio2Voice::GetVoiceDetails**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-getvoicedetails).</span></span>

    ```
    // Assuming pVoice sends to pMasteringVoice

    XAUDIO2_VOICE_DETAILS VoiceDetails;
    pVoice->GetVoiceDetails(&VoiceDetails);

    XAUDIO2_VOICE_DETAILS MasterVoiceDetails;
    pMasteringVoice->GetVoiceDetails(&MasterVoiceDetails);

    pVoice->SetOutputMatrix( NULL, VoiceDetails.InputChannels, MasterVoiceDetails.InputChannels, outputMatrix );
    ```

    

## <a name="related-topics"></a><span data-ttu-id="1fce1-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1fce1-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1fce1-119">Guida alla programmazione di XAudio2</span><span class="sxs-lookup"><span data-stu-id="1fce1-119">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="1fce1-120">Procedura: Creare un grafico di elaborazione audio di base</span><span class="sxs-lookup"><span data-stu-id="1fce1-120">How to: Build a Basic Audio Processing Graph</span></span>](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[<span data-ttu-id="1fce1-121">Controllo volume e pitch XAudio2</span><span class="sxs-lookup"><span data-stu-id="1fce1-121">XAudio2 Volume and Pitch Control</span></span>](volume-and-pitch-control.md)
</dt> </dl>

 

 
