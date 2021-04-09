---
description: In questa esercitazione viene illustrato come scrivere un nuovo file audio (WMA) estraendo contenuto multimediale da un file audio non compresso (WAV) e quindi comprimerlo in formato ASF.
ms.assetid: f310c6ed-52e7-4828-9d4c-2f7ced9080c5
title: 'Esercitazione: scrittura di un file WMA usando oggetti WMContainer'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d156b75ced6cde2953ec90362ed13b0cc53bb83c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880581"
---
# <a name="tutorial-writing-a-wma-file-by-using-wmcontainer-objects"></a>Esercitazione: scrittura di un file WMA usando oggetti WMContainer

In questa esercitazione viene illustrato come scrivere un nuovo file audio (WMA) estraendo contenuto multimediale da un file audio non compresso (WAV) e quindi comprimerlo in formato ASF. La modalità di codifica utilizzata per la conversione è la [codifica della velocità in bit costante](constant-bit-rate-encoding.md) (CBR). In questa modalità, prima della sessione di codifica, l'applicazione specifica una velocità in bit di destinazione che il codificatore deve raggiungere.

In questa esercitazione verrà creata un'applicazione console che accetta i nomi dei file di input e di output come argomenti. L'applicazione ottiene gli esempi di supporti non compressi da un'applicazione di analisi di file Wave, fornita con questa esercitazione. Questi esempi vengono inviati al codificatore per la conversione nel formato Windows Media Audio 9. Il codificatore è configurato per la codifica CBR e usa la velocità del primo bit disponibile durante la negoziazione del tipo di supporto come velocità in bit di destinazione. Gli esempi codificati vengono inviati al multiplexer per la pacchettizzazione nel formato dati ASF. Questi pacchetti verranno scritti in un flusso di byte che rappresenta l'oggetto dati ASF. Quando la sezione dati è pronta, si creerà un file audio ASF e si scriverà il nuovo oggetto intestazione ASF che consolida tutte le informazioni di intestazione e quindi aggiungerà il flusso di byte dell'oggetto dati ASF.

Questa esercitazione contiene le sezioni seguenti:

-   [Prerequisiti](#prerequisites)
-   [Terminologia](#terminology)
-   [1. configurare il progetto](#1-set-up-the-project)
-   [2. dichiarare le funzioni helper](#2-declare-helper-functions)
-   [3. aprire un file audio](#3-open-an-audio-file)
-   [4. configurare il codificatore](#4-configure-the-encoder)
-   [5. creare l'oggetto ContentInfo ASF.](#5-create-the-asf-contentinfo-object)
-   [6. creare il multiplexer ASF](#6-create-the-asf-multiplexer)
-   [7. generare nuovi pacchetti di dati ASF](#7-generate-new-asf-data-packets)
-   [8. scrivere il file ASF](#8-write-the-asf-file)
-   [9. definire la funzione Entry-Point](#9-define-the-entry-point-function)
-   [Argomenti correlati](#related-topics)

## <a name="prerequisites"></a>Prerequisiti

Nell’esercitazione si presuppongono le condizioni seguenti:

-   Si ha familiarità con la struttura di un file ASF e i componenti forniti da Media Foundation per lavorare con gli oggetti ASF. Questi componenti includono oggetti ContentInfo, Splitter, multiplexer e profile. Per altre informazioni, vedere [WMCONTAINER ASF Components](wmcontainer-asf-components.md).
-   Si ha familiarità con i codificatori Windows Media e con i vari tipi di codifica, in particolare CBR. Per ulteriori informazioni, vedere [codificatori Windows Media](windows-media-encoders.md) .
-   Si ha familiarità con i [buffer multimediali](media-buffers.md) e i flussi di byte: in particolare, le operazioni sui file che usano un flusso di byte e la scrittura del contenuto di un buffer multimediale in un flusso di byte.

## <a name="terminology"></a>Terminologia

Questa esercitazione usa i termini seguenti:

-   Tipo di supporto di origine: oggetto tipo di supporto, espone l'interfaccia [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) , che descrive il contenuto del file di input.
-   Profilo audio: oggetto profilo, espone l'interfaccia [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) , che contiene solo flussi audio del file di output.
-   Esempio di flusso: supporto di esempio, espone l'interfaccia [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) , che rappresenta i dati multimediali del file di input ottenuti dal codificatore in uno stato compresso.
-   Oggetto ContentInfo: [oggetto ContentInfo ASF](asf-contentinfo-object.md), espone l'interfaccia [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) , che rappresenta l'oggetto intestazione ASF del file di output.
-   Data byte stream: oggetto flusso di byte, espone l'interfaccia [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) , che rappresenta l'intera parte dell'oggetto dati ASF del file di output.
-   Pacchetto di dati: esempio di supporto, espone l'interfaccia [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) , generata da [ASF Multiplexer](asf-multiplexer.md); rappresenta un pacchetto di dati ASF che verrà scritto nel flusso di byte di dati.
-   Flusso di byte di output: oggetto flusso di byte, espone l'interfaccia [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) , che contiene il contenuto del file di output.

## <a name="1-set-up-the-project"></a>1. configurare il progetto

1.  Includere le intestazioni seguenti nel file di origine:

    ```C++
    #include <new>
    #include <stdio.h>       // Standard I/O
    #include <windows.h>     // Windows headers
    #include <mfapi.h>       // Media Foundation platform
    #include <wmcontainer.h> // ASF interfaces
    #include <mferror.h>     // Media Foundation error codes
    ```

    

2.  Collegamento ai file di libreria seguenti:

    -   mfplat. lib
    -   MF. lib
    -   mfuuid. lib

3.  Dichiarare la funzione [SafeRelease](saferelease.md) .
4.  Includere la classe CWmaEncoder nel progetto. Per il codice sorgente completo di questa classe, vedere [codice di esempio del codificatore](encoder-example-code.md).

## <a name="2-declare-helper-functions"></a>2. dichiarare le funzioni helper

Questa esercitazione usa le funzioni di supporto seguenti per leggere e scrivere da un flusso di byte.

-   `AppendToByteStream`: Accoda il contenuto di un flusso di byte a un altro flusso di byte.
-   WriteBufferToByteStream: scrive i dati da un buffer multimediale a un flusso di byte.

Per ulteriori informazioni, vedere [**IMFByteStream:: Write**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-write). Il codice seguente illustra le funzioni di supporto seguenti:


```C++
//-------------------------------------------------------------------
// AppendToByteStream
//
// Reads the contents of pSrc and writes them to pDest.
//-------------------------------------------------------------------

HRESULT AppendToByteStream(IMFByteStream *pSrc, IMFByteStream *pDest)
{
    HRESULT hr = S_OK;

    const DWORD READ_SIZE = 1024;

    BYTE buffer[READ_SIZE];

    while (1)
    {
        ULONG cbRead;

        hr = pSrc->Read(buffer, READ_SIZE, &cbRead);

        if (FAILED(hr)) { break; }

        if (cbRead == 0)
        {
            break;
        }

        hr = pDest->Write(buffer, cbRead, &cbRead);

        if (FAILED(hr)) { break; }
    }

    return hr;
}
```




```C++
//-------------------------------------------------------------------
// WriteBufferToByteStream
//
// Writes data from a media buffer to a byte stream.
//-------------------------------------------------------------------

HRESULT WriteBufferToByteStream(
    IMFByteStream *pStream,   // Pointer to the byte stream.
    IMFMediaBuffer *pBuffer,  // Pointer to the media buffer.
    DWORD *pcbWritten         // Receives the number of bytes written.
    )
{
    HRESULT hr = S_OK;
    DWORD cbData = 0;
    DWORD cbWritten = 0;
    BYTE *pMem = NULL;

    hr = pBuffer->Lock(&pMem, NULL, &cbData);

    if (SUCCEEDED(hr))
    {
        hr = pStream->Write(pMem, cbData, &cbWritten);
    }

    if (SUCCEEDED(hr))
    {
        if (pcbWritten)
        {
            *pcbWritten = cbWritten;
        }
    }

    if (pMem)
    {
        pBuffer->Unlock();
    }
    return hr;
}
```



## <a name="3-open-an-audio-file"></a>3. aprire un file audio

In questa esercitazione si presuppone che l'applicazione generi audio non compresso per la codifica. A tale scopo, in questa esercitazione vengono dichiarate due funzioni:


```C++
HRESULT OpenAudioFile(PCWSTR pszURL, IMFMediaType **ppAudioFormat);
HRESULT GetNextAudioSample(BOOL *pbEOS, IMFSample **ppSample);
```



L'implementazione di queste funzioni viene lasciata al lettore.

-   La `OpenAudioFile` funzione deve aprire il file multimediale specificato da *pszURL* e restituire un puntatore a un tipo di supporto che descrive un flusso audio.
-   La `GetNextAudioSample` funzione deve leggere l'audio PCM non compresso dal file aperto da `OpenAudioFile` . Quando viene raggiunta la fine del file, *pbEOS* riceve il valore **true**. In caso contrario, *ppSample* riceve un esempio multimediale che contiene il buffer audio.

## <a name="4-configure-the-encoder"></a>4. configurare il codificatore

Successivamente, creare il codificatore, configurarlo per produrre esempi di flusso con codifica CBR e negoziare i tipi di supporto di input e di output.

In Media Foundation i codificatori (esporre l'interfaccia [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) ) vengono implementati come [Media Foundation Transforms](media-foundation-transforms.md) (MFT).

In questa esercitazione il codificatore viene implementato nella `CWmaEncoder` classe che fornisce un wrapper per il MFT. Per il codice sorgente completo di questa classe, vedere [codice di esempio del codificatore](encoder-example-code.md).

> [!Note]  
> Facoltativamente, è possibile specificare il tipo di codifica come CBR. Per impostazione predefinita, il codificatore è configurato per usare la codifica CBR. Per altre informazioni, vedere [codifica della velocità in bit costante](constant-bit-rate-encoding.md). È possibile impostare proprietà aggiuntive a seconda del tipo di codifica. per informazioni sulle proprietà specifiche di una modalità di codifica, vedere [codifica della velocità in bit variabile basata sulla qualità](quality-based-variable-bit-rate--vbr--encoding.md), codifica della velocità in bit variabile non [vincolata](unconstrained-variable-bit-rate--vbr--encoding.md)e [codifica della velocità in bit a variabili](peak-constrained-variable-bit-rate--vbr--encoding.md)vincolate di picco.

 


```C++
    CWmaEncoder* pEncoder = NULL; //Pointer to the Encoder object.

    hr = OpenAudioFile(sInputFileName, &pInputType);
    if (FAILED(hr))
    {
        goto done;
    }

    // Initialize the WMA encoder wrapper.

    pEncoder = new (std::nothrow) CWmaEncoder();
    if (pEncoder == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto done;
    }

    hr = pEncoder->Initialize();
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pEncoder->SetEncodingType(EncodeMode_CBR);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pEncoder->SetInputType(pInputType);
    if (FAILED(hr))
    {
        goto done;
    }
```



## <a name="5-create-the-asf-contentinfo-object"></a>5. creare l'oggetto ContentInfo ASF.

L' [oggetto ContentInfo ASF](asf-contentinfo-object.md) contiene informazioni sui vari oggetti Header del file di output.

Per prima cosa, creare un profilo ASF per il flusso audio:

1.  Chiamare [**MFCreateASFProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile) per creare un oggetto profilo ASF vuoto. Il profilo ASF espone l'interfaccia [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) . Per ulteriori informazioni, vedere [creazione e configurazione di flussi ASF](creating-and-configuring-asf-streams.md).
2.  Ottenere il formato audio codificato dall' `CWmaEncoder` oggetto.
3.  Chiamare [**IMFASFProfile:: CreateStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstream) per creare un nuovo flusso per il profilo ASF. Passare un puntatore all'interfaccia [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) , che rappresenta il formato del flusso.
4.  Chiamare [**IMFASFStreamConfig:: SetStreamNumber**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-setstreamnumber) per assegnare un identificatore di flusso.
5.  Impostare i parametri "leaky bucket" impostando l'attributo [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) nell'oggetto flusso.
6.  Chiamare [**IMFASFProfile:: sestream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream) per aggiungere il nuovo flusso al profilo.

A questo punto, creare l'oggetto ContentInfo ASF come segue:

1.  Chiamare [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) per creare un oggetto ContentInfo vuoto.
2.  Chiamare [**IMFASFContentInfo:: seprofile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) per impostare il profilo ASF.

Il codice seguente illustra questi passaggi:


```C++
HRESULT CreateASFContentInfo(
    CWmaEncoder* pEncoder,
    IMFASFContentInfo** ppContentInfo
    )
{
    HRESULT hr = S_OK;
    
    IMFASFProfile* pProfile = NULL;
    IMFMediaType* pMediaType = NULL;
    IMFASFStreamConfig* pStream = NULL;
    IMFASFContentInfo* pContentInfo = NULL;

    // Create the ASF profile object.

    hr = MFCreateASFProfile(&pProfile); 
    if (FAILED(hr))
    {
        goto done;
    }

    // Create a stream description for the encoded audio.

    hr = pEncoder->GetOutputType(&pMediaType); 
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pProfile->CreateStream(pMediaType, &pStream); 
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pStream->SetStreamNumber(DEFAULT_STREAM_NUMBER); 
    if (FAILED(hr))
    {
        goto done;
    }

    // Set "leaky bucket" values.

    LeakyBucket bucket;

    hr = pEncoder->GetLeakyBucket1(&bucket);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pStream->SetBlob(
        MF_ASFSTREAMCONFIG_LEAKYBUCKET1, 
        (UINT8*)&bucket, 
        sizeof(bucket)
        );

    if (FAILED(hr))
    {
        goto done;
    }

    //Add the stream to the profile

    hr = pProfile->SetStream(pStream);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the ASF ContentInfo object.

    hr = MFCreateASFContentInfo(&pContentInfo); 
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pContentInfo->SetProfile(pProfile); 
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the pointer to the caller.

    *ppContentInfo = pContentInfo;
    (*ppContentInfo)->AddRef();

done:
    SafeRelease(&pProfile);
    SafeRelease(&pStream);
    SafeRelease(&pMediaType);
    SafeRelease(&pContentInfo);
    return hr;
}
```



## <a name="6-create-the-asf-multiplexer"></a>6. creare il multiplexer ASF

Il [multiplexer ASF](asf-multiplexer.md) genera pacchetti di dati ASF.

1.  Chiamare [**MFCreateASFMultiplexer**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmultiplexer) per creare il multiplexing ASF.
2.  Chiamare [**IMFASFMultiplexer:: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) per inizializzare il multiplexer. Passare un puntatore all'oggetto informazioni sul contenuto ASF, che è stato creato nella sezione precedente.
3.  Chiamare [**IMFASFMultiplexer:: Seflags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-setflags) per impostare il flag **MFASF \_ multiplexer \_ AutoAdjust \_ bitrate** . Quando si usa questa impostazione, il multiplexer regola automaticamente la velocità in bit del contenuto ASF in modo che corrisponda alle caratteristiche dei flussi sottoposto a multiplexing.


```C++
HRESULT CreateASFMux( 
    IMFASFContentInfo* pContentInfo,
    IMFASFMultiplexer** ppMultiplexer
    )
{
    HRESULT hr = S_OK;
    
    IMFMediaType* pMediaType = NULL;
    IMFASFMultiplexer *pMultiplexer = NULL;

    // Create and initialize the ASF Multiplexer object.

    hr = MFCreateASFMultiplexer(&pMultiplexer);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pMultiplexer->Initialize(pContentInfo);
    if (FAILED(hr))
    {
        goto done;
    }

    // Enable automatic bit-rate adjustment.

    hr = pMultiplexer->SetFlags(MFASF_MULTIPLEXER_AUTOADJUST_BITRATE);
    if (FAILED(hr))
    {
        goto done;
    }

    *ppMultiplexer = pMultiplexer;
    (*ppMultiplexer)->AddRef();

done:
    SafeRelease(&pMultiplexer);
    return hr;
}
```



## <a name="7-generate-new-asf-data-packets"></a>7. generare nuovi pacchetti di dati ASF

Generare quindi i pacchetti di dati ASF per il nuovo file. Questi pacchetti di dati costituiranno l'oggetto dati ASF finale per il nuovo file. Per generare nuovi pacchetti di dati ASF:

1.  Chiamare [**MFCreateTempFile**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatetempfile) per creare un flusso di byte temporaneo che contenga i pacchetti di dati ASF.
2.  Chiamare la funzione definita dall'applicazione `GetNextAudioSample` per ottenere i dati audio non compressi per il codificatore.
3.  Passare l'audio non compresso al codificatore per la compressione. Per altre informazioni, vedere [elaborazione dei dati nel codificatore](processing-data-in-the-encoder.md)
4.  Chiamare [**IMFASFMultiplexer::P rocesssample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) per inviare i campioni audio compressi al multiplexer ASF per la pacchettizzazione.
5.  Ottenere i pacchetti ASF dal multiplexer e scriverli nel flusso di byte temporaneo. Per ulteriori informazioni, vedere [generazione di nuovi pacchetti di dati ASF](generating-new-asf-data-packets.md).
6.  Quando si raggiunge la fine del flusso di origine, svuotare il codificatore ed estrarre gli esempi compressi rimanenti dal codificatore. Per altre informazioni sullo svuotamento di un MFT, vedere [modello di elaborazione MFT di base](basic-mft-processing-model.md).
7.  Dopo che tutti i campioni sono stati inviati al multiplexer, chiamare [**IMFASFMultiplexer:: Flush**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-flush) ed estrarre i pacchetti ASF rimanenti dal multiplexer.
8.  Chiamare [**IMFASFMultiplexer:: end**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-end).

Il codice seguente genera pacchetti di dati ASF. La funzione restituisce un puntatore a un flusso di byte che contiene l'oggetto dati ASF.


```C++
HRESULT EncodeData(
    CWmaEncoder* pEncoder, 
    IMFASFContentInfo* pContentInfo,
    IMFASFMultiplexer* pMux, 
    IMFByteStream** ppDataStream) 
{
    HRESULT hr = S_OK;

    IMFByteStream* pStream = NULL;
    IMFSample* pInputSample = NULL;
    IMFSample* pWmaSample = NULL;

    BOOL bEOF = FALSE;

   // Create a temporary file to hold the data stream.
   hr = MFCreateTempFile(
        MF_ACCESSMODE_READWRITE, 
        MF_OPENMODE_DELETE_IF_EXIST,
        MF_FILEFLAGS_NONE,
        &pStream
        );

   if (FAILED(hr))
   {
       goto done;
   }

    BOOL bNeedInput = TRUE;

    while (TRUE)
    {
        if (bNeedInput)
        {
            hr = GetNextAudioSample(&bEOF, &pInputSample);
            if (FAILED(hr))
            {
                goto done;
            }

            if (bEOF)
            {
                // Reached the end of the input file.
                break;
            }

            // Encode the uncompressed audio sample.
            hr = pEncoder->ProcessInput(pInputSample);
            if (FAILED(hr))
            {
                goto done;
            }

            bNeedInput = FALSE;
        }

        if (bNeedInput == FALSE)
        {
            // Get data from the encoder.

            hr = pEncoder->ProcessOutput(&pWmaSample);
            if (FAILED(hr))
            {
                goto done;
            }

            // pWmaSample can be NULL if the encoder needs more input.

            if (pWmaSample)
            {
                hr = pMux->ProcessSample(DEFAULT_STREAM_NUMBER, pWmaSample, 0);
                if (FAILED(hr))
                {
                    goto done;
                }

                //Collect the data packets and write them to a stream
                hr = GenerateASFDataPackets(pMux, pStream);
                if (FAILED(hr))
                {
                    goto done;
                }
            }
            else
            {
                bNeedInput = TRUE;
            }
        }
        
        SafeRelease(&pInputSample);
        SafeRelease(&pWmaSample);
    }

    // Drain the MFT and pull any remaining samples from the encoder.

    hr = pEncoder->Drain();
    if (FAILED(hr))
    {
        goto done;
    }

    while (TRUE)
    {
        hr = pEncoder->ProcessOutput(&pWmaSample);
        if (FAILED(hr))
        {
            goto done;
        }

        if (pWmaSample == NULL)
        {
            break;
        }

        hr = pMux->ProcessSample(DEFAULT_STREAM_NUMBER, pWmaSample, 0);
        if (FAILED(hr))
        {
            goto done;
        }

        //Collect the data packets and write them to a stream
        hr = GenerateASFDataPackets(pMux, pStream);
        if (FAILED(hr))
        {
            goto done;
        }

        SafeRelease(&pWmaSample);
    }

    // Flush the mux and get any pending ASF data packets.
    hr = pMux->Flush();
    if (FAILED(hr))
    {
        goto done;
    }

    hr = GenerateASFDataPackets(pMux, pStream);
    if (FAILED(hr))
    {
        goto done;
    }
    
    // Update the ContentInfo object
    hr = pMux->End(pContentInfo);
    if (FAILED(hr))
    {
        goto done;
    }

    //Return stream to the caller that contains the ASF encoded data.
    *ppDataStream = pStream;
    (*ppDataStream)->AddRef();

done:
    SafeRelease(&pStream);
    SafeRelease(&pInputSample);
    SafeRelease(&pWmaSample);
    return hr;
}
```



Il codice per la `GenerateASFDataPackets` funzione è illustrato nell'argomento [generazione di nuovi pacchetti di dati ASF](generating-new-asf-data-packets.md).

## <a name="8-write-the-asf-file"></a>8. scrivere il file ASF

Quindi, scrivere l'intestazione ASF in un buffer multimediale chiamando [**IMFASFContentInfo:: GenerateHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader). Questo metodo converte i dati archiviati nell'oggetto ContentInfo in dati binari nel formato dell'oggetto intestazione ASF. Per ulteriori informazioni, vedere [generazione di un nuovo oggetto intestazione ASF](generating-a-new-asf-header-object.md).

Dopo la generazione del nuovo oggetto intestazione ASF, creare un flusso di byte per il file di output. Prima di tutto, scrivere l'oggetto Header nel flusso di byte di output. Seguire l'oggetto Header con l'oggetto dati contenuto nel flusso di byte di dati.


```C++
HRESULT WriteASFFile( 
     IMFASFContentInfo *pContentInfo, 
     IMFByteStream *pDataStream,
     PCWSTR pszFile
     )
{
    HRESULT hr = S_OK;
    
    IMFMediaBuffer* pHeaderBuffer = NULL;
    IMFByteStream* pWmaStream = NULL;

    DWORD cbHeaderSize = 0;
    DWORD cbWritten = 0;

    //Create output file
    hr = MFCreateFile(MF_ACCESSMODE_WRITE, MF_OPENMODE_DELETE_IF_EXIST,
        MF_FILEFLAGS_NONE, pszFile, &pWmaStream);

    if (FAILED(hr))
    {
        goto done;
    }


    // Get the size of the ASF Header Object.
    hr = pContentInfo->GenerateHeader (NULL, &cbHeaderSize);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create a media buffer.
    hr = MFCreateMemoryBuffer(cbHeaderSize, &pHeaderBuffer);
    if (FAILED(hr))
    {
        goto done;
    }

    // Populate the media buffer with the ASF Header Object.
    hr = pContentInfo->GenerateHeader(pHeaderBuffer, &cbHeaderSize);
    if (FAILED(hr))
    {
        goto done;
    }

    // Write the ASF header to the output file.
    hr = WriteBufferToByteStream(pWmaStream, pHeaderBuffer, &cbWritten);
    if (FAILED(hr))
    {
        goto done;
    }

    // Append the data stream to the file.

    hr = pDataStream->SetCurrentPosition(0);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = AppendToByteStream(pDataStream, pWmaStream);

done:
    SafeRelease(&pHeaderBuffer);
    SafeRelease(&pWmaStream);
    return hr;
}
```



## <a name="9-define-the-entry-point-function"></a>9. definire la funzione Entry-Point

È ora possibile inserire i passaggi precedenti in un'applicazione completa. Prima di usare uno degli oggetti Media Foundation, inizializzare la piattaforma Media Foundation chiamando [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup). Al termine, chiamare [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown). Per ulteriori informazioni, vedere [inizializzazione di Media Foundation](initializing-media-foundation.md).

Nel codice seguente viene illustrata l'applicazione console completa. L'argomento della riga di comando specifica il nome del file da convertire e il nome del nuovo file audio.


```C++
int wmain(int argc, WCHAR* argv[])
{
    HeapSetInformation(NULL, HeapEnableTerminationOnCorruption, NULL, 0);

    if (argc != 3)
    {
        wprintf_s(L"Usage: %s input.wmv, %s output.wma");
        return 0;
    }

    const WCHAR* sInputFileName = argv[1];    // Source file name
    const WCHAR* sOutputFileName = argv[2];  // Output file name
    
    IMFMediaType* pInputType = NULL;
    IMFASFContentInfo* pContentInfo = NULL;
    IMFASFMultiplexer* pMux = NULL;
    IMFByteStream* pDataStream = NULL;

    CWmaEncoder* pEncoder = NULL; //Pointer to the Encoder object.

    HRESULT hr = CoInitializeEx(
        NULL, COINIT_APARTMENTTHREADED | COINIT_DISABLE_OLE1DDE);

    if (FAILED(hr))
    {
        goto done;
    }

    hr = MFStartup(MF_VERSION);
    if (FAILED(hr))
    {
        goto done;
    }

    CWmaEncoder* pEncoder = NULL; //Pointer to the Encoder object.

    hr = OpenAudioFile(sInputFileName, &pInputType);
    if (FAILED(hr))
    {
        goto done;
    }

    // Initialize the WMA encoder wrapper.

    pEncoder = new (std::nothrow) CWmaEncoder();
    if (pEncoder == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto done;
    }

    hr = pEncoder->Initialize();
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pEncoder->SetEncodingType(EncodeMode_CBR);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pEncoder->SetInputType(pInputType);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the WMContainer objects.
    hr = CreateASFContentInfo(pEncoder, &pContentInfo);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = CreateASFMux(pContentInfo, &pMux);
    if (FAILED(hr))
    {
        goto done;
    }

    // Convert uncompressed data to ASF format.
    hr = EncodeData(pEncoder, pContentInfo, pMux, &pDataStream);
    if (FAILED(hr))
    {
        goto done;
    }

    // Write the ASF objects to the output file.
    hr = WriteASFFile(pContentInfo, pDataStream, sOutputFileName);

done:
    SafeRelease(&pInputType);
    SafeRelease(&pContentInfo);
    SafeRelease(&pMux);
    SafeRelease(&pDataStream);
    delete pEncoder;

    MFShutdown();
    CoUninitialize();

    if (FAILED(hr))
    {
        wprintf_s(L"Error: 0x%X\n", hr);
    }

    return 0;
} 
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Componenti ASF WMContainer](wmcontainer-asf-components.md)
</dt> <dt>

[Supporto ASF in Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



