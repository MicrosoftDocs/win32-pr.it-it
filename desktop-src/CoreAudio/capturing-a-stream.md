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
# <a name="capturing-a-stream"></a>Acquisizione di un flusso

Il client chiama i metodi nell'interfaccia [**IAudioCaptureClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient) per leggere i dati acquisiti da un buffer dell'endpoint. Il client condivide il buffer dell'endpoint con il motore audio in modalità condivisa e con il dispositivo audio in modalità esclusiva. Per richiedere un buffer dell'endpoint di una determinata dimensione, il client chiama il metodo [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) . Per ottenere le dimensioni del buffer allocato, che potrebbe essere diverso dalla dimensione richiesta, il client chiama il metodo [**IAudioClient:: GetBufferSize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getbuffersize) .

Per spostare un flusso di dati acquisiti tramite il buffer dell'endpoint, il client chiama in modo alternativo il metodo [**IAudioCaptureClient:: GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) e il metodo [**IAudioCaptureClient:: ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-releasebuffer) . Il client accede ai dati nel buffer dell'endpoint come una serie di pacchetti di dati. La chiamata a **GetBuffer** Recupera il pacchetto successivo di dati acquisiti dal buffer. Dopo aver letto i dati dal pacchetto, il client chiama **ReleaseBuffer** per rilasciare il pacchetto e renderlo disponibile per più dati acquisiti.

Le dimensioni del pacchetto possono variare da una chiamata a [**GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) a quella successiva. Prima di chiamare **GetBuffer**, il client ha la possibilità di chiamare il metodo [**IAudioCaptureClient:: GetNextPacketSize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getnextpacketsize) per ottenere in anticipo le dimensioni del pacchetto successivo. Inoltre, il client può chiamare il metodo [**IAudioClient:: GetCurrentPadding**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getcurrentpadding) per ottenere la quantità totale di dati acquisiti disponibili nel buffer. In qualsiasi istante, le dimensioni del pacchetto sono sempre inferiori o uguali alla quantità totale di dati acquisiti nel buffer.

Durante ogni passaggio di elaborazione, il client ha la possibilità di elaborare i dati acquisiti in uno dei modi seguenti:

-   Il client chiama in alternativa [**GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) e [**ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-releasebuffer), leggendo un pacchetto con ogni coppia di chiamate, finché **GetBuffer** restituisce AUDCNT \_ S \_ BUFFEREMPTY, a indicare che il buffer è vuoto.
-   Il client chiama [**GetNextPacketSize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getnextpacketsize) prima di ogni coppia di chiamate a [**GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) e [**ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-releasebuffer) fino a quando **GetNextPacketSize** segnala una dimensione del pacchetto pari a 0, che indica che il buffer è vuoto.

Le due tecniche producono risultati equivalenti.

Nell'esempio di codice seguente viene illustrato come registrare un flusso audio dal dispositivo di acquisizione predefinito:


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



Nell'esempio precedente, la funzione RecordAudioStream accetta un solo parametro, `pMySink` , che è un puntatore a un oggetto che appartiene a una classe definita dal client, MyAudioSink, con due funzioni, CopyData e Formatter. Il codice di esempio non include l'implementazione di MyAudioSink perché:

-   Nessuno dei membri della classe comunica direttamente con uno dei metodi nelle interfacce in WASAPI.
-   La classe può essere implementata in diversi modi, a seconda dei requisiti del client. Ad esempio, potrebbe scrivere i dati di acquisizione in un file WAV.

Tuttavia, le informazioni sul funzionamento dei due metodi sono utili per comprendere l'esempio.

La funzione CopyData copia un numero specificato di frame audio da una posizione del buffer specificata. La funzione RecordAudioStream usa la funzione CopyData per leggere e salvare i dati audio dal buffer condiviso. La funzione seformatt specifica il formato per la funzione CopyData da utilizzare per i dati.

Finché l'oggetto MyAudioSink richiede dati aggiuntivi, la funzione CopyData restituisce il valore **false** tramite il terzo parametro, che, nell'esempio di codice precedente, è un puntatore alla variabile `bDone` . Quando l'oggetto MyAudioSink dispone di tutti i dati necessari, la funzione CopyData imposta `bDone` su **true**, che fa sì che il programma esca dal ciclo nella funzione RecordAudioStream.

La funzione RecordAudioStream alloca un buffer condiviso con una durata di un secondo. Il buffer allocato potrebbe avere una durata leggermente superiore. All'interno del ciclo principale, la chiamata alla funzione di [**sospensione**](/windows/desktop/api/synchapi/nf-synchapi-sleep) di Windows fa sì che il programma attenda un mezzo secondo. All'inizio di ogni chiamata di **sospensione** , il buffer condiviso è vuoto o quasi vuoto. Quando la chiamata di **sospensione** viene restituita, il buffer condiviso è circa la metà dei dati di acquisizione.

Dopo la chiamata al metodo [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) , il flusso rimane aperto finché il client non rilascia tutti i relativi riferimenti all'interfaccia [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) e a tutti i riferimenti alle interfacce del servizio ottenute dal client tramite il metodo [**IAudioClient:: GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) . La chiamata alla [**versione**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) finale chiude il flusso.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione dei flussi](stream-management.md)
</dt> </dl>

 

 
