---
description: Questo argomento illustra come usare uno degli effetti inclusi in XAPOFX in una catena di effetti XAudio2.
ms.assetid: dc325584-13f7-231a-e0c7-17f38d54ae11
title: 'Procedura: Usare XAPOFX in XAudio2'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77b0bb4cbeabb38f408d9102a2534634e8eed7cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307942"
---
# <a name="how-to-use-xapofx-in-xaudio2"></a><span data-ttu-id="3180d-103">Procedura: Usare XAPOFX in XAudio2</span><span class="sxs-lookup"><span data-stu-id="3180d-103">How to: Use XAPOFX in XAudio2</span></span>

<span data-ttu-id="3180d-104">Questo argomento illustra come usare uno degli effetti inclusi in XAPOFX in una catena di effetti XAudio2.</span><span class="sxs-lookup"><span data-stu-id="3180d-104">This topic shows you how to use one of the effects included in XAPOFX in an XAudio2 effect chain.</span></span>

## <a name="to-use-an-effect-from-xapofx-in-an-xaudio2-effect-chain"></a><span data-ttu-id="3180d-105">Per usare un effetto di XAPOFX in una catena di effetti XAudio2</span><span class="sxs-lookup"><span data-stu-id="3180d-105">To use an effect from XAPOFX in an XAudio2 effect chain</span></span>

1.  <span data-ttu-id="3180d-106">Creare l'effetto passando il CLSID di un effetto XAPOFX alla funzione [**CreateFX**](/windows/desktop/api/XAPOFX/nf-xapofx-createfx) .</span><span class="sxs-lookup"><span data-stu-id="3180d-106">Create the effect by passing the CLSID of an XAPOFX effect to the [**CreateFX**](/windows/desktop/api/XAPOFX/nf-xapofx-createfx) function.</span></span>

    <span data-ttu-id="3180d-107">In questo caso, viene creato l'effetto di riverbero semplificato FXReverb.</span><span class="sxs-lookup"><span data-stu-id="3180d-107">In this case, the simplified reverb effect FXReverb is being created.</span></span>

    ```
    IUnknown * pXAPO;
    CreateFX(__uuidof(FXReverb),&pXAPO);
    ```

    

2.  <span data-ttu-id="3180d-108">Popola una struttura del [**\_ \_ descrittore dell'effetto XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) con i dati.</span><span class="sxs-lookup"><span data-stu-id="3180d-108">Populate an [**XAUDIO2\_EFFECT\_DESCRIPTOR**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) structure with data.</span></span>

    ```
    XAUDIO2_EFFECT_DESCRIPTOR descriptor;
    descriptor.InitialState = true;
    descriptor.OutputChannels = 1;
    descriptor.pEffect = pXAPO;
    ```

    

3.  <span data-ttu-id="3180d-109">Popola una struttura della [**\_ \_ catena di effetti XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain) con i dati.</span><span class="sxs-lookup"><span data-stu-id="3180d-109">Populate an [**XAUDIO2\_EFFECT\_CHAIN**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain) structure with data.</span></span>

    ```
    XAUDIO2_EFFECT_CHAIN chain;
    chain.EffectCount = 1;
    chain.pEffectDescriptors = &descriptor;
    ```

    

4.  <span data-ttu-id="3180d-110">Applicare la catena di effetti a una voce XAudio2 con la funzione [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain) .</span><span class="sxs-lookup"><span data-stu-id="3180d-110">Apply the effect chain to an XAudio2 voice with the [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain) function.</span></span>

    ```
    pVoice->SetEffectChain(&chain);
    ```

    

    > [!Note]  
    > <span data-ttu-id="3180d-111">È anche possibile applicare una catena di effetti a una voce quando si crea la voce passando la catena come parametro a [**IXAudio2:: CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice), [**IXAudio2:: CreateSubmixVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsubmixvoice)o [**IXAudio2:: CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice).</span><span class="sxs-lookup"><span data-stu-id="3180d-111">You can also apply an effect chain to a voice when you create the voice by passing the chain as a parameter to [**IXAudio2::CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice), [**IXAudio2::CreateSubmixVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsubmixvoice), or [**IXAudio2::CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice).</span></span>

     

5.  <span data-ttu-id="3180d-112">Rilasciare l'effetto con IUnknown:: Release.</span><span class="sxs-lookup"><span data-stu-id="3180d-112">Release the effect with IUnknown::Release.</span></span> <span data-ttu-id="3180d-113">Quando si crea un XAPO, il conteggio dei riferimenti sarà 1.</span><span class="sxs-lookup"><span data-stu-id="3180d-113">When you create an XAPO, it will have a reference count of 1.</span></span> <span data-ttu-id="3180d-114">Quando XAPO viene passato a XAudio2 con [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain), XAudio2 incrementa il conteggio dei riferimenti in XAPO.</span><span class="sxs-lookup"><span data-stu-id="3180d-114">When the XAPO is passed to XAudio2 with [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain), XAudio2 increments the reference count on the XAPO.</span></span> <span data-ttu-id="3180d-115">Il rilascio del riferimento del client a XAPO consente a XAudio2 di assumere la proprietà del XAPO.</span><span class="sxs-lookup"><span data-stu-id="3180d-115">Releasing the client's reference to the XAPO allows XAudio2 to take ownership of the XAPO.</span></span> <span data-ttu-id="3180d-116">Se XAudio2 ha l'unico riferimento a XAPO, questo riferimento viene eliminato quando non è più usato da XAudio2.</span><span class="sxs-lookup"><span data-stu-id="3180d-116">If XAudio2 has the only reference to the XAPO, this reference is disposed of when it is no longer being used by XAudio2.</span></span> <span data-ttu-id="3180d-117">Se il codice client deve mantenere un riferimento a XAPO, ad esempio per riutilizzarlo in un secondo momento, è possibile ignorare questo passaggio.</span><span class="sxs-lookup"><span data-stu-id="3180d-117">If the client code needs to maintain a reference to the XAPO—for example, for reuse later—you can skip this step.</span></span>

    ```
    pXAPO->Release();
    ```

    

6.  <span data-ttu-id="3180d-118">Popola la struttura di parametri, se presente, associata all'effetto.</span><span class="sxs-lookup"><span data-stu-id="3180d-118">Populate the parameter structure, if any, associated with the effect.</span></span>

    <span data-ttu-id="3180d-119">In questo caso, la struttura dei [**\_ parametri FXREVERB**](/windows/desktop/api/xapofx/ns-xapofx-fxreverb_parameters) viene utilizzata per impostare le dimensioni della diffusione e della stanza che devono essere utilizzate dall'effetto di riverbero.</span><span class="sxs-lookup"><span data-stu-id="3180d-119">In this case, the [**FXREVERB\_PARAMETERS**](/windows/desktop/api/xapofx/ns-xapofx-fxreverb_parameters) structure is used to set the diffusion and room size that the reverb effect should use.</span></span>

    ```
    FXREVERB_PARAMETERS XAPOParameters;
    XAPOParameters.Diffusion = FXREVERB_DEFAULT_DIFFUSION;
    XAPOParameters.RoomSize = FXREVERB_DEFAULT_ROOMSIZE;
    ```

    

7.  <span data-ttu-id="3180d-120">Passare la struttura del parametro Effect all'effetto chiamando la funzione [**SetEffectParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters) sulla voce a cui è collegato l'effetto.</span><span class="sxs-lookup"><span data-stu-id="3180d-120">Pass the effect parameter structure to the effect by calling the [**SetEffectParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters) function on the voice to which the effect is attached.</span></span>

    ```
    hr = pVoice->SetEffectParameters( 0, &XAPOParameters, sizeof( FXREVERB_PARAMETERS ) );
    ```

    

## <a name="related-topics"></a><span data-ttu-id="3180d-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3180d-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3180d-122">Effetti audio</span><span class="sxs-lookup"><span data-stu-id="3180d-122">Audio Effects</span></span>](audio-effects.md)
</dt> <dt>

[<span data-ttu-id="3180d-123">Guida alla programmazione di XAudio2</span><span class="sxs-lookup"><span data-stu-id="3180d-123">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> </dl>

 

 
