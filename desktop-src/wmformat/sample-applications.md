---
title: Applicazioni di esempio di Windows Media Format SDK
description: Applicazioni di esempio di Windows Media Format SDK
ms.assetid: 037741cb-c5fb-485f-bf62-79b5465abfe4
keywords:
- Windows Media Format SDK, applicazioni di esempio
- Digital Rights Management (DRM), applicazioni di esempio
- DRM (Digital Rights Management), applicazioni di esempio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20ce7a9baf53c289e9420cf3c226bf21a3c6bd16
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104474867"
---
# <a name="windows-media-format-sdk-sample-applications"></a><span data-ttu-id="66caa-106">Applicazioni di esempio di Windows Media Format SDK</span><span class="sxs-lookup"><span data-stu-id="66caa-106">Windows Media Format SDK Sample Applications</span></span>

<span data-ttu-id="66caa-107">Il codice di esempio fornito con questo SDK è sotto forma di progetti per Microsoft Visual Studio 2005.</span><span class="sxs-lookup"><span data-stu-id="66caa-107">The sample code supplied with this SDK is in the form of projects for Microsoft Visual Studio 2005.</span></span> <span data-ttu-id="66caa-108">La maggior parte degli esempi è in C++, ma ManagedWMFSDKWrapper e ManagedMetadataEdit richiedono C#.</span><span class="sxs-lookup"><span data-stu-id="66caa-108">Most of the samples are in C++, but ManagedWMFSDKWrapper and ManagedMetadataEdit require C#.</span></span>

<span data-ttu-id="66caa-109">Questi esempi non funzioneranno a meno che non sia stato installato Windows Media Format SDK o Windows Player SDK.</span><span class="sxs-lookup"><span data-stu-id="66caa-109">These samples will not work unless the Windows Media Format SDK or the Windows Player SDK has been installed.</span></span>

<span data-ttu-id="66caa-110">Le informazioni sull'utilizzo per ogni campione sono contenute in un file di readme.txt in ogni directory di esempio.</span><span class="sxs-lookup"><span data-stu-id="66caa-110">Usage information for each sample is contained in a readme.txt file in each sample directory.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="66caa-111">Samle</span><span class="sxs-lookup"><span data-stu-id="66caa-111">Samle</span></span></th>
<th><span data-ttu-id="66caa-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="66caa-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="66caa-113">AudioPlayer</span><span class="sxs-lookup"><span data-stu-id="66caa-113">AudioPlayer</span></span></td>
<td><span data-ttu-id="66caa-114">Riproduce file Windows Media, inclusi i file protetti da DRM.</span><span class="sxs-lookup"><span data-stu-id="66caa-114">Plays Windows Media files including DRM-protected files.</span></span> <span data-ttu-id="66caa-115">Viene controllata tramite un'interfaccia utente grafica e i comandi includono Play, pause, seek e stop.</span><span class="sxs-lookup"><span data-stu-id="66caa-115">It is controlled through a GUI, and commands include Play, Pause, Seek and Stop.</span></span> <span data-ttu-id="66caa-116">Può riprodurre file o file locali letti da Internet (incluso l'output in Internet usando l'esempio WMVNetWrite).</span><span class="sxs-lookup"><span data-stu-id="66caa-116">It can play local files or files read from the Internet (including those output to the Internet by using the WMVNetWrite sample).</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="66caa-117">Le parti DRM di questo esempio non sono supportate nelle versioni di Windows basate su x64.</span><span class="sxs-lookup"><span data-stu-id="66caa-117">The DRM portions of this sample are not supported on x64-based versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66caa-118">DRMHeader</span><span class="sxs-lookup"><span data-stu-id="66caa-118">DRMHeader</span></span></td>
<td><span data-ttu-id="66caa-119">DRMHeader è un'applicazione console che usa l'interfaccia <a href="/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor"><strong>IWMDRMEditor</strong></a> dell'editor dei metadati per leggere gli attributi DRM dei file senza collegarsi alla libreria statica DRM.</span><span class="sxs-lookup"><span data-stu-id="66caa-119">DRMHeader is a console application that uses the metadata editor's <a href="/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor"><strong>IWMDRMEditor</strong></a> interface to read DRM attributes of files without linking to the DRM static library.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="66caa-120">Questo esempio non è supportato nelle versioni di Windows basate su x64.</span><span class="sxs-lookup"><span data-stu-id="66caa-120">This sample is not supported on x64-based versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66caa-121">DRMShow</span><span class="sxs-lookup"><span data-stu-id="66caa-121">DRMShow</span></span></td>
<td><span data-ttu-id="66caa-122">DRMShow è un'applicazione console che Mostra come leggere le proprietà <a href="wmformat-glossary.md"><em>DRM</em></a> di un file Windows Media usando il metodo <strong>IWMDRMReader:: GetDRMProperty</strong> . Questo esempio illustra l'uso del metodo <strong>IWMDRMReader:: GetDRMProperty</strong> e delle proprietà che possono essere recuperate dal lettore DRM.</span><span class="sxs-lookup"><span data-stu-id="66caa-122">DRMShow is a console application that shows how to read <a href="wmformat-glossary.md"><em>DRM</em></a> properties of a Windows Media file using the <strong>IWMDRMReader::GetDRMProperty</strong> method.This sample demonstrates the use of the <strong>IWMDRMReader::GetDRMProperty</strong> method and the properties that can be retrieved from the DRM reader.</span></span> <span data-ttu-id="66caa-123">Non viene illustrato come acquisire una licenza per il contenuto protetto da DRM.</span><span class="sxs-lookup"><span data-stu-id="66caa-123">It does not demonstrate how to acquire a license for DRM-protected content.</span></span> <span data-ttu-id="66caa-124">Questo esempio richiede la libreria stub DRM WMStubDRM. lib per la compilazione.</span><span class="sxs-lookup"><span data-stu-id="66caa-124">This sample requires the DRM stub library WMStubDRM.lib to build.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="66caa-125">Questo esempio non è supportato nelle versioni di Windows basate su x64.</span><span class="sxs-lookup"><span data-stu-id="66caa-125">This sample is not supported on x64-based versions of Windows.</span></span>
</blockquote>
<br/> <span data-ttu-id="66caa-126">Quando si acquisisce WMStubDRM. lib da Microsoft, alla libreria viene assegnato un livello di sicurezza dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="66caa-126">When you acquire the WMStubDRM.lib from Microsoft, the library is assigned an application security level.</span></span> <span data-ttu-id="66caa-127">Se il livello di sicurezza della libreria ricevuta non è sufficiente per riprodurre un file protetto, in questo esempio verrà visualizzato un errore.</span><span class="sxs-lookup"><span data-stu-id="66caa-127">If the security level of the library you receive is not sufficient to play a protected file, this sample will display an error.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66caa-128">DirectShowInterop/DSCopy</span><span class="sxs-lookup"><span data-stu-id="66caa-128">DirectShowInterop/DSCopy</span></span></td>
<td><span data-ttu-id="66caa-129">Consente di eseguire la transcodifica di uno o più file in un file ASF usando il filtro del writer ASF di DirectShow WM.</span><span class="sxs-lookup"><span data-stu-id="66caa-129">Transcodes one or more files to an ASF file using the DirectShow  WM ASF Writer filter.</span></span> <span data-ttu-id="66caa-130">Il file di input può essere qualsiasi formato compresso o non compresso supportato da DirectShow.</span><span class="sxs-lookup"><span data-stu-id="66caa-130">The input file may be any compressed or uncompressed format supported by DirectShow.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66caa-131">DirectShowInterop/DSPlay</span><span class="sxs-lookup"><span data-stu-id="66caa-131">DirectShowInterop/DSPlay</span></span></td>
<td><span data-ttu-id="66caa-132">Questo esempio è un lettore di file multimediale audio/video interattivo con supporto <a href="wmformat-glossary.md"><em>DRM</em></a> .</span><span class="sxs-lookup"><span data-stu-id="66caa-132">This sample is an interactive audio/video media file player with <a href="wmformat-glossary.md"><em>DRM</em></a> support.</span></span> <span data-ttu-id="66caa-133">Usa il filtro per i lettori WM ASF di DirectShow per riprodurre file Windows Media (ASF, WMA, WMV) senza protezione DRM e file che usano DRM a un livello di 100 o di seguito.</span><span class="sxs-lookup"><span data-stu-id="66caa-133">It uses DirectShow's WM ASF Reader filter to play Windows Media files (ASF, WMA, WMV) without DRM protection and files which use DRM at a level of 100 or below.</span></span> <span data-ttu-id="66caa-134">Per ulteriori informazioni, vedere readme.txt nella directory dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="66caa-134">See readme.txt in the sample's directory for more information.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66caa-135">DirectShowInterop/DSSeekFm</span><span class="sxs-lookup"><span data-stu-id="66caa-135">DirectShowInterop/DSSeekFm</span></span></td>
<td><span data-ttu-id="66caa-136">In questo esempio viene illustrato come utilizzare il filtro lettore ASF di DirectShow WM per riprodurre contenuto ASF in un grafico filtro DirectShow e come utilizzare il frame che cerca supporto in Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="66caa-136">This sample demonstrates how to use the DirectShow WM ASF Reader Filter to play ASF content in a DirectShow filter graph, and also how to use the frame seeking support in the Windows Media Format SDK.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66caa-137">Gestito/WMFSDKWrapper</span><span class="sxs-lookup"><span data-stu-id="66caa-137">Managed/WMFSDKWrapper</span></span></td>
<td><span data-ttu-id="66caa-138">Questo assembly gestito funge da wrapper utilizzato dagli esempi di codice gestito per accedere ad alcune interfacce di metadati di questo SDK.</span><span class="sxs-lookup"><span data-stu-id="66caa-138">This managed assembly serves as a wrapper used by managed-code samples for accessing some metadata interfaces of this SDK.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66caa-139">Gestito/MetadataEdit</span><span class="sxs-lookup"><span data-stu-id="66caa-139">Managed/MetadataEdit</span></span></td>
<td><span data-ttu-id="66caa-140">Questa applicazione C# può essere usata per visualizzare e modificare i metadati dai file di Windows Media.</span><span class="sxs-lookup"><span data-stu-id="66caa-140">This C# application can be used to view and edit metadata from Windows Media files.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66caa-141">MetaDataEdit</span><span class="sxs-lookup"><span data-stu-id="66caa-141">MetaDataEdit</span></span></td>
<td><span data-ttu-id="66caa-142">Si tratta di una versione C++ dell'applicazione MetadataEdit gestita.</span><span class="sxs-lookup"><span data-stu-id="66caa-142">This is a C++ version of the Managed MetadataEdit application.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66caa-143">ReadFromStream</span><span class="sxs-lookup"><span data-stu-id="66caa-143">ReadFromStream</span></span></td>
<td><span data-ttu-id="66caa-144">Questo esempio di applicazione console Mostra come leggere i dati da <strong>IStream</strong> con WMReader.</span><span class="sxs-lookup"><span data-stu-id="66caa-144">This console application sample shows how to read data from <strong>IStream</strong> with WMReader.</span></span> <span data-ttu-id="66caa-145">L'origine <strong>IStream</strong> è stata implementata per usare un file in formato Windows Media (WMA/WMV/ASF).</span><span class="sxs-lookup"><span data-stu-id="66caa-145"><strong>IStream</strong> source has been implemented to use a file in Windows Media Format (WMA/WMV/ASF).</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="66caa-146">Questo esempio non Mostra come elaborare gli esempi di supporti provenienti da WMReader.</span><span class="sxs-lookup"><span data-stu-id="66caa-146">This sample does not show how to process the media samples coming out of WMReader.</span></span> <span data-ttu-id="66caa-147">Per esempi su come elaborare audio/video o altri tipi di esempi multimediali, fare riferimento ad altri esempi, ad esempio AudioPlayer, inclusi in Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="66caa-147">For examples on how to process audio/video or other types of media samples, please refer to other samples, for instance AudioPlayer, that are included with the Windows Media Format SDK.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66caa-148">UncompAVIToWMV</span><span class="sxs-lookup"><span data-stu-id="66caa-148">UncompAVIToWMV</span></span></td>
<td><span data-ttu-id="66caa-149">Questo esempio di applicazione console mostra il codice necessario per comprimere un file AVI in un file WMV.</span><span class="sxs-lookup"><span data-stu-id="66caa-149">This console application sample shows the necessary code to compress an AVI file to a WMV file.</span></span> <span data-ttu-id="66caa-150">Mostra come unire esempi per flussi audio e video da diversi file AVI e unirli in flussi simili o creare un nuovo flusso basato sul profilo del flusso di origine.</span><span class="sxs-lookup"><span data-stu-id="66caa-150">It shows how to merge samples for audio and video streams from several AVI files and either merge these into similar streams or create a new stream based on the source stream profile.</span></span> <span data-ttu-id="66caa-151">Viene inoltre illustrato come creare un flusso arbitrario, eseguire la codifica Multipass, aggiungere codice ora SMPTE e applicare la protezione DRM versione 1.</span><span class="sxs-lookup"><span data-stu-id="66caa-151">It also shows how to create an arbitrary stream, do multipass encoding, add SMPTE time code, and apply DRM version 1 protection.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66caa-152">WMGenProfile/exe</span><span class="sxs-lookup"><span data-stu-id="66caa-152">WMGenProfile/exe</span></span></td>
<td><span data-ttu-id="66caa-153">Questo esempio è stato aggiornato dalla versione 7,1.</span><span class="sxs-lookup"><span data-stu-id="66caa-153">This sample has been updated from the 7.1 release.</span></span> <span data-ttu-id="66caa-154">È ora un'applicazione di dialogo MFC.</span><span class="sxs-lookup"><span data-stu-id="66caa-154">It is now an MFC Dialog application.</span></span> <span data-ttu-id="66caa-155">L'esempio WMGenProfile illustra l'uso della libreria statica WMGenProfile.</span><span class="sxs-lookup"><span data-stu-id="66caa-155">WMGenProfile sample demonstrates the use of the WMGenProfile static library.</span></span> <span data-ttu-id="66caa-156">Funge anche da strumento per la creazione di profili.</span><span class="sxs-lookup"><span data-stu-id="66caa-156">It also serves as a tool for the creation of profiles.</span></span> <span data-ttu-id="66caa-157">Questo strumento è destinato agli sviluppatori che hanno familiarità con il formato Windows Media.</span><span class="sxs-lookup"><span data-stu-id="66caa-157">This tool is meant for developers familiar with the Windows Media Format.</span></span> <span data-ttu-id="66caa-158">L'interfaccia utente non è stata testata per l'esperienza utente e non è destinata a una raccomandazione su come presentare queste informazioni a un utente.</span><span class="sxs-lookup"><span data-stu-id="66caa-158">The UI has not been tested for user experience and is not meant as a recommendation about how to present this information to a user.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66caa-159">WMGenProfile/lib</span><span class="sxs-lookup"><span data-stu-id="66caa-159">WMGenProfile/lib</span></span></td>
<td><span data-ttu-id="66caa-160">Nell'esempio di libreria GenProfile viene illustrata la creazione di profili.</span><span class="sxs-lookup"><span data-stu-id="66caa-160">The GenProfile library sample demonstrates the creation of profiles.</span></span> <span data-ttu-id="66caa-161">Viene illustrato come creare flussi e tipi di supporti per diversi tipi di flusso (audio, video, script, immagine, trasferimento di file e Web).</span><span class="sxs-lookup"><span data-stu-id="66caa-161">It shows how to create media types and streams for various stream types (audio, video, script, image, file transfer, and Web).</span></span> <span data-ttu-id="66caa-162">Non viene illustrato come utilizzare i profili di sistema o come convertire i profili di sistema in profili che specificano i codec della serie Windows Media Audio e video 9.</span><span class="sxs-lookup"><span data-stu-id="66caa-162">It does not demonstrate how to work with system profiles or how to convert system profiles to profiles that specify the Windows Media Audio and Video 9 Series codecs.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66caa-163">WMProp</span><span class="sxs-lookup"><span data-stu-id="66caa-163">WMProp</span></span></td>
<td><span data-ttu-id="66caa-164">In questa applicazione console viene illustrato come recuperare gli attributi utilizzando l'oggetto dell'editor dei metadati e le informazioni sul profilo dal reader.</span><span class="sxs-lookup"><span data-stu-id="66caa-164">This console application demonstrates how to retrieve attributes by using the metadata editor object and profile information from the reader.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66caa-165">WMStats</span><span class="sxs-lookup"><span data-stu-id="66caa-165">WMStats</span></span></td>
<td><span data-ttu-id="66caa-166">Questa applicazione console Visualizza le statistiche di Reader e writer.</span><span class="sxs-lookup"><span data-stu-id="66caa-166">This console application displays Reader and Writer statistics.</span></span> <span data-ttu-id="66caa-167">È anche possibile usare più istanze di WMStats contemporaneamente in un computer.</span><span class="sxs-lookup"><span data-stu-id="66caa-167">Multiple instances of WMStats can also be used concurrently on one machine.</span></span> <span data-ttu-id="66caa-168">Avviare un'istanza di come server per inviare il flusso alla rete e quindi eseguire una seconda istanza come client per verificare che il flusso del server sia corretto.</span><span class="sxs-lookup"><span data-stu-id="66caa-168">Start one instance as a server to send the stream to the network and then run a second instance as a client to verify that server is streaming correctly.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66caa-169">WMSyncReader</span><span class="sxs-lookup"><span data-stu-id="66caa-169">WMSyncReader</span></span></td>
<td><span data-ttu-id="66caa-170">Questo esempio di applicazione console Mostra come leggere un file multimediale usando <strong>IWMSyncReader</strong> senza creare alcun thread aggiuntivo o usare i callback.</span><span class="sxs-lookup"><span data-stu-id="66caa-170">This console application sample shows how to read a media file using <strong>IWMSyncReader</strong> without creating any extra thread or using callbacks.</span></span> <span data-ttu-id="66caa-171">Sono state implementate le funzionalità seguenti: lettura di esempi compressi o decompressi</span><span class="sxs-lookup"><span data-stu-id="66caa-171">The following features are implemented :Reading compressed or decompressed samples</span></span><br/> <span data-ttu-id="66caa-172">Ricerca basata sul tempo</span><span class="sxs-lookup"><span data-stu-id="66caa-172">Time-based seeking</span></span><br/> <span data-ttu-id="66caa-173">Ricerca basata su frame</span><span class="sxs-lookup"><span data-stu-id="66caa-173">Frame-based seeking</span></span><br/> <span data-ttu-id="66caa-174">Origine derivata <strong>IStream</strong></span><span class="sxs-lookup"><span data-stu-id="66caa-174"><strong>IStream</strong> derived source</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66caa-175">WMVAppend</span><span class="sxs-lookup"><span data-stu-id="66caa-175">WMVAppend</span></span></td>
<td><span data-ttu-id="66caa-176">Questa applicazione console accetta due file di Windows Media per l'input e tenta di creare un file di output con il contenuto del primo seguito dal secondo.</span><span class="sxs-lookup"><span data-stu-id="66caa-176">This console application takes two Windows Media files for input, and attempts to create an output file with the contents of the first followed by the second.</span></span> <span data-ttu-id="66caa-177">Nell'esempio vengono confrontati i profili dei due file di input per assicurarsi che siano sufficientemente simili da accodare.</span><span class="sxs-lookup"><span data-stu-id="66caa-177">The sample compares the profiles of the two input files to ensure they are similar enough to be appended.</span></span> <span data-ttu-id="66caa-178">In caso contrario, viene visualizzato un messaggio di errore.</span><span class="sxs-lookup"><span data-stu-id="66caa-178">If this is not the case, an error message appears.</span></span> <span data-ttu-id="66caa-179">Ad esempio, un messaggio di errore si verifica quando un file è solo audio e il secondo è un file audio-video o quando due file audio hanno velocità in bit diverse. L'esempio accetta le origini della velocità in bit variabile (VBR).</span><span class="sxs-lookup"><span data-stu-id="66caa-179">For example, an error message occurs when one file is audio only and the second is an audio-video file, or when two audio files have different bit rates.The sample accepts variable bit rate (VBR) sources.</span></span> <span data-ttu-id="66caa-180">Tuttavia, quando si confrontano i profili delle due origini VBR, l'esempio Ignora la differenza media della velocità in bit perché due flussi VBR avranno frequenze di bit medie diverse anche se sono state create con lo stesso profilo.</span><span class="sxs-lookup"><span data-stu-id="66caa-180">However, when comparing the profiles of the two VBR sources, the sample ignores the average bit rate difference because two VBR streams will have different average bit rates even if they were created using the same profile.</span></span> <span data-ttu-id="66caa-181">WMVAppend non è in grado di confrontare la velocità in bit massima dei flussi VBR non vincolati basati sulla velocità in bit o il livello di qualità dei flussi VBR basati sulla qualità, perché queste informazioni non sono presenti nei file di origine.</span><span class="sxs-lookup"><span data-stu-id="66caa-181">WMVAppend cannot compare the peak bit rate of unconstrained bit-rate-based VBR streams, or the quality level of quality-based VBR streams, because this information does not exist in the source files.</span></span> <span data-ttu-id="66caa-182">È pertanto responsabilità dell'utente verificare che vengano creati due file di origine usando lo stesso profilo.</span><span class="sxs-lookup"><span data-stu-id="66caa-182">It is therefore the user's responsibility to make sure that two source files are created using the same profile.</span></span> <span data-ttu-id="66caa-183">In caso contrario, è possibile creare contenuto non valido.</span><span class="sxs-lookup"><span data-stu-id="66caa-183">Otherwise, invalid content can be created.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66caa-184">WMVCopy</span><span class="sxs-lookup"><span data-stu-id="66caa-184">WMVCopy</span></span></td>
<td><span data-ttu-id="66caa-185">In questo esempio viene illustrato il codice necessario per copiare un file WMV.</span><span class="sxs-lookup"><span data-stu-id="66caa-185">This sample shows the code necessary to copy a WMV file.</span></span> <span data-ttu-id="66caa-186">Viene illustrato come leggere e scrivere esempi compressi, leggere gli attributi e gli script di intestazione e modificare gli attributi dell'intestazione.</span><span class="sxs-lookup"><span data-stu-id="66caa-186">It shows how to read and write compressed samples, read header attributes and scripts, and modify header attributes.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66caa-187">WMVNetWrite</span><span class="sxs-lookup"><span data-stu-id="66caa-187">WMVNetWrite</span></span></td>
<td><span data-ttu-id="66caa-188">Questa applicazione console Mostra come un file di Windows Media viene trasmesso attraverso Internet.</span><span class="sxs-lookup"><span data-stu-id="66caa-188">This console application shows how a Windows Media file is streamed across the Internet.</span></span> <span data-ttu-id="66caa-189">Per l'esempio è necessario specificare una porta e quindi il file può essere riprodotto utilizzando un lettore.</span><span class="sxs-lookup"><span data-stu-id="66caa-189">The sample requires a port to be specified, and then the file can be played using a player.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66caa-190">WMVRecompress</span><span class="sxs-lookup"><span data-stu-id="66caa-190">WMVRecompress</span></span></td>
<td><span data-ttu-id="66caa-191">Questa applicazione console Mostra come ricomprimere un file WMV.</span><span class="sxs-lookup"><span data-stu-id="66caa-191">This console application shows how to recompress a WMV file.</span></span> <span data-ttu-id="66caa-192">Viene illustrata la lettura di esempi non compressi, la scrittura di esempi non compressi e la codifica Multipass, l'output multicanale e la ricompressione intelligente.</span><span class="sxs-lookup"><span data-stu-id="66caa-192">It demonstrates reading uncompressed samples, writing uncompressed samples, and doing multi-pass encoding, multi-channel output, and smart recompression.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="66caa-193">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="66caa-193">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="66caa-194">**Informazioni su Windows Media Format SDK**</span><span class="sxs-lookup"><span data-stu-id="66caa-194">**About the Windows Media Format SDK**</span></span>](about-the-windows-media-format-sdk.md)
</dt> <dt>

[<span data-ttu-id="66caa-195">**Guida per programmatori**</span><span class="sxs-lookup"><span data-stu-id="66caa-195">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 





