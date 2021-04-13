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
# <a name="rendering-a-stream"></a>Rendering di un flusso

Il client chiama i metodi nell'interfaccia [**IAudioRenderClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiorenderclient) per scrivere i dati di rendering in un buffer dell'endpoint. Per un flusso in modalità condivisa, il client condivide il buffer dell'endpoint con il motore audio. Per un flusso in modalità esclusiva, il client condivide il buffer dell'endpoint con il dispositivo audio. Per richiedere un buffer dell'endpoint di una determinata dimensione, il client chiama il metodo [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) . Per ottenere le dimensioni del buffer allocato, che potrebbe essere diverso dalla dimensione richiesta, il client chiama il metodo [**IAudioClient:: GetBufferSize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getbuffersize) .

Per spostare un flusso di dati di rendering tramite il buffer dell'endpoint, il client chiama in modo alternativo il metodo [**IAudioRenderClient:: GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) e il metodo [**IAudioRenderClient:: ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-releasebuffer) . Il client accede ai dati nel buffer dell'endpoint come una serie di pacchetti di dati. La chiamata a **GetBuffer** Recupera il pacchetto successivo in modo che il client possa riempirlo con i dati di rendering. Dopo aver scritto i dati nel pacchetto, il client chiama **ReleaseBuffer** per aggiungere il pacchetto completato alla coda di rendering.

Per un buffer di rendering, il valore di riempimento riportato dal metodo [**IAudioClient:: GetCurrentPadding**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getcurrentpadding) rappresenta la quantità di dati di rendering accodati per la riproduzione nel buffer. Un'applicazione di rendering può usare il valore di riempimento per determinare la quantità di nuovi dati che è in grado di scrivere nel buffer senza il rischio di sovrascrivere i dati scritti in precedenza che il motore audio non ha ancora letto dal buffer. Lo spazio disponibile è semplicemente la dimensione del buffer meno le dimensioni della spaziatura interna. Il client può richiedere una dimensione del pacchetto che rappresenta parte o tutto lo spazio disponibile nella successiva chiamata [**GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) .

Le dimensioni di un pacchetto sono espresse in *frame audio*. Un frame audio in un flusso PCM è costituito da un set di esempi (il set contiene un campione per ogni canale nel flusso) che viene riprodotto o registrato allo stesso tempo (tick Clock). Quindi, le dimensioni di un frame audio sono le dimensioni di esempio moltiplicate per il numero di canali nel flusso. Ad esempio, le dimensioni del frame per un flusso stereo (2 canali) con campioni a 16 bit sono quattro byte.

Nell'esempio di codice seguente viene illustrato come riprodurre un flusso audio sul dispositivo di rendering predefinito:


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



Nell'esempio precedente, la funzione PlayAudioStream accetta un solo parametro, `pMySource` , che è un puntatore a un oggetto che appartiene a una classe definita dal client, MyAudioSource, con due funzioni membro, LoadData e Formatter. Il codice di esempio non include l'implementazione di MyAudioSource perché:

-   Nessuno dei membri della classe comunica direttamente con uno dei metodi nelle interfacce in WASAPI.
-   La classe può essere implementata in diversi modi, a seconda dei requisiti del client. Ad esempio, potrebbe leggere i dati di rendering da un file WAV ed eseguire la conversione in tempo reale nel formato del flusso.

Tuttavia, alcune informazioni sul funzionamento delle due funzioni sono utili per comprendere l'esempio.

La funzione LoadData scrive un numero specificato di fotogrammi audio (primo parametro) in una posizione del buffer specificata (secondo parametro). (La dimensione di un frame audio è il numero di canali nel flusso moltiplicato per le dimensioni del campione.) La funzione PlayAudioStream USA LoadData per riempire parti del buffer condiviso con dati audio. La funzione seformatt specifica il formato per la funzione LoadData da utilizzare per i dati. Se la funzione LoadData è in grado di scrivere almeno un frame nella posizione del buffer specificata, ma esaurisce i dati prima di scrivere il numero specificato di frame, scrive il silenzio nei frame rimanenti.

Fino a quando LoadData riesce a scrivere almeno un frame di dati reali (non in silenzio) nella posizione del buffer specificata, restituisce 0 tramite il terzo parametro, che, nell'esempio di codice precedente, è un puntatore di output alla `flags` variabile. Quando LoadData non è presente nei dati e non è in grado di scrivere neanche un singolo frame nella posizione del buffer specificata, non scrive nulla nel buffer (anche in silenzio) e scrive il valore AUDCLNT \_ BUFFERFLAGS \_ invisibile alla `flags` variabile. La `flags` variabile trasmette questo valore al metodo [**IAudioRenderClient:: ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-releasebuffer) , che risponde compilando il numero specificato di frame nel buffer con il silenzio.

Nella chiamata al metodo [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) la funzione PlayAudioStream nell'esempio precedente richiede un buffer condiviso con una durata di un secondo. Il buffer allocato potrebbe avere una durata leggermente superiore. Nelle chiamate iniziali ai metodi [**IAudioRenderClient:: GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) e [**IAudioRenderClient:: ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-releasebuffer) , la funzione riempie l'intero buffer prima di chiamare il metodo [**IAudioClient:: Start**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-start) per iniziare a riprodurre il buffer.

All'interno del ciclo principale, la funzione riempie in modo iterativo la metà del buffer a intervalli di mezzo secondo. Appena prima di ogni chiamata alla funzione di [**sospensione**](/windows/win32/api/synchapi/nf-synchapi-sleep) di Windows nel ciclo principale, il buffer è pieno o quasi pieno. Quando la chiamata di **sospensione** restituisce, il buffer è circa la metà piena. Il ciclo termina dopo la chiamata finale alla funzione LoadData imposta la `flags` variabile sul valore AUDCLNT \_ BUFFERFLAGS \_ Silent. A questo punto, il buffer contiene almeno un frame di dati reali e potrebbe contenere fino a un mezzo secondo di dati reali. Il resto del buffer contiene il silenzio. La chiamata di **sospensione** che segue il ciclo fornisce tempo sufficiente (un mezzo secondo) per riprodurre tutti i dati rimanenti. Il silenzio che segue i dati impedisce i suoni indesiderati prima che la chiamata al metodo [**IAudioClient:: Stop**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-stop) arresti il flusso audio. Per ulteriori informazioni sulla **sospensione**, vedere la documentazione Windows SDK.

Dopo la chiamata al metodo [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) , il flusso rimane aperto finché il client non rilascia tutti i relativi riferimenti all'interfaccia [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) e a tutti i riferimenti alle interfacce del servizio ottenute dal client tramite il metodo [**IAudioClient:: GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) . La chiamata alla [**versione**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) finale chiude il flusso.

La funzione PlayAudioStream nell'esempio di codice precedente chiama la funzione [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per creare un enumeratore per i dispositivi dell'endpoint audio nel sistema. A meno che il programma chiamante abbia precedentemente chiamato la funzione **CoCreateInstance** o [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) per inizializzare la libreria com, la chiamata **CoCreateInstance** avrà esito negativo. Per ulteriori informazioni su **CoCreateInstance**, **CoCreateInstance** e **CoInitializeEx**, vedere la documentazione Windows SDK.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione dei flussi](stream-management.md)
</dt> </dl>

 

 
