---
description: Rendering di un flusso
ms.assetid: 00bfcfd1-6592-43e3-90ad-730c92aa4cd3
title: Rendering di un flusso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d96e720bab43c75b0a3958bb3b6137d3a3d9ef6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483477"
---
# <a name="rendering-a-stream"></a><span data-ttu-id="ff990-103">Rendering di un flusso</span><span class="sxs-lookup"><span data-stu-id="ff990-103">Rendering a Stream</span></span>

<span data-ttu-id="ff990-104">Il client chiama i metodi nell'interfaccia [**IAudioRenderClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiorenderclient) per scrivere i dati di rendering in un buffer dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="ff990-104">The client calls the methods in the [**IAudioRenderClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiorenderclient) interface to write rendering data to an endpoint buffer.</span></span> <span data-ttu-id="ff990-105">Per un flusso in modalità condivisa, il client condivide il buffer dell'endpoint con il motore audio.</span><span class="sxs-lookup"><span data-stu-id="ff990-105">For a shared-mode stream, the client shares the endpoint buffer with the audio engine.</span></span> <span data-ttu-id="ff990-106">Per un flusso in modalità esclusiva, il client condivide il buffer dell'endpoint con il dispositivo audio.</span><span class="sxs-lookup"><span data-stu-id="ff990-106">For an exclusive-mode stream, the client shares the endpoint buffer with the audio device.</span></span> <span data-ttu-id="ff990-107">Per richiedere un buffer dell'endpoint di una determinata dimensione, il client chiama il metodo [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) .</span><span class="sxs-lookup"><span data-stu-id="ff990-107">To request an endpoint buffer of a particular size, the client calls the [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) method.</span></span> <span data-ttu-id="ff990-108">Per ottenere le dimensioni del buffer allocato, che potrebbe essere diverso dalla dimensione richiesta, il client chiama il metodo [**IAudioClient:: GetBufferSize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getbuffersize) .</span><span class="sxs-lookup"><span data-stu-id="ff990-108">To get the size of the allocated buffer, which might be different from the requested size, the client calls the [**IAudioClient::GetBufferSize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getbuffersize) method.</span></span>

<span data-ttu-id="ff990-109">Per spostare un flusso di dati di rendering tramite il buffer dell'endpoint, il client chiama in modo alternativo il metodo [**IAudioRenderClient:: GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) e il metodo [**IAudioRenderClient:: ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-releasebuffer) .</span><span class="sxs-lookup"><span data-stu-id="ff990-109">To move a stream of rendering data through the endpoint buffer, the client alternately calls the [**IAudioRenderClient::GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) method and the [**IAudioRenderClient::ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-releasebuffer) method.</span></span> <span data-ttu-id="ff990-110">Il client accede ai dati nel buffer dell'endpoint come una serie di pacchetti di dati.</span><span class="sxs-lookup"><span data-stu-id="ff990-110">The client accesses the data in the endpoint buffer as a series of data packets.</span></span> <span data-ttu-id="ff990-111">La chiamata a **GetBuffer** Recupera il pacchetto successivo in modo che il client possa riempirlo con i dati di rendering.</span><span class="sxs-lookup"><span data-stu-id="ff990-111">The **GetBuffer** call retrieves the next packet so that the client can fill it with rendering data.</span></span> <span data-ttu-id="ff990-112">Dopo aver scritto i dati nel pacchetto, il client chiama **ReleaseBuffer** per aggiungere il pacchetto completato alla coda di rendering.</span><span class="sxs-lookup"><span data-stu-id="ff990-112">After writing the data to the packet, the client calls **ReleaseBuffer** to add the completed packet to the rendering queue.</span></span>

<span data-ttu-id="ff990-113">Per un buffer di rendering, il valore di riempimento riportato dal metodo [**IAudioClient:: GetCurrentPadding**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getcurrentpadding) rappresenta la quantità di dati di rendering accodati per la riproduzione nel buffer.</span><span class="sxs-lookup"><span data-stu-id="ff990-113">For a rendering buffer, the padding value that is reported by the [**IAudioClient::GetCurrentPadding**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getcurrentpadding) method represents the amount of rendering data that is queued up to play in the buffer.</span></span> <span data-ttu-id="ff990-114">Un'applicazione di rendering può usare il valore di riempimento per determinare la quantità di nuovi dati che è in grado di scrivere nel buffer senza il rischio di sovrascrivere i dati scritti in precedenza che il motore audio non ha ancora letto dal buffer.</span><span class="sxs-lookup"><span data-stu-id="ff990-114">A rendering application can use the padding value to determine how much new data it can safely write to the buffer without the risk of overwriting previously written data that the audio engine has not yet read from the buffer.</span></span> <span data-ttu-id="ff990-115">Lo spazio disponibile è semplicemente la dimensione del buffer meno le dimensioni della spaziatura interna.</span><span class="sxs-lookup"><span data-stu-id="ff990-115">The available space is simply the buffer size minus the padding size.</span></span> <span data-ttu-id="ff990-116">Il client può richiedere una dimensione del pacchetto che rappresenta parte o tutto lo spazio disponibile nella successiva chiamata [**GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) .</span><span class="sxs-lookup"><span data-stu-id="ff990-116">The client can request a packet size that represents some or all of this available space in its next [**GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) call.</span></span>

<span data-ttu-id="ff990-117">Le dimensioni di un pacchetto sono espresse in *frame audio*.</span><span class="sxs-lookup"><span data-stu-id="ff990-117">The size of a packet is expressed in *audio frames*.</span></span> <span data-ttu-id="ff990-118">Un frame audio in un flusso PCM è costituito da un set di esempi (il set contiene un campione per ogni canale nel flusso) che viene riprodotto o registrato allo stesso tempo (tick Clock).</span><span class="sxs-lookup"><span data-stu-id="ff990-118">An audio frame in a PCM stream is a set of samples (the set contains one sample for each channel in the stream) that play or are recorded at the same time (clock tick).</span></span> <span data-ttu-id="ff990-119">Quindi, le dimensioni di un frame audio sono le dimensioni di esempio moltiplicate per il numero di canali nel flusso.</span><span class="sxs-lookup"><span data-stu-id="ff990-119">Thus, the size of an audio frame is the sample size multiplied by the number of channels in the stream.</span></span> <span data-ttu-id="ff990-120">Ad esempio, le dimensioni del frame per un flusso stereo (2 canali) con campioni a 16 bit sono quattro byte.</span><span class="sxs-lookup"><span data-stu-id="ff990-120">For example, the frame size for a stereo (2-channel) stream with 16-bit samples is four bytes.</span></span>

<span data-ttu-id="ff990-121">Nell'esempio di codice seguente viene illustrato come riprodurre un flusso audio sul dispositivo di rendering predefinito:</span><span class="sxs-lookup"><span data-stu-id="ff990-121">The following code example shows how to play an audio stream on the default rendering device:</span></span>


```C++
//-----------------------------------------------------------
// Play an audio stream on the default audio rendering
// device. The PlayAudioStream function allocates a shared
// buffer big enough to hold one second of PCM audio data.
// The function uses this buffer to stream data to the
// rendering device. The inner loop runs every 1/2 second.
//-----------------------------------------------------------

// REFERENCE_TIME time units per second and per millisecond
#define REFTIMES_PER_SEC  10000000
#define REFTIMES_PER_MILLISEC  10000

#define EXIT_ON_ERROR(hres)  \
              if (FAILED(hres)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

const CLSID CLSID_MMDeviceEnumerator = __uuidof(MMDeviceEnumerator);
const IID IID_IMMDeviceEnumerator = __uuidof(IMMDeviceEnumerator);
const IID IID_IAudioClient = __uuidof(IAudioClient);
const IID IID_IAudioRenderClient = __uuidof(IAudioRenderClient);

HRESULT PlayAudioStream(MyAudioSource *pMySource)
{
    HRESULT hr;
    REFERENCE_TIME hnsRequestedDuration = REFTIMES_PER_SEC;
    REFERENCE_TIME hnsActualDuration;
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDevice *pDevice = NULL;
    IAudioClient *pAudioClient = NULL;
    IAudioRenderClient *pRenderClient = NULL;
    WAVEFORMATEX *pwfx = NULL;
    UINT32 bufferFrameCount;
    UINT32 numFramesAvailable;
    UINT32 numFramesPadding;
    BYTE *pData;
    DWORD flags = 0;

    hr = CoCreateInstance(
           CLSID_MMDeviceEnumerator, NULL,
           CLSCTX_ALL, IID_IMMDeviceEnumerator,
           (void**)&pEnumerator);
    EXIT_ON_ERROR(hr)

    hr = pEnumerator->GetDefaultAudioEndpoint(
                        eRender, eConsole, &pDevice);
    EXIT_ON_ERROR(hr)

    hr = pDevice->Activate(
                    IID_IAudioClient, CLSCTX_ALL,
                    NULL, (void**)&pAudioClient);
    EXIT_ON_ERROR(hr)

    hr = pAudioClient->GetMixFormat(&pwfx);
    EXIT_ON_ERROR(hr)

    hr = pAudioClient->Initialize(
                         AUDCLNT_SHAREMODE_SHARED,
                         0,
                         hnsRequestedDuration,
                         0,
                         pwfx,
                         NULL);
    EXIT_ON_ERROR(hr)

    // Tell the audio source which format to use.
    hr = pMySource->SetFormat(pwfx);
    EXIT_ON_ERROR(hr)

    // Get the actual size of the allocated buffer.
    hr = pAudioClient->GetBufferSize(&bufferFrameCount);
    EXIT_ON_ERROR(hr)

    hr = pAudioClient->GetService(
                         IID_IAudioRenderClient,
                         (void**)&pRenderClient);
    EXIT_ON_ERROR(hr)

    // Grab the entire buffer for the initial fill operation.
    hr = pRenderClient->GetBuffer(bufferFrameCount, &pData);
    EXIT_ON_ERROR(hr)

    // Load the initial data into the shared buffer.
    hr = pMySource->LoadData(bufferFrameCount, pData, &flags);
    EXIT_ON_ERROR(hr)

    hr = pRenderClient->ReleaseBuffer(bufferFrameCount, flags);
    EXIT_ON_ERROR(hr)

    // Calculate the actual duration of the allocated buffer.
    hnsActualDuration = (double)REFTIMES_PER_SEC *
                        bufferFrameCount / pwfx->nSamplesPerSec;

    hr = pAudioClient->Start();  // Start playing.
    EXIT_ON_ERROR(hr)

    // Each loop fills about half of the shared buffer.
    while (flags != AUDCLNT_BUFFERFLAGS_SILENT)
    {
        // Sleep for half the buffer duration.
        Sleep((DWORD)(hnsActualDuration/REFTIMES_PER_MILLISEC/2));

        // See how much buffer space is available.
        hr = pAudioClient->GetCurrentPadding(&numFramesPadding);
        EXIT_ON_ERROR(hr)

        numFramesAvailable = bufferFrameCount - numFramesPadding;

        // Grab all the available space in the shared buffer.
        hr = pRenderClient->GetBuffer(numFramesAvailable, &pData);
        EXIT_ON_ERROR(hr)

        // Get next 1/2-second of data from the audio source.
        hr = pMySource->LoadData(numFramesAvailable, pData, &flags);
        EXIT_ON_ERROR(hr)

        hr = pRenderClient->ReleaseBuffer(numFramesAvailable, flags);
        EXIT_ON_ERROR(hr)
    }

    // Wait for last data in buffer to play before stopping.
    Sleep((DWORD)(hnsActualDuration/REFTIMES_PER_MILLISEC/2));

    hr = pAudioClient->Stop();  // Stop playing.
    EXIT_ON_ERROR(hr)

Exit:
    CoTaskMemFree(pwfx);
    SAFE_RELEASE(pEnumerator)
    SAFE_RELEASE(pDevice)
    SAFE_RELEASE(pAudioClient)
    SAFE_RELEASE(pRenderClient)

    return hr;
}
```



<span data-ttu-id="ff990-122">Nell'esempio precedente, la funzione PlayAudioStream accetta un solo parametro, `pMySource` , che è un puntatore a un oggetto che appartiene a una classe definita dal client, MyAudioSource, con due funzioni membro, LoadData e Formatter.</span><span class="sxs-lookup"><span data-stu-id="ff990-122">In the preceding example, the PlayAudioStream function takes a single parameter, `pMySource`, which is a pointer to an object that belongs to a client-defined class, MyAudioSource, with two member functions, LoadData and SetFormat.</span></span> <span data-ttu-id="ff990-123">Il codice di esempio non include l'implementazione di MyAudioSource perché:</span><span class="sxs-lookup"><span data-stu-id="ff990-123">The example code does not include the implementation of MyAudioSource because:</span></span>

-   <span data-ttu-id="ff990-124">Nessuno dei membri della classe comunica direttamente con uno dei metodi nelle interfacce in WASAPI.</span><span class="sxs-lookup"><span data-stu-id="ff990-124">None of the class members communicates directly with any of the methods in the interfaces in WASAPI.</span></span>
-   <span data-ttu-id="ff990-125">La classe può essere implementata in diversi modi, a seconda dei requisiti del client.</span><span class="sxs-lookup"><span data-stu-id="ff990-125">The class could be implemented in a variety of ways, depending on the requirements of the client.</span></span> <span data-ttu-id="ff990-126">Ad esempio, potrebbe leggere i dati di rendering da un file WAV ed eseguire la conversione in tempo reale nel formato del flusso.</span><span class="sxs-lookup"><span data-stu-id="ff990-126">(For example, it might read the rendering data from a WAV file and perform on-the-fly conversion to the stream format.)</span></span>

<span data-ttu-id="ff990-127">Tuttavia, alcune informazioni sul funzionamento delle due funzioni sono utili per comprendere l'esempio.</span><span class="sxs-lookup"><span data-stu-id="ff990-127">However, some information about the operation of the two functions is useful for understanding the example.</span></span>

<span data-ttu-id="ff990-128">La funzione LoadData scrive un numero specificato di fotogrammi audio (primo parametro) in una posizione del buffer specificata (secondo parametro).</span><span class="sxs-lookup"><span data-stu-id="ff990-128">The LoadData function writes a specified number of audio frames (first parameter) to a specified buffer location (second parameter).</span></span> <span data-ttu-id="ff990-129">(La dimensione di un frame audio è il numero di canali nel flusso moltiplicato per le dimensioni del campione.) La funzione PlayAudioStream USA LoadData per riempire parti del buffer condiviso con dati audio.</span><span class="sxs-lookup"><span data-stu-id="ff990-129">(The size of an audio frame is the number of channels in the stream multiplied by the sample size.) The PlayAudioStream function uses LoadData to fill portions of the shared buffer with audio data.</span></span> <span data-ttu-id="ff990-130">La funzione seformatt specifica il formato per la funzione LoadData da utilizzare per i dati.</span><span class="sxs-lookup"><span data-stu-id="ff990-130">The SetFormat function specifies the format for the LoadData function to use for the data.</span></span> <span data-ttu-id="ff990-131">Se la funzione LoadData è in grado di scrivere almeno un frame nella posizione del buffer specificata, ma esaurisce i dati prima di scrivere il numero specificato di frame, scrive il silenzio nei frame rimanenti.</span><span class="sxs-lookup"><span data-stu-id="ff990-131">If the LoadData function is able to write at least one frame to the specified buffer location but runs out of data before it has written the specified number of frames, then it writes silence to the remaining frames.</span></span>

<span data-ttu-id="ff990-132">Fino a quando LoadData riesce a scrivere almeno un frame di dati reali (non in silenzio) nella posizione del buffer specificata, restituisce 0 tramite il terzo parametro, che, nell'esempio di codice precedente, è un puntatore di output alla `flags` variabile.</span><span class="sxs-lookup"><span data-stu-id="ff990-132">As long as LoadData succeeds in writing at least one frame of real data (not silence) to the specified buffer location, it outputs 0 through its third parameter, which, in the preceding code example, is an output pointer to the `flags` variable.</span></span> <span data-ttu-id="ff990-133">Quando LoadData non è presente nei dati e non è in grado di scrivere neanche un singolo frame nella posizione del buffer specificata, non scrive nulla nel buffer (anche in silenzio) e scrive il valore AUDCLNT \_ BUFFERFLAGS \_ invisibile alla `flags` variabile.</span><span class="sxs-lookup"><span data-stu-id="ff990-133">When LoadData is out of data and cannot write even a single frame to the specified buffer location, it writes nothing to the buffer (not even silence), and it writes the value AUDCLNT\_BUFFERFLAGS\_SILENT to the `flags` variable.</span></span> <span data-ttu-id="ff990-134">La `flags` variabile trasmette questo valore al metodo [**IAudioRenderClient:: ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-releasebuffer) , che risponde compilando il numero specificato di frame nel buffer con il silenzio.</span><span class="sxs-lookup"><span data-stu-id="ff990-134">The `flags` variable conveys this value to the [**IAudioRenderClient::ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-releasebuffer) method, which responds by filling the specified number of frames in the buffer with silence.</span></span>

<span data-ttu-id="ff990-135">Nella chiamata al metodo [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) la funzione PlayAudioStream nell'esempio precedente richiede un buffer condiviso con una durata di un secondo.</span><span class="sxs-lookup"><span data-stu-id="ff990-135">In its call to the [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) method, the PlayAudioStream function in the preceding example requests a shared buffer that has a duration of one second.</span></span> <span data-ttu-id="ff990-136">Il buffer allocato potrebbe avere una durata leggermente superiore. Nelle chiamate iniziali ai metodi [**IAudioRenderClient:: GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) e [**IAudioRenderClient:: ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-releasebuffer) , la funzione riempie l'intero buffer prima di chiamare il metodo [**IAudioClient:: Start**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-start) per iniziare a riprodurre il buffer.</span><span class="sxs-lookup"><span data-stu-id="ff990-136">(The allocated buffer might have a slightly longer duration.) In its initial calls to the [**IAudioRenderClient::GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) and [**IAudioRenderClient::ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-releasebuffer) methods, the function fills the entire buffer before calling the [**IAudioClient::Start**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-start) method to begin playing the buffer.</span></span>

<span data-ttu-id="ff990-137">All'interno del ciclo principale, la funzione riempie in modo iterativo la metà del buffer a intervalli di mezzo secondo.</span><span class="sxs-lookup"><span data-stu-id="ff990-137">Within the main loop, the function iteratively fills half of the buffer at half-second intervals.</span></span> <span data-ttu-id="ff990-138">Appena prima di ogni chiamata alla funzione di [**sospensione**](/windows/win32/api/synchapi/nf-synchapi-sleep) di Windows nel ciclo principale, il buffer è pieno o quasi pieno.</span><span class="sxs-lookup"><span data-stu-id="ff990-138">Just before each call to the Windows [**Sleep**](/windows/win32/api/synchapi/nf-synchapi-sleep) function in the main loop, the buffer is full or nearly full.</span></span> <span data-ttu-id="ff990-139">Quando la chiamata di **sospensione** restituisce, il buffer è circa la metà piena.</span><span class="sxs-lookup"><span data-stu-id="ff990-139">When the **Sleep** call returns, the buffer is about half full.</span></span> <span data-ttu-id="ff990-140">Il ciclo termina dopo la chiamata finale alla funzione LoadData imposta la `flags` variabile sul valore AUDCLNT \_ BUFFERFLAGS \_ Silent.</span><span class="sxs-lookup"><span data-stu-id="ff990-140">The loop ends after the final call to the LoadData function sets the `flags` variable to the value AUDCLNT\_BUFFERFLAGS\_SILENT.</span></span> <span data-ttu-id="ff990-141">A questo punto, il buffer contiene almeno un frame di dati reali e potrebbe contenere fino a un mezzo secondo di dati reali.</span><span class="sxs-lookup"><span data-stu-id="ff990-141">At that point, the buffer contains at least one frame of real data, and it might contain as much as a half second of real data.</span></span> <span data-ttu-id="ff990-142">Il resto del buffer contiene il silenzio.</span><span class="sxs-lookup"><span data-stu-id="ff990-142">The remainder of the buffer contains silence.</span></span> <span data-ttu-id="ff990-143">La chiamata di **sospensione** che segue il ciclo fornisce tempo sufficiente (un mezzo secondo) per riprodurre tutti i dati rimanenti.</span><span class="sxs-lookup"><span data-stu-id="ff990-143">The **Sleep** call that follows the loop provides sufficient time (a half second) to play all of the remaining data.</span></span> <span data-ttu-id="ff990-144">Il silenzio che segue i dati impedisce i suoni indesiderati prima che la chiamata al metodo [**IAudioClient:: Stop**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-stop) arresti il flusso audio.</span><span class="sxs-lookup"><span data-stu-id="ff990-144">The silence that follows the data prevents unwanted sounds before the call to the [**IAudioClient::Stop**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-stop) method stops the audio stream.</span></span> <span data-ttu-id="ff990-145">Per ulteriori informazioni sulla **sospensione**, vedere la documentazione Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="ff990-145">For more information about **Sleep**, see the Windows SDK documentation.</span></span>

<span data-ttu-id="ff990-146">Dopo la chiamata al metodo [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) , il flusso rimane aperto finché il client non rilascia tutti i relativi riferimenti all'interfaccia [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) e a tutti i riferimenti alle interfacce del servizio ottenute dal client tramite il metodo [**IAudioClient:: GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) .</span><span class="sxs-lookup"><span data-stu-id="ff990-146">Following the call to the [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) method, the stream remains open until the client releases all of its references to the [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) interface and to all references to service interfaces that the client obtained through the [**IAudioClient::GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) method.</span></span> <span data-ttu-id="ff990-147">La chiamata alla [**versione**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) finale chiude il flusso.</span><span class="sxs-lookup"><span data-stu-id="ff990-147">The final [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) call closes the stream.</span></span>

<span data-ttu-id="ff990-148">La funzione PlayAudioStream nell'esempio di codice precedente chiama la funzione [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per creare un enumeratore per i dispositivi dell'endpoint audio nel sistema.</span><span class="sxs-lookup"><span data-stu-id="ff990-148">The PlayAudioStream function in the preceding code example calls the [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function to create an enumerator for the audio endpoint devices in the system.</span></span> <span data-ttu-id="ff990-149">A meno che il programma chiamante abbia precedentemente chiamato la funzione **CoCreateInstance** o [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) per inizializzare la libreria com, la chiamata **CoCreateInstance** avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="ff990-149">Unless the calling program previously called either the **CoCreateInstance** or [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) function to initialize the COM library, the **CoCreateInstance** call will fail.</span></span> <span data-ttu-id="ff990-150">Per ulteriori informazioni su **CoCreateInstance**, **CoCreateInstance** e **CoInitializeEx**, vedere la documentazione Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="ff990-150">For more information about **CoCreateInstance**, **CoCreateInstance**, and **CoInitializeEx**, see the Windows SDK documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ff990-151">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ff990-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff990-152">Gestione dei flussi</span><span class="sxs-lookup"><span data-stu-id="ff990-152">Stream Management</span></span>](stream-management.md)
</dt> </dl>

 

 
