---
description: Questo argomento illustra come applicare una catena di effetti a una voce per consentire l'elaborazione personalizzata dei dati audio per tale voce. In questo argomento viene descritto come utilizzare l'effetto Reverb, che è uno degli effetti XAudio2 predefiniti.
ms.assetid: 4c33bd83-2654-cd6f-ea6c-bbc0d5872638
title: 'Procedura: Creare una catena di effetti'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85d58186b623dca04da99001a29e54cf3ecc39fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129770"
---
# <a name="how-to-create-an-effect-chain"></a><span data-ttu-id="903eb-104">Procedura: Creare una catena di effetti</span><span class="sxs-lookup"><span data-stu-id="903eb-104">How to: Create an Effect Chain</span></span>

<span data-ttu-id="903eb-105">Questo argomento illustra come applicare una catena di effetti a una voce per consentire l'elaborazione personalizzata dei dati audio per tale voce.</span><span class="sxs-lookup"><span data-stu-id="903eb-105">This topic shows you how you can apply an effect chain to a voice to allow custom processing of the audio data for that voice.</span></span> <span data-ttu-id="903eb-106">In questo argomento viene descritto come utilizzare l'effetto Reverb, che è uno degli effetti XAudio2 predefiniti.</span><span class="sxs-lookup"><span data-stu-id="903eb-106">This topic describes how to use the reverb effect, which is one of the built-in XAudio2 effects.</span></span>

## <a name="to-create-a-basic-effect-chain-that-applies-an-effect-to-a-voice"></a><span data-ttu-id="903eb-107">Per creare una catena di effetti di base che applica un effetto a una voce</span><span class="sxs-lookup"><span data-stu-id="903eb-107">To create a basic effect chain that applies an effect to a voice</span></span>

1.  <span data-ttu-id="903eb-108">Creare l'effetto.</span><span class="sxs-lookup"><span data-stu-id="903eb-108">Create the effect.</span></span>

    <span data-ttu-id="903eb-109">In questo esempio, la funzione [**XAudio2CreateReverb**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createreverb) crea un effetto di riverbero.</span><span class="sxs-lookup"><span data-stu-id="903eb-109">In this example, the [**XAudio2CreateReverb**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createreverb) function creates a reverb effect.</span></span> <span data-ttu-id="903eb-110">Per un elenco delle possibili origini degli effetti da usare con XAudio2, vedere [XAudio2 Audio Effects](xaudio2-audio-effects.md) .</span><span class="sxs-lookup"><span data-stu-id="903eb-110">See [XAudio2 Audio Effects](xaudio2-audio-effects.md) for a list of possible sources of effects for use with XAudio2.</span></span>

    ```
    IUnknown * pXAPO;
    hr = XAudio2CreateReverb(&pXAPO);
    ```

    

2.  <span data-ttu-id="903eb-111">Popola una struttura del [**\_ \_ descrittore dell'effetto XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) con i dati.</span><span class="sxs-lookup"><span data-stu-id="903eb-111">Populate an [**XAUDIO2\_EFFECT\_DESCRIPTOR**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) structure with data.</span></span>

    <span data-ttu-id="903eb-112">Se sono presenti più effetti nella catena, ogni effetto avrà bisogno di una struttura del [**\_ \_ descrittore dell'effetto XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) .</span><span class="sxs-lookup"><span data-stu-id="903eb-112">If there are multiple effects in the chain, each effect will need a [**XAUDIO2\_EFFECT\_DESCRIPTOR**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) structure.</span></span>

    ```
    XAUDIO2_EFFECT_DESCRIPTOR descriptor;
    descriptor.InitialState = true;
    descriptor.OutputChannels = 1;
    descriptor.pEffect = pXAPO;
    ```

    

3.  <span data-ttu-id="903eb-113">Popola una struttura della [**\_ \_ catena di effetti XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain) con i dati.</span><span class="sxs-lookup"><span data-stu-id="903eb-113">Populate an [**XAUDIO2\_EFFECT\_CHAIN**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain) structure with data.</span></span> <span data-ttu-id="903eb-114">In questo caso, la catena ha un solo effetto.</span><span class="sxs-lookup"><span data-stu-id="903eb-114">In this case, the chain only has one effect.</span></span> <span data-ttu-id="903eb-115">Se la catena ha più di un effetto, il membro EffectCount conterrà il conteggio degli effetti e il membro pEffectDescriptors punterà a una matrice di strutture di \_ \_ descrittore di effetto XAUDIO2.</span><span class="sxs-lookup"><span data-stu-id="903eb-115">If the chain has more than one effect, the EffectCount member will contain the count of effects, and the pEffectDescriptors member will point to an array of XAUDIO2\_EFFECT\_DESCRIPTOR structures.</span></span>

    ```
    XAUDIO2_EFFECT_CHAIN chain;
    chain.EffectCount = 1;
    chain.pEffectDescriptors = &descriptor;
    ```

    

4.  <span data-ttu-id="903eb-116">Applicare la catena di effetti a una voce con la funzione [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain) .</span><span class="sxs-lookup"><span data-stu-id="903eb-116">Apply the effect chain to a voice with the [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain) function.</span></span>

    <span data-ttu-id="903eb-117">È possibile applicare catene di effetti a voci Master, voci di origine e voci submix.</span><span class="sxs-lookup"><span data-stu-id="903eb-117">You can apply effect chains to master voices, source voices, and submix voices.</span></span>

    ```
    pVoice->SetEffectChain(&chain);
    ```

    

5.  <span data-ttu-id="903eb-118">Rilasciare l'effetto con IUnknown:: Release.</span><span class="sxs-lookup"><span data-stu-id="903eb-118">Release the effect with IUnknown::Release.</span></span>

    <span data-ttu-id="903eb-119">Quando si crea un XAPO, il conteggio dei riferimenti sarà 1.</span><span class="sxs-lookup"><span data-stu-id="903eb-119">When you create an XAPO, it will have a reference count of 1.</span></span> <span data-ttu-id="903eb-120">Quando XAPO viene passato a XAudio2 con [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain), XAudio2 incrementa il conteggio dei riferimenti in XAPO.</span><span class="sxs-lookup"><span data-stu-id="903eb-120">When the XAPO is passed to XAudio2 with [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain), XAudio2 increments the reference count on the XAPO.</span></span> <span data-ttu-id="903eb-121">Il rilascio del riferimento del client a XAPO consente a XAudio2 di assumere la proprietà del XAPO.</span><span class="sxs-lookup"><span data-stu-id="903eb-121">Releasing the client's reference to the XAPO allows XAudio2 to take ownership of the XAPO.</span></span> <span data-ttu-id="903eb-122">Se XAudio2 ha l'unico riferimento a XAPO, verrà eliminato quando non verrà più usato da XAudio2..</span><span class="sxs-lookup"><span data-stu-id="903eb-122">If XAudio2 has the only reference to the XAPO, it will be disposed of when it is no longer being used by XAudio2.</span></span> <span data-ttu-id="903eb-123">Se il codice client deve mantenere un riferimento a XAPO, ad esempio per un riutilizzo successivo, è consigliabile ignorare questo passaggio.</span><span class="sxs-lookup"><span data-stu-id="903eb-123">If the client code needs to maintain a reference to the XAPO—for example for later reuse—you should skip this step.</span></span>

    ```
    pXAPO->Release();
    ```

    

6.  <span data-ttu-id="903eb-124">Popola la struttura di parametri, se presente, associata all'effetto.</span><span class="sxs-lookup"><span data-stu-id="903eb-124">Populate the parameter structure, if any, associated with the effect.</span></span> <span data-ttu-id="903eb-125">L'effetto di riverbero usa una struttura di [**\_ \_ parametri di reverbi XAUDIO2FX**](/windows/desktop/api/xaudio2fx/ns-xaudio2fx-xaudio2fx_reverb_parameters) .</span><span class="sxs-lookup"><span data-stu-id="903eb-125">The reverb effect uses an [**XAUDIO2FX\_REVERB\_PARAMETERS**](/windows/desktop/api/xaudio2fx/ns-xaudio2fx-xaudio2fx_reverb_parameters) structure.</span></span>

    ```
    XAUDIO2FX_REVERB_PARAMETERS reverbParameters;
    reverbParameters.ReflectionsDelay = XAUDIO2FX_REVERB_DEFAULT_REFLECTIONS_DELAY;
    reverbParameters.ReverbDelay = XAUDIO2FX_REVERB_DEFAULT_REVERB_DELAY;
    reverbParameters.RearDelay = XAUDIO2FX_REVERB_DEFAULT_REAR_DELAY;
    reverbParameters.PositionLeft = XAUDIO2FX_REVERB_DEFAULT_POSITION;
    reverbParameters.PositionRight = XAUDIO2FX_REVERB_DEFAULT_POSITION;
    reverbParameters.PositionMatrixLeft = XAUDIO2FX_REVERB_DEFAULT_POSITION_MATRIX;
    reverbParameters.PositionMatrixRight = XAUDIO2FX_REVERB_DEFAULT_POSITION_MATRIX;
    reverbParameters.EarlyDiffusion = XAUDIO2FX_REVERB_DEFAULT_EARLY_DIFFUSION;
    reverbParameters.LateDiffusion = XAUDIO2FX_REVERB_DEFAULT_LATE_DIFFUSION;
    reverbParameters.LowEQGain = XAUDIO2FX_REVERB_DEFAULT_LOW_EQ_GAIN;
    reverbParameters.LowEQCutoff = XAUDIO2FX_REVERB_DEFAULT_LOW_EQ_CUTOFF;
    reverbParameters.HighEQGain = XAUDIO2FX_REVERB_DEFAULT_HIGH_EQ_GAIN;
    reverbParameters.HighEQCutoff = XAUDIO2FX_REVERB_DEFAULT_HIGH_EQ_CUTOFF;
    reverbParameters.RoomFilterFreq = XAUDIO2FX_REVERB_DEFAULT_ROOM_FILTER_FREQ;
    reverbParameters.RoomFilterMain = XAUDIO2FX_REVERB_DEFAULT_ROOM_FILTER_MAIN;
    reverbParameters.RoomFilterHF = XAUDIO2FX_REVERB_DEFAULT_ROOM_FILTER_HF;
    reverbParameters.ReflectionsGain = XAUDIO2FX_REVERB_DEFAULT_REFLECTIONS_GAIN;
    reverbParameters.ReverbGain = XAUDIO2FX_REVERB_DEFAULT_REVERB_GAIN;
    reverbParameters.DecayTime = XAUDIO2FX_REVERB_DEFAULT_DECAY_TIME;
    reverbParameters.Density = XAUDIO2FX_REVERB_DEFAULT_DENSITY;
    reverbParameters.RoomSize = XAUDIO2FX_REVERB_DEFAULT_ROOM_SIZE;
    reverbParameters.WetDryMix = XAUDIO2FX_REVERB_DEFAULT_WET_DRY_MIX;
    ```

    

7.  <span data-ttu-id="903eb-126">Passare la struttura del parametro Effect all'effetto chiamando la funzione [**SetEffectParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters) sulla voce a cui è collegato l'effetto.</span><span class="sxs-lookup"><span data-stu-id="903eb-126">Pass the effect parameter structure to the effect by calling the [**SetEffectParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters) function on the voice to which the effect is attached.</span></span>

    ```
    hr = pVoice->SetEffectParameters( 0, &reverbParameters, sizeof( reverbParameters ) );
    ```

    

8.  <span data-ttu-id="903eb-127">Disabilitare o abilitare l'effetto, quando appropriato.</span><span class="sxs-lookup"><span data-stu-id="903eb-127">Disable or enable the effect, whenever appropriate.</span></span>

    <span data-ttu-id="903eb-128">È possibile utilizzare [**DisableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-disableeffect) in qualsiasi momento per disattivare un effetto.</span><span class="sxs-lookup"><span data-stu-id="903eb-128">You can use [**DisableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-disableeffect) at any time to turn an effect off.</span></span>

    ```
    pVoice->DisableEffect(0);
    ```

    

    <span data-ttu-id="903eb-129">È possibile attivare di nuovo un effetto con [**EnableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect).</span><span class="sxs-lookup"><span data-stu-id="903eb-129">You can turn on an effect again with [**EnableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect).</span></span>

    ```
    pVoice->EnableEffect(0);
    ```

    

    <span data-ttu-id="903eb-130">I parametri per [**DisableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-disableeffect) e [**EnableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect) specificano l'effetto della catena da abilitare o disabilitare.</span><span class="sxs-lookup"><span data-stu-id="903eb-130">The parameters for [**DisableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-disableeffect) and [**EnableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect) specify which effect in the chain to enable or disable.</span></span>

## <a name="related-topics"></a><span data-ttu-id="903eb-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="903eb-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="903eb-132">Effetti audio</span><span class="sxs-lookup"><span data-stu-id="903eb-132">Audio Effects</span></span>](audio-effects.md)
</dt> <dt>

[<span data-ttu-id="903eb-133">Guida alla programmazione di XAudio2</span><span class="sxs-lookup"><span data-stu-id="903eb-133">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="903eb-134">Procedura: Creare un grafico di elaborazione audio di base</span><span class="sxs-lookup"><span data-stu-id="903eb-134">How to: Build a Basic Audio Processing Graph</span></span>](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[<span data-ttu-id="903eb-135">Panoramica di XAPO</span><span class="sxs-lookup"><span data-stu-id="903eb-135">XAPO Overview</span></span>](xapo-overview.md)
</dt> <dt>

[<span data-ttu-id="903eb-136">Procedura: usare XAOPFX in XAudio2</span><span class="sxs-lookup"><span data-stu-id="903eb-136">How to: Use XAOPFX in XAudio2</span></span>](how-to--use-xapofx-in-xaudio2.md)
</dt> <dt>

[<span data-ttu-id="903eb-137">Procedura: usare un XAOP in XAudio2</span><span class="sxs-lookup"><span data-stu-id="903eb-137">How to: Use an XAOP in XAudio2</span></span>](how-to--use-an-xapo-in-xaudio2.md)
</dt> </dl>

 

 
