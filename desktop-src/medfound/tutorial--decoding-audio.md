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
# <a name="tutorial-decoding-audio"></a><span data-ttu-id="9e0c4-103">Esercitazione: decodifica audio</span><span class="sxs-lookup"><span data-stu-id="9e0c4-103">Tutorial: Decoding Audio</span></span>

<span data-ttu-id="9e0c4-104">Questa esercitazione illustra come usare il [lettore di origine](source-reader.md) per decodificare l'audio da un file multimediale e scrivere l'audio in un file Wave.</span><span class="sxs-lookup"><span data-stu-id="9e0c4-104">This tutorial shows how to use the [Source Reader](source-reader.md) to decode audio from a media file and write the audio to a WAVE file.</span></span> <span data-ttu-id="9e0c4-105">L'esercitazione è basata sull'esempio di [clip audio](audio-clip-sample.md) .</span><span class="sxs-lookup"><span data-stu-id="9e0c4-105">The tutorial is based on the [Audio Clip](audio-clip-sample.md) sample.</span></span>

-   [<span data-ttu-id="9e0c4-106">Overview</span><span class="sxs-lookup"><span data-stu-id="9e0c4-106">Overview</span></span>](#overview)
-   [<span data-ttu-id="9e0c4-107">File di intestazione e di libreria</span><span class="sxs-lookup"><span data-stu-id="9e0c4-107">Header and Library Files</span></span>](#header-and-library-files)
-   [<span data-ttu-id="9e0c4-108">Implementare wmain</span><span class="sxs-lookup"><span data-stu-id="9e0c4-108">Implement wmain</span></span>](#implement-wmain)
-   [<span data-ttu-id="9e0c4-109">Scrivere il file WAVE</span><span class="sxs-lookup"><span data-stu-id="9e0c4-109">Write the WAVE File</span></span>](#write-the-wave-file)
-   [<span data-ttu-id="9e0c4-110">Configurare il lettore di origine</span><span class="sxs-lookup"><span data-stu-id="9e0c4-110">Configure the Source Reader</span></span>](#configure-the-source-reader)
-   [<span data-ttu-id="9e0c4-111">Scrivere l'intestazione del file WAVE</span><span class="sxs-lookup"><span data-stu-id="9e0c4-111">Write the WAVE File Header</span></span>](#write-the-wave-file-header)
-   [<span data-ttu-id="9e0c4-112">Calcolare la dimensione massima dei dati</span><span class="sxs-lookup"><span data-stu-id="9e0c4-112">Calculate the Maximum Data Size</span></span>](#calculate-the-maximum-data-size)
-   [<span data-ttu-id="9e0c4-113">Decodifica audio</span><span class="sxs-lookup"><span data-stu-id="9e0c4-113">Decode the Audio</span></span>](#decode-the-audio)
-   [<span data-ttu-id="9e0c4-114">Finalizzare l'intestazione del file</span><span class="sxs-lookup"><span data-stu-id="9e0c4-114">Finalize the File Header</span></span>](#finalize-the-file-header)
-   [<span data-ttu-id="9e0c4-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9e0c4-115">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="9e0c4-116">Panoramica</span><span class="sxs-lookup"><span data-stu-id="9e0c4-116">Overview</span></span>

<span data-ttu-id="9e0c4-117">In questa esercitazione si creerà un'applicazione console che accetta due argomenti della riga di comando: il nome di un file di input che contiene un flusso audio e il nome del file di output.</span><span class="sxs-lookup"><span data-stu-id="9e0c4-117">In this tutorial, you will create a console application that takes two command-line arguments: The name of an input file that contains an audio stream, and the output file name.</span></span> <span data-ttu-id="9e0c4-118">L'applicazione legge cinque secondi di dati audio dal file di input e scrive l'audio nel file di output come dati WAVE.</span><span class="sxs-lookup"><span data-stu-id="9e0c4-118">The application reads five seconds of audio data from the input file and writes the audio to the output file as WAVE data.</span></span>

<span data-ttu-id="9e0c4-119">Per ottenere i dati audio decodificati, l'applicazione utilizza l'oggetto lettore di origine.</span><span class="sxs-lookup"><span data-stu-id="9e0c4-119">To get the decoded audio data, the application uses the source reader object.</span></span> <span data-ttu-id="9e0c4-120">Il lettore di origine espone l'interfaccia [**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) .</span><span class="sxs-lookup"><span data-stu-id="9e0c4-120">The source reader exposes the [**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) interface.</span></span> <span data-ttu-id="9e0c4-121">Per scrivere l'audio decodificato nel file WAVE, le applicazioni usano le funzioni di I/O di Windows.</span><span class="sxs-lookup"><span data-stu-id="9e0c4-121">To write the decoded audio to the WAVE file, the applications uses Windows I/O functions.</span></span> <span data-ttu-id="9e0c4-122">Questo processo è illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="9e0c4-122">The following image illustrates this process.</span></span>

![diagramma che mostra al lettore di origine i dati audio ottenuti dal file di origine.](images/audio-clip-tutorial.gif)

<span data-ttu-id="9e0c4-124">Nella sua forma più semplice, un file WAVE ha la struttura seguente:</span><span class="sxs-lookup"><span data-stu-id="9e0c4-124">In its simplest form, a WAVE file has the following structure:</span></span>



| <span data-ttu-id="9e0c4-125">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="9e0c4-125">Data Type</span></span>                              | <span data-ttu-id="9e0c4-126">Dimensioni (byte)</span><span class="sxs-lookup"><span data-stu-id="9e0c4-126">Size (Bytes)</span></span> | <span data-ttu-id="9e0c4-127">Valore</span><span class="sxs-lookup"><span data-stu-id="9e0c4-127">Value</span></span>                                                                 |
|----------------------------------------|--------------|-----------------------------------------------------------------------|
| <span data-ttu-id="9e0c4-128">**FOURCC**</span><span class="sxs-lookup"><span data-stu-id="9e0c4-128">**FOURCC**</span></span>                             | <span data-ttu-id="9e0c4-129">4</span><span class="sxs-lookup"><span data-stu-id="9e0c4-129">4</span></span>            | <span data-ttu-id="9e0c4-130">RIFF</span><span class="sxs-lookup"><span data-stu-id="9e0c4-130">'RIFF'</span></span>                                                                |
| <span data-ttu-id="9e0c4-131">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="9e0c4-131">**DWORD**</span></span>                              | <span data-ttu-id="9e0c4-132">4</span><span class="sxs-lookup"><span data-stu-id="9e0c4-132">4</span></span>            | <span data-ttu-id="9e0c4-133">Dimensioni totali del file, esclusi i primi 8 byte</span><span class="sxs-lookup"><span data-stu-id="9e0c4-133">Total file size, not including the first 8 bytes</span></span>                      |
| <span data-ttu-id="9e0c4-134">**FOURCC**</span><span class="sxs-lookup"><span data-stu-id="9e0c4-134">**FOURCC**</span></span>                             | <span data-ttu-id="9e0c4-135">4</span><span class="sxs-lookup"><span data-stu-id="9e0c4-135">4</span></span>            | <span data-ttu-id="9e0c4-136">ONDA</span><span class="sxs-lookup"><span data-stu-id="9e0c4-136">'WAVE'</span></span>                                                                |
| <span data-ttu-id="9e0c4-137">**FOURCC**</span><span class="sxs-lookup"><span data-stu-id="9e0c4-137">**FOURCC**</span></span>                             | <span data-ttu-id="9e0c4-138">4</span><span class="sxs-lookup"><span data-stu-id="9e0c4-138">4</span></span>            | <span data-ttu-id="9e0c4-139">FMT</span><span class="sxs-lookup"><span data-stu-id="9e0c4-139">'fmt '</span></span>                                                                |
| <span data-ttu-id="9e0c4-140">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="9e0c4-140">**DWORD**</span></span>                              | <span data-ttu-id="9e0c4-141">4</span><span class="sxs-lookup"><span data-stu-id="9e0c4-141">4</span></span>            | <span data-ttu-id="9e0c4-142">Dimensione dei dati di [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) che segue.</span><span class="sxs-lookup"><span data-stu-id="9e0c4-142">Size of the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) data that follows.</span></span> |
| <span data-ttu-id="9e0c4-143">[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9e0c4-143">[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))</span></span> | <span data-ttu-id="9e0c4-144">Varia</span><span class="sxs-lookup"><span data-stu-id="9e0c4-144">Varies</span></span>       | <span data-ttu-id="9e0c4-145">Intestazione del formato audio.</span><span class="sxs-lookup"><span data-stu-id="9e0c4-145">Audio format header.</span></span>                                                  |
| <span data-ttu-id="9e0c4-146">**FOURCC**</span><span class="sxs-lookup"><span data-stu-id="9e0c4-146">**FOURCC**</span></span>                             | <span data-ttu-id="9e0c4-147">4</span><span class="sxs-lookup"><span data-stu-id="9e0c4-147">4</span></span>            | <span data-ttu-id="9e0c4-148">dati</span><span class="sxs-lookup"><span data-stu-id="9e0c4-148">'data'</span></span>                                                                |
| <span data-ttu-id="9e0c4-149">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="9e0c4-149">**DWORD**</span></span>                              | <span data-ttu-id="9e0c4-150">4</span><span class="sxs-lookup"><span data-stu-id="9e0c4-150">4</span></span>            | <span data-ttu-id="9e0c4-151">Dimensioni dei dati audio.</span><span class="sxs-lookup"><span data-stu-id="9e0c4-151">Size of the audio data.</span></span>                                               |
| <span data-ttu-id="9e0c4-152">**BYTE**\[\]</span><span class="sxs-lookup"><span data-stu-id="9e0c4-152">**BYTE**\[\]</span></span>                           | <span data-ttu-id="9e0c4-153">Varia</span><span class="sxs-lookup"><span data-stu-id="9e0c4-153">Varies</span></span>       | <span data-ttu-id="9e0c4-154">Dati audio.</span><span class="sxs-lookup"><span data-stu-id="9e0c4-154">Audio data.</span></span>                                                           |



 

> [!Note]  
> <span data-ttu-id="9e0c4-155">Un **fourcc** è un **DWORD** formato dalla concatenazione di quattro caratteri ASCII.</span><span class="sxs-lookup"><span data-stu-id="9e0c4-155">A **FOURCC** is a **DWORD** formed by concatenating four ASCII characters.</span></span>

 

<span data-ttu-id="9e0c4-156">Questa struttura di base può essere estesa aggiungendo metadati di file e altre informazioni che esulano dall'ambito di questa esercitazione.</span><span class="sxs-lookup"><span data-stu-id="9e0c4-156">This basic structure can be extended by adding file metadata and other information, which is beyond the scope of this tutorial.</span></span>

## <a name="header-and-library-files"></a><span data-ttu-id="9e0c4-157">File di intestazione e di libreria</span><span class="sxs-lookup"><span data-stu-id="9e0c4-157">Header and Library Files</span></span>

<span data-ttu-id="9e0c4-158">Includere i file di intestazione seguenti nel progetto:</span><span class="sxs-lookup"><span data-stu-id="9e0c4-158">Include the following header files in your project:</span></span>


```C++
#define WINVER _WIN32_WINNT_WIN7

#include <windows.h>
#include <mfapi.h>
#include <mfidl.h>
#include <mfreadwrite.h>
#include <stdio.h>
#include <mferror.h>
```



<span data-ttu-id="9e0c4-159">Collegamento alle librerie seguenti:</span><span class="sxs-lookup"><span data-stu-id="9e0c4-159">Link to the following libraries:</span></span>

-   <span data-ttu-id="9e0c4-160">mfplat. lib</span><span class="sxs-lookup"><span data-stu-id="9e0c4-160">mfplat.lib</span></span>
-   <span data-ttu-id="9e0c4-161">mfreadwrite. lib</span><span class="sxs-lookup"><span data-stu-id="9e0c4-161">mfreadwrite.lib</span></span>
-   <span data-ttu-id="9e0c4-162">mfuuid. lib</span><span class="sxs-lookup"><span data-stu-id="9e0c4-162">mfuuid.lib</span></span>

## <a name="implement-wmain"></a><span data-ttu-id="9e0c4-163">Implementare wmain</span><span class="sxs-lookup"><span data-stu-id="9e0c4-163">Implement wmain</span></span>

<span data-ttu-id="9e0c4-164">Il codice seguente illustra la funzione del punto di ingresso per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9e0c4-164">The following code shows the entry-point function for the application.</span></span>


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



<span data-ttu-id="9e0c4-165">Questa funzione esegue le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="9e0c4-165">This function does the following:</span></span>

1.  <span data-ttu-id="9e0c4-166">Chiama [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) per inizializzare la libreria com.</span><span class="sxs-lookup"><span data-stu-id="9e0c4-166">Calls [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) to initialize the COM library.</span></span>
2.  <span data-ttu-id="9e0c4-167">Chiama [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) per inizializzare la piattaforma Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="9e0c4-167">Calls [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) to initialize the Media Foundation platform.</span></span>
3.  <span data-ttu-id="9e0c4-168">Chiama [**MFCreateSourceReaderFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl) per creare il lettore di origine.</span><span class="sxs-lookup"><span data-stu-id="9e0c4-168">Calls [**MFCreateSourceReaderFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl) to create the source reader.</span></span> <span data-ttu-id="9e0c4-169">Questa funzione accetta il nome del file di input e riceve un puntatore di interfaccia [**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) .</span><span class="sxs-lookup"><span data-stu-id="9e0c4-169">This function takes the name of the input file and receives an [**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) interface pointer.</span></span>
4.  <span data-ttu-id="9e0c4-170">Crea il file di output chiamando la funzione **CreateFile** , che restituisce un handle di file.</span><span class="sxs-lookup"><span data-stu-id="9e0c4-170">Creates the output file by calling the **CreateFile** function, which returns a file handle.</span></span>
5.  <span data-ttu-id="9e0c4-171">Chiama la funzione [WriteWavFile](#write-the-wave-file) definita dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9e0c4-171">Calls the application-defined [WriteWavFile](#write-the-wave-file) function.</span></span> <span data-ttu-id="9e0c4-172">Questa funzione decodifica l'audio e scrive il file WAVE.</span><span class="sxs-lookup"><span data-stu-id="9e0c4-172">This function decodes the audio and writes the WAVE file.</span></span>
6.  <span data-ttu-id="9e0c4-173">Rilascia il puntatore [**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) e l'handle di file.</span><span class="sxs-lookup"><span data-stu-id="9e0c4-173">Releases the [**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) pointer and the file handle.</span></span>
7.  <span data-ttu-id="9e0c4-174">Chiama [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) per arrestare la piattaforma Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="9e0c4-174">Calls [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) to shut down the Media Foundation platform.</span></span>
8.  <span data-ttu-id="9e0c4-175">Chiama [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) per rilasciare la libreria com.</span><span class="sxs-lookup"><span data-stu-id="9e0c4-175">Calls [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) to release the COM library.</span></span>

## <a name="write-the-wave-file"></a><span data-ttu-id="9e0c4-176">Scrivere il file WAVE</span><span class="sxs-lookup"><span data-stu-id="9e0c4-176">Write the WAVE File</span></span>

<span data-ttu-id="9e0c4-177">La maggior parte del lavoro si verifica nella `WriteWavFile` funzione, che viene chiamata da `wmain` .</span><span class="sxs-lookup"><span data-stu-id="9e0c4-177">Most of the work happens in the `WriteWavFile` function, which is called from `wmain`.</span></span>


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



<span data-ttu-id="9e0c4-178">Questa funzione chiama una serie di altre funzioni definite dall'applicazione:</span><span class="sxs-lookup"><span data-stu-id="9e0c4-178">This function calls a series of other application-defined functions:</span></span>

1.  <span data-ttu-id="9e0c4-179">La funzione [ConfigureAudioStream](#configure-the-source-reader) Inizializza il lettore di origine.</span><span class="sxs-lookup"><span data-stu-id="9e0c4-179">The [ConfigureAudioStream](#configure-the-source-reader) function initializes the source reader.</span></span> <span data-ttu-id="9e0c4-180">Questa funzione riceve un puntatore all'interfaccia [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) , che viene usata per ottenere una descrizione del formato audio decodificato, inclusa la frequenza di campionamento, il numero di canali e la profondità di bit (bit per esempio).</span><span class="sxs-lookup"><span data-stu-id="9e0c4-180">This function receives a pointer to the [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface, which is used to get a description of the decoded audio format, including sample rate, number of channels, and bit depth (bits per sample).</span></span>
2.  <span data-ttu-id="9e0c4-181">La funzione WriteWaveHeader scrive la prima parte del file WAVE, incluse l'intestazione e l'inizio del blocco "data".</span><span class="sxs-lookup"><span data-stu-id="9e0c4-181">The WriteWaveHeader function writes the first part of the WAVE file, including the header and the start of the 'data' chunk.</span></span>
3.  <span data-ttu-id="9e0c4-182">La funzione CalculateMaxAudioDataSize calcola la quantità massima di audio da scrivere nel file, in byte.</span><span class="sxs-lookup"><span data-stu-id="9e0c4-182">The CalculateMaxAudioDataSize function calculates the maximum amount of audio to write to the file, in bytes.</span></span>
4.  <span data-ttu-id="9e0c4-183">La funzione WriteWaveData scrive i dati audio PCM nel file.</span><span class="sxs-lookup"><span data-stu-id="9e0c4-183">The WriteWaveData function writes the PCM audio data to the file.</span></span>
5.  <span data-ttu-id="9e0c4-184">La funzione FixUpChunkSizes scrive le informazioni sulle dimensioni del file visualizzate dopo i valori **fourcc** ' riff ' è data ' nel file Wave.</span><span class="sxs-lookup"><span data-stu-id="9e0c4-184">The FixUpChunkSizes function writes the file-size information that appears after the 'RIFF' and 'data' **FOURCC** values in the WAVE file.</span></span> <span data-ttu-id="9e0c4-185">Questi valori non sono noti fino al `WriteWaveData` completamento.</span><span class="sxs-lookup"><span data-stu-id="9e0c4-185">(These values are not known until `WriteWaveData` completes.)</span></span>

<span data-ttu-id="9e0c4-186">Queste funzioni sono illustrate nelle sezioni rimanenti di questa esercitazione.</span><span class="sxs-lookup"><span data-stu-id="9e0c4-186">These functions are shown in the remaining sections of this tutorial.</span></span>

## <a name="configure-the-source-reader"></a><span data-ttu-id="9e0c4-187">Configurare il lettore di origine</span><span class="sxs-lookup"><span data-stu-id="9e0c4-187">Configure the Source Reader</span></span>

<span data-ttu-id="9e0c4-188">La `ConfigureAudioStream` funzione configura il lettore di origine per decodificare il flusso audio nel file di origine.</span><span class="sxs-lookup"><span data-stu-id="9e0c4-188">The `ConfigureAudioStream` function configures the source reader to decode the audio stream in the source file.</span></span> <span data-ttu-id="9e0c4-189">Restituisce anche informazioni sul formato dell'audio decodificato.</span><span class="sxs-lookup"><span data-stu-id="9e0c4-189">It also returns information about the format of the decoded audio.</span></span>

<span data-ttu-id="9e0c4-190">In Media Foundation i formati multimediali vengono descritti utilizzando oggetti di *tipo supporto* .</span><span class="sxs-lookup"><span data-stu-id="9e0c4-190">In Media Foundation, media formats are described using *media type* objects.</span></span> <span data-ttu-id="9e0c4-191">Un oggetto del tipo di supporto espone l'interfaccia [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) , che eredita l'interfaccia [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="9e0c4-191">A media type object exposes the [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface, which inherits the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span> <span data-ttu-id="9e0c4-192">Essenzialmente, un tipo di supporto è una raccolta di proprietà che descrivono il formato.</span><span class="sxs-lookup"><span data-stu-id="9e0c4-192">Essentially, a media type is a collection of properties that describe the format.</span></span> <span data-ttu-id="9e0c4-193">Per ulteriori informazioni, vedere [tipi di supporti](media-types.md).</span><span class="sxs-lookup"><span data-stu-id="9e0c4-193">For more information, see [Media Types](media-types.md).</span></span>


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



<span data-ttu-id="9e0c4-194">La `ConfigureAudioStream` funzione esegue le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="9e0c4-194">The `ConfigureAudioStream` function does the following:</span></span>

1.  <span data-ttu-id="9e0c4-195">Chiama il metodo [**IMFSourceReader:: SetStreamSelection**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setstreamselection) per selezionare il flusso audio e deselezionare tutti gli altri flussi.</span><span class="sxs-lookup"><span data-stu-id="9e0c4-195">Calls the [**IMFSourceReader::SetStreamSelection**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setstreamselection) method to select the audio stream and deselect all other streams.</span></span> <span data-ttu-id="9e0c4-196">Questo passaggio può migliorare le prestazioni, in quanto impedisce al lettore di origine di mantenere i frame video non usati dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9e0c4-196">This step can improve performance, because it prevents the source reader from holding onto video frames that the application does not use.</span></span>
2.  <span data-ttu-id="9e0c4-197">Crea un tipo di supporto *parziale* che specifica l'audio PCM.</span><span class="sxs-lookup"><span data-stu-id="9e0c4-197">Creates a *partial* media type that specifies PCM audio.</span></span> <span data-ttu-id="9e0c4-198">La funzione crea il tipo parziale come segue:</span><span class="sxs-lookup"><span data-stu-id="9e0c4-198">The function creates the partial type as follows:</span></span>
    1.  <span data-ttu-id="9e0c4-199">Chiama [**MFCreateMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatype) per creare un oggetto di tipo di supporto vuoto.</span><span class="sxs-lookup"><span data-stu-id="9e0c4-199">Calls [**MFCreateMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatype) to create an empty media type object.</span></span>
    2.  <span data-ttu-id="9e0c4-200">Imposta l'attributo del [**\_ \_ \_ tipo principale MF mt**](mf-mt-major-type-attribute.md) su **MFMediaType \_ audio**.</span><span class="sxs-lookup"><span data-stu-id="9e0c4-200">Sets the [**MF\_MT\_MAJOR\_TYPE**](mf-mt-major-type-attribute.md) attribute to **MFMediaType\_Audio**.</span></span>
    3.  <span data-ttu-id="9e0c4-201">Imposta l'attributo del [**\_ \_ sottotipo MF mt**](mf-mt-subtype-attribute.md) su **MFAudioFormat \_ PCM**.</span><span class="sxs-lookup"><span data-stu-id="9e0c4-201">Sets the [**MF\_MT\_SUBTYPE**](mf-mt-subtype-attribute.md) attribute to **MFAudioFormat\_PCM**.</span></span>
3.  <span data-ttu-id="9e0c4-202">Chiama [**IMFSourceReader:: SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype) per impostare il tipo parziale nel lettore di origine.</span><span class="sxs-lookup"><span data-stu-id="9e0c4-202">Calls [**IMFSourceReader::SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype) to set the partial type on the source reader.</span></span> <span data-ttu-id="9e0c4-203">Se il file di origine contiene audio codificato, il lettore di origine carica automaticamente il decoder audio necessario.</span><span class="sxs-lookup"><span data-stu-id="9e0c4-203">If the source file contains encoded audio, the source reader automatically loads the necessary audio decoder.</span></span>
4.  <span data-ttu-id="9e0c4-204">Chiama [**IMFSourceReader:: GetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getcurrentmediatype) per ottenere il tipo di supporto PCM effettivo.</span><span class="sxs-lookup"><span data-stu-id="9e0c4-204">Calls [**IMFSourceReader::GetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getcurrentmediatype) to get the actual PCM media type.</span></span> <span data-ttu-id="9e0c4-205">Questo metodo restituisce un tipo di supporto con tutti i dettagli di formato compilati, ad esempio la frequenza di campionamento audio e il numero di canali.</span><span class="sxs-lookup"><span data-stu-id="9e0c4-205">This method returns a media type with all of the format details filled in, such as the audio sample rate and the number of channels.</span></span>
5.  <span data-ttu-id="9e0c4-206">Chiama [**IMFSourceReader:: SetStreamSelection**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setstreamselection) per abilitare il flusso audio.</span><span class="sxs-lookup"><span data-stu-id="9e0c4-206">Calls [**IMFSourceReader::SetStreamSelection**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setstreamselection) to enable the audio stream.</span></span>

## <a name="write-the-wave-file-header"></a><span data-ttu-id="9e0c4-207">Scrivere l'intestazione del file WAVE</span><span class="sxs-lookup"><span data-stu-id="9e0c4-207">Write the WAVE File Header</span></span>

<span data-ttu-id="9e0c4-208">La `WriteWaveHeader` funzione scrive l'intestazione del file Wave.</span><span class="sxs-lookup"><span data-stu-id="9e0c4-208">The `WriteWaveHeader` function writes the WAVE file header.</span></span>

<span data-ttu-id="9e0c4-209">L'unica API Media Foundation chiamata da questa funzione è [**MFCreateWaveFormatExFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatewaveformatexfrommfmediatype), che converte il tipo di supporto in una struttura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="9e0c4-209">The only Media Foundation API called from this function is [**MFCreateWaveFormatExFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatewaveformatexfrommfmediatype), which converts the media type to a [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure.</span></span>


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



<span data-ttu-id="9e0c4-210">La `WriteToFile` funzione è una funzione di supporto semplice che esegue il wrapping della funzione **WriteFile** di Windows e restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9e0c4-210">The `WriteToFile` function is a simple helper function that wraps the Windows **WriteFile** function and returns an **HRESULT** value.</span></span>


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



## <a name="calculate-the-maximum-data-size"></a><span data-ttu-id="9e0c4-211">Calcolare la dimensione massima dei dati</span><span class="sxs-lookup"><span data-stu-id="9e0c4-211">Calculate the Maximum Data Size</span></span>

<span data-ttu-id="9e0c4-212">Poiché le dimensioni del file vengono archiviate come valore a 4 byte nell'intestazione del file, un file WAVE è limitato a una dimensione massima di 0xFFFFFFFF byte, circa 4 GB.</span><span class="sxs-lookup"><span data-stu-id="9e0c4-212">Because the file size is stored as a 4-byte value in the file header, a WAVE file is limited to a maximum size of 0xFFFFFFFF bytes—approximately 4 GB.</span></span> <span data-ttu-id="9e0c4-213">Questo valore include le dimensioni dell'intestazione del file.</span><span class="sxs-lookup"><span data-stu-id="9e0c4-213">This value includes the size of the file header.</span></span> <span data-ttu-id="9e0c4-214">L'audio PCM ha una velocità in bit costante, quindi è possibile calcolare le dimensioni massime dei dati dal formato audio, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="9e0c4-214">PCM audio has a constant bit rate, so you can calculate the maximum data size from the audio format, as follows:</span></span>


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



<span data-ttu-id="9e0c4-215">Per evitare i frame audio parziali, la dimensione viene arrotondata all'allineamento del blocco, che è archiviato nell'attributo di [**\_ \_ \_ \_ allineamento a blocchi audio di MF mt**](mf-mt-audio-block-alignment-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="9e0c4-215">To avoid partial audio frames, the size is rounded to the block alignment, which is stored in the [**MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT**](mf-mt-audio-block-alignment-attribute.md) attribute.</span></span>

## <a name="decode-the-audio"></a><span data-ttu-id="9e0c4-216">Decodifica audio</span><span class="sxs-lookup"><span data-stu-id="9e0c4-216">Decode the Audio</span></span>

<span data-ttu-id="9e0c4-217">La `WriteWaveData` funzione legge l'audio decodificato dal file di origine e scrive nel file Wave.</span><span class="sxs-lookup"><span data-stu-id="9e0c4-217">The `WriteWaveData` function reads decoded audio from the source file and writes to the WAVE file.</span></span>


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



<span data-ttu-id="9e0c4-218">La `WriteWaveData` funzione esegue le operazioni seguenti in un ciclo:</span><span class="sxs-lookup"><span data-stu-id="9e0c4-218">The `WriteWaveData` function does the following in a loop:</span></span>

1.  <span data-ttu-id="9e0c4-219">Chiama [**IMFSourceReader:: ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) per leggere l'audio dal file di origine.</span><span class="sxs-lookup"><span data-stu-id="9e0c4-219">Calls [**IMFSourceReader::ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) to read audio from the source file.</span></span> <span data-ttu-id="9e0c4-220">Il parametro *dwFlags* riceve **un operatore OR** bit per bit di flag dall'enumerazione del [**flag del \_ lettore di origine \_ \_ MF**](/windows/desktop/api/mfreadwrite/ne-mfreadwrite-mf_source_reader_flag) .</span><span class="sxs-lookup"><span data-stu-id="9e0c4-220">The *dwFlags* parameter receives a bitwise **OR** of flags from the [**MF\_SOURCE\_READER\_FLAG**](/windows/desktop/api/mfreadwrite/ne-mfreadwrite-mf_source_reader_flag) enumeration.</span></span> <span data-ttu-id="9e0c4-221">Il parametro *pSample* riceve un puntatore all'interfaccia [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) , che viene usata per accedere ai dati audio.</span><span class="sxs-lookup"><span data-stu-id="9e0c4-221">The *pSample* parameter receives a pointer to the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface, which is used to access the audio data.</span></span> <span data-ttu-id="9e0c4-222">In alcuni casi una chiamata a **ReadSample** non genera dati, nel qual caso il puntatore **IMFSample** è **null**.</span><span class="sxs-lookup"><span data-stu-id="9e0c4-222">In some cases a call to **ReadSample** does not generate data, in which case the **IMFSample** pointer is **NULL**.</span></span>
2.  <span data-ttu-id="9e0c4-223">Controlla *dwFlags* per i flag seguenti:</span><span class="sxs-lookup"><span data-stu-id="9e0c4-223">Checks *dwFlags* for the following flags:</span></span>
    -   <span data-ttu-id="9e0c4-224">**MF \_ \_ \_ CURRENTMEDIATYPECHANGED READERF di origine**.</span><span class="sxs-lookup"><span data-stu-id="9e0c4-224">**MF\_SOURCE\_READERF\_CURRENTMEDIATYPECHANGED**.</span></span> <span data-ttu-id="9e0c4-225">Questo flag indica una modifica del formato nel file di origine.</span><span class="sxs-lookup"><span data-stu-id="9e0c4-225">This flag indicates a format change in the source file.</span></span> <span data-ttu-id="9e0c4-226">I file WAVE non supportano le modifiche del formato.</span><span class="sxs-lookup"><span data-stu-id="9e0c4-226">WAVE files do not support format changes.</span></span>
    -   <span data-ttu-id="9e0c4-227">**MF \_ \_ \_ ENDOFSTREAM READERF di origine**.</span><span class="sxs-lookup"><span data-stu-id="9e0c4-227">**MF\_SOURCE\_READERF\_ENDOFSTREAM**.</span></span> <span data-ttu-id="9e0c4-228">Questo flag indica la fine del flusso.</span><span class="sxs-lookup"><span data-stu-id="9e0c4-228">This flag indicates the end of the stream.</span></span>
3.  <span data-ttu-id="9e0c4-229">Chiama [**IMFSample:: ConvertToContiguousBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-converttocontiguousbuffer) per ottenere un puntatore a un oggetto buffer.</span><span class="sxs-lookup"><span data-stu-id="9e0c4-229">Calls [**IMFSample::ConvertToContiguousBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-converttocontiguousbuffer) to get a pointer to a buffer object.</span></span>
4.  <span data-ttu-id="9e0c4-230">Chiama [**IMFMediaBuffer:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) per ottenere un puntatore alla memoria del buffer.</span><span class="sxs-lookup"><span data-stu-id="9e0c4-230">Calls [**IMFMediaBuffer::Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) to get a pointer to the buffer memory.</span></span>
5.  <span data-ttu-id="9e0c4-231">Scrive i dati audio nel file di output.</span><span class="sxs-lookup"><span data-stu-id="9e0c4-231">Writes the audio data to the output file.</span></span>
6.  <span data-ttu-id="9e0c4-232">Chiama [**IMFMediaBuffer:: Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) per sbloccare l'oggetto buffer.</span><span class="sxs-lookup"><span data-stu-id="9e0c4-232">Calls [**IMFMediaBuffer::Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) to unlock the buffer object.</span></span>

<span data-ttu-id="9e0c4-233">La funzione interrompe il ciclo quando si verifica una delle condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="9e0c4-233">The function breaks out of the loop when any of the following occur:</span></span>

-   <span data-ttu-id="9e0c4-234">Il formato del flusso cambia.</span><span class="sxs-lookup"><span data-stu-id="9e0c4-234">The stream format changes.</span></span>
-   <span data-ttu-id="9e0c4-235">È stata raggiunta la fine del flusso.</span><span class="sxs-lookup"><span data-stu-id="9e0c4-235">The end of the stream is reached.</span></span>
-   <span data-ttu-id="9e0c4-236">La quantità massima di dati audio viene scritta nel file di output.</span><span class="sxs-lookup"><span data-stu-id="9e0c4-236">The maximum amount of audio data is written to the output file.</span></span>
-   <span data-ttu-id="9e0c4-237">Si è verificato un errore.</span><span class="sxs-lookup"><span data-stu-id="9e0c4-237">An error occurs.</span></span>

## <a name="finalize-the-file-header"></a><span data-ttu-id="9e0c4-238">Finalizzare l'intestazione del file</span><span class="sxs-lookup"><span data-stu-id="9e0c4-238">Finalize the File Header</span></span>

<span data-ttu-id="9e0c4-239">I valori delle dimensioni archiviati nell'intestazione WAVE non sono noti fino al completamento della funzione precedente.</span><span class="sxs-lookup"><span data-stu-id="9e0c4-239">The size values that are stored in the WAVE header are not known until the previous function completes.</span></span> <span data-ttu-id="9e0c4-240">Il `FixUpChunkSizes` Compila i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="9e0c4-240">The `FixUpChunkSizes` fills in these values:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="9e0c4-241">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9e0c4-241">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9e0c4-242">Tipi di supporti audio</span><span class="sxs-lookup"><span data-stu-id="9e0c4-242">Audio Media Types</span></span>](audio-media-types.md)
</dt> <dt>

[<span data-ttu-id="9e0c4-243">Lettore di origine</span><span class="sxs-lookup"><span data-stu-id="9e0c4-243">Source Reader</span></span>](source-reader.md)
</dt> <dt>

[<span data-ttu-id="9e0c4-244">**IMFSourceReader**</span><span class="sxs-lookup"><span data-stu-id="9e0c4-244">**IMFSourceReader**</span></span>](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader)
</dt> </dl>

 

 
