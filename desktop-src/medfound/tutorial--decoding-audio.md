---
description: Questa esercitazione illustra come usare il lettore di origine per decodificare l'audio da un file multimediale e scrivere l'audio in un file WAVE.
ms.assetid: ed40e201-c6ed-444f-bdaa-a5f33d1cc068
title: 'Esercitazione: decodifica audio'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 539eb6d9f48419b62fa1c379c636abaf2bb0a63a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104552270"
---
# <a name="tutorial-decoding-audio"></a>Esercitazione: decodifica audio

Questa esercitazione illustra come usare il [lettore di origine](source-reader.md) per decodificare l'audio da un file multimediale e scrivere l'audio in un file Wave. L'esercitazione è basata sull'esempio di [clip audio](audio-clip-sample.md) .

-   [Overview](#overview)
-   [File di intestazione e di libreria](#header-and-library-files)
-   [Implementare wmain](#implement-wmain)
-   [Scrivere il file WAVE](#write-the-wave-file)
-   [Configurare il lettore di origine](#configure-the-source-reader)
-   [Scrivere l'intestazione del file WAVE](#write-the-wave-file-header)
-   [Calcolare la dimensione massima dei dati](#calculate-the-maximum-data-size)
-   [Decodifica audio](#decode-the-audio)
-   [Finalizzare l'intestazione del file](#finalize-the-file-header)
-   [Argomenti correlati](#related-topics)

## <a name="overview"></a>Panoramica

In questa esercitazione si creerà un'applicazione console che accetta due argomenti della riga di comando: il nome di un file di input che contiene un flusso audio e il nome del file di output. L'applicazione legge cinque secondi di dati audio dal file di input e scrive l'audio nel file di output come dati WAVE.

Per ottenere i dati audio decodificati, l'applicazione utilizza l'oggetto lettore di origine. Il lettore di origine espone l'interfaccia [**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) . Per scrivere l'audio decodificato nel file WAVE, le applicazioni usano le funzioni di I/O di Windows. Questo processo è illustrato nella figura seguente.

![diagramma che mostra al lettore di origine i dati audio ottenuti dal file di origine.](images/audio-clip-tutorial.gif)

Nella sua forma più semplice, un file WAVE ha la struttura seguente:



| Tipo di dati                              | Dimensioni (byte) | Valore                                                                 |
|----------------------------------------|--------------|-----------------------------------------------------------------------|
| **FOURCC**                             | 4            | RIFF                                                                |
| **DWORD**                              | 4            | Dimensioni totali del file, esclusi i primi 8 byte                      |
| **FOURCC**                             | 4            | ONDA                                                                |
| **FOURCC**                             | 4            | FMT                                                                |
| **DWORD**                              | 4            | Dimensione dei dati di [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) che segue. |
| [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) | Varia       | Intestazione del formato audio.                                                  |
| **FOURCC**                             | 4            | dati                                                                |
| **DWORD**                              | 4            | Dimensioni dei dati audio.                                               |
| **BYTE**\[\]                           | Varia       | Dati audio.                                                           |



 

> [!Note]  
> Un **fourcc** è un **DWORD** formato dalla concatenazione di quattro caratteri ASCII.

 

Questa struttura di base può essere estesa aggiungendo metadati di file e altre informazioni che esulano dall'ambito di questa esercitazione.

## <a name="header-and-library-files"></a>File di intestazione e di libreria

Includere i file di intestazione seguenti nel progetto:


```C++
#define WINVER _WIN32_WINNT_WIN7

#include <windows.h>
#include <mfapi.h>
#include <mfidl.h>
#include <mfreadwrite.h>
#include <stdio.h>
#include <mferror.h>
```



Collegamento alle librerie seguenti:

-   mfplat. lib
-   mfreadwrite. lib
-   mfuuid. lib

## <a name="implement-wmain"></a>Implementare wmain

Il codice seguente illustra la funzione del punto di ingresso per l'applicazione.


```C++
int wmain(int argc, wchar_t* argv[])
{
    HeapSetInformation(NULL, HeapEnableTerminationOnCorruption, NULL, 0);

    if (argc != 3)
    {
        printf("arguments: input_file output_file.wav\n");
        return 1;
    }

    const WCHAR *wszSourceFile = argv[1];
    const WCHAR *wszTargetFile = argv[2];

    const LONG MAX_AUDIO_DURATION_MSEC = 5000; // 5 seconds

    HRESULT hr = S_OK;

    IMFSourceReader *pReader = NULL;
    HANDLE hFile = INVALID_HANDLE_VALUE;

    // Initialize the COM library.
    hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | COINIT_DISABLE_OLE1DDE);

    // Initialize the Media Foundation platform.
    if (SUCCEEDED(hr))
    {
        hr = MFStartup(MF_VERSION);
    }

    // Create the source reader to read the input file.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateSourceReaderFromURL(wszSourceFile, NULL, &pReader);
        if (FAILED(hr))
        {
            printf("Error opening input file: %S\n", wszSourceFile, hr);
        }
    }

    // Open the output file for writing.
    if (SUCCEEDED(hr))
    {
        hFile = CreateFile(wszTargetFile, GENERIC_WRITE, FILE_SHARE_READ, NULL,
            CREATE_ALWAYS, 0, NULL);

        if (hFile == INVALID_HANDLE_VALUE)
        {
            hr = HRESULT_FROM_WIN32(GetLastError());
            printf("Cannot create output file: %S\n", wszTargetFile, hr);
        }
    }

    // Write the WAVE file.
    if (SUCCEEDED(hr))
    {
        hr = WriteWaveFile(pReader, hFile, MAX_AUDIO_DURATION_MSEC);
    }

    if (FAILED(hr))
    {
        printf("Failed, hr = 0x%X\n", hr);
    }

    // Clean up.
    if (hFile != INVALID_HANDLE_VALUE)
    {
        CloseHandle(hFile);
    }

    SafeRelease(&pReader);
    MFShutdown();
    CoUninitialize();

    return SUCCEEDED(hr) ? 0 : 1;
};
```



Questa funzione esegue le operazioni seguenti:

1.  Chiama [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) per inizializzare la libreria com.
2.  Chiama [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) per inizializzare la piattaforma Media Foundation.
3.  Chiama [**MFCreateSourceReaderFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl) per creare il lettore di origine. Questa funzione accetta il nome del file di input e riceve un puntatore di interfaccia [**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) .
4.  Crea il file di output chiamando la funzione **CreateFile** , che restituisce un handle di file.
5.  Chiama la funzione [WriteWavFile](#write-the-wave-file) definita dall'applicazione. Questa funzione decodifica l'audio e scrive il file WAVE.
6.  Rilascia il puntatore [**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) e l'handle di file.
7.  Chiama [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) per arrestare la piattaforma Media Foundation.
8.  Chiama [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) per rilasciare la libreria com.

## <a name="write-the-wave-file"></a>Scrivere il file WAVE

La maggior parte del lavoro si verifica nella `WriteWavFile` funzione, che viene chiamata da `wmain` .


```C++
//-------------------------------------------------------------------
// WriteWaveFile
//
// Writes a WAVE file by getting audio data from the source reader.
//
//-------------------------------------------------------------------

HRESULT WriteWaveFile(
    IMFSourceReader *pReader,   // Pointer to the source reader.
    HANDLE hFile,               // Handle to the output file.
    LONG msecAudioData          // Maximum amount of audio data to write, in msec.
    )
{
    HRESULT hr = S_OK;

    DWORD cbHeader = 0;         // Size of the WAVE file header, in bytes.
    DWORD cbAudioData = 0;      // Total bytes of PCM audio data written to the file.
    DWORD cbMaxAudioData = 0;

    IMFMediaType *pAudioType = NULL;    // Represents the PCM audio format.

    // Configure the source reader to get uncompressed PCM audio from the source file.

    hr = ConfigureAudioStream(pReader, &pAudioType);

    // Write the WAVE file header.
    if (SUCCEEDED(hr))
    {
        hr = WriteWaveHeader(hFile, pAudioType, &cbHeader);
    }

    // Calculate the maximum amount of audio to decode, in bytes.
    if (SUCCEEDED(hr))
    {
        cbMaxAudioData = CalculateMaxAudioDataSize(pAudioType, cbHeader, msecAudioData);

        // Decode audio data to the file.
        hr = WriteWaveData(hFile, pReader, cbMaxAudioData, &cbAudioData);
    }

    // Fix up the RIFF headers with the correct sizes.
    if (SUCCEEDED(hr))
    {
        hr = FixUpChunkSizes(hFile, cbHeader, cbAudioData);
    }

    SafeRelease(&pAudioType);
    return hr;
}
```



Questa funzione chiama una serie di altre funzioni definite dall'applicazione:

1.  La funzione [ConfigureAudioStream](#configure-the-source-reader) Inizializza il lettore di origine. Questa funzione riceve un puntatore all'interfaccia [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) , che viene usata per ottenere una descrizione del formato audio decodificato, inclusa la frequenza di campionamento, il numero di canali e la profondità di bit (bit per esempio).
2.  La funzione WriteWaveHeader scrive la prima parte del file WAVE, incluse l'intestazione e l'inizio del blocco "data".
3.  La funzione CalculateMaxAudioDataSize calcola la quantità massima di audio da scrivere nel file, in byte.
4.  La funzione WriteWaveData scrive i dati audio PCM nel file.
5.  La funzione FixUpChunkSizes scrive le informazioni sulle dimensioni del file visualizzate dopo i valori **fourcc** ' riff ' è data ' nel file Wave. Questi valori non sono noti fino al `WriteWaveData` completamento.

Queste funzioni sono illustrate nelle sezioni rimanenti di questa esercitazione.

## <a name="configure-the-source-reader"></a>Configurare il lettore di origine

La `ConfigureAudioStream` funzione configura il lettore di origine per decodificare il flusso audio nel file di origine. Restituisce anche informazioni sul formato dell'audio decodificato.

In Media Foundation i formati multimediali vengono descritti utilizzando oggetti di *tipo supporto* . Un oggetto del tipo di supporto espone l'interfaccia [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) , che eredita l'interfaccia [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) . Essenzialmente, un tipo di supporto è una raccolta di proprietà che descrivono il formato. Per ulteriori informazioni, vedere [tipi di supporti](media-types.md).


```C++
//-------------------------------------------------------------------
// ConfigureAudioStream
//
// Selects an audio stream from the source file, and configures the
// stream to deliver decoded PCM audio.
//-------------------------------------------------------------------

HRESULT ConfigureAudioStream(
    IMFSourceReader *pReader,   // Pointer to the source reader.
    IMFMediaType **ppPCMAudio   // Receives the audio format.
    )
{
    IMFMediaType *pUncompressedAudioType = NULL;
    IMFMediaType *pPartialType = NULL;

    // Select the first audio stream, and deselect all other streams.
    HRESULT hr = pReader->SetStreamSelection(
        (DWORD)MF_SOURCE_READER_ALL_STREAMS, FALSE);

    if (SUCCEEDED(hr))
    {
        hr = pReader->SetStreamSelection(
            (DWORD)MF_SOURCE_READER_FIRST_AUDIO_STREAM, TRUE);
    }

    // Create a partial media type that specifies uncompressed PCM audio.
    hr = MFCreateMediaType(&pPartialType);

    if (SUCCEEDED(hr))
    {
        hr = pPartialType->SetGUID(MF_MT_MAJOR_TYPE, MFMediaType_Audio);
    }

    if (SUCCEEDED(hr))
    {
        hr = pPartialType->SetGUID(MF_MT_SUBTYPE, MFAudioFormat_PCM);
    }

    // Set this type on the source reader. The source reader will
    // load the necessary decoder.
    if (SUCCEEDED(hr))
    {
        hr = pReader->SetCurrentMediaType(
            (DWORD)MF_SOURCE_READER_FIRST_AUDIO_STREAM,
            NULL, pPartialType);
    }

    // Get the complete uncompressed format.
    if (SUCCEEDED(hr))
    {
        hr = pReader->GetCurrentMediaType(
            (DWORD)MF_SOURCE_READER_FIRST_AUDIO_STREAM,
            &pUncompressedAudioType);
    }

    // Ensure the stream is selected.
    if (SUCCEEDED(hr))
    {
        hr = pReader->SetStreamSelection(
            (DWORD)MF_SOURCE_READER_FIRST_AUDIO_STREAM,
            TRUE);
    }

    // Return the PCM format to the caller.
    if (SUCCEEDED(hr))
    {
        *ppPCMAudio = pUncompressedAudioType;
        (*ppPCMAudio)->AddRef();
    }

    SafeRelease(&pUncompressedAudioType);
    SafeRelease(&pPartialType);
    return hr;
}
```



La `ConfigureAudioStream` funzione esegue le operazioni seguenti:

1.  Chiama il metodo [**IMFSourceReader:: SetStreamSelection**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setstreamselection) per selezionare il flusso audio e deselezionare tutti gli altri flussi. Questo passaggio può migliorare le prestazioni, in quanto impedisce al lettore di origine di mantenere i frame video non usati dall'applicazione.
2.  Crea un tipo di supporto *parziale* che specifica l'audio PCM. La funzione crea il tipo parziale come segue:
    1.  Chiama [**MFCreateMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatype) per creare un oggetto di tipo di supporto vuoto.
    2.  Imposta l'attributo del [**\_ \_ \_ tipo principale MF mt**](mf-mt-major-type-attribute.md) su **MFMediaType \_ audio**.
    3.  Imposta l'attributo del [**\_ \_ sottotipo MF mt**](mf-mt-subtype-attribute.md) su **MFAudioFormat \_ PCM**.
3.  Chiama [**IMFSourceReader:: SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype) per impostare il tipo parziale nel lettore di origine. Se il file di origine contiene audio codificato, il lettore di origine carica automaticamente il decoder audio necessario.
4.  Chiama [**IMFSourceReader:: GetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getcurrentmediatype) per ottenere il tipo di supporto PCM effettivo. Questo metodo restituisce un tipo di supporto con tutti i dettagli di formato compilati, ad esempio la frequenza di campionamento audio e il numero di canali.
5.  Chiama [**IMFSourceReader:: SetStreamSelection**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setstreamselection) per abilitare il flusso audio.

## <a name="write-the-wave-file-header"></a>Scrivere l'intestazione del file WAVE

La `WriteWaveHeader` funzione scrive l'intestazione del file Wave.

L'unica API Media Foundation chiamata da questa funzione è [**MFCreateWaveFormatExFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatewaveformatexfrommfmediatype), che converte il tipo di supporto in una struttura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .


```C++
//-------------------------------------------------------------------
// WriteWaveHeader
//
// Write the WAVE file header.
//
// Note: This function writes placeholder values for the file size
// and data size, as these values will need to be filled in later.
//-------------------------------------------------------------------

HRESULT WriteWaveHeader(
    HANDLE hFile,               // Output file.
    IMFMediaType *pMediaType,   // PCM audio format.
    DWORD *pcbWritten           // Receives the size of the header.
    )
{
    HRESULT hr = S_OK;
    UINT32 cbFormat = 0;

    WAVEFORMATEX *pWav = NULL;

    *pcbWritten = 0;

    // Convert the PCM audio format into a WAVEFORMATEX structure.
    hr = MFCreateWaveFormatExFromMFMediaType(pMediaType, &pWav, &cbFormat);

    // Write the 'RIFF' header and the start of the 'fmt ' chunk.
    if (SUCCEEDED(hr))
    {
        DWORD header[] = {
            // RIFF header
            FCC('RIFF'),
            0,
            FCC('WAVE'),
            // Start of 'fmt ' chunk
            FCC('fmt '),
            cbFormat
        };

        DWORD dataHeader[] = { FCC('data'), 0 };

        hr = WriteToFile(hFile, header, sizeof(header));

        // Write the WAVEFORMATEX structure.
        if (SUCCEEDED(hr))
        {
            hr = WriteToFile(hFile, pWav, cbFormat);
        }

        // Write the start of the 'data' chunk

        if (SUCCEEDED(hr))
        {
            hr = WriteToFile(hFile, dataHeader, sizeof(dataHeader));
        }

        if (SUCCEEDED(hr))
        {
            *pcbWritten = sizeof(header) + cbFormat + sizeof(dataHeader);
        }
    }


    CoTaskMemFree(pWav);
    return hr;
}
```



La `WriteToFile` funzione è una funzione di supporto semplice che esegue il wrapping della funzione **WriteFile** di Windows e restituisce un valore **HRESULT** .


```C++
//-------------------------------------------------------------------
//
// Writes a block of data to a file
//
// hFile: Handle to the file.
// p: Pointer to the buffer to write.
// cb: Size of the buffer, in bytes.
//
//-------------------------------------------------------------------

HRESULT WriteToFile(HANDLE hFile, void* p, DWORD cb)
{
    DWORD cbWritten = 0;
    HRESULT hr = S_OK;

    BOOL bResult = WriteFile(hFile, p, cb, &cbWritten, NULL);
    if (!bResult)
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
    }
    return hr;
}
```



## <a name="calculate-the-maximum-data-size"></a>Calcolare la dimensione massima dei dati

Poiché le dimensioni del file vengono archiviate come valore a 4 byte nell'intestazione del file, un file WAVE è limitato a una dimensione massima di 0xFFFFFFFF byte, circa 4 GB. Questo valore include le dimensioni dell'intestazione del file. L'audio PCM ha una velocità in bit costante, quindi è possibile calcolare le dimensioni massime dei dati dal formato audio, come indicato di seguito:


```C++
//-------------------------------------------------------------------
// CalculateMaxAudioDataSize
//
// Calculates how much audio to write to the WAVE file, given the
// audio format and the maximum duration of the WAVE file.
//-------------------------------------------------------------------

DWORD CalculateMaxAudioDataSize(
    IMFMediaType *pAudioType,    // The PCM audio format.
    DWORD cbHeader,              // The size of the WAVE file header.
    DWORD msecAudioData          // Maximum duration, in milliseconds.
    )
{
    UINT32 cbBlockSize = 0;         // Audio frame size, in bytes.
    UINT32 cbBytesPerSecond = 0;    // Bytes per second.

    // Get the audio block size and number of bytes/second from the audio format.

    cbBlockSize = MFGetAttributeUINT32(pAudioType, MF_MT_AUDIO_BLOCK_ALIGNMENT, 0);
    cbBytesPerSecond = MFGetAttributeUINT32(pAudioType, MF_MT_AUDIO_AVG_BYTES_PER_SECOND, 0);

    // Calculate the maximum amount of audio data to write.
    // This value equals (duration in seconds x bytes/second), but cannot
    // exceed the maximum size of the data chunk in the WAVE file.

        // Size of the desired audio clip in bytes:
    DWORD cbAudioClipSize = (DWORD)MulDiv(cbBytesPerSecond, msecAudioData, 1000);

    // Largest possible size of the data chunk:
    DWORD cbMaxSize = MAXDWORD - cbHeader;

    // Maximum size altogether.
    cbAudioClipSize = min(cbAudioClipSize, cbMaxSize);

    // Round to the audio block size, so that we do not write a partial audio frame.
    cbAudioClipSize = (cbAudioClipSize / cbBlockSize) * cbBlockSize;

    return cbAudioClipSize;
}
```



Per evitare i frame audio parziali, la dimensione viene arrotondata all'allineamento del blocco, che è archiviato nell'attributo di [**\_ \_ \_ \_ allineamento a blocchi audio di MF mt**](mf-mt-audio-block-alignment-attribute.md) .

## <a name="decode-the-audio"></a>Decodifica audio

La `WriteWaveData` funzione legge l'audio decodificato dal file di origine e scrive nel file Wave.


```C++
//-------------------------------------------------------------------
// WriteWaveData
//
// Decodes PCM audio data from the source file and writes it to
// the WAVE file.
//-------------------------------------------------------------------

HRESULT WriteWaveData(
    HANDLE hFile,               // Output file.
    IMFSourceReader *pReader,   // Source reader.
    DWORD cbMaxAudioData,       // Maximum amount of audio data (bytes).
    DWORD *pcbDataWritten       // Receives the amount of data written.
    )
{
    HRESULT hr = S_OK;
    DWORD cbAudioData = 0;
    DWORD cbBuffer = 0;
    BYTE *pAudioData = NULL;

    IMFSample *pSample = NULL;
    IMFMediaBuffer *pBuffer = NULL;

    // Get audio samples from the source reader.
    while (true)
    {
        DWORD dwFlags = 0;

        // Read the next sample.
        hr = pReader->ReadSample(
            (DWORD)MF_SOURCE_READER_FIRST_AUDIO_STREAM,
            0, NULL, &dwFlags, NULL, &pSample );

        if (FAILED(hr)) { break; }

        if (dwFlags & MF_SOURCE_READERF_CURRENTMEDIATYPECHANGED)
        {
            printf("Type change - not supported by WAVE file format.\n");
            break;
        }
        if (dwFlags & MF_SOURCE_READERF_ENDOFSTREAM)
        {
            printf("End of input file.\n");
            break;
        }

        if (pSample == NULL)
        {
            printf("No sample\n");
            continue;
        }

        // Get a pointer to the audio data in the sample.

        hr = pSample->ConvertToContiguousBuffer(&pBuffer);

        if (FAILED(hr)) { break; }


        hr = pBuffer->Lock(&pAudioData, NULL, &cbBuffer);

        if (FAILED(hr)) { break; }


        // Make sure not to exceed the specified maximum size.
        if (cbMaxAudioData - cbAudioData < cbBuffer)
        {
            cbBuffer = cbMaxAudioData - cbAudioData;
        }

        // Write this data to the output file.
        hr = WriteToFile(hFile, pAudioData, cbBuffer);

        if (FAILED(hr)) { break; }

        // Unlock the buffer.
        hr = pBuffer->Unlock();
        pAudioData = NULL;

        if (FAILED(hr)) { break; }

        // Update running total of audio data.
        cbAudioData += cbBuffer;

        if (cbAudioData >= cbMaxAudioData)
        {
            break;
        }

        SafeRelease(&pSample);
        SafeRelease(&pBuffer);
    }

    if (SUCCEEDED(hr))
    {
        printf("Wrote %d bytes of audio data.\n", cbAudioData);

        *pcbDataWritten = cbAudioData;
    }

    if (pAudioData)
    {
        pBuffer->Unlock();
    }

    SafeRelease(&pBuffer);
    SafeRelease(&pSample);
    return hr;
}
```



La `WriteWaveData` funzione esegue le operazioni seguenti in un ciclo:

1.  Chiama [**IMFSourceReader:: ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) per leggere l'audio dal file di origine. Il parametro *dwFlags* riceve **un operatore OR** bit per bit di flag dall'enumerazione del [**flag del \_ lettore di origine \_ \_ MF**](/windows/desktop/api/mfreadwrite/ne-mfreadwrite-mf_source_reader_flag) . Il parametro *pSample* riceve un puntatore all'interfaccia [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) , che viene usata per accedere ai dati audio. In alcuni casi una chiamata a **ReadSample** non genera dati, nel qual caso il puntatore **IMFSample** è **null**.
2.  Controlla *dwFlags* per i flag seguenti:
    -   **MF \_ \_ \_ CURRENTMEDIATYPECHANGED READERF di origine**. Questo flag indica una modifica del formato nel file di origine. I file WAVE non supportano le modifiche del formato.
    -   **MF \_ \_ \_ ENDOFSTREAM READERF di origine**. Questo flag indica la fine del flusso.
3.  Chiama [**IMFSample:: ConvertToContiguousBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-converttocontiguousbuffer) per ottenere un puntatore a un oggetto buffer.
4.  Chiama [**IMFMediaBuffer:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) per ottenere un puntatore alla memoria del buffer.
5.  Scrive i dati audio nel file di output.
6.  Chiama [**IMFMediaBuffer:: Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) per sbloccare l'oggetto buffer.

La funzione interrompe il ciclo quando si verifica una delle condizioni seguenti:

-   Il formato del flusso cambia.
-   È stata raggiunta la fine del flusso.
-   La quantità massima di dati audio viene scritta nel file di output.
-   Si è verificato un errore.

## <a name="finalize-the-file-header"></a>Finalizzare l'intestazione del file

I valori delle dimensioni archiviati nell'intestazione WAVE non sono noti fino al completamento della funzione precedente. Il `FixUpChunkSizes` Compila i valori seguenti:


```C++
//-------------------------------------------------------------------
// FixUpChunkSizes
//
// Writes the file-size information into the WAVE file header.
//
// WAVE files use the RIFF file format. Each RIFF chunk has a data
// size, and the RIFF header has a total file size.
//-------------------------------------------------------------------

HRESULT FixUpChunkSizes(
    HANDLE hFile,           // Output file.
    DWORD cbHeader,         // Size of the 'fmt ' chuck.
    DWORD cbAudioData       // Size of the 'data' chunk.
    )
{
    HRESULT hr = S_OK;

    LARGE_INTEGER ll;
    ll.QuadPart = cbHeader - sizeof(DWORD);

    if (0 == SetFilePointerEx(hFile, ll, NULL, FILE_BEGIN))
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
    }

    // Write the data size.

    if (SUCCEEDED(hr))
    {
        hr = WriteToFile(hFile, &cbAudioData, sizeof(cbAudioData));
    }

    if (SUCCEEDED(hr))
    {
        // Write the file size.
        ll.QuadPart = sizeof(FOURCC);

        if (0 == SetFilePointerEx(hFile, ll, NULL, FILE_BEGIN))
        {
            hr = HRESULT_FROM_WIN32(GetLastError());
        }
    }

    if (SUCCEEDED(hr))
    {
        DWORD cbRiffFileSize = cbHeader + cbAudioData - 8;

        // NOTE: The "size" field in the RIFF header does not include
        // the first 8 bytes of the file. (That is, the size of the
        // data that appears after the size field.)

        hr = WriteToFile(hFile, &cbRiffFileSize, sizeof(cbRiffFileSize));
    }

    return hr;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di supporti audio](audio-media-types.md)
</dt> <dt>

[Lettore di origine](source-reader.md)
</dt> <dt>

[**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader)
</dt> </dl>

 

 
