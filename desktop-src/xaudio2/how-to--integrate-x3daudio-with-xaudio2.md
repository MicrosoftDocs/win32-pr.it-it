---
description: In questo argomento viene illustrato come integrare X3DAudio con XAudio2.
ms.assetid: a8f41f0d-b284-aefa-923b-471b13b4a3ec
title: 'Procedura: Integrare X3DAudio con XAudio2'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dc54fa5f673e319712808ca6d2b587b8ad2d0fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757691"
---
# <a name="how-to-integrate-x3daudio-with-xaudio2"></a><span data-ttu-id="ccfa3-103">Procedura: Integrare X3DAudio con XAudio2</span><span class="sxs-lookup"><span data-stu-id="ccfa3-103">How to: Integrate X3DAudio with XAudio2</span></span>

<span data-ttu-id="ccfa3-104">In questo argomento viene illustrato come integrare X3DAudio con XAudio2.</span><span class="sxs-lookup"><span data-stu-id="ccfa3-104">This topic shows how to integrate X3DAudio with XAudio2.</span></span> <span data-ttu-id="ccfa3-105">È possibile usare X3DAudio per fornire i valori volume e pitch per le voci XAudio2 e i parametri per l'effetto XAudio2 incorporato.</span><span class="sxs-lookup"><span data-stu-id="ccfa3-105">You can use X3DAudio to provide the volume and pitch values for XAudio2 voices and the parameters for the XAudio2 built in reverb effect.</span></span> <span data-ttu-id="ccfa3-106">In questo argomento si presuppone che sia stato creato un grafico audio come descritto in [procedura: creare un grafico di elaborazione audio di base](how-to--build-a-basic-audio-processing-graph.md).</span><span class="sxs-lookup"><span data-stu-id="ccfa3-106">This topic assumes that you have created an audio graph as described in [How to: Build a Basic Audio Processing Graph](how-to--build-a-basic-audio-processing-graph.md).</span></span> <span data-ttu-id="ccfa3-107">Se non è già stato creato un grafico audio, [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize) avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="ccfa3-107">If you have not already created an audio graph, [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize) will fail.</span></span>

<span data-ttu-id="ccfa3-108">**Per inizializzare X3DAudio**</span><span class="sxs-lookup"><span data-stu-id="ccfa3-108">**To initialize X3DAudio**</span></span>

1.  <span data-ttu-id="ccfa3-109">Inizializzare X3DAudio chiamando [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize).</span><span class="sxs-lookup"><span data-stu-id="ccfa3-109">Initialize X3DAudio by calling [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize).</span></span>

    <span data-ttu-id="ccfa3-110">La funzione [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize) accetta flag che indicano la configurazione del relatore, la velocità del suono nelle unità internazionali definite dall'utente al secondo e un handle per restituire un'istanza del motore X3DAudio.</span><span class="sxs-lookup"><span data-stu-id="ccfa3-110">The [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize) function takes flags indicating the speaker setup, the speed of sound in user-defined world units per second, and a handle to return an instance of the X3DAudio engine.</span></span> <span data-ttu-id="ccfa3-111">Chiamare [**IXAudio2MasteringVoice:: GetChannelMask**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2masteringvoice-getchannelmask) per ottenere la maschera di canale del formato di output.</span><span class="sxs-lookup"><span data-stu-id="ccfa3-111">Call [**IXAudio2MasteringVoice::GetChannelMask**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2masteringvoice-getchannelmask) to get the output format's channel mask.</span></span>

    ```
    DWORD dwChannelMask;       
    pMasteringVoice->GetChannelMask( &dwChannelMask );       

    X3DAUDIO_HANDLE X3DInstance;
    X3DAudioInitialize( dwChannelMask, X3DAUDIO_SPEED_OF_SOUND, X3DInstance );
    ```

    

2.  <span data-ttu-id="ccfa3-112">Creare istanze del [**\_ listener X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) e delle strutture di [**\_ emettitore X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) .</span><span class="sxs-lookup"><span data-stu-id="ccfa3-112">Create instances of the [**X3DAUDIO\_LISTENER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) and [**X3DAUDIO\_EMITTER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) structures.</span></span>

    <span data-ttu-id="ccfa3-113">La struttura del [**\_ listener X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) rappresenta la posizione in cui viene udito il suono.</span><span class="sxs-lookup"><span data-stu-id="ccfa3-113">The [**X3DAUDIO\_LISTENER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) structure represents the position of whatever is hearing the sound.</span></span> <span data-ttu-id="ccfa3-114">In genere, si tratta della posizione della fotocamera o di una posizione vicina.</span><span class="sxs-lookup"><span data-stu-id="ccfa3-114">Generally, this is the position of the camera or a position close to it.</span></span> <span data-ttu-id="ccfa3-115">La struttura dell' [**\_ emettitore X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) rappresenta la posizione dell'elemento che crea il suono.</span><span class="sxs-lookup"><span data-stu-id="ccfa3-115">The [**X3DAUDIO\_EMITTER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) structure represents the position of the thing making the sound.</span></span> <span data-ttu-id="ccfa3-116">Ci sarà una struttura **di \_ emettitore X3DAUDIO** per ogni suono rilevato.</span><span class="sxs-lookup"><span data-stu-id="ccfa3-116">There will be one **X3DAUDIO\_EMITTER** structure for each sound that is being tracked.</span></span>

    <span data-ttu-id="ccfa3-117">I membri delle strutture che non verranno aggiornati in un ciclo di gioco devono essere inizializzati qui.</span><span class="sxs-lookup"><span data-stu-id="ccfa3-117">Members of the structures that will not be updated in a game loop should be initialized here.</span></span> <span data-ttu-id="ccfa3-118">La maggior parte dei membri delle strutture può semplicemente essere inizializzata su zero.</span><span class="sxs-lookup"><span data-stu-id="ccfa3-118">Most members of the structures can simply be initialized to zero.</span></span> <span data-ttu-id="ccfa3-119">Tuttavia, alcuni membri di [**X3DAUDIO \_ emittor**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) devono essere impostati in modo da essere inizializzati su valori diversi da zero.</span><span class="sxs-lookup"><span data-stu-id="ccfa3-119">However, some members of [**X3DAUDIO\_EMITTER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) need to be set to be initialized to non-zero values.</span></span> <span data-ttu-id="ccfa3-120">Il membro ChannelCount dell' **\_ emettitore X3DAUDIO** deve essere inizializzato sul numero di canali nella voce rappresentata dall'emittente.</span><span class="sxs-lookup"><span data-stu-id="ccfa3-120">The ChannelCount member of the **X3DAUDIO\_EMITTER** needs to be initialized to the number of channels in the voice the emitter represents.</span></span> <span data-ttu-id="ccfa3-121">Inoltre, il membro CurveDistanceScaler di **X3DAUDIO \_ emittor** deve essere compreso nell'intervallo \_ da FLT min a flt \_ max.</span><span class="sxs-lookup"><span data-stu-id="ccfa3-121">Also, the CurveDistanceScaler member of **X3DAUDIO\_EMITTER** must be in the range FLT\_MIN to FLT\_MAX.</span></span>

    ```
    X3DAUDIO_LISTENER Listener = {0};
    X3DAUDIO_EMITTER Emitter = {0};
    Emitter.ChannelCount = 1;
    Emitter.CurveDistanceScaler = FLT_MIN;
    ```

    

3.  <span data-ttu-id="ccfa3-122">Creare un'istanza della struttura [**delle \_ \_ impostazioni di X3DAUDIO DSP**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings) .</span><span class="sxs-lookup"><span data-stu-id="ccfa3-122">Create an instance of the [**X3DAUDIO\_DSP\_SETTINGS**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings) structure.</span></span>

    <span data-ttu-id="ccfa3-123">La [**struttura \_ \_ delle impostazioni di X3DAUDIO DSP**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings) viene utilizzata per restituire i risultati calcolati da [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate).</span><span class="sxs-lookup"><span data-stu-id="ccfa3-123">The [**X3DAUDIO\_DSP\_SETTINGS**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings) structure is used to return results calculated by [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate).</span></span> <span data-ttu-id="ccfa3-124">La funzione **X3DAudioCalculate** non alloca memoria per alcun parametro.</span><span class="sxs-lookup"><span data-stu-id="ccfa3-124">The **X3DAudioCalculate** function does not allocate memory for any of its parameters.</span></span> <span data-ttu-id="ccfa3-125">Ciò significa che è necessario allocare matrici per i membri pMatrixCoefficients e pDelayTimes della struttura **\_ \_ delle impostazioni DSP X3DAUDIO** se si intende usarli.</span><span class="sxs-lookup"><span data-stu-id="ccfa3-125">This means that you need to allocate arrays for the **X3DAUDIO\_DSP\_SETTINGS** structure's pMatrixCoefficients and pDelayTimes members if you intend to use them.</span></span> <span data-ttu-id="ccfa3-126">Inoltre, è necessario impostare i membri SrcChannelCount e DstChannelCount sul numero di canali nelle voci di origine e di destinazione del emettitore.</span><span class="sxs-lookup"><span data-stu-id="ccfa3-126">In addition, you need to set the SrcChannelCount and DstChannelCount members to the number of channels in the emitter's source and destination voices.</span></span>

    ```
    X3DAUDIO_DSP_SETTINGS DSPSettings = {0};
    FLOAT32 * matrix = new FLOAT32[deviceDetails.OutputFormat.Format.nChannels];
    DSPSettings.SrcChannelCount = 1;
    DSPSettings.DstChannelCount = deviceDetails.OutputFormat.Format.nChannels;
    DSPSettings.pMatrixCoefficients = matrix;
    ```

    

    > [!Note]  
    > <span data-ttu-id="ccfa3-127">Usare [**IXAudio2Voice:: GetVoiceDetails**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-getvoicedetails) nella voce mastering per ottenere il numero di InputChannels per **nChannels**.</span><span class="sxs-lookup"><span data-stu-id="ccfa3-127">Use [**IXAudio2Voice::GetVoiceDetails**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-getvoicedetails) on the mastering voice to obtain the number of InputChannels for **nChannels**.</span></span> <span data-ttu-id="ccfa3-128">Per le versioni di XAUDIO2 di DirectX SDK precedenti a Windows 8, usare IXAudio2:: GetDeviceDetails.</span><span class="sxs-lookup"><span data-stu-id="ccfa3-128">For DirectX SDK versions of XAUDIO2 prior to Windows 8, use IXAudio2::GetDeviceDetails.</span></span>

     

<span data-ttu-id="ccfa3-129">Eseguire questi passaggi una volta ogni due o tre fotogrammi per calcolare le nuove impostazioni e applicarle.</span><span class="sxs-lookup"><span data-stu-id="ccfa3-129">Perform these steps once every two to three frames to calculate new settings and apply them.</span></span> <span data-ttu-id="ccfa3-130">In questo esempio, una voce di origine invia direttamente alla voce mastering e a una voce submix con un effetto di riverbero applicato.</span><span class="sxs-lookup"><span data-stu-id="ccfa3-130">In this example, a source voice is sending directly to the mastering voice and to a submix voice with a reverb effect applied to it.</span></span>

<span data-ttu-id="ccfa3-131">**Per usare X3DAudio per calcolare e applicare nuove impostazioni audio 3D**</span><span class="sxs-lookup"><span data-stu-id="ccfa3-131">**To use X3DAudio to calculate and apply new 3D audio settings**</span></span>

1.  <span data-ttu-id="ccfa3-132">Aggiornare le [**strutture \_ listener X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) e [**\_ emittor X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) con la posizione, la velocità e l'orientamento correnti.</span><span class="sxs-lookup"><span data-stu-id="ccfa3-132">Update the [**X3DAUDIO\_LISTENER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) and [**X3DAUDIO\_EMITTER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) structures with their current position, velocity, and orientation.</span></span>

    ```
    Emitter.OrientFront = EmitterOrientFront;
    Emitter.OrientTop = EmitterOrientTop;
    Emitter.Position = EmitterPosition;
    Emitter.Velocity = EmitterVelocity;
    Listener.OrientFront = ListenerOrientFront;
    Listener.OrientTop = ListenerOrientTop;
    Listener.Position = ListenerPosition;
    Listener.Velocity = ListenerVelocity;
    ```

    

2.  <span data-ttu-id="ccfa3-133">Chiamare [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate) per calcolare le nuove impostazioni per le voci.</span><span class="sxs-lookup"><span data-stu-id="ccfa3-133">Call [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate) to calculate new settings for the voices.</span></span>

    <span data-ttu-id="ccfa3-134">I parametri per [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate) saranno il [**\_ listener X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) aggiornato e le strutture di [**\_ emissione X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) .</span><span class="sxs-lookup"><span data-stu-id="ccfa3-134">The parameters for [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate) will be the updated [**X3DAUDIO\_LISTENER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) and [**X3DAUDIO\_EMITTER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) structures.</span></span> <span data-ttu-id="ccfa3-135">I flag indicheranno i valori che **X3DAudioCalculate** deve calcolare e la [**struttura \_ \_ delle impostazioni DSP X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings) che conterrà i risultati dei calcoli eseguiti.</span><span class="sxs-lookup"><span data-stu-id="ccfa3-135">The flags will indicate what values **X3DAudioCalculate** should calculate, and which [**X3DAUDIO\_DSP\_SETTINGS**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings) structure will hold the results of the calculations performed.</span></span>

    ```
    X3DAudioCalculate(X3DInstance, &Listener, &Emitter,
        X3DAUDIO_CALCULATE_MATRIX | X3DAUDIO_CALCULATE_DOPPLER | X3DAUDIO_CALCULATE_LPF_DIRECT | X3DAUDIO_CALCULATE_REVERB,
        &DSPSettings );
    ```

    

3.  <span data-ttu-id="ccfa3-136">Usare [**IXAudio2Voice:: SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) e [**IXAudio2SourceVoice:: SetFrequencyRatio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) per applicare i valori volume e pitch alla voce di origine.</span><span class="sxs-lookup"><span data-stu-id="ccfa3-136">Use [**IXAudio2Voice::SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) and [**IXAudio2SourceVoice::SetFrequencyRatio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) to apply the volume and pitch values to the source voice.</span></span>

    ```
    pSFXSourceVoice->SetOutputMatrix( pMasterVoice, 1, deviceDetails.OutputFormat.Format.nChannels, DSPSettings.pMatrixCoefficients ) ;
    pSFXSourceVoice->SetFrequencyRatio(DSPSettings.DopplerFactor);
    ```

    

4.  <span data-ttu-id="ccfa3-137">Usare [**IXAudio2Voice:: SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) per applicare il livello di riverbero calcolato alla voce submix.</span><span class="sxs-lookup"><span data-stu-id="ccfa3-137">Use [**IXAudio2Voice::SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) to apply the calculated reverb level to the submix voice.</span></span>

    ```
    pSFXSourceVoice->SetOutputMatrix(pSubmixVoice, 1, 1, &DSPSettings.ReverbLevel);
    ```

    

5.  <span data-ttu-id="ccfa3-138">Usare [**IXAudio2Voice:: SetFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters) per applicare il coefficiente diretto del filtro di passaggio basso calcolato alla voce di origine.</span><span class="sxs-lookup"><span data-stu-id="ccfa3-138">Use [**IXAudio2Voice::SetFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters) to apply the calculated low pass filter direct coefficient to the source voice.</span></span>

    ```
    XAUDIO2_FILTER_PARAMETERS FilterParameters = { LowPassFilter, 2.0f * sinf(X3DAUDIO_PI/6.0f * DSPSettings.LPFDirectCoefficient), 1.0f };
    pSFXSourceVoice->SetFilterParameters(&FilterParameters);
    ```

    

## <a name="related-topics"></a><span data-ttu-id="ccfa3-139">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ccfa3-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ccfa3-140">X3DAudio</span><span class="sxs-lookup"><span data-stu-id="ccfa3-140">X3DAudio</span></span>](x3daudio.md)
</dt> <dt>

[<span data-ttu-id="ccfa3-141">Panoramica di X3DAudio</span><span class="sxs-lookup"><span data-stu-id="ccfa3-141">X3DAudio Overview</span></span>](x3daudio-overview.md)
</dt> <dt>

[<span data-ttu-id="ccfa3-142">Guida alla programmazione di XAudio2</span><span class="sxs-lookup"><span data-stu-id="ccfa3-142">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="ccfa3-143">Controllo volume e pitch XAudio2</span><span class="sxs-lookup"><span data-stu-id="ccfa3-143">XAudio2 Volume and Pitch Control</span></span>](volume-and-pitch-control.md)
</dt> </dl>

 

 
