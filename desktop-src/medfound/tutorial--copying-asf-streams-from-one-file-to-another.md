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
# <a name="tutorial-copying-asf-streams-by-using-wmcontainer-objects"></a><span data-ttu-id="4c2d8-103">Esercitazione: copia di flussi ASF usando oggetti WMContainer</span><span class="sxs-lookup"><span data-stu-id="4c2d8-103">Tutorial: Copying ASF Streams by Using WMContainer Objects</span></span>

<span data-ttu-id="4c2d8-104">Un modo per creare un file ASF consiste nel copiare i flussi ASF da un file esistente.</span><span class="sxs-lookup"><span data-stu-id="4c2d8-104">One way to create an ASF file is to copy ASF streams from an existing file.</span></span> <span data-ttu-id="4c2d8-105">A tale scopo, è possibile recuperare i dati multimediali dal file di origine e scrivere nel file di output.</span><span class="sxs-lookup"><span data-stu-id="4c2d8-105">To do this, you can retrieve the media data from the source file and write to the output file.</span></span> <span data-ttu-id="4c2d8-106">Se il file di origine è un file ASF, è possibile copiare gli esempi di flusso senza decomprimerli e ricomprimerli.</span><span class="sxs-lookup"><span data-stu-id="4c2d8-106">If the source file is an ASF file, you can copy stream samples without decompressing and recompressing them.</span></span>

<span data-ttu-id="4c2d8-107">Questa esercitazione illustra questo scenario estraendo il primo flusso audio da un file audio-video ASF (con estensione WMV) e copiando il file in un nuovo file audio ASF (WMA).</span><span class="sxs-lookup"><span data-stu-id="4c2d8-107">This tutorial demonstrates this scenario by extracting the first audio stream from an ASF audio-video file (.wmv) and copying it to a new ASF audio file (.wma).</span></span> <span data-ttu-id="4c2d8-108">In questa esercitazione verrà creata un'applicazione console che accetta i nomi dei file di input e di output come argomenti.</span><span class="sxs-lookup"><span data-stu-id="4c2d8-108">In this tutorial, you will create a console application that takes the input and output filenames as arguments.</span></span> <span data-ttu-id="4c2d8-109">L'applicazione usa la barra di divisione ASF per analizzare gli esempi di flusso di input e quindi li invia al multiplexer ASF per scrivere i pacchetti di dati ASF per il flusso audio.</span><span class="sxs-lookup"><span data-stu-id="4c2d8-109">The application uses the ASF Splitter to parse the input stream samples and then sends them to the ASF Multiplexer to write the ASF data packets for the audio stream.</span></span>

<span data-ttu-id="4c2d8-110">Questa esercitazione include i passaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="4c2d8-110">This tutorial contains the following steps:</span></span>

-   [<span data-ttu-id="4c2d8-111">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="4c2d8-111">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="4c2d8-112">Terminologia</span><span class="sxs-lookup"><span data-stu-id="4c2d8-112">Terminology</span></span>](#terminology)
-   [<span data-ttu-id="4c2d8-113">1. configurare il progetto</span><span class="sxs-lookup"><span data-stu-id="4c2d8-113">1. Set up the Project</span></span>](#1-set-up-the-project)
-   [<span data-ttu-id="4c2d8-114">2. dichiarare le funzioni helper</span><span class="sxs-lookup"><span data-stu-id="4c2d8-114">2. Declare Helper Functions</span></span>](#2-declare-helper-functions)
-   [<span data-ttu-id="4c2d8-115">3. Aprire il file ASF di input</span><span class="sxs-lookup"><span data-stu-id="4c2d8-115">3. Open the Input ASF File</span></span>](#3-open-the-input-asf-file)
-   [<span data-ttu-id="4c2d8-116">4. inizializzare gli oggetti per il file di input</span><span class="sxs-lookup"><span data-stu-id="4c2d8-116">4. Initialize Objects for the Input File</span></span>](#4-initialize-objects-for-the-input-file)
-   [<span data-ttu-id="4c2d8-117">5. creare un profilo audio</span><span class="sxs-lookup"><span data-stu-id="4c2d8-117">5. Create an Audio Profile</span></span>](#5-create-an-audio-profile)
-   [<span data-ttu-id="4c2d8-118">6. inizializzare gli oggetti per il file di output</span><span class="sxs-lookup"><span data-stu-id="4c2d8-118">6. Initialize Objects for the Output File</span></span>](#6-initialize-objects-for-the-output-file)
-   [<span data-ttu-id="4c2d8-119">7. generare nuovi pacchetti di dati ASF</span><span class="sxs-lookup"><span data-stu-id="4c2d8-119">7. Generate New ASF Data Packets</span></span>](#7-generate-new-asf-data-packets)
-   [<span data-ttu-id="4c2d8-120">8. scrivere gli oggetti ASF nel nuovo file</span><span class="sxs-lookup"><span data-stu-id="4c2d8-120">8. Write the ASF Objects in the New File</span></span>](#8-write-the-asf-objects-in-the-new-file)
-   [<span data-ttu-id="4c2d8-121">9 scrivere la funzione Entry-Point</span><span class="sxs-lookup"><span data-stu-id="4c2d8-121">9 Write the Entry-Point Function</span></span>](#9-write-the-entry-point-function)
-   [<span data-ttu-id="4c2d8-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4c2d8-122">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="4c2d8-123">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="4c2d8-123">Prerequisites</span></span>

<span data-ttu-id="4c2d8-124">Nell’esercitazione si presuppongono le condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="4c2d8-124">This tutorial assumes the following:</span></span>

-   <span data-ttu-id="4c2d8-125">Si ha familiarità con la struttura di un file ASF e i componenti forniti da Media Foundation per lavorare con gli oggetti ASF.</span><span class="sxs-lookup"><span data-stu-id="4c2d8-125">You are familiar with the structure of an ASF file and the components provided by Media Foundation to work with ASF Objects.</span></span> <span data-ttu-id="4c2d8-126">Questi componenti includono oggetti ContentInfo, Splitter, multiplexer e profile.</span><span class="sxs-lookup"><span data-stu-id="4c2d8-126">These components include ContentInfo, splitter, multiplexer, and profile objects.</span></span> <span data-ttu-id="4c2d8-127">Per altre informazioni, vedere [WMCONTAINER ASF Components](wmcontainer-asf-components.md).</span><span class="sxs-lookup"><span data-stu-id="4c2d8-127">For more information, see [WMContainer ASF Components](wmcontainer-asf-components.md).</span></span>
-   <span data-ttu-id="4c2d8-128">Si ha familiarità con il processo di analisi dell'oggetto intestazione ASF e dei pacchetti di dati ASF di un file esistente e di generazione di esempi di flussi compressi tramite la barra di divisione.</span><span class="sxs-lookup"><span data-stu-id="4c2d8-128">You are familiar with the process of parsing the ASF Header Object and the ASF data packets of an existing file and generating compressed stream samples by using the splitter.</span></span> <span data-ttu-id="4c2d8-129">Per ulteriori informazioni [, vedere Esercitazione: lettura di un file ASF](tutorial--reading-an-asf-file.md).</span><span class="sxs-lookup"><span data-stu-id="4c2d8-129">For more information see [Tutorial: Reading an ASF File](tutorial--reading-an-asf-file.md).</span></span>
-   <span data-ttu-id="4c2d8-130">Si ha familiarità con i buffer multimediali e i flussi di byte: in particolare, le operazioni sui file che usano un flusso di byte e la scrittura del contenuto di un buffer multimediale in un flusso di byte.</span><span class="sxs-lookup"><span data-stu-id="4c2d8-130">You are familiar with media buffers and byte streams: Specifically, file operations using a byte stream, and writing the contents of a media buffer into a byte stream.</span></span> <span data-ttu-id="4c2d8-131">(Vedere [2. Dichiarare le funzioni di supporto](#2-declare-helper-functions).</span><span class="sxs-lookup"><span data-stu-id="4c2d8-131">(See [2. Declare Helper Functions](#2-declare-helper-functions).)</span></span>

## <a name="terminology"></a><span data-ttu-id="4c2d8-132">Terminologia</span><span class="sxs-lookup"><span data-stu-id="4c2d8-132">Terminology</span></span>

<span data-ttu-id="4c2d8-133">Questa esercitazione usa i termini seguenti:</span><span class="sxs-lookup"><span data-stu-id="4c2d8-133">This tutorial uses the following terms:</span></span>

-   <span data-ttu-id="4c2d8-134">Flusso di byte di origine: oggetto flusso di byte, espone l'interfaccia [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) , che contiene il contenuto del file di input.</span><span class="sxs-lookup"><span data-stu-id="4c2d8-134">Source byte stream: Byte stream object, exposes [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) interface, which contains the contents of the input file.</span></span>
-   <span data-ttu-id="4c2d8-135">Oggetto ContentInfo di origine: oggetto ContentInfo, espone l'interfaccia [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) , che rappresenta l'oggetto intestazione ASF del file di input.</span><span class="sxs-lookup"><span data-stu-id="4c2d8-135">Source ContentInfo object: ContentInfo object, exposes [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) interface, which represents the ASF Header Object of the input file.</span></span>
-   <span data-ttu-id="4c2d8-136">Profilo audio: oggetto profilo, espone l'interfaccia [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) , che contiene solo flussi audio del file di input.</span><span class="sxs-lookup"><span data-stu-id="4c2d8-136">Audio profile: Profile object, exposes [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) interface, which contains only audio streams of the input file.</span></span>
-   <span data-ttu-id="4c2d8-137">Esempio di flusso: supporto di esempio, espone l'interfaccia [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) , generata dalla barra di divisione che rappresenta i dati multimediali del flusso selezionato ottenuti dal file di input in stato compresso.</span><span class="sxs-lookup"><span data-stu-id="4c2d8-137">Stream sample: Media sample, exposes [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface, generated by the splitter represents the selected stream's media data obtained from the input file in compressed state.</span></span>
-   <span data-ttu-id="4c2d8-138">Output oggetto ContentInfo: oggetto ContentInfo, espone l'interfaccia [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) , che rappresenta l'oggetto intestazione ASF del file di output.</span><span class="sxs-lookup"><span data-stu-id="4c2d8-138">Output ContentInfo object: ContentInfo object, exposes [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) interface, which represents the ASF Header Object of the output file.</span></span>
-   <span data-ttu-id="4c2d8-139">Data byte stream: oggetto flusso di byte, espone l'interfaccia [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) , che rappresenta l'intera parte dell'oggetto dati ASF del file di output.</span><span class="sxs-lookup"><span data-stu-id="4c2d8-139">Data byte stream: Byte stream object, exposes [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) interface, which represents the entire ASF Data Object portion of the output file.</span></span>
-   <span data-ttu-id="4c2d8-140">Pacchetto dati: l'esempio di supporto espone l'interfaccia [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) , generata dal multiplexer, che rappresenta un pacchetto di dati ASF che verrà scritto nel flusso di byte dei dati.</span><span class="sxs-lookup"><span data-stu-id="4c2d8-140">Data packet: Media sample, exposes [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface, generated by the multiplexer represents an ASF data packet that will be written to the data byte stream.</span></span>
-   <span data-ttu-id="4c2d8-141">Flusso di byte di output: oggetto flusso di byte, espone l'interfaccia [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) , che contiene il contenuto del file di output.</span><span class="sxs-lookup"><span data-stu-id="4c2d8-141">Output byte stream: Byte stream object, exposes [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) interface, which contains the contents of the output file.</span></span>

## <a name="1-set-up-the-project"></a><span data-ttu-id="4c2d8-142">1. configurare il progetto</span><span class="sxs-lookup"><span data-stu-id="4c2d8-142">1. Set up the Project</span></span>

<span data-ttu-id="4c2d8-143">Includere le intestazioni seguenti nel file di origine:</span><span class="sxs-lookup"><span data-stu-id="4c2d8-143">Include the following headers in your source file:</span></span>


```C++
#include <stdio.h>       // Standard I/O
#include <windows.h>     // Windows headers
#include <mfapi.h>       // Media Foundation platform
#include <wmcontainer.h> // ASF interfaces
#include <mferror.h>     // Media Foundation error codes
```



<span data-ttu-id="4c2d8-144">Collegamento ai file di libreria seguenti:</span><span class="sxs-lookup"><span data-stu-id="4c2d8-144">Link to the following library files:</span></span>

-   <span data-ttu-id="4c2d8-145">mfplat. lib</span><span class="sxs-lookup"><span data-stu-id="4c2d8-145">mfplat.lib</span></span>
-   <span data-ttu-id="4c2d8-146">MF. lib</span><span class="sxs-lookup"><span data-stu-id="4c2d8-146">mf.lib</span></span>
-   <span data-ttu-id="4c2d8-147">mfuuid. lib</span><span class="sxs-lookup"><span data-stu-id="4c2d8-147">mfuuid.lib</span></span>

<span data-ttu-id="4c2d8-148">Dichiarare la funzione [SafeRelease](saferelease.md) :</span><span class="sxs-lookup"><span data-stu-id="4c2d8-148">Declare the [SafeRelease](saferelease.md) function:</span></span>


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



## <a name="2-declare-helper-functions"></a><span data-ttu-id="4c2d8-149">2. dichiarare le funzioni helper</span><span class="sxs-lookup"><span data-stu-id="4c2d8-149">2. Declare Helper Functions</span></span>

<span data-ttu-id="4c2d8-150">Questa esercitazione usa le funzioni di supporto seguenti per leggere e scrivere da un flusso di byte.</span><span class="sxs-lookup"><span data-stu-id="4c2d8-150">This tutorial uses the following helper functions to read and write from a byte stream.</span></span>

<span data-ttu-id="4c2d8-151">La `AllocReadFromByteStream` funzione legge i dati da un flusso di byte e alloca un nuovo buffer multimediale per conservare i dati.</span><span class="sxs-lookup"><span data-stu-id="4c2d8-151">The `AllocReadFromByteStream` function reads data from a byte stream and allocates a new media buffer to hold the data.</span></span> <span data-ttu-id="4c2d8-152">Per ulteriori informazioni, vedere [**IMFByteStream:: Read**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-read).</span><span class="sxs-lookup"><span data-stu-id="4c2d8-152">For more information, see [**IMFByteStream::Read**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-read).</span></span>


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



<span data-ttu-id="4c2d8-153">La `WriteBufferToByteStream` funzione scrive i dati da un buffer multimediale a un flusso di byte.</span><span class="sxs-lookup"><span data-stu-id="4c2d8-153">The `WriteBufferToByteStream` function writes data from a media buffer to a byte stream.</span></span> <span data-ttu-id="4c2d8-154">Per ulteriori informazioni, vedere [**IMFByteStream:: Write**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-write).</span><span class="sxs-lookup"><span data-stu-id="4c2d8-154">For more information, see [**IMFByteStream::Write**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-write).</span></span>


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



<span data-ttu-id="4c2d8-155">La `AppendToByteStream` funzione aggiunge il contenuto di un flusso di byte a un altro:</span><span class="sxs-lookup"><span data-stu-id="4c2d8-155">The `AppendToByteStream` function appends the contents of one byte stream to another:</span></span>


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



## <a name="3-open-the-input-asf-file"></a><span data-ttu-id="4c2d8-156">3. Aprire il file ASF di input</span><span class="sxs-lookup"><span data-stu-id="4c2d8-156">3. Open the Input ASF File</span></span>

<span data-ttu-id="4c2d8-157">Aprire il file di input chiamando la funzione [**MFCreateFile**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatefile) .</span><span class="sxs-lookup"><span data-stu-id="4c2d8-157">Open the input file by calling the [**MFCreateFile**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatefile) function.</span></span> <span data-ttu-id="4c2d8-158">Il metodo restituisce un puntatore all'oggetto flusso di byte che contiene il contenuto del file.</span><span class="sxs-lookup"><span data-stu-id="4c2d8-158">The method returns a pointer to the byte stream object that contains the contents of the file.</span></span> <span data-ttu-id="4c2d8-159">Il nome file viene specificato dall'utente tramite gli argomenti della riga di comando dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4c2d8-159">The filename is specified by the user through command line arguments of the application.</span></span>

<span data-ttu-id="4c2d8-160">Il codice di esempio seguente accetta un nome di file e restituisce un puntatore a un oggetto flusso di byte che può essere usato per leggere il file.</span><span class="sxs-lookup"><span data-stu-id="4c2d8-160">The following example code takes a file name and returns a pointer to a byte stream object that can be used to read the file.</span></span>


```C++
        // Open the file.
        hr = MFCreateFile(MF_ACCESSMODE_READ, MF_OPENMODE_FAIL_IF_NOT_EXIST, 
            MF_FILEFLAGS_NONE, pszFileName, &pStream);
```



## <a name="4-initialize-objects-for-the-input-file"></a><span data-ttu-id="4c2d8-161">4. inizializzare gli oggetti per il file di input</span><span class="sxs-lookup"><span data-stu-id="4c2d8-161">4. Initialize Objects for the Input File</span></span>

<span data-ttu-id="4c2d8-162">Successivamente, sarà possibile creare e inizializzare l'oggetto ContentInfo di origine e la barra di divisione per generare esempi di flusso.</span><span class="sxs-lookup"><span data-stu-id="4c2d8-162">Next, you will create and initialize the source ContentInfo object and the splitter for generating stream samples.</span></span>

<span data-ttu-id="4c2d8-163">Questo flusso di byte di origine creato nel passaggio 2 verrà usato per analizzare l'oggetto intestazione ASF e popolare l'oggetto ContentInfo di origine.</span><span class="sxs-lookup"><span data-stu-id="4c2d8-163">This source byte stream created in step 2 will be used to parse the ASF Header Object and populate the source ContentInfo object.</span></span> <span data-ttu-id="4c2d8-164">Questo oggetto verrà utilizzato per inizializzare la barra di divisione per semplificare l'analisi dei pacchetti di dati ASF per il flusso audio nel file di input.</span><span class="sxs-lookup"><span data-stu-id="4c2d8-164">This object will be used to initialize the splitter to facilitate the parsing of the ASF data packets for the audio stream in the input file.</span></span> <span data-ttu-id="4c2d8-165">Sarà inoltre possibile recuperare la lunghezza dell'oggetto dati ASF nel file di input e l'offset al primo pacchetto di dati ASF relativo all'inizio del file.</span><span class="sxs-lookup"><span data-stu-id="4c2d8-165">You will also retrieve the length of the ASF Data Object in the input file and the offset to the first ASF data packet relative to the start of the file.</span></span> <span data-ttu-id="4c2d8-166">Questi attributi verranno usati dalla barra di divisione per generare esempi di flusso audio.</span><span class="sxs-lookup"><span data-stu-id="4c2d8-166">These attributes will be used by the splitter to generate audio stream samples.</span></span>

<span data-ttu-id="4c2d8-167">Per creare e inizializzare i componenti ASF per il file di input:</span><span class="sxs-lookup"><span data-stu-id="4c2d8-167">To create and initialize ASF components for the input file:</span></span>

1.  <span data-ttu-id="4c2d8-168">Chiamare [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) per creare l'oggetto ContentInfo.</span><span class="sxs-lookup"><span data-stu-id="4c2d8-168">Call [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) to create the ContentInfo object.</span></span> <span data-ttu-id="4c2d8-169">Questa funzione restituisce un puntatore all'interfaccia [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) .</span><span class="sxs-lookup"><span data-stu-id="4c2d8-169">This function returns a pointer to the [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) interface.</span></span>
2.  <span data-ttu-id="4c2d8-170">Chiamare [**IMFASFContentInfo::P arseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) per analizzare l'intestazione ASF.</span><span class="sxs-lookup"><span data-stu-id="4c2d8-170">Call [**IMFASFContentInfo::ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) to parse the ASF Header.</span></span> <span data-ttu-id="4c2d8-171">Per ulteriori informazioni su questo passaggio, vedere [lettura dell'oggetto intestazione ASF di un file esistente](reading-the-asf-header-object-of-an-existing-file.md).</span><span class="sxs-lookup"><span data-stu-id="4c2d8-171">For more information about this step, see [Reading the ASF Header Object of an Existing File](reading-the-asf-header-object-of-an-existing-file.md).</span></span>
3.  <span data-ttu-id="4c2d8-172">Chiamare [**MFCreateASFSplitter**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfsplitter) per creare l'oggetto Splitter ASF.</span><span class="sxs-lookup"><span data-stu-id="4c2d8-172">Call [**MFCreateASFSplitter**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfsplitter) to create the ASF splitter object.</span></span> <span data-ttu-id="4c2d8-173">Questa funzione restituisce un puntatore all'interfaccia [**IMFASFSplitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) .</span><span class="sxs-lookup"><span data-stu-id="4c2d8-173">This function returns a pointer to the [**IMFASFSplitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) interface.</span></span>
4.  <span data-ttu-id="4c2d8-174">Chiamare [**IMFASFSplitter:: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize), passando il puntatore [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo).</span><span class="sxs-lookup"><span data-stu-id="4c2d8-174">Call [**IMFASFSplitter::Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize), passing in the [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo)pointer.</span></span> <span data-ttu-id="4c2d8-175">Per ulteriori informazioni su questo passaggio, vedere [Creating the ASF Splitter Object](creating-the-asf-splitter-object.md).</span><span class="sxs-lookup"><span data-stu-id="4c2d8-175">For more information about this step, see [Creating the ASF Splitter Object](creating-the-asf-splitter-object.md).</span></span>
5.  <span data-ttu-id="4c2d8-176">Chiamare [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) per ottenere un descrittore di presentazione per il file ASF.</span><span class="sxs-lookup"><span data-stu-id="4c2d8-176">Call [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) to get a presentation descriptor for the ASF file.</span></span>
6.  <span data-ttu-id="4c2d8-177">Ottenere il valore dell'attributo [**MF \_ PD \_ ASF \_ data \_ Start \_ offset**](mf-pd-asf-data-start-offset-attribute.md) dal descrittore della presentazione.</span><span class="sxs-lookup"><span data-stu-id="4c2d8-177">Get the value of the [**MF\_PD\_ASF\_DATA\_START\_OFFSET**](mf-pd-asf-data-start-offset-attribute.md) attribute from the presentation descriptor.</span></span> <span data-ttu-id="4c2d8-178">Questo valore è il percorso dell'oggetto dati ASF nel file, come offset di byte dall'inizio del file.</span><span class="sxs-lookup"><span data-stu-id="4c2d8-178">This value is the location of the ASF Data Object in the file, as a byte offset from the start of the file.</span></span>
7.  <span data-ttu-id="4c2d8-179">Ottenere il valore dell'attributo [**di \_ \_ lunghezza dei \_ dati \_ MF PD ASF**](mf-pd-asf-data-length-attribute.md) dal descrittore della presentazione.</span><span class="sxs-lookup"><span data-stu-id="4c2d8-179">Get the value of the [**MF\_PD\_ASF\_DATA\_LENGTH**](mf-pd-asf-data-length-attribute.md) attribute from the presentation descriptor.</span></span> <span data-ttu-id="4c2d8-180">Questo valore corrisponde alle dimensioni totali dell'oggetto dati ASF, in byte.</span><span class="sxs-lookup"><span data-stu-id="4c2d8-180">This value is the total size of the ASF Data Object, in bytes.</span></span> <span data-ttu-id="4c2d8-181">Per ulteriori informazioni, vedere [recupero di informazioni da oggetti intestazione ASF](getting-information-from-asf-header-objects.md).</span><span class="sxs-lookup"><span data-stu-id="4c2d8-181">For more information, see [Getting Information from ASF Header Objects](getting-information-from-asf-header-objects.md).</span></span>

<span data-ttu-id="4c2d8-182">Nell'esempio di codice seguente viene illustrata una funzione che consolida tutti i passaggi.</span><span class="sxs-lookup"><span data-stu-id="4c2d8-182">The following example code shows a function that consolidates all of the steps.</span></span> <span data-ttu-id="4c2d8-183">Questa funzione accetta un puntatore al flusso di byte di origine e restituisce i puntatori all'oggetto ContentInfo di origine e alla barra di divisione.</span><span class="sxs-lookup"><span data-stu-id="4c2d8-183">This function takes a pointer to the source byte stream and returns pointers to the source ContentInfo object and the splitter.</span></span> <span data-ttu-id="4c2d8-184">Inoltre, riceve la lunghezza e gli offset nell'oggetto dati ASF.</span><span class="sxs-lookup"><span data-stu-id="4c2d8-184">Also, it receives the length and offsets to the ASF Data Object.</span></span>


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



## <a name="5-create-an-audio-profile"></a><span data-ttu-id="4c2d8-185">5. creare un profilo audio</span><span class="sxs-lookup"><span data-stu-id="4c2d8-185">5. Create an Audio Profile</span></span>

<span data-ttu-id="4c2d8-186">Successivamente, si creerà un oggetto profilo per il file di input ottenendolo dall'oggetto ContentInfo di origine.</span><span class="sxs-lookup"><span data-stu-id="4c2d8-186">Next, you will create a profile object for the input file by obtaining it from the source ContentInfo object.</span></span> <span data-ttu-id="4c2d8-187">Il profilo verrà quindi configurato in modo che contenga solo i flussi audio del file di input.</span><span class="sxs-lookup"><span data-stu-id="4c2d8-187">You will then configure the profile so that it contains only the audio streams of the input file.</span></span> <span data-ttu-id="4c2d8-188">A tale scopo, enumerare i flussi e rimuovere i flussi non audio dal profilo.</span><span class="sxs-lookup"><span data-stu-id="4c2d8-188">To do this, enumerate the streams and remove non-audio streams from the profile.</span></span> <span data-ttu-id="4c2d8-189">L'oggetto profilo audio verrà usato più avanti in questa esercitazione per inizializzare l'oggetto ContentInfo di output.</span><span class="sxs-lookup"><span data-stu-id="4c2d8-189">The audio profile object will be used later in this tutorial to initialize the output ContentInfo object.</span></span>

<span data-ttu-id="4c2d8-190">Per creare un profilo audio</span><span class="sxs-lookup"><span data-stu-id="4c2d8-190">To create an audio profile</span></span>

1.  <span data-ttu-id="4c2d8-191">Ottenere l'oggetto profilo per il file di input dall'oggetto ContentInfo di origine chiamando [**IMFASFContentInfo:: GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile).</span><span class="sxs-lookup"><span data-stu-id="4c2d8-191">Get the profile object for the input file from the source ContentInfo object by calling [**IMFASFContentInfo::GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile).</span></span> <span data-ttu-id="4c2d8-192">Il metodo restituisce un puntatore a un oggetto profilo che contiene tutti i flussi nel file di input.</span><span class="sxs-lookup"><span data-stu-id="4c2d8-192">The method returns a pointer to a profile object that contains all of the streams in the input file.</span></span> <span data-ttu-id="4c2d8-193">Per ulteriori informazioni, vedere [creazione di un profilo ASF](creating-an-asf-profile.md).</span><span class="sxs-lookup"><span data-stu-id="4c2d8-193">For more information see [Creating an ASF Profile](creating-an-asf-profile.md).</span></span>
2.  <span data-ttu-id="4c2d8-194">Rimuovere gli oggetti di esclusione reciproca dal profilo.</span><span class="sxs-lookup"><span data-stu-id="4c2d8-194">Remove any mutual exclusion objects from the profile.</span></span> <span data-ttu-id="4c2d8-195">Questo passaggio è necessario perché i flussi non audio verranno rimossi dal profilo, che potrebbero invalidare gli oggetti di esclusione reciproca.</span><span class="sxs-lookup"><span data-stu-id="4c2d8-195">This step is required because non-audio streams will be removed from the profile, which could invalidate the mutual exclusion objects.</span></span>
3.  <span data-ttu-id="4c2d8-196">Rimuovere tutti i flussi non audio dal profilo, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="4c2d8-196">Remove all non-audio streams from the profile, as follows:</span></span>
    -   <span data-ttu-id="4c2d8-197">Chiamare [**IMFASFProfile:: GetStreamCount**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamcount) per ottenere il numero di flussi.</span><span class="sxs-lookup"><span data-stu-id="4c2d8-197">Call [**IMFASFProfile::GetStreamCount**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamcount) to get the number of streams.</span></span>
    -   <span data-ttu-id="4c2d8-198">In un ciclo, chiamare [**IMFASFProfile:: GetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream) per ottenere ogni flusso in base all'indice.</span><span class="sxs-lookup"><span data-stu-id="4c2d8-198">In a loop, call [**IMFASFProfile::GetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream) to get each stream by index.</span></span>
    -   <span data-ttu-id="4c2d8-199">Chiamare [**IMFASFStreamConfig:: GetStreamType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getstreamtype) per ottenere il tipo di flusso.</span><span class="sxs-lookup"><span data-stu-id="4c2d8-199">Call [**IMFASFStreamConfig::GetStreamType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getstreamtype) to get the stream type.</span></span>
    -   <span data-ttu-id="4c2d8-200">Per i flussi non audio, chiamare [**IMFASFProfile:: RemoveStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removestream) per rimuovere il flusso.</span><span class="sxs-lookup"><span data-stu-id="4c2d8-200">For non-audio streams, call [**IMFASFProfile::RemoveStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removestream) to remove the stream.</span></span>
4.  <span data-ttu-id="4c2d8-201">Archiviare il numero di flusso del primo flusso audio.</span><span class="sxs-lookup"><span data-stu-id="4c2d8-201">Store the stream number of the first audio stream.</span></span> <span data-ttu-id="4c2d8-202">Questo verrà selezionato nella barra di divisione per generare esempi di flusso.</span><span class="sxs-lookup"><span data-stu-id="4c2d8-202">This will be selected on the splitter to generate stream samples.</span></span> <span data-ttu-id="4c2d8-203">Se il numero del flusso è zero, il chiamante può presumere che non esistano file di flussi audio.</span><span class="sxs-lookup"><span data-stu-id="4c2d8-203">If the stream number is zero, the caller can assume that there were no audio streams file.</span></span>

<span data-ttu-id="4c2d8-204">Il codice seguente illustra questi passaggi:</span><span class="sxs-lookup"><span data-stu-id="4c2d8-204">The following code these steps:</span></span>


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



<span data-ttu-id="4c2d8-205">La `RemoveMutexes` funzione rimuove gli oggetti di esclusione reciproca dal profilo:</span><span class="sxs-lookup"><span data-stu-id="4c2d8-205">The `RemoveMutexes` function removes any mutual exclusion objects from the profile:</span></span>


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



## <a name="6-initialize-objects-for-the-output-file"></a><span data-ttu-id="4c2d8-206">6. inizializzare gli oggetti per il file di output</span><span class="sxs-lookup"><span data-stu-id="4c2d8-206">6. Initialize Objects for the Output File</span></span>

<span data-ttu-id="4c2d8-207">Successivamente, si creerà l'oggetto ContentInfo di output e il multiplexer per la generazione dei pacchetti di dati per il file di output.</span><span class="sxs-lookup"><span data-stu-id="4c2d8-207">Next, you will create the output ContentInfo object and the multiplexer for generating data packets for the output file.</span></span>

<span data-ttu-id="4c2d8-208">Il profilo audio creato nel passaggio 4 verrà usato per popolare l'oggetto ContentInfo di output.</span><span class="sxs-lookup"><span data-stu-id="4c2d8-208">The audio profile created in step 4 will be used to populate the output ContentInfo object.</span></span> <span data-ttu-id="4c2d8-209">Questo oggetto contiene informazioni quali gli attributi di file globali e le proprietà del flusso.</span><span class="sxs-lookup"><span data-stu-id="4c2d8-209">This object contains information such as global file attributes and stream properties.</span></span> <span data-ttu-id="4c2d8-210">L'oggetto ContentInfo di output verrà usato per inizializzare il multiplexer che genererà i pacchetti di dati per il file di output.</span><span class="sxs-lookup"><span data-stu-id="4c2d8-210">The output ContentInfo object will be used to initialize the multiplexer that will generate data packets for the output file.</span></span> <span data-ttu-id="4c2d8-211">Dopo la generazione dei pacchetti di dati, l'oggetto ContentInfo deve essere aggiornato in modo da riflettere i nuovi valori.</span><span class="sxs-lookup"><span data-stu-id="4c2d8-211">After the data packets are generated, the ContentInfo object must be updated to reflect the new values.</span></span>

<span data-ttu-id="4c2d8-212">Per creare e inizializzare i componenti ASF per il file di output</span><span class="sxs-lookup"><span data-stu-id="4c2d8-212">To create and initialize ASF components for the output file</span></span>

1.  <span data-ttu-id="4c2d8-213">Creare un oggetto ContentInfo vuoto chiamando [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) e popolarlo con le informazioni del profilo audio creato nel passaggio 3 chiamando [**IMFASFContentInfo:: seprofile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile).</span><span class="sxs-lookup"><span data-stu-id="4c2d8-213">Create an empty ContentInfo object by calling [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) and populate it with information from the audio profile created in step 3 by calling [**IMFASFContentInfo::SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile).</span></span> <span data-ttu-id="4c2d8-214">Per ulteriori informazioni, vedere [inizializzazione dell'oggetto ContentInfo di un nuovo file ASF](initializing-the-contentinfo-object-of-a-new-asf-file.md).</span><span class="sxs-lookup"><span data-stu-id="4c2d8-214">For more information, see [Initializing the ContentInfo Object of a New ASF File](initializing-the-contentinfo-object-of-a-new-asf-file.md).</span></span>
2.  <span data-ttu-id="4c2d8-215">Creare e inizializzare l'oggetto multiplexer usando l'oggetto ContentInfo di output.</span><span class="sxs-lookup"><span data-stu-id="4c2d8-215">Create and initialize the multiplexer object by using the output ContentInfo object.</span></span> <span data-ttu-id="4c2d8-216">Per ulteriori informazioni, vedere [creazione dell'oggetto multiplexer](creating-the-multiplexer-object.md).</span><span class="sxs-lookup"><span data-stu-id="4c2d8-216">For more information, see [Creating the Multiplexer Object](creating-the-multiplexer-object.md).</span></span>

<span data-ttu-id="4c2d8-217">Nell'esempio di codice seguente viene illustrata una funzione che consolida i passaggi.</span><span class="sxs-lookup"><span data-stu-id="4c2d8-217">The following example code shows a function that consolidates the steps.</span></span> <span data-ttu-id="4c2d8-218">Questa funzione accetta un puntatore a un oggetto profilo e restituisce i puntatori all'oggetto ContentInfo di output e al multiplexer.</span><span class="sxs-lookup"><span data-stu-id="4c2d8-218">This function takes a pointer to a profile object and returns pointers to the output ContentInfo object and the multiplexer.</span></span>


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



## <a name="7-generate-new-asf-data-packets"></a><span data-ttu-id="4c2d8-219">7. generare nuovi pacchetti di dati ASF</span><span class="sxs-lookup"><span data-stu-id="4c2d8-219">7. Generate New ASF Data Packets</span></span>

<span data-ttu-id="4c2d8-220">Successivamente, si genereranno esempi di flusso audio dal flusso di byte di origine usando la barra di divisione e li invierà al multiplexer per creare pacchetti di dati ASF.</span><span class="sxs-lookup"><span data-stu-id="4c2d8-220">Next, you will generate audio stream samples from the source byte stream by using the splitter and send them to the multiplexer to create ASF data packets.</span></span> <span data-ttu-id="4c2d8-221">Questi pacchetti di dati costituiranno l'oggetto dati ASF finale per il nuovo file.</span><span class="sxs-lookup"><span data-stu-id="4c2d8-221">These data packets will constitute the final ASF Data Object for the new file.</span></span>

<span data-ttu-id="4c2d8-222">Per generare esempi di flusso audio</span><span class="sxs-lookup"><span data-stu-id="4c2d8-222">To generate audio stream samples</span></span>

1.  <span data-ttu-id="4c2d8-223">Selezionare il primo flusso audio nella barra di divisione chiamando [**IMFASFSplitter:: SelectStreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-selectstreams).</span><span class="sxs-lookup"><span data-stu-id="4c2d8-223">Select the first audio stream on the splitter by calling [**IMFASFSplitter::SelectStreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-selectstreams).</span></span>
2.  <span data-ttu-id="4c2d8-224">Legge i blocchi a dimensione fissa dei dati multimediali dal flusso di byte di origine in un buffer multimediale.</span><span class="sxs-lookup"><span data-stu-id="4c2d8-224">Read fixed-size blocks of media data from the source byte stream into a media buffer.</span></span>
3.  <span data-ttu-id="4c2d8-225">Raccogliere gli esempi di flusso come esempi di supporti dalla barra di divisione chiamando [**IMFASFSplitter:: GetNextSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample) in un ciclo, purché riceva il \_ flag ASF STATUSFLAGS \_ incomplete nel parametro *pdwStatusFlags* .</span><span class="sxs-lookup"><span data-stu-id="4c2d8-225">Collect the stream samples as media samples from the splitter by calling [**IMFASFSplitter::GetNextSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample) in a loop as long as it receives the ASF\_STATUSFLAGS\_INCOMPLETE flag in the *pdwStatusFlags* parameter.</span></span> <span data-ttu-id="4c2d8-226">Per ulteriori informazioni, vedere generazione di esempi per i pacchetti di dati ASF in [generazione di esempi di flusso da un oggetto dati ASF esistente](generating-stream-samples-from-an-existing-asf-data-object.md).</span><span class="sxs-lookup"><span data-stu-id="4c2d8-226">For more information, see Generating Samples for ASF Data Packets" in [Generating Stream Samples from an Existing ASF Data Object](generating-stream-samples-from-an-existing-asf-data-object.md).</span></span>
4.  <span data-ttu-id="4c2d8-227">Per ogni esempio di supporto, chiamare [**IMFASFMultiplexer::P rocesssample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) per inviare l'esempio multimediale al multiplexer.</span><span class="sxs-lookup"><span data-stu-id="4c2d8-227">For each media sample, call [**IMFASFMultiplexer::ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) to send the media sample to the multiplexer.</span></span> <span data-ttu-id="4c2d8-228">Il multiplexer genera i pacchetti di dati per l'oggetto dati ASF.</span><span class="sxs-lookup"><span data-stu-id="4c2d8-228">The multiplexer generates the data packets for the ASF Data Object.</span></span>
5.  <span data-ttu-id="4c2d8-229">Scrivere il pacchetto di dati generato dal multiplexer nel flusso di byte di dati.</span><span class="sxs-lookup"><span data-stu-id="4c2d8-229">Write the data packet generated by the multiplexer to the data byte stream.</span></span>
6.  <span data-ttu-id="4c2d8-230">Dopo aver generato tutti i pacchetti di dati, chiamare [**IMFASFMultiplexer:: end**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-end) per aggiornare l'oggetto ContentInfo di output con le informazioni raccolte durante la generazione del pacchetto di dati ASF.</span><span class="sxs-lookup"><span data-stu-id="4c2d8-230">After all the data packets have been generated, call [**IMFASFMultiplexer::End**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-end) to update the output ContentInfo object with information collected during ASF data packet generation.</span></span>

<span data-ttu-id="4c2d8-231">Il codice di esempio seguente genera esempi di flusso dal separatore ASF e li invia al multiplexer.</span><span class="sxs-lookup"><span data-stu-id="4c2d8-231">The following example code generates stream samples from the ASF splitter and sends them to the multiplexer.</span></span> <span data-ttu-id="4c2d8-232">Il multiplexer genera pacchetti di dati ASF e li scrive in un flusso.</span><span class="sxs-lookup"><span data-stu-id="4c2d8-232">The multiplexer generates ASF data packets and writes it to a stream.</span></span>


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



<span data-ttu-id="4c2d8-233">Per ottenere i pacchetti dal separatore ASF, il codice precedente chiama la `GetPacketsFromSplitter` funzione, mostrata di seguito:</span><span class="sxs-lookup"><span data-stu-id="4c2d8-233">To get packets from the ASF splitter, the previous code calls the `GetPacketsFromSplitter` function, shown here:</span></span>


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



<span data-ttu-id="4c2d8-234">La `GenerateDataPackets` funzione ottiene i pacchetti di dati da multiplexer.</span><span class="sxs-lookup"><span data-stu-id="4c2d8-234">The `GenerateDataPackets` function gets data packets from multiplexer.</span></span> <span data-ttu-id="4c2d8-235">Per ulteriori informazioni, vedere [recupero di pacchetti di dati ASF](generating-new-asf-data-packets.md).</span><span class="sxs-lookup"><span data-stu-id="4c2d8-235">For more information, see [Getting ASF Data Packets](generating-new-asf-data-packets.md).</span></span>


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



## <a name="8-write-the-asf-objects-in-the-new-file"></a><span data-ttu-id="4c2d8-236">8. scrivere gli oggetti ASF nel nuovo file</span><span class="sxs-lookup"><span data-stu-id="4c2d8-236">8. Write the ASF Objects in the New File</span></span>

<span data-ttu-id="4c2d8-237">Successivamente, si scriverà il contenuto dell'oggetto ContentInfo di output in un buffer multimediale chiamando [**IMFASFContentInfo:: GenerateHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader).</span><span class="sxs-lookup"><span data-stu-id="4c2d8-237">Next, you will write the contents of the output ContentInfo object to a media buffer by calling [**IMFASFContentInfo::GenerateHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader).</span></span> <span data-ttu-id="4c2d8-238">Questo metodo converte i dati archiviati nell'oggetto ContentInfo in dati binari nel formato dell'oggetto intestazione ASF.</span><span class="sxs-lookup"><span data-stu-id="4c2d8-238">This method converts data stored in the ContentInfo object into binary data in ASF Header Object format.</span></span> <span data-ttu-id="4c2d8-239">Per ulteriori informazioni, vedere [generazione di un nuovo oggetto intestazione ASF](generating-a-new-asf-header-object.md).</span><span class="sxs-lookup"><span data-stu-id="4c2d8-239">For more information, see [Generating a New ASF Header Object](generating-a-new-asf-header-object.md).</span></span>

<span data-ttu-id="4c2d8-240">Dopo la generazione del nuovo oggetto intestazione ASF, scrivere il file di output scrivendo prima l'oggetto Header nel flusso di byte di output creato nel passaggio 2 chiamando la funzione di supporto WriteBufferToByteStream.</span><span class="sxs-lookup"><span data-stu-id="4c2d8-240">After the new ASF Header Object has been generated, write the output file by first writing the Header Object to the output byte stream created in step 2 by calling the helper function WriteBufferToByteStream.</span></span> <span data-ttu-id="4c2d8-241">Seguire l'oggetto Header con l'oggetto dati contenuto nel flusso di byte di dati.</span><span class="sxs-lookup"><span data-stu-id="4c2d8-241">Follow the Header Object with the Data Object contained in the data byte stream.</span></span> <span data-ttu-id="4c2d8-242">Nel codice di esempio viene illustrata una funzione che trasferisce il contenuto del flusso di byte di dati al flusso di byte di output.</span><span class="sxs-lookup"><span data-stu-id="4c2d8-242">The example code shows a function that transfers contents of the data bytes stream to the output byte stream.</span></span>


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



## <a name="9-write-the-entry-point-function"></a><span data-ttu-id="4c2d8-243">9 scrivere la funzione Entry-Point</span><span class="sxs-lookup"><span data-stu-id="4c2d8-243">9 Write the Entry-Point Function</span></span>

<span data-ttu-id="4c2d8-244">È ora possibile inserire i passaggi precedenti in un'applicazione completa.</span><span class="sxs-lookup"><span data-stu-id="4c2d8-244">Now you can put the previous steps together into a complete application.</span></span> <span data-ttu-id="4c2d8-245">Prima di usare uno degli oggetti Media Foundation, inizializzare la piattaforma Media Foundation chiamando [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup).</span><span class="sxs-lookup"><span data-stu-id="4c2d8-245">Before using any of the Media Foundation objects, initialize the Media Foundation platform by calling [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup).</span></span> <span data-ttu-id="4c2d8-246">Al termine, chiamare [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown).</span><span class="sxs-lookup"><span data-stu-id="4c2d8-246">When you are done, call [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown).</span></span> <span data-ttu-id="4c2d8-247">Per ulteriori informazioni, vedere [inizializzazione di Media Foundation](initializing-media-foundation.md).</span><span class="sxs-lookup"><span data-stu-id="4c2d8-247">For more information, see [Initializing Media Foundation](initializing-media-foundation.md).</span></span>

<span data-ttu-id="4c2d8-248">Nel codice seguente viene illustrata l'applicazione console completa.</span><span class="sxs-lookup"><span data-stu-id="4c2d8-248">The following code shows the complete console application.</span></span> <span data-ttu-id="4c2d8-249">L'argomento della riga di comando specifica il nome del file da convertire e il nome del nuovo file audio.</span><span class="sxs-lookup"><span data-stu-id="4c2d8-249">The command-line argument specifies the name of the file to convert and the name of the new audio file.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="4c2d8-250">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4c2d8-250">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c2d8-251">Componenti ASF WMContainer</span><span class="sxs-lookup"><span data-stu-id="4c2d8-251">WMContainer ASF Components</span></span>](wmcontainer-asf-components.md)
</dt> <dt>

[<span data-ttu-id="4c2d8-252">Supporto ASF in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4c2d8-252">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



