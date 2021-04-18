---
description: Questa esercitazione illustra come ottenere pacchetti di dati da un file ASF (Advanced Systems Format) usando il separatore ASF.
ms.assetid: e3a55275-e8f0-4ab7-98db-a2f2c54d5a51
title: 'Esercitazione: lettura di un file ASF usando oggetti WMContainer'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0225f434f650f0423771122e6fc345022e69ec1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310188"
---
# <a name="tutorial-reading-an-asf-file-by-using-wmcontainer-objects"></a><span data-ttu-id="c75d7-103">Esercitazione: lettura di un file ASF usando oggetti WMContainer</span><span class="sxs-lookup"><span data-stu-id="c75d7-103">Tutorial: Reading an ASF File by Using WMContainer Objects</span></span>

<span data-ttu-id="c75d7-104">Questa esercitazione illustra come ottenere pacchetti di dati da un file ASF (Advanced Systems Format) usando il [separatore ASF](asf-splitter.md).</span><span class="sxs-lookup"><span data-stu-id="c75d7-104">This tutorial shows how to get data packets from an Advanced Systems Format (ASF) file using the [ASF Splitter](asf-splitter.md).</span></span> <span data-ttu-id="c75d7-105">In questa esercitazione verrà creata una semplice applicazione console che legge un file ASF e genera esempi di supporti compressi per il primo flusso video nel file.</span><span class="sxs-lookup"><span data-stu-id="c75d7-105">In this tutorial, you will create a simple console application that reads an ASF file and generates compressed media samples for the first video stream in the file.</span></span> <span data-ttu-id="c75d7-106">L'applicazione Visualizza informazioni sui fotogrammi chiave nel flusso video.</span><span class="sxs-lookup"><span data-stu-id="c75d7-106">The application displays information about the key frames in the video stream.</span></span>

<span data-ttu-id="c75d7-107">Questa esercitazione include i passaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="c75d7-107">This tutorial contains the following steps:</span></span>

-   [<span data-ttu-id="c75d7-108">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="c75d7-108">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="c75d7-109">1. configurare il progetto</span><span class="sxs-lookup"><span data-stu-id="c75d7-109">1. Set up the Project</span></span>](#1-set-up-the-project)
-   [<span data-ttu-id="c75d7-110">2. aprire un file ASF</span><span class="sxs-lookup"><span data-stu-id="c75d7-110">2. Open an ASF File</span></span>](#2-open-an-asf-file)
-   [<span data-ttu-id="c75d7-111">3. leggere l'oggetto intestazione ASF</span><span class="sxs-lookup"><span data-stu-id="c75d7-111">3. Read the ASF Header Object</span></span>](#3-read-the-asf-header-object)
-   [<span data-ttu-id="c75d7-112">4. creare il separatore ASF</span><span class="sxs-lookup"><span data-stu-id="c75d7-112">4. Create the ASF Splitter</span></span>](#4-create-the-asf-splitter)
-   [<span data-ttu-id="c75d7-113">5. Selezionare un flusso per l'analisi</span><span class="sxs-lookup"><span data-stu-id="c75d7-113">5. Select a Stream for Parsing</span></span>](#5-select-a-stream-for-parsing)
-   [<span data-ttu-id="c75d7-114">6. generare esempi di supporti compressi</span><span class="sxs-lookup"><span data-stu-id="c75d7-114">6. Generate Compressed Media Samples</span></span>](#6-generate-compressed-media-samples)
-   [<span data-ttu-id="c75d7-115">7. scrivere la funzione Entry-Point</span><span class="sxs-lookup"><span data-stu-id="c75d7-115">7. Write the Entry-Point Function</span></span>](#7-write-the-entry-point-function)
-   [<span data-ttu-id="c75d7-116">Elenco programmi</span><span class="sxs-lookup"><span data-stu-id="c75d7-116">Program Listing</span></span>](#program-listing)
-   [<span data-ttu-id="c75d7-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c75d7-117">Related topics</span></span>](#related-topics)

<span data-ttu-id="c75d7-118">Nell'esercitazione non viene illustrato come decodificare i dati compressi che l'applicazione ottiene dal separatore ASF.</span><span class="sxs-lookup"><span data-stu-id="c75d7-118">The tutorial does not cover how to decode the compressed data that the application gets from the ASF splitter.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="c75d7-119">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="c75d7-119">Prerequisites</span></span>

<span data-ttu-id="c75d7-120">Nell’esercitazione si presuppongono le condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="c75d7-120">This tutorial assumes the following:</span></span>

-   <span data-ttu-id="c75d7-121">Si ha familiarità con la struttura di un file ASF e i componenti forniti da Media Foundation per lavorare con gli oggetti ASF.</span><span class="sxs-lookup"><span data-stu-id="c75d7-121">You are familiar with the structure of an ASF file and the components provided by Media Foundation to work with ASF Objects.</span></span> <span data-ttu-id="c75d7-122">Questi componenti includono l'oggetto ContentInfo, la barra di divisione, il multiplexer e il profilo.</span><span class="sxs-lookup"><span data-stu-id="c75d7-122">These components include the ContentInfo object, splitter, multiplexer, and profile.</span></span> <span data-ttu-id="c75d7-123">Per altre informazioni, vedere [WMCONTAINER ASF Components](wmcontainer-asf-components.md).</span><span class="sxs-lookup"><span data-stu-id="c75d7-123">For more information, see [WMContainer ASF Components](wmcontainer-asf-components.md).</span></span>
-   <span data-ttu-id="c75d7-124">Si ha familiarità con i [buffer multimediali](media-buffers.md) e i flussi di byte: in particolare, le operazioni sui file che usano un flusso di byte, la lettura da un flusso di byte in un buffer multimediale e la scrittura del contenuto di un buffer multimediale in un flusso di byte.</span><span class="sxs-lookup"><span data-stu-id="c75d7-124">You are familiar with [Media Buffers](media-buffers.md) and byte streams: Specifically, file operations using a byte stream, reading from a byte stream into a media buffer, and writing the contents of a media buffer to a byte stream.</span></span>

## <a name="1-set-up-the-project"></a><span data-ttu-id="c75d7-125">1. configurare il progetto</span><span class="sxs-lookup"><span data-stu-id="c75d7-125">1. Set up the Project</span></span>

<span data-ttu-id="c75d7-126">Includere le intestazioni seguenti nel file di origine:</span><span class="sxs-lookup"><span data-stu-id="c75d7-126">Include the following headers in your source file:</span></span>


```C++
#include <stdio.h>       // Standard I/O
#include <windows.h>     // Windows headers
#include <mfapi.h>       // Media Foundation platform
#include <wmcontainer.h> // ASF interfaces
#include <Mferror.h>
```



<span data-ttu-id="c75d7-127">Collegamento ai file di libreria seguenti:</span><span class="sxs-lookup"><span data-stu-id="c75d7-127">Link to the following library files:</span></span>

-   <span data-ttu-id="c75d7-128">mfplat. lib</span><span class="sxs-lookup"><span data-stu-id="c75d7-128">mfplat.lib</span></span>
-   <span data-ttu-id="c75d7-129">MF. lib</span><span class="sxs-lookup"><span data-stu-id="c75d7-129">mf.lib</span></span>
-   <span data-ttu-id="c75d7-130">mfuuid. lib</span><span class="sxs-lookup"><span data-stu-id="c75d7-130">mfuuid.lib</span></span>

<span data-ttu-id="c75d7-131">Dichiarare la funzione [SafeRelease](saferelease.md) :</span><span class="sxs-lookup"><span data-stu-id="c75d7-131">Declare the [SafeRelease](saferelease.md) function:</span></span>


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



## <a name="2-open-an-asf-file"></a><span data-ttu-id="c75d7-132">2. aprire un file ASF</span><span class="sxs-lookup"><span data-stu-id="c75d7-132">2. Open an ASF File</span></span>

<span data-ttu-id="c75d7-133">Successivamente, aprire il file specificato chiamando la funzione [**MFCreateFile**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatefile) .</span><span class="sxs-lookup"><span data-stu-id="c75d7-133">Next, open the specified file by calling the [**MFCreateFile**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatefile) function.</span></span> <span data-ttu-id="c75d7-134">Il metodo restituisce un puntatore all'oggetto flusso di byte che contiene il contenuto del file.</span><span class="sxs-lookup"><span data-stu-id="c75d7-134">The method returns a pointer to the byte stream object that contains the contents of the file.</span></span> <span data-ttu-id="c75d7-135">Il nome file viene specificato dall'utente tramite gli argomenti della riga di comando dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c75d7-135">The filename is specified by the user through command line arguments of the application.</span></span>

<span data-ttu-id="c75d7-136">Il codice di esempio seguente accetta un nome di file e restituisce un puntatore a un oggetto flusso di byte che può essere usato per leggere il file.</span><span class="sxs-lookup"><span data-stu-id="c75d7-136">The following example code takes a file name and returns a pointer to a byte stream object that can be used to read the file.</span></span>


```C++
        // Open the file.
        hr = MFCreateFile(MF_ACCESSMODE_READ, MF_OPENMODE_FAIL_IF_NOT_EXIST, 
            MF_FILEFLAGS_NONE, pszFileName, &pStream);
```



## <a name="3-read-the-asf-header-object"></a><span data-ttu-id="c75d7-137">3. leggere l'oggetto intestazione ASF</span><span class="sxs-lookup"><span data-stu-id="c75d7-137">3. Read the ASF Header Object</span></span>

<span data-ttu-id="c75d7-138">Successivamente, creare l' [oggetto ContentInfo ASF](asf-contentinfo-object.md) e usarlo per analizzare l'oggetto intestazione ASF del file specificato.</span><span class="sxs-lookup"><span data-stu-id="c75d7-138">Next, create the [ASF ContentInfo Object](asf-contentinfo-object.md) and use it to parse the ASF Header Object of the specified file.</span></span> <span data-ttu-id="c75d7-139">L'oggetto ContentInfo archivia le informazioni dall'intestazione ASF, inclusi gli attributi di file globali e le informazioni su ogni flusso.</span><span class="sxs-lookup"><span data-stu-id="c75d7-139">The ContentInfo object stores information from the ASF header, including global file attributes and information about each stream.</span></span> <span data-ttu-id="c75d7-140">L'oggetto ContentInfo sarà utilizzato più avanti nell'esercitazione per inizializzare il separatore ASF e ottenere il numero di flusso del flusso video.</span><span class="sxs-lookup"><span data-stu-id="c75d7-140">You will use the ContentInfo object later in the tutorial to initialize the ASF splitter and get the stream number of the video stream.</span></span>

<span data-ttu-id="c75d7-141">Per creare l'oggetto ContentInfo ASF:</span><span class="sxs-lookup"><span data-stu-id="c75d7-141">To create the ASF ContentInfo object:</span></span>

1.  <span data-ttu-id="c75d7-142">Chiamare la funzione [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) per creare un oggetto ContentInfo.</span><span class="sxs-lookup"><span data-stu-id="c75d7-142">Call the [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) function to create a ContentInfo object.</span></span> <span data-ttu-id="c75d7-143">Il metodo restituisce un puntatore all'interfaccia [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) .</span><span class="sxs-lookup"><span data-stu-id="c75d7-143">The method returns a pointer to the [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) interface.</span></span>
2.  <span data-ttu-id="c75d7-144">Leggere i primi 30 byte di dati dal file ASF in un buffer multimediale.</span><span class="sxs-lookup"><span data-stu-id="c75d7-144">Read the first 30 bytes of data from the ASF file into a media buffer.</span></span>
3.  <span data-ttu-id="c75d7-145">Passare il buffer multimediale al metodo [**IMFASFContentInfo:: GetHeaderSize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getheadersize) .</span><span class="sxs-lookup"><span data-stu-id="c75d7-145">Pass the media buffer to the [**IMFASFContentInfo::GetHeaderSize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getheadersize) method.</span></span> <span data-ttu-id="c75d7-146">Questo metodo restituisce le dimensioni totali dell'oggetto intestazione nel file ASF.</span><span class="sxs-lookup"><span data-stu-id="c75d7-146">This method returns the total size of the Header Object in the ASF file.</span></span>
4.  <span data-ttu-id="c75d7-147">Passare lo stesso buffer multimediale al metodo [**IMFASFContentInfo::P arseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) .</span><span class="sxs-lookup"><span data-stu-id="c75d7-147">Pass the same media buffer to the [**IMFASFContentInfo::ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) method.</span></span>
5.  <span data-ttu-id="c75d7-148">Leggere il resto dell'oggetto intestazione in un nuovo buffer multimediale.</span><span class="sxs-lookup"><span data-stu-id="c75d7-148">Read the remainder of the Header Object into a new media buffer.</span></span>
6.  <span data-ttu-id="c75d7-149">Passare il secondo buffer al metodo [**ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) .</span><span class="sxs-lookup"><span data-stu-id="c75d7-149">Pass the second buffer to the [**ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) method.</span></span> <span data-ttu-id="c75d7-150">Specificare l'offset di 30 byte nel parametro *cbOffsetWithinHeader* di **ParseHeader**.</span><span class="sxs-lookup"><span data-stu-id="c75d7-150">Specify the 30-byte offset in the *cbOffsetWithinHeader* parameter of **ParseHeader**.</span></span> <span data-ttu-id="c75d7-151">Il metodo **ParseHeader** Inizializza l'oggetto ContentInfo con le informazioni raccolte dai vari oggetti ASF contenuti nell'oggetto intestazione.</span><span class="sxs-lookup"><span data-stu-id="c75d7-151">The **ParseHeader** method initializes the ContentInfo object with information gathered from the various ASF objects contained in the Header Object.</span></span>


```C++
// Read the ASF Header Object from a byte stream and return a pointer to the 
// populated ASF ContentInfo object.
//
// The current read position of the byte stream must be at the start of the
// ASF Header Object.

HRESULT CreateContentInfo(IMFByteStream *pStream, 
    IMFASFContentInfo **ppContentInfo)
{
    const DWORD MIN_ASF_HEADER_SIZE = 30;
    
    QWORD cbHeader = 0;
    DWORD cbBuffer = 0;

    IMFASFContentInfo *pContentInfo = NULL;
    IMFMediaBuffer *pBuffer = NULL;

    // Create the ASF ContentInfo object.
    HRESULT hr = MFCreateASFContentInfo(&pContentInfo);
    
    // Read the first 30 bytes to find the total header size.

    if (SUCCEEDED(hr))
    {
        hr = MFCreateMemoryBuffer(MIN_ASF_HEADER_SIZE, &pBuffer);
    }
    if (SUCCEEDED(hr))
    {
        hr = ReadFromByteStream(pStream, pBuffer,MIN_ASF_HEADER_SIZE);
    }
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->GetHeaderSize(pBuffer, &cbHeader);
    }

    // Pass the first 30 bytes to the ContentInfo object.
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->ParseHeader(pBuffer, 0);
    }

    SafeRelease(&pBuffer);

    if (SUCCEEDED(hr))
    {
        cbBuffer = (DWORD)(cbHeader - MIN_ASF_HEADER_SIZE);

        hr = MFCreateMemoryBuffer(cbBuffer, &pBuffer);
    }

    // Read the rest of the header and finish parsing the header.
    if (SUCCEEDED(hr))
    {
        hr = ReadFromByteStream(pStream, pBuffer, cbBuffer);
    }
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->ParseHeader(pBuffer, MIN_ASF_HEADER_SIZE);
    }
    if (SUCCEEDED(hr))
    {
        // Return the pointer to the caller.
        *ppContentInfo = pContentInfo;
        (*ppContentInfo)->AddRef();
    }
    SafeRelease(&pBuffer);
    SafeRelease(&pContentInfo);
    return hr;
} 
```



<span data-ttu-id="c75d7-152">Questa funzione usa la `ReadFromByteStream` funzione per leggere da un flusso di byte in un buffer multimediale:</span><span class="sxs-lookup"><span data-stu-id="c75d7-152">This function uses the `ReadFromByteStream` function to read from a byte stream into a media buffer:</span></span>


```C++
// Read data from a byte stream into a media buffer.
//
// This function reads a maximum of cbMax bytes, or up to the size size of the 
// buffer, whichever is smaller. If the end of the byte stream is reached, the 
// actual amount of data read might be less than either of these values.
//
// To find out how much data was read, call IMFMediaBuffer::GetCurrentLength.

HRESULT ReadFromByteStream(
    IMFByteStream *pStream,     // Pointer to the byte stream.
    IMFMediaBuffer *pBuffer,    // Pointer to the media buffer.
    DWORD cbMax                 // Maximum amount to read.
    )
{
    DWORD cbBufferMax = 0;
    DWORD cbRead = 0;
    BYTE *pData= NULL;

    HRESULT hr = pBuffer->Lock(&pData, &cbBufferMax, NULL);

    // Do not exceed the maximum size of the buffer.
    if (SUCCEEDED(hr))
    {
        if (cbMax > cbBufferMax)
        {
            cbMax = cbBufferMax;
        }

        // Read up to cbMax bytes.
        hr = pStream->Read(pData, cbMax, &cbRead);
    }

    // Update the size of the valid data in the buffer.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->SetCurrentLength(cbRead);
    }
    if (pData)
    {
        pBuffer->Unlock();
    }
    return hr;
}
```



## <a name="4-create-the-asf-splitter"></a><span data-ttu-id="c75d7-153">4. creare il separatore ASF</span><span class="sxs-lookup"><span data-stu-id="c75d7-153">4. Create the ASF Splitter</span></span>

<span data-ttu-id="c75d7-154">Successivamente, creare l'oggetto [splitter ASF](asf-splitter.md) .</span><span class="sxs-lookup"><span data-stu-id="c75d7-154">Next, create the [ASF Splitter](asf-splitter.md) object.</span></span> <span data-ttu-id="c75d7-155">Si userà la barra di divisione ASF per analizzare l'oggetto dati ASF, che contiene i dati multimediali in pacchetto per il file ASF.</span><span class="sxs-lookup"><span data-stu-id="c75d7-155">You will use the ASF splitter to parse the ASF Data Object, which contains packetized media data for the ASF file.</span></span>

<span data-ttu-id="c75d7-156">Per creare un oggetto Splitter per il file ASF:</span><span class="sxs-lookup"><span data-stu-id="c75d7-156">To create a splitter object for the ASF File:</span></span>

1.  <span data-ttu-id="c75d7-157">Chiamare la funzione [**MFCreateASFSplitter**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfsplitter) per creare il separatore ASF.</span><span class="sxs-lookup"><span data-stu-id="c75d7-157">Call the [**MFCreateASFSplitter**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfsplitter) function to create the ASF splitter.</span></span> <span data-ttu-id="c75d7-158">La funzione restituisce un puntatore all'interfaccia [**IMFASFSplitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) .</span><span class="sxs-lookup"><span data-stu-id="c75d7-158">The function returns a pointer to the [**IMFASFSplitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) interface.</span></span>
2.  <span data-ttu-id="c75d7-159">Chiamare [**IMFASFSplitter:: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize) per inizializzare il separatore ASF.</span><span class="sxs-lookup"><span data-stu-id="c75d7-159">Call [**IMFASFSplitter::Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize) to initialize the ASF splitter.</span></span> <span data-ttu-id="c75d7-160">Questo metodo accetta un puntatore all'oggetto ContentInfo, che è stato creato nella procedura 3.</span><span class="sxs-lookup"><span data-stu-id="c75d7-160">This method takes a pointer to the ContentInfo object, which was created in procedure 3.</span></span>


```C++
// Create and initialize the ASF splitter.

HRESULT CreateASFSplitter (IMFASFContentInfo* pContentInfo, 
    IMFASFSplitter** ppSplitter)
{
    IMFASFSplitter *pSplitter = NULL;

    // Create the splitter object.
    HRESULT hr = MFCreateASFSplitter(&pSplitter);

    // Initialize the splitter to work with specific ASF data.
    if (SUCCEEDED(hr))
    {
        hr = pSplitter->Initialize(pContentInfo);
    }
    if (SUCCEEDED(hr))
    {
        // Return the object to the caller.
        *ppSplitter = pSplitter;
        (*ppSplitter)->AddRef();
    }
    SafeRelease(&pSplitter);
    return hr;
}
```



## <a name="5-select-a-stream-for-parsing"></a><span data-ttu-id="c75d7-161">5. Selezionare un flusso per l'analisi</span><span class="sxs-lookup"><span data-stu-id="c75d7-161">5. Select a Stream for Parsing</span></span>

<span data-ttu-id="c75d7-162">Quindi, enumerare i flussi nel file ASF e selezionare il primo flusso video per l'analisi.</span><span class="sxs-lookup"><span data-stu-id="c75d7-162">Next, enumerate the streams in the ASF file and select the first video stream for parsing.</span></span> <span data-ttu-id="c75d7-163">Per enumerare i flussi, usare un oggetto profilo ASF e cercare i flussi con un tipo di supporto video.</span><span class="sxs-lookup"><span data-stu-id="c75d7-163">To enumerate the streams, you will use an ASF profile object and search for streams that have a video media type.</span></span>

<span data-ttu-id="c75d7-164">Per selezionare il flusso video:</span><span class="sxs-lookup"><span data-stu-id="c75d7-164">To select the video stream:</span></span>

1.  <span data-ttu-id="c75d7-165">Per creare un profilo ASF, chiamare [**IMFASFContentInfo:: GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile) nell'oggetto ContentInfo.</span><span class="sxs-lookup"><span data-stu-id="c75d7-165">Call [**IMFASFContentInfo::GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile) on the ContentInfo object to create an ASF profile.</span></span> <span data-ttu-id="c75d7-166">Tra le altre informazioni, il profilo descrive i flussi nel file ASF.</span><span class="sxs-lookup"><span data-stu-id="c75d7-166">Among other information, the profile describes the streams in the ASF file.</span></span>
2.  <span data-ttu-id="c75d7-167">Chiamare [**IMFASFProfile:: GetStreamCount**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamcount) per ottenere il numero di flussi nel file ASF.</span><span class="sxs-lookup"><span data-stu-id="c75d7-167">Call [**IMFASFProfile::GetStreamCount**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamcount) to get the number of streams in the ASF file.</span></span>
3.  <span data-ttu-id="c75d7-168">Chiamare [**IMFASFProfile:: GetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream) in un ciclo per enumerare i flussi.</span><span class="sxs-lookup"><span data-stu-id="c75d7-168">Call [**IMFASFProfile::GetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream) in a loop to enumerate the streams.</span></span> <span data-ttu-id="c75d7-169">Il metodo restituisce un puntatore all'interfaccia [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) .</span><span class="sxs-lookup"><span data-stu-id="c75d7-169">The method returns a pointer to the [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) interface.</span></span> <span data-ttu-id="c75d7-170">Restituisce anche l'identificatore del flusso.</span><span class="sxs-lookup"><span data-stu-id="c75d7-170">It also returns the stream identifier.</span></span>
4.  <span data-ttu-id="c75d7-171">Chiamare [**IMFASFStreamConfig:: GetStreamType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getstreamtype) per ottenere il GUID di tipo principale per il flusso.</span><span class="sxs-lookup"><span data-stu-id="c75d7-171">Call [**IMFASFStreamConfig::GetStreamType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getstreamtype) to get the major type GUID for the stream.</span></span> <span data-ttu-id="c75d7-172">Se il tipo principale GUID è MFMediaType \_ video, il flusso contiene video.</span><span class="sxs-lookup"><span data-stu-id="c75d7-172">If the major type GUID is MFMediaType\_Video, the stream contains video.</span></span>
5.  <span data-ttu-id="c75d7-173">Se nel passaggio 4 è stato trovato un flusso video, chiamare [**IMFASFSplitter:: SelectStreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-selectstreams) per selezionare il flusso.</span><span class="sxs-lookup"><span data-stu-id="c75d7-173">If you found a video stream in step 4, call [**IMFASFSplitter::SelectStreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-selectstreams) to select the stream.</span></span> <span data-ttu-id="c75d7-174">Questo metodo accetta una matrice di identificatori di flusso.</span><span class="sxs-lookup"><span data-stu-id="c75d7-174">This method takes an array of stream identifiers.</span></span> <span data-ttu-id="c75d7-175">Per questa esercitazione, le dimensioni della matrice sono pari a 1 perché l'applicazione analizza un singolo flusso.</span><span class="sxs-lookup"><span data-stu-id="c75d7-175">For this tutorial, the array size is 1 because the application will parse a single stream.</span></span>

<span data-ttu-id="c75d7-176">Il codice di esempio seguente enumera i flussi nel file ASF e seleziona il primo flusso video nella barra di divisione ASF:</span><span class="sxs-lookup"><span data-stu-id="c75d7-176">The following example code enumerates the streams in the ASF file and selects the first video stream on the ASF splitter:</span></span>


```C++
// Select the first video stream for parsing with the ASF splitter.

HRESULT SelectVideoStream(IMFASFContentInfo *pContentInfo, 
    IMFASFSplitter *pSplitter, BOOL *pbHasVideo)
{
    DWORD   cStreams = 0;
    WORD    wStreamID = 0;

    IMFASFProfile *pProfile = NULL;
    IMFASFStreamConfig *pStream = NULL;

    // Get the ASF profile from the ContentInfo object.
    HRESULT hr = pContentInfo->GetProfile(&pProfile);

    // Loop through all of the streams in the profile.
    if (SUCCEEDED(hr))
    {
        hr = pProfile->GetStreamCount(&cStreams);
    }

    if (SUCCEEDED(hr))
    {
        for (DWORD i = 0; i < cStreams; i++)
        {
            GUID    streamType = GUID_NULL;

            // Get the stream type and stream identifier.
            hr = pProfile->GetStream(i, &wStreamID, &pStream);
            if (FAILED(hr)) 
            {
                break;
            }

            hr = pStream->GetStreamType(&streamType);
            if (FAILED(hr)) 
            {
                break;
            }

            if (streamType == MFMediaType_Video)
            {
                *pbHasVideo = TRUE;
                break;
            }
            SafeRelease(&pStream);
        }
    }

    // Select the video stream, if found.
    if (SUCCEEDED(hr))
    {
        if (*pbHasVideo)
        {
            // SelectStreams takes an array of stream identifiers.
            hr = pSplitter->SelectStreams(&wStreamID, 1);
        }
    }
    SafeRelease(&pStream);
    SafeRelease(&pProfile);
    return hr;
}
```



## <a name="6-generate-compressed-media-samples"></a><span data-ttu-id="c75d7-177">6. generare esempi di supporti compressi</span><span class="sxs-lookup"><span data-stu-id="c75d7-177">6. Generate Compressed Media Samples</span></span>

<span data-ttu-id="c75d7-178">Usare quindi la barra di divisione ASF per analizzare l'oggetto dati ASF e ottenere i pacchetti di dati per il flusso video selezionato.</span><span class="sxs-lookup"><span data-stu-id="c75d7-178">Next, use the ASF splitter to parse the ASF Data Object and get the data packets for the selected video stream.</span></span> <span data-ttu-id="c75d7-179">L'applicazione legge i dati dal file ASF nei blocchi a dimensione fissa e passa i dati alla barra di divisione ASF.</span><span class="sxs-lookup"><span data-stu-id="c75d7-179">The application reads data from the ASF file in fixed-size blocks and passes the data to the ASF splitter.</span></span> <span data-ttu-id="c75d7-180">La barra di divisione analizza i dati e genera [esempi multimediali](media-samples.md) contenenti i dati video compressi.</span><span class="sxs-lookup"><span data-stu-id="c75d7-180">The splitter parses the data and generates [Media Samples](media-samples.md) that contain the compressed video data.</span></span> <span data-ttu-id="c75d7-181">L'applicazione controlla se ogni esempio rappresenta un fotogramma chiave.</span><span class="sxs-lookup"><span data-stu-id="c75d7-181">The application checks whether each sample represents a key frame.</span></span> <span data-ttu-id="c75d7-182">In tal caso, nell'applicazione vengono visualizzate alcune informazioni di base sull'esempio:</span><span class="sxs-lookup"><span data-stu-id="c75d7-182">If so, the application displays some basic information about the sample:</span></span>

-   <span data-ttu-id="c75d7-183">Numero di buffer multimediali</span><span class="sxs-lookup"><span data-stu-id="c75d7-183">Number of media buffers</span></span>
-   <span data-ttu-id="c75d7-184">Dimensioni totali dei dati</span><span class="sxs-lookup"><span data-stu-id="c75d7-184">Total size of the data</span></span>
-   <span data-ttu-id="c75d7-185">Timestamp</span><span class="sxs-lookup"><span data-stu-id="c75d7-185">Time stamp</span></span>

<span data-ttu-id="c75d7-186">Per generare esempi di supporti compressi:</span><span class="sxs-lookup"><span data-stu-id="c75d7-186">To generate compressed media samples:</span></span>

1.  <span data-ttu-id="c75d7-187">Allocare un nuovo buffer multimediale.</span><span class="sxs-lookup"><span data-stu-id="c75d7-187">Allocate a new media buffer.</span></span>
2.  <span data-ttu-id="c75d7-188">Legge i dati dal flusso di byte nel buffer multimediale.</span><span class="sxs-lookup"><span data-stu-id="c75d7-188">Read data from the byte stream into the media buffer.</span></span>
3.  <span data-ttu-id="c75d7-189">Passare il buffer multimediale al metodo [**IMFASFSplitter::P arsedata**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) .</span><span class="sxs-lookup"><span data-stu-id="c75d7-189">Pass the media buffer to the [**IMFASFSplitter::ParseData**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) method.</span></span> <span data-ttu-id="c75d7-190">Il metodo analizza i dati ASF nel buffer.</span><span class="sxs-lookup"><span data-stu-id="c75d7-190">The method parses the ASF data in the buffer.</span></span>
4.  <span data-ttu-id="c75d7-191">In un ciclo, ottenere gli esempi di supporti dalla barra di divisione chiamando [**IMFASFSplitter:: GetNextSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample).</span><span class="sxs-lookup"><span data-stu-id="c75d7-191">In a loop, get media samples from the splitter by calling [**IMFASFSplitter::GetNextSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample).</span></span> <span data-ttu-id="c75d7-192">Se il parametro *ppISample* riceve un puntatore [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) valido, significa che il separatore ASF ha analizzato uno o più pacchetti di dati.</span><span class="sxs-lookup"><span data-stu-id="c75d7-192">If the *ppISample* parameter receives a valid [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) pointer, it means the ASF splitter has parsed one or more data packets.</span></span> <span data-ttu-id="c75d7-193">Se *ppISample* riceve il valore **null**, interrompere il ciclo e tornare al passaggio 1.</span><span class="sxs-lookup"><span data-stu-id="c75d7-193">If *ppISample* receives the value **NULL**, break from the loop and go back to step 1.</span></span>
5.  <span data-ttu-id="c75d7-194">Visualizzare informazioni sull'esempio.</span><span class="sxs-lookup"><span data-stu-id="c75d7-194">Display information about the sample.</span></span>
6.  <span data-ttu-id="c75d7-195">Interrompere il ciclo con le condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="c75d7-195">Break from the loop in the following conditions:</span></span>
    -   <span data-ttu-id="c75d7-196">Il parametro *ppISample* riceve il valore **null**.</span><span class="sxs-lookup"><span data-stu-id="c75d7-196">The *ppISample* parameter receives the value **NULL**.</span></span>
    -   <span data-ttu-id="c75d7-197">Il parametro *pdwStatusFlags* non riceve il flag **ASF \_ STATUSFLAGS \_ incompleto** .</span><span class="sxs-lookup"><span data-stu-id="c75d7-197">The *pdwStatusFlags* parameter does not receive the **ASF\_STATUSFLAGS\_INCOMPLETE** flag.</span></span>

<span data-ttu-id="c75d7-198">Ripetere questi passaggi fino a raggiungere la fine del file.</span><span class="sxs-lookup"><span data-stu-id="c75d7-198">Repeat these steps until you reach the end of the file.</span></span> <span data-ttu-id="c75d7-199">Il codice seguente illustra questi passaggi:</span><span class="sxs-lookup"><span data-stu-id="c75d7-199">The following code shows these steps:</span></span>


```C++
// Parse the video stream and display information about the video samples.
//
// The current read position of the byte stream must be at the start of the ASF
// Data Object.

HRESULT DisplayKeyFrames(IMFByteStream *pStream, IMFASFSplitter *pSplitter)
{
    const DWORD cbReadSize = 2048;  // Read size (arbitrary value)

    IMFMediaBuffer *pBuffer = NULL;
    IMFSample *pSample = NULL;

    HRESULT hr = S_OK;
    while (SUCCEEDED(hr))
    {
        // The parser must get a newly allocated buffer each time.
        hr = MFCreateMemoryBuffer(cbReadSize, &pBuffer);
        if (FAILED(hr))
        {
            break;
        }

        // Read data into the buffer.
        hr = ReadFromByteStream(pStream, pBuffer, cbReadSize);
        if (FAILED(hr)) 
        {
            break; 
        }

        // Get the amound of data that was read.
        DWORD cbData;
        hr = pBuffer->GetCurrentLength(&cbData);
        if (FAILED(hr)) 
        { 
            break; 
        }

        if (cbData == 0)
        {
            break; // End of file.
        }

        // Send the data to the ASF splitter.
        hr = pSplitter->ParseData(pBuffer, 0, 0);
        SafeRelease(&pBuffer);
        if (FAILED(hr)) 
        { 
            break; 
        }

        // Pull samples from the splitter.
        DWORD parsingStatus = 0;
        do
        {
            WORD streamID;
            hr = pSplitter->GetNextSample(&parsingStatus, &streamID, &pSample);
            if (FAILED(hr)) 
            { 
                break; 
            }
            if (pSample == NULL)
            {
                // No samples yet. Parse more data.
                break;
            }
            if (IsRandomAccessPoint(pSample))
            {
                DisplayKeyFrame(pSample);
            }
            SafeRelease(&pSample);
            
        } while (parsingStatus & ASF_STATUSFLAGS_INCOMPLETE);
    }
    SafeRelease(&pSample);
    SafeRelease(&pBuffer);
    return hr;
}
```



<span data-ttu-id="c75d7-200">La funzione di fotogramma chiave verifica se un campione è un fotogramma chiave ottenendo il valore dell' [**attributo \_ CleanPoint di MFSampleExtension**](mfsampleextension-cleanpoint-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="c75d7-200">The IsKeyFrame function tests whether a sample is a key frame, by getting the value of the [**MFSampleExtension\_CleanPoint**](mfsampleextension-cleanpoint-attribute.md) attribute.</span></span>


```C++
inline BOOL IsRandomAccessPoint(IMFSample *pSample)
{
    // Check for the "clean point" attribute. Default to FALSE.
    return MFGetAttributeUINT32(pSample, MFSampleExtension_CleanPoint, FALSE);
}
```



<span data-ttu-id="c75d7-201">A scopo illustrativo, in questa esercitazione vengono visualizzate alcune informazioni per ogni fotogramma chiave video, chiamando la funzione seguente:</span><span class="sxs-lookup"><span data-stu-id="c75d7-201">For illustration purposes, this tutorial displays some information for each video key frame, by calling the following function:</span></span>


```C++
void DisplayKeyFrame(IMFSample *pSample)
{
    DWORD   cBuffers = 0;           // Buffer count
    DWORD   cbTotalLength = 0;      // Buffer length
    MFTIME  hnsTime = 0;            // Time stamp

    // Print various information about the key frame.
    if (SUCCEEDED(pSample->GetBufferCount(&cBuffers)))
    {
        wprintf_s(L"Buffer count: %d\n", cBuffers);
    }
    if (SUCCEEDED(pSample->GetTotalLength(&cbTotalLength)))
    {
        wprintf_s(L"Length: %d bytes\n", cbTotalLength);
    }
    if (SUCCEEDED(pSample->GetSampleTime(&hnsTime)))
    {
        // Convert the time stamp to seconds.
        double sec = static_cast<double>(hnsTime / 10000) / 1000;
        wprintf_s(L"Time stamp: %f sec.\n", sec);
    }
    wprintf_s(L"\n");
}
```



<span data-ttu-id="c75d7-202">Un'applicazione tipica usa i pacchetti di dati per la decodifica, remuxing, l'invio in rete o un'altra attività.</span><span class="sxs-lookup"><span data-stu-id="c75d7-202">A typical application would use the data packets for decoding, remuxing, sending over the network, or some other task.</span></span>

## <a name="7-write-the-entry-point-function"></a><span data-ttu-id="c75d7-203">7. scrivere la funzione Entry-Point</span><span class="sxs-lookup"><span data-stu-id="c75d7-203">7. Write the Entry-Point Function</span></span>

<span data-ttu-id="c75d7-204">È ora possibile inserire i passaggi precedenti in un'applicazione completa.</span><span class="sxs-lookup"><span data-stu-id="c75d7-204">Now you can put the previous steps together into a complete application.</span></span> <span data-ttu-id="c75d7-205">Prima di usare uno degli oggetti Media Foundation, inizializzare la piattaforma Media Foundation chiamando [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup).</span><span class="sxs-lookup"><span data-stu-id="c75d7-205">Before using any of the Media Foundation objects, initialize the Media Foundation platform by calling [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup).</span></span> <span data-ttu-id="c75d7-206">Al termine, chiamare [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown).</span><span class="sxs-lookup"><span data-stu-id="c75d7-206">When you are done, call [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown).</span></span> <span data-ttu-id="c75d7-207">Per ulteriori informazioni, [inizializzazione di Media Foundation](initializing-media-foundation.md).</span><span class="sxs-lookup"><span data-stu-id="c75d7-207">For more information, [Initializing Media Foundation](initializing-media-foundation.md).</span></span>


```C++
int wmain(int argc, WCHAR* argv[])
{
    if (argc != 2)
    {
        _s(L"Usage: %s input.wmv");
        return 0;
    }

    // Start the Media Foundation platform.
    HRESULT hr = MFStartup(MF_VERSION);
    if (SUCCEEDED(hr))
    {
        PCWSTR pszFileName = argv[1]; 
        BOOL   bHasVideo = FALSE;

        IMFByteStream       *pStream = NULL;
        IMFASFContentInfo   *pContentInfo = NULL;
        IMFASFSplitter      *pSplitter = NULL;

        // Open the file.
        hr = MFCreateFile(MF_ACCESSMODE_READ, MF_OPENMODE_FAIL_IF_NOT_EXIST, 
            MF_FILEFLAGS_NONE, pszFileName, &pStream);

        // Read the ASF header.
        if (SUCCEEDED(hr))
        {
            hr = CreateContentInfo(pStream, &pContentInfo);
        }

        // Create the ASF splitter.
        if (SUCCEEDED(hr))
        {
            hr = CreateASFSplitter(pContentInfo, &pSplitter);
        }

        // Select the first video stream.
        if (SUCCEEDED(hr))
        {
            hr = SelectVideoStream(pContentInfo, pSplitter, &bHasVideo);
        }

        // Parse the ASF file.
        if (SUCCEEDED(hr))
        {
            if (bHasVideo)
            {
                hr = DisplayKeyFrames(pStream, pSplitter);
            }
            else
            {
                wprintf_s(L"No video stream.\n");
            }
        }
        SafeRelease(&pSplitter);
        SafeRelease(&pContentInfo);
        SafeRelease(&pStream);
    
        // Shut down the Media Foundation platform.
        MFShutdown();
    }
    if (FAILED(hr))
    {
        wprintf_s(L"Error: 0x%X\n", hr);
    }
    return 0;
}
```



## <a name="program-listing"></a><span data-ttu-id="c75d7-208">Elenco programmi</span><span class="sxs-lookup"><span data-stu-id="c75d7-208">Program Listing</span></span>

<span data-ttu-id="c75d7-209">Il codice seguente illustra l'elenco completo per l'esercitazione.</span><span class="sxs-lookup"><span data-stu-id="c75d7-209">The following code shows the complete listing for the tutorial.</span></span>


```C++
#include <stdio.h>       // Standard I/O
#include <windows.h>     // Windows headers
#include <mfapi.h>       // Media Foundation platform
#include <wmcontainer.h> // ASF interfaces
#include <Mferror.h>

#pragma comment(lib, "mfplat")
#pragma comment(lib, "mf")
#pragma comment(lib, "mfuuid")

template <class T> void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}

// Read data from a byte stream into a media buffer.
//
// This function reads a maximum of cbMax bytes, or up to the size size of the 
// buffer, whichever is smaller. If the end of the byte stream is reached, the 
// actual amount of data read might be less than either of these values.
//
// To find out how much data was read, call IMFMediaBuffer::GetCurrentLength.

HRESULT ReadFromByteStream(
    IMFByteStream *pStream,     // Pointer to the byte stream.
    IMFMediaBuffer *pBuffer,    // Pointer to the media buffer.
    DWORD cbMax                 // Maximum amount to read.
    )
{
    DWORD cbBufferMax = 0;
    DWORD cbRead = 0;
    BYTE *pData= NULL;

    HRESULT hr = pBuffer->Lock(&pData, &cbBufferMax, NULL);

    // Do not exceed the maximum size of the buffer.
    if (SUCCEEDED(hr))
    {
        if (cbMax > cbBufferMax)
        {
            cbMax = cbBufferMax;
        }

        // Read up to cbMax bytes.
        hr = pStream->Read(pData, cbMax, &cbRead);
    }

    // Update the size of the valid data in the buffer.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->SetCurrentLength(cbRead);
    }
    if (pData)
    {
        pBuffer->Unlock();
    }
    return hr;
}


// Read the ASF Header Object from a byte stream and return a pointer to the 
// populated ASF ContentInfo object.
//
// The current read position of the byte stream must be at the start of the
// ASF Header Object.

HRESULT CreateContentInfo(IMFByteStream *pStream, 
    IMFASFContentInfo **ppContentInfo)
{
    const DWORD MIN_ASF_HEADER_SIZE = 30;
    
    QWORD cbHeader = 0;
    DWORD cbBuffer = 0;

    IMFASFContentInfo *pContentInfo = NULL;
    IMFMediaBuffer *pBuffer = NULL;

    // Create the ASF ContentInfo object.
    HRESULT hr = MFCreateASFContentInfo(&pContentInfo);
    
    // Read the first 30 bytes to find the total header size.

    if (SUCCEEDED(hr))
    {
        hr = MFCreateMemoryBuffer(MIN_ASF_HEADER_SIZE, &pBuffer);
    }
    if (SUCCEEDED(hr))
    {
        hr = ReadFromByteStream(pStream, pBuffer,MIN_ASF_HEADER_SIZE);
    }
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->GetHeaderSize(pBuffer, &cbHeader);
    }

    // Pass the first 30 bytes to the ContentInfo object.
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->ParseHeader(pBuffer, 0);
    }

    SafeRelease(&pBuffer);

    if (SUCCEEDED(hr))
    {
        cbBuffer = (DWORD)(cbHeader - MIN_ASF_HEADER_SIZE);

        hr = MFCreateMemoryBuffer(cbBuffer, &pBuffer);
    }

    // Read the rest of the header and finish parsing the header.
    if (SUCCEEDED(hr))
    {
        hr = ReadFromByteStream(pStream, pBuffer, cbBuffer);
    }
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->ParseHeader(pBuffer, MIN_ASF_HEADER_SIZE);
    }
    if (SUCCEEDED(hr))
    {
        // Return the pointer to the caller.
        *ppContentInfo = pContentInfo;
        (*ppContentInfo)->AddRef();
    }
    SafeRelease(&pBuffer);
    SafeRelease(&pContentInfo);
    return hr;
} 

// Create and initialize the ASF splitter.

HRESULT CreateASFSplitter (IMFASFContentInfo* pContentInfo, 
    IMFASFSplitter** ppSplitter)
{
    IMFASFSplitter *pSplitter = NULL;

    // Create the splitter object.
    HRESULT hr = MFCreateASFSplitter(&pSplitter);

    // Initialize the splitter to work with specific ASF data.
    if (SUCCEEDED(hr))
    {
        hr = pSplitter->Initialize(pContentInfo);
    }
    if (SUCCEEDED(hr))
    {
        // Return the object to the caller.
        *ppSplitter = pSplitter;
        (*ppSplitter)->AddRef();
    }
    SafeRelease(&pSplitter);
    return hr;
}


// Select the first video stream for parsing with the ASF splitter.

HRESULT SelectVideoStream(IMFASFContentInfo *pContentInfo, 
    IMFASFSplitter *pSplitter, BOOL *pbHasVideo)
{
    DWORD   cStreams = 0;
    WORD    wStreamID = 0;

    IMFASFProfile *pProfile = NULL;
    IMFASFStreamConfig *pStream = NULL;

    // Get the ASF profile from the ContentInfo object.
    HRESULT hr = pContentInfo->GetProfile(&pProfile);

    // Loop through all of the streams in the profile.
    if (SUCCEEDED(hr))
    {
        hr = pProfile->GetStreamCount(&cStreams);
    }

    if (SUCCEEDED(hr))
    {
        for (DWORD i = 0; i < cStreams; i++)
        {
            GUID    streamType = GUID_NULL;

            // Get the stream type and stream identifier.
            hr = pProfile->GetStream(i, &wStreamID, &pStream);
            if (FAILED(hr)) 
            {
                break;
            }

            hr = pStream->GetStreamType(&streamType);
            if (FAILED(hr)) 
            {
                break;
            }

            if (streamType == MFMediaType_Video)
            {
                *pbHasVideo = TRUE;
                break;
            }
            SafeRelease(&pStream);
        }
    }

    // Select the video stream, if found.
    if (SUCCEEDED(hr))
    {
        if (*pbHasVideo)
        {
            // SelectStreams takes an array of stream identifiers.
            hr = pSplitter->SelectStreams(&wStreamID, 1);
        }
    }
    SafeRelease(&pStream);
    SafeRelease(&pProfile);
    return hr;
}

inline BOOL IsRandomAccessPoint(IMFSample *pSample)
{
    // Check for the "clean point" attribute. Default to FALSE.
    return MFGetAttributeUINT32(pSample, MFSampleExtension_CleanPoint, FALSE);
}

void DisplayKeyFrame(IMFSample *pSample)
{
    DWORD   cBuffers = 0;           // Buffer count
    DWORD   cbTotalLength = 0;      // Buffer length
    MFTIME  hnsTime = 0;            // Time stamp

    // Print various information about the key frame.
    if (SUCCEEDED(pSample->GetBufferCount(&cBuffers)))
    {
        wprintf_s(L"Buffer count: %d\n", cBuffers);
    }
    if (SUCCEEDED(pSample->GetTotalLength(&cbTotalLength)))
    {
        wprintf_s(L"Length: %d bytes\n", cbTotalLength);
    }
    if (SUCCEEDED(pSample->GetSampleTime(&hnsTime)))
    {
        // Convert the time stamp to seconds.
        double sec = static_cast<double>(hnsTime / 10000) / 1000;
        wprintf_s(L"Time stamp: %f sec.\n", sec);
    }
    wprintf_s(L"\n");
}


// Parse the video stream and display information about the video samples.
//
// The current read position of the byte stream must be at the start of the ASF
// Data Object.

HRESULT DisplayKeyFrames(IMFByteStream *pStream, IMFASFSplitter *pSplitter)
{
    const DWORD cbReadSize = 2048;  // Read size (arbitrary value)

    IMFMediaBuffer *pBuffer = NULL;
    IMFSample *pSample = NULL;

    HRESULT hr = S_OK;
    while (SUCCEEDED(hr))
    {
        // The parser must get a newly allocated buffer each time.
        hr = MFCreateMemoryBuffer(cbReadSize, &pBuffer);
        if (FAILED(hr))
        {
            break;
        }

        // Read data into the buffer.
        hr = ReadFromByteStream(pStream, pBuffer, cbReadSize);
        if (FAILED(hr)) 
        {
            break; 
        }

        // Get the amound of data that was read.
        DWORD cbData;
        hr = pBuffer->GetCurrentLength(&cbData);
        if (FAILED(hr)) 
        { 
            break; 
        }

        if (cbData == 0)
        {
            break; // End of file.
        }

        // Send the data to the ASF splitter.
        hr = pSplitter->ParseData(pBuffer, 0, 0);
        SafeRelease(&pBuffer);
        if (FAILED(hr)) 
        { 
            break; 
        }

        // Pull samples from the splitter.
        DWORD parsingStatus = 0;
        do
        {
            WORD streamID;
            hr = pSplitter->GetNextSample(&parsingStatus, &streamID, &pSample);
            if (FAILED(hr)) 
            { 
                break; 
            }
            if (pSample == NULL)
            {
                // No samples yet. Parse more data.
                break;
            }
            if (IsRandomAccessPoint(pSample))
            {
                DisplayKeyFrame(pSample);
            }
            SafeRelease(&pSample);
            
        } while (parsingStatus & ASF_STATUSFLAGS_INCOMPLETE);
    }
    SafeRelease(&pSample);
    SafeRelease(&pBuffer);
    return hr;
}

int wmain(int argc, WCHAR* argv[])
{
    if (argc != 2)
    {
        _s(L"Usage: %s input.wmv");
        return 0;
    }

    // Start the Media Foundation platform.
    HRESULT hr = MFStartup(MF_VERSION);
    if (SUCCEEDED(hr))
    {
        PCWSTR pszFileName = argv[1]; 
        BOOL   bHasVideo = FALSE;

        IMFByteStream       *pStream = NULL;
        IMFASFContentInfo   *pContentInfo = NULL;
        IMFASFSplitter      *pSplitter = NULL;

        // Open the file.
        hr = MFCreateFile(MF_ACCESSMODE_READ, MF_OPENMODE_FAIL_IF_NOT_EXIST, 
            MF_FILEFLAGS_NONE, pszFileName, &pStream);

        // Read the ASF header.
        if (SUCCEEDED(hr))
        {
            hr = CreateContentInfo(pStream, &pContentInfo);
        }

        // Create the ASF splitter.
        if (SUCCEEDED(hr))
        {
            hr = CreateASFSplitter(pContentInfo, &pSplitter);
        }

        // Select the first video stream.
        if (SUCCEEDED(hr))
        {
            hr = SelectVideoStream(pContentInfo, pSplitter, &bHasVideo);
        }

        // Parse the ASF file.
        if (SUCCEEDED(hr))
        {
            if (bHasVideo)
            {
                hr = DisplayKeyFrames(pStream, pSplitter);
            }
            else
            {
                wprintf_s(L"No video stream.\n");
            }
        }
        SafeRelease(&pSplitter);
        SafeRelease(&pContentInfo);
        SafeRelease(&pStream);
    
        // Shut down the Media Foundation platform.
        MFShutdown();
    }
    if (FAILED(hr))
    {
        wprintf_s(L"Error: 0x%X\n", hr);
    }
    return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="c75d7-210">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c75d7-210">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c75d7-211">Componenti ASF WMContainer</span><span class="sxs-lookup"><span data-stu-id="c75d7-211">WMContainer ASF Components</span></span>](wmcontainer-asf-components.md)
</dt> <dt>

[<span data-ttu-id="c75d7-212">Supporto ASF in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c75d7-212">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



