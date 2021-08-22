---
description: Rendering di un flusso
ms.assetid: 00bfcfd1-6592-43e3-90ad-730c92aa4cd3
title: Rendering di un flusso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a49632e89e42e4e353cec48ee993f990904bc4557c0f63fcaec4d13bed5becf3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119318571"
---
# <a name="rendering-a-stream"></a>Rendering di un flusso

Il client chiama i metodi [**nell'interfaccia IAudioRenderClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiorenderclient) per scrivere i dati di rendering in un buffer dell'endpoint. Per un flusso in modalità condivisa, il client condivide il buffer dell'endpoint con il motore audio. Per un flusso in modalità esclusiva, il client condivide il buffer dell'endpoint con il dispositivo audio. Per richiedere un buffer dell'endpoint di una determinata dimensione, il client chiama il [**metodo IAudioClient::Initialize.**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) Per ottenere la dimensione del buffer allocato, che potrebbe essere diversa dalla dimensione richiesta, il client chiama il [**metodo IAudioClient::GetBufferSize.**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getbuffersize)

Per spostare un flusso di dati di rendering tramite il buffer dell'endpoint, il client chiama in alternativa il metodo [**IAudioRenderClient::GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) e [**il metodo IAudioRenderClient::ReleaseBuffer.**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-releasebuffer) Il client accede ai dati nel buffer dell'endpoint come una serie di pacchetti di dati. La **chiamata GetBuffer** recupera il pacchetto successivo in modo che il client possa riempirlo con i dati di rendering. Dopo aver scritto i dati nel pacchetto, il client chiama **ReleaseBuffer** per aggiungere il pacchetto completato alla coda di rendering.

Per un buffer di rendering, il valore della spaziatura interna segnalato dal metodo [**IAudioClient::GetCurrentPadding**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getcurrentpadding) rappresenta la quantità di dati di rendering accodati per la riproduzione nel buffer. Un'applicazione per il rendering può usare il valore di spaziatura interna per determinare la quantità di nuovi dati che può scrivere in modo sicuro nel buffer senza il rischio di sovrascrivere i dati scritti in precedenza che il motore audio non ha ancora letto dal buffer. Lo spazio disponibile è semplicemente la dimensione del buffer meno la dimensione del riempimento. Il client può richiedere una dimensione del pacchetto che rappresenta parte o tutto lo spazio disponibile nella chiamata [**GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) successiva.

Le dimensioni di un pacchetto sono espresse in *fotogrammi audio*. Un frame audio in un flusso PCM è un set di campioni (il set contiene un campione per ogni canale nel flusso) che vengono riprodotti o registrati contemporaneamente (tick del clock). Di conseguenza, le dimensioni di un frame audio sono le dimensioni del campione moltiplicate per il numero di canali nel flusso. Ad esempio, la dimensione del frame per un flusso stereo (a 2 canali) con campioni a 16 bit è di quattro byte.

L'esempio di codice seguente illustra come riprodurre un flusso audio nel dispositivo di rendering predefinito:


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



Nell'esempio precedente la funzione PlayAudioStream accetta un solo parametro, , ovvero un puntatore a un oggetto che appartiene a una classe definita dal client, MyAudioSource, con due funzioni `pMySource` membro, LoadData e SetFormat. Il codice di esempio non include l'implementazione di MyAudioSource perché:

-   Nessuno dei membri della classe comunica direttamente con nessuno dei metodi nelle interfacce in WASAPI.
-   La classe può essere implementata in diversi modi, a seconda dei requisiti del client. Ad esempio, potrebbe leggere i dati di rendering da un file WAV ed eseguire la conversione in tempo reale nel formato di flusso.

Tuttavia, alcune informazioni sul funzionamento delle due funzioni sono utili per comprendere l'esempio.

La funzione LoadData scrive un numero specificato di fotogrammi audio (primo parametro) in una posizione del buffer specificata (secondo parametro). Le dimensioni di un fotogramma audio sono il numero di canali nel flusso moltiplicato per le dimensioni del campione. La funzione PlayAudioStream usa LoadData per riempire parti del buffer condiviso con dati audio. La funzione SetFormat specifica il formato per la funzione LoadData da usare per i dati. Se la funzione LoadData è in grado di scrivere almeno un frame nella posizione del buffer specificata, ma esaure i dati prima di scrivere il numero specificato di frame, scrive silenzio nei frame rimanenti.

Se LoadData riesce a scrivere almeno un frame di dati reali (non silenzio) nella posizione del buffer specificata, restituisce 0 tramite il terzo parametro, che, nell'esempio di codice precedente, è un puntatore di output alla `flags` variabile. Quando LoadData non contiene dati e non è in grado di scrivere nemmeno un singolo frame nella posizione del buffer specificata, non scrive nulla nel buffer (neanche in silenzio) e scrive il valore AUDCLNT \_ BUFFERFLAGS SILENT nella \_ `flags` variabile. La variabile trasmette questo valore al metodo `flags` [**IAudioRenderClient::ReleaseBuffer,**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-releasebuffer) che risponde riempiendo il numero specificato di frame nel buffer con silenzio.

Nella chiamata al metodo [**IAudioClient::Initialize,**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) la funzione PlayAudioStream nell'esempio precedente richiede un buffer condiviso con una durata di un secondo. Il buffer allocato potrebbe avere una durata leggermente più lunga. Nelle chiamate iniziali ai metodi [**IAudioRenderClient::GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) e [**IAudioRenderClient::ReleaseBuffer,**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-releasebuffer) la funzione riempie l'intero buffer prima di chiamare il metodo [**IAudioClient::Start**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-start) per iniziare a riprodurre il buffer.

All'interno del ciclo principale, la funzione riempie in modo iterativo metà del buffer a intervalli di mezzo secondo. Subito prima di ogni chiamata alla Windows [**sospensione**](/windows/win32/api/synchapi/nf-synchapi-sleep) nel ciclo principale, il buffer è pieno o quasi pieno. Quando la **chiamata Sleep** viene restituita, il buffer è circa mezzo pieno. Il ciclo termina dopo la chiamata finale alla funzione LoadData imposta la variabile sul `flags` valore AUDCLNT \_ BUFFERFLAGS \_ SILENT. A questo punto, il buffer contiene almeno un frame di dati reali e può contenere fino a mezzo secondo di dati reali. Il resto del buffer contiene silenzio. La **chiamata Sleep** che segue il ciclo fornisce tempo sufficiente (mezzo secondo) per riprodurre tutti i dati rimanenti. Il silenzio che segue i dati impedisce suoni indesiderati prima che la chiamata al [**metodo IAudioClient::Stop**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-stop) arresti il flusso audio. Per altre informazioni su **Sleep,** vedere la documentazione Windows SDK.

Dopo la chiamata al metodo [**IAudioClient::Initialize,**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) il flusso rimane aperto fino a quando il client non rilascia tutti i relativi riferimenti [**all'interfaccia IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) e a tutti i riferimenti alle interfacce del servizio ottenute dal client tramite il [**metodo IAudioClient::GetService.**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) La chiamata [**release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) finale chiude il flusso.

La funzione PlayAudioStream nell'esempio di codice precedente chiama la funzione [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per creare un enumeratore per i dispositivi endpoint audio nel sistema. A meno che il programma chiamante non chiami in precedenza la funzione **CoCreateInstance** o [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) per inizializzare la libreria COM, la **chiamata a CoCreateInstance** avrà esito negativo. Per altre informazioni su **CoCreateInstance,** **CoCreateInstance** e **CoInitializeEx,** vedere la documentazione Windows SDK.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione dei flussi](stream-management.md)
</dt> </dl>

 

 
