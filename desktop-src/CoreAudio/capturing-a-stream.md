---
description: Acquisizione di un flusso
ms.assetid: 1d9072dc-4f9b-4111-a747-5eb33ad3ae5b
title: Acquisizione di un flusso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 371d4b92b97a26e81074edee68216255d576e614
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877857"
---
# <a name="capturing-a-stream"></a><span data-ttu-id="478fc-103">Acquisizione di un flusso</span><span class="sxs-lookup"><span data-stu-id="478fc-103">Capturing a Stream</span></span>

<span data-ttu-id="478fc-104">Il client chiama i metodi nell'interfaccia [**IAudioCaptureClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient) per leggere i dati acquisiti da un buffer dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="478fc-104">The client calls the methods in the [**IAudioCaptureClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient) interface to read captured data from an endpoint buffer.</span></span> <span data-ttu-id="478fc-105">Il client condivide il buffer dell'endpoint con il motore audio in modalità condivisa e con il dispositivo audio in modalità esclusiva.</span><span class="sxs-lookup"><span data-stu-id="478fc-105">The client shares the endpoint buffer with the audio engine in shared mode and with the audio device in exclusive mode.</span></span> <span data-ttu-id="478fc-106">Per richiedere un buffer dell'endpoint di una determinata dimensione, il client chiama il metodo [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) .</span><span class="sxs-lookup"><span data-stu-id="478fc-106">To request an endpoint buffer of a particular size, the client calls the [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) method.</span></span> <span data-ttu-id="478fc-107">Per ottenere le dimensioni del buffer allocato, che potrebbe essere diverso dalla dimensione richiesta, il client chiama il metodo [**IAudioClient:: GetBufferSize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getbuffersize) .</span><span class="sxs-lookup"><span data-stu-id="478fc-107">To get the size of the allocated buffer, which might be different from the requested size, the client calls the [**IAudioClient::GetBufferSize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getbuffersize) method.</span></span>

<span data-ttu-id="478fc-108">Per spostare un flusso di dati acquisiti tramite il buffer dell'endpoint, il client chiama in modo alternativo il metodo [**IAudioCaptureClient:: GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) e il metodo [**IAudioCaptureClient:: ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-releasebuffer) .</span><span class="sxs-lookup"><span data-stu-id="478fc-108">To move a stream of captured data through the endpoint buffer, the client alternately calls the [**IAudioCaptureClient::GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) method and the [**IAudioCaptureClient::ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-releasebuffer) method.</span></span> <span data-ttu-id="478fc-109">Il client accede ai dati nel buffer dell'endpoint come una serie di pacchetti di dati.</span><span class="sxs-lookup"><span data-stu-id="478fc-109">The client accesses the data in the endpoint buffer as a series of data packets.</span></span> <span data-ttu-id="478fc-110">La chiamata a **GetBuffer** Recupera il pacchetto successivo di dati acquisiti dal buffer.</span><span class="sxs-lookup"><span data-stu-id="478fc-110">The **GetBuffer** call retrieves the next packet of captured data from the buffer.</span></span> <span data-ttu-id="478fc-111">Dopo aver letto i dati dal pacchetto, il client chiama **ReleaseBuffer** per rilasciare il pacchetto e renderlo disponibile per più dati acquisiti.</span><span class="sxs-lookup"><span data-stu-id="478fc-111">After reading the data from the packet, the client calls **ReleaseBuffer** to release the packet and make it available for more captured data.</span></span>

<span data-ttu-id="478fc-112">Le dimensioni del pacchetto possono variare da una chiamata a [**GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) a quella successiva.</span><span class="sxs-lookup"><span data-stu-id="478fc-112">The packet size can vary from one [**GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) call to the next.</span></span> <span data-ttu-id="478fc-113">Prima di chiamare **GetBuffer**, il client ha la possibilità di chiamare il metodo [**IAudioCaptureClient:: GetNextPacketSize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getnextpacketsize) per ottenere in anticipo le dimensioni del pacchetto successivo.</span><span class="sxs-lookup"><span data-stu-id="478fc-113">Before calling **GetBuffer**, the client has the option of calling the [**IAudioCaptureClient::GetNextPacketSize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getnextpacketsize) method to get the size of the next packet in advance.</span></span> <span data-ttu-id="478fc-114">Inoltre, il client può chiamare il metodo [**IAudioClient:: GetCurrentPadding**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getcurrentpadding) per ottenere la quantità totale di dati acquisiti disponibili nel buffer.</span><span class="sxs-lookup"><span data-stu-id="478fc-114">In addition, the client can call the [**IAudioClient::GetCurrentPadding**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getcurrentpadding) method to get the total amount of captured data that is available in the buffer.</span></span> <span data-ttu-id="478fc-115">In qualsiasi istante, le dimensioni del pacchetto sono sempre inferiori o uguali alla quantità totale di dati acquisiti nel buffer.</span><span class="sxs-lookup"><span data-stu-id="478fc-115">At any instant, the packet size is always less than or equal to the total amount of captured data in the buffer.</span></span>

<span data-ttu-id="478fc-116">Durante ogni passaggio di elaborazione, il client ha la possibilità di elaborare i dati acquisiti in uno dei modi seguenti:</span><span class="sxs-lookup"><span data-stu-id="478fc-116">During each processing pass, the client has the option of processing the captured data in one of the following ways:</span></span>

-   <span data-ttu-id="478fc-117">Il client chiama in alternativa [**GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) e [**ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-releasebuffer), leggendo un pacchetto con ogni coppia di chiamate, finché **GetBuffer** restituisce AUDCNT \_ S \_ BUFFEREMPTY, a indicare che il buffer è vuoto.</span><span class="sxs-lookup"><span data-stu-id="478fc-117">The client alternately calls [**GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) and [**ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-releasebuffer), reading one packet with each pair of calls, until **GetBuffer** returns AUDCNT\_S\_BUFFEREMPTY, indicating that the buffer is empty.</span></span>
-   <span data-ttu-id="478fc-118">Il client chiama [**GetNextPacketSize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getnextpacketsize) prima di ogni coppia di chiamate a [**GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) e [**ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-releasebuffer) fino a quando **GetNextPacketSize** segnala una dimensione del pacchetto pari a 0, che indica che il buffer è vuoto.</span><span class="sxs-lookup"><span data-stu-id="478fc-118">The client calls [**GetNextPacketSize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getnextpacketsize) before each pair of calls to [**GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) and [**ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-releasebuffer) until **GetNextPacketSize** reports a packet size of 0, indicating that the buffer is empty.</span></span>

<span data-ttu-id="478fc-119">Le due tecniche producono risultati equivalenti.</span><span class="sxs-lookup"><span data-stu-id="478fc-119">The two techniques yield equivalent results.</span></span>

<span data-ttu-id="478fc-120">Nell'esempio di codice seguente viene illustrato come registrare un flusso audio dal dispositivo di acquisizione predefinito:</span><span class="sxs-lookup"><span data-stu-id="478fc-120">The following code example shows how to record an audio stream from the default capture device:</span></span>


```C++
//-----------------------------------------------------------
// Record an audio stream from the default audio capture
// device. The RecordAudioStream function allocates a shared
// buffer big enough to hold one second of PCM audio data.
// The function uses this buffer to stream data from the
// capture device. The main loop runs every 1/2 second.
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
const IID IID_IAudioCaptureClient = __uuidof(IAudioCaptureClient);

HRESULT RecordAudioStream(MyAudioSink *pMySink)
{
    HRESULT hr;
    REFERENCE_TIME hnsRequestedDuration = REFTIMES_PER_SEC;
    REFERENCE_TIME hnsActualDuration;
    UINT32 bufferFrameCount;
    UINT32 numFramesAvailable;
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDevice *pDevice = NULL;
    IAudioClient *pAudioClient = NULL;
    IAudioCaptureClient *pCaptureClient = NULL;
    WAVEFORMATEX *pwfx = NULL;
    UINT32 packetLength = 0;
    BOOL bDone = FALSE;
    BYTE *pData;
    DWORD flags;

    hr = CoCreateInstance(
           CLSID_MMDeviceEnumerator, NULL,
           CLSCTX_ALL, IID_IMMDeviceEnumerator,
           (void**)&pEnumerator);
    EXIT_ON_ERROR(hr)

    hr = pEnumerator->GetDefaultAudioEndpoint(
                        eCapture, eConsole, &pDevice);
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

    // Get the size of the allocated buffer.
    hr = pAudioClient->GetBufferSize(&bufferFrameCount);
    EXIT_ON_ERROR(hr)

    hr = pAudioClient->GetService(
                         IID_IAudioCaptureClient,
                         (void**)&pCaptureClient);
    EXIT_ON_ERROR(hr)

    // Notify the audio sink which format to use.
    hr = pMySink->SetFormat(pwfx);
    EXIT_ON_ERROR(hr)

    // Calculate the actual duration of the allocated buffer.
    hnsActualDuration = (double)REFTIMES_PER_SEC *
                     bufferFrameCount / pwfx->nSamplesPerSec;

    hr = pAudioClient->Start();  // Start recording.
    EXIT_ON_ERROR(hr)

    // Each loop fills about half of the shared buffer.
    while (bDone == FALSE)
    {
        // Sleep for half the buffer duration.
        Sleep(hnsActualDuration/REFTIMES_PER_MILLISEC/2);

        hr = pCaptureClient->GetNextPacketSize(&packetLength);
        EXIT_ON_ERROR(hr)

        while (packetLength != 0)
        {
            // Get the available data in the shared buffer.
            hr = pCaptureClient->GetBuffer(
                                   &pData,
                                   &numFramesAvailable,
                                   &flags, NULL, NULL);
            EXIT_ON_ERROR(hr)

            if (flags & AUDCLNT_BUFFERFLAGS_SILENT)
            {
                pData = NULL;  // Tell CopyData to write silence.
            }

            // Copy the available capture data to the audio sink.
            hr = pMySink->CopyData(
                              pData, numFramesAvailable, &bDone);
            EXIT_ON_ERROR(hr)

            hr = pCaptureClient->ReleaseBuffer(numFramesAvailable);
            EXIT_ON_ERROR(hr)

            hr = pCaptureClient->GetNextPacketSize(&packetLength);
            EXIT_ON_ERROR(hr)
        }
    }

    hr = pAudioClient->Stop();  // Stop recording.
    EXIT_ON_ERROR(hr)

Exit:
    CoTaskMemFree(pwfx);
    SAFE_RELEASE(pEnumerator)
    SAFE_RELEASE(pDevice)
    SAFE_RELEASE(pAudioClient)
    SAFE_RELEASE(pCaptureClient)

    return hr;
}
```



<span data-ttu-id="478fc-121">Nell'esempio precedente, la funzione RecordAudioStream accetta un solo parametro, `pMySink` , che è un puntatore a un oggetto che appartiene a una classe definita dal client, MyAudioSink, con due funzioni, CopyData e Formatter.</span><span class="sxs-lookup"><span data-stu-id="478fc-121">In the preceding example, the RecordAudioStream function takes a single parameter, `pMySink`, which is a pointer to an object that belongs to a client-defined class, MyAudioSink, with two functions, CopyData and SetFormat.</span></span> <span data-ttu-id="478fc-122">Il codice di esempio non include l'implementazione di MyAudioSink perché:</span><span class="sxs-lookup"><span data-stu-id="478fc-122">The example code does not include the implementation of MyAudioSink because:</span></span>

-   <span data-ttu-id="478fc-123">Nessuno dei membri della classe comunica direttamente con uno dei metodi nelle interfacce in WASAPI.</span><span class="sxs-lookup"><span data-stu-id="478fc-123">None of the class members communicates directly with any of the methods in the interfaces in WASAPI.</span></span>
-   <span data-ttu-id="478fc-124">La classe può essere implementata in diversi modi, a seconda dei requisiti del client.</span><span class="sxs-lookup"><span data-stu-id="478fc-124">The class could be implemented in a variety of ways, depending on the requirements of the client.</span></span> <span data-ttu-id="478fc-125">Ad esempio, potrebbe scrivere i dati di acquisizione in un file WAV.</span><span class="sxs-lookup"><span data-stu-id="478fc-125">(For example, it might write the capture data to a WAV file.)</span></span>

<span data-ttu-id="478fc-126">Tuttavia, le informazioni sul funzionamento dei due metodi sono utili per comprendere l'esempio.</span><span class="sxs-lookup"><span data-stu-id="478fc-126">However, information about the operation of the two methods is useful for understanding the example.</span></span>

<span data-ttu-id="478fc-127">La funzione CopyData copia un numero specificato di frame audio da una posizione del buffer specificata.</span><span class="sxs-lookup"><span data-stu-id="478fc-127">The CopyData function copies a specified number of audio frames from a specified buffer location.</span></span> <span data-ttu-id="478fc-128">La funzione RecordAudioStream usa la funzione CopyData per leggere e salvare i dati audio dal buffer condiviso.</span><span class="sxs-lookup"><span data-stu-id="478fc-128">The RecordAudioStream function uses the CopyData function to read and save the audio data from the shared buffer.</span></span> <span data-ttu-id="478fc-129">La funzione seformatt specifica il formato per la funzione CopyData da utilizzare per i dati.</span><span class="sxs-lookup"><span data-stu-id="478fc-129">The SetFormat function specifies the format for the CopyData function to use for the data.</span></span>

<span data-ttu-id="478fc-130">Finché l'oggetto MyAudioSink richiede dati aggiuntivi, la funzione CopyData restituisce il valore **false** tramite il terzo parametro, che, nell'esempio di codice precedente, è un puntatore alla variabile `bDone` .</span><span class="sxs-lookup"><span data-stu-id="478fc-130">As long as the MyAudioSink object requires additional data, the CopyData function outputs the value **FALSE** through its third parameter, which, in the preceding code example, is a pointer to the variable `bDone`.</span></span> <span data-ttu-id="478fc-131">Quando l'oggetto MyAudioSink dispone di tutti i dati necessari, la funzione CopyData imposta `bDone` su **true**, che fa sì che il programma esca dal ciclo nella funzione RecordAudioStream.</span><span class="sxs-lookup"><span data-stu-id="478fc-131">When the MyAudioSink object has all the data that it requires, the CopyData function sets `bDone` to **TRUE**, which causes the program to exit the loop in the RecordAudioStream function.</span></span>

<span data-ttu-id="478fc-132">La funzione RecordAudioStream alloca un buffer condiviso con una durata di un secondo.</span><span class="sxs-lookup"><span data-stu-id="478fc-132">The RecordAudioStream function allocates a shared buffer that has a duration of one second.</span></span> <span data-ttu-id="478fc-133">Il buffer allocato potrebbe avere una durata leggermente superiore. All'interno del ciclo principale, la chiamata alla funzione di [**sospensione**](/windows/desktop/api/synchapi/nf-synchapi-sleep) di Windows fa sì che il programma attenda un mezzo secondo.</span><span class="sxs-lookup"><span data-stu-id="478fc-133">(The allocated buffer might have a slightly longer duration.) Within the main loop, the call to the Windows [**Sleep**](/windows/desktop/api/synchapi/nf-synchapi-sleep) function causes the program to wait for a half second.</span></span> <span data-ttu-id="478fc-134">All'inizio di ogni chiamata di **sospensione** , il buffer condiviso è vuoto o quasi vuoto.</span><span class="sxs-lookup"><span data-stu-id="478fc-134">At the start of each **Sleep** call, the shared buffer is empty or nearly empty.</span></span> <span data-ttu-id="478fc-135">Quando la chiamata di **sospensione** viene restituita, il buffer condiviso è circa la metà dei dati di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="478fc-135">By the time the **Sleep** call returns, the shared buffer is about half filled with capture data.</span></span>

<span data-ttu-id="478fc-136">Dopo la chiamata al metodo [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) , il flusso rimane aperto finché il client non rilascia tutti i relativi riferimenti all'interfaccia [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) e a tutti i riferimenti alle interfacce del servizio ottenute dal client tramite il metodo [**IAudioClient:: GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) .</span><span class="sxs-lookup"><span data-stu-id="478fc-136">Following the call to the [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) method, the stream remains open until the client releases all of its references to the [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) interface and to all references to service interfaces that the client obtained through the [**IAudioClient::GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) method.</span></span> <span data-ttu-id="478fc-137">La chiamata alla [**versione**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) finale chiude il flusso.</span><span class="sxs-lookup"><span data-stu-id="478fc-137">The final [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) call closes the stream.</span></span>

## <a name="related-topics"></a><span data-ttu-id="478fc-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="478fc-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="478fc-139">Gestione dei flussi</span><span class="sxs-lookup"><span data-stu-id="478fc-139">Stream Management</span></span>](stream-management.md)
</dt> </dl>

 

 
