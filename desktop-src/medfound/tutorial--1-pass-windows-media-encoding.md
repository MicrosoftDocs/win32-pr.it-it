---
description: La codifica si riferisce al processo di conversione di file multimediali digitali da un formato a un altro. Ad esempio, la conversione di audio MP3 nel formato Windows Media Audio come definito dalla specifica ASF (Advanced Systems Format).
ms.assetid: 4fe202d8-c8f5-4e9a-ad40-1aea8f767362
title: 'Esercitazione: codifica Windows Media da 1 passaggio'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d670b107f315966a048a2f847183431f9a57bd4
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "103761459"
---
# <a name="tutorial-1-pass-windows-media-encoding"></a>Esercitazione: codifica Windows Media da 1 passaggio

La codifica si riferisce al processo di conversione di file multimediali digitali da un formato a un altro. Ad esempio, la conversione di audio MP3 nel formato Windows Media Audio come definito dalla specifica ASF (Advanced Systems Format).

**Nota**  La specifica ASF definisce un tipo di contenitore per il file di output (WMA o WMV) che può contenere dati multimediali in qualsiasi formato, compresso o decompresso. Ad esempio, un contenitore ASF, ad esempio un file con estensione WMA, può contenere dati multimediali in formato MP3. Il processo di codifica converte il formato effettivo dei dati contenuti all'interno del file.

In questa esercitazione viene illustrata la codifica di un'origine di input non protetta da DRM in contenuto Windows Media e la scrittura dei dati in un nuovo file ASF (WM \* ) utilizzando i componenti ASF del livello pipeline. Questi componenti verranno utilizzati per compilare una topologia di codifica parziale, che verrà controllata da un'istanza della sessione multimediale.

In questa esercitazione si creerà un'applicazione console che accetta i nomi dei file di input e di output e la modalità di codifica come argomenti. Il file di input può trovarsi in un formato multimediale compresso o non compresso. Le modalità di codifica valide sono "CBR" (velocità in bit costante) o "VBR" (velocità in bit variabile). L'applicazione crea un'origine multimediale per rappresentare l'origine specificata dal nome file di input e il sink di file ASF per archiviare il contenuto codificato del file di origine in un file ASF. Per semplificare l'implementazione dello scenario, il file di output avrà un solo flusso audio e un flusso video. L'applicazione inserisce il codec Windows Media Audio 9,1 Professional per la conversione del formato del flusso audio e il codec Windows Media Video 9 per il flusso video.

Per la codifica della velocità in bit costante, prima dell'inizio della sessione di codifica, il codificatore deve essere a conoscenza della velocità in bit di destinazione che deve raggiungere. In questa esercitazione, per la modalità "CBR", l'applicazione usa la velocità in bit disponibile con il primo tipo di supporto di output recuperato dal codificatore durante la negoziazione del tipo di supporto come velocità in bit di destinazione. Per la codifica della velocità in bit variabile, in questa esercitazione viene illustrata la codifica con velocità in bit variabile impostando un livello di qualità. I flussi audio vengono codificati a livello di qualità 98 e flussi video a livello di qualità 95.

Nella procedura riportata di seguito vengono riepilogati i passaggi per codificare il contenuto di Windows Media in un contenitore ASF utilizzando una modalità di codifica a 1 passaggio.

1.  Creare un'origine multimediale per l'oggetto specificato utilizzando il resolver di origine.
2.  Enumerare i flussi nell'origine multimediale.
3.  Creare il sink multimediale ASF e aggiungere i sink di flusso a seconda dei flussi nell'origine multimediale che devono essere codificati.
4.  Configurare il sink multimediale con le proprietà di codifica obbligatorie.
5.  Creare i codificatori Windows Media per i flussi nel file di output.
6.  Configurare i codificatori con le proprietà impostate nel sink multimediale.
7.  Compilazione di una topologia di codifica parziale.
8.  Creare un'istanza della sessione multimediale e impostare la topologia nella sessione multimediale.
9.  Avviare la sessione di codifica controllando la sessione multimediale e ottenendo tutti gli eventi rilevanti dalla sessione multimediale.
10. Per la codifica VBR, ottenere i valori delle proprietà di codifica dal codificatore e impostarli nel sink multimediale.
11. Chiudere e arrestare la sessione di codifica.

Questa esercitazione contiene le sezioni seguenti:

-   [Prerequisiti](#prerequisites)
-   [Configurare il progetto](#set-up-the-project)
-   [Creare l'origine multimediale](#create-the-media-source)
-   [Creare il sink di file ASF](#create-the-asf-file-sink)
    -   [Creazione dell'oggetto profilo ASF](#create-the-asf-profile-object)
    -   [Creare un tipo di supporto audio compresso](#create-a-compressed-audio-media-type)
    -   [Creare un tipo di supporto video compresso](#create-a-compressed-video-media-type)
    -   [Creare l'oggetto ContentInfo ASF](#create-the-asf-contentinfo-object)
    -   [Creare il sink di file ASF](#create-the-asf-file-sink)
-   [Compilare la topologia di codifica parziale](#build-the-partial-encoding-topology)
    -   [Creare il nodo topologia di origine per l'origine multimediale](#create-the-source-topology-node-for-the-media-source)
    -   [Creare un'istanza dei codificatori necessari e creare i nodi di trasformazione](#instantiate-the-required-encoders-and-create-the-transform-nodes)
    -   [Creare i nodi della topologia di output per il sink di file](#create-the-output-topology-nodes-for-the-file-sink)
    -   [Connettere i nodi di origine, trasformazione e sink](#connect-the-source-transform-and-sink-nodes)
-   [Gestione della sessione di codifica](#handling-the-encoding-session)
-   [Aggiornare le proprietà di codifica nel sink di file](#update-encoding-properties-in-the-file-sink)
-   [Implementare Main](#implement-main)
-   [Testare il file di output](#test-the-output-file)
-   [Codici di errore comuni e suggerimenti per il debug](#common-error-codes-and-debugging-tips)
-   [Argomenti correlati](#related-topics)

## <a name="prerequisites"></a>Prerequisiti

Nell’esercitazione si presuppongono le condizioni seguenti:

-   Si ha familiarità con la [struttura dei file ASF](asf-file-structure.md), i [componenti ASF del livello Pipeline](pipeline-layer-asf-components.md) forniti da Media Foundation per lavorare con gli oggetti ASF. Questi componenti includono gli oggetti seguenti:
    -   [Origini supporti](media-sources.md)

        **Nota**  Se si esegue la transclassificazione (convertendo un file di velocità in bit superiore in un file con velocità in bit inferiore senza modificare i formati), si userà l' [origine dei supporti ASF](asf-media-source.md).

    -   [Codificatori Windows Media](windows-media-encoders.md)
    -   [Sink di supporti ASF](asf-media-sinks.md)
    -   [Oggetto ContentInfo ASF](asf-contentinfo-object.md)
    -   [Profilo ASF](asf-profile.md)

-   Si ha familiarità con i codificatori Windows Media e i vari tipi di codifica, in particolare la [codifica della velocità in bit costante](constant-bit-rate-encoding.md) e la [codifica della velocità in bit variabile basata sulla qualità](quality-based-variable-bit-rate--vbr--encoding.md).
-   Si ha familiarità con le operazioni del codificatore MFT. In particolare, creazione di un'istanza del codificatore e impostazione dei tipi di input e di output nel codificatore.
-   Si ha familiarità con gli oggetti della topologia e come creare una topologia di codifica. Per ulteriori informazioni sulle topologie e sui nodi della topologia, vedere [creazione](creating-topologies.md)di topologie.
-   Si ha familiarità con il modello di eventi della [sessione multimediale](media-session.md)e le operazioni di controllo di flusso. Per informazioni, vedere [eventi della sessione multimediale](media-session-events.md).

## <a name="set-up-the-project"></a>Configurare il progetto

1.  Includere le intestazioni seguenti nel file di origine:

    ```C++
    #include <new>
    #include <mfidl.h>            // Media Foundation interfaces
    #include <mfapi.h>            // Media Foundation platform APIs
    #include <mferror.h>        // Media Foundation error codes
    #include <wmcontainer.h>    // ASF-specific components
    #include <wmcodecdsp.h>        // Windows Media DSP interfaces
    #include <Dmo.h>            // DMO objects
    #include <uuids.h>            // Definition for FORMAT_VideoInfo
    #include <propvarutil.h>
    
    ```

    

2.  Collegamento ai file di libreria seguenti:

    ```C++
    // The required link libraries 
    #pragma comment(lib, "mfplat")
    #pragma comment(lib, "mf")
    #pragma comment(lib, "mfuuid")
    #pragma comment(lib, "msdmo")
    #pragma comment(lib, "strmiids")
    #pragma comment(lib, "propsys")
    
    ```

    

3.  Dichiarare la funzione [SafeRelease](saferelease.md) .

    ```C++
    template <class T> void SafeRelease(T **ppT)
    {
        if (*ppT)
        {
            (*ppT)->Release();
            *ppT = NULL;
        }
    }
    ```

    

4.  Dichiarare l' \_ enumerazione della modalità di codifica per definire i tipi di codifica CBR e VBR.

    ```C++
    // Encoding mode
    typedef enum ENCODING_MODE {
      NONE  = 0x00000000,
      CBR   = 0x00000001,
      VBR   = 0x00000002,
    } ;
    
    ```

    

5.  Definire una costante per la finestra del buffer per un flusso video.

    ```C++
    // Video buffer window
    const INT32 VIDEO_WINDOW_MSEC = 3000;
    
    ```

    

## <a name="create-the-media-source"></a>Creare l'origine multimediale

Creare un'origine multimediale per l'origine di input. Media Foundation fornisce origini multimediali predefinite per diversi formati multimediali: MP3, MP4/3GP, AVI/WAVE. Per informazioni sui formati supportati da Media Foundation, vedere [formati multimediali supportati in Media Foundation](supported-media-formats-in-media-foundation.md).

Per creare l'origine multimediale, usare il [resolver di origine](source-resolver.md). Questo oggetto analizza l'URL specificato per il file di origine e crea l'origine multimediale appropriata.

Effettuare le chiamate seguenti:

-   [**MFCreateSourceResolver**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesourceresolver)
-   [**IMFSourceResolver::CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl)

    Per ulteriori informazioni su queste chiamate, vedere [using the source resolver](using-the-source-resolver.md).

    Se il file di input è in formato ASF e si desidera convertirlo in un file con frequenza di bit diverso senza modificare i formati, il Risolutore di origine crea un'istanza dell' [origine dei supporti ASF](asf-media-source.md).

Nell'esempio di codice seguente viene illustrata una funzione CreateMediaSource che consente di creare un'origine multimediale per il file specificato.


```C++
//  Create a media source from a URL.
HRESULT CreateMediaSource(PCWSTR sURL, IMFMediaSource **ppSource)
{
    MF_OBJECT_TYPE ObjectType = MF_OBJECT_INVALID;

    IMFSourceResolver* pSourceResolver = NULL;
    IUnknown* pSource = NULL;

    // Create the source resolver.
    HRESULT hr = MFCreateSourceResolver(&pSourceResolver);
    if (FAILED(hr))
    {
        goto done;
    }

    // Use the source resolver to create the media source.

    // Note: For simplicity this sample uses the synchronous method to create 
    // the media source. However, creating a media source can take a noticeable
    // amount of time, especially for a network source. For a more responsive 
    // UI, use the asynchronous BeginCreateObjectFromURL method.

    hr = pSourceResolver->CreateObjectFromURL(
        sURL,                       // URL of the source.
        MF_RESOLUTION_MEDIASOURCE,  // Create a source object.
        NULL,                       // Optional property store.
        &ObjectType,        // Receives the created object type. 
        &pSource            // Receives a pointer to the media source.
        );
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the IMFMediaSource interface from the media source.
    hr = pSource->QueryInterface(IID_PPV_ARGS(ppSource));

done:
    SafeRelease(&pSourceResolver);
    SafeRelease(&pSource);
    return hr;
}
```



## <a name="create-the-asf-file-sink"></a>Creare il sink di file ASF

Consente di creare un'istanza del sink di file ASF che archivia i dati multimediali codificati in un file ASF alla fine della sessione di codifica.

In questa esercitazione verrà creato un oggetto attivazione per il sink di file ASF. Il sink di file richiede le informazioni seguenti per creare i sink di flusso richiesti.

-   Flussi da codificare e scrivere nel file finale.
-   Proprietà di codifica utilizzate per codificare il contenuto multimediale, ad esempio, il tipo di codifica, il numero di sessioni di codifica e le proprietà correlate.
-   Le proprietà del file globale che indicano al sink multimediale se devono modificare automaticamente i parametri del bucket di perdita (velocità in bit e dimensione del buffer).

Le informazioni sul flusso vengono configurate nell'oggetto profilo ASF e le proprietà di codifica e globali vengono impostate in un archivio di proprietà gestito dall'oggetto ContentInfo ASF.

Per una panoramica del sink di file ASF, vedere [ASF media sinks](asf-media-sinks.md).

### <a name="create-the-asf-profile-object"></a>Creazione dell'oggetto profilo ASF

Affinché il sink di file ASF scriva i dati multimediali codificati in un file ASF, è necessario che il sink conosca il numero di flussi e il tipo di flussi per i quali creare i sink di flusso. In questa esercitazione si estratteranno le informazioni dall'origine multimediale e si creeranno i flussi di output corrispondenti. Limitare i flussi di output a un flusso audio e a un flusso video. Per ogni flusso selezionato nell'origine, creare un flusso di destinazione e aggiungerlo al profilo.

Per implementare questo passaggio, sono necessari gli oggetti seguenti.

-   [Profilo ASF](asf-profile.md)
-   Descrittore della presentazione per l'origine multimediale
-   Descrittori di flusso per i flussi selezionati nell'origine multimediale.
-   Tipi di supporto per i flussi selezionati.

Nei passaggi seguenti viene descritto il processo di creazione del profilo ASF e dei flussi di destinazione.

**Per creare il profilo ASF**

1.  Chiamare [**MFCreateASFProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile) per creare un oggetto profilo vuoto.
2.  Chiamare [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) per creare il descrittore di presentazione per l'origine multimediale creata nel passaggio descritto nella sezione "creare l'origine dei supporti" di questa esercitazione.
3.  Chiamare [**IMFPresentationDescriptor:: GetStreamDescriptorCount**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorcount) per ottenere il numero di flussi nell'origine multimediale.
4.  Chiamare [**IMFPresentationDescriptor:: GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) per ogni flusso nell'origine multimediale, ottenere il descrittore del flusso del flusso.
5.  Chiamare [**IMFStreamDescriptor:: GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) seguito da [**IMFMediaTypeHandler:: GetMediaTypeByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) e ottenere il primo tipo di supporto per il flusso.

    **Nota**   Per evitare chiamate complesse, si supponga che esista un solo tipo di supporto per flusso e selezionare il primo tipo di supporto del flusso. Per i flussi complessi è necessario enumerare ogni tipo di supporto dal gestore del tipo di supporto e scegliere il tipo di supporto che si desidera codificare.

6.  Chiamare I [**IMFMediaType:: GetMajorType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getmajortype) per ottenere il tipo principale del flusso per determinare se il flusso contiene audio o video.
7.  A seconda del tipo principale del flusso, creare i tipi di supporto di destinazione. Questi tipi di supporto manterranno le informazioni sul formato che il codificatore userà durante la sessione di codifica. Le sezioni seguenti di questa esercitazione descrivono il processo di creazione dei tipi di supporto di destinazione.
    -   Creare un tipo di supporto audio compresso
    -   Creare un tipo di supporto video compresso
8.  Creare un flusso in base al tipo di supporto di destinazione, configurare il flusso in base ai requisiti dell'applicazione e aggiungere il flusso al profilo. Per ulteriori informazioni, vedere [aggiunta di informazioni sul flusso al sink di file ASF](adding-stream-information-to-the-asf-file-sink.md).

    1.  Chiamare [**IMFASFProfile:: CreateStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstream) e passare il tipo di supporto di destinazione per creare il flusso di output. Il metodo recupera l'interfaccia IMFASFStreamConfig dell'oggetto flusso.
    2.  Configurare il flusso.
        -   Chiamare [**IMFASFStreamConfig:: SetStreamNumber**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-setstreamnumber) per assegnare un numero al flusso. Questa impostazione è obbligatoria.
        -   Facoltativamente, è possibile configurare i parametri del bucket di perdita, l'estensione del payload, l'esclusione reciproca in ogni flusso chiamando metodi [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) e gli attributi di configurazione del flusso rilevanti.
    3.  Aggiungere le proprietà di codifica a livello di flusso usando l'oggetto di ASF. Per ulteriori informazioni su questo passaggio, vedere la sezione "Create the ASF ContentInfo Object" in questa esercitazione.
    4.  Chiamare [**IMFASFProfile:: sestream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream) per aggiungere il flusso al profilo.

    L'esempio di codice seguente crea un flusso audio di output.

    ```C++
    //-------------------------------------------------------------------
    //  CreateAudioStream
    //  Create an audio stream and add it to the profile.
    //
    //  pProfile: A pointer to the ASF profile.
    //  wStreamNumber: Stream number to assign for the new stream.
    //-------------------------------------------------------------------

    HRESULT CreateAudioStream(IMFASFProfile* pProfile, WORD wStreamNumber)
    {
        if (!pProfile)
        {
            return E_INVALIDARG;
        }
        if (wStreamNumber < 1 || wStreamNumber > 127 )
        {
            return MF_E_INVALIDSTREAMNUMBER;
        }

        IMFMediaType* pAudioType = NULL;
        IMFASFStreamConfig* pAudioStream = NULL;
        
        //Create an output type from the encoder
        HRESULT hr = GetOutputTypeFromWMAEncoder(&pAudioType);
        if (FAILED(hr))
        {
            goto done;
        }
        
        //Create a new stream with the audio type
        hr = pProfile->CreateStream(pAudioType, &pAudioStream);
        if (FAILED(hr))
        {
            goto done;
        }

        //Set stream number
        hr = pAudioStream->SetStreamNumber(wStreamNumber);
        if (FAILED(hr))
        {
            goto done;
        }
        
        //Add the stream to the profile
        hr = pProfile->SetStream(pAudioStream);
        if (FAILED(hr))
        {
            goto done;
        }

        wprintf_s(L"Audio Stream created. Stream Number: %d.\n", wStreamNumber);

    done:
        SafeRelease(&pAudioStream);
        SafeRelease(&pAudioType);
        return hr;
    }
    ```

    

    L'esempio di codice seguente crea un flusso video di output.

    ```C++
    //-------------------------------------------------------------------
    //  CreateVideoStream
    //  Create an video stream and add it to the profile.
    //
    //  pProfile: A pointer to the ASF profile.
    //  wStreamNumber: Stream number to assign for the new stream.
    //    pType: A pointer to the source's video media type.
    //-------------------------------------------------------------------

    HRESULT CreateVideoStream(IMFASFProfile* pProfile, WORD wStreamNumber, IMFMediaType* pType)
    {
        if (!pProfile)
        {
            return E_INVALIDARG;
        }
        if (wStreamNumber < 1 || wStreamNumber > 127 )
        {
            return MF_E_INVALIDSTREAMNUMBER;
        }

        HRESULT hr = S_OK;

        
        IMFMediaType* pVideoType = NULL;
        IMFASFStreamConfig* pVideoStream = NULL;

        UINT32 dwBitRate = 0;
            
        //Create a new video type from the source type
        hr = CreateCompressedVideoType(pType, &pVideoType);
        if (FAILED(hr))
        {
            goto done;
        }

        //Create a new stream with the video type
        hr = pProfile->CreateStream(pVideoType, &pVideoStream);
        if (FAILED(hr))
        {
            goto done;
        }
        

        //Set a valid stream number
        hr = pVideoStream->SetStreamNumber(wStreamNumber);
        if (FAILED(hr))
        {
            goto done;
        }

        //Add the stream to the profile
        hr = pProfile->SetStream(pVideoStream);
        if (FAILED(hr))
        {
            goto done;
        }

        wprintf_s(L"Video Stream created. Stream Number: %d .\n", wStreamNumber);

    done:

        SafeRelease(&pVideoStream);
        SafeRelease(&pVideoType);

        return hr;
    }
    ```

    

Nell'esempio di codice seguente vengono creati flussi di output a seconda dei flussi nell'origine.


```C++
    //For each stream in the source, add target stream information in the profile
    for (DWORD iStream = 0; iStream < dwSrcStream; iStream++)
    {
        hr = pPD->GetStreamDescriptorByIndex(
            iStream, &fSelected, &pStreamDesc);
        if (FAILED(hr))
        {
            goto done;
        }

        if (!fSelected)
        {
            continue;
        }

        //Get the media type handler
        hr = pStreamDesc->GetMediaTypeHandler(&pHandler);
        if (FAILED(hr))
        {
            goto done;
        }

        //Get the first media type 
        hr = pHandler->GetMediaTypeByIndex(0, &pMediaType);
        if (FAILED(hr))
        {
            goto done;
        }

        //Get the major type
        hr = pMediaType->GetMajorType(&guidMajor);
        if (FAILED(hr))
        {
            goto done;
        }

        // If this is a video stream, create the target video stream
        if (guidMajor == MFMediaType_Video)
        {
            //The stream level encoding properties will be set in this call
            hr = CreateVideoStream(pProfile, wStreamID, pMediaType);

            if (FAILED(hr))
            {
                goto done;
            }
        }
        
        // If this is an audio stream, create the target audio stream
        if (guidMajor == MFMediaType_Audio)
        {
            //The stream level encoding properties will be set in this call
            hr = CreateAudioStream(pProfile, wStreamID);

            if (FAILED(hr))
            {
                goto done;
            }
        }

        //Get stream's encoding property
        hr = pContentInfo->GetEncodingConfigurationPropertyStore(wStreamID, &pContentInfoProps);
        if (FAILED(hr))
        {
            goto done;
        }

        //Set the stream-level encoding properties
        hr = SetEncodingProperties(guidMajor, pContentInfoProps);       
        if (FAILED(hr))
        {
            goto done;
        }


        SafeRelease(&pMediaType);
        SafeRelease(&pStreamDesc);
        SafeRelease(&pContentInfoProps);
        wStreamID++;
    }
```



### <a name="create-a-compressed-audio-media-type"></a>Creare un tipo di supporto audio compresso

Se si vuole includere un flusso audio nel file di output, creare un tipo di audio specificando le caratteristiche del tipo codificato impostando gli attributi obbligatori. Per assicurarsi che il tipo di audio sia compatibile con il codificatore audio Windows Media, creare un'istanza del codificatore MFT, impostare le proprietà di codifica e ottenere un tipo di supporto chiamando [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype). Ottenere il tipo di output richiesto eseguendo il ciclo di tutti i tipi disponibili, ottenendo gli attributi di ogni tipo di supporto e selezionando il tipo più vicino ai propri requisiti. In questa esercitazione, ottenere il primo tipo disponibile dall'elenco dei tipi di supporti di output supportati dal codificatore.

**Nota**  Per Windows 7, Media Foundation fornisce una nuova funzione, [**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) , che recupera un elenco di tipi audio compatibili. Questa funzione ottiene solo i tipi di supporto per la codifica CBR.

Un tipo audio completo deve avere il set di attributi seguente:

-   [**\_ \_ tipo principale MF \_ mt**](mf-mt-major-type-attribute.md)
-   [**sottotipo MF \_ mt \_**](mf-mt-subtype-attribute.md)
-   [**numero \_ di \_ \_ canali audio MF mt \_**](mf-mt-audio-num-channels-attribute.md)
-   [**\_ \_ campioni audio MF \_ mt \_ al \_ secondo**](mf-mt-audio-samples-per-second-attribute.md)
-   [**\_ \_ \_ allineamento blocchi audio MF \_ mt**](mf-mt-audio-block-alignment-attribute.md)
-   [**\_ \_ Media byte audio MF mt \_ \_ \_ al \_ secondo**](mf-mt-audio-avg-bytes-per-second-attribute.md)
-   [**\_ \_ bit audio MF \_ mt \_ per \_ campione**](mf-mt-audio-bits-per-sample-attribute.md)

Nell'esempio di codice seguente viene creato un tipo di audio compresso ottenendo un tipo compatibile dal codificatore Windows Media Audio. L'implementazione per SetEncodingProperties è illustrata nella sezione "creare l'oggetto di un oggetto ContentInfo ASF" di questa esercitazione.


```C++
//-------------------------------------------------------------------
//  GetOutputTypeFromWMAEncoder
//  Gets a compatible output type from the Windows Media audio encoder.
//
//  ppAudioType: Receives a pointer to the media type.
//-------------------------------------------------------------------

HRESULT GetOutputTypeFromWMAEncoder(IMFMediaType** ppAudioType)
{
    if (!ppAudioType)
    {
        return E_POINTER;
    }

    IMFTransform* pMFT = NULL;
    IMFMediaType* pType = NULL;
    IPropertyStore* pProps = NULL;

    //We need to find a suitable output media type
    //We need to create the encoder to get the available output types
    //and discard the instance.

    CLSID *pMFTCLSIDs = NULL;   // Pointer to an array of CLISDs. 
    UINT32 cCLSID = 0;            // Size of the array.

    MFT_REGISTER_TYPE_INFO tinfo;
    
    tinfo.guidMajorType = MFMediaType_Audio;
    tinfo.guidSubtype = MFAudioFormat_WMAudioV9;

    // Look for an encoder.
    HRESULT hr = MFTEnum(
        MFT_CATEGORY_AUDIO_ENCODER,
        0,                  // Reserved
        NULL,                // Input type to match. None.
        &tinfo,             // WMV encoded type.
        NULL,               // Attributes to match. (None.)
        &pMFTCLSIDs,        // Receives a pointer to an array of CLSIDs.
        &cCLSID             // Receives the size of the array.
        );
    if (FAILED(hr))
    {
        goto done;
    }

    // MFTEnum can return zero matches.
    if (cCLSID == 0)
    {
        hr = MF_E_TOPO_CODEC_NOT_FOUND;
        goto done;
    }
    else
    {
        // Create the MFT decoder
        hr = CoCreateInstance(pMFTCLSIDs[0], NULL,
            CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pMFT));

        if (FAILED(hr))
        {
            goto done;
        }

    }

    // Get the encoder's property store

    hr = pMFT->QueryInterface(IID_PPV_ARGS(&pProps));
    if (FAILED(hr))
    {
        goto done;
    }
    
    //Set encoding properties
    hr = SetEncodingProperties(MFMediaType_Audio, pProps);
    if (FAILED(hr))
    {
        goto done;
    }

    //Get the first output type
    //You can loop through the available output types to choose 
    //the one that meets your target requirements
    hr = pMFT->GetOutputAvailableType(0, 0, &pType);
    if (FAILED(hr))
    {
        goto done;
    }

    //Return to the caller
    *ppAudioType = pType;
    (*ppAudioType)->AddRef();
    
done:
    SafeRelease(&pProps);
    SafeRelease(&pType);
    SafeRelease(&pMFT);
    CoTaskMemFree(pMFTCLSIDs);
    return hr;
}
```



### <a name="create-a-compressed-video-media-type"></a>Creare un tipo di supporto video compresso

Se si vuole includere un flusso video nel file di output, creare un tipo di video con codifica completa. Il tipo di supporto completo deve includere la velocità in bit desiderata e i dati privati del codec.

Esistono due modi per creare un tipo di supporto video completo.

-   Creare un tipo di supporto vuoto e copiare gli attributi del tipo di supporto dal tipo di video di origine e sovrascrivere l'attributo del [**\_ \_ sottotipo MF mt**](mf-mt-subtype-attribute.md) con la costante GUID MFVideoFormat \_ WMV3.

    Un tipo di video completo deve avere il set di attributi seguente:

    -   \_ \_ tipo principale MF \_ mt
    -   sottotipo MF \_ mt \_
    -   \_ \_ frequenza fotogrammi MF mt \_
    -   \_dimensioni del \_ frame MF mt \_
    -   \_modalità di \_ intreccio MF mt \_
    -   proporzioni MF \_ mt \_ pixel \_ \_
    -   \_velocità in \_ bit media MF mt \_
    -   \_ \_ dati utente MF \_ mt

    Nell'esempio di codice seguente viene creato un tipo di video compresso dal tipo di video dell'origine.

    ```C++
    //-------------------------------------------------------------------
    //  CreateCompressedVideoType
    //  Creates an output type from source's video media type.
    //
    //    pType: A pointer to the source's video media type.
    //  ppVideoType: Receives a pointer to the media type.
    //-------------------------------------------------------------------

    HRESULT CreateCompressedVideoType(
            IMFMediaType* pType, 
            IMFMediaType** ppVideoType)
    {
        if (!pType)
        {
            return E_INVALIDARG;
        }
        if (!ppVideoType)
        {
            return E_POINTER;
        }
        
        HRESULT hr = S_OK;
        MFRatio fps = { 0 };
        MFRatio par = { 0 };
        UINT32 width = 0, height = 0;
        UINT32 interlace = MFVideoInterlace_Unknown;
        UINT32 fSamplesIndependent = 0;
        UINT32 cBitrate = 0;

        IMFMediaType* pMediaType = NULL;

        GUID guidMajor = GUID_NULL;

        hr = pType->GetMajorType(&guidMajor);
        if (FAILED(hr))
        {
            goto done;
        }

        if (guidMajor != MFMediaType_Video )
        {
            hr = MF_E_INVALID_FORMAT;
            goto done;
        }

        hr = MFCreateMediaType(&pMediaType);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pType->CopyAllItems(pMediaType);
        if (FAILED(hr))
        {
            goto done;
        }

        //Fill the missing attributes
        //1. Frame rate
        hr = MFGetAttributeRatio(pMediaType, MF_MT_FRAME_RATE, (UINT32*)&fps.Numerator, (UINT32*)&fps.Denominator);
        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            fps.Numerator = 30000;
            fps.Denominator = 1001;

            hr = MFSetAttributeRatio(pMediaType, MF_MT_FRAME_RATE, fps.Numerator, fps.Denominator);
            if (FAILED(hr))
            {
                goto done;
            }
        }

        ////2. Frame size
        hr = MFGetAttributeSize(pMediaType, MF_MT_FRAME_SIZE, &width, &height);
        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            width = 1280;
            height = 720;
                
            hr = MFSetAttributeSize(pMediaType, MF_MT_FRAME_SIZE, width, height);
            if (FAILED(hr))
            {
                goto done;
            }
        }

        ////3. Interlace mode
        
        if (FAILED(pMediaType->GetUINT32(MF_MT_INTERLACE_MODE, &interlace)))
        {
            hr = pMediaType->SetUINT32(MF_MT_INTERLACE_MODE, MFVideoInterlace_Progressive);
            if (FAILED(hr))
            {
                goto done;
            }

        }

        ////4. Pixel aspect Ratio
        hr = MFGetAttributeRatio(pMediaType, MF_MT_PIXEL_ASPECT_RATIO, (UINT32*)&par.Numerator, (UINT32*)&par.Denominator);
        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            par.Numerator = par.Denominator = 1;
            hr = MFSetAttributeRatio(pMediaType, MF_MT_PIXEL_ASPECT_RATIO, (UINT32)par.Numerator, (UINT32)par.Denominator);
            if (FAILED(hr))
            {
                goto done;
            }

        }

        //6. bit rate
        if (FAILED(pMediaType->GetUINT32(MF_MT_AVG_BITRATE, &cBitrate)))
        {
            hr = pMediaType->SetUINT32(MF_MT_AVG_BITRATE, 1000000);
            if (FAILED(hr))
            {
                goto done;
            }

        }

        hr = pMediaType->SetGUID(MF_MT_SUBTYPE, MFVideoFormat_WMV3);
        if (FAILED(hr))
        {
            goto done;
        }

        // Return the pointer to the caller.
        *ppVideoType = pMediaType;
        (*ppVideoType)->AddRef();


    done:
        SafeRelease(&pMediaType);
        return hr;
    }
    
    ```

    

-   Ottenere un tipo di supporto compatibile dal codificatore video Windows Media impostando le proprietà di codifica e quindi chiamando [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype). Questo metodo restituisce il tipo parziale. Assicurarsi di convertire il tipo parziale in un tipo completo aggiungendo le informazioni seguenti:

    -   Impostare la velocità in bit video nell'attributo [**MF \_ mt \_ Avg \_ bitrate**](mf-mt-avg-bitrate-attribute.md) .
    -   Aggiungere i dati privati dei codec impostando l'attributo [**\_ \_ \_ dati utente MF mt**](mf-mt-user-data-attribute.md) . Per istruzioni dettagliate, vedere la sezione relativa ai dati di un codec privato in [configurazione di un codificatore WMV](configuring-a-wmv-encoder.md).

    Poiché [**IWMCodecPrivateData:: GetPrivateData**](../wmformat/iwmcodecprivatedata-getprivatedata.md) controlla la velocità in bit prima di restituire i dati privati del codec, assicurarsi di impostare la velocità in bit prima di ottenere i dati privati del codec.

    Nell'esempio di codice seguente viene creato un tipo di video compresso ottenendo un tipo compatibile dal codificatore Windows Media Video. Crea anche un tipo di video non compresso e lo imposta come input del codificatore. Questa operazione viene implementata nella funzione helper CreateUncompressedVideoType. GetOutputTypeFromWMVEncoder converte il tipo parziale restituito in un tipo completo mediante l'aggiunta di dati privati di codec. L'implementazione per SetEncodingProperties è illustrata nella sezione "creare l'oggetto di un oggetto ContentInfo ASF" di questa esercitazione.

    ```C++
    //-------------------------------------------------------------------
    //  GetOutputTypeFromWMVEncoder
    //  Gets a compatible output type from the Windows Media video encoder.
    //
    //  pType: A pointer to the source video stream's media type.
    //  ppVideoType: Receives a pointer to the media type.
    //-------------------------------------------------------------------

    HRESULT GetOutputTypeFromWMVEncoder(IMFMediaType* pType, IMFMediaType** ppVideoType)
    {
        if (!ppVideoType)
        {
            return E_POINTER;
        }

        IMFTransform* pMFT = NULL;
        IPropertyStore* pProps = NULL;
        IMFMediaType* pInputType = NULL;
        IMFMediaType* pOutputType = NULL;
        
        UINT32 cBitrate = 0;

        //We need to find a suitable output media type
        //We need to create the encoder to get the available output types
        //and discard the instance.

        CLSID *pMFTCLSIDs = NULL;   // Pointer to an array of CLISDs. 
        UINT32 cCLSID = 0;          // Size of the array.

        MFT_REGISTER_TYPE_INFO tinfo;
        
        tinfo.guidMajorType = MFMediaType_Video;
        tinfo.guidSubtype = MFVideoFormat_WMV3;

        // Look for an encoder.
        HRESULT hr = MFTEnum(
            MFT_CATEGORY_VIDEO_ENCODER,
            0,                  // Reserved
            NULL,               // Input type to match. None.
            &tinfo,             // WMV encoded type.
            NULL,               // Attributes to match. (None.)
            &pMFTCLSIDs,        // Receives a pointer to an array of CLSIDs.
            &cCLSID             // Receives the size of the array.
            );
        if (FAILED(hr))
        {
            goto done;
        }

        // MFTEnum can return zero matches.
        if (cCLSID == 0)
        {
            hr = MF_E_TOPO_CODEC_NOT_FOUND;
            goto done;
        }
        else
        {
            //Create the MFT decoder
            hr = CoCreateInstance(pMFTCLSIDs[0], NULL,
                CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pMFT));
            if (FAILED(hr))
            {
                goto done;
            }

        }
        
        //Get the video encoder property store
        hr = pMFT->QueryInterface(IID_PPV_ARGS(&pProps));
        if (FAILED(hr))
        {
            goto done;
        }

        //Set encoding properties
        hr = SetEncodingProperties(MFMediaType_Video, pProps);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = CreateUncompressedVideoType(pType, &pInputType);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pMFT->SetInputType(0, pInputType, 0);

        //Get the first output type
        //You can loop through the available output types to choose 
        //the one that meets your target requirements
        hr =  pMFT->GetOutputAvailableType(0, 0, &pOutputType);
        if (FAILED(hr))
        {
            goto done;
        }
        
        hr = pType->GetUINT32(MF_MT_AVG_BITRATE, &cBitrate);
        if (FAILED(hr))
        {
            goto done;
        }

        //Now set the bit rate
        hr = pOutputType->SetUINT32(MF_MT_AVG_BITRATE, cBitrate);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = AddPrivateData(pMFT, pOutputType);
        if (FAILED(hr))
        {
            goto done;
        }

        //Return to the caller
        *ppVideoType = pOutputType;
        (*ppVideoType)->AddRef();
        
    done:
        SafeRelease(&pProps);
        SafeRelease(&pOutputType);
        SafeRelease(&pInputType);
        SafeRelease(&pMFT);
        CoTaskMemFree(pMFTCLSIDs);
        return hr;
    }
    ```

    

    Nell'esempio di codice seguente viene creato un tipo di video non compresso.

    ```C++
    //-------------------------------------------------------------------
    //  CreateUncompressedVideoType
    //  Creates an uncompressed video type.
    //
    //    pType: A pointer to the source's video media type.
    //  ppVideoType: Receives a pointer to the media type.
    //-------------------------------------------------------------------

    HRESULT CreateUncompressedVideoType(IMFMediaType* pType, IMFMediaType** ppMediaType)
    {
        if (!pType)
        {
            return E_INVALIDARG;
        }
        if (!ppMediaType)
        {
            return E_POINTER;
        }
        
        MFRatio fps = { 0 };
        MFRatio par = { 0 };
        UINT32 width = 0, height = 0;
        UINT32 interlace = MFVideoInterlace_Unknown;
        UINT32 cBitrate = 0;

        IMFMediaType* pMediaType = NULL;

        GUID guidMajor = GUID_NULL;

        HRESULT hr = pType->GetMajorType(&guidMajor);
        if (FAILED(hr))
        {
            goto done;
        }

        if (guidMajor != MFMediaType_Video )
        {
            hr = MF_E_INVALID_FORMAT;
            goto done;
        }

        hr = MFGetAttributeRatio(pType, MF_MT_FRAME_RATE, (UINT32*)&fps.Numerator, (UINT32*)&fps.Denominator);
        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            fps.Numerator = 30000;
            fps.Denominator = 1001;

        }
        hr = MFGetAttributeSize(pType, MF_MT_FRAME_SIZE, &width, &height);
        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            width = 1280;
            height = 720;

        }

        interlace = MFGetAttributeUINT32(pType, MF_MT_INTERLACE_MODE, MFVideoInterlace_Progressive);

        hr = MFGetAttributeRatio(pType, MF_MT_PIXEL_ASPECT_RATIO, (UINT32*)&par.Numerator, (UINT32*)&par.Denominator);
        if (FAILED(hr))
        {
            par.Numerator = par.Denominator = 1;
        }

        cBitrate = MFGetAttributeUINT32(pType, MF_MT_AVG_BITRATE, 1000000);

        hr = MFCreateMediaType(&pMediaType);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = pMediaType->SetGUID(MF_MT_MAJOR_TYPE, guidMajor);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = pMediaType->SetGUID(MF_MT_SUBTYPE, MFVideoFormat_RGB32);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = MFSetAttributeRatio(pMediaType, MF_MT_FRAME_RATE, fps.Numerator, fps.Denominator);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = MFSetAttributeSize(pMediaType, MF_MT_FRAME_SIZE, width, height);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = pMediaType->SetUINT32(MF_MT_INTERLACE_MODE, 2);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pMediaType->SetUINT32(MF_MT_ALL_SAMPLES_INDEPENDENT, TRUE);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pMediaType->SetUINT32(MF_MT_AVG_BITRATE, cBitrate);
        if (FAILED(hr))
        {
            goto done;
        }

        // Return the pointer to the caller.
        *ppMediaType = pMediaType;
        (*ppMediaType)->AddRef();


    done:
        SafeRelease(&pMediaType);
        return hr;
    }
    ```

    

    Nell'esempio di codice seguente i dati privati del codec vengono aggiunti al tipo di supporto video specificato.

    ```C++
    //
    // AddPrivateData
    // Appends the private codec data to a media type.
    //
    // pMFT: The video encoder
    // pTypeOut: A video type from the encoder's type list.
    //
    // The function modifies pTypeOut by adding the codec data.
    //

    HRESULT AddPrivateData(IMFTransform *pMFT, IMFMediaType *pTypeOut)
    {
        HRESULT hr = S_OK;
        ULONG cbData = 0;
        BYTE *pData = NULL;

        IWMCodecPrivateData *pPrivData = NULL;

        DMO_MEDIA_TYPE mtOut = { 0 };

        // Convert the type to a DMO type.
        hr = MFInitAMMediaTypeFromMFMediaType(
            pTypeOut, 
            FORMAT_VideoInfo, 
            (AM_MEDIA_TYPE*)&mtOut
            );
        
        if (SUCCEEDED(hr))
        {
            hr = pMFT->QueryInterface(IID_PPV_ARGS(&pPrivData));
        }

        if (SUCCEEDED(hr))
        {
            hr = pPrivData->SetPartialOutputType(&mtOut);
        }

        //
        // Get the private codec data
        //

        // First get the buffer size.
        if (SUCCEEDED(hr))
        {
            hr = pPrivData->GetPrivateData(NULL, &cbData);
        }

        if (SUCCEEDED(hr))
        {
            pData = new BYTE[cbData];

            if (pData == NULL)
            {
                hr = E_OUTOFMEMORY;
            }
        }

        // Now get the data.
        if (SUCCEEDED(hr))
        {
            hr = pPrivData->GetPrivateData(pData, &cbData);
        }

        // Add the data to the media type.
        if (SUCCEEDED(hr))
        {
            hr = pTypeOut->SetBlob(MF_MT_USER_DATA, pData, cbData);
        }

        delete [] pData;
        MoFreeMediaType(&mtOut);
        SafeRelease(&pPrivData);
        return hr;
    }
    ```

    

### <a name="create-the-asf-contentinfo-object"></a>Creare l'oggetto ContentInfo ASF

L'oggetto di questo oggetto è un componente di livello WMContainer progettato principalmente per archiviare le informazioni sull'oggetto intestazione ASF. Il sink di file ASF implementa l'oggetto ContentInfo per archiviare le informazioni (in un archivio di proprietà) che verranno usate per scrivere l'oggetto intestazione ASF del file codificato. A tale scopo, è necessario creare e configurare il set di Informazioni seguente nell'oggetto ContentInfo prima di avviare la sessione di codifica.

1.  Chiamare [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) per creare un oggetto ContentInfo vuoto.

    Nell'esempio di codice seguente viene creato un oggetto ContentInfo vuoto.

    ```C++
        // Create an empty ContentInfo object
        hr = MFCreateASFContentInfo(&pContentInfo);
        if (FAILED(hr))
        {
            goto done;
        }
    
    ```

    

2.  Chiamare [**IMFASFContentInfo:: GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) per ottenere l'archivio delle proprietà a livello di flusso del sink di file. In questa chiamata, è necessario passare il numero di flusso assegnato per il flusso durante la creazione del profilo ASF.
3.  Impostare le [proprietà di codifica](configuring-the-encoder.md) a livello di flusso nell'archivio delle proprietà di flusso del sink di file. Per ulteriori informazioni, vedere la sezione relativa alle proprietà di codifica del flusso in [impostazione delle proprietà nel sink di file](setting-properties-in-the-file-sink.md).

    Nell'esempio di codice seguente vengono impostate le proprietà a livello di flusso nell'archivio delle proprietà del sink di file.

    ```C++
            //Get stream's encoding property
            hr = pContentInfo->GetEncodingConfigurationPropertyStore(wStreamID, &pContentInfoProps);
            if (FAILED(hr))
            {
                goto done;
            }

            //Set the stream-level encoding properties
            hr = SetEncodingProperties(guidMajor, pContentInfoProps);       
            if (FAILED(hr))
            {
                goto done;
            }

    
    ```

    

    Nell'esempio di codice riportato di seguito viene illustrata l'implementazione di SetEncodingProperties. Questa funzione imposta le proprietà di codifica a livello di flusso per CBR e VBR.

    ```C++
    //-------------------------------------------------------------------
    //  SetEncodingProperties
    //  Create a media source from a URL.
    //
    //  guidMT:  Major type of the stream, audio or video
    //  pProps:  A pointer to the property store in which 
    //           to set the required encoding properties.
    //-------------------------------------------------------------------

    HRESULT SetEncodingProperties (const GUID guidMT, IPropertyStore* pProps)
    {
        if (!pProps)
        {
            return E_INVALIDARG;
        }

        if (EncodingMode == NONE)
        {
            return MF_E_NOT_INITIALIZED;
        }
       
        HRESULT hr = S_OK;

        PROPVARIANT var;

        switch (EncodingMode)
        {
            case CBR:
                // Set VBR to false.
                hr = InitPropVariantFromBoolean(FALSE, &var);
                if (FAILED(hr))
                {
                    goto done;
                }

                hr = pProps->SetValue(MFPKEY_VBRENABLED, var);
                if (FAILED(hr))
                {
                    goto done;
                }

                // Set the video buffer window.
                if (guidMT == MFMediaType_Video)
                {
                    hr = InitPropVariantFromInt32(VIDEO_WINDOW_MSEC, &var);
                    if (FAILED(hr))
                    {
                        goto done;
                    }

                    hr = pProps->SetValue(MFPKEY_VIDEOWINDOW, var);    
                    if (FAILED(hr))
                    {
                        goto done;
                    }
                }
                break;

            case VBR:
                //Set VBR to true.
                hr = InitPropVariantFromBoolean(TRUE, &var);
                if (FAILED(hr))
                {
                    goto done;
                }

                hr = pProps->SetValue(MFPKEY_VBRENABLED, var);
                if (FAILED(hr))
                {
                    goto done;
                }

                // Number of encoding passes is 1.

                hr = InitPropVariantFromInt32(1, &var);
                if (FAILED(hr))
                {
                    goto done;
                }

                hr = pProps->SetValue(MFPKEY_PASSESUSED, var);
                if (FAILED(hr))
                {
                    goto done;
                }

                // Set the quality level.

                if (guidMT == MFMediaType_Audio)
                {
                    hr = InitPropVariantFromUInt32(98, &var);
                    if (FAILED(hr))
                    {
                        goto done;
                    }

                    hr = pProps->SetValue(MFPKEY_DESIRED_VBRQUALITY, var);    
                    if (FAILED(hr))
                    {
                        goto done;
                    }
                }
                else if (guidMT == MFMediaType_Video)
                {
                    hr = InitPropVariantFromUInt32(95, &var);
                    if (FAILED(hr))
                    {
                        goto done;
                    }

                    hr = pProps->SetValue(MFPKEY_VBRQUALITY, var);    
                    if (FAILED(hr))
                    {
                        goto done;
                    }
                }
                break;

            default:
                hr = E_UNEXPECTED;
                break;
        }    

    done:
        PropVariantClear(&var);
        return hr;
    }
    ```

    

4.  Chiamare [**IMFASFContentInfo:: GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) per ottenere l'archivio delle proprietà globali del sink di file. In questa chiamata, è necessario passare 0 nel primo parametro. Per ulteriori informazioni, vedere l'argomento relativo alle proprietà di sink di file globali in [impostazione delle proprietà nel sink di file](setting-properties-in-the-file-sink.md).
5.  Impostare la [**velocità in bit di MFPKEY \_ ASFMEDIASINK \_ AutoAdjust \_**](mfpkey-asfmediasink-autoadjust-bitrate-property.md) su Variant \_ true per assicurarsi che i valori dei bucket persi nel multiplexer ASF siano stati modificati correttamente. Per informazioni su questa proprietà, vedere l'argomento relativo all'inizializzazione del multiplexer e alle impostazioni dei bucket persi nella [creazione dell'oggetto multiplexer](creating-the-multiplexer-object.md).

    Nell'esempio di codice seguente vengono impostate le proprietà a livello di flusso nell'archivio delle proprietà del sink di file.

    ```C++
        //Now we need to set global properties that will be set on the media sink
        hr = pContentInfo->GetEncodingConfigurationPropertyStore(0, &pContentInfoProps);
        if (FAILED(hr))
        {
            goto done;
        }

        //Auto adjust Bitrate
        var.vt = VT_BOOL;
        var.boolVal = VARIANT_TRUE;

        hr = pContentInfoProps->SetValue(MFPKEY_ASFMEDIASINK_AUTOADJUST_BITRATE, var);
        
        //Initialize with the profile
        hr = pContentInfo->SetProfile(pProfile);
        if (FAILED(hr))
        {
            goto done;
        }
    ```

    

    > [!Note]  
    > Sono disponibili altre proprietà che è possibile impostare a livello globale per il sink di file. Per ulteriori informazioni, vedere "configurazione dell'oggetto ContentInfo con le impostazioni del codificatore" in [impostazione delle proprietà nell'oggetto ContentInfo](setting-properties-in-the-contentinfo-object.md).

     

Per creare un oggetto attivazione per il sink di file ASF (descritto nella sezione successiva) verrà usato il file di configurazione ASF configurato.

Se si sta creando un sink di file out-of-process ([**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate)), ovvero usando un oggetto Activation, è possibile usare l'oggetto ContentInfo configurato per creare un'istanza del sink multimediale ASF (descritto nella sezione successiva). Se si sta creando un sink di file in-process ([**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink)), anziché creare l'oggetto ContentInfo vuoto come descritto nel passaggio 1, ottenere un riferimento all'interfaccia [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) chiamando **IMFMediaSink:: QueryInterface** sul sink di file. È quindi necessario configurare l'oggetto ContentInfo come descritto in questa sezione.

### <a name="create-the-asf-file-sink"></a>Creare il sink di file ASF

In questo passaggio dell'esercitazione verrà usato il file ASF configurato, creato nel passaggio precedente, per creare un oggetto attivazione per il sink di file ASF chiamando la funzione [**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate) . Per ulteriori informazioni, vedere [creazione del sink di file ASF](creating-the-asf-file-sink.md).

Nell'esempio di codice seguente viene creato l'oggetto attivazione per il sink di file.


```C++
    //Create the activation object for the  file sink
    hr = MFCreateASFMediaSinkActivate(sURL, pContentInfo, &pActivate);
    if (FAILED(hr))
    {
        goto done;
    }

```



## <a name="build-the-partial-encoding-topology"></a>Compilare la topologia di codifica parziale

Successivamente, verrà compilata una topologia di codifica parziale creando nodi della topologia per l'origine multimediale, i codificatori Windows Media necessari e il sink di file ASF. Dopo aver aggiunto i nodi della topologia, è necessario connettere i nodi di origine, trasformazione e sink. Prima di aggiungere nodi della topologia, è necessario creare un oggetto topologia vuoto chiamando [**MFCreateTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology).

### <a name="create-the-source-topology-node-for-the-media-source"></a>Creare il nodo topologia di origine per l'origine multimediale

In questo passaggio verrà creato il nodo della topologia di origine per l'origine multimediale.

Per creare questo nodo sono necessari i riferimenti seguenti:

-   Un puntatore all'origine multimediale creata nel passaggio descritto nella sezione "creare l'origine dei supporti" di questa esercitazione.
-   Puntatore al descrittore di presentazione per l'origine multimediale. È possibile ottenere un riferimento all'interfaccia IMFPresentationDescriptor dell'origine multimediale chiamando [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).
-   Puntatore al descrittore di flusso per ogni flusso nell'origine multimediale per cui è stato creato un flusso di destinazione nel passaggio descritto nella sezione "creare l'oggetto profilo ASF" di questa esercitazione.

Per ulteriori informazioni sulla creazione di nodi di origine ed esempi di codice, vedere [creazione di nodi di origine](creating-source-nodes.md).

Nell'esempio di codice seguente viene creata una topologia parziale aggiungendo il nodo di origine e i nodi di trasformazione necessari. Questo codice chiama le funzioni di supporto AddSourceNode e AddTransformOutputNodes. Queste funzioni sono incluse più avanti in questa esercitazione.


```C++
//-------------------------------------------------------------------
//  BuildPartialTopology
//  Create a partial encoding topology by adding the source and the sink.
//
//  pSource:  A pointer to the media source to enumerate the source streams.
//  pSinkActivate: A pointer to the activation object for ASF file sink.
//  ppTopology:  Receives a pointer to the topology.
//-------------------------------------------------------------------

HRESULT BuildPartialTopology(
       IMFMediaSource *pSource, 
       IMFActivate* pSinkActivate,
       IMFTopology** ppTopology)
{
    if (!pSource || !pSinkActivate)
    {
        return E_INVALIDARG;
    }
    if (!ppTopology)
    {
        return E_POINTER;
    }

    HRESULT hr = S_OK;

    IMFPresentationDescriptor* pPD = NULL;
    IMFStreamDescriptor *pStreamDesc = NULL;
    IMFMediaTypeHandler* pMediaTypeHandler = NULL;
    IMFMediaType* pSrcType = NULL;

    IMFTopology* pTopology = NULL;
    IMFTopologyNode* pSrcNode = NULL;
    IMFTopologyNode* pEncoderNode = NULL;
    IMFTopologyNode* pOutputNode = NULL;


    DWORD cElems = 0;
    DWORD dwSrcStream = 0;
    DWORD StreamID = 0;
    GUID guidMajor = GUID_NULL;
    BOOL fSelected = FALSE;


    //Create the topology that represents the encoding pipeline
    hr = MFCreateTopology (&pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

        
    hr = pSource->CreatePresentationDescriptor(&pPD);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pPD->GetStreamDescriptorCount(&dwSrcStream);
    if (FAILED(hr))
    {
        goto done;
    }

    for (DWORD iStream = 0; iStream < dwSrcStream; iStream++)
    {
        hr = pPD->GetStreamDescriptorByIndex(
            iStream, &fSelected, &pStreamDesc);
        if (FAILED(hr))
        {
            goto done;
        }

        if (!fSelected)
        {
            continue;
        }

        hr = AddSourceNode(pTopology, pSource, pPD, pStreamDesc, &pSrcNode);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pStreamDesc->GetMediaTypeHandler (&pMediaTypeHandler);
        if (FAILED(hr))
        {
            goto done;
        }
        
        hr = pStreamDesc->GetStreamIdentifier(&StreamID);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pMediaTypeHandler->GetMediaTypeByIndex(0, &pSrcType);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pSrcType->GetMajorType(&guidMajor);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = AddTransformOutputNodes(pTopology, pSinkActivate, pSrcType, &pEncoderNode);
        if (FAILED(hr))
        {
            goto done;
        }

        //now we have the transform node, connect it to the source node
        hr = pSrcNode->ConnectOutput(0, pEncoderNode, 0);
        if (FAILED(hr))
        {
            goto done;
        }
                

        SafeRelease(&pStreamDesc);
        SafeRelease(&pMediaTypeHandler);
        SafeRelease(&pSrcType);
        SafeRelease(&pEncoderNode);
        SafeRelease(&pOutputNode);
        guidMajor = GUID_NULL;
    }

    *ppTopology = pTopology;
   (*ppTopology)->AddRef();


    wprintf_s(L"Partial Topology Built.\n");

done:
    SafeRelease(&pStreamDesc);
    SafeRelease(&pMediaTypeHandler);
    SafeRelease(&pSrcType);
    SafeRelease(&pEncoderNode);
    SafeRelease(&pOutputNode);
    SafeRelease(&pTopology);

    return hr;
}
```



Nell'esempio di codice seguente viene creato e aggiunto il nodo della topologia di origine alla topologia di codifica. Accetta i puntatori a un oggetto topologia precedente, l'origine multimediale per enumerare i flussi di origine, il descrittore di presentazione dell'origine multimediale e il descrittore del flusso dell'origine multimediale. Il chiamante riceve un puntatore al nodo della topologia di origine.


```C++
// Add a source node to a topology.
HRESULT AddSourceNode(
    IMFTopology *pTopology,           // Topology.
    IMFMediaSource *pSource,          // Media source.
    IMFPresentationDescriptor *pPD,   // Presentation descriptor.
    IMFStreamDescriptor *pSD,         // Stream descriptor.
    IMFTopologyNode **ppNode)         // Receives the node pointer.
{
    IMFTopologyNode *pNode = NULL;

    // Create the node.
    HRESULT hr = MFCreateTopologyNode(MF_TOPOLOGY_SOURCESTREAM_NODE, &pNode);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the attributes.
    hr = pNode->SetUnknown(MF_TOPONODE_SOURCE, pSource);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pNode->SetUnknown(MF_TOPONODE_PRESENTATION_DESCRIPTOR, pPD);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pNode->SetUnknown(MF_TOPONODE_STREAM_DESCRIPTOR, pSD);
    if (FAILED(hr))
    {
        goto done;
    }
    
    // Add the node to the topology.
    hr = pTopology->AddNode(pNode);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the pointer to the caller.
    *ppNode = pNode;
    (*ppNode)->AddRef();

done:
    SafeRelease(&pNode);
    return hr;
}
```



### <a name="instantiate-the-required-encoders-and-create-the-transform-nodes"></a>Creare un'istanza dei codificatori necessari e creare i nodi di trasformazione

La pipeline Media Foundation non inserisce automaticamente i codificatori Windows Media richiesti per i flussi che devono essere codificati. L'applicazione deve aggiungere i codificatori manualmente. A tale scopo, enumerare i flussi nel profilo ASF creati nel passaggio descritto nella sezione "creare l'oggetto profilo ASF" di questa esercitazione. Per ogni flusso nell'origine e il flusso corrispondente nel profilo, creare un'istanza dei codificatori necessari. Per questo passaggio, è necessario un puntatore all'oggetto attivazione per il sink di file creato nel passaggio descritto nella sezione "creare il sink di file ASF" di questa esercitazione.

Per una panoramica sulla creazione di codificatori tramite oggetti di attivazione, vedere [uso di oggetti di attivazione di un codificatore](using-an-encoder-s-activation-objects.md).

Nella procedura riportata di seguito vengono descritti i passaggi necessari per creare un'istanza dei codificatori necessari.

1.  Ottenere un riferimento all'oggetto ContentInfo del sink chiamando [**IMFActivate:: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) sull'attivazione del sink di file e quindi eseguendo una query per [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) dal sink di file chiamando **QueryInterface**.
2.  Ottenere il profilo ASF associato all'oggetto ContentInfo chiamando [**IMFASFContentInfo:: GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile).
3.  Enumerare i flussi nel profilo. A tale proposito, sarà necessario il numero di flussi e un riferimento all'interfaccia [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) di ogni flusso.

    Chiamare i metodi seguenti:

    -   [**IMFASFProfile::GetStreamCount**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamcount)
    -   [**IMFASFProfile:: GetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream)

4.  Per ogni flusso, ottenere il tipo principale e le proprietà di codifica del flusso dall'oggetto ContentInfo.

    Chiamare i metodi seguenti:

    -   [**IMFASFStreamConfig::GetMediaType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getmediatype)
    -   [**IMFMediaType::GetMajorType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getmajortype)
    -   [**IMFASFContentInfo::GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore)

        Per questa chiamata è necessario il numero di flusso recuperato dalla chiamata [**IMFASFProfile:: GetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream) .

5.  A seconda del tipo di flusso, audio o video, creare un'istanza dell'oggetto attivazione per il codificatore chiamando [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) o [**MFCreateWMVEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate).

    Per chiamare queste funzioni, sono necessari i riferimenti seguenti:

    -   Puntatore al tipo di supporto del flusso recuperato da [**IMFASFStreamConfig:: GetMediaType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getmediatype) nel passaggio precedente.
    -   Puntatore all'archivio delle proprietà di codifica del flusso recuperato da [**IMFASFContentInfo:: GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore). Passando un puntatore all'archivio delle proprietà, le proprietà del flusso impostate nel sink di file vengono copiate nel file con estensione MFT del codificatore.

6.  Aggiornare il parametro bucket Leaky per il flusso audio.

    [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) imposta il tipo di output sul codificatore MFT sottostante per il codec audio Windows Media. Dopo aver impostato il tipo di supporto di output, il codificatore ottiene la velocità in bit media dal tipo di supporto di output, calcola la velocità in bit della finestra del buffer e imposta i valori bucket che verranno usati durante la sessione di codifica. È possibile aggiornare questi valori nel sink di file eseguendo una query sul codificatore o impostando i valori personalizzati. Per aggiornare i valori, è necessario il set di Informazioni seguente:

    -   Velocità in bit media: ottenere la velocità in bit media dall'attributo [**MF \_ mt \_ audio \_ Avg \_ bytes \_ al \_ secondo**](mf-mt-audio-avg-bytes-per-second-attribute.md) impostato sul tipo di supporto di output selezionato durante la negoziazione del tipo di supporto.
    -   Finestra buffer: è possibile recuperarla chiamando [**IWMCodecLeakyBucket:: GetBufferSizeBits**](../wmformat/iwmcodecleakybucket-getbuffersizebits.md).
    -   Dimensioni iniziali del buffer: impostare su 0.

    Creare una matrice di valori DWORD e impostare il valore nella proprietà [**MFPKEY \_ ASFSTREAMSINK \_ corrected \_ LEAKYBUCKET**](mfpkey-asfstreamsink-corrected-leakybucket-property.md) del sink del flusso audio. Se non si specificano i valori aggiornati, la sessione multimediale li imposta in modo appropriato.

    Per ulteriori informazioni, vedere [il modello di buffer di bucket a perdita](the-leaky-bucket-buffer-model.md).

Gli oggetti attivazione creati nel passaggio 5 devono essere aggiunti alla topologia come nodi della topologia di trasformazione. Per ulteriori informazioni ed esempi di codice, vedere "creazione di un nodo Transform da un oggetto Activation" in [creazione di nodi di trasformazione](creating-transform-nodes.md).

Nell'esempio di codice seguente viene creato e aggiunto il codificatore richiesto attivato. Accetta i puntatori a un oggetto topologia creato in precedenza, l'oggetto attivazione del sink di file e il tipo di supporto del flusso di origine. Chiama anche AddOutputNode (vedere l'esempio di codice successivo) che crea e aggiunge il nodo sink alla topologia di codifica. Il chiamante riceve un puntatore al nodo della topologia di origine.


```C++
//-------------------------------------------------------------------
//  AddTransformOutputNodes
//  Creates and adds the sink node to the encoding topology.
//  Creates and adds the required encoder activates.

//  pTopology:  A pointer to the topology.
//  pSinkActivate:  A pointer to the file sink's activation object.
//  pSourceType: A pointer to the source stream's media type.
//  ppNode:  Receives a pointer to the topology node.
//-------------------------------------------------------------------

HRESULT AddTransformOutputNodes(
    IMFTopology* pTopology,
    IMFActivate* pSinkActivate,
    IMFMediaType* pSourceType,
    IMFTopologyNode **ppNode    // Receives the node pointer.
    )
{
    if (!pTopology || !pSinkActivate || !pSourceType)
    {
        return E_INVALIDARG;
    }

    IMFTopologyNode* pEncNode = NULL;
    IMFTopologyNode* pOutputNode = NULL;
    IMFASFContentInfo* pContentInfo = NULL;
    IMFASFProfile* pProfile = NULL;
    IMFASFStreamConfig* pStream = NULL;
    IMFMediaType* pMediaType = NULL;
    IPropertyStore* pProps = NULL;
    IMFActivate *pEncoderActivate = NULL;
    IMFMediaSink *pSink = NULL; 

    GUID guidMT = GUID_NULL;
    GUID guidMajor = GUID_NULL;

    DWORD cStreams = 0;
    WORD wStreamNumber = 0;

    HRESULT hr = S_OK;
        
    hr = pSourceType->GetMajorType(&guidMajor);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the node.
    hr = MFCreateTopologyNode(MF_TOPOLOGY_TRANSFORM_NODE, &pEncNode);
    if (FAILED(hr))
    {
        goto done;
    }
    
    //Activate the sink
    hr = pSinkActivate->ActivateObject(__uuidof(IMFMediaSink), (void**)&pSink);
    if (FAILED(hr))
    {
        goto done;
    }
    //find the media type in the sink
    //Get content info from the sink
    hr = pSink->QueryInterface(__uuidof(IMFASFContentInfo), (void**)&pContentInfo);
    if (FAILED(hr))
    {
        goto done;
    }
    

    hr = pContentInfo->GetProfile(&pProfile);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pProfile->GetStreamCount(&cStreams);
    if (FAILED(hr))
    {
        goto done;
    }

    for(DWORD index = 0; index < cStreams ; index++)
    {
        hr = pProfile->GetStream(index, &wStreamNumber, &pStream);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = pStream->GetMediaType(&pMediaType);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = pMediaType->GetMajorType(&guidMT);
        if (FAILED(hr))
        {
            goto done;
        }
        if (guidMT!=guidMajor)
        {
            SafeRelease(&pStream);
            SafeRelease(&pMediaType);
            guidMT = GUID_NULL;

            continue;
        }
        //We need to activate the encoder
        hr = pContentInfo->GetEncodingConfigurationPropertyStore(wStreamNumber, &pProps);
        if (FAILED(hr))
        {
            goto done;
        }

        if (guidMT == MFMediaType_Audio)
        {
             hr = MFCreateWMAEncoderActivate(pMediaType, pProps, &pEncoderActivate);
            if (FAILED(hr))
            {
                goto done;
            }
            wprintf_s(L"Audio Encoder created. Stream Number: %d .\n", wStreamNumber);

            break;
        }
        if (guidMT == MFMediaType_Video)
        {
            hr = MFCreateWMVEncoderActivate(pMediaType, pProps, &pEncoderActivate);
            if (FAILED(hr))
            {
                goto done;
            }
            wprintf_s(L"Video Encoder created. Stream Number: %d .\n", wStreamNumber);

            break;
        }
    }

    // Set the object pointer.
    hr = pEncNode->SetObject(pEncoderActivate);
    if (FAILED(hr))
    {
        goto done;
    }

    // Add the node to the topology.
    hr = pTopology->AddNode(pEncNode);
    if (FAILED(hr))
    {
        goto done;
    }

    //Add the output node to this node.
    hr = AddOutputNode(pTopology, pSinkActivate, wStreamNumber, &pOutputNode);
    if (FAILED(hr))
    {
        goto done;
    }

    //now we have the output node, connect it to the transform node
    hr = pEncNode->ConnectOutput(0, pOutputNode, 0);
    if (FAILED(hr))
    {
        goto done;
    }

   // Return the pointer to the caller.
    *ppNode = pEncNode;
    (*ppNode)->AddRef();


done:
    SafeRelease(&pEncNode);
    SafeRelease(&pOutputNode);
    SafeRelease(&pEncoderActivate);
    SafeRelease(&pMediaType);
    SafeRelease(&pProps);
    SafeRelease(&pStream);
    SafeRelease(&pProfile);
    SafeRelease(&pContentInfo);
    SafeRelease(&pSink);
    return hr;
}
```



### <a name="create-the-output-topology-nodes-for-the-file-sink"></a>Creare i nodi della topologia di output per il sink di file

In questo passaggio verrà creato il nodo della topologia di output per il sink di file ASF.

Per creare questo nodo sono necessari i riferimenti seguenti:

-   Un puntatore all'oggetto attivazione creato nel passaggio descritto nella sezione "creare il sink di file ASF" di questa esercitazione.
-   I numeri di flusso per identificare i sink del flusso aggiunti al sink di file. I numeri dei flussi corrispondono all'identificazione del flusso impostata durante la creazione del flusso.

Per ulteriori informazioni sulla creazione di nodi di output ed esempi di codice, vedere la sezione relativa alla creazione di un nodo di output da un oggetto Activation in [creazione di nodi di output](creating-output-nodes.md).

Se non si utilizza l'oggetto attivazione per il sink di file, è necessario enumerare i sink di flusso nel sink di file ASF e impostare ogni sink di flusso come nodo di output nella topologia. Per informazioni sull'enumerazione del sink di flusso, vedere "enumerazione dei sink di flusso" in [aggiunta di informazioni sul flusso al sink di file ASF](adding-stream-information-to-the-asf-file-sink.md).

Nell'esempio di codice seguente viene creato e aggiunto il nodo sink alla topologia di codifica. Accetta i puntatori a un oggetto topologia creato in precedenza, l'oggetto attivazione del sink di file e il numero di identificazione del flusso. Il chiamante riceve un puntatore al nodo della topologia di origine.


```C++
// Add an output node to a topology.
HRESULT AddOutputNode(
    IMFTopology *pTopology,     // Topology.
    IMFActivate *pActivate,     // Media sink activation object.
    DWORD dwId,                 // Identifier of the stream sink.
    IMFTopologyNode **ppNode)   // Receives the node pointer.
{
    IMFTopologyNode *pNode = NULL;

    // Create the node.
    HRESULT hr = MFCreateTopologyNode(MF_TOPOLOGY_OUTPUT_NODE, &pNode);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the object pointer.
    hr = pNode->SetObject(pActivate);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the stream sink ID attribute.
    hr = pNode->SetUINT32(MF_TOPONODE_STREAMID, dwId);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pNode->SetUINT32(MF_TOPONODE_NOSHUTDOWN_ON_REMOVE, FALSE);
    if (FAILED(hr))
    {
        goto done;
    }

    // Add the node to the topology.
    hr = pTopology->AddNode(pNode);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the pointer to the caller.
    *ppNode = pNode;
    (*ppNode)->AddRef();

done:
    SafeRelease(&pNode);
    return hr;
}
```



Nell'esempio di codice seguente vengono enumerati i sink di flusso per un determinato sink multimediale.


```C++
//-------------------------------------------------------------------
//  EnumerateStreamSinks
//  Enumerates the stream sinks within the specified media sink.
//
//  pSink:  A pointer to the media sink.
//-------------------------------------------------------------------
HRESULT EnumerateStreamSinks (IMFMediaSink* pSink)
{
    if (!pSink)
    {
        return E_INVALIDARG;
    }
    
    IMFStreamSink* pStreamSink = NULL;
    DWORD cStreamSinks = 0;

    HRESULT hr = pSink->GetStreamSinkCount(&cStreamSinks);
    if (FAILED(hr))
    {
        goto done;
    }

    for(DWORD index = 0; index < cStreamSinks; index++)
    {
        hr = pSink->GetStreamSinkByIndex (index, &pStreamSink);
        if (FAILED(hr))
        {
            goto done;
        }

        //Use the stream sink
        //Not shown.
    }
done:
    SafeRelease(&pStreamSink);

    return hr;
}
```



### <a name="connect-the-source-transform-and-sink-nodes"></a>Connettere i nodi di origine, trasformazione e sink

In questo passaggio si collegherà il nodo di origine al nodo Transform che fa riferimento alla codifica attivata che è stata creata nel passaggio descritto nella sezione "creare un'istanza dei codificatori necessari e creare i nodi di trasformazione" di questa esercitazione. Il nodo Transform verrà connesso al nodo di output contenente l'oggetto Activation per il sink di file.

## <a name="handling-the-encoding-session"></a>Gestione della sessione di codifica

Nel passaggio si eseguiranno i passaggi seguenti:

1.  Chiamare [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) per creare una sessione di codifica.
2.  Chiamare [**IMFMediaSession:: Setopologia**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) per impostare la topologia di codifica nella sessione. Se la chiamata viene completata, la sessione multimediale valuta i nodi della topologia e inserisce oggetti Transform aggiuntivi, ad esempio un decodificatore, che converte l'origine compressa specificata in campioni non compressi da inserire come input nel codificatore.
3.  Chiamare [**IMFMediaSession:: GetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-getevent) per richiedere gli eventi generati dalla sessione multimediale.

    Nel ciclo di eventi si avvierà e si chiude la sessione di codifica a seconda degli eventi generati dalla sessione multimediale. La chiamata a [**IMFMediaSession:: Setopologie**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) genera una sessione multimediale che genera l'evento [MESessionTopologyStatus](mesessiontopologystatus.md) con il \_ flag di disponibilità MF TOPOSTATUS \_ impostato. Tutti gli eventi vengono generati in modo asincrono e un'applicazione può recuperare questi eventi in modo sincrono o asincrono. Poiché l'applicazione in questa esercitazione è un'applicazione console e il blocco dei thread dell'interfaccia utente non costituisce un problema, gli eventi vengono generati in modo sincrono dalla sessione multimediale.

    Per ottenere gli eventi in modo asincrono, l'applicazione deve implementare l'interfaccia [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) . Per ulteriori informazioni e per un esempio di implementazione di questa interfaccia, vedere "gestione degli eventi di sessione" in [come riprodurre file multimediali con Media Foundation](how-to-play-unprotected-media-files.md).

Nel ciclo di eventi per ottenere gli eventi della sessione multimediale, attendere l'evento [MESessionTopologyStatus](mesessiontopologystatus.md) generato quando [**IMFMediaSession:: la topologia**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) viene completata e la topologia viene risolta. Quando si recupera l'evento MESessionTopologyStatus, avviare la sessione di codifica chiamando [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start). La sessione multimediale genera l'evento [MEEndOfPresentation](meendofpresentation.md) quando tutte le operazioni di codifica sono completate. Questo evento deve essere gestito per la codifica VBR e viene illustrato nella sezione successiva "aggiornare le proprietà di codifica nel sink di file per la codifica VBR" di questa esercitazione.

La sessione multimediale genera l'oggetto intestazione ASF e finalizza il file al termine della sessione di codifica e quindi genera l'evento [MESessionClosed](mesessionclosed.md) . Questo evento deve essere gestito eseguendo operazioni di arresto appropriate nella sessione multimediale. Per avviare le operazioni di arresto, chiamare [**IMFMediaSession:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown). Dopo la chiusura della sessione di codifica, non è possibile impostare un'altra topologia per la codifica nella stessa istanza di sessione multimediale. Per codificare un altro file, è necessario chiudere e rilasciare la sessione multimediale corrente e impostare la nuova topologia in una sessione multimediale appena creata. Nell'esempio di codice seguente viene creata la sessione multimediale, viene impostata la topologia di codifica e vengono gestiti gli eventi della sessione multimediale.

L'esempio di codice seguente crea la sessione multimediale, imposta la topologia di codifica e controlla la sessione di codifica gestendo gli eventi dalla sessione multimediale.


```C++
//-------------------------------------------------------------------
//  Encode
//  Controls the encoding session and handles events from the media session.
//
//  pTopology:  A pointer to the encoding topology.
//-------------------------------------------------------------------

HRESULT Encode(IMFTopology *pTopology)
{
    if (!pTopology)
    {
        return E_INVALIDARG;
    }
    
    IMFMediaSession *pSession = NULL;
    IMFMediaEvent* pEvent = NULL;
    IMFTopology* pFullTopology = NULL;
    IUnknown* pTopoUnk = NULL;


    MediaEventType meType = MEUnknown;  // Event type

    HRESULT hr = S_OK;
    HRESULT hrStatus = S_OK;            // Event status
                
    MF_TOPOSTATUS TopoStatus = MF_TOPOSTATUS_INVALID; // Used with MESessionTopologyStatus event.    
        

    hr = MFCreateMediaSession(NULL, &pSession);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSession->SetTopology(MFSESSION_SETTOPOLOGY_IMMEDIATE, pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    //Get media session events synchronously
    while (1)
    {
        hr = pSession->GetEvent(0, &pEvent);
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

       switch(meType)
        {
            case MESessionTopologyStatus:
                {
                    // Get the status code.
                    MF_TOPOSTATUS status = (MF_TOPOSTATUS)MFGetAttributeUINT32(
                                             pEvent, MF_EVENT_TOPOLOGY_STATUS, MF_TOPOSTATUS_INVALID);

                    if (status == MF_TOPOSTATUS_READY)
                    {
                        PROPVARIANT var;
                        PropVariantInit(&var);
                        wprintf_s(L"Topology resolved and set on the media session.\n");

                        hr = pSession->Start(NULL, &var);
                        if (FAILED(hr))
                        {
                            goto done;
                        }

                    }
                    if (status == MF_TOPOSTATUS_STARTED_SOURCE)
                    {
                        wprintf_s(L"Encoding started.\n");
                        break;
                    }
                    if (status == MF_TOPOSTATUS_ENDED)
                    {
                        wprintf_s(L"Encoding complete.\n");
                        hr = pSession->Close();
                        if (FAILED(hr))
                        {
                            goto done;
                        }

                        break;
                    }
                }
                break;


            case MESessionEnded:
                wprintf_s(L"Encoding complete.\n");
                hr = pSession->Close();
                if (FAILED(hr))
                {
                    goto done;
                }
                break;

            case MEEndOfPresentation:
                {
                    if (EncodingMode == VBR)
                    {
                        hr = pSession->GetFullTopology(MFSESSION_GETFULLTOPOLOGY_CURRENT, 0, &pFullTopology);
                        if (FAILED(hr))
                        {
                            goto done;
                        }
                        hr = PostEncodingUpdate(pFullTopology);
                        if (FAILED(hr))
                        {
                            goto done;
                        }
                        wprintf_s(L"Updated sinks for VBR. \n");
                    }
                }
                break;

            case MESessionClosed:
                wprintf_s(L"Encoding session closed.\n");

                hr = pSession->Shutdown();
                goto done;
        }
        if (FAILED(hr))
        {
            goto done;
        }

        SafeRelease(&pEvent);

    }
done:
    SafeRelease(&pEvent);
    SafeRelease(&pSession);
    SafeRelease(&pFullTopology);
    SafeRelease(&pTopoUnk);
    return hr;
}
```



## <a name="update-encoding-properties-in-the-file-sink"></a>Aggiornare le proprietà di codifica nel sink di file

Alcune proprietà di codifica, ad esempio la velocità in bit di codifica e i valori accurati dei bucket a perdita, non sono note finché la codifica non è completa, soprattutto per la codifica VBR. Per ottenere i valori corretti, l'applicazione deve attendere l'evento [MEEndOfPresentation](meendofpresentation.md) che indica che la sessione di codifica è stata completata. È necessario aggiornare i valori dei bucket persi nel sink, in modo che l'oggetto intestazione ASF possa riflettere i valori accurati.

Nella procedura riportata di seguito vengono descritti i passaggi necessari per attraversare i nodi nella topologia di codifica per ottenere il nodo sink di file e impostare le proprietà del bucket di perdita richieste.

**Per aggiornare i valori delle proprietà post-codifica nel sink di file ASF**

1.  Chiamare [**IMFTopology:: GetOutputNodeCollection**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-getoutputnodecollection) per ottenere la raccolta di nodi di output dalla topologia di codifica.
2.  Per ogni nodo, ottenere un puntatore al sink del flusso nel nodo chiamando [**IMFTopologyNode:: GetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getobject). Query per l'interfaccia [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) sul puntatore [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) restituito da **IMFTopologyNode:: GetObject**.
3.  Per ogni sink di flusso, ottenere il nodo downstream (codificatore) chiamando [**IMFTopologyNode:: GetInput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getinput).
4.  Eseguire una query sul nodo per ottenere il puntatore [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) dal nodo del codificatore.
5.  Eseguire una query sul codificatore per il puntatore [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) per ottenere l'archivio delle proprietà di codifica dal codificatore.
6.  Eseguire una query sul sink di flusso per il puntatore [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) per ottenere l'archivio delle proprietà del sink di flusso.
7.  Chiamare [**IPropertyStore:: GetValue**](/windows/win32/api/propsys/nn-propsys-ipropertystore) per ottenere i valori di proprietà richiesti dall'archivio delle proprietà del codificatore e copiarli nell'archivio delle proprietà del sink di flusso chiamando **IPropertyStore:: SetValue**.

La tabella seguente mostra i valori delle proprietà post-codifica che devono essere impostati nel sink di flusso per il flusso video.



| Tipo di codifica                                                                                  | Nome proprietà (GetValue)                                                                        | Nome proprietà (SetValue)                                                                                                |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [Codifica della velocità in bit costante](constant-bit-rate-encoding.md)                                   | \_BAVG MFPKEY<br/> \_RAVG MFPKEY<br/>                                                 | MFPKEY \_ Stat \_ BAVG<br/> MFPKEY \_ Stat \_ RAVG<br/>                                                             |
| [Codifica della velocità in bit della variabile basata sulla qualità](quality-based-variable-bit-rate--vbr--encoding.md) | \_BAVG MFPKEY<br/> \_RAVG MFPKEY<br/> \_BMAX MFPKEY<br/> \_Rmax MFPKEY<br/> | MFPKEY \_ Stat \_ BAVG<br/> MFPKEY \_ Stat \_ RAVG<br/> MFPKEY \_ Stat \_ BMAX<br/> MFPKEY \_ Stat \_ Rmax<br/> |



 

Nell'esempio di codice seguente vengono impostati i valori delle proprietà post-codifica.


```C++
//-------------------------------------------------------------------
//  PostEncodingUpdate
//  Updates the file sink with encoding properties set on the encoder
//  during the encoding session.
    //1. Get the output nodes
    //2. For each node, get the downstream node
    //3. For the downstream node, get the MFT
    //4. Get the property store
    //5. Get the required values
    //6. Set them on the stream sink
//
//  pTopology: A pointer to the full topology retrieved from the media session.
//-------------------------------------------------------------------

HRESULT PostEncodingUpdate(IMFTopology *pTopology)
{
    if (!pTopology)
    {
        return E_INVALIDARG;
    }

    HRESULT hr = S_OK;

    IMFCollection* pOutputColl = NULL;
    IUnknown* pNodeUnk = NULL;
    IMFMediaType* pType = NULL;
    IMFTopologyNode* pNode = NULL;
    IUnknown* pSinkUnk = NULL;
    IMFStreamSink* pStreamSink = NULL;
    IMFTopologyNode* pEncoderNode = NULL;
    IUnknown* pEncoderUnk = NULL;
    IMFTransform* pEncoder = NULL;
    IPropertyStore* pStreamSinkProps = NULL;
    IPropertyStore* pEncoderProps = NULL;

    GUID guidMajorType = GUID_NULL;

    PROPVARIANT var;
    PropVariantInit( &var );

    DWORD cElements = 0;

    hr = pTopology->GetOutputNodeCollection( &pOutputColl);
    if (FAILED(hr))
    {
        goto done;
    }


    hr = pOutputColl->GetElementCount(&cElements);
    if (FAILED(hr))
    {
        goto done;
    }


    for(DWORD index = 0; index < cElements; index++)
    {
        hr = pOutputColl->GetElement(index, &pNodeUnk);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pNodeUnk->QueryInterface(IID_IMFTopologyNode, (void**)&pNode);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pNode->GetInputPrefType(0, &pType);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pType->GetMajorType( &guidMajorType );
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pNode->GetObject(&pSinkUnk);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pSinkUnk->QueryInterface(IID_IMFStreamSink, (void**)&pStreamSink);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pNode->GetInput( 0, &pEncoderNode, NULL );
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pEncoderNode->GetObject(&pEncoderUnk);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pEncoderUnk->QueryInterface(IID_IMFTransform, (void**)&pEncoder);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pStreamSink->QueryInterface(IID_IPropertyStore, (void**)&pStreamSinkProps);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pEncoder->QueryInterface(IID_IPropertyStore, (void**)&pEncoderProps);
        if (FAILED(hr))
        {
            goto done;
        }

        if( guidMajorType == MFMediaType_Video )
        {            
            hr = pEncoderProps->GetValue( MFPKEY_BAVG, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_BAVG, var );
            if (FAILED(hr))
            {
                goto done;
            }

            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_RAVG, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_RAVG, var);
            if (FAILED(hr))
            {
                goto done;
            }

            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_BMAX, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_BMAX, var);
            if (FAILED(hr))
            {
                goto done;
            }

            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_RMAX, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_RMAX, var);
            if (FAILED(hr))
            {
                goto done;
            }
        }
        else if( guidMajorType == MFMediaType_Audio )
        {      
            hr = pEncoderProps->GetValue( MFPKEY_STAT_BAVG, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_BAVG, var );
            if (FAILED(hr))
            {
                goto done;
            }
            
            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_STAT_RAVG, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_RAVG, var );
            if (FAILED(hr))
            {
                goto done;
            }
            
            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_STAT_BMAX, &var);
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_BMAX, var);
            if (FAILED(hr))
            {
                goto done;
            }

            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_STAT_RMAX, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_RMAX, var );         
            if (FAILED(hr))
            {
                goto done;
            }

            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_WMAENC_AVGBYTESPERSEC, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_WMAENC_AVGBYTESPERSEC, var );         
            if (FAILED(hr))
            {
                goto done;
            }
        } 
        PropVariantClear( &var ); 
   }
done:
    SafeRelease (&pOutputColl);
    SafeRelease (&pNodeUnk);
    SafeRelease (&pType);
    SafeRelease (&pNode);
    SafeRelease (&pSinkUnk);
    SafeRelease (&pStreamSink);
    SafeRelease (&pEncoderNode);
    SafeRelease (&pEncoderUnk);
    SafeRelease (&pEncoder);
    SafeRelease (&pStreamSinkProps);
    SafeRelease (&pEncoderProps);

    return hr;
   
}
```



## <a name="implement-main"></a>Implementare Main

Nell'esempio di codice seguente viene illustrata la funzione principale dell'applicazione console.


```C++
int wmain(int argc, wchar_t* argv[])
{
    HeapSetInformation(NULL, HeapEnableTerminationOnCorruption, NULL, 0);

    if (argc != 4)
    {
        wprintf_s(L"Usage: %s inputaudio.mp3, %s output.wm*, %Encoding Type: CBR, VBR\n");
        return 0;
    }


    HRESULT             hr = S_OK;

    IMFMediaSource* pSource = NULL;
    IMFTopology* pTopology = NULL;
    IMFActivate* pFileSinkActivate = NULL;

    hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | COINIT_DISABLE_OLE1DDE);
    if (FAILED(hr))
    {
        goto done;
    }

    //Set the requested encoding mode
    if (wcscmp(argv[3], L"CBR")==0)
    {
        EncodingMode = CBR;
    }
    else if (wcscmp(argv[3], L"VBR")==0)
    {
        EncodingMode = VBR;
    }
    else
    {
        EncodingMode = CBR;
    }

    // Start up Media Foundation platform.
    hr = MFStartup(MF_VERSION);
    if (FAILED(hr))
    {
        goto done;
    }

    //Create the media source
    hr = CreateMediaSource(argv[1], &pSource);
    if (FAILED(hr))
    {
        goto done;
    }

    //Create the file sink activate
    hr = CreateMediaSink(argv[2], pSource, &pFileSinkActivate);
    if (FAILED(hr))
    {
        goto done;
    }

    //Build the encoding topology.
    hr = BuildPartialTopology(pSource, pFileSinkActivate, &pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    //Instantiate the media session and start encoding
    hr = Encode(pTopology);
    if (FAILED(hr))
    {
        goto done;
    }


done:
    // Clean up.
    SafeRelease(&pSource);
    SafeRelease(&pTopology);
    SafeRelease(&pFileSinkActivate);

    MFShutdown();
    CoUninitialize();

    if (FAILED(hr))
    {
        wprintf_s(L"Could not create the output file due to 0x%X\n", hr);
    }
    return 0;
}
```



## <a name="test-the-output-file"></a>Testare il file di output

Nell'elenco seguente viene descritto un elenco di controllo per il test del file codificato. Questi valori possono essere controllati nella finestra di dialogo Proprietà file che è possibile visualizzare facendo clic con il pulsante destro del mouse sul file codificato e scegliendo **Proprietà** dal menu di scelta rapida.

-   Il percorso del file codificato è accurato.
-   Le dimensioni del file sono maggiori di zero KB e la durata della riproduzione corrisponde alla durata del file di origine.
-   Per il flusso video, controllare la larghezza del frame e l'altezza, frequenza dei fotogrammi. Questi valori devono corrispondere ai valori specificati nel profilo ASF creato nel passaggio descritto nella sezione "creare l'oggetto profilo ASF".
-   Per il flusso audio, la velocità in bit deve essere vicina al valore specificato nel tipo di supporto di destinazione.
-   Aprire il file in Windows Media Player e verificare la qualità della codifica.
-   Aprire il file ASF in ASFViewer per visualizzare la struttura di un file ASF. Questo strumento può essere scaricato da questo [sito Web Microsoft](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea).

## <a name="common-error-codes-and-debugging-tips"></a>Codici di errore comuni e suggerimenti per il debug

Nell'elenco seguente vengono descritti i codici di errore comuni che potrebbero essere ricevuti e i suggerimenti per il debug.

-   La chiamata a [**IMFSourceResolver:: CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) blocca l'applicazione.

    Assicurarsi di aver inizializzato la piattaforma di Media Foundation chiamando [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup). Questa funzione imposta la piattaforma asincrona usata da tutti i metodi che avviano operazioni asincrone, ad esempio [**IMFSourceResolver:: CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl), internamente.

-   [**IMFSourceResolver:: CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) restituisce HRESULT 0x80070002 "Impossibile trovare il file specificato.

    Verificare che il nome del file di input specificato dall'utente nel primo argomento esista.

-   HRESULT 0x80070020 "il processo non può accedere al file perché è in uso da un altro processo. "

    Assicurarsi che i file di input e di output non siano attualmente in uso da un'altra risorsa nel sistema.

-   Le chiamate ai metodi [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) restituiscono MF \_ E \_ INVALIDMEDIATYPE.

    Verificare che siano soddisfatte le condizioni seguenti:

    -   Il tipo di input o il tipo di output specificato è compatibile con i tipi di supporto supportati dal codificatore.
    -   I tipi di supporto specificati sono completi. Per completare i tipi di supporto, vedere gli attributi obbligatori nella sezione "creare un tipo di supporto audio compresso" e "creare un tipo di supporto video compresso" di questa esercitazione.
    -   Assicurarsi di aver impostato la velocità in bit di destinazione per il tipo di supporto parziale a cui si aggiungono i dati privati del codec.

-   La sessione multimediale restituisce \_ \_ \_ il tipo D3D non supportato \_ nello stato dell'evento.

    Questo errore viene restituito quando il tipo di supporto dell'origine indica una modalità mista a interlacciamento non supportata dal codificatore Windows Media Video. Se il tipo di supporto video compresso è impostato per usare la modalità progressiva, la pipeline deve usare una trasformazione di deinterlacciamento. Poiché la pipeline non è in grado di trovare una corrispondenza (indicata dal codice di errore), è necessario inserire manualmente un decodificatore (transcodificatore video) tra i nodi del codificatore e del codificatore.

-   La sessione multimediale restituisce E \_ INVALIDARG nello stato dell'evento.

    Questo errore viene restituito quando gli attributi del tipo di supporto di origine non sono compatibili con gli attributi del tipo di supporto di output impostato nel codificatore Windows Media.

-   [**IWMCodecPrivateData:: GetPrivateData**](../wmformat/iwmcodecprivatedata-getprivatedata.md) restituisce HRESULT 0x80040203 "si è verificato un errore di sintassi durante il tentativo di valutare una stringa di query"

    Verificare che il tipo di input sia impostato sul codificatore MFT.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Componenti ASF a livello pipeline](pipeline-layer-asf-components.md)
</dt> </dl>

 

 
