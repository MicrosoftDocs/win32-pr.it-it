---
description: Questa esercitazione illustra come usare l'API transcode per codificare un file MP4, usando H. 264 per il flusso video e AAC per il flusso audio.
ms.assetid: 60873aa6-46ec-4a73-94b9-0d8ac602f850
title: 'Esercitazione: codifica di un file MP4'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae895ef321b35f080bf946384ee32d83c2c539fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226903"
---
# <a name="tutorial-encoding-an-mp4-file"></a>Esercitazione: codifica di un file MP4

Questa esercitazione illustra come usare l' [API transcode](transcode-api.md) per codificare un file MP4, usando H. 264 per il flusso video e AAC per il flusso audio.

-   [Intestazioni e file di libreria](#headers-and-library-files)
-   [Definire i profili di codifica](#define-the-encoding-profiles)
-   [Scrivere la funzione wmain](#write-the-wmain-function)
-   [Codificare il file](#encode-the-file)
    -   [Creare l'origine multimediale](#create-the-media-source)
    -   [Ottenere la durata di origine](#get-the-source-duration)
    -   [Creare il profilo di transcodifica](#create-the-transcode-profile)
    -   [Eseguire la sessione di codifica](#run-the-encoding-session)
-   [Helper della sessione multimediale](#media-session-helper)
-   [Argomenti correlati](#related-topics)

## <a name="headers-and-library-files"></a>Intestazioni e file di libreria

Includere i file di intestazione seguenti.


```C++
#include <new>
#include <iostream>
#include <windows.h>
#include <mfapi.h>
#include <Mfidl.h>
#include <shlwapi.h>
```



Collegare i seguenti file di libreria.


```C++
#pragma comment(lib, "mfplat")
#pragma comment(lib, "mf")
#pragma comment(lib, "mfuuid")
#pragma comment(lib, "shlwapi")
```



## <a name="define-the-encoding-profiles"></a>Definire i profili di codifica

Un approccio alla codifica consiste nel definire un elenco di profili di codifica di destinazione noti in anticipo. Per questa esercitazione, viene adottato un approccio relativamente semplice e viene archiviato un elenco di formati di codifica per audio AAC e video H. 264.

Per H. 264, gli attributi di formato più importanti sono il profilo H. 264, la frequenza dei fotogrammi, le dimensioni del frame e la velocità in bit codificata. La matrice seguente contiene un elenco di formati di codifica H. 264.


```C++
struct H264ProfileInfo
{
    UINT32  profile;
    MFRatio fps;
    MFRatio frame_size;
    UINT32  bitrate;
};

H264ProfileInfo h264_profiles[] = 
{
    { eAVEncH264VProfile_Base, { 15, 1 },       { 176, 144 },   128000 },
    { eAVEncH264VProfile_Base, { 15, 1 },       { 352, 288 },   384000 },
    { eAVEncH264VProfile_Base, { 30, 1 },       { 352, 288 },   384000 },
    { eAVEncH264VProfile_Base, { 29970, 1000 }, { 320, 240 },   528560 },
    { eAVEncH264VProfile_Base, { 15, 1 },       { 720, 576 },  4000000 },
    { eAVEncH264VProfile_Main, { 25, 1 },       { 720, 576 }, 10000000 },
    { eAVEncH264VProfile_Main, { 30, 1 },       { 352, 288 }, 10000000 },
};
```



I profili H. 264 vengono specificati usando l'enumerazione [**eAVEncH264VProfile**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) . È anche possibile specificare il livello H. 264, ma il [**codificatore video h. 264**](h-264-video-encoder.md) Microsoft Media Foundation può derivare il livello appropriato per un determinato flusso video, pertanto è consigliabile non eseguire l'override del livello selezionato del codificatore. Per i contenuti interlacciati, è necessario specificare anche la modalità interlacciata (vedere [interlacciamento video](video-interlacing.md)).

Per l'audio AAC, gli attributi di formato più importanti sono la frequenza di campionamento audio, il numero di canali, il numero di bit per campione e la velocità in bit codificata. Facoltativamente, è possibile impostare l'indicazione del livello di profilo audio AAC. Per ulteriori informazioni, vedere [**AAC Encoder**](aac-encoder.md). La matrice seguente contiene un elenco di formati di codifica AAC.


```C++
struct AACProfileInfo
{
    UINT32  samplesPerSec;
    UINT32  numChannels;
    UINT32  bitsPerSample;
    UINT32  bytesPerSec;
    UINT32  aacProfile;
};

AACProfileInfo aac_profiles[] = 
{
    { 96000, 2, 16, 24000, 0x29}, 
    { 48000, 2, 16, 24000, 0x29}, 
    { 44100, 2, 16, 16000, 0x29}, 
    { 44100, 2, 16, 12000, 0x29}, 
};
```



> [!Note]  
> Le `H264ProfileInfo` `AACProfileInfo` strutture e definite qui non fanno parte dell'API Media Foundation.

 

## <a name="write-the-wmain-function"></a>Scrivere la funzione wmain

Il codice seguente illustra il punto di ingresso per l'applicazione console.


```C++
int video_profile = 0;
int audio_profile = 0;

int wmain(int argc, wchar_t* argv[])
{
    HeapSetInformation(NULL, HeapEnableTerminationOnCorruption, NULL, 0);

    if (argc < 3 || argc > 5)
    {
        std::cout << "Usage:" << std::endl;
        std::cout << "input output [ audio_profile video_profile ]" << std::endl;
        return 1;
    }

    if (argc > 3)
    {
        audio_profile = _wtoi(argv[3]);
    }
    if (argc > 4)
    {
        video_profile = _wtoi(argv[4]);
    }

    HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);
    if (SUCCEEDED(hr))
    {
        hr = MFStartup(MF_VERSION);
        if (SUCCEEDED(hr))
        {
            hr = EncodeFile(argv[1], argv[2]);
            MFShutdown();
        }
        CoUninitialize();
    }

    if (SUCCEEDED(hr))
    {
        std::cout << "Done." << std::endl;
    }
    else
    {
        std::cout << "Error: " << std::hex << hr << std::endl;
    }

    return 0;
}
```



La `wmain` funzione esegue le operazioni seguenti:

1.  Chiama la funzione [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) per inizializzare la libreria com.
2.  Chiama la funzione [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) per inizializzare Media Foundation.
3.  Chiama la funzione definita dall'applicazione `EncodeFile` . Questa funzione transcodifica il file di input nel file di output e viene illustrato nella sezione successiva.
4.  Chiama la funzione [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) per arrestare Media Foundation.
5.  Chiamare la funzione [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) per annullare l'inizializzazione della libreria com.

## <a name="encode-the-file"></a>Codificare il file

Nel codice seguente viene illustrata la `EncodeFile` funzione, che esegue la transcodifica. Questa funzione è costituita principalmente da chiamate ad altre funzioni definite dall'applicazione, illustrate più avanti in questo argomento.


```C++
HRESULT EncodeFile(PCWSTR pszInput, PCWSTR pszOutput)
{
    IMFTranscodeProfile *pProfile = NULL;
    IMFMediaSource *pSource = NULL;
    IMFTopology *pTopology = NULL;
    CSession *pSession = NULL;

    MFTIME duration = 0;

    HRESULT hr = CreateMediaSource(pszInput, &pSource);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = GetSourceDuration(pSource, &duration);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = CreateTranscodeProfile(&pProfile);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = MFCreateTranscodeTopology(pSource, pszOutput, pProfile, &pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = CSession::Create(&pSession);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSession->StartEncodingSession(pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = RunEncodingSession(pSession, duration);

done:            
    if (pSource)
    {
        pSource->Shutdown();
    }

    SafeRelease(&pSession);
    SafeRelease(&pProfile);
    SafeRelease(&pSource);
    SafeRelease(&pTopology);
    return hr;
}
```



La `EncodeFile` funzione esegue i passaggi seguenti.

1.  Crea un'origine multimediale per il file di input, usando l'URL o il percorso del file di input. (Vedere [creare l'origine multimediale](#create-the-media-source)).
2.  Ottiene la durata del file di input. (Vedere [ottenere la durata dell'origine](#get-the-source-duration)).
3.  Creare il profilo transcodifica. (Vedere [creare il profilo transcodifica](#create-the-transcode-profile)).
4.  Chiamare [**MFCreateTranscodeTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) per creare la topologia transcodifica parziale.
5.  Creare un oggetto helper che gestisce la sessione multimediale. (Vedere helper della sessione multimediale).
6.  Eseguire la sessione di codifica e attenderne il completamento. (Vedere [eseguire la sessione di codifica](#run-the-encoding-session)).
7.  Chiamare [**IMFMediaSource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) per arrestare l'origine del supporto.
8.  Puntatori dell'interfaccia della versione. Questo codice usa la funzione [SafeRelease](saferelease.md) per rilasciare i puntatori a interfaccia. Un'altra opzione consiste nell'usare una classe di puntatore intelligente COM, ad esempio **CComPtr**.

### <a name="create-the-media-source"></a>Creare l'origine multimediale

L'origine del supporto è l'oggetto che legge e analizza il file di input. Per creare l'origine del supporto, passare l'URL del file di input al [resolver di origine](source-resolver.md). A tal fine, osservare il codice indicato di seguito.


```C++
HRESULT CreateMediaSource(PCWSTR pszURL, IMFMediaSource **ppSource)
{
    MF_OBJECT_TYPE ObjectType = MF_OBJECT_INVALID;

    IMFSourceResolver* pResolver = NULL;
    IUnknown* pSource = NULL;

    // Create the source resolver.
    HRESULT hr = MFCreateSourceResolver(&pResolver);
    if (FAILED(hr))
    {
        goto done;
    }

    // Use the source resolver to create the media source
    hr = pResolver->CreateObjectFromURL(pszURL, MF_RESOLUTION_MEDIASOURCE, 
        NULL, &ObjectType, &pSource);
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the IMFMediaSource interface from the media source.
    hr = pSource->QueryInterface(IID_PPV_ARGS(ppSource));

done:
    SafeRelease(&pResolver);
    SafeRelease(&pSource);
    return hr;
}
```



Per ulteriori informazioni, vedere [using the source resolver](using-the-source-resolver.md).

### <a name="get-the-source-duration"></a>Ottenere la durata di origine

Sebbene non sia obbligatorio, è utile eseguire una query sull'origine multimediale per la durata del file di input. Questo valore può essere usato per tenere traccia dello stato di avanzamento della codifica. La durata viene archiviata nell'attributo della [**\_ \_ durata MF PD**](mf-pd-duration-attribute.md) del descrittore di presentazione. Ottenere il descrittore della presentazione chiamando [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).


```C++
HRESULT GetSourceDuration(IMFMediaSource *pSource, MFTIME *pDuration)
{
    *pDuration = 0;

    IMFPresentationDescriptor *pPD = NULL;

    HRESULT hr = pSource->CreatePresentationDescriptor(&pPD);
    if (SUCCEEDED(hr))
    {
        hr = pPD->GetUINT64(MF_PD_DURATION, (UINT64*)pDuration);
        pPD->Release();
    }
    return hr;
}
```



### <a name="create-the-transcode-profile"></a>Creare il profilo di transcodifica

Il profilo transcode descrive i parametri di codifica. Per ulteriori informazioni sulla creazione di un profilo transcodifica, vedere [utilizzo dell'API transcodifica](fast-transcode-objects.md). Per creare il profilo, seguire questa procedura.

1.  Chiamare [**MFCreateTranscodeProfile**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodeprofile) per creare il profilo vuoto.
2.  Creare un tipo di supporto per il flusso audio AAC. Aggiungerlo al profilo chiamando [**IMFTranscodeProfile:: SetAudioAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes).
3.  Creare un tipo di supporto per il flusso video H. 264. Aggiungerlo al profilo chiamando [**IMFTranscodeProfile:: SetVideoAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes).
4.  Chiamare [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) per creare un archivio di attributi per gli attributi a livello di contenitore.
5.  Impostare l'attributo [MF \_ transcode \_ CONTAINERTYPE](mf-transcode-containertype.md) . Si tratta dell'unico attributo a livello di contenitore obbligatorio. Per l'output del file MP4, impostare questo attributo su **MFTranscodeContainerType \_ MPEG4**.
6.  Chiamare [**IMFTranscodeProfile:: SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes) per impostare gli attributi a livello di contenitore.

Nel codice seguente vengono illustrati questi passaggi.


```C++
HRESULT CreateTranscodeProfile(IMFTranscodeProfile **ppProfile)
{
    IMFTranscodeProfile *pProfile = NULL;
    IMFAttributes *pAudio = NULL;
    IMFAttributes *pVideo = NULL;
    IMFAttributes *pContainer = NULL;

    HRESULT hr = MFCreateTranscodeProfile(&pProfile);
    if (FAILED(hr)) 
    {
        goto done;
    }

    // Audio attributes.
    hr = CreateAACProfile(audio_profile, &pAudio);
    if (FAILED(hr)) 
    {
        goto done;
    }

    hr = pProfile->SetAudioAttributes(pAudio);
    if (FAILED(hr)) 
    {
        goto done;
    }

    // Video attributes.
    hr = CreateH264Profile(video_profile, &pVideo);
    if (FAILED(hr)) 
    {
        goto done;
    }

    hr = pProfile->SetVideoAttributes(pVideo);
    if (FAILED(hr)) 
    {
        goto done;
    }

    // Container attributes.
    hr = MFCreateAttributes(&pContainer, 1);
    if (FAILED(hr)) 
    {
        goto done;
    }

    hr = pContainer->SetGUID(MF_TRANSCODE_CONTAINERTYPE, MFTranscodeContainerType_MPEG4);
    if (FAILED(hr)) 
    {
        goto done;
    }

    hr = pProfile->SetContainerAttributes(pContainer);
    if (FAILED(hr)) 
    {
        goto done;
    }

    *ppProfile = pProfile;
    (*ppProfile)->AddRef();

done:
    SafeRelease(&pProfile);
    SafeRelease(&pAudio);
    SafeRelease(&pVideo);
    SafeRelease(&pContainer);
    return hr;
}
```



Per specificare gli attributi per il flusso video H. 264, creare un archivio di attributi e impostare i seguenti attributi:



| Attributo                                                       | Descrizione                      |
|-----------------------------------------------------------------|---------------------------------|
| [**sottotipo MF \_ mt \_**](mf-mt-subtype-attribute.md)              | Impostare su **MFVideoFormat \_ H264**. |
| [**\_ \_ Profilo MPEG2 MF \_ mt**](mf-mt-mpeg2-profile-attribute.md) | Profilo H. 264.                  |
| [**\_dimensioni del \_ frame MF mt \_**](mf-mt-frame-size-attribute.md)       | Dimensioni del frame.                     |
| [**\_ \_ frequenza fotogrammi MF mt \_**](mf-mt-frame-rate-attribute.md)       | Frequenza di fotogrammi.                     |
| [**\_velocità in \_ bit media MF mt \_**](mf-mt-avg-bitrate-attribute.md)     | Velocità in bit codificata.               |



 

Per specificare gli attributi per il flusso audio AAC, creare un archivio di attributi e impostare i seguenti attributi:



| Attributo                                                                                      | Descrizione                               |
|------------------------------------------------------------------------------------------------|------------------------------------------|
| [**sottotipo MF \_ mt \_**](mf-mt-subtype-attribute.md)                                             | Imposta su **MFAudioFormat \_ AAC**            |
| [**\_ \_ campioni audio MF \_ mt \_ al \_ secondo**](mf-mt-audio-samples-per-second-attribute.md)        | Frequenza di campionamento audio.                       |
| [**\_ \_ bit audio MF \_ mt \_ per \_ campione**](mf-mt-audio-bits-per-sample-attribute.md)              | Bit per esempio audio.                   |
| [**numero \_ di \_ \_ canali audio MF mt \_**](mf-mt-audio-num-channels-attribute.md)                     | Numero dei canali audio.                |
| [**\_ \_ Media byte audio MF mt \_ \_ \_ al \_ secondo**](mf-mt-audio-avg-bytes-per-second-attribute.md)   | Velocità in bit codificata.                        |
| [**\_ \_ \_ allineamento blocchi audio MF \_ mt**](mf-mt-audio-block-alignment-attribute.md)               | impostare su 1.                                |
| [\_ \_ \_ \_ \_ indicazione livello profilo audio MF mt \_ AAC](mf-mt-aac-audio-profile-level-indication.md) | Indicazione del livello di profilo AAC (facoltativo). |



 

Il codice seguente crea gli attributi del flusso video.


```C++
HRESULT CreateH264Profile(DWORD index, IMFAttributes **ppAttributes)
{
    if (index >= ARRAYSIZE(h264_profiles))
    {
        return E_INVALIDARG;
    }

    IMFAttributes *pAttributes = NULL;

    const H264ProfileInfo& profile = h264_profiles[index];

    HRESULT hr = MFCreateAttributes(&pAttributes, 5);
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetGUID(MF_MT_SUBTYPE, MFVideoFormat_H264);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(MF_MT_MPEG2_PROFILE, profile.profile);
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeSize(
            pAttributes, MF_MT_FRAME_SIZE, 
            profile.frame_size.Numerator, profile.frame_size.Numerator);
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeRatio(
            pAttributes, MF_MT_FRAME_RATE, 
            profile.fps.Numerator, profile.fps.Denominator);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(MF_MT_AVG_BITRATE, profile.bitrate);
    }
    if (SUCCEEDED(hr))
    {
        *ppAttributes = pAttributes;
        (*ppAttributes)->AddRef();
    }
    SafeRelease(&pAttributes);
    return hr;
}
```



Il codice seguente crea gli attributi del flusso audio.


```C++
HRESULT CreateAACProfile(DWORD index, IMFAttributes **ppAttributes)
{
    if (index >= ARRAYSIZE(h264_profiles))
    {
        return E_INVALIDARG;
    }

    const AACProfileInfo& profile = aac_profiles[index];

    IMFAttributes *pAttributes = NULL;

    HRESULT hr = MFCreateAttributes(&pAttributes, 7);
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetGUID(MF_MT_SUBTYPE, MFAudioFormat_AAC);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(
            MF_MT_AUDIO_BITS_PER_SAMPLE, profile.bitsPerSample);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(
            MF_MT_AUDIO_SAMPLES_PER_SECOND, profile.samplesPerSec);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(
            MF_MT_AUDIO_NUM_CHANNELS, profile.numChannels);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(
            MF_MT_AUDIO_AVG_BYTES_PER_SECOND, profile.bytesPerSec);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(MF_MT_AUDIO_BLOCK_ALIGNMENT, 1);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(
            MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION, profile.aacProfile);
    }
    if (SUCCEEDED(hr))
    {
        *ppAttributes = pAttributes;
        (*ppAttributes)->AddRef();
    }
    SafeRelease(&pAttributes);
    return hr;
}
```



Si noti che l'API transcode non richiede un vero tipo di supporto, sebbene usi gli attributi di tipo supporto. In particolare, l'attributo del [**\_ \_ \_ tipo principale MF mt**](mf-mt-major-type-attribute.md) non è obbligatorio perché i metodi [**SetVideoAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes) e [**SetAudioAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes) implicano il tipo principale. Tuttavia, è anche possibile passare un tipo di supporto effettivo a questi metodi. (L'interfaccia [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) eredita [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)).

### <a name="run-the-encoding-session"></a>Eseguire la sessione di codifica

Il codice seguente esegue la sessione di codifica. Usa la classe helper della sessione multimediale, illustrata nella sezione successiva.


```C++
HRESULT RunEncodingSession(CSession *pSession, MFTIME duration)
{
    const DWORD WAIT_PERIOD = 500;
    const int   UPDATE_INCR = 5;

    HRESULT hr = S_OK;
    MFTIME pos;
    LONGLONG prev = 0;
    while (1)
    {
        hr = pSession->Wait(WAIT_PERIOD);
        if (hr == E_PENDING)
        {
            hr = pSession->GetEncodingPosition(&pos);

            LONGLONG percent = (100 * pos) / duration ;
            if (percent >= prev + UPDATE_INCR)
            {
                std::cout << percent << "% .. ";  
                prev = percent;
            }
        }
        else
        {
            std::cout << std::endl;
            break;
        }
    }
    return hr;
}
```



## <a name="media-session-helper"></a>Helper della sessione multimediale

La [sessione multimediale](media-session.md) è descritta più dettagliatamente nella sezione [architettura Media Foundation](media-foundation-architecture.md) di questa documentazione. La sessione multimediale usa un modello di eventi asincrono. In un'applicazione GUI è necessario rispondere agli eventi di sessione senza bloccare il thread dell'interfaccia utente per attendere l'evento successivo. L'esercitazione [come riprodurre file multimediali non protetti](how-to-play-unprotected-media-files.md) Mostra come eseguire questa operazione in un'applicazione di riproduzione. Per la codifica, il principio è lo stesso, ma un minor numero di eventi è pertinente:



| Evento                                  | Descrizione                                                                                                                                                       |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MESessionEnded](mesessionended.md)   | Generato quando la codifica è completa.                                                                                                                            |
| [MESessionClosed](mesessionclosed.md) | Generato quando il metodo [**IMFMediaSession:: Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) viene completato. Dopo la generazione di questo evento, è possibile arrestare la sessione multimediale. |



 

Per un'applicazione console, è ragionevole bloccarsi e attendere gli eventi. A seconda del file di origine e delle impostazioni di codifica, potrebbe essere necessario un po' di tempo per completare la codifica. È possibile ottenere gli aggiornamenti dello stato di avanzamento come segue:

1.  Chiamare [**IMFMediaSession:: getclock**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getclock) per ottenere il clock di presentazione.
2.  Eseguire una query sul clock per l'interfaccia [**IMFPresentationClock**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock) .
3.  Chiamare [**IMFPresentationClock:: GetTime**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-gettime) per ottenere la posizione corrente.
4.  La posizione viene specificata in unità di tempo. Per ottenere la percentuale completata, usare il valore `(100 * position) / duration` .

Di seguito è illustrata la dichiarazione della `CSession` classe.


```C++
class CSession  : public IMFAsyncCallback 
{
public:
    static HRESULT Create(CSession **ppSession);

    // IUnknown methods
    STDMETHODIMP QueryInterface(REFIID riid, void** ppv);
    STDMETHODIMP_(ULONG) AddRef();
    STDMETHODIMP_(ULONG) Release();

    // IMFAsyncCallback methods
    STDMETHODIMP GetParameters(DWORD* pdwFlags, DWORD* pdwQueue)
    {
        // Implementation of this method is optional.
        return E_NOTIMPL;
    }
    STDMETHODIMP Invoke(IMFAsyncResult *pResult);

    // Other methods
    HRESULT StartEncodingSession(IMFTopology *pTopology);
    HRESULT GetEncodingPosition(MFTIME *pTime);
    HRESULT Wait(DWORD dwMsec);

private:
    CSession() : m_cRef(1), m_pSession(NULL), m_pClock(NULL), m_hrStatus(S_OK), m_hWaitEvent(NULL)
    {
    }
    virtual ~CSession()
    {
        if (m_pSession)
        {
            m_pSession->Shutdown();
        }

        SafeRelease(&m_pClock);
        SafeRelease(&m_pSession);
        CloseHandle(m_hWaitEvent);
    }

    HRESULT Initialize();

private:
    IMFMediaSession      *m_pSession;
    IMFPresentationClock *m_pClock;
    HRESULT m_hrStatus;
    HANDLE  m_hWaitEvent;
    long    m_cRef;
};
```



Nel codice seguente viene illustrata l'implementazione completa della `CSession` classe.


```C++
HRESULT CSession::Create(CSession **ppSession)
{
    *ppSession = NULL;

    CSession *pSession = new (std::nothrow) CSession();
    if (pSession == NULL)
    {
        return E_OUTOFMEMORY;
    }

    HRESULT hr = pSession->Initialize();
    if (FAILED(hr))
    {
        pSession->Release();
        return hr;
    }
    *ppSession = pSession;
    return S_OK;
}

STDMETHODIMP CSession::QueryInterface(REFIID riid, void** ppv)
{
    static const QITAB qit[] = 
    {
        QITABENT(CSession, IMFAsyncCallback),
        { 0 }
    };
    return QISearch(this, qit, riid, ppv);
}

STDMETHODIMP_(ULONG) CSession::AddRef()
{
    return InterlockedIncrement(&m_cRef);
}

STDMETHODIMP_(ULONG) CSession::Release()
{
    long cRef = InterlockedDecrement(&m_cRef);
    if (cRef == 0)
    {
        delete this;
    }
    return cRef;
}

HRESULT CSession::Initialize()
{
    IMFClock *pClock = NULL;

    HRESULT hr = MFCreateMediaSession(NULL, &m_pSession);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = m_pSession->GetClock(&pClock);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pClock->QueryInterface(IID_PPV_ARGS(&m_pClock));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = m_pSession->BeginGetEvent(this, NULL);
    if (FAILED(hr))
    {
        goto done;
    }

    m_hWaitEvent = CreateEvent(NULL, FALSE, FALSE, NULL);  
    if (m_hWaitEvent == NULL)
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
    }
done:
    SafeRelease(&pClock);
    return hr;
}

// Implements IMFAsyncCallback::Invoke
STDMETHODIMP CSession::Invoke(IMFAsyncResult *pResult)
{
    IMFMediaEvent* pEvent = NULL;
    MediaEventType meType = MEUnknown;
    HRESULT hrStatus = S_OK;

    HRESULT hr = m_pSession->EndGetEvent(pResult, &pEvent);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pEvent->GetType(&meType);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pEvent->GetStatus(&hrStatus);
    if (FAILED(hr))
    {
        goto done;
    }

    if (FAILED(hrStatus))
    {
        hr = hrStatus;
        goto done;
    }

    switch (meType)
    {
    case MESessionEnded:
        hr = m_pSession->Close();
        if (FAILED(hr))
        {
            goto done;
        }
        break;

    case MESessionClosed:
        SetEvent(m_hWaitEvent);
        break;
    }

    if (meType != MESessionClosed)
    {
        hr = m_pSession->BeginGetEvent(this, NULL);
    }

done:
    if (FAILED(hr))
    {
        m_hrStatus = hr;
        m_pSession->Close();
    }

    SafeRelease(&pEvent);
    return hr;
}

HRESULT CSession::StartEncodingSession(IMFTopology *pTopology)
{
    HRESULT hr = m_pSession->SetTopology(0, pTopology);
    if (SUCCEEDED(hr))
    {
        PROPVARIANT varStart;
        PropVariantClear(&varStart);
        hr = m_pSession->Start(&GUID_NULL, &varStart);
    }
    return hr;
}

HRESULT CSession::GetEncodingPosition(MFTIME *pTime)
{
    return m_pClock->GetTime(pTime);
}

HRESULT CSession::Wait(DWORD dwMsec)
{
    HRESULT hr = S_OK;

    DWORD dwTimeoutStatus = WaitForSingleObject(m_hWaitEvent, dwMsec);
    if (dwTimeoutStatus != WAIT_OBJECT_0)
    {
        hr = E_PENDING;
    }
    else
    {
        hr = m_hrStatus;
    }
    return hr;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Codificatore AAC**](aac-encoder.md)
</dt> <dt>

[**Codificatore video H. 264**](h-264-video-encoder.md)
</dt> <dt>

[Sessione multimediale](media-session.md)
</dt> <dt>

[Tipi di supporto](media-types.md)
</dt> <dt>

[API transcodifica](transcode-api.md)
</dt> </dl>

 

 
