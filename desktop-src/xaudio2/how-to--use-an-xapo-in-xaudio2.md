---
description: Questo argomento illustra come usare un effetto creato con l'API XAPO in una catena di effetti XAudio2.
ms.assetid: d4d24177-25eb-13ca-0e38-0c876a273e0d
title: 'Procedura: Usare un oggetto di elaborazione audio XAPO in XAudio2'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 780e0ba59b5032ddc01b2709f1f3e9c5a0fcce1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307944"
---
# <a name="how-to-use-an-xapo-in-xaudio2"></a><span data-ttu-id="12f85-103">Procedura: Usare un oggetto di elaborazione audio XAPO in XAudio2</span><span class="sxs-lookup"><span data-stu-id="12f85-103">How to: Use an XAPO in XAudio2</span></span>

<span data-ttu-id="12f85-104">Questo argomento illustra come usare un effetto creato con l'API XAPO in una catena di effetti XAudio2.</span><span class="sxs-lookup"><span data-stu-id="12f85-104">This topic shows you how to use an effect created with the XAPO API in an XAudio2 effect chain.</span></span>

1.  <span data-ttu-id="12f85-105">Creare il XAPO come descritto in [procedura: creare un XAPO](how-to--create-an-xapo.md).</span><span class="sxs-lookup"><span data-stu-id="12f85-105">Create the XAPO as described in [How to: Create an XAPO](how-to--create-an-xapo.md).</span></span>

    <span data-ttu-id="12f85-106">È anche possibile implementare la funzionalità del parametro in fase di esecuzione, come descritto in [procedura: aggiungere il supporto per i parametri della fase di esecuzione a un XAPO](how-to--add-run-time-parameter-support-to-an-xapo.md).</span><span class="sxs-lookup"><span data-stu-id="12f85-106">You can also implement run-time parameter functionality as described in [How to: Add Run-time Parameter Support to an XAPO](how-to--add-run-time-parameter-support-to-an-xapo.md).</span></span>

2.  <span data-ttu-id="12f85-107">Creare un'istanza di XAPO.</span><span class="sxs-lookup"><span data-stu-id="12f85-107">Create an instance of the XAPO.</span></span>

    ```
    IUnknown * pXAPO;
    pXAPO = new SimpleXAPO();
    ```

    

3.  <span data-ttu-id="12f85-108">Popola una struttura del [**\_ \_ descrittore dell'effetto XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) con i dati.</span><span class="sxs-lookup"><span data-stu-id="12f85-108">Populate an [**XAUDIO2\_EFFECT\_DESCRIPTOR**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) structure with data.</span></span>

    ```
    XAUDIO2_EFFECT_DESCRIPTOR descriptor;
    descriptor.InitialState = true;
    descriptor.OutputChannels = 1;
    descriptor.pEffect = pXAPO;
    ```

    

4.  <span data-ttu-id="12f85-109">Popola una struttura della [**\_ \_ catena di effetti XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain) con i dati.</span><span class="sxs-lookup"><span data-stu-id="12f85-109">Populate an [**XAUDIO2\_EFFECT\_CHAIN**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain) structure with data.</span></span>

    ```
    XAUDIO2_EFFECT_CHAIN chain;
    chain.EffectCount = 1;
    chain.pEffectDescriptors = &descriptor;
    ```

    

5.  <span data-ttu-id="12f85-110">Applicare la catena di effetti a una voce XAudio2 con la funzione [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain) .</span><span class="sxs-lookup"><span data-stu-id="12f85-110">Apply the effect chain to an XAudio2 voice with the [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain) function.</span></span>

    ```
    pVoice->SetEffectChain(&chain);
    ```

    

    > [!Note]  
    > <span data-ttu-id="12f85-111">Una catena di effetti può anche essere applicata a una voce quando la voce viene creata passando la catena come parametro a [**IXAudio2:: CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice), [**IXAudio2:: CreateSubmixVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsubmixvoice)o [**IXAudio2:: CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice).</span><span class="sxs-lookup"><span data-stu-id="12f85-111">An effect chain can also be applied to a voice when the voice is created by passing the chain as a parameter to [**IXAudio2::CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice), [**IXAudio2::CreateSubmixVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsubmixvoice), or [**IXAudio2::CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice).</span></span>

     

6.  <span data-ttu-id="12f85-112">Rilasciare l'effetto con IUnknown:: Release.</span><span class="sxs-lookup"><span data-stu-id="12f85-112">Release the effect with IUnknown::Release.</span></span>

    <span data-ttu-id="12f85-113">Quando si crea un XAPO, il conteggio dei riferimenti sarà 1.</span><span class="sxs-lookup"><span data-stu-id="12f85-113">When you create an XAPO, it will have a reference count of 1.</span></span> <span data-ttu-id="12f85-114">Quando XAPO viene passato a XAudio2 con [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain), XAudio2 incrementa il conteggio dei riferimenti in XAPO.</span><span class="sxs-lookup"><span data-stu-id="12f85-114">When the XAPO is passed to XAudio2 with [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain), XAudio2 increments the reference count on the XAPO.</span></span> <span data-ttu-id="12f85-115">Il rilascio del riferimento del client a XAPO consente a XAudio2 di assumere la proprietà del XAPO.</span><span class="sxs-lookup"><span data-stu-id="12f85-115">Releasing the client's reference to the XAPO allows XAudio2 to take ownership of the XAPO.</span></span> <span data-ttu-id="12f85-116">Se XAudio2 ha l'unico riferimento a XAPO, verrà eliminato quando non verrà più usato da XAudio2..</span><span class="sxs-lookup"><span data-stu-id="12f85-116">If XAudio2 has the only reference to the XAPO, it will be disposed of when it is no longer being used by XAudio2.</span></span> <span data-ttu-id="12f85-117">Se il codice client deve mantenere un riferimento a XAPO per un riutilizzo successivo, ad esempio, è consigliabile ignorare questo passaggio.</span><span class="sxs-lookup"><span data-stu-id="12f85-117">If the client code needs to maintain a reference to the XAPO for later reuse, for example, you should skip this step.</span></span>

    ```
    pXAPO->Release();
    ```

    

7.  <span data-ttu-id="12f85-118">Popola la struttura di parametri, se presente, associata all'effetto.</span><span class="sxs-lookup"><span data-stu-id="12f85-118">Populate the parameter structure, if any, associated with the effect.</span></span> <span data-ttu-id="12f85-119">In questo caso, la percentuale di attendibilità totale in cui deve essere applicato l'effetto.</span><span class="sxs-lookup"><span data-stu-id="12f85-119">In this case, the percentage of full strength at which the effect should be applied.</span></span>

    ```
    XAPO_PARAMETERS XAPOParameters;
    XAPOParameters.Level = 0.75;
    ```

    

8.  <span data-ttu-id="12f85-120">Passare la struttura del parametro Effect all'effetto chiamando la funzione [**SetEffectParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters) sulla voce a cui è collegato l'effetto.</span><span class="sxs-lookup"><span data-stu-id="12f85-120">Pass the effect parameter structure to the effect by calling the [**SetEffectParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters) function on the voice to which the effect is attached.</span></span>

    ```
    hr = pVoice->SetEffectParameters( 0, &XAPOParameters, sizeof( XAPO_PARAMETERS ) );
    ```

    

## <a name="related-topics"></a><span data-ttu-id="12f85-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="12f85-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12f85-122">Effetti audio</span><span class="sxs-lookup"><span data-stu-id="12f85-122">Audio Effects</span></span>](audio-effects.md)
</dt> <dt>

[<span data-ttu-id="12f85-123">Panoramica di XAPO</span><span class="sxs-lookup"><span data-stu-id="12f85-123">XAPO Overview</span></span>](xapo-overview.md)
</dt> <dt>

[<span data-ttu-id="12f85-124">Guida alla programmazione di XAudio2</span><span class="sxs-lookup"><span data-stu-id="12f85-124">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> </dl>

 

 
