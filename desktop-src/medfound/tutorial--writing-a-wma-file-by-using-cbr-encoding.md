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
# <a name="tutorial-writing-a-wma-file-by-using-wmcontainer-objects"></a><span data-ttu-id="8071c-103">Esercitazione: scrittura di un file WMA usando oggetti WMContainer</span><span class="sxs-lookup"><span data-stu-id="8071c-103">Tutorial: Writing a WMA File by Using WMContainer Objects</span></span>

<span data-ttu-id="8071c-104">In questa esercitazione viene illustrato come scrivere un nuovo file audio (WMA) estraendo contenuto multimediale da un file audio non compresso (WAV) e quindi comprimerlo in formato ASF.</span><span class="sxs-lookup"><span data-stu-id="8071c-104">This tutorial demonstrates writing a new audio file (.wma) by extracting media content from an uncompressed audio file (.wav) and then compressing it in ASF format.</span></span> <span data-ttu-id="8071c-105">La modalità di codifica utilizzata per la conversione è la [codifica della velocità in bit costante](constant-bit-rate-encoding.md) (CBR).</span><span class="sxs-lookup"><span data-stu-id="8071c-105">The encoding mode used for the conversion is [Constant Bit Rate Encoding](constant-bit-rate-encoding.md) (CBR).</span></span> <span data-ttu-id="8071c-106">In questa modalità, prima della sessione di codifica, l'applicazione specifica una velocità in bit di destinazione che il codificatore deve raggiungere.</span><span class="sxs-lookup"><span data-stu-id="8071c-106">In this mode, before the encoding session, the application specifies a target bit rate that the encoder must achieve.</span></span>

<span data-ttu-id="8071c-107">In questa esercitazione verrà creata un'applicazione console che accetta i nomi dei file di input e di output come argomenti.</span><span class="sxs-lookup"><span data-stu-id="8071c-107">In this tutorial, you will create a console application that takes the input and output filenames as arguments.</span></span> <span data-ttu-id="8071c-108">L'applicazione ottiene gli esempi di supporti non compressi da un'applicazione di analisi di file Wave, fornita con questa esercitazione.</span><span class="sxs-lookup"><span data-stu-id="8071c-108">The application gets the uncompressed media samples from a wave file parsing application, which is provided with this tutorial.</span></span> <span data-ttu-id="8071c-109">Questi esempi vengono inviati al codificatore per la conversione nel formato Windows Media Audio 9.</span><span class="sxs-lookup"><span data-stu-id="8071c-109">These samples are sent to the encoder for conversion to Windows Media Audio 9 format.</span></span> <span data-ttu-id="8071c-110">Il codificatore è configurato per la codifica CBR e usa la velocità del primo bit disponibile durante la negoziazione del tipo di supporto come velocità in bit di destinazione.</span><span class="sxs-lookup"><span data-stu-id="8071c-110">The encoder is configured for CBR encoding and uses the first bit rate available during media type negotiation as the target bit rate.</span></span> <span data-ttu-id="8071c-111">Gli esempi codificati vengono inviati al multiplexer per la pacchettizzazione nel formato dati ASF.</span><span class="sxs-lookup"><span data-stu-id="8071c-111">The encoded samples are sent to the multiplexer for packetization in ASF data format.</span></span> <span data-ttu-id="8071c-112">Questi pacchetti verranno scritti in un flusso di byte che rappresenta l'oggetto dati ASF.</span><span class="sxs-lookup"><span data-stu-id="8071c-112">These packets will be written to a byte stream that represents the ASF Data Object.</span></span> <span data-ttu-id="8071c-113">Quando la sezione dati è pronta, si creerà un file audio ASF e si scriverà il nuovo oggetto intestazione ASF che consolida tutte le informazioni di intestazione e quindi aggiungerà il flusso di byte dell'oggetto dati ASF.</span><span class="sxs-lookup"><span data-stu-id="8071c-113">After the data section is ready, you will create an ASF audio file and write the new ASF Header Object that consolidates all the header information and then append the ASF Data Object byte stream.</span></span>

<span data-ttu-id="8071c-114">Questa esercitazione contiene le sezioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="8071c-114">This tutorial contains the following sections:</span></span>

-   [<span data-ttu-id="8071c-115">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="8071c-115">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="8071c-116">Terminologia</span><span class="sxs-lookup"><span data-stu-id="8071c-116">Terminology</span></span>](#terminology)
-   [<span data-ttu-id="8071c-117">1. configurare il progetto</span><span class="sxs-lookup"><span data-stu-id="8071c-117">1. Set up the Project</span></span>](#1-set-up-the-project)
-   [<span data-ttu-id="8071c-118">2. dichiarare le funzioni helper</span><span class="sxs-lookup"><span data-stu-id="8071c-118">2. Declare Helper Functions</span></span>](#2-declare-helper-functions)
-   [<span data-ttu-id="8071c-119">3. aprire un file audio</span><span class="sxs-lookup"><span data-stu-id="8071c-119">3. Open an Audio File</span></span>](#3-open-an-audio-file)
-   [<span data-ttu-id="8071c-120">4. configurare il codificatore</span><span class="sxs-lookup"><span data-stu-id="8071c-120">4. Configure the Encoder</span></span>](#4-configure-the-encoder)
-   [<span data-ttu-id="8071c-121">5. creare l'oggetto ContentInfo ASF.</span><span class="sxs-lookup"><span data-stu-id="8071c-121">5. Create the ASF ContentInfo object.</span></span>](#5-create-the-asf-contentinfo-object)
-   [<span data-ttu-id="8071c-122">6. creare il multiplexer ASF</span><span class="sxs-lookup"><span data-stu-id="8071c-122">6. Create the ASF Multiplexer</span></span>](#6-create-the-asf-multiplexer)
-   [<span data-ttu-id="8071c-123">7. generare nuovi pacchetti di dati ASF</span><span class="sxs-lookup"><span data-stu-id="8071c-123">7. Generate New ASF Data Packets</span></span>](#7-generate-new-asf-data-packets)
-   [<span data-ttu-id="8071c-124">8. scrivere il file ASF</span><span class="sxs-lookup"><span data-stu-id="8071c-124">8. Write the ASF File</span></span>](#8-write-the-asf-file)
-   [<span data-ttu-id="8071c-125">9. definire la funzione Entry-Point</span><span class="sxs-lookup"><span data-stu-id="8071c-125">9. Define the Entry-Point Function</span></span>](#9-define-the-entry-point-function)
-   [<span data-ttu-id="8071c-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8071c-126">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="8071c-127">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="8071c-127">Prerequisites</span></span>

<span data-ttu-id="8071c-128">Nell’esercitazione si presuppongono le condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="8071c-128">This tutorial assumes the following:</span></span>

-   <span data-ttu-id="8071c-129">Si ha familiarità con la struttura di un file ASF e i componenti forniti da Media Foundation per lavorare con gli oggetti ASF.</span><span class="sxs-lookup"><span data-stu-id="8071c-129">You are familiar with the structure of an ASF file and the components provided by Media Foundation to work with ASF Objects.</span></span> <span data-ttu-id="8071c-130">Questi componenti includono oggetti ContentInfo, Splitter, multiplexer e profile.</span><span class="sxs-lookup"><span data-stu-id="8071c-130">These components include ContentInfo, splitter, multiplexer, and profile objects.</span></span> <span data-ttu-id="8071c-131">Per altre informazioni, vedere [WMCONTAINER ASF Components](wmcontainer-asf-components.md).</span><span class="sxs-lookup"><span data-stu-id="8071c-131">For more information, see [WMContainer ASF Components](wmcontainer-asf-components.md).</span></span>
-   <span data-ttu-id="8071c-132">Si ha familiarità con i codificatori Windows Media e con i vari tipi di codifica, in particolare CBR.</span><span class="sxs-lookup"><span data-stu-id="8071c-132">You are familiar with Windows Media encoders, and the various encoding types, particularly CBR.</span></span> <span data-ttu-id="8071c-133">Per ulteriori informazioni, vedere [codificatori Windows Media](windows-media-encoders.md) .</span><span class="sxs-lookup"><span data-stu-id="8071c-133">For more information, see [Windows Media Encoders](windows-media-encoders.md) .</span></span>
-   <span data-ttu-id="8071c-134">Si ha familiarità con i [buffer multimediali](media-buffers.md) e i flussi di byte: in particolare, le operazioni sui file che usano un flusso di byte e la scrittura del contenuto di un buffer multimediale in un flusso di byte.</span><span class="sxs-lookup"><span data-stu-id="8071c-134">You are familiar with [Media Buffers](media-buffers.md) and byte streams: Specifically, file operations using a byte stream, and writing the contents of a media buffer to a byte stream.</span></span>

## <a name="terminology"></a><span data-ttu-id="8071c-135">Terminologia</span><span class="sxs-lookup"><span data-stu-id="8071c-135">Terminology</span></span>

<span data-ttu-id="8071c-136">Questa esercitazione usa i termini seguenti:</span><span class="sxs-lookup"><span data-stu-id="8071c-136">This tutorial uses the following terms:</span></span>

-   <span data-ttu-id="8071c-137">Tipo di supporto di origine: oggetto tipo di supporto, espone l'interfaccia [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) , che descrive il contenuto del file di input.</span><span class="sxs-lookup"><span data-stu-id="8071c-137">Source media type: Media type object, exposes [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface, which describes the contents of the input file.</span></span>
-   <span data-ttu-id="8071c-138">Profilo audio: oggetto profilo, espone l'interfaccia [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) , che contiene solo flussi audio del file di output.</span><span class="sxs-lookup"><span data-stu-id="8071c-138">Audio profile: Profile object, exposes [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) interface, which contains only audio streams of the output file.</span></span>
-   <span data-ttu-id="8071c-139">Esempio di flusso: supporto di esempio, espone l'interfaccia [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) , che rappresenta i dati multimediali del file di input ottenuti dal codificatore in uno stato compresso.</span><span class="sxs-lookup"><span data-stu-id="8071c-139">Stream sample: Media sample, exposes [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface, represents the input file's media data obtained from the encoder in a compressed state.</span></span>
-   <span data-ttu-id="8071c-140">Oggetto ContentInfo: [oggetto ContentInfo ASF](asf-contentinfo-object.md), espone l'interfaccia [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) , che rappresenta l'oggetto intestazione ASF del file di output.</span><span class="sxs-lookup"><span data-stu-id="8071c-140">ContentInfo object: [ASF ContentInfo Object](asf-contentinfo-object.md), exposes [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) interface, which represents the ASF Header Object of the output file.</span></span>
-   <span data-ttu-id="8071c-141">Data byte stream: oggetto flusso di byte, espone l'interfaccia [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) , che rappresenta l'intera parte dell'oggetto dati ASF del file di output.</span><span class="sxs-lookup"><span data-stu-id="8071c-141">Data byte stream: Byte stream object, exposes [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) interface, which represents the entire ASF Data Object portion of the output file.</span></span>
-   <span data-ttu-id="8071c-142">Pacchetto di dati: esempio di supporto, espone l'interfaccia [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) , generata da [ASF Multiplexer](asf-multiplexer.md); rappresenta un pacchetto di dati ASF che verrà scritto nel flusso di byte di dati.</span><span class="sxs-lookup"><span data-stu-id="8071c-142">Data packet: Media sample, exposes [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface, generated by the [ASF Multiplexer](asf-multiplexer.md); represents an ASF data packet that will be written to the data byte stream.</span></span>
-   <span data-ttu-id="8071c-143">Flusso di byte di output: oggetto flusso di byte, espone l'interfaccia [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) , che contiene il contenuto del file di output.</span><span class="sxs-lookup"><span data-stu-id="8071c-143">Output byte stream: Byte stream object, exposes [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) interface, which contains the contents of the output file.</span></span>

## <a name="1-set-up-the-project"></a><span data-ttu-id="8071c-144">1. configurare il progetto</span><span class="sxs-lookup"><span data-stu-id="8071c-144">1. Set up the Project</span></span>

1.  <span data-ttu-id="8071c-145">Includere le intestazioni seguenti nel file di origine:</span><span class="sxs-lookup"><span data-stu-id="8071c-145">Include the following headers in your source file:</span></span>

    ```C++
    #include <new>
    #include <stdio.h>       // Standard I/O
    #include <windows.h>     // Windows headers
    #include <mfapi.h>       // Media Foundation platform
    #include <wmcontainer.h> // ASF interfaces
    #include <mferror.h>     // Media Foundation error codes
    ```

    

2.  <span data-ttu-id="8071c-146">Collegamento ai file di libreria seguenti:</span><span class="sxs-lookup"><span data-stu-id="8071c-146">Link to the following library files:</span></span>

    -   <span data-ttu-id="8071c-147">mfplat. lib</span><span class="sxs-lookup"><span data-stu-id="8071c-147">mfplat.lib</span></span>
    -   <span data-ttu-id="8071c-148">MF. lib</span><span class="sxs-lookup"><span data-stu-id="8071c-148">mf.lib</span></span>
    -   <span data-ttu-id="8071c-149">mfuuid. lib</span><span class="sxs-lookup"><span data-stu-id="8071c-149">mfuuid.lib</span></span>

3.  <span data-ttu-id="8071c-150">Dichiarare la funzione [SafeRelease](saferelease.md) .</span><span class="sxs-lookup"><span data-stu-id="8071c-150">Declare the [SafeRelease](saferelease.md) function.</span></span>
4.  <span data-ttu-id="8071c-151">Includere la classe CWmaEncoder nel progetto.</span><span class="sxs-lookup"><span data-stu-id="8071c-151">Include the CWmaEncoder class in your project.</span></span> <span data-ttu-id="8071c-152">Per il codice sorgente completo di questa classe, vedere [codice di esempio del codificatore](encoder-example-code.md).</span><span class="sxs-lookup"><span data-stu-id="8071c-152">For the complete source code of this class, see [Encoder Example Code](encoder-example-code.md).</span></span>

## <a name="2-declare-helper-functions"></a><span data-ttu-id="8071c-153">2. dichiarare le funzioni helper</span><span class="sxs-lookup"><span data-stu-id="8071c-153">2. Declare Helper Functions</span></span>

<span data-ttu-id="8071c-154">Questa esercitazione usa le funzioni di supporto seguenti per leggere e scrivere da un flusso di byte.</span><span class="sxs-lookup"><span data-stu-id="8071c-154">This tutorial uses the following helper functions to read and write from a byte stream.</span></span>

-   <span data-ttu-id="8071c-155">`AppendToByteStream`: Accoda il contenuto di un flusso di byte a un altro flusso di byte.</span><span class="sxs-lookup"><span data-stu-id="8071c-155">`AppendToByteStream`: Appends the contents of one byte stream to another byte stream.</span></span>
-   <span data-ttu-id="8071c-156">WriteBufferToByteStream: scrive i dati da un buffer multimediale a un flusso di byte.</span><span class="sxs-lookup"><span data-stu-id="8071c-156">WriteBufferToByteStream: Writes data from a media buffer to a byte stream.</span></span>

<span data-ttu-id="8071c-157">Per ulteriori informazioni, vedere [**IMFByteStream:: Write**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-write).</span><span class="sxs-lookup"><span data-stu-id="8071c-157">For more information, see [**IMFByteStream::Write**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-write).</span></span> <span data-ttu-id="8071c-158">Il codice seguente illustra le funzioni di supporto seguenti:</span><span class="sxs-lookup"><span data-stu-id="8071c-158">The following code shows these helper functions:</span></span>


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



## <a name="3-open-an-audio-file"></a><span data-ttu-id="8071c-159">3. aprire un file audio</span><span class="sxs-lookup"><span data-stu-id="8071c-159">3. Open an Audio File</span></span>

<span data-ttu-id="8071c-160">In questa esercitazione si presuppone che l'applicazione generi audio non compresso per la codifica.</span><span class="sxs-lookup"><span data-stu-id="8071c-160">This tutorial assumes that your application will generate uncompressed audio for encoding.</span></span> <span data-ttu-id="8071c-161">A tale scopo, in questa esercitazione vengono dichiarate due funzioni:</span><span class="sxs-lookup"><span data-stu-id="8071c-161">For that purpose, two functions are declared in this tutorial:</span></span>


```C++
HRESULT OpenAudioFile(PCWSTR pszURL, IMFMediaType **ppAudioFormat);
HRESULT GetNextAudioSample(BOOL *pbEOS, IMFSample **ppSample);
```



<span data-ttu-id="8071c-162">L'implementazione di queste funzioni viene lasciata al lettore.</span><span class="sxs-lookup"><span data-stu-id="8071c-162">The implementation of these functions is left to the reader.</span></span>

-   <span data-ttu-id="8071c-163">La `OpenAudioFile` funzione deve aprire il file multimediale specificato da *pszURL* e restituire un puntatore a un tipo di supporto che descrive un flusso audio.</span><span class="sxs-lookup"><span data-stu-id="8071c-163">The `OpenAudioFile` function should open the media file specified by *pszURL* and return a pointer to a media type that describes an audio stream.</span></span>
-   <span data-ttu-id="8071c-164">La `GetNextAudioSample` funzione deve leggere l'audio PCM non compresso dal file aperto da `OpenAudioFile` .</span><span class="sxs-lookup"><span data-stu-id="8071c-164">The `GetNextAudioSample` function should read uncompressed PCM audio from the file that was opened by `OpenAudioFile`.</span></span> <span data-ttu-id="8071c-165">Quando viene raggiunta la fine del file, *pbEOS* riceve il valore **true**.</span><span class="sxs-lookup"><span data-stu-id="8071c-165">When the end of the file is reached, *pbEOS* receives the value **TRUE**.</span></span> <span data-ttu-id="8071c-166">In caso contrario, *ppSample* riceve un esempio multimediale che contiene il buffer audio.</span><span class="sxs-lookup"><span data-stu-id="8071c-166">Otherwise, *ppSample* receives a media sample that contains the audio buffer.</span></span>

## <a name="4-configure-the-encoder"></a><span data-ttu-id="8071c-167">4. configurare il codificatore</span><span class="sxs-lookup"><span data-stu-id="8071c-167">4. Configure the Encoder</span></span>

<span data-ttu-id="8071c-168">Successivamente, creare il codificatore, configurarlo per produrre esempi di flusso con codifica CBR e negoziare i tipi di supporto di input e di output.</span><span class="sxs-lookup"><span data-stu-id="8071c-168">Next, create the encoder, configure it to produce CBR-encoded stream samples, and negotiate the input and the output media types.</span></span>

<span data-ttu-id="8071c-169">In Media Foundation i codificatori (esporre l'interfaccia [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) ) vengono implementati come [Media Foundation Transforms](media-foundation-transforms.md) (MFT).</span><span class="sxs-lookup"><span data-stu-id="8071c-169">In Media Foundation, encoders (expose the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface) are implemented as [Media Foundation Transforms](media-foundation-transforms.md) (MFT).</span></span>

<span data-ttu-id="8071c-170">In questa esercitazione il codificatore viene implementato nella `CWmaEncoder` classe che fornisce un wrapper per il MFT.</span><span class="sxs-lookup"><span data-stu-id="8071c-170">In this tutorial, the encoder is implemented in the `CWmaEncoder` class that provides a wrapper for the MFT.</span></span> <span data-ttu-id="8071c-171">Per il codice sorgente completo di questa classe, vedere [codice di esempio del codificatore](encoder-example-code.md).</span><span class="sxs-lookup"><span data-stu-id="8071c-171">For the complete source code of this class, see [Encoder Example Code](encoder-example-code.md).</span></span>

> [!Note]  
> <span data-ttu-id="8071c-172">Facoltativamente, è possibile specificare il tipo di codifica come CBR.</span><span class="sxs-lookup"><span data-stu-id="8071c-172">You can optionally specify the encoding type as CBR.</span></span> <span data-ttu-id="8071c-173">Per impostazione predefinita, il codificatore è configurato per usare la codifica CBR.</span><span class="sxs-lookup"><span data-stu-id="8071c-173">By default, the encoder is configured to use CBR encoding.</span></span> <span data-ttu-id="8071c-174">Per altre informazioni, vedere [codifica della velocità in bit costante](constant-bit-rate-encoding.md).</span><span class="sxs-lookup"><span data-stu-id="8071c-174">For more information, see [Constant Bit Rate Encoding](constant-bit-rate-encoding.md).</span></span> <span data-ttu-id="8071c-175">È possibile impostare proprietà aggiuntive a seconda del tipo di codifica. per informazioni sulle proprietà specifiche di una modalità di codifica, vedere [codifica della velocità in bit variabile basata sulla qualità](quality-based-variable-bit-rate--vbr--encoding.md), codifica della velocità in bit variabile non [vincolata](unconstrained-variable-bit-rate--vbr--encoding.md)e [codifica della velocità in bit a variabili](peak-constrained-variable-bit-rate--vbr--encoding.md)vincolate di picco.</span><span class="sxs-lookup"><span data-stu-id="8071c-175">You can set additional properties depending on the type of encoding, for information about the properties that are specific to an encoding mode, see [Quality-Based Variable Bit Rate Encoding](quality-based-variable-bit-rate--vbr--encoding.md), [Unconstrained Variable Bit Rate Encoding](unconstrained-variable-bit-rate--vbr--encoding.md), and [Peak-Constrained Variable Bit Rate Encoding](peak-constrained-variable-bit-rate--vbr--encoding.md).</span></span>

 


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



## <a name="5-create-the-asf-contentinfo-object"></a><span data-ttu-id="8071c-176">5. creare l'oggetto ContentInfo ASF.</span><span class="sxs-lookup"><span data-stu-id="8071c-176">5. Create the ASF ContentInfo object.</span></span>

<span data-ttu-id="8071c-177">L' [oggetto ContentInfo ASF](asf-contentinfo-object.md) contiene informazioni sui vari oggetti Header del file di output.</span><span class="sxs-lookup"><span data-stu-id="8071c-177">The [ASF ContentInfo Object](asf-contentinfo-object.md) contains information about the various header objects of the output file.</span></span>

<span data-ttu-id="8071c-178">Per prima cosa, creare un profilo ASF per il flusso audio:</span><span class="sxs-lookup"><span data-stu-id="8071c-178">First, create an ASF profile for the audio stream:</span></span>

1.  <span data-ttu-id="8071c-179">Chiamare [**MFCreateASFProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile) per creare un oggetto profilo ASF vuoto.</span><span class="sxs-lookup"><span data-stu-id="8071c-179">Call [**MFCreateASFProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile) to create an empty ASF profile object.</span></span> <span data-ttu-id="8071c-180">Il profilo ASF espone l'interfaccia [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) .</span><span class="sxs-lookup"><span data-stu-id="8071c-180">The ASF profile exposes the [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) interface.</span></span> <span data-ttu-id="8071c-181">Per ulteriori informazioni, vedere [creazione e configurazione di flussi ASF](creating-and-configuring-asf-streams.md).</span><span class="sxs-lookup"><span data-stu-id="8071c-181">For more information, see [Creating and Configuring ASF Streams](creating-and-configuring-asf-streams.md).</span></span>
2.  <span data-ttu-id="8071c-182">Ottenere il formato audio codificato dall' `CWmaEncoder` oggetto.</span><span class="sxs-lookup"><span data-stu-id="8071c-182">Get the encoded audio format from the `CWmaEncoder` object.</span></span>
3.  <span data-ttu-id="8071c-183">Chiamare [**IMFASFProfile:: CreateStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstream) per creare un nuovo flusso per il profilo ASF.</span><span class="sxs-lookup"><span data-stu-id="8071c-183">Call [**IMFASFProfile::CreateStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstream) to create a new stream for the ASF profile.</span></span> <span data-ttu-id="8071c-184">Passare un puntatore all'interfaccia [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) , che rappresenta il formato del flusso.</span><span class="sxs-lookup"><span data-stu-id="8071c-184">Pass in a pointer to the [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface, which represents the stream format.</span></span>
4.  <span data-ttu-id="8071c-185">Chiamare [**IMFASFStreamConfig:: SetStreamNumber**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-setstreamnumber) per assegnare un identificatore di flusso.</span><span class="sxs-lookup"><span data-stu-id="8071c-185">Call [**IMFASFStreamConfig::SetStreamNumber**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-setstreamnumber) to assign a stream identifier.</span></span>
5.  <span data-ttu-id="8071c-186">Impostare i parametri "leaky bucket" impostando l'attributo [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) nell'oggetto flusso.</span><span class="sxs-lookup"><span data-stu-id="8071c-186">Set the "leaky bucket" parameters by setting the [**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) attribute on the stream object.</span></span>
6.  <span data-ttu-id="8071c-187">Chiamare [**IMFASFProfile:: sestream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream) per aggiungere il nuovo flusso al profilo.</span><span class="sxs-lookup"><span data-stu-id="8071c-187">Call [**IMFASFProfile::SetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream) to add the new stream to the profile.</span></span>

<span data-ttu-id="8071c-188">A questo punto, creare l'oggetto ContentInfo ASF come segue:</span><span class="sxs-lookup"><span data-stu-id="8071c-188">Now create the ASF ContentInfo object as follows:</span></span>

1.  <span data-ttu-id="8071c-189">Chiamare [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) per creare un oggetto ContentInfo vuoto.</span><span class="sxs-lookup"><span data-stu-id="8071c-189">Call [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) to create an empty ContentInfo object.</span></span>
2.  <span data-ttu-id="8071c-190">Chiamare [**IMFASFContentInfo:: seprofile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) per impostare il profilo ASF.</span><span class="sxs-lookup"><span data-stu-id="8071c-190">Call [**IMFASFContentInfo::SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) to set the ASF profile.</span></span>

<span data-ttu-id="8071c-191">Il codice seguente illustra questi passaggi:</span><span class="sxs-lookup"><span data-stu-id="8071c-191">The following code shows these steps:</span></span>


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



## <a name="6-create-the-asf-multiplexer"></a><span data-ttu-id="8071c-192">6. creare il multiplexer ASF</span><span class="sxs-lookup"><span data-stu-id="8071c-192">6. Create the ASF Multiplexer</span></span>

<span data-ttu-id="8071c-193">Il [multiplexer ASF](asf-multiplexer.md) genera pacchetti di dati ASF.</span><span class="sxs-lookup"><span data-stu-id="8071c-193">The [ASF Multiplexer](asf-multiplexer.md) generates ASF data packets.</span></span>

1.  <span data-ttu-id="8071c-194">Chiamare [**MFCreateASFMultiplexer**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmultiplexer) per creare il multiplexing ASF.</span><span class="sxs-lookup"><span data-stu-id="8071c-194">Call [**MFCreateASFMultiplexer**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmultiplexer) to create the ASF multiplexer.</span></span>
2.  <span data-ttu-id="8071c-195">Chiamare [**IMFASFMultiplexer:: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) per inizializzare il multiplexer.</span><span class="sxs-lookup"><span data-stu-id="8071c-195">Call [**IMFASFMultiplexer::Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) to initialize the multiplexer.</span></span> <span data-ttu-id="8071c-196">Passare un puntatore all'oggetto informazioni sul contenuto ASF, che è stato creato nella sezione precedente.</span><span class="sxs-lookup"><span data-stu-id="8071c-196">Pass in a pointer to the ASF Content Info object, which was created in the previous section.</span></span>
3.  <span data-ttu-id="8071c-197">Chiamare [**IMFASFMultiplexer:: Seflags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-setflags) per impostare il flag **MFASF \_ multiplexer \_ AutoAdjust \_ bitrate** .</span><span class="sxs-lookup"><span data-stu-id="8071c-197">Call [**IMFASFMultiplexer::SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-setflags) to set the **MFASF\_MULTIPLEXER\_AUTOADJUST\_BITRATE** flag.</span></span> <span data-ttu-id="8071c-198">Quando si usa questa impostazione, il multiplexer regola automaticamente la velocità in bit del contenuto ASF in modo che corrisponda alle caratteristiche dei flussi sottoposto a multiplexing.</span><span class="sxs-lookup"><span data-stu-id="8071c-198">When this setting is used, the multiplexer automatically adjusts the bit rate of the ASF content to match the characteristics of the streams being multiplexed.</span></span>


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



## <a name="7-generate-new-asf-data-packets"></a><span data-ttu-id="8071c-199">7. generare nuovi pacchetti di dati ASF</span><span class="sxs-lookup"><span data-stu-id="8071c-199">7. Generate New ASF Data Packets</span></span>

<span data-ttu-id="8071c-200">Generare quindi i pacchetti di dati ASF per il nuovo file.</span><span class="sxs-lookup"><span data-stu-id="8071c-200">Next, generate ASF data packets for the new file.</span></span> <span data-ttu-id="8071c-201">Questi pacchetti di dati costituiranno l'oggetto dati ASF finale per il nuovo file.</span><span class="sxs-lookup"><span data-stu-id="8071c-201">These data packets will constitute the final ASF Data Object for the new file.</span></span> <span data-ttu-id="8071c-202">Per generare nuovi pacchetti di dati ASF:</span><span class="sxs-lookup"><span data-stu-id="8071c-202">To generate new ASF data packets:</span></span>

1.  <span data-ttu-id="8071c-203">Chiamare [**MFCreateTempFile**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatetempfile) per creare un flusso di byte temporaneo che contenga i pacchetti di dati ASF.</span><span class="sxs-lookup"><span data-stu-id="8071c-203">Call [**MFCreateTempFile**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatetempfile) to create a temporary byte stream to hold the ASF data packets.</span></span>
2.  <span data-ttu-id="8071c-204">Chiamare la funzione definita dall'applicazione `GetNextAudioSample` per ottenere i dati audio non compressi per il codificatore.</span><span class="sxs-lookup"><span data-stu-id="8071c-204">Call the application-defined `GetNextAudioSample` function to get uncompressed audio data for the encoder.</span></span>
3.  <span data-ttu-id="8071c-205">Passare l'audio non compresso al codificatore per la compressione.</span><span class="sxs-lookup"><span data-stu-id="8071c-205">Pass the uncompressed audio to the encoder for compression.</span></span> <span data-ttu-id="8071c-206">Per altre informazioni, vedere [elaborazione dei dati nel codificatore](processing-data-in-the-encoder.md)</span><span class="sxs-lookup"><span data-stu-id="8071c-206">For more information, see [Processing Data in the Encoder](processing-data-in-the-encoder.md)</span></span>
4.  <span data-ttu-id="8071c-207">Chiamare [**IMFASFMultiplexer::P rocesssample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) per inviare i campioni audio compressi al multiplexer ASF per la pacchettizzazione.</span><span class="sxs-lookup"><span data-stu-id="8071c-207">Call [**IMFASFMultiplexer::ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) to send the compressed audio samples to the ASF multiplexer for packetization.</span></span>
5.  <span data-ttu-id="8071c-208">Ottenere i pacchetti ASF dal multiplexer e scriverli nel flusso di byte temporaneo.</span><span class="sxs-lookup"><span data-stu-id="8071c-208">Get the ASF packets from the multiplexer and write them to the temporary byte stream.</span></span> <span data-ttu-id="8071c-209">Per ulteriori informazioni, vedere [generazione di nuovi pacchetti di dati ASF](generating-new-asf-data-packets.md).</span><span class="sxs-lookup"><span data-stu-id="8071c-209">For more information, see [Generating New ASF Data Packets](generating-new-asf-data-packets.md).</span></span>
6.  <span data-ttu-id="8071c-210">Quando si raggiunge la fine del flusso di origine, svuotare il codificatore ed estrarre gli esempi compressi rimanenti dal codificatore.</span><span class="sxs-lookup"><span data-stu-id="8071c-210">When you reach the end of the source stream, drain the encoder and pull the remaining compressed samples from the encoder.</span></span> <span data-ttu-id="8071c-211">Per altre informazioni sullo svuotamento di un MFT, vedere [modello di elaborazione MFT di base](basic-mft-processing-model.md).</span><span class="sxs-lookup"><span data-stu-id="8071c-211">For more information about draining an MFT, see [Basic MFT Processing Model](basic-mft-processing-model.md).</span></span>
7.  <span data-ttu-id="8071c-212">Dopo che tutti i campioni sono stati inviati al multiplexer, chiamare [**IMFASFMultiplexer:: Flush**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-flush) ed estrarre i pacchetti ASF rimanenti dal multiplexer.</span><span class="sxs-lookup"><span data-stu-id="8071c-212">After all samples are sent to the multiplexer, call [**IMFASFMultiplexer::Flush**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-flush) and pull the remaining ASF packets from the multiplexer.</span></span>
8.  <span data-ttu-id="8071c-213">Chiamare [**IMFASFMultiplexer:: end**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-end).</span><span class="sxs-lookup"><span data-stu-id="8071c-213">Call [**IMFASFMultiplexer::End**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-end).</span></span>

<span data-ttu-id="8071c-214">Il codice seguente genera pacchetti di dati ASF.</span><span class="sxs-lookup"><span data-stu-id="8071c-214">The following code generates ASF data packets.</span></span> <span data-ttu-id="8071c-215">La funzione restituisce un puntatore a un flusso di byte che contiene l'oggetto dati ASF.</span><span class="sxs-lookup"><span data-stu-id="8071c-215">The function returns a pointer to a byte stream that contains the ASF Data Object.</span></span>


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



<span data-ttu-id="8071c-216">Il codice per la `GenerateASFDataPackets` funzione è illustrato nell'argomento [generazione di nuovi pacchetti di dati ASF](generating-new-asf-data-packets.md).</span><span class="sxs-lookup"><span data-stu-id="8071c-216">Code for the `GenerateASFDataPackets` function is shown in the topic [Generating New ASF Data Packets](generating-new-asf-data-packets.md).</span></span>

## <a name="8-write-the-asf-file"></a><span data-ttu-id="8071c-217">8. scrivere il file ASF</span><span class="sxs-lookup"><span data-stu-id="8071c-217">8. Write the ASF File</span></span>

<span data-ttu-id="8071c-218">Quindi, scrivere l'intestazione ASF in un buffer multimediale chiamando [**IMFASFContentInfo:: GenerateHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader).</span><span class="sxs-lookup"><span data-stu-id="8071c-218">Next, write the ASF header to a media buffer by calling [**IMFASFContentInfo::GenerateHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader).</span></span> <span data-ttu-id="8071c-219">Questo metodo converte i dati archiviati nell'oggetto ContentInfo in dati binari nel formato dell'oggetto intestazione ASF.</span><span class="sxs-lookup"><span data-stu-id="8071c-219">This method converts data stored in the ContentInfo object into binary data in ASF Header Object format.</span></span> <span data-ttu-id="8071c-220">Per ulteriori informazioni, vedere [generazione di un nuovo oggetto intestazione ASF](generating-a-new-asf-header-object.md).</span><span class="sxs-lookup"><span data-stu-id="8071c-220">For more information, see [Generating a New ASF Header Object](generating-a-new-asf-header-object.md).</span></span>

<span data-ttu-id="8071c-221">Dopo la generazione del nuovo oggetto intestazione ASF, creare un flusso di byte per il file di output.</span><span class="sxs-lookup"><span data-stu-id="8071c-221">After the new ASF Header Object has been generated, create a byte stream for the output file.</span></span> <span data-ttu-id="8071c-222">Prima di tutto, scrivere l'oggetto Header nel flusso di byte di output.</span><span class="sxs-lookup"><span data-stu-id="8071c-222">First write the Header Object to the output byte stream.</span></span> <span data-ttu-id="8071c-223">Seguire l'oggetto Header con l'oggetto dati contenuto nel flusso di byte di dati.</span><span class="sxs-lookup"><span data-stu-id="8071c-223">Follow the Header Object with the Data Object contained in the data byte stream.</span></span>


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



## <a name="9-define-the-entry-point-function"></a><span data-ttu-id="8071c-224">9. definire la funzione Entry-Point</span><span class="sxs-lookup"><span data-stu-id="8071c-224">9. Define the Entry-Point Function</span></span>

<span data-ttu-id="8071c-225">È ora possibile inserire i passaggi precedenti in un'applicazione completa.</span><span class="sxs-lookup"><span data-stu-id="8071c-225">Now you can put the previous steps together into a complete application.</span></span> <span data-ttu-id="8071c-226">Prima di usare uno degli oggetti Media Foundation, inizializzare la piattaforma Media Foundation chiamando [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup).</span><span class="sxs-lookup"><span data-stu-id="8071c-226">Before using any of the Media Foundation objects, initialize the Media Foundation platform by calling [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup).</span></span> <span data-ttu-id="8071c-227">Al termine, chiamare [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown).</span><span class="sxs-lookup"><span data-stu-id="8071c-227">When you are done, call [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown).</span></span> <span data-ttu-id="8071c-228">Per ulteriori informazioni, vedere [inizializzazione di Media Foundation](initializing-media-foundation.md).</span><span class="sxs-lookup"><span data-stu-id="8071c-228">For more information, see [Initializing Media Foundation](initializing-media-foundation.md).</span></span>

<span data-ttu-id="8071c-229">Nel codice seguente viene illustrata l'applicazione console completa.</span><span class="sxs-lookup"><span data-stu-id="8071c-229">The following code shows the complete console application.</span></span> <span data-ttu-id="8071c-230">L'argomento della riga di comando specifica il nome del file da convertire e il nome del nuovo file audio.</span><span class="sxs-lookup"><span data-stu-id="8071c-230">The command-line argument specifies the name of the file to convert and the name of the new audio file.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="8071c-231">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8071c-231">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8071c-232">Componenti ASF WMContainer</span><span class="sxs-lookup"><span data-stu-id="8071c-232">WMContainer ASF Components</span></span>](wmcontainer-asf-components.md)
</dt> <dt>

[<span data-ttu-id="8071c-233">Supporto ASF in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8071c-233">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



