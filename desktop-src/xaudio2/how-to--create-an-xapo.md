---
description: L'API XAPO fornisce l'interfaccia IXAPO e la classe CXAPOBase per la compilazione di nuovi tipi XAPO.
ms.assetid: 34f5c3d5-ee40-e304-7c97-d30c17621d26
title: 'Procedura: Creare un oggetto di elaborazione audio di XAudio2 (XAPO)'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 549739462a0e76cbb437f0aa1403b099f72f5224
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234064"
---
# <a name="how-to-create-an-xapo"></a><span data-ttu-id="43681-103">Procedura: Creare un oggetto di elaborazione audio di XAudio2 (XAPO)</span><span class="sxs-lookup"><span data-stu-id="43681-103">How to: Create an XAPO</span></span>

<span data-ttu-id="43681-104">L'API XAPO fornisce l'interfaccia [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) e la classe [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) per la compilazione di nuovi tipi XAPO.</span><span class="sxs-lookup"><span data-stu-id="43681-104">The XAPO API provides the [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) interface and the [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) class for building new XAPO types.</span></span> <span data-ttu-id="43681-105">L'interfaccia **IXAPO** contiene tutti i metodi che devono essere implementati per creare un nuovo XAPO.</span><span class="sxs-lookup"><span data-stu-id="43681-105">The **IXAPO** interface contains all of the methods that need to be implemented to create a new XAPO.</span></span> <span data-ttu-id="43681-106">La classe **CXAPOBase** fornisce un'implementazione di base dell'interfaccia **IXAPO** .</span><span class="sxs-lookup"><span data-stu-id="43681-106">The **CXAPOBase** class provides a basic implementation of the **IXAPO** interface.</span></span> <span data-ttu-id="43681-107">**CXAPOBase** implementa tutti i metodi dell'interfaccia **IXAPO** ad eccezione del metodo [**IXAPO::P rocess**](/windows/win32/api/xapo/nf-xapo-ixapo-process) , che è univoco per ogni XAPO.</span><span class="sxs-lookup"><span data-stu-id="43681-107">**CXAPOBase** implements all of the **IXAPO** interface methods except the [**IXAPO::Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process) method, which is unique to each XAPO.</span></span>

## <a name="to-create-a-new-static-xapo"></a><span data-ttu-id="43681-108">Per creare un nuovo XAPO statico</span><span class="sxs-lookup"><span data-stu-id="43681-108">To create a new static XAPO</span></span>

1.  <span data-ttu-id="43681-109">Derivare una nuova classe XAPO dalla classe di base [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) .</span><span class="sxs-lookup"><span data-stu-id="43681-109">Derive a new XAPO class from the [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) base class.</span></span>

    > [!Note]  
    > <span data-ttu-id="43681-110">XAPOs implementano l'interfaccia **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="43681-110">XAPOs implement the **IUnknown** interface.</span></span> <span data-ttu-id="43681-111">Le interfacce [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) e [**IXAPOParameters**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters) includono i tre metodi **IUnknown** : **QueryInterface**, **AddRef** e **Release**.</span><span class="sxs-lookup"><span data-stu-id="43681-111">The [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) and [**IXAPOParameters**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters) interfaces include the three **IUnknown** methods: **QueryInterface**, **AddRef**, and **Release**.</span></span> <span data-ttu-id="43681-112">[**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) fornisce implementazioni di tutti e tre i metodi **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="43681-112">[**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) provides implementations of all three of the **IUnknown** methods.</span></span> <span data-ttu-id="43681-113">Una nuova istanza di **CXAPOBase** avrà un conteggio dei riferimenti pari a 1.</span><span class="sxs-lookup"><span data-stu-id="43681-113">A new instance of **CXAPOBase** will have a reference count of 1.</span></span> <span data-ttu-id="43681-114">Verrà eliminato definitivamente quando il conteggio dei riferimenti diventa 0.</span><span class="sxs-lookup"><span data-stu-id="43681-114">It will be destroyed when its reference count becomes 0.</span></span> <span data-ttu-id="43681-115">Per consentire a XAudio2 di eliminare un'istanza di un XAPO quando non è più necessario, chiamare **IUnknown:: Release** sul XAPO dopo che è stato aggiunto a una catena di effetti XAudio2.</span><span class="sxs-lookup"><span data-stu-id="43681-115">To allow XAudio2 to destroy an instance of an XAPO when it is no longer needed, call **IUnknown::Release** on the XAPO after it is added to an XAudio2 effect chain.</span></span> <span data-ttu-id="43681-116">Vedere [procedura: usare un XAPO in XAudio2](how-to--use-an-xapo-in-xaudio2.md) per altre informazioni sull'uso di un XAPO con XAudio2.</span><span class="sxs-lookup"><span data-stu-id="43681-116">See [How to: Use an XAPO in XAudio2](how-to--use-an-xapo-in-xaudio2.md) for more information about using an XAPO with XAudio2.</span></span>

     

2.  <span data-ttu-id="43681-117">Eseguire l'override dell'implementazione della classe [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) del metodo [**IXAPO:: LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) .</span><span class="sxs-lookup"><span data-stu-id="43681-117">Override the [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) class implementation of the [**IXAPO::LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) method.</span></span>

    <span data-ttu-id="43681-118">L'override di [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) consente di archiviare le informazioni sul formato dei dati audio da usare in [**IXAPO::P rocess**](/windows/win32/api/xapo/nf-xapo-ixapo-process).</span><span class="sxs-lookup"><span data-stu-id="43681-118">Overriding [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) allows information about the format of audio data to be stored for use in [**IXAPO::Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process).</span></span>

3.  <span data-ttu-id="43681-119">Implementare il metodo [**IXAPO::P rocess**](/windows/win32/api/xapo/nf-xapo-ixapo-process) .</span><span class="sxs-lookup"><span data-stu-id="43681-119">Implement the [**IXAPO::Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process) method.</span></span>

    <span data-ttu-id="43681-120">XAudio2 chiama il metodo [**IXAPO::P rocess**](/windows/win32/api/xapo/nf-xapo-ixapo-process) ogni volta che un XAPO deve elaborare dati audio.</span><span class="sxs-lookup"><span data-stu-id="43681-120">XAudio2 calls the [**IXAPO::Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process) method whenever an XAPO needs to process audio data.</span></span> <span data-ttu-id="43681-121">Il **processo** contiene la maggior parte del codice per un XAPO.</span><span class="sxs-lookup"><span data-stu-id="43681-121">**Process** contains the bulk of the code for an XAPO.</span></span>

## <a name="implementing-the-process-method"></a><span data-ttu-id="43681-122">Implementazione del metodo Process</span><span class="sxs-lookup"><span data-stu-id="43681-122">Implementing the Process Method</span></span>

<span data-ttu-id="43681-123">Il metodo [**IXAPO::P rocess**](/windows/win32/api/xapo/nf-xapo-ixapo-process) accetta buffer di flusso per i dati audio di input e di output.</span><span class="sxs-lookup"><span data-stu-id="43681-123">The [**IXAPO::Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process) method accepts stream buffers for input and output audio data.</span></span> <span data-ttu-id="43681-124">Un XAPO tipico prevede un buffer del flusso di input e un buffer del flusso di output.</span><span class="sxs-lookup"><span data-stu-id="43681-124">A typical XAPO will expect one input stream buffer and one output stream buffer.</span></span> <span data-ttu-id="43681-125">È necessario basare l'elaborazione dei dati dal buffer del flusso di input nel formato specificato nella funzione [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) e tutti i flag passati alla funzione **Process** con il buffer del flusso di input.</span><span class="sxs-lookup"><span data-stu-id="43681-125">You should base the processing of data from the input stream buffer on the format specified in the [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) function and any flags passed to the **Process** function with the input stream buffer.</span></span> <span data-ttu-id="43681-126">Copiare i dati del buffer del flusso di input elaborato nel buffer del flusso di output.</span><span class="sxs-lookup"><span data-stu-id="43681-126">Copy the processed input stream buffer data to the output stream buffer.</span></span> <span data-ttu-id="43681-127">Impostare il parametro BufferFlags del buffer del flusso di output [**come \_ buffer XAPO \_ valido**](/windows/desktop/api/xapo/ne-xapo-xapo_buffer_flags) o **XAPO \_ buffer invisibile all' \_ utente**.</span><span class="sxs-lookup"><span data-stu-id="43681-127">Set the output stream buffer's BufferFlags parameter as either [**XAPO\_BUFFER\_VALID**](/windows/desktop/api/xapo/ne-xapo-xapo_buffer_flags) or **XAPO\_BUFFER\_SILENT**.</span></span>

<span data-ttu-id="43681-128">Nell'esempio seguente viene illustrata un'implementazione di [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) e [**Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process) che copia semplicemente i dati da un buffer di input a un buffer di output.</span><span class="sxs-lookup"><span data-stu-id="43681-128">The following example demonstrates a [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) and [**Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process) implementation that simply copies data from an input buffer to an output buffer.</span></span> <span data-ttu-id="43681-129">Tuttavia, non esiste alcuna elaborazione se il buffer di input è contrassegnato con il [**\_ buffer XAPO invisibile all' \_ utente**](/windows/desktop/api/xapo/ne-xapo-xapo_buffer_flags).</span><span class="sxs-lookup"><span data-stu-id="43681-129">However, there is no processing if the input buffer is marked with [**XAPO\_BUFFER\_SILENT**](/windows/desktop/api/xapo/ne-xapo-xapo_buffer_flags).</span></span>


```
STDMETHOD(LockForProcess) (UINT32 InputLockedParameterCount,
          const XAPO_LOCKFORPROCESS_BUFFER_PARAMETERS* pInputLockedParameters,
          UINT32 OutputLockedParameterCount,
          const XAPO_LOCKFORPROCESS_BUFFER_PARAMETERS* pOutputLockedParameters)
{
    assert(!IsLocked());
    assert(InputLockedParameterCount == 1);
    assert(OutputLockedParameterCount == 1);
    assert(pInputLockedParameters != NULL);
    assert(pOutputLockedParameters != NULL);
    assert(pInputLockedParameters[0].pFormat != NULL);
    assert(pOutputLockedParameters[0].pFormat != NULL);


    m_uChannels = pInputLockedParameters[0].pFormat->nChannels;
    m_uBytesPerSample = (pInputLockedParameters[0].pFormat->wBitsPerSample >> 3);

    return CXAPOBase::LockForProcess(
        InputLockedParameterCount,
        pInputLockedParameters,
        OutputLockedParameterCount,
        pOutputLockedParameters);
}
STDMETHOD_(void, Process)(UINT32 InputProcessParameterCount,
           const XAPO_PROCESS_BUFFER_PARAMETERS* pInputProcessParameters,
           UINT32 OutputProcessParameterCount,
           XAPO_PROCESS_BUFFER_PARAMETERS* pOutputProcessParameters,
           BOOL IsEnabled)
{
    assert(IsLocked());
    assert(InputProcessParameterCount == 1);
    assert(OutputProcessParameterCount == 1);
    assert(NULL != pInputProcessParameters);
    assert(NULL != pOutputProcessParameters);


    XAPO_BUFFER_FLAGS inFlags = pInputProcessParameters[0].BufferFlags;
    XAPO_BUFFER_FLAGS outFlags = pOutputProcessParameters[0].BufferFlags;

    // assert buffer flags are legitimate
    assert(inFlags == XAPO_BUFFER_VALID || inFlags == XAPO_BUFFER_SILENT);
    assert(outFlags == XAPO_BUFFER_VALID || outFlags == XAPO_BUFFER_SILENT);

    // check input APO_BUFFER_FLAGS
    switch (inFlags)
    {
    case XAPO_BUFFER_VALID:
        {
            void* pvSrc = pInputProcessParameters[0].pBuffer;
            assert(pvSrc != NULL);

            void* pvDst = pOutputProcessParameters[0].pBuffer;
            assert(pvDst != NULL);

            memcpy(pvDst,pvSrc,pInputProcessParameters[0].ValidFrameCount * m_uChannels * m_uBytesPerSample);
            break;
        }

    case XAPO_BUFFER_SILENT:
        {
            // All that needs to be done for this case is setting the
            // output buffer flag to XAPO_BUFFER_SILENT which is done below.
            break;
        }

    }

    // set destination valid frame count, and buffer flags
    pOutputProcessParameters[0].ValidFrameCount = pInputProcessParameters[0].ValidFrameCount; // set destination frame count same as source
    pOutputProcessParameters[0].BufferFlags     = pInputProcessParameters[0].BufferFlags;     // set destination buffer flags same as source

}
```



<span data-ttu-id="43681-130">Quando si scrive un metodo di [**processo**](/windows/win32/api/xapo/nf-xapo-ixapo-process) , è importante notare che i dati audio XAudio2 sono Interleaved.</span><span class="sxs-lookup"><span data-stu-id="43681-130">When writing a [**Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process) method, it is important to note XAudio2 audio data is interleaved.</span></span> <span data-ttu-id="43681-131">Ciò significa che i dati di ogni canale sono adiacenti per un determinato numero di campione.</span><span class="sxs-lookup"><span data-stu-id="43681-131">This means data from each channel is adjacent for a particular sample number.</span></span> <span data-ttu-id="43681-132">Se ad esempio è presente un'onda a 4 canali in una voce di origine XAudio2, i dati audio sono un campione di Channel 0, un campione di Channel 1, un campione di Channel 2, un campione di Channel 3 e quindi il campione successivo di canali 0, 1, 2, 3 e così via.</span><span class="sxs-lookup"><span data-stu-id="43681-132">For example, if there is a 4-channel wave playing into an XAudio2 source voice, the audio data is a sample of channel 0, a sample of channel 1, a sample of channel 2, a sample of channel 3, and then the next sample of channels 0, 1, 2, 3, and so on.</span></span>

## <a name="related-topics"></a><span data-ttu-id="43681-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="43681-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43681-134">Effetti audio</span><span class="sxs-lookup"><span data-stu-id="43681-134">Audio Effects</span></span>](audio-effects.md)
</dt> <dt>

[<span data-ttu-id="43681-135">Panoramica di XAPO</span><span class="sxs-lookup"><span data-stu-id="43681-135">XAPO Overview</span></span>](xapo-overview.md)
</dt> </dl>

 

 
