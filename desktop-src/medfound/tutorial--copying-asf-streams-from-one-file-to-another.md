---
description: Un modo per creare un file ASF consiste nel copiare i flussi ASF da un file esistente.
ms.assetid: 158fe3a1-42e6-461d-b56b-5419cd961fca
title: 'Esercitazione: copia di flussi ASF usando oggetti WMContainer'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44bac13626a8c80f474eeb029db4eb1351273910
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310190"
---
# <a name="tutorial-copying-asf-streams-by-using-wmcontainer-objects"></a>Esercitazione: copia di flussi ASF usando oggetti WMContainer

Un modo per creare un file ASF consiste nel copiare i flussi ASF da un file esistente. A tale scopo, è possibile recuperare i dati multimediali dal file di origine e scrivere nel file di output. Se il file di origine è un file ASF, è possibile copiare gli esempi di flusso senza decomprimerli e ricomprimerli.

Questa esercitazione illustra questo scenario estraendo il primo flusso audio da un file audio-video ASF (con estensione WMV) e copiando il file in un nuovo file audio ASF (WMA). In questa esercitazione verrà creata un'applicazione console che accetta i nomi dei file di input e di output come argomenti. L'applicazione usa la barra di divisione ASF per analizzare gli esempi di flusso di input e quindi li invia al multiplexer ASF per scrivere i pacchetti di dati ASF per il flusso audio.

Questa esercitazione include i passaggi seguenti:

-   [Prerequisiti](#prerequisites)
-   [Terminologia](#terminology)
-   [1. configurare il progetto](#1-set-up-the-project)
-   [2. dichiarare le funzioni helper](#2-declare-helper-functions)
-   [3. Aprire il file ASF di input](#3-open-the-input-asf-file)
-   [4. inizializzare gli oggetti per il file di input](#4-initialize-objects-for-the-input-file)
-   [5. creare un profilo audio](#5-create-an-audio-profile)
-   [6. inizializzare gli oggetti per il file di output](#6-initialize-objects-for-the-output-file)
-   [7. generare nuovi pacchetti di dati ASF](#7-generate-new-asf-data-packets)
-   [8. scrivere gli oggetti ASF nel nuovo file](#8-write-the-asf-objects-in-the-new-file)
-   [9 scrivere la funzione Entry-Point](#9-write-the-entry-point-function)
-   [Argomenti correlati](#related-topics)

## <a name="prerequisites"></a>Prerequisiti

Nell’esercitazione si presuppongono le condizioni seguenti:

-   Si ha familiarità con la struttura di un file ASF e i componenti forniti da Media Foundation per lavorare con gli oggetti ASF. Questi componenti includono oggetti ContentInfo, Splitter, multiplexer e profile. Per altre informazioni, vedere [WMCONTAINER ASF Components](wmcontainer-asf-components.md).
-   Si ha familiarità con il processo di analisi dell'oggetto intestazione ASF e dei pacchetti di dati ASF di un file esistente e di generazione di esempi di flussi compressi tramite la barra di divisione. Per ulteriori informazioni [, vedere Esercitazione: lettura di un file ASF](tutorial--reading-an-asf-file.md).
-   Si ha familiarità con i buffer multimediali e i flussi di byte: in particolare, le operazioni sui file che usano un flusso di byte e la scrittura del contenuto di un buffer multimediale in un flusso di byte. (Vedere [2. Dichiarare le funzioni di supporto](#2-declare-helper-functions).

## <a name="terminology"></a>Terminologia

Questa esercitazione usa i termini seguenti:

-   Flusso di byte di origine: oggetto flusso di byte, espone l'interfaccia [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) , che contiene il contenuto del file di input.
-   Oggetto ContentInfo di origine: oggetto ContentInfo, espone l'interfaccia [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) , che rappresenta l'oggetto intestazione ASF del file di input.
-   Profilo audio: oggetto profilo, espone l'interfaccia [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) , che contiene solo flussi audio del file di input.
-   Esempio di flusso: supporto di esempio, espone l'interfaccia [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) , generata dalla barra di divisione che rappresenta i dati multimediali del flusso selezionato ottenuti dal file di input in stato compresso.
-   Output oggetto ContentInfo: oggetto ContentInfo, espone l'interfaccia [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) , che rappresenta l'oggetto intestazione ASF del file di output.
-   Data byte stream: oggetto flusso di byte, espone l'interfaccia [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) , che rappresenta l'intera parte dell'oggetto dati ASF del file di output.
-   Pacchetto dati: l'esempio di supporto espone l'interfaccia [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) , generata dal multiplexer, che rappresenta un pacchetto di dati ASF che verrà scritto nel flusso di byte dei dati.
-   Flusso di byte di output: oggetto flusso di byte, espone l'interfaccia [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) , che contiene il contenuto del file di output.

## <a name="1-set-up-the-project"></a>1. configurare il progetto

Includere le intestazioni seguenti nel file di origine:


```C++
#include <stdio.h>       // Standard I/O
#include <windows.h>     // Windows headers
#include <mfapi.h>       // Media Foundation platform
#include <wmcontainer.h> // ASF interfaces
#include <mferror.h>     // Media Foundation error codes
```



Collegamento ai file di libreria seguenti:

-   mfplat. lib
-   MF. lib
-   mfuuid. lib

Dichiarare la funzione [SafeRelease](saferelease.md) :


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



## <a name="2-declare-helper-functions"></a>2. dichiarare le funzioni helper

Questa esercitazione usa le funzioni di supporto seguenti per leggere e scrivere da un flusso di byte.

La `AllocReadFromByteStream` funzione legge i dati da un flusso di byte e alloca un nuovo buffer multimediale per conservare i dati. Per ulteriori informazioni, vedere [**IMFByteStream:: Read**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-read).


```C++
//-------------------------------------------------------------------
// AllocReadFromByteStream
//
// Reads data from a byte stream and returns a media buffer that
// contains the data.
//-------------------------------------------------------------------

HRESULT AllocReadFromByteStream(
    IMFByteStream *pStream,         // Pointer to the byte stream.
    DWORD cbToRead,                 // Number of bytes to read.
    IMFMediaBuffer **ppBuffer       // Receives a pointer to the media buffer. 
    )
{
    HRESULT hr = S_OK;
    BYTE *pData = NULL;
    DWORD cbRead = 0;   // Actual amount of data read.

    IMFMediaBuffer *pBuffer = NULL;

    // Create the media buffer. 
    // This function allocates the memory for the buffer.
    hr = MFCreateMemoryBuffer(cbToRead, &pBuffer);

    // Get a pointer to the memory buffer.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->Lock(&pData, NULL, NULL);
    }

    // Read the data from the byte stream.
    if (SUCCEEDED(hr))
    {
        hr = pStream->Read(pData, cbToRead, &cbRead);
    }

    // Update the size of the valid data in the buffer.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->SetCurrentLength(cbRead);
    }

    // Return the pointer to the caller.
    if (SUCCEEDED(hr))
    {
        *ppBuffer = pBuffer;
        (*ppBuffer)->AddRef();
    }

    if (pData)
    {
        pBuffer->Unlock();
    }
    SafeRelease(&pBuffer);
    return hr;
}
```



La `WriteBufferToByteStream` funzione scrive i dati da un buffer multimediale a un flusso di byte. Per ulteriori informazioni, vedere [**IMFByteStream:: Write**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-write).


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



La `AppendToByteStream` funzione aggiunge il contenuto di un flusso di byte a un altro:


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



## <a name="3-open-the-input-asf-file"></a>3. Aprire il file ASF di input

Aprire il file di input chiamando la funzione [**MFCreateFile**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatefile) . Il metodo restituisce un puntatore all'oggetto flusso di byte che contiene il contenuto del file. Il nome file viene specificato dall'utente tramite gli argomenti della riga di comando dell'applicazione.

Il codice di esempio seguente accetta un nome di file e restituisce un puntatore a un oggetto flusso di byte che può essere usato per leggere il file.


```C++
        // Open the file.
        hr = MFCreateFile(MF_ACCESSMODE_READ, MF_OPENMODE_FAIL_IF_NOT_EXIST, 
            MF_FILEFLAGS_NONE, pszFileName, &pStream);
```



## <a name="4-initialize-objects-for-the-input-file"></a>4. inizializzare gli oggetti per il file di input

Successivamente, sarà possibile creare e inizializzare l'oggetto ContentInfo di origine e la barra di divisione per generare esempi di flusso.

Questo flusso di byte di origine creato nel passaggio 2 verrà usato per analizzare l'oggetto intestazione ASF e popolare l'oggetto ContentInfo di origine. Questo oggetto verrà utilizzato per inizializzare la barra di divisione per semplificare l'analisi dei pacchetti di dati ASF per il flusso audio nel file di input. Sarà inoltre possibile recuperare la lunghezza dell'oggetto dati ASF nel file di input e l'offset al primo pacchetto di dati ASF relativo all'inizio del file. Questi attributi verranno usati dalla barra di divisione per generare esempi di flusso audio.

Per creare e inizializzare i componenti ASF per il file di input:

1.  Chiamare [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) per creare l'oggetto ContentInfo. Questa funzione restituisce un puntatore all'interfaccia [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) .
2.  Chiamare [**IMFASFContentInfo::P arseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) per analizzare l'intestazione ASF. Per ulteriori informazioni su questo passaggio, vedere [lettura dell'oggetto intestazione ASF di un file esistente](reading-the-asf-header-object-of-an-existing-file.md).
3.  Chiamare [**MFCreateASFSplitter**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfsplitter) per creare l'oggetto Splitter ASF. Questa funzione restituisce un puntatore all'interfaccia [**IMFASFSplitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) .
4.  Chiamare [**IMFASFSplitter:: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize), passando il puntatore [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo). Per ulteriori informazioni su questo passaggio, vedere [Creating the ASF Splitter Object](creating-the-asf-splitter-object.md).
5.  Chiamare [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) per ottenere un descrittore di presentazione per il file ASF.
6.  Ottenere il valore dell'attributo [**MF \_ PD \_ ASF \_ data \_ Start \_ offset**](mf-pd-asf-data-start-offset-attribute.md) dal descrittore della presentazione. Questo valore è il percorso dell'oggetto dati ASF nel file, come offset di byte dall'inizio del file.
7.  Ottenere il valore dell'attributo [**di \_ \_ lunghezza dei \_ dati \_ MF PD ASF**](mf-pd-asf-data-length-attribute.md) dal descrittore della presentazione. Questo valore corrisponde alle dimensioni totali dell'oggetto dati ASF, in byte. Per ulteriori informazioni, vedere [recupero di informazioni da oggetti intestazione ASF](getting-information-from-asf-header-objects.md).

Nell'esempio di codice seguente viene illustrata una funzione che consolida tutti i passaggi. Questa funzione accetta un puntatore al flusso di byte di origine e restituisce i puntatori all'oggetto ContentInfo di origine e alla barra di divisione. Inoltre, riceve la lunghezza e gli offset nell'oggetto dati ASF.


```C++
//-------------------------------------------------------------------
// CreateSourceParsers
//
// Creates the ASF splitter and the ASF Content Info object for the 
// source file.
// 
// This function also calulates the offset and length of the ASF 
// Data Object.
//-------------------------------------------------------------------

HRESULT CreateSourceParsers(
    IMFByteStream *pSourceStream,
    IMFASFContentInfo **ppSourceContentInfo,
    IMFASFSplitter **ppSplitter,
    UINT64 *pcbDataOffset,
    UINT64 *pcbDataLength
    )
{
    const DWORD MIN_ASF_HEADER_SIZE = 30;

    IMFMediaBuffer *pBuffer = NULL;
    IMFPresentationDescriptor *pPD = NULL;
    IMFASFContentInfo *pSourceContentInfo = NULL;
    IMFASFSplitter *pSplitter = NULL;

    QWORD cbHeader = 0;

    /*------- Parse the ASF header. -------*/

    // Create the ASF ContentInfo object.
    HRESULT hr = MFCreateASFContentInfo(&pSourceContentInfo);
    
    // Read the first 30 bytes to find the total header size.
    if (SUCCEEDED(hr))
    {
        hr = AllocReadFromByteStream(
            pSourceStream, 
            MIN_ASF_HEADER_SIZE, 
            &pBuffer
            );
    }

    // Get the header size.
    if (SUCCEEDED(hr))
    {
        hr = pSourceContentInfo->GetHeaderSize(pBuffer, &cbHeader);
    }

    // Release the buffer; we will reuse it.
    SafeRelease(&pBuffer);
    
    // Read the entire header into a buffer.
    if (SUCCEEDED(hr))
    {
        hr = pSourceStream->SetCurrentPosition(0);
    }

    if (SUCCEEDED(hr))
    {
        hr = AllocReadFromByteStream(
            pSourceStream, 
            (DWORD)cbHeader, 
            &pBuffer
            );
    }

    // Parse the buffer and populate the header object.
    if (SUCCEEDED(hr))
    {
        hr = pSourceContentInfo->ParseHeader(pBuffer, 0);
    }

    /*------- Initialize the ASF splitter. -------*/

    // Create the splitter.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateASFSplitter(&pSplitter);
    }
    
    // initialize the splitter with the ContentInfo object.
    if (SUCCEEDED(hr))
    {
        hr = pSplitter->Initialize(pSourceContentInfo);
    }


    /*------- Get the offset and size of the ASF Data Object. -------*/

    // Generate the presentation descriptor.
    if (SUCCEEDED(hr))
    {
        hr =  pSourceContentInfo->GeneratePresentationDescriptor(&pPD);
    }

    // Get the offset to the start of the Data Object.
    if (SUCCEEDED(hr))
    {
        hr = pPD->GetUINT64(MF_PD_ASF_DATA_START_OFFSET, pcbDataOffset);
    }

    // Get the length of the Data Object.
    if (SUCCEEDED(hr))
    {
        hr = pPD->GetUINT64(MF_PD_ASF_DATA_LENGTH, pcbDataLength);
    }

    // Return the pointers to the caller.
    if (SUCCEEDED(hr))
    {
        *ppSourceContentInfo = pSourceContentInfo;
        (*ppSourceContentInfo)->AddRef();

        *ppSplitter = pSplitter;
        (*ppSplitter)->AddRef();

    }

    SafeRelease(&pPD);
    SafeRelease(&pBuffer);
    SafeRelease(&pSourceContentInfo);
    SafeRelease(&pSplitter);

    return S_OK;
}
```



## <a name="5-create-an-audio-profile"></a>5. creare un profilo audio

Successivamente, si creerà un oggetto profilo per il file di input ottenendolo dall'oggetto ContentInfo di origine. Il profilo verrà quindi configurato in modo che contenga solo i flussi audio del file di input. A tale scopo, enumerare i flussi e rimuovere i flussi non audio dal profilo. L'oggetto profilo audio verrà usato più avanti in questa esercitazione per inizializzare l'oggetto ContentInfo di output.

Per creare un profilo audio

1.  Ottenere l'oggetto profilo per il file di input dall'oggetto ContentInfo di origine chiamando [**IMFASFContentInfo:: GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile). Il metodo restituisce un puntatore a un oggetto profilo che contiene tutti i flussi nel file di input. Per ulteriori informazioni, vedere [creazione di un profilo ASF](creating-an-asf-profile.md).
2.  Rimuovere gli oggetti di esclusione reciproca dal profilo. Questo passaggio è necessario perché i flussi non audio verranno rimossi dal profilo, che potrebbero invalidare gli oggetti di esclusione reciproca.
3.  Rimuovere tutti i flussi non audio dal profilo, come indicato di seguito:
    -   Chiamare [**IMFASFProfile:: GetStreamCount**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamcount) per ottenere il numero di flussi.
    -   In un ciclo, chiamare [**IMFASFProfile:: GetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream) per ottenere ogni flusso in base all'indice.
    -   Chiamare [**IMFASFStreamConfig:: GetStreamType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getstreamtype) per ottenere il tipo di flusso.
    -   Per i flussi non audio, chiamare [**IMFASFProfile:: RemoveStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removestream) per rimuovere il flusso.
4.  Archiviare il numero di flusso del primo flusso audio. Questo verrà selezionato nella barra di divisione per generare esempi di flusso. Se il numero del flusso è zero, il chiamante può presumere che non esistano file di flussi audio.

Il codice seguente illustra questi passaggi:


```C++
//-------------------------------------------------------------------
// GetAudioProfile
//
// Gets the ASF profile from the source file and removes any video
// streams from the profile.
//-------------------------------------------------------------------

HRESULT GetAudioProfile(
    IMFASFContentInfo *pSourceContentInfo, 
    IMFASFProfile **ppAudioProfile, 
    WORD *pwSelectStreamNumber
    )
{
    IMFASFStreamConfig *pStream = NULL;
    IMFASFProfile *pProfile = NULL;

    DWORD dwTotalStreams = 0;
    WORD  wStreamNumber = 0; 
    GUID guidMajorType = GUID_NULL;
    
    // Get the profile object from the source ContentInfo object.
    HRESULT hr = pSourceContentInfo->GetProfile(&pProfile);

    // Remove mutexes from the profile
    if (SUCCEEDED(hr))
    {
        hr = RemoveMutexes(pProfile);
    }

    // Get the total number of streams on the profile.
    if (SUCCEEDED(hr))
    {
        hr = pProfile->GetStreamCount(&dwTotalStreams);
    }

    // Enumerate the streams and remove the non-audio streams.
    if (SUCCEEDED(hr))
    {
        for (DWORD index = 0; index < dwTotalStreams; )
        {
            hr = pProfile->GetStream(index, &wStreamNumber, &pStream);

            if (FAILED(hr)) { break; }

            hr = pStream->GetStreamType(&guidMajorType);

            SafeRelease(&pStream);

            if (FAILED(hr)) { break; }

            if (guidMajorType != MFMediaType_Audio)
            {
                hr = pProfile->RemoveStream(wStreamNumber);
    
                if (FAILED(hr)) { break; }

                index = 0;
                dwTotalStreams--;
            }
            else
            {
                // Store the first audio stream number. 
                // This will be selected on the splitter.

                if (*pwSelectStreamNumber == 0)
                {
                    *pwSelectStreamNumber = wStreamNumber;
                }

                index++;
            }
        }
    }

    if (SUCCEEDED(hr))
    {
        *ppAudioProfile = pProfile;
        (*ppAudioProfile)->AddRef();
    }

    SafeRelease(&pStream);
    SafeRelease(&pProfile);

    return S_OK;
}
```



La `RemoveMutexes` funzione rimuove gli oggetti di esclusione reciproca dal profilo:


```C++
HRESULT RemoveMutexes(IMFASFProfile *pProfile)
{
    DWORD cMutex = 0;
    HRESULT hr = pProfile->GetMutualExclusionCount(&cMutex);

    if (SUCCEEDED(hr))
    {
        for (DWORD i = 0; i < cMutex; i++)
        {
            hr = pProfile->RemoveMutualExclusion(0);

            if (FAILED(hr))
            {
                break;
            }
        }
    }

    return hr;
}
```



## <a name="6-initialize-objects-for-the-output-file"></a>6. inizializzare gli oggetti per il file di output

Successivamente, si creerà l'oggetto ContentInfo di output e il multiplexer per la generazione dei pacchetti di dati per il file di output.

Il profilo audio creato nel passaggio 4 verrà usato per popolare l'oggetto ContentInfo di output. Questo oggetto contiene informazioni quali gli attributi di file globali e le proprietà del flusso. L'oggetto ContentInfo di output verrà usato per inizializzare il multiplexer che genererà i pacchetti di dati per il file di output. Dopo la generazione dei pacchetti di dati, l'oggetto ContentInfo deve essere aggiornato in modo da riflettere i nuovi valori.

Per creare e inizializzare i componenti ASF per il file di output

1.  Creare un oggetto ContentInfo vuoto chiamando [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) e popolarlo con le informazioni del profilo audio creato nel passaggio 3 chiamando [**IMFASFContentInfo:: seprofile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile). Per ulteriori informazioni, vedere [inizializzazione dell'oggetto ContentInfo di un nuovo file ASF](initializing-the-contentinfo-object-of-a-new-asf-file.md).
2.  Creare e inizializzare l'oggetto multiplexer usando l'oggetto ContentInfo di output. Per ulteriori informazioni, vedere [creazione dell'oggetto multiplexer](creating-the-multiplexer-object.md).

Nell'esempio di codice seguente viene illustrata una funzione che consolida i passaggi. Questa funzione accetta un puntatore a un oggetto profilo e restituisce i puntatori all'oggetto ContentInfo di output e al multiplexer.


```C++
//-------------------------------------------------------------------
// CreateOutputGenerators
//
// Creates the ASF mux and the ASF Content Info object for the 
// output file.
//-------------------------------------------------------------------

HRESULT CreateOutputGenerators(
    IMFASFProfile *pProfile, 
    IMFASFContentInfo **ppContentInfo, 
    IMFASFMultiplexer **ppMux
    )
{
    IMFASFContentInfo *pContentInfo = NULL;
    IMFASFMultiplexer *pMux = NULL;

    // Use the ASF profile to create the ContentInfo object.
    HRESULT hr = MFCreateASFContentInfo(&pContentInfo);

    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->SetProfile(pProfile);
    }

    // Create the ASF Multiplexer object.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateASFMultiplexer(&pMux);
    }
    
    // Initialize it using the new ContentInfo object.
    if (SUCCEEDED(hr))
    {
        hr = pMux->Initialize(pContentInfo);
    }

    // Return the pointers to the caller.
    if (SUCCEEDED(hr))
    {
        *ppContentInfo = pContentInfo;
        (*ppContentInfo)->AddRef();

        *ppMux = pMux;
        (*ppMux)->AddRef();
    }

    SafeRelease(&pContentInfo);
    SafeRelease(&pMux);

    return hr;
}
```



## <a name="7-generate-new-asf-data-packets"></a>7. generare nuovi pacchetti di dati ASF

Successivamente, si genereranno esempi di flusso audio dal flusso di byte di origine usando la barra di divisione e li invierà al multiplexer per creare pacchetti di dati ASF. Questi pacchetti di dati costituiranno l'oggetto dati ASF finale per il nuovo file.

Per generare esempi di flusso audio

1.  Selezionare il primo flusso audio nella barra di divisione chiamando [**IMFASFSplitter:: SelectStreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-selectstreams).
2.  Legge i blocchi a dimensione fissa dei dati multimediali dal flusso di byte di origine in un buffer multimediale.
3.  Raccogliere gli esempi di flusso come esempi di supporti dalla barra di divisione chiamando [**IMFASFSplitter:: GetNextSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample) in un ciclo, purché riceva il \_ flag ASF STATUSFLAGS \_ incomplete nel parametro *pdwStatusFlags* . Per ulteriori informazioni, vedere generazione di esempi per i pacchetti di dati ASF in [generazione di esempi di flusso da un oggetto dati ASF esistente](generating-stream-samples-from-an-existing-asf-data-object.md).
4.  Per ogni esempio di supporto, chiamare [**IMFASFMultiplexer::P rocesssample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) per inviare l'esempio multimediale al multiplexer. Il multiplexer genera i pacchetti di dati per l'oggetto dati ASF.
5.  Scrivere il pacchetto di dati generato dal multiplexer nel flusso di byte di dati.
6.  Dopo aver generato tutti i pacchetti di dati, chiamare [**IMFASFMultiplexer:: end**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-end) per aggiornare l'oggetto ContentInfo di output con le informazioni raccolte durante la generazione del pacchetto di dati ASF.

Il codice di esempio seguente genera esempi di flusso dal separatore ASF e li invia al multiplexer. Il multiplexer genera pacchetti di dati ASF e li scrive in un flusso.


```C++
//-------------------------------------------------------------------
// GenerateASFDataObject
// 
// Creates a byte stream that contains the ASF Data Object for the
// output file.
//-------------------------------------------------------------------

HRESULT GenerateASFDataObject(
    IMFByteStream *pSourceStream, 
    IMFASFSplitter *pSplitter, 
    IMFASFMultiplexer *pMux, 
    UINT64   cbDataOffset,
    UINT64   cbDataLength,
    IMFByteStream **ppDataStream
    )
{
    IMFMediaBuffer *pBuffer = NULL;
    IMFByteStream *pDataStream = NULL;
    
    const DWORD READ_SIZE = 1024 * 4;

    // Flush the splitter to remove any pending samples.
    HRESULT hr = pSplitter->Flush();

    if (SUCCEEDED(hr))
    {
        hr = MFCreateTempFile(
            MF_ACCESSMODE_READWRITE, 
            MF_OPENMODE_DELETE_IF_EXIST,
            MF_FILEFLAGS_NONE,
            &pDataStream
            );
    }

    if (SUCCEEDED(hr))
    {
        hr = pSourceStream->SetCurrentPosition(cbDataOffset);
    }

    if (SUCCEEDED(hr))
    {
        while (cbDataLength > 0)
        {
            DWORD cbRead = min(READ_SIZE, (DWORD)cbDataLength);

            hr = AllocReadFromByteStream(
                pSourceStream, 
                cbRead, 
                &pBuffer
                );

            if (FAILED(hr)) 
            { 
                break; 
            }

            cbDataLength -= cbRead;

            // Push data on the splitter.
            hr =  pSplitter->ParseData(pBuffer, 0, 0);

            if (FAILED(hr)) 
            { 
                break; 
            }

            // Get ASF packets from the splitter and feed them to the mux.
            hr = GetPacketsFromSplitter(pSplitter, pMux, pDataStream);

            if (FAILED(hr)) 
            { 
                break; 
            }

            SafeRelease(&pBuffer);
        }
    }

    // Flush the mux and generate any remaining samples.
    if (SUCCEEDED(hr))
    {
        hr = pMux->Flush();
    }

    if (SUCCEEDED(hr))
    {
        hr = GenerateASFDataPackets(pMux, pDataStream);
    }

     // Return the pointer to the caller.
    if (SUCCEEDED(hr))
    {
        *ppDataStream = pDataStream;
        (*ppDataStream)->AddRef();
    }

    SafeRelease(&pBuffer);
    SafeRelease(&pDataStream);
    return hr;
}
```



Per ottenere i pacchetti dal separatore ASF, il codice precedente chiama la `GetPacketsFromSplitter` funzione, mostrata di seguito:


```C++
//-------------------------------------------------------------------
// GetPacketsFromSplitter
//
// Gets samples from the ASF splitter.
//
// This function is called after calling IMFASFSplitter::ParseData.
//-------------------------------------------------------------------

HRESULT GetPacketsFromSplitter(
    IMFASFSplitter *pSplitter,
    IMFASFMultiplexer *pMux,
    IMFByteStream *pDataStream
    )
{
    HRESULT hr = S_OK;
    DWORD   dwStatus = ASF_STATUSFLAGS_INCOMPLETE;
    WORD    wStreamNum = 0;

    IMFSample *pSample = NULL;

    while (dwStatus & ASF_STATUSFLAGS_INCOMPLETE) 
    {
        hr = pSplitter->GetNextSample(&dwStatus, &wStreamNum, &pSample);

        if (FAILED(hr))
        {
            break;
        }

        if (pSample)
        {
            //Send to the multiplexer to convert it into ASF format
            hr = pMux->ProcessSample(wStreamNum, pSample, 0);

            if (FAILED(hr)) 
            { 
                break; 
            }

            hr = GenerateASFDataPackets(pMux, pDataStream);

            if (FAILED(hr)) 
            { 
                break; 
            }
        }

        SafeRelease(&pSample);
    }

    SafeRelease(&pSample);
    return hr;
}
```



La `GenerateDataPackets` funzione ottiene i pacchetti di dati da multiplexer. Per ulteriori informazioni, vedere [recupero di pacchetti di dati ASF](generating-new-asf-data-packets.md).


```C++
//-------------------------------------------------------------------
// GenerateASFDataPackets
// 
// Gets data packets from the mux. This function is called after 
// calling IMFASFMultiplexer::ProcessSample. 
//-------------------------------------------------------------------

HRESULT GenerateASFDataPackets( 
    IMFASFMultiplexer *pMux, 
    IMFByteStream *pDataStream
    )
{
    HRESULT hr = S_OK;

    IMFSample *pOutputSample = NULL;
    IMFMediaBuffer *pDataPacketBuffer = NULL;

    DWORD dwMuxStatus = ASF_STATUSFLAGS_INCOMPLETE;

    while (dwMuxStatus & ASF_STATUSFLAGS_INCOMPLETE)
    {
        hr = pMux->GetNextPacket(&dwMuxStatus, &pOutputSample);

        if (FAILED(hr))
        {
            break;
        }

        if (pOutputSample)
        {
            //Convert to contiguous buffer
            hr = pOutputSample->ConvertToContiguousBuffer(&pDataPacketBuffer);
            
            if (FAILED(hr))
            {
                break;
            }

            //Write buffer to byte stream
            hr = WriteBufferToByteStream(pDataStream, pDataPacketBuffer, NULL);

            if (FAILED(hr))
            {
                break;
            }
        }

        SafeRelease(&pDataPacketBuffer);
        SafeRelease(&pOutputSample);
    }

    SafeRelease(&pOutputSample);
    SafeRelease(&pDataPacketBuffer);
    return hr;
}
```



## <a name="8-write-the-asf-objects-in-the-new-file"></a>8. scrivere gli oggetti ASF nel nuovo file

Successivamente, si scriverà il contenuto dell'oggetto ContentInfo di output in un buffer multimediale chiamando [**IMFASFContentInfo:: GenerateHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader). Questo metodo converte i dati archiviati nell'oggetto ContentInfo in dati binari nel formato dell'oggetto intestazione ASF. Per ulteriori informazioni, vedere [generazione di un nuovo oggetto intestazione ASF](generating-a-new-asf-header-object.md).

Dopo la generazione del nuovo oggetto intestazione ASF, scrivere il file di output scrivendo prima l'oggetto Header nel flusso di byte di output creato nel passaggio 2 chiamando la funzione di supporto WriteBufferToByteStream. Seguire l'oggetto Header con l'oggetto dati contenuto nel flusso di byte di dati. Nel codice di esempio viene illustrata una funzione che trasferisce il contenuto del flusso di byte di dati al flusso di byte di output.


```C++
//-------------------------------------------------------------------
// WriteASFFile
//
// Writes the complete ASF file.
//-------------------------------------------------------------------

HRESULT WriteASFFile( 
    IMFASFContentInfo *pContentInfo, // ASF Content Info for the output file.
    IMFByteStream *pDataStream,      // Data stream.
    PCWSTR pszFile                   // Output file name.
    )
{
    
    IMFMediaBuffer *pHeaderBuffer = NULL;
    IMFByteStream *pWmaStream = NULL;

    DWORD cbHeaderSize = 0;
    DWORD cbWritten = 0;

    // Create output file.
    HRESULT hr = MFCreateFile(
        MF_ACCESSMODE_WRITE, 
        MF_OPENMODE_DELETE_IF_EXIST,
        MF_FILEFLAGS_NONE,
        pszFile,
        &pWmaStream
        );

    // Get the size of the ASF Header Object.
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->GenerateHeader(NULL, &cbHeaderSize);
    }

    // Create a media buffer.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateMemoryBuffer(cbHeaderSize, &pHeaderBuffer);
    }

    // Populate the media buffer with the ASF Header Object.
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->GenerateHeader(pHeaderBuffer, &cbHeaderSize);
    }
 
    // Write the header contents to the byte stream for the output file.
    if (SUCCEEDED(hr))
    {
        hr = WriteBufferToByteStream(pWmaStream, pHeaderBuffer, &cbWritten);
    }

    if (SUCCEEDED(hr))
    {
        hr = pDataStream->SetCurrentPosition(0);
    }

    // Append the data stream to the file.

    if (SUCCEEDED(hr))
    {
        hr = AppendToByteStream(pDataStream, pWmaStream);
    }

    SafeRelease(&pHeaderBuffer);
    SafeRelease(&pWmaStream);

    return hr;
}
```



## <a name="9-write-the-entry-point-function"></a>9 scrivere la funzione Entry-Point

È ora possibile inserire i passaggi precedenti in un'applicazione completa. Prima di usare uno degli oggetti Media Foundation, inizializzare la piattaforma Media Foundation chiamando [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup). Al termine, chiamare [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown). Per ulteriori informazioni, vedere [inizializzazione di Media Foundation](initializing-media-foundation.md).

Nel codice seguente viene illustrata l'applicazione console completa. L'argomento della riga di comando specifica il nome del file da convertire e il nome del nuovo file audio.


```C++
int wmain(int argc, WCHAR* argv[])
{
    if (argc != 3)
    {
        wprintf_s(L"Usage: %s input.wmv, %s output.wma\n");
        return 0;
    }

    HRESULT hr = MFStartup(MF_VERSION);

    if (FAILED(hr))
    {
        wprintf_s(L"MFStartup failed: 0x%X\n", hr);
        return 0;
    }

    PCWSTR pszInputFile = argv[1];      
    PCWSTR pszOutputFile = argv[2];     
    
    IMFByteStream      *pSourceStream = NULL;       
    IMFASFContentInfo  *pSourceContentInfo = NULL;  
    IMFASFProfile      *pAudioProfile = NULL;       
    IMFASFContentInfo  *pOutputContentInfo = NULL;  
    IMFByteStream      *pDataStream = NULL;         
    IMFASFSplitter     *pSplitter = NULL;           
    IMFASFMultiplexer  *pMux = NULL;                

    UINT64  cbDataOffset = 0;           
    UINT64  cbDataLength = 0;           
    WORD    wSelectStreamNumber = 0;    

    // Open the input file.

    hr = OpenFile(pszInputFile, &pSourceStream);

    // Initialize the objects that will parse the source file.

    if (SUCCEEDED(hr))
    {
        hr = CreateSourceParsers(
            pSourceStream, 
            &pSourceContentInfo,    // ASF Header for the source file.
            &pSplitter,             // Generates audio samples.
            &cbDataOffset,          // Offset to the first data packet.
            &cbDataLength           // Length of the ASF Data Object.
            );
    }

    // Create a profile object for the audio streams in the source file.

    if (SUCCEEDED(hr))
    {
        hr = GetAudioProfile(
            pSourceContentInfo, 
            &pAudioProfile,         // ASF profile for the audio stream.
            &wSelectStreamNumber    // Stream number of the first audio stream.
            );
    }

    // Initialize the objects that will generate the output data.

    if (SUCCEEDED(hr))
    {
        hr = CreateOutputGenerators(
            pAudioProfile, 
            &pOutputContentInfo,    // ASF Header for the output file.
            &pMux                   // Generates ASF data packets.
            );
    }

    // Set up the splitter to generate samples for the first
    // audio stream in the source media.

    if (SUCCEEDED(hr))
    {
        hr = pSplitter->SelectStreams(&wSelectStreamNumber, 1);
    }
    
    // Generate ASF Data Packets and store them in a byte stream.

    if (SUCCEEDED(hr))
    {
        hr = GenerateASFDataObject(
               pSourceStream, 
               pSplitter, 
               pMux, 
               cbDataOffset, 
               cbDataLength, 
               &pDataStream    // Byte stream for the ASF data packets.    
               );
    }

    // Update the header with new information if any.

    if (SUCCEEDED(hr))
    {
        hr = pMux->End(pOutputContentInfo);
    }

    //Write the ASF objects to the output file
    if (SUCCEEDED(hr))
    {
        hr = WriteASFFile(pOutputContentInfo, pDataStream, pszOutputFile);
    }

    // Clean up.
    SafeRelease(&pMux);
    SafeRelease(&pSplitter);
    SafeRelease(&pDataStream);
    SafeRelease(&pOutputContentInfo);
    SafeRelease(&pAudioProfile);
    SafeRelease(&pSourceContentInfo);
    SafeRelease(&pSourceStream);

    MFShutdown();

    if (FAILED(hr))
    {
        wprintf_s(L"Could not create the audio file: 0x%X\n", hr);
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

 

 



