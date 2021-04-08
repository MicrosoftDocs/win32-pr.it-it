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
# <a name="tutorial-1-pass-windows-media-encoding"></a><span data-ttu-id="0c1b0-104">Esercitazione: codifica Windows Media da 1 passaggio</span><span class="sxs-lookup"><span data-stu-id="0c1b0-104">Tutorial: 1-Pass Windows Media Encoding</span></span>

<span data-ttu-id="0c1b0-105">La codifica si riferisce al processo di conversione di file multimediali digitali da un formato a un altro.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-105">Encoding refers to the process of converting digital media from one format into another.</span></span> <span data-ttu-id="0c1b0-106">Ad esempio, la conversione di audio MP3 nel formato Windows Media Audio come definito dalla specifica ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="0c1b0-106">For example, converting MP3 audio into Windows Media Audio format as defined by the Advanced Systems Format (ASF) specification.</span></span>

<span data-ttu-id="0c1b0-107">**Nota**  La specifica ASF definisce un tipo di contenitore per il file di output (WMA o WMV) che può contenere dati multimediali in qualsiasi formato, compresso o decompresso.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-107">**Note**  The ASF specification defines a container type for the output file (.wma or .wmv) that can contain media data in any format, compressed or uncompressed.</span></span> <span data-ttu-id="0c1b0-108">Ad esempio, un contenitore ASF, ad esempio un file con estensione WMA, può contenere dati multimediali in formato MP3.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-108">For example, an ASF container such as a .wma file can contain media data in MP3 format.</span></span> <span data-ttu-id="0c1b0-109">Il processo di codifica converte il formato effettivo dei dati contenuti all'interno del file.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-109">The encoding process converts the actual format of the data contained within the file.</span></span>

<span data-ttu-id="0c1b0-110">In questa esercitazione viene illustrata la codifica di un'origine di input non protetta da DRM in contenuto Windows Media e la scrittura dei dati in un nuovo file ASF (WM \* ) utilizzando i componenti ASF del livello pipeline.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-110">This tutorial demonstrates encoding clear content (non DRM-protected) input source into Windows Media content and writing the data in a new ASF file (.wm\*) by using Pipeline Layer ASF Components.</span></span> <span data-ttu-id="0c1b0-111">Questi componenti verranno utilizzati per compilare una topologia di codifica parziale, che verrà controllata da un'istanza della sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-111">These components will be used to build a partial encoding topology, which will be controlled by an instance of the Media Session.</span></span>

<span data-ttu-id="0c1b0-112">In questa esercitazione si creerà un'applicazione console che accetta i nomi dei file di input e di output e la modalità di codifica come argomenti.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-112">In this tutorial, you will create a console application that takes the input and output filenames, and the encoding mode as arguments.</span></span> <span data-ttu-id="0c1b0-113">Il file di input può trovarsi in un formato multimediale compresso o non compresso.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-113">The input file can be in a compressed or an uncompressed media format.</span></span> <span data-ttu-id="0c1b0-114">Le modalità di codifica valide sono "CBR" (velocità in bit costante) o "VBR" (velocità in bit variabile).</span><span class="sxs-lookup"><span data-stu-id="0c1b0-114">The valid encoding modes are "CBR" (constant bit rate) or "VBR" (variable bit rate).</span></span> <span data-ttu-id="0c1b0-115">L'applicazione crea un'origine multimediale per rappresentare l'origine specificata dal nome file di input e il sink di file ASF per archiviare il contenuto codificato del file di origine in un file ASF.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-115">The application creates a media source to represent the source specified by the input filename, and the ASF file sink to archive the encoded contents of source file into an ASF file.</span></span> <span data-ttu-id="0c1b0-116">Per semplificare l'implementazione dello scenario, il file di output avrà un solo flusso audio e un flusso video.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-116">To keep the scenario simple to implement, the output file will have only one audio stream and one video stream.</span></span> <span data-ttu-id="0c1b0-117">L'applicazione inserisce il codec Windows Media Audio 9,1 Professional per la conversione del formato del flusso audio e il codec Windows Media Video 9 per il flusso video.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-117">The application inserts the Windows Media Audio 9.1 Professional codec for the audio stream format conversion and Windows Media Video 9 codec for the video stream.</span></span>

<span data-ttu-id="0c1b0-118">Per la codifica della velocità in bit costante, prima dell'inizio della sessione di codifica, il codificatore deve essere a conoscenza della velocità in bit di destinazione che deve raggiungere.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-118">For constant bit rate encoding, before the encoding session begins, the encoder must know the target bit rate that it must achieve.</span></span> <span data-ttu-id="0c1b0-119">In questa esercitazione, per la modalità "CBR", l'applicazione usa la velocità in bit disponibile con il primo tipo di supporto di output recuperato dal codificatore durante la negoziazione del tipo di supporto come velocità in bit di destinazione.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-119">In this tutorial, for "CBR" mode, the application uses the bit rate available with the first output media type that is retrieved from the encoder during media type negotiation as the target bit rate.</span></span> <span data-ttu-id="0c1b0-120">Per la codifica della velocità in bit variabile, in questa esercitazione viene illustrata la codifica con velocità in bit variabile impostando un livello di qualità.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-120">For variable bit rate encoding, this tutorial demonstrates encoding with variable bit rate by setting a quality level.</span></span> <span data-ttu-id="0c1b0-121">I flussi audio vengono codificati a livello di qualità 98 e flussi video a livello di qualità 95.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-121">The audio streams are encoded at the quality level of 98 and video streams at the quality level of 95.</span></span>

<span data-ttu-id="0c1b0-122">Nella procedura riportata di seguito vengono riepilogati i passaggi per codificare il contenuto di Windows Media in un contenitore ASF utilizzando una modalità di codifica a 1 passaggio.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-122">The following procedure summarizes the steps for encoding Windows Media content in an ASF container by using a 1-pass encoding mode.</span></span>

1.  <span data-ttu-id="0c1b0-123">Creare un'origine multimediale per l'oggetto specificato utilizzando il resolver di origine.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-123">Create a media source for the specified by using the source resolver.</span></span>
2.  <span data-ttu-id="0c1b0-124">Enumerare i flussi nell'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-124">Enumerate the streams in the media source.</span></span>
3.  <span data-ttu-id="0c1b0-125">Creare il sink multimediale ASF e aggiungere i sink di flusso a seconda dei flussi nell'origine multimediale che devono essere codificati.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-125">Create the ASF media sink and add stream sinks depending on the streams in the media source that need to be encoded.</span></span>
4.  <span data-ttu-id="0c1b0-126">Configurare il sink multimediale con le proprietà di codifica obbligatorie.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-126">Configure the media sink with the required encoding properties.</span></span>
5.  <span data-ttu-id="0c1b0-127">Creare i codificatori Windows Media per i flussi nel file di output.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-127">Create the Windows Media encoders for the streams in the output file.</span></span>
6.  <span data-ttu-id="0c1b0-128">Configurare i codificatori con le proprietà impostate nel sink multimediale.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-128">Configure the encoders with the properties that are set on the media sink.</span></span>
7.  <span data-ttu-id="0c1b0-129">Compilazione di una topologia di codifica parziale.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-129">Build a partial encoding topology.</span></span>
8.  <span data-ttu-id="0c1b0-130">Creare un'istanza della sessione multimediale e impostare la topologia nella sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-130">Instantiate the Media Session and set the topology on the Media Session.</span></span>
9.  <span data-ttu-id="0c1b0-131">Avviare la sessione di codifica controllando la sessione multimediale e ottenendo tutti gli eventi rilevanti dalla sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-131">Start the encoding session by controlling the Media Session and getting all the relevant events from the Media Session.</span></span>
10. <span data-ttu-id="0c1b0-132">Per la codifica VBR, ottenere i valori delle proprietà di codifica dal codificatore e impostarli nel sink multimediale.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-132">For VBR encoding, get the encoding property values from the encoder and set them on the media sink.</span></span>
11. <span data-ttu-id="0c1b0-133">Chiudere e arrestare la sessione di codifica.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-133">Close and shutdown the encoding session.</span></span>

<span data-ttu-id="0c1b0-134">Questa esercitazione contiene le sezioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="0c1b0-134">This tutorial contains the following sections:</span></span>

-   [<span data-ttu-id="0c1b0-135">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="0c1b0-135">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="0c1b0-136">Configurare il progetto</span><span class="sxs-lookup"><span data-stu-id="0c1b0-136">Set up the Project</span></span>](#set-up-the-project)
-   [<span data-ttu-id="0c1b0-137">Creare l'origine multimediale</span><span class="sxs-lookup"><span data-stu-id="0c1b0-137">Create the Media Source</span></span>](#create-the-media-source)
-   [<span data-ttu-id="0c1b0-138">Creare il sink di file ASF</span><span class="sxs-lookup"><span data-stu-id="0c1b0-138">Create the ASF File Sink</span></span>](#create-the-asf-file-sink)
    -   [<span data-ttu-id="0c1b0-139">Creazione dell'oggetto profilo ASF</span><span class="sxs-lookup"><span data-stu-id="0c1b0-139">Create the ASF Profile Object</span></span>](#create-the-asf-profile-object)
    -   [<span data-ttu-id="0c1b0-140">Creare un tipo di supporto audio compresso</span><span class="sxs-lookup"><span data-stu-id="0c1b0-140">Create a Compressed Audio Media Type</span></span>](#create-a-compressed-audio-media-type)
    -   [<span data-ttu-id="0c1b0-141">Creare un tipo di supporto video compresso</span><span class="sxs-lookup"><span data-stu-id="0c1b0-141">Create a Compressed Video Media Type</span></span>](#create-a-compressed-video-media-type)
    -   [<span data-ttu-id="0c1b0-142">Creare l'oggetto ContentInfo ASF</span><span class="sxs-lookup"><span data-stu-id="0c1b0-142">Create the ASF ContentInfo Object</span></span>](#create-the-asf-contentinfo-object)
    -   [<span data-ttu-id="0c1b0-143">Creare il sink di file ASF</span><span class="sxs-lookup"><span data-stu-id="0c1b0-143">Create the ASF File Sink</span></span>](#create-the-asf-file-sink)
-   [<span data-ttu-id="0c1b0-144">Compilare la topologia di codifica parziale</span><span class="sxs-lookup"><span data-stu-id="0c1b0-144">Build the Partial Encoding Topology</span></span>](#build-the-partial-encoding-topology)
    -   [<span data-ttu-id="0c1b0-145">Creare il nodo topologia di origine per l'origine multimediale</span><span class="sxs-lookup"><span data-stu-id="0c1b0-145">Create the Source Topology Node for the Media Source</span></span>](#create-the-source-topology-node-for-the-media-source)
    -   [<span data-ttu-id="0c1b0-146">Creare un'istanza dei codificatori necessari e creare i nodi di trasformazione</span><span class="sxs-lookup"><span data-stu-id="0c1b0-146">Instantiate the Required Encoders and Create the Transform Nodes</span></span>](#instantiate-the-required-encoders-and-create-the-transform-nodes)
    -   [<span data-ttu-id="0c1b0-147">Creare i nodi della topologia di output per il sink di file</span><span class="sxs-lookup"><span data-stu-id="0c1b0-147">Create the Output Topology Nodes for the File Sink</span></span>](#create-the-output-topology-nodes-for-the-file-sink)
    -   [<span data-ttu-id="0c1b0-148">Connettere i nodi di origine, trasformazione e sink</span><span class="sxs-lookup"><span data-stu-id="0c1b0-148">Connect the Source, Transform, and Sink Nodes</span></span>](#connect-the-source-transform-and-sink-nodes)
-   [<span data-ttu-id="0c1b0-149">Gestione della sessione di codifica</span><span class="sxs-lookup"><span data-stu-id="0c1b0-149">Handling the Encoding Session</span></span>](#handling-the-encoding-session)
-   [<span data-ttu-id="0c1b0-150">Aggiornare le proprietà di codifica nel sink di file</span><span class="sxs-lookup"><span data-stu-id="0c1b0-150">Update Encoding Properties in the File Sink</span></span>](#update-encoding-properties-in-the-file-sink)
-   [<span data-ttu-id="0c1b0-151">Implementare Main</span><span class="sxs-lookup"><span data-stu-id="0c1b0-151">Implement Main</span></span>](#implement-main)
-   [<span data-ttu-id="0c1b0-152">Testare il file di output</span><span class="sxs-lookup"><span data-stu-id="0c1b0-152">Test the Output File</span></span>](#test-the-output-file)
-   [<span data-ttu-id="0c1b0-153">Codici di errore comuni e suggerimenti per il debug</span><span class="sxs-lookup"><span data-stu-id="0c1b0-153">Common Error Codes and Debugging Tips</span></span>](#common-error-codes-and-debugging-tips)
-   [<span data-ttu-id="0c1b0-154">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0c1b0-154">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="0c1b0-155">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="0c1b0-155">Prerequisites</span></span>

<span data-ttu-id="0c1b0-156">Nell’esercitazione si presuppongono le condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="0c1b0-156">This tutorial assumes the following:</span></span>

-   <span data-ttu-id="0c1b0-157">Si ha familiarità con la [struttura dei file ASF](asf-file-structure.md), i [componenti ASF del livello Pipeline](pipeline-layer-asf-components.md) forniti da Media Foundation per lavorare con gli oggetti ASF.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-157">You are familiar with the [ASF File Structure](asf-file-structure.md), the [Pipeline Layer ASF Components](pipeline-layer-asf-components.md) provided by Media Foundation to work with ASF Objects.</span></span> <span data-ttu-id="0c1b0-158">Questi componenti includono gli oggetti seguenti:</span><span class="sxs-lookup"><span data-stu-id="0c1b0-158">These components include the following objects:</span></span>
    -   [<span data-ttu-id="0c1b0-159">Origini supporti</span><span class="sxs-lookup"><span data-stu-id="0c1b0-159">Media Sources</span></span>](media-sources.md)

        <span data-ttu-id="0c1b0-160">**Nota**  Se si esegue la transclassificazione (convertendo un file di velocità in bit superiore in un file con velocità in bit inferiore senza modificare i formati), si userà l' [origine dei supporti ASF](asf-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="0c1b0-160">**Note**  If you are performing transrating (converting a higher bit-rate file to a lower bit-rate file without changing formats), you will use the [ASF Media Source](asf-media-source.md).</span></span>

    -   [<span data-ttu-id="0c1b0-161">Codificatori Windows Media</span><span class="sxs-lookup"><span data-stu-id="0c1b0-161">Windows Media Encoders</span></span>](windows-media-encoders.md)
    -   [<span data-ttu-id="0c1b0-162">Sink di supporti ASF</span><span class="sxs-lookup"><span data-stu-id="0c1b0-162">ASF Media Sinks</span></span>](asf-media-sinks.md)
    -   [<span data-ttu-id="0c1b0-163">Oggetto ContentInfo ASF</span><span class="sxs-lookup"><span data-stu-id="0c1b0-163">ASF ContentInfo Object</span></span>](asf-contentinfo-object.md)
    -   [<span data-ttu-id="0c1b0-164">Profilo ASF</span><span class="sxs-lookup"><span data-stu-id="0c1b0-164">ASF Profile</span></span>](asf-profile.md)

-   <span data-ttu-id="0c1b0-165">Si ha familiarità con i codificatori Windows Media e i vari tipi di codifica, in particolare la [codifica della velocità in bit costante](constant-bit-rate-encoding.md) e la [codifica della velocità in bit variabile basata sulla qualità](quality-based-variable-bit-rate--vbr--encoding.md).</span><span class="sxs-lookup"><span data-stu-id="0c1b0-165">You are familiar with Windows Media encoders, and the various encoding types, particularly [Constant Bit Rate Encoding](constant-bit-rate-encoding.md) and [Quality-Based Variable Bit Rate Encoding](quality-based-variable-bit-rate--vbr--encoding.md).</span></span>
-   <span data-ttu-id="0c1b0-166">Si ha familiarità con le operazioni del codificatore MFT.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-166">You are familiar with encoder MFT operations.</span></span> <span data-ttu-id="0c1b0-167">In particolare, creazione di un'istanza del codificatore e impostazione dei tipi di input e di output nel codificatore.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-167">Specifically, creating an instance of the encoder and setting input and output types on the encoder.</span></span>
-   <span data-ttu-id="0c1b0-168">Si ha familiarità con gli oggetti della topologia e come creare una topologia di codifica.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-168">You are familiar with topology objects and how to build an encoding topology.</span></span> <span data-ttu-id="0c1b0-169">Per ulteriori informazioni sulle topologie e sui nodi della topologia, vedere [creazione](creating-topologies.md)di topologie.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-169">For more information about topologies and topology nodes, see [Creating Topologies](creating-topologies.md).</span></span>
-   <span data-ttu-id="0c1b0-170">Si ha familiarità con il modello di eventi della [sessione multimediale](media-session.md)e le operazioni di controllo di flusso.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-170">You are familiar with [Media Session](media-session.md)'s event model and the flow control operations.</span></span> <span data-ttu-id="0c1b0-171">Per informazioni, vedere [eventi della sessione multimediale](media-session-events.md).</span><span class="sxs-lookup"><span data-stu-id="0c1b0-171">For information, see [Media Session Events](media-session-events.md).</span></span>

## <a name="set-up-the-project"></a><span data-ttu-id="0c1b0-172">Configurare il progetto</span><span class="sxs-lookup"><span data-stu-id="0c1b0-172">Set up the Project</span></span>

1.  <span data-ttu-id="0c1b0-173">Includere le intestazioni seguenti nel file di origine:</span><span class="sxs-lookup"><span data-stu-id="0c1b0-173">Include the following headers in your source file:</span></span>

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

    

2.  <span data-ttu-id="0c1b0-174">Collegamento ai file di libreria seguenti:</span><span class="sxs-lookup"><span data-stu-id="0c1b0-174">Link to the following library files:</span></span>

    ```C++
    // The required link libraries 
    #pragma comment(lib, "mfplat")
    #pragma comment(lib, "mf")
    #pragma comment(lib, "mfuuid")
    #pragma comment(lib, "msdmo")
    #pragma comment(lib, "strmiids")
    #pragma comment(lib, "propsys")
    
    ```

    

3.  <span data-ttu-id="0c1b0-175">Dichiarare la funzione [SafeRelease](saferelease.md) .</span><span class="sxs-lookup"><span data-stu-id="0c1b0-175">Declare the [SafeRelease](saferelease.md) function.</span></span>

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

    

4.  <span data-ttu-id="0c1b0-176">Dichiarare l' \_ enumerazione della modalità di codifica per definire i tipi di codifica CBR e VBR.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-176">Declare the ENCODING\_MODE enumeration to define CBR and VBR encoding types.</span></span>

    ```C++
    // Encoding mode
    typedef enum ENCODING_MODE {
      NONE  = 0x00000000,
      CBR   = 0x00000001,
      VBR   = 0x00000002,
    } ;
    
    ```

    

5.  <span data-ttu-id="0c1b0-177">Definire una costante per la finestra del buffer per un flusso video.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-177">Define a constant for buffer window for a video stream.</span></span>

    ```C++
    // Video buffer window
    const INT32 VIDEO_WINDOW_MSEC = 3000;
    
    ```

    

## <a name="create-the-media-source"></a><span data-ttu-id="0c1b0-178">Creare l'origine multimediale</span><span class="sxs-lookup"><span data-stu-id="0c1b0-178">Create the Media Source</span></span>

<span data-ttu-id="0c1b0-179">Creare un'origine multimediale per l'origine di input.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-179">Create a media source for the input source.</span></span> <span data-ttu-id="0c1b0-180">Media Foundation fornisce origini multimediali predefinite per diversi formati multimediali: MP3, MP4/3GP, AVI/WAVE.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-180">Media Foundation provides built-in media sources for various media formats: MP3, MP4/3GP, AVI/WAVE.</span></span> <span data-ttu-id="0c1b0-181">Per informazioni sui formati supportati da Media Foundation, vedere [formati multimediali supportati in Media Foundation](supported-media-formats-in-media-foundation.md).</span><span class="sxs-lookup"><span data-stu-id="0c1b0-181">For information about the formats supported by Media Foundation, see [Supported Media Formats in Media Foundation](supported-media-formats-in-media-foundation.md).</span></span>

<span data-ttu-id="0c1b0-182">Per creare l'origine multimediale, usare il [resolver di origine](source-resolver.md).</span><span class="sxs-lookup"><span data-stu-id="0c1b0-182">To create the media source, use the [Source Resolver](source-resolver.md).</span></span> <span data-ttu-id="0c1b0-183">Questo oggetto analizza l'URL specificato per il file di origine e crea l'origine multimediale appropriata.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-183">This object analyzes the URL that was specified for the source file and creates the appropriate media source.</span></span>

<span data-ttu-id="0c1b0-184">Effettuare le chiamate seguenti:</span><span class="sxs-lookup"><span data-stu-id="0c1b0-184">Make the following calls:</span></span>

-   [<span data-ttu-id="0c1b0-185">**MFCreateSourceResolver**</span><span class="sxs-lookup"><span data-stu-id="0c1b0-185">**MFCreateSourceResolver**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesourceresolver)
-   [<span data-ttu-id="0c1b0-186">**IMFSourceResolver::CreateObjectFromURL**</span><span class="sxs-lookup"><span data-stu-id="0c1b0-186">**IMFSourceResolver::CreateObjectFromURL**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl)

    <span data-ttu-id="0c1b0-187">Per ulteriori informazioni su queste chiamate, vedere [using the source resolver](using-the-source-resolver.md).</span><span class="sxs-lookup"><span data-stu-id="0c1b0-187">For more information about these calls, see [Using the Source Resolver](using-the-source-resolver.md).</span></span>

    <span data-ttu-id="0c1b0-188">Se il file di input è in formato ASF e si desidera convertirlo in un file con frequenza di bit diverso senza modificare i formati, il Risolutore di origine crea un'istanza dell' [origine dei supporti ASF](asf-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="0c1b0-188">If your input file is in ASF format and you want to convert it to a different bit-rate file without changing formats, the source solver creates an instance of the [ASF Media Source](asf-media-source.md).</span></span>

<span data-ttu-id="0c1b0-189">Nell'esempio di codice seguente viene illustrata una funzione CreateMediaSource che consente di creare un'origine multimediale per il file specificato.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-189">The following code example shows a function CreateMediaSource that creates a media source for the specified file.</span></span>


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



## <a name="create-the-asf-file-sink"></a><span data-ttu-id="0c1b0-190">Creare il sink di file ASF</span><span class="sxs-lookup"><span data-stu-id="0c1b0-190">Create the ASF File Sink</span></span>

<span data-ttu-id="0c1b0-191">Consente di creare un'istanza del sink di file ASF che archivia i dati multimediali codificati in un file ASF alla fine della sessione di codifica.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-191">Create an instance of the ASF file sink that will archive encoded media data to an ASF file at the end of the encoding session.</span></span>

<span data-ttu-id="0c1b0-192">In questa esercitazione verrà creato un oggetto attivazione per il sink di file ASF.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-192">In this tutorial, you will create an activation object for the ASF file sink.</span></span> <span data-ttu-id="0c1b0-193">Il sink di file richiede le informazioni seguenti per creare i sink di flusso richiesti.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-193">The file sink needs the following information in order to create the required stream sinks.</span></span>

-   <span data-ttu-id="0c1b0-194">Flussi da codificare e scrivere nel file finale.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-194">The streams to be encoded and written in the final file.</span></span>
-   <span data-ttu-id="0c1b0-195">Proprietà di codifica utilizzate per codificare il contenuto multimediale, ad esempio, il tipo di codifica, il numero di sessioni di codifica e le proprietà correlate.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-195">The encoding properties that are used to encode the media content, such as, type of encoding, number of encoding passes, and the related properties.</span></span>
-   <span data-ttu-id="0c1b0-196">Le proprietà del file globale che indicano al sink multimediale se devono modificare automaticamente i parametri del bucket di perdita (velocità in bit e dimensione del buffer).</span><span class="sxs-lookup"><span data-stu-id="0c1b0-196">The global file properties that indicate to the media sink whether it should adjust the leaky bucket parameters (bit rate and buffer size) automatically.</span></span>

<span data-ttu-id="0c1b0-197">Le informazioni sul flusso vengono configurate nell'oggetto profilo ASF e le proprietà di codifica e globali vengono impostate in un archivio di proprietà gestito dall'oggetto ContentInfo ASF.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-197">The stream information is configured in the ASF Profile object and the encoding and global properties are set in a property store managed by the ASF ContentInfo Object.</span></span>

<span data-ttu-id="0c1b0-198">Per una panoramica del sink di file ASF, vedere [ASF media sinks](asf-media-sinks.md).</span><span class="sxs-lookup"><span data-stu-id="0c1b0-198">For an overview of the ASF file sink, see [ASF Media Sinks](asf-media-sinks.md).</span></span>

### <a name="create-the-asf-profile-object"></a><span data-ttu-id="0c1b0-199">Creazione dell'oggetto profilo ASF</span><span class="sxs-lookup"><span data-stu-id="0c1b0-199">Create the ASF Profile Object</span></span>

<span data-ttu-id="0c1b0-200">Affinché il sink di file ASF scriva i dati multimediali codificati in un file ASF, è necessario che il sink conosca il numero di flussi e il tipo di flussi per i quali creare i sink di flusso.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-200">For the ASF file sink to write encoded media data into an ASF file, the sink needs to know the number of streams and the type of streams for which to create stream sinks.</span></span> <span data-ttu-id="0c1b0-201">In questa esercitazione si estratteranno le informazioni dall'origine multimediale e si creeranno i flussi di output corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-201">In this tutorial you will extract that information from the media source and create corresponding output streams.</span></span> <span data-ttu-id="0c1b0-202">Limitare i flussi di output a un flusso audio e a un flusso video.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-202">Restrict your output streams to one audio stream and one video stream.</span></span> <span data-ttu-id="0c1b0-203">Per ogni flusso selezionato nell'origine, creare un flusso di destinazione e aggiungerlo al profilo.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-203">For each selected stream in the source, create a target stream and add it to the profile.</span></span>

<span data-ttu-id="0c1b0-204">Per implementare questo passaggio, sono necessari gli oggetti seguenti.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-204">To implement this step, you need the following objects.</span></span>

-   [<span data-ttu-id="0c1b0-205">Profilo ASF</span><span class="sxs-lookup"><span data-stu-id="0c1b0-205">ASF Profile</span></span>](asf-profile.md)
-   <span data-ttu-id="0c1b0-206">Descrittore della presentazione per l'origine multimediale</span><span class="sxs-lookup"><span data-stu-id="0c1b0-206">Presentation Descriptor for the media source</span></span>
-   <span data-ttu-id="0c1b0-207">Descrittori di flusso per i flussi selezionati nell'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-207">Stream descriptors for the selected streams in the media source.</span></span>
-   <span data-ttu-id="0c1b0-208">Tipi di supporto per i flussi selezionati.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-208">Media Types for the selected streams.</span></span>

<span data-ttu-id="0c1b0-209">Nei passaggi seguenti viene descritto il processo di creazione del profilo ASF e dei flussi di destinazione.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-209">The following steps describe the process of creating the ASF profile and the target streams.</span></span>

<span data-ttu-id="0c1b0-210">**Per creare il profilo ASF**</span><span class="sxs-lookup"><span data-stu-id="0c1b0-210">**To create the ASF profile**</span></span>

1.  <span data-ttu-id="0c1b0-211">Chiamare [**MFCreateASFProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile) per creare un oggetto profilo vuoto.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-211">Call [**MFCreateASFProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile) to create an empty profile object.</span></span>
2.  <span data-ttu-id="0c1b0-212">Chiamare [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) per creare il descrittore di presentazione per l'origine multimediale creata nel passaggio descritto nella sezione "creare l'origine dei supporti" di questa esercitazione.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-212">Call [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) to create the presentation descriptor for the media source created in the step described in the "Create the Media Source" section of this tutorial.</span></span>
3.  <span data-ttu-id="0c1b0-213">Chiamare [**IMFPresentationDescriptor:: GetStreamDescriptorCount**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorcount) per ottenere il numero di flussi nell'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-213">Call [**IMFPresentationDescriptor::GetStreamDescriptorCount**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorcount) to get the number of streams in the media source.</span></span>
4.  <span data-ttu-id="0c1b0-214">Chiamare [**IMFPresentationDescriptor:: GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) per ogni flusso nell'origine multimediale, ottenere il descrittore del flusso del flusso.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-214">Call [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) for each stream in the media source, get the stream's stream descriptor.</span></span>
5.  <span data-ttu-id="0c1b0-215">Chiamare [**IMFStreamDescriptor:: GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) seguito da [**IMFMediaTypeHandler:: GetMediaTypeByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) e ottenere il primo tipo di supporto per il flusso.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-215">Call [**IMFStreamDescriptor::GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) followed by [**IMFMediaTypeHandler::GetMediaTypeByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) and get the first media type for the stream.</span></span>

    <span data-ttu-id="0c1b0-216">**Nota**   Per evitare chiamate complesse, si supponga che esista un solo tipo di supporto per flusso e selezionare il primo tipo di supporto del flusso.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-216">**Note**   To avoid complex calls, assume that only one media type exists per stream and select the first media type of the stream.</span></span> <span data-ttu-id="0c1b0-217">Per i flussi complessi è necessario enumerare ogni tipo di supporto dal gestore del tipo di supporto e scegliere il tipo di supporto che si desidera codificare.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-217">For complex streams, you need to enumerate each media type from the media type handler and choose the media type that you would like to encode.</span></span>

6.  <span data-ttu-id="0c1b0-218">Chiamare I [**IMFMediaType:: GetMajorType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getmajortype) per ottenere il tipo principale del flusso per determinare se il flusso contiene audio o video.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-218">Call I [**IMFMediaType::GetMajorType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getmajortype) to get the major type of the stream to determine whether the stream is contains audio or video.</span></span>
7.  <span data-ttu-id="0c1b0-219">A seconda del tipo principale del flusso, creare i tipi di supporto di destinazione.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-219">Depending on the major type of the stream, create target media types.</span></span> <span data-ttu-id="0c1b0-220">Questi tipi di supporto manterranno le informazioni sul formato che il codificatore userà durante la sessione di codifica.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-220">These media types will hold format information that the encoder will use during the encoding session.</span></span> <span data-ttu-id="0c1b0-221">Le sezioni seguenti di questa esercitazione descrivono il processo di creazione dei tipi di supporto di destinazione.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-221">The following sections of this tutorial describe the process of creating the target media types.</span></span>
    -   <span data-ttu-id="0c1b0-222">Creare un tipo di supporto audio compresso</span><span class="sxs-lookup"><span data-stu-id="0c1b0-222">Create a Compressed Audio Media Type</span></span>
    -   <span data-ttu-id="0c1b0-223">Creare un tipo di supporto video compresso</span><span class="sxs-lookup"><span data-stu-id="0c1b0-223">Create a Compressed Video Media Type</span></span>
8.  <span data-ttu-id="0c1b0-224">Creare un flusso in base al tipo di supporto di destinazione, configurare il flusso in base ai requisiti dell'applicazione e aggiungere il flusso al profilo.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-224">Create a stream based on the target media type, configure the stream according to the application's requirements, and add the stream to the profile.</span></span> <span data-ttu-id="0c1b0-225">Per ulteriori informazioni, vedere [aggiunta di informazioni sul flusso al sink di file ASF](adding-stream-information-to-the-asf-file-sink.md).</span><span class="sxs-lookup"><span data-stu-id="0c1b0-225">For more information, see [Adding Stream Information to the ASF File Sink](adding-stream-information-to-the-asf-file-sink.md).</span></span>

    1.  <span data-ttu-id="0c1b0-226">Chiamare [**IMFASFProfile:: CreateStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstream) e passare il tipo di supporto di destinazione per creare il flusso di output.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-226">Call [**IMFASFProfile::CreateStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstream) and pass the target media type to create the output stream.</span></span> <span data-ttu-id="0c1b0-227">Il metodo recupera l'interfaccia IMFASFStreamConfig dell'oggetto flusso.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-227">The method retrieves the IMFASFStreamConfig interface of the stream object.</span></span>
    2.  <span data-ttu-id="0c1b0-228">Configurare il flusso.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-228">Configure the stream.</span></span>
        -   <span data-ttu-id="0c1b0-229">Chiamare [**IMFASFStreamConfig:: SetStreamNumber**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-setstreamnumber) per assegnare un numero al flusso.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-229">Call [**IMFASFStreamConfig::SetStreamNumber**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-setstreamnumber) to assign a number to the stream.</span></span> <span data-ttu-id="0c1b0-230">Questa impostazione è obbligatoria.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-230">This setting is mandatory.</span></span>
        -   <span data-ttu-id="0c1b0-231">Facoltativamente, è possibile configurare i parametri del bucket di perdita, l'estensione del payload, l'esclusione reciproca in ogni flusso chiamando metodi [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) e gli attributi di configurazione del flusso rilevanti.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-231">Optionally configure the leaky bucket parameters, payload extension, mutual exclusion on each stream by calling [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) methods and relevant stream configuration attributes.</span></span>
    3.  <span data-ttu-id="0c1b0-232">Aggiungere le proprietà di codifica a livello di flusso usando l'oggetto di ASF.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-232">Add the stream level encoding properties by using the ASF ContentInfo object.</span></span> <span data-ttu-id="0c1b0-233">Per ulteriori informazioni su questo passaggio, vedere la sezione "Create the ASF ContentInfo Object" in questa esercitazione.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-233">For more information about this step, see the "Create the ASF ContentInfo Object" section in this tutorial.</span></span>
    4.  <span data-ttu-id="0c1b0-234">Chiamare [**IMFASFProfile:: sestream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream) per aggiungere il flusso al profilo.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-234">Call [**IMFASFProfile::SetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream) to add the stream to the profile.</span></span>

    <span data-ttu-id="0c1b0-235">L'esempio di codice seguente crea un flusso audio di output.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-235">The following code example creates an output audio stream.</span></span>

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

    

    <span data-ttu-id="0c1b0-236">L'esempio di codice seguente crea un flusso video di output.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-236">The following code example creates an output video stream.</span></span>

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

    

<span data-ttu-id="0c1b0-237">Nell'esempio di codice seguente vengono creati flussi di output a seconda dei flussi nell'origine.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-237">The following code example creates output streams depending on the streams in the source.</span></span>


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



### <a name="create-a-compressed-audio-media-type"></a><span data-ttu-id="0c1b0-238">Creare un tipo di supporto audio compresso</span><span class="sxs-lookup"><span data-stu-id="0c1b0-238">Create a Compressed Audio Media Type</span></span>

<span data-ttu-id="0c1b0-239">Se si vuole includere un flusso audio nel file di output, creare un tipo di audio specificando le caratteristiche del tipo codificato impostando gli attributi obbligatori.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-239">If you want to include an audio stream in the output file, create an audio type by specifying the characteristics of the encoded type by setting the required attributes.</span></span> <span data-ttu-id="0c1b0-240">Per assicurarsi che il tipo di audio sia compatibile con il codificatore audio Windows Media, creare un'istanza del codificatore MFT, impostare le proprietà di codifica e ottenere un tipo di supporto chiamando [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype).</span><span class="sxs-lookup"><span data-stu-id="0c1b0-240">To make sure that the audio type is compatible with the Windows Media audio encoder, instantiate the encoder MFT, set the encoding properties, and get a media type by calling [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype).</span></span> <span data-ttu-id="0c1b0-241">Ottenere il tipo di output richiesto eseguendo il ciclo di tutti i tipi disponibili, ottenendo gli attributi di ogni tipo di supporto e selezionando il tipo più vicino ai propri requisiti.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-241">Get the required output type by looping through all the available types, getting the attributes of each media type, and selecting the type that is closest to your requirements.</span></span> <span data-ttu-id="0c1b0-242">In questa esercitazione, ottenere il primo tipo disponibile dall'elenco dei tipi di supporti di output supportati dal codificatore.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-242">In this tutorial, get the first available type from the list of output media types supported by the encoder.</span></span>

<span data-ttu-id="0c1b0-243">**Nota**  Per Windows 7, Media Foundation fornisce una nuova funzione, [**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) , che recupera un elenco di tipi audio compatibili.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-243">**Note**  For Windows 7, Media Foundation provides a new function, [**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) that retrieves a list of the compatible audio types.</span></span> <span data-ttu-id="0c1b0-244">Questa funzione ottiene solo i tipi di supporto per la codifica CBR.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-244">This function only gets media types for CBR encoding.</span></span>

<span data-ttu-id="0c1b0-245">Un tipo audio completo deve avere il set di attributi seguente:</span><span class="sxs-lookup"><span data-stu-id="0c1b0-245">A complete audio type must have the following attributes set:</span></span>

-   [<span data-ttu-id="0c1b0-246">**\_ \_ tipo principale MF \_ mt**</span><span class="sxs-lookup"><span data-stu-id="0c1b0-246">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md)
-   [<span data-ttu-id="0c1b0-247">**sottotipo MF \_ mt \_**</span><span class="sxs-lookup"><span data-stu-id="0c1b0-247">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)
-   [<span data-ttu-id="0c1b0-248">**numero \_ di \_ \_ canali audio MF mt \_**</span><span class="sxs-lookup"><span data-stu-id="0c1b0-248">**MF\_MT\_AUDIO\_NUM\_CHANNELS**</span></span>](mf-mt-audio-num-channels-attribute.md)
-   [<span data-ttu-id="0c1b0-249">**\_ \_ campioni audio MF \_ mt \_ al \_ secondo**</span><span class="sxs-lookup"><span data-stu-id="0c1b0-249">**MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND**</span></span>](mf-mt-audio-samples-per-second-attribute.md)
-   [<span data-ttu-id="0c1b0-250">**\_ \_ \_ allineamento blocchi audio MF \_ mt**</span><span class="sxs-lookup"><span data-stu-id="0c1b0-250">**MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT**</span></span>](mf-mt-audio-block-alignment-attribute.md)
-   [<span data-ttu-id="0c1b0-251">**\_ \_ Media byte audio MF mt \_ \_ \_ al \_ secondo**</span><span class="sxs-lookup"><span data-stu-id="0c1b0-251">**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md)
-   [<span data-ttu-id="0c1b0-252">**\_ \_ bit audio MF \_ mt \_ per \_ campione**</span><span class="sxs-lookup"><span data-stu-id="0c1b0-252">**MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE**</span></span>](mf-mt-audio-bits-per-sample-attribute.md)

<span data-ttu-id="0c1b0-253">Nell'esempio di codice seguente viene creato un tipo di audio compresso ottenendo un tipo compatibile dal codificatore Windows Media Audio.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-253">The following code example creates a compressed audio type by getting a compatible type from the Windows Media Audio encoder.</span></span> <span data-ttu-id="0c1b0-254">L'implementazione per SetEncodingProperties è illustrata nella sezione "creare l'oggetto di un oggetto ContentInfo ASF" di questa esercitazione.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-254">The implementation for SetEncodingProperties is shown in the "Create the ASF ContentInfo Object" section of this tutorial.</span></span>


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



### <a name="create-a-compressed-video-media-type"></a><span data-ttu-id="0c1b0-255">Creare un tipo di supporto video compresso</span><span class="sxs-lookup"><span data-stu-id="0c1b0-255">Create a Compressed Video Media Type</span></span>

<span data-ttu-id="0c1b0-256">Se si vuole includere un flusso video nel file di output, creare un tipo di video con codifica completa.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-256">If you want to include a video stream in the output file, create a complete-encoded video type.</span></span> <span data-ttu-id="0c1b0-257">Il tipo di supporto completo deve includere la velocità in bit desiderata e i dati privati del codec.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-257">The complete media type must include the desired bit rate and codec private data.</span></span>

<span data-ttu-id="0c1b0-258">Esistono due modi per creare un tipo di supporto video completo.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-258">There are two ways you can create a complete video media type.</span></span>

-   <span data-ttu-id="0c1b0-259">Creare un tipo di supporto vuoto e copiare gli attributi del tipo di supporto dal tipo di video di origine e sovrascrivere l'attributo del [**\_ \_ sottotipo MF mt**](mf-mt-subtype-attribute.md) con la costante GUID MFVideoFormat \_ WMV3.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-259">Create an empty media type and copy the media type attributes from the source video type and overwrite the [**MF\_MT\_SUBTYPE**](mf-mt-subtype-attribute.md) attribute with the GUID constant MFVideoFormat\_WMV3.</span></span>

    <span data-ttu-id="0c1b0-260">Un tipo di video completo deve avere il set di attributi seguente:</span><span class="sxs-lookup"><span data-stu-id="0c1b0-260">A complete video type must have the following attributes set:</span></span>

    -   <span data-ttu-id="0c1b0-261">\_ \_ tipo principale MF \_ mt</span><span class="sxs-lookup"><span data-stu-id="0c1b0-261">MF\_MT\_MAJOR\_TYPE</span></span>
    -   <span data-ttu-id="0c1b0-262">sottotipo MF \_ mt \_</span><span class="sxs-lookup"><span data-stu-id="0c1b0-262">MF\_MT\_SUBTYPE</span></span>
    -   <span data-ttu-id="0c1b0-263">\_ \_ frequenza fotogrammi MF mt \_</span><span class="sxs-lookup"><span data-stu-id="0c1b0-263">MF\_MT\_FRAME\_RATE</span></span>
    -   <span data-ttu-id="0c1b0-264">\_dimensioni del \_ frame MF mt \_</span><span class="sxs-lookup"><span data-stu-id="0c1b0-264">MF\_MT\_FRAME\_SIZE</span></span>
    -   <span data-ttu-id="0c1b0-265">\_modalità di \_ intreccio MF mt \_</span><span class="sxs-lookup"><span data-stu-id="0c1b0-265">MF\_MT\_INTERLACE\_MODE</span></span>
    -   <span data-ttu-id="0c1b0-266">proporzioni MF \_ mt \_ pixel \_ \_</span><span class="sxs-lookup"><span data-stu-id="0c1b0-266">MF\_MT\_PIXEL\_ASPECT\_RATIO</span></span>
    -   <span data-ttu-id="0c1b0-267">\_velocità in \_ bit media MF mt \_</span><span class="sxs-lookup"><span data-stu-id="0c1b0-267">MF\_MT\_AVG\_BITRATE</span></span>
    -   <span data-ttu-id="0c1b0-268">\_ \_ dati utente MF \_ mt</span><span class="sxs-lookup"><span data-stu-id="0c1b0-268">MF\_MT\_USER\_DATA</span></span>

    <span data-ttu-id="0c1b0-269">Nell'esempio di codice seguente viene creato un tipo di video compresso dal tipo di video dell'origine.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-269">The following code example creates a compressed video type from the source's video type.</span></span>

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

    

-   <span data-ttu-id="0c1b0-270">Ottenere un tipo di supporto compatibile dal codificatore video Windows Media impostando le proprietà di codifica e quindi chiamando [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype).</span><span class="sxs-lookup"><span data-stu-id="0c1b0-270">Get a compatible media type from the Windows Media video encoder by setting the encoding properties and then calling [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype).</span></span> <span data-ttu-id="0c1b0-271">Questo metodo restituisce il tipo parziale.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-271">This method returns the partial type.</span></span> <span data-ttu-id="0c1b0-272">Assicurarsi di convertire il tipo parziale in un tipo completo aggiungendo le informazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="0c1b0-272">Make sure you convert the partial type to a complete type by adding the following information:</span></span>

    -   <span data-ttu-id="0c1b0-273">Impostare la velocità in bit video nell'attributo [**MF \_ mt \_ Avg \_ bitrate**](mf-mt-avg-bitrate-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="0c1b0-273">Set the video bit rate in the [**MF\_MT\_AVG\_BITRATE**](mf-mt-avg-bitrate-attribute.md) attribute.</span></span>
    -   <span data-ttu-id="0c1b0-274">Aggiungere i dati privati dei codec impostando l'attributo [**\_ \_ \_ dati utente MF mt**](mf-mt-user-data-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="0c1b0-274">Add codec private data by setting the [**MF\_MT\_USER\_DATA**](mf-mt-user-data-attribute.md) attribute.</span></span> <span data-ttu-id="0c1b0-275">Per istruzioni dettagliate, vedere la sezione relativa ai dati di un codec privato in [configurazione di un codificatore WMV](configuring-a-wmv-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="0c1b0-275">For detailed instructions, see "Private Codec Data" in [Configuring a WMV Encoder](configuring-a-wmv-encoder.md).</span></span>

    <span data-ttu-id="0c1b0-276">Poiché [**IWMCodecPrivateData:: GetPrivateData**](../wmformat/iwmcodecprivatedata-getprivatedata.md) controlla la velocità in bit prima di restituire i dati privati del codec, assicurarsi di impostare la velocità in bit prima di ottenere i dati privati del codec.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-276">Because [**IWMCodecPrivateData::GetPrivateData**](../wmformat/iwmcodecprivatedata-getprivatedata.md) checks the bit rate before returning the codec private data, make sure that you set the bit rate before getting the codec private data.</span></span>

    <span data-ttu-id="0c1b0-277">Nell'esempio di codice seguente viene creato un tipo di video compresso ottenendo un tipo compatibile dal codificatore Windows Media Video.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-277">The following code example creates a compressed video type by getting a compatible type from the Windows Media Video encoder.</span></span> <span data-ttu-id="0c1b0-278">Crea anche un tipo di video non compresso e lo imposta come input del codificatore.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-278">It also creates an uncompressed video type and sets it as the encoder's input.</span></span> <span data-ttu-id="0c1b0-279">Questa operazione viene implementata nella funzione helper CreateUncompressedVideoType.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-279">This is implemented in the helper function CreateUncompressedVideoType.</span></span> <span data-ttu-id="0c1b0-280">GetOutputTypeFromWMVEncoder converte il tipo parziale restituito in un tipo completo mediante l'aggiunta di dati privati di codec.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-280">GetOutputTypeFromWMVEncoder converts the returned partial type into a complete type by adding codec private data.</span></span> <span data-ttu-id="0c1b0-281">L'implementazione per SetEncodingProperties è illustrata nella sezione "creare l'oggetto di un oggetto ContentInfo ASF" di questa esercitazione.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-281">The implementation for SetEncodingProperties is shown in the "Create the ASF ContentInfo Object" section of this tutorial.</span></span>

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

    

    <span data-ttu-id="0c1b0-282">Nell'esempio di codice seguente viene creato un tipo di video non compresso.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-282">The following code example creates an uncompressed video type.</span></span>

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

    

    <span data-ttu-id="0c1b0-283">Nell'esempio di codice seguente i dati privati del codec vengono aggiunti al tipo di supporto video specificato.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-283">The following code example adds codec private data to the specified video media type.</span></span>

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

    

### <a name="create-the-asf-contentinfo-object"></a><span data-ttu-id="0c1b0-284">Creare l'oggetto ContentInfo ASF</span><span class="sxs-lookup"><span data-stu-id="0c1b0-284">Create the ASF ContentInfo Object</span></span>

<span data-ttu-id="0c1b0-285">L'oggetto di questo oggetto è un componente di livello WMContainer progettato principalmente per archiviare le informazioni sull'oggetto intestazione ASF.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-285">The ASF ContentInfo object is a WMContainer level component that is primarily designed to store ASF Header Object information.</span></span> <span data-ttu-id="0c1b0-286">Il sink di file ASF implementa l'oggetto ContentInfo per archiviare le informazioni (in un archivio di proprietà) che verranno usate per scrivere l'oggetto intestazione ASF del file codificato.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-286">The ASF file sink, implements the ContentInfo object in order to store information (in a property store) that will be used to write the ASF Header Object of the encoded file.</span></span> <span data-ttu-id="0c1b0-287">A tale scopo, è necessario creare e configurare il set di Informazioni seguente nell'oggetto ContentInfo prima di avviare la sessione di codifica.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-287">To do so, you must create and configure the following set of information on the ContentInfo object before starting the encoding session.</span></span>

1.  <span data-ttu-id="0c1b0-288">Chiamare [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) per creare un oggetto ContentInfo vuoto.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-288">Call [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) to create an empty ContentInfo object.</span></span>

    <span data-ttu-id="0c1b0-289">Nell'esempio di codice seguente viene creato un oggetto ContentInfo vuoto.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-289">The following code example creates an empty ContentInfo object.</span></span>

    ```C++
        // Create an empty ContentInfo object
        hr = MFCreateASFContentInfo(&pContentInfo);
        if (FAILED(hr))
        {
            goto done;
        }
    
    ```

    

2.  <span data-ttu-id="0c1b0-290">Chiamare [**IMFASFContentInfo:: GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) per ottenere l'archivio delle proprietà a livello di flusso del sink di file.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-290">Call [**IMFASFContentInfo::GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) to get the file sink's stream-level property store.</span></span> <span data-ttu-id="0c1b0-291">In questa chiamata, è necessario passare il numero di flusso assegnato per il flusso durante la creazione del profilo ASF.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-291">In this call, you need to pass the stream number that you assigned for the stream while creating the ASF profile.</span></span>
3.  <span data-ttu-id="0c1b0-292">Impostare le [proprietà di codifica](configuring-the-encoder.md) a livello di flusso nell'archivio delle proprietà di flusso del sink di file.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-292">Set the stream-level [Encoding Properties](configuring-the-encoder.md) in the file sink's stream property store.</span></span> <span data-ttu-id="0c1b0-293">Per ulteriori informazioni, vedere la sezione relativa alle proprietà di codifica del flusso in [impostazione delle proprietà nel sink di file](setting-properties-in-the-file-sink.md).</span><span class="sxs-lookup"><span data-stu-id="0c1b0-293">For more information, see "Stream Encoding Properties" in [Setting Properties in the File Sink](setting-properties-in-the-file-sink.md).</span></span>

    <span data-ttu-id="0c1b0-294">Nell'esempio di codice seguente vengono impostate le proprietà a livello di flusso nell'archivio delle proprietà del sink di file.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-294">The following code example sets the stream level properties in the file sink's property store.</span></span>

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

    

    <span data-ttu-id="0c1b0-295">Nell'esempio di codice riportato di seguito viene illustrata l'implementazione di SetEncodingProperties.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-295">The following code example shows the implementation for SetEncodingProperties.</span></span> <span data-ttu-id="0c1b0-296">Questa funzione imposta le proprietà di codifica a livello di flusso per CBR e VBR.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-296">This function sets stream level encoding properties for CBR and VBR.</span></span>

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

    

4.  <span data-ttu-id="0c1b0-297">Chiamare [**IMFASFContentInfo:: GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) per ottenere l'archivio delle proprietà globali del sink di file.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-297">Call [**IMFASFContentInfo::GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) to get the file sink's global property store.</span></span> <span data-ttu-id="0c1b0-298">In questa chiamata, è necessario passare 0 nel primo parametro.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-298">In this call, you need to pass 0 in the first parameter.</span></span> <span data-ttu-id="0c1b0-299">Per ulteriori informazioni, vedere l'argomento relativo alle proprietà di sink di file globali in [impostazione delle proprietà nel sink di file](setting-properties-in-the-file-sink.md).</span><span class="sxs-lookup"><span data-stu-id="0c1b0-299">For more information, see "Global File Sink Properties" in [Setting Properties in the File Sink](setting-properties-in-the-file-sink.md).</span></span>
5.  <span data-ttu-id="0c1b0-300">Impostare la [**velocità in bit di MFPKEY \_ ASFMEDIASINK \_ AutoAdjust \_**](mfpkey-asfmediasink-autoadjust-bitrate-property.md) su Variant \_ true per assicurarsi che i valori dei bucket persi nel multiplexer ASF siano stati modificati correttamente.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-300">Set the [**MFPKEY\_ASFMEDIASINK\_AUTOADJUST\_BITRATE**](mfpkey-asfmediasink-autoadjust-bitrate-property.md) to VARIANT\_TRUE to ensure the leaky bucket values in the ASF multiplexer are adjusted properly.</span></span> <span data-ttu-id="0c1b0-301">Per informazioni su questa proprietà, vedere l'argomento relativo all'inizializzazione del multiplexer e alle impostazioni dei bucket persi nella [creazione dell'oggetto multiplexer](creating-the-multiplexer-object.md).</span><span class="sxs-lookup"><span data-stu-id="0c1b0-301">For information about this property, see "Multiplexer Initialization and Leaky Bucket Settings" in [Creating the Multiplexer Object](creating-the-multiplexer-object.md).</span></span>

    <span data-ttu-id="0c1b0-302">Nell'esempio di codice seguente vengono impostate le proprietà a livello di flusso nell'archivio delle proprietà del sink di file.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-302">The following code example sets the stream level properties in the file sink's property store.</span></span>

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
    > <span data-ttu-id="0c1b0-303">Sono disponibili altre proprietà che è possibile impostare a livello globale per il sink di file.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-303">There are other properties that you can set at the global level for the file sink.</span></span> <span data-ttu-id="0c1b0-304">Per ulteriori informazioni, vedere "configurazione dell'oggetto ContentInfo con le impostazioni del codificatore" in [impostazione delle proprietà nell'oggetto ContentInfo](setting-properties-in-the-contentinfo-object.md).</span><span class="sxs-lookup"><span data-stu-id="0c1b0-304">For more information, see "Configuring the ContentInfo Object with Encoder Settings" in [Setting Properties in the ContentInfo Object](setting-properties-in-the-contentinfo-object.md).</span></span>

     

<span data-ttu-id="0c1b0-305">Per creare un oggetto attivazione per il sink di file ASF (descritto nella sezione successiva) verrà usato il file di configurazione ASF configurato.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-305">You will use the configured ASF ContentInfo to create an activation object for the ASF file sink (described in the next section).</span></span>

<span data-ttu-id="0c1b0-306">Se si sta creando un sink di file out-of-process ([**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate)), ovvero usando un oggetto Activation, è possibile usare l'oggetto ContentInfo configurato per creare un'istanza del sink multimediale ASF (descritto nella sezione successiva).</span><span class="sxs-lookup"><span data-stu-id="0c1b0-306">If you are creating an out-of-process file sink ([**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate)), that is by using an activation object, you can use the configured ContentInfo object to instantiate the ASF media sink (described in the next section).</span></span> <span data-ttu-id="0c1b0-307">Se si sta creando un sink di file in-process ([**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink)), anziché creare l'oggetto ContentInfo vuoto come descritto nel passaggio 1, ottenere un riferimento all'interfaccia [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) chiamando **IMFMediaSink:: QueryInterface** sul sink di file.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-307">If you are creating an in-process file sink ([**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink)), instead of creating the empty ContentInfo object as described in step 1, get a reference to the [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) interface by calling **IMFMediaSink::QueryInterface** on the file sink.</span></span> <span data-ttu-id="0c1b0-308">È quindi necessario configurare l'oggetto ContentInfo come descritto in questa sezione.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-308">You must then configure the ContentInfo object as described in this section.</span></span>

### <a name="create-the-asf-file-sink"></a><span data-ttu-id="0c1b0-309">Creare il sink di file ASF</span><span class="sxs-lookup"><span data-stu-id="0c1b0-309">Create the ASF File Sink</span></span>

<span data-ttu-id="0c1b0-310">In questo passaggio dell'esercitazione verrà usato il file ASF configurato, creato nel passaggio precedente, per creare un oggetto attivazione per il sink di file ASF chiamando la funzione [**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate) .</span><span class="sxs-lookup"><span data-stu-id="0c1b0-310">In this step of the tutorial, you will use the configured ASF ContentInfo, which you created in the previous step, to create an activation object for the ASF file sink by calling the [**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate) function.</span></span> <span data-ttu-id="0c1b0-311">Per ulteriori informazioni, vedere [creazione del sink di file ASF](creating-the-asf-file-sink.md).</span><span class="sxs-lookup"><span data-stu-id="0c1b0-311">For more information, see [Creating the ASF File Sink](creating-the-asf-file-sink.md).</span></span>

<span data-ttu-id="0c1b0-312">Nell'esempio di codice seguente viene creato l'oggetto attivazione per il sink di file.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-312">The following code example creates the activation object for the file sink.</span></span>


```C++
    //Create the activation object for the  file sink
    hr = MFCreateASFMediaSinkActivate(sURL, pContentInfo, &pActivate);
    if (FAILED(hr))
    {
        goto done;
    }

```



## <a name="build-the-partial-encoding-topology"></a><span data-ttu-id="0c1b0-313">Compilare la topologia di codifica parziale</span><span class="sxs-lookup"><span data-stu-id="0c1b0-313">Build the Partial Encoding Topology</span></span>

<span data-ttu-id="0c1b0-314">Successivamente, verrà compilata una topologia di codifica parziale creando nodi della topologia per l'origine multimediale, i codificatori Windows Media necessari e il sink di file ASF.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-314">Next, you will build a partial encoding topology by creating topology nodes for the media source, the required Windows Media encoders, and the ASF file sink.</span></span> <span data-ttu-id="0c1b0-315">Dopo aver aggiunto i nodi della topologia, è necessario connettere i nodi di origine, trasformazione e sink.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-315">After adding the topology nodes, you will connect the source, transform, and the sink nodes.</span></span> <span data-ttu-id="0c1b0-316">Prima di aggiungere nodi della topologia, è necessario creare un oggetto topologia vuoto chiamando [**MFCreateTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology).</span><span class="sxs-lookup"><span data-stu-id="0c1b0-316">Before adding topology nodes, you must create an empty topology object by calling [**MFCreateTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology).</span></span>

### <a name="create-the-source-topology-node-for-the-media-source"></a><span data-ttu-id="0c1b0-317">Creare il nodo topologia di origine per l'origine multimediale</span><span class="sxs-lookup"><span data-stu-id="0c1b0-317">Create the Source Topology Node for the Media Source</span></span>

<span data-ttu-id="0c1b0-318">In questo passaggio verrà creato il nodo della topologia di origine per l'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-318">In this step, you will create the source topology node for the media source.</span></span>

<span data-ttu-id="0c1b0-319">Per creare questo nodo sono necessari i riferimenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="0c1b0-319">To create this node you need the following references:</span></span>

-   <span data-ttu-id="0c1b0-320">Un puntatore all'origine multimediale creata nel passaggio descritto nella sezione "creare l'origine dei supporti" di questa esercitazione.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-320">A pointer to the media source that you created in the step described in the "Create the Media Source" section of this tutorial.</span></span>
-   <span data-ttu-id="0c1b0-321">Puntatore al descrittore di presentazione per l'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-321">A pointer to the presentation descriptor for the media source.</span></span> <span data-ttu-id="0c1b0-322">È possibile ottenere un riferimento all'interfaccia IMFPresentationDescriptor dell'origine multimediale chiamando [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span><span class="sxs-lookup"><span data-stu-id="0c1b0-322">You can get a reference to IMFPresentationDescriptor interface of the media source by calling [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span></span>
-   <span data-ttu-id="0c1b0-323">Puntatore al descrittore di flusso per ogni flusso nell'origine multimediale per cui è stato creato un flusso di destinazione nel passaggio descritto nella sezione "creare l'oggetto profilo ASF" di questa esercitazione.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-323">A pointer to the stream descriptor for each stream in the media source for which you have created a target stream in the step described in the "Create the ASF Profile Object" section of this tutorial.</span></span>

<span data-ttu-id="0c1b0-324">Per ulteriori informazioni sulla creazione di nodi di origine ed esempi di codice, vedere [creazione di nodi di origine](creating-source-nodes.md).</span><span class="sxs-lookup"><span data-stu-id="0c1b0-324">For more information about creating source nodes and code example, see [Creating Source Nodes](creating-source-nodes.md).</span></span>

<span data-ttu-id="0c1b0-325">Nell'esempio di codice seguente viene creata una topologia parziale aggiungendo il nodo di origine e i nodi di trasformazione necessari.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-325">The following code example creates a partial topology by adding the source node and the required transform nodes.</span></span> <span data-ttu-id="0c1b0-326">Questo codice chiama le funzioni di supporto AddSourceNode e AddTransformOutputNodes.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-326">This code calls the helper functions AddSourceNode, and AddTransformOutputNodes.</span></span> <span data-ttu-id="0c1b0-327">Queste funzioni sono incluse più avanti in questa esercitazione.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-327">These functions are included later in this tutorial.</span></span>


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



<span data-ttu-id="0c1b0-328">Nell'esempio di codice seguente viene creato e aggiunto il nodo della topologia di origine alla topologia di codifica.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-328">The following code example creates and adds the source topology node to the encoding topology.</span></span> <span data-ttu-id="0c1b0-329">Accetta i puntatori a un oggetto topologia precedente, l'origine multimediale per enumerare i flussi di origine, il descrittore di presentazione dell'origine multimediale e il descrittore del flusso dell'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-329">It takes pointers to a previously topology object, the media source to enumerate the source streams, the media source's presentation descriptor, and the media source's stream descriptor.</span></span> <span data-ttu-id="0c1b0-330">Il chiamante riceve un puntatore al nodo della topologia di origine.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-330">The caller receives a pointer to the source topology node.</span></span>


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



### <a name="instantiate-the-required-encoders-and-create-the-transform-nodes"></a><span data-ttu-id="0c1b0-331">Creare un'istanza dei codificatori necessari e creare i nodi di trasformazione</span><span class="sxs-lookup"><span data-stu-id="0c1b0-331">Instantiate the Required Encoders and Create the Transform Nodes</span></span>

<span data-ttu-id="0c1b0-332">La pipeline Media Foundation non inserisce automaticamente i codificatori Windows Media richiesti per i flussi che devono essere codificati.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-332">The Media Foundation pipeline does not automatically insert the required Windows Media encoders for the streams that it must encode.</span></span> <span data-ttu-id="0c1b0-333">L'applicazione deve aggiungere i codificatori manualmente.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-333">The application must add the encoders manually.</span></span> <span data-ttu-id="0c1b0-334">A tale scopo, enumerare i flussi nel profilo ASF creati nel passaggio descritto nella sezione "creare l'oggetto profilo ASF" di questa esercitazione.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-334">To do so, enumerate the streams in the ASF profile that you created in the step described in the "Create the ASF Profile Object" section of this tutorial.</span></span> <span data-ttu-id="0c1b0-335">Per ogni flusso nell'origine e il flusso corrispondente nel profilo, creare un'istanza dei codificatori necessari.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-335">For each stream in the source and the corresponding stream in the profile, instantiate the required encoders.</span></span> <span data-ttu-id="0c1b0-336">Per questo passaggio, è necessario un puntatore all'oggetto attivazione per il sink di file creato nel passaggio descritto nella sezione "creare il sink di file ASF" di questa esercitazione.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-336">For this step, you need a pointer to the activation object for the file sink that you created in the step described in the "Create the ASF File Sink" section of this tutorial.</span></span>

<span data-ttu-id="0c1b0-337">Per una panoramica sulla creazione di codificatori tramite oggetti di attivazione, vedere [uso di oggetti di attivazione di un codificatore](using-an-encoder-s-activation-objects.md).</span><span class="sxs-lookup"><span data-stu-id="0c1b0-337">For an overview on creating encoders through activation objects, see [Using an Encoder's Activation Objects](using-an-encoder-s-activation-objects.md).</span></span>

<span data-ttu-id="0c1b0-338">Nella procedura riportata di seguito vengono descritti i passaggi necessari per creare un'istanza dei codificatori necessari.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-338">The following procedure describes the steps required to instantiate the required encoders.</span></span>

1.  <span data-ttu-id="0c1b0-339">Ottenere un riferimento all'oggetto ContentInfo del sink chiamando [**IMFActivate:: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) sull'attivazione del sink di file e quindi eseguendo una query per [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) dal sink di file chiamando **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-339">Get a reference to the sink's ContentInfo object by calling [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) on the file sink activate and then querying for [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) from the file sink by calling **QueryInterface**.</span></span>
2.  <span data-ttu-id="0c1b0-340">Ottenere il profilo ASF associato all'oggetto ContentInfo chiamando [**IMFASFContentInfo:: GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile).</span><span class="sxs-lookup"><span data-stu-id="0c1b0-340">Get the ASF profile associated with the ContentInfo object by calling [**IMFASFContentInfo::GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile).</span></span>
3.  <span data-ttu-id="0c1b0-341">Enumerare i flussi nel profilo.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-341">Enumerate the streams in the profile.</span></span> <span data-ttu-id="0c1b0-342">A tale proposito, sarà necessario il numero di flussi e un riferimento all'interfaccia [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) di ogni flusso.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-342">For this you will need the stream count and a reference to each stream's [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) interface.</span></span>

    <span data-ttu-id="0c1b0-343">Chiamare i metodi seguenti:</span><span class="sxs-lookup"><span data-stu-id="0c1b0-343">Call the following methods:</span></span>

    -   [<span data-ttu-id="0c1b0-344">**IMFASFProfile::GetStreamCount**</span><span class="sxs-lookup"><span data-stu-id="0c1b0-344">**IMFASFProfile::GetStreamCount**</span></span>](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamcount)
    -   [<span data-ttu-id="0c1b0-345">**IMFASFProfile:: GetStream**</span><span class="sxs-lookup"><span data-stu-id="0c1b0-345">**IMFASFProfile::GetStream**</span></span>](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream)

4.  <span data-ttu-id="0c1b0-346">Per ogni flusso, ottenere il tipo principale e le proprietà di codifica del flusso dall'oggetto ContentInfo.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-346">For each stream get the major type and the stream's encoding properties from the ContentInfo object.</span></span>

    <span data-ttu-id="0c1b0-347">Chiamare i metodi seguenti:</span><span class="sxs-lookup"><span data-stu-id="0c1b0-347">Call the following methods:</span></span>

    -   [<span data-ttu-id="0c1b0-348">**IMFASFStreamConfig::GetMediaType**</span><span class="sxs-lookup"><span data-stu-id="0c1b0-348">**IMFASFStreamConfig::GetMediaType**</span></span>](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getmediatype)
    -   [<span data-ttu-id="0c1b0-349">**IMFMediaType::GetMajorType**</span><span class="sxs-lookup"><span data-stu-id="0c1b0-349">**IMFMediaType::GetMajorType**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getmajortype)
    -   [<span data-ttu-id="0c1b0-350">**IMFASFContentInfo::GetEncodingConfigurationPropertyStore**</span><span class="sxs-lookup"><span data-stu-id="0c1b0-350">**IMFASFContentInfo::GetEncodingConfigurationPropertyStore**</span></span>](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore)

        <span data-ttu-id="0c1b0-351">Per questa chiamata è necessario il numero di flusso recuperato dalla chiamata [**IMFASFProfile:: GetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream) .</span><span class="sxs-lookup"><span data-stu-id="0c1b0-351">For this call you need the stream number retrieved by the [**IMFASFProfile::GetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream) call.</span></span>

5.  <span data-ttu-id="0c1b0-352">A seconda del tipo di flusso, audio o video, creare un'istanza dell'oggetto attivazione per il codificatore chiamando [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) o [**MFCreateWMVEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate).</span><span class="sxs-lookup"><span data-stu-id="0c1b0-352">Depending on the type of the stream, audio or video, instantiate the activation object for the encoder by calling [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) or [**MFCreateWMVEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate).</span></span>

    <span data-ttu-id="0c1b0-353">Per chiamare queste funzioni, sono necessari i riferimenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="0c1b0-353">To call these functions, you need the following references:</span></span>

    -   <span data-ttu-id="0c1b0-354">Puntatore al tipo di supporto del flusso recuperato da [**IMFASFStreamConfig:: GetMediaType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getmediatype) nel passaggio precedente.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-354">A pointer to the stream's media type retrieved by [**IMFASFStreamConfig::GetMediaType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getmediatype) in the previous step.</span></span>
    -   <span data-ttu-id="0c1b0-355">Puntatore all'archivio delle proprietà di codifica del flusso recuperato da [**IMFASFContentInfo:: GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore).</span><span class="sxs-lookup"><span data-stu-id="0c1b0-355">A pointer to the stream's encoding property store retrieved by [**IMFASFContentInfo::GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore).</span></span> <span data-ttu-id="0c1b0-356">Passando un puntatore all'archivio delle proprietà, le proprietà del flusso impostate nel sink di file vengono copiate nel file con estensione MFT del codificatore.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-356">By passing a pointer to the property store, the stream properties set in the file sink are copied on the encoder MFT.</span></span>

6.  <span data-ttu-id="0c1b0-357">Aggiornare il parametro bucket Leaky per il flusso audio.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-357">Update the leaky bucket parameter for the audio stream.</span></span>

    <span data-ttu-id="0c1b0-358">[**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) imposta il tipo di output sul codificatore MFT sottostante per il codec audio Windows Media.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-358">[**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) sets the output type on the underlying encoder MFT for the Windows Media audio codec.</span></span> <span data-ttu-id="0c1b0-359">Dopo aver impostato il tipo di supporto di output, il codificatore ottiene la velocità in bit media dal tipo di supporto di output, calcola la velocità in bit della finestra del buffer e imposta i valori bucket che verranno usati durante la sessione di codifica.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-359">After the output media type is set, the encoder gets the average bit rate from the output media type, calculates the buffer window rage bit rate, and sets the leaky bucket values that will be used during the encoding session.</span></span> <span data-ttu-id="0c1b0-360">È possibile aggiornare questi valori nel sink di file eseguendo una query sul codificatore o impostando i valori personalizzati.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-360">You can update these values in the file sink by either querying the encoder or setting custom values.</span></span> <span data-ttu-id="0c1b0-361">Per aggiornare i valori, è necessario il set di Informazioni seguente:</span><span class="sxs-lookup"><span data-stu-id="0c1b0-361">To update values you need the following set of information:</span></span>

    -   <span data-ttu-id="0c1b0-362">Velocità in bit media: ottenere la velocità in bit media dall'attributo [**MF \_ mt \_ audio \_ Avg \_ bytes \_ al \_ secondo**](mf-mt-audio-avg-bytes-per-second-attribute.md) impostato sul tipo di supporto di output selezionato durante la negoziazione del tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-362">Average bit rate: Get the average bit rate from the [**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**](mf-mt-audio-avg-bytes-per-second-attribute.md) attribute set on the output media type that is selected during media type negotiation.</span></span>
    -   <span data-ttu-id="0c1b0-363">Finestra buffer: è possibile recuperarla chiamando [**IWMCodecLeakyBucket:: GetBufferSizeBits**](../wmformat/iwmcodecleakybucket-getbuffersizebits.md).</span><span class="sxs-lookup"><span data-stu-id="0c1b0-363">Buffer window: you can retrieve it by calling [**IWMCodecLeakyBucket::GetBufferSizeBits**](../wmformat/iwmcodecleakybucket-getbuffersizebits.md).</span></span>
    -   <span data-ttu-id="0c1b0-364">Dimensioni iniziali del buffer: impostare su 0.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-364">Initial buffer size: Set to 0.</span></span>

    <span data-ttu-id="0c1b0-365">Creare una matrice di valori DWORD e impostare il valore nella proprietà [**MFPKEY \_ ASFSTREAMSINK \_ corrected \_ LEAKYBUCKET**](mfpkey-asfstreamsink-corrected-leakybucket-property.md) del sink del flusso audio.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-365">Create an array of DWORDs and set the value in the [**MFPKEY\_ASFSTREAMSINK\_CORRECTED\_LEAKYBUCKET**](mfpkey-asfstreamsink-corrected-leakybucket-property.md) property of the audio stream sink.</span></span> <span data-ttu-id="0c1b0-366">Se non si specificano i valori aggiornati, la sessione multimediale li imposta in modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-366">If you do not provide the updated values, the Media Session sets them appropriately.</span></span>

    <span data-ttu-id="0c1b0-367">Per ulteriori informazioni, vedere [il modello di buffer di bucket a perdita](the-leaky-bucket-buffer-model.md).</span><span class="sxs-lookup"><span data-stu-id="0c1b0-367">For more information, see [The Leaky Bucket Buffer Model](the-leaky-bucket-buffer-model.md).</span></span>

<span data-ttu-id="0c1b0-368">Gli oggetti attivazione creati nel passaggio 5 devono essere aggiunti alla topologia come nodi della topologia di trasformazione.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-368">The activation objects created in step 5 must be added to the topology as transform topology nodes.</span></span> <span data-ttu-id="0c1b0-369">Per ulteriori informazioni ed esempi di codice, vedere "creazione di un nodo Transform da un oggetto Activation" in [creazione di nodi di trasformazione](creating-transform-nodes.md).</span><span class="sxs-lookup"><span data-stu-id="0c1b0-369">For more information and code example, see "Creating a Transform Node from an Activation Object" in [Creating Transform Nodes](creating-transform-nodes.md).</span></span>

<span data-ttu-id="0c1b0-370">Nell'esempio di codice seguente viene creato e aggiunto il codificatore richiesto attivato.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-370">The following code example creates and adds the required encoder activates.</span></span> <span data-ttu-id="0c1b0-371">Accetta i puntatori a un oggetto topologia creato in precedenza, l'oggetto attivazione del sink di file e il tipo di supporto del flusso di origine.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-371">It takes pointers to a previously created topology object, the file sink's activation object and the source stream's media type.</span></span> <span data-ttu-id="0c1b0-372">Chiama anche AddOutputNode (vedere l'esempio di codice successivo) che crea e aggiunge il nodo sink alla topologia di codifica.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-372">It also calls AddOutputNode (see next code example) that creates and adds the sink node to the encoding topology.</span></span> <span data-ttu-id="0c1b0-373">Il chiamante riceve un puntatore al nodo della topologia di origine.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-373">It The caller receives a pointer to the source topology node.</span></span>


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



### <a name="create-the-output-topology-nodes-for-the-file-sink"></a><span data-ttu-id="0c1b0-374">Creare i nodi della topologia di output per il sink di file</span><span class="sxs-lookup"><span data-stu-id="0c1b0-374">Create the Output Topology Nodes for the File Sink</span></span>

<span data-ttu-id="0c1b0-375">In questo passaggio verrà creato il nodo della topologia di output per il sink di file ASF.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-375">In this step, you will create the output topology node for the ASF file sink.</span></span>

<span data-ttu-id="0c1b0-376">Per creare questo nodo sono necessari i riferimenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="0c1b0-376">To create this node you need the following references:</span></span>

-   <span data-ttu-id="0c1b0-377">Un puntatore all'oggetto attivazione creato nel passaggio descritto nella sezione "creare il sink di file ASF" di questa esercitazione.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-377">A pointer to the activation object that you created in the step described in the "Create the ASF File Sink" section of this tutorial.</span></span>
-   <span data-ttu-id="0c1b0-378">I numeri di flusso per identificare i sink del flusso aggiunti al sink di file.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-378">The stream numbers to identify the stream sinks added to the file sink.</span></span> <span data-ttu-id="0c1b0-379">I numeri dei flussi corrispondono all'identificazione del flusso impostata durante la creazione del flusso.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-379">The stream numbers match the stream's identification that was set during stream creation.</span></span>

<span data-ttu-id="0c1b0-380">Per ulteriori informazioni sulla creazione di nodi di output ed esempi di codice, vedere la sezione relativa alla creazione di un nodo di output da un oggetto Activation in [creazione di nodi di output](creating-output-nodes.md).</span><span class="sxs-lookup"><span data-stu-id="0c1b0-380">For more information about creating output nodes and code example, see "Creating an Output Node from an Activation Object" in [Creating Output Nodes](creating-output-nodes.md).</span></span>

<span data-ttu-id="0c1b0-381">Se non si utilizza l'oggetto attivazione per il sink di file, è necessario enumerare i sink di flusso nel sink di file ASF e impostare ogni sink di flusso come nodo di output nella topologia.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-381">If you are not using activation object for the file sink, you must enumerate the stream sinks in the ASF file sink and set each stream sink as the output node in the topology.</span></span> <span data-ttu-id="0c1b0-382">Per informazioni sull'enumerazione del sink di flusso, vedere "enumerazione dei sink di flusso" in [aggiunta di informazioni sul flusso al sink di file ASF](adding-stream-information-to-the-asf-file-sink.md).</span><span class="sxs-lookup"><span data-stu-id="0c1b0-382">For information about stream sink enumeration, see "Enumerating Stream Sinks" in [Adding Stream Information to the ASF File Sink](adding-stream-information-to-the-asf-file-sink.md).</span></span>

<span data-ttu-id="0c1b0-383">Nell'esempio di codice seguente viene creato e aggiunto il nodo sink alla topologia di codifica.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-383">The following code example creates and adds the sink node to the encoding topology.</span></span> <span data-ttu-id="0c1b0-384">Accetta i puntatori a un oggetto topologia creato in precedenza, l'oggetto attivazione del sink di file e il numero di identificazione del flusso.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-384">It takes pointers to a previously created topology object, the file sink's activation object and the stream's identification number.</span></span> <span data-ttu-id="0c1b0-385">Il chiamante riceve un puntatore al nodo della topologia di origine.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-385">It The caller receives a pointer to the source topology node.</span></span>


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



<span data-ttu-id="0c1b0-386">Nell'esempio di codice seguente vengono enumerati i sink di flusso per un determinato sink multimediale.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-386">The following code example enumerates the stream sinks for a given media sink.</span></span>


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



### <a name="connect-the-source-transform-and-sink-nodes"></a><span data-ttu-id="0c1b0-387">Connettere i nodi di origine, trasformazione e sink</span><span class="sxs-lookup"><span data-stu-id="0c1b0-387">Connect the Source, Transform, and Sink Nodes</span></span>

<span data-ttu-id="0c1b0-388">In questo passaggio si collegherà il nodo di origine al nodo Transform che fa riferimento alla codifica attivata che è stata creata nel passaggio descritto nella sezione "creare un'istanza dei codificatori necessari e creare i nodi di trasformazione" di questa esercitazione.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-388">In this step, you will connect the source node to the transform node referencing the encoding activates that you created in the step described in the "Instantiate the Required Encoders and Create the Transform Nodes" section of this tutorial.</span></span> <span data-ttu-id="0c1b0-389">Il nodo Transform verrà connesso al nodo di output contenente l'oggetto Activation per il sink di file.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-389">The transform node will be connected to the output node containing the activation object for the file sink.</span></span>

## <a name="handling-the-encoding-session"></a><span data-ttu-id="0c1b0-390">Gestione della sessione di codifica</span><span class="sxs-lookup"><span data-stu-id="0c1b0-390">Handling the Encoding Session</span></span>

<span data-ttu-id="0c1b0-391">Nel passaggio si eseguiranno i passaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="0c1b0-391">In the step, you will perform the following steps:</span></span>

1.  <span data-ttu-id="0c1b0-392">Chiamare [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) per creare una sessione di codifica.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-392">Call [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) to create an encoding session.</span></span>
2.  <span data-ttu-id="0c1b0-393">Chiamare [**IMFMediaSession:: Setopologia**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) per impostare la topologia di codifica nella sessione.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-393">Call [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) to set the encoding topology on the session.</span></span> <span data-ttu-id="0c1b0-394">Se la chiamata viene completata, la sessione multimediale valuta i nodi della topologia e inserisce oggetti Transform aggiuntivi, ad esempio un decodificatore, che converte l'origine compressa specificata in campioni non compressi da inserire come input nel codificatore.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-394">If the call completes, the Media Session evaluates the topology nodes and inserts additional transform objects such as a decoder that converts the specified compressed source to uncompressed samples to feed as input to the encoder.</span></span>
3.  <span data-ttu-id="0c1b0-395">Chiamare [**IMFMediaSession:: GetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-getevent) per richiedere gli eventi generati dalla sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-395">Call [**IMFMediaSession::GetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-getevent) to request for the events raised by the Media Session.</span></span>

    <span data-ttu-id="0c1b0-396">Nel ciclo di eventi si avvierà e si chiude la sessione di codifica a seconda degli eventi generati dalla sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-396">In the event loop you will start and close the encoding session depending on the events raised by the Media Session.</span></span> <span data-ttu-id="0c1b0-397">La chiamata a [**IMFMediaSession:: Setopologie**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) genera una sessione multimediale che genera l'evento [MESessionTopologyStatus](mesessiontopologystatus.md) con il \_ flag di disponibilità MF TOPOSTATUS \_ impostato.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-397">The [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) call results in Media Session raising the [MESessionTopologyStatus](mesessiontopologystatus.md) event with the MF\_TOPOSTATUS\_READY flag set.</span></span> <span data-ttu-id="0c1b0-398">Tutti gli eventi vengono generati in modo asincrono e un'applicazione può recuperare questi eventi in modo sincrono o asincrono.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-398">All events are generated asynchronously and an application can retrieve these events synchronously or asynchronously.</span></span> <span data-ttu-id="0c1b0-399">Poiché l'applicazione in questa esercitazione è un'applicazione console e il blocco dei thread dell'interfaccia utente non costituisce un problema, gli eventi vengono generati in modo sincrono dalla sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-399">Because the application in this tutorial is a console application and blocking user interface threads is not a concern, we will get the events from Media Session synchronously.</span></span>

    <span data-ttu-id="0c1b0-400">Per ottenere gli eventi in modo asincrono, l'applicazione deve implementare l'interfaccia [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) .</span><span class="sxs-lookup"><span data-stu-id="0c1b0-400">To get the events asynchronously, your application must implement the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface.</span></span> <span data-ttu-id="0c1b0-401">Per ulteriori informazioni e per un esempio di implementazione di questa interfaccia, vedere "gestione degli eventi di sessione" in [come riprodurre file multimediali con Media Foundation](how-to-play-unprotected-media-files.md).</span><span class="sxs-lookup"><span data-stu-id="0c1b0-401">For more information and an example implementation of this interface, see "Handling Session Events" in [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md).</span></span>

<span data-ttu-id="0c1b0-402">Nel ciclo di eventi per ottenere gli eventi della sessione multimediale, attendere l'evento [MESessionTopologyStatus](mesessiontopologystatus.md) generato quando [**IMFMediaSession:: la topologia**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) viene completata e la topologia viene risolta.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-402">In the event loop for getting Media Session events, wait for the [MESessionTopologyStatus](mesessiontopologystatus.md) event that is raised when the [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) completes and the topology is resolved.</span></span> <span data-ttu-id="0c1b0-403">Quando si recupera l'evento MESessionTopologyStatus, avviare la sessione di codifica chiamando [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).</span><span class="sxs-lookup"><span data-stu-id="0c1b0-403">Upon getting the MESessionTopologyStatus event, start the encoding session by calling [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).</span></span> <span data-ttu-id="0c1b0-404">La sessione multimediale genera l'evento [MEEndOfPresentation](meendofpresentation.md) quando tutte le operazioni di codifica sono completate.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-404">The Media Session generates the [MEEndOfPresentation](meendofpresentation.md) event when all of the encoding operations are complete.</span></span> <span data-ttu-id="0c1b0-405">Questo evento deve essere gestito per la codifica VBR e viene illustrato nella sezione successiva "aggiornare le proprietà di codifica nel sink di file per la codifica VBR" di questa esercitazione.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-405">This event must be handled for VBR encoding and is discussed in the next section "Update Encoding Properties on the File Sink for VBR Encoding" of this tutorial.</span></span>

<span data-ttu-id="0c1b0-406">La sessione multimediale genera l'oggetto intestazione ASF e finalizza il file al termine della sessione di codifica e quindi genera l'evento [MESessionClosed](mesessionclosed.md) .</span><span class="sxs-lookup"><span data-stu-id="0c1b0-406">The Media Session generates the ASF Header Object and finalizes the file when the encoding session completes and then raises the [MESessionClosed](mesessionclosed.md) event.</span></span> <span data-ttu-id="0c1b0-407">Questo evento deve essere gestito eseguendo operazioni di arresto appropriate nella sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-407">This event must be handled by performing proper shutdown operations on the Media Session.</span></span> <span data-ttu-id="0c1b0-408">Per avviare le operazioni di arresto, chiamare [**IMFMediaSession:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown).</span><span class="sxs-lookup"><span data-stu-id="0c1b0-408">To begin the shutdown operations, call [**IMFMediaSession::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown).</span></span> <span data-ttu-id="0c1b0-409">Dopo la chiusura della sessione di codifica, non è possibile impostare un'altra topologia per la codifica nella stessa istanza di sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-409">After the encoding session is closed, you cannot set another topology for encoding on the same Media Session instance.</span></span> <span data-ttu-id="0c1b0-410">Per codificare un altro file, è necessario chiudere e rilasciare la sessione multimediale corrente e impostare la nuova topologia in una sessione multimediale appena creata.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-410">To encode another file, the current Media Session must be closed and released and the new topology must be set on a newly created Media Session.</span></span> <span data-ttu-id="0c1b0-411">Nell'esempio di codice seguente viene creata la sessione multimediale, viene impostata la topologia di codifica e vengono gestiti gli eventi della sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-411">The following code example creates the Media Session, sets the encoding topology and handles the Media Session events.</span></span>

<span data-ttu-id="0c1b0-412">L'esempio di codice seguente crea la sessione multimediale, imposta la topologia di codifica e controlla la sessione di codifica gestendo gli eventi dalla sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-412">The following code example creates the Media Session, sets the encoding topology, and controls the encoding session by handling events from the Media Session.</span></span>


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



## <a name="update-encoding-properties-in-the-file-sink"></a><span data-ttu-id="0c1b0-413">Aggiornare le proprietà di codifica nel sink di file</span><span class="sxs-lookup"><span data-stu-id="0c1b0-413">Update Encoding Properties in the File Sink</span></span>

<span data-ttu-id="0c1b0-414">Alcune proprietà di codifica, ad esempio la velocità in bit di codifica e i valori accurati dei bucket a perdita, non sono note finché la codifica non è completa, soprattutto per la codifica VBR.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-414">Certain encoding properties such as the encoding bit rate and the accurate leaky bucket values are not known until the encoding is complete, especially for VBR encoding.</span></span> <span data-ttu-id="0c1b0-415">Per ottenere i valori corretti, l'applicazione deve attendere l'evento [MEEndOfPresentation](meendofpresentation.md) che indica che la sessione di codifica è stata completata.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-415">To get the correct values the application must wait for the [MEEndOfPresentation](meendofpresentation.md) event that indicates that the encoding session is complete.</span></span> <span data-ttu-id="0c1b0-416">È necessario aggiornare i valori dei bucket persi nel sink, in modo che l'oggetto intestazione ASF possa riflettere i valori accurati.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-416">The leaky bucket values must be updated in the sink so that the ASF Header Object can reflect the accurate values.</span></span>

<span data-ttu-id="0c1b0-417">Nella procedura riportata di seguito vengono descritti i passaggi necessari per attraversare i nodi nella topologia di codifica per ottenere il nodo sink di file e impostare le proprietà del bucket di perdita richieste.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-417">The following procedure describes the steps required to traverse the nodes in the encoding topology to get the file sink node and set the required leaky bucket properties.</span></span>

<span data-ttu-id="0c1b0-418">**Per aggiornare i valori delle proprietà post-codifica nel sink di file ASF**</span><span class="sxs-lookup"><span data-stu-id="0c1b0-418">**To update the post encoding property values on the ASF file sink**</span></span>

1.  <span data-ttu-id="0c1b0-419">Chiamare [**IMFTopology:: GetOutputNodeCollection**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-getoutputnodecollection) per ottenere la raccolta di nodi di output dalla topologia di codifica.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-419">Call [**IMFTopology::GetOutputNodeCollection**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-getoutputnodecollection) to get the output node collection from the encoding topology.</span></span>
2.  <span data-ttu-id="0c1b0-420">Per ogni nodo, ottenere un puntatore al sink del flusso nel nodo chiamando [**IMFTopologyNode:: GetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getobject).</span><span class="sxs-lookup"><span data-stu-id="0c1b0-420">For each node, get a pointer to the stream sink in the node by calling [**IMFTopologyNode::GetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getobject).</span></span> <span data-ttu-id="0c1b0-421">Query per l'interfaccia [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) sul puntatore [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) restituito da **IMFTopologyNode:: GetObject**.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-421">Query for the [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) interface on the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) pointer returned by **IMFTopologyNode::GetObject**.</span></span>
3.  <span data-ttu-id="0c1b0-422">Per ogni sink di flusso, ottenere il nodo downstream (codificatore) chiamando [**IMFTopologyNode:: GetInput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getinput).</span><span class="sxs-lookup"><span data-stu-id="0c1b0-422">For each stream sink get the downstream node (encoder) by calling [**IMFTopologyNode::GetInput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getinput).</span></span>
4.  <span data-ttu-id="0c1b0-423">Eseguire una query sul nodo per ottenere il puntatore [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) dal nodo del codificatore.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-423">Query the node to get the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) pointer from the encoder node.</span></span>
5.  <span data-ttu-id="0c1b0-424">Eseguire una query sul codificatore per il puntatore [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) per ottenere l'archivio delle proprietà di codifica dal codificatore.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-424">Query the encoder for the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) pointer to get the encoding property store from the encoder.</span></span>
6.  <span data-ttu-id="0c1b0-425">Eseguire una query sul sink di flusso per il puntatore [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) per ottenere l'archivio delle proprietà del sink di flusso.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-425">Query the stream sink for the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) pointer to get the stream sink's property store.</span></span>
7.  <span data-ttu-id="0c1b0-426">Chiamare [**IPropertyStore:: GetValue**](/windows/win32/api/propsys/nn-propsys-ipropertystore) per ottenere i valori di proprietà richiesti dall'archivio delle proprietà del codificatore e copiarli nell'archivio delle proprietà del sink di flusso chiamando **IPropertyStore:: SetValue**.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-426">Call [**IPropertyStore::GetValue**](/windows/win32/api/propsys/nn-propsys-ipropertystore) to get the required property values from the encoder's property store and copy them to the stream sink's property store by calling **IPropertyStore::SetValue**.</span></span>

<span data-ttu-id="0c1b0-427">La tabella seguente mostra i valori delle proprietà post-codifica che devono essere impostati nel sink di flusso per il flusso video.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-427">The following table shows the post encoding property values that must be set on the stream sink for the video stream.</span></span>



| <span data-ttu-id="0c1b0-428">Tipo di codifica</span><span class="sxs-lookup"><span data-stu-id="0c1b0-428">Encoding type</span></span>                                                                                  | <span data-ttu-id="0c1b0-429">Nome proprietà (GetValue)</span><span class="sxs-lookup"><span data-stu-id="0c1b0-429">Property name (GetValue)</span></span>                                                                        | <span data-ttu-id="0c1b0-430">Nome proprietà (SetValue)</span><span class="sxs-lookup"><span data-stu-id="0c1b0-430">Property name (SetValue)</span></span>                                                                                                |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0c1b0-431">Codifica della velocità in bit costante</span><span class="sxs-lookup"><span data-stu-id="0c1b0-431">Constant Bit Rate Encoding</span></span>](constant-bit-rate-encoding.md)                                   | <span data-ttu-id="0c1b0-432">\_BAVG MFPKEY</span><span class="sxs-lookup"><span data-stu-id="0c1b0-432">MFPKEY\_BAVG</span></span><br/> <span data-ttu-id="0c1b0-433">\_RAVG MFPKEY</span><span class="sxs-lookup"><span data-stu-id="0c1b0-433">MFPKEY\_RAVG</span></span><br/>                                                 | <span data-ttu-id="0c1b0-434">MFPKEY \_ Stat \_ BAVG</span><span class="sxs-lookup"><span data-stu-id="0c1b0-434">MFPKEY\_STAT\_BAVG</span></span><br/> <span data-ttu-id="0c1b0-435">MFPKEY \_ Stat \_ RAVG</span><span class="sxs-lookup"><span data-stu-id="0c1b0-435">MFPKEY\_STAT\_RAVG</span></span><br/>                                                             |
| [<span data-ttu-id="0c1b0-436">Codifica della velocità in bit della variabile basata sulla qualità</span><span class="sxs-lookup"><span data-stu-id="0c1b0-436">Quality-Based Variable Bit Rate Encoding</span></span>](quality-based-variable-bit-rate--vbr--encoding.md) | <span data-ttu-id="0c1b0-437">\_BAVG MFPKEY</span><span class="sxs-lookup"><span data-stu-id="0c1b0-437">MFPKEY\_BAVG</span></span><br/> <span data-ttu-id="0c1b0-438">\_RAVG MFPKEY</span><span class="sxs-lookup"><span data-stu-id="0c1b0-438">MFPKEY\_RAVG</span></span><br/> <span data-ttu-id="0c1b0-439">\_BMAX MFPKEY</span><span class="sxs-lookup"><span data-stu-id="0c1b0-439">MFPKEY\_BMAX</span></span><br/> <span data-ttu-id="0c1b0-440">\_Rmax MFPKEY</span><span class="sxs-lookup"><span data-stu-id="0c1b0-440">MFPKEY\_RMAX</span></span><br/> | <span data-ttu-id="0c1b0-441">MFPKEY \_ Stat \_ BAVG</span><span class="sxs-lookup"><span data-stu-id="0c1b0-441">MFPKEY\_STAT\_BAVG</span></span><br/> <span data-ttu-id="0c1b0-442">MFPKEY \_ Stat \_ RAVG</span><span class="sxs-lookup"><span data-stu-id="0c1b0-442">MFPKEY\_STAT\_RAVG</span></span><br/> <span data-ttu-id="0c1b0-443">MFPKEY \_ Stat \_ BMAX</span><span class="sxs-lookup"><span data-stu-id="0c1b0-443">MFPKEY\_STAT\_BMAX</span></span><br/> <span data-ttu-id="0c1b0-444">MFPKEY \_ Stat \_ Rmax</span><span class="sxs-lookup"><span data-stu-id="0c1b0-444">MFPKEY\_STAT\_RMAX</span></span><br/> |



 

<span data-ttu-id="0c1b0-445">Nell'esempio di codice seguente vengono impostati i valori delle proprietà post-codifica.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-445">The following code example sets the post-encoding property values.</span></span>


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



## <a name="implement-main"></a><span data-ttu-id="0c1b0-446">Implementare Main</span><span class="sxs-lookup"><span data-stu-id="0c1b0-446">Implement Main</span></span>

<span data-ttu-id="0c1b0-447">Nell'esempio di codice seguente viene illustrata la funzione principale dell'applicazione console.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-447">The following code example shows the main function of your console application.</span></span>


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



## <a name="test-the-output-file"></a><span data-ttu-id="0c1b0-448">Testare il file di output</span><span class="sxs-lookup"><span data-stu-id="0c1b0-448">Test the Output File</span></span>

<span data-ttu-id="0c1b0-449">Nell'elenco seguente viene descritto un elenco di controllo per il test del file codificato.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-449">The following list describes a check list for testing the encoded file.</span></span> <span data-ttu-id="0c1b0-450">Questi valori possono essere controllati nella finestra di dialogo Proprietà file che è possibile visualizzare facendo clic con il pulsante destro del mouse sul file codificato e scegliendo **Proprietà** dal menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-450">These values can be checked in the file properties dialog box that you can display by right-clicking the encoded file and selecting **Properties** from the context menu.</span></span>

-   <span data-ttu-id="0c1b0-451">Il percorso del file codificato è accurato.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-451">The path of the encoded file is accurate.</span></span>
-   <span data-ttu-id="0c1b0-452">Le dimensioni del file sono maggiori di zero KB e la durata della riproduzione corrisponde alla durata del file di origine.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-452">The size of the file is more than zero KB and the play duration matches the source file's duration.</span></span>
-   <span data-ttu-id="0c1b0-453">Per il flusso video, controllare la larghezza del frame e l'altezza, frequenza dei fotogrammi.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-453">For the video stream, check the frame width and height, frame rate.</span></span> <span data-ttu-id="0c1b0-454">Questi valori devono corrispondere ai valori specificati nel profilo ASF creato nel passaggio descritto nella sezione "creare l'oggetto profilo ASF".</span><span class="sxs-lookup"><span data-stu-id="0c1b0-454">These values should match the values that you specified in the ASF profile that you created in the step described in the section "Create the ASF Profile Object".</span></span>
-   <span data-ttu-id="0c1b0-455">Per il flusso audio, la velocità in bit deve essere vicina al valore specificato nel tipo di supporto di destinazione.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-455">For the audio stream, the bit rate must be close to the value you specified on the target media type.</span></span>
-   <span data-ttu-id="0c1b0-456">Aprire il file in Windows Media Player e verificare la qualità della codifica.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-456">Open the file in Windows Media Player and check the quality of the encoding.</span></span>
-   <span data-ttu-id="0c1b0-457">Aprire il file ASF in ASFViewer per visualizzare la struttura di un file ASF.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-457">Open the ASF file in ASFViewer to see the structure of an ASF file.</span></span> <span data-ttu-id="0c1b0-458">Questo strumento può essere scaricato da questo [sito Web Microsoft](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea).</span><span class="sxs-lookup"><span data-stu-id="0c1b0-458">This tool can be downloaded from this [Microsoft website](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea).</span></span>

## <a name="common-error-codes-and-debugging-tips"></a><span data-ttu-id="0c1b0-459">Codici di errore comuni e suggerimenti per il debug</span><span class="sxs-lookup"><span data-stu-id="0c1b0-459">Common Error Codes and Debugging Tips</span></span>

<span data-ttu-id="0c1b0-460">Nell'elenco seguente vengono descritti i codici di errore comuni che potrebbero essere ricevuti e i suggerimenti per il debug.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-460">The following list describes the common error codes that your might receive and the debugging tips.</span></span>

-   <span data-ttu-id="0c1b0-461">La chiamata a [**IMFSourceResolver:: CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) blocca l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-461">The call to [**IMFSourceResolver::CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) stalls the application.</span></span>

    <span data-ttu-id="0c1b0-462">Assicurarsi di aver inizializzato la piattaforma di Media Foundation chiamando [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup).</span><span class="sxs-lookup"><span data-stu-id="0c1b0-462">Make sure that you have initialized the Media Foundation platform by calling [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup).</span></span> <span data-ttu-id="0c1b0-463">Questa funzione imposta la piattaforma asincrona usata da tutti i metodi che avviano operazioni asincrone, ad esempio [**IMFSourceResolver:: CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl), internamente.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-463">This function sets up the asynchronous platform that is used by all methods that start asynchronous operations, such as [**IMFSourceResolver::CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl), internally.</span></span>

-   <span data-ttu-id="0c1b0-464">[**IMFSourceResolver:: CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) restituisce HRESULT 0x80070002 "Impossibile trovare il file specificato.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-464">[**IMFSourceResolver::CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) returns HRESULT 0x80070002 "The system cannot find the file specified.</span></span>

    <span data-ttu-id="0c1b0-465">Verificare che il nome del file di input specificato dall'utente nel primo argomento esista.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-465">Make sure that the input file name specified by the user in the first argument exists.</span></span>

-   <span data-ttu-id="0c1b0-466">HRESULT 0x80070020 "il processo non può accedere al file perché è in uso da un altro processo.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-466">HRESULT 0x80070020 "The process cannot access the file because it is being used by another process.</span></span> <span data-ttu-id="0c1b0-467">"</span><span class="sxs-lookup"><span data-stu-id="0c1b0-467">"</span></span>

    <span data-ttu-id="0c1b0-468">Assicurarsi che i file di input e di output non siano attualmente in uso da un'altra risorsa nel sistema.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-468">Make sure that the input and the output files are not currently in use by another resource in the system.</span></span>

-   <span data-ttu-id="0c1b0-469">Le chiamate ai metodi [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) restituiscono MF \_ E \_ INVALIDMEDIATYPE.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-469">Calls to [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) methods return MF\_E\_INVALIDMEDIATYPE.</span></span>

    <span data-ttu-id="0c1b0-470">Verificare che siano soddisfatte le condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="0c1b0-470">Make sure that the following conditions are true:</span></span>

    -   <span data-ttu-id="0c1b0-471">Il tipo di input o il tipo di output specificato è compatibile con i tipi di supporto supportati dal codificatore.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-471">The input type or the output type that you specified is compatible with media types that the encoder supports.</span></span>
    -   <span data-ttu-id="0c1b0-472">I tipi di supporto specificati sono completi.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-472">The media types that you specified are complete.</span></span> <span data-ttu-id="0c1b0-473">Per completare i tipi di supporto, vedere gli attributi obbligatori nella sezione "creare un tipo di supporto audio compresso" e "creare un tipo di supporto video compresso" di questa esercitazione.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-473">For media types to be complete, see the required attributes in the "Create a Compressed Audio Media Type" and "Create a Compressed Video Media Type" sections of this tutorial.</span></span>
    -   <span data-ttu-id="0c1b0-474">Assicurarsi di aver impostato la velocità in bit di destinazione per il tipo di supporto parziale a cui si aggiungono i dati privati del codec.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-474">Make sure that you have set the target bit rate on the partial media type to which you are adding the codec private data.</span></span>

-   <span data-ttu-id="0c1b0-475">La sessione multimediale restituisce \_ \_ \_ il tipo D3D non supportato \_ nello stato dell'evento.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-475">The Media Session returns MF\_E\_UNSUPPORTED\_D3D\_TYPE in the event status.</span></span>

    <span data-ttu-id="0c1b0-476">Questo errore viene restituito quando il tipo di supporto dell'origine indica una modalità mista a interlacciamento non supportata dal codificatore Windows Media Video.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-476">This error is returned when the source's media type indicates a mixed interlace mode that is not supported by Windows Media Video encoder.</span></span> <span data-ttu-id="0c1b0-477">Se il tipo di supporto video compresso è impostato per usare la modalità progressiva, la pipeline deve usare una trasformazione di deinterlacciamento.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-477">If your compressed video media type is set to use progressive mode, the pipeline must use a de-interlacing transform.</span></span> <span data-ttu-id="0c1b0-478">Poiché la pipeline non è in grado di trovare una corrispondenza (indicata dal codice di errore), è necessario inserire manualmente un decodificatore (transcodificatore video) tra i nodi del codificatore e del codificatore.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-478">Because the pipeline is unable to find a match (indicated by this error code), you must insert a de-interlacer (transcode video processor) between the decoder and encoder nodes manually.</span></span>

-   <span data-ttu-id="0c1b0-479">La sessione multimediale restituisce E \_ INVALIDARG nello stato dell'evento.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-479">The Media Session returns E\_INVALIDARG in the event status.</span></span>

    <span data-ttu-id="0c1b0-480">Questo errore viene restituito quando gli attributi del tipo di supporto di origine non sono compatibili con gli attributi del tipo di supporto di output impostato nel codificatore Windows Media.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-480">This error is returned when the source's media type attributes are not compatible with the attributes of the output media type set on the Windows Media encoder.</span></span>

-   <span data-ttu-id="0c1b0-481">[**IWMCodecPrivateData:: GetPrivateData**](../wmformat/iwmcodecprivatedata-getprivatedata.md) restituisce HRESULT 0x80040203 "si è verificato un errore di sintassi durante il tentativo di valutare una stringa di query"</span><span class="sxs-lookup"><span data-stu-id="0c1b0-481">[**IWMCodecPrivateData::GetPrivateData**](../wmformat/iwmcodecprivatedata-getprivatedata.md) returns HRESULT 0x80040203 "A syntax error occurred trying to evaluate a query string"</span></span>

    <span data-ttu-id="0c1b0-482">Verificare che il tipo di input sia impostato sul codificatore MFT.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-482">Make sure that the input type is set on the encoder MFT.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0c1b0-483">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0c1b0-483">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c1b0-484">Componenti ASF a livello pipeline</span><span class="sxs-lookup"><span data-stu-id="0c1b0-484">Pipeline Layer ASF Components</span></span>](pipeline-layer-asf-components.md)
</dt> </dl>

 

 
