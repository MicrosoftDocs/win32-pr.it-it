---
title: Interfacce IMAPi
description: Le tabelle seguenti identificano e descrivono brevemente le interfacce usate dagli sviluppatori C/C++ e dall'oggetto di scripting associato. Anteporre il prefisso \ 0034; IMAPI2 al nome dell'oggetto nella tabella. \ 0034; per qualificare completamente il nome dell'oggetto durante la creazione dell'oggetto nello script.
ms.assetid: dba81a45-34a8-4b49-9ccb-d61a7e7ee1f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bac989a9871b761a1f1700ec599cc51affd30b2e
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/11/2020
ms.locfileid: "106299357"
---
# <a name="imapi-interfaces"></a><span data-ttu-id="64a85-105">Interfacce IMAPi</span><span class="sxs-lookup"><span data-stu-id="64a85-105">IMAPI Interfaces</span></span>

<span data-ttu-id="64a85-106">Le tabelle seguenti identificano e descrivono brevemente le interfacce usate dagli sviluppatori C/C++ e dall'oggetto di scripting associato.</span><span class="sxs-lookup"><span data-stu-id="64a85-106">The following tables identify and briefly describe the interfaces used C/C++ developers and the associated scripting object.</span></span> <span data-ttu-id="64a85-107">Anteporre il prefisso "IMAPI2" al nome dell'oggetto nella tabella.</span><span class="sxs-lookup"><span data-stu-id="64a85-107">Prefix the object name in the table with "IMAPI2."</span></span> <span data-ttu-id="64a85-108">per qualificare completamente il nome dell'oggetto durante la creazione dell'oggetto nello script.</span><span class="sxs-lookup"><span data-stu-id="64a85-108">to fully qualify the object name when creating the object in script.</span></span>

<span data-ttu-id="64a85-109">La tabella seguente elenca le interfacce associate a dispositivi, il motore di masterizzazione e il formato writer e gomma.</span><span class="sxs-lookup"><span data-stu-id="64a85-109">The following table lists the interfaces associated with devices, the burn engine, and the format writers and eraser.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="64a85-110">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="64a85-110">Interface</span></span></td>
<td><span data-ttu-id="64a85-111">Oggetto</span><span class="sxs-lookup"><span data-stu-id="64a85-111">Object</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64a85-112">Motore di masterizzazione di basso livello.</span><span class="sxs-lookup"><span data-stu-id="64a85-112">Low-level burn engine.</span></span>
<ul>
<li><span data-ttu-id="64a85-113"><a href="/windows/desktop/api/imapi2/nn-imapi2-dwriteengine2events"><strong>DWriteEngine2Events</strong></a></span><span class="sxs-lookup"><span data-stu-id="64a85-113"><a href="/windows/desktop/api/imapi2/nn-imapi2-dwriteengine2events"><strong>DWriteEngine2Events</strong></a></span></span></li>
<li><span data-ttu-id="64a85-114"><a href="/windows/desktop/api/imapi2/nn-imapi2-iwriteengine2"><strong>IWriteEngine2</strong></a></span><span class="sxs-lookup"><span data-stu-id="64a85-114"><a href="/windows/desktop/api/imapi2/nn-imapi2-iwriteengine2"><strong>IWriteEngine2</strong></a></span></span></li>
<li><span data-ttu-id="64a85-115"><a href="/windows/desktop/api/imapi2/nn-imapi2-iwriteengine2eventargs"><strong>IWriteEngine2EventArgs</strong></a></span><span class="sxs-lookup"><span data-stu-id="64a85-115"><a href="/windows/desktop/api/imapi2/nn-imapi2-iwriteengine2eventargs"><strong>IWriteEngine2EventArgs</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="64a85-116">MsftWriteEngine2</span><span class="sxs-lookup"><span data-stu-id="64a85-116">MsftWriteEngine2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="64a85-117">Autore dell'immagine principale.</span><span class="sxs-lookup"><span data-stu-id="64a85-117">Main image writer.</span></span>
<ul>
<li><span data-ttu-id="64a85-118"><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2dataevents"><strong>DDiscFormat2DataEvents</strong></a></span><span class="sxs-lookup"><span data-stu-id="64a85-118"><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2dataevents"><strong>DDiscFormat2DataEvents</strong></a></span></span></li>
<li><span data-ttu-id="64a85-119"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data"><strong>IDiscFormat2Data</strong></a></span><span class="sxs-lookup"><span data-stu-id="64a85-119"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data"><strong>IDiscFormat2Data</strong></a></span></span></li>
<li><span data-ttu-id="64a85-120"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2dataeventargs"><strong>IDiscFormat2DataEventArgs</strong></a></span><span class="sxs-lookup"><span data-stu-id="64a85-120"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2dataeventargs"><strong>IDiscFormat2DataEventArgs</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="64a85-121">MsftDiscFormat2Data</span><span class="sxs-lookup"><span data-stu-id="64a85-121">MsftDiscFormat2Data</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64a85-122">Gomma del disco.</span><span class="sxs-lookup"><span data-stu-id="64a85-122">Disc eraser.</span></span>
<ul>
<li><span data-ttu-id="64a85-123"><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2eraseevents"><strong>DDiscFormat2EraseEvents</strong></a></span><span class="sxs-lookup"><span data-stu-id="64a85-123"><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2eraseevents"><strong>DDiscFormat2EraseEvents</strong></a></span></span></li>
<li><span data-ttu-id="64a85-124"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase"><strong>IDiscFormat2Erase</strong></a></span><span class="sxs-lookup"><span data-stu-id="64a85-124"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase"><strong>IDiscFormat2Erase</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="64a85-125">MsftDiscFormat2Erase</span><span class="sxs-lookup"><span data-stu-id="64a85-125">MsftDiscFormat2Erase</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="64a85-126">Writer di immagini non elaborate.</span><span class="sxs-lookup"><span data-stu-id="64a85-126">Raw image writer.</span></span>
<ul>
<li><span data-ttu-id="64a85-127"><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2rawcdevents"><strong>DDiscFormat2RawCDEvents</strong></a></span><span class="sxs-lookup"><span data-stu-id="64a85-127"><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2rawcdevents"><strong>DDiscFormat2RawCDEvents</strong></a></span></span></li>
<li><span data-ttu-id="64a85-128"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd"><strong>IDiscFormat2RawCD</strong></a></span><span class="sxs-lookup"><span data-stu-id="64a85-128"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd"><strong>IDiscFormat2RawCD</strong></a></span></span></li>
<li><span data-ttu-id="64a85-129"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcdeventargs"><strong>IDiscFormat2RawCDEventArgs</strong></a></span><span class="sxs-lookup"><span data-stu-id="64a85-129"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcdeventargs"><strong>IDiscFormat2RawCDEventArgs</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="64a85-130">MsftDiscFormat2RawCD</span><span class="sxs-lookup"><span data-stu-id="64a85-130">MsftDiscFormat2RawCD</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64a85-131">Writer di immagini Track-at-once.</span><span class="sxs-lookup"><span data-stu-id="64a85-131">Track-At-Once image writer.</span></span>
<ul>
<li><span data-ttu-id="64a85-132"><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2trackatonceevents"><strong>DDiscFormat2TrackAtOnceEvents</strong></a></span><span class="sxs-lookup"><span data-stu-id="64a85-132"><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2trackatonceevents"><strong>DDiscFormat2TrackAtOnceEvents</strong></a></span></span></li>
<li><span data-ttu-id="64a85-133"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonce"><strong>IDiscFormat2TrackAtOnce</strong></a></span><span class="sxs-lookup"><span data-stu-id="64a85-133"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonce"><strong>IDiscFormat2TrackAtOnce</strong></a></span></span></li>
<li><span data-ttu-id="64a85-134"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonceeventargs"><strong>IDiscFormat2TrackAtOnceEventArgs</strong></a></span><span class="sxs-lookup"><span data-stu-id="64a85-134"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonceeventargs"><strong>IDiscFormat2TrackAtOnceEventArgs</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="64a85-135">MsftDiscFormat2TrackAtOnce</span><span class="sxs-lookup"><span data-stu-id="64a85-135">MsftDiscFormat2TrackAtOnce</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="64a85-136">Enumerazione dei dispositivi disco nell'elenco hardware del sistema.</span><span class="sxs-lookup"><span data-stu-id="64a85-136">Enumeration of disc devices in the system hardware list.</span></span>
<ul>
<li><span data-ttu-id="64a85-137"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2"><strong>IDiscMaster2</strong></a></span><span class="sxs-lookup"><span data-stu-id="64a85-137"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2"><strong>IDiscMaster2</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="64a85-138">MsftDiscMaster2</span><span class="sxs-lookup"><span data-stu-id="64a85-138">MsftDiscMaster2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64a85-139">Delegato di notifica per l'oggetto MsftDiscMaster2.</span><span class="sxs-lookup"><span data-stu-id="64a85-139">Notification delegate for the MsftDiscMaster2 object.</span></span>
<ul>
<li><span data-ttu-id="64a85-140"><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscmaster2events"><strong>DDiscMaster2Events</strong></a></span><span class="sxs-lookup"><span data-stu-id="64a85-140"><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscmaster2events"><strong>DDiscMaster2Events</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="64a85-141">DDiscMaster2Events</span><span class="sxs-lookup"><span data-stu-id="64a85-141">DDiscMaster2Events</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="64a85-142">Singolo dispositivo di registrazione.</span><span class="sxs-lookup"><span data-stu-id="64a85-142">Individual recording device.</span></span>
<ul>
<li><span data-ttu-id="64a85-143"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2"><strong>IDiscRecorder2</strong></a></span><span class="sxs-lookup"><span data-stu-id="64a85-143"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2"><strong>IDiscRecorder2</strong></a></span></span></li>
<li><span data-ttu-id="64a85-144"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2ex"><strong>IDiscRecorder2Ex</strong></a></span><span class="sxs-lookup"><span data-stu-id="64a85-144"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2ex"><strong>IDiscRecorder2Ex</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="64a85-145">MsftDiscRecorder2</span><span class="sxs-lookup"><span data-stu-id="64a85-145">MsftDiscRecorder2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64a85-146">Attributi di scrittura del dispositivo, inclusi il tipo di supporto, la velocità di scrittura e il tipo di controllo della velocità angolare.</span><span class="sxs-lookup"><span data-stu-id="64a85-146">Device writing attributes, including the media type, writing speed, and type of angular velocity control.</span></span>
<ul>
<li><span data-ttu-id="64a85-147"><a href="/windows/desktop/api/imapi2/nn-imapi2-iwritespeeddescriptor"><strong>IWriteSpeedDescriptor</strong></a></span><span class="sxs-lookup"><span data-stu-id="64a85-147"><a href="/windows/desktop/api/imapi2/nn-imapi2-iwritespeeddescriptor"><strong>IWriteSpeedDescriptor</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="64a85-148">MsftWriteSpeedDescriptor</span><span class="sxs-lookup"><span data-stu-id="64a85-148">MsftWriteSpeedDescriptor</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="64a85-149">Nella tabella seguente sono elencate le interfacce file system.</span><span class="sxs-lookup"><span data-stu-id="64a85-149">The following table lists the file system interfaces.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="64a85-150">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="64a85-150">Interface</span></span></td>
<td><span data-ttu-id="64a85-151">Oggetto</span><span class="sxs-lookup"><span data-stu-id="64a85-151">Object</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64a85-152">Flusso di immagini d'avvio e proprietà per l'integrazione dell'immagine di avvio nell'immagine del disco.</span><span class="sxs-lookup"><span data-stu-id="64a85-152">Boot image stream and properties for integrating the bootable image in the disc image.</span></span>
<ul>
<li><span data-ttu-id="64a85-153"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ibootoptions"><strong>IBootOptions</strong></a></span><span class="sxs-lookup"><span data-stu-id="64a85-153"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ibootoptions"><strong>IBootOptions</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="64a85-154">BootOptions</span><span class="sxs-lookup"><span data-stu-id="64a85-154">BootOptions</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="64a85-155">Immagine e proprietà del file System.</span><span class="sxs-lookup"><span data-stu-id="64a85-155">File system image and properties.</span></span> <span data-ttu-id="64a85-156">Questo oggetto include tutte le tracce e i riferimenti all'immagine di avvio e all'immagine di risultato.</span><span class="sxs-lookup"><span data-stu-id="64a85-156">This object includes all tracks, and references to the boot image and result image.</span></span>
<ul>
<li><span data-ttu-id="64a85-157"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-dfilesystemimageevents"><strong>DFileSystemImageEvents</strong></a></span><span class="sxs-lookup"><span data-stu-id="64a85-157"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-dfilesystemimageevents"><strong>DFileSystemImageEvents</strong></a></span></span></li>
<li><span data-ttu-id="64a85-158"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-dfilesystemimageimportevents"><strong>DFileSystemImageImportEvents</strong></a></span><span class="sxs-lookup"><span data-stu-id="64a85-158"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-dfilesystemimageimportevents"><strong>DFileSystemImageImportEvents</strong></a></span></span></li>
<li><span data-ttu-id="64a85-159"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage"><strong>IFileSystemImage</strong></a></span><span class="sxs-lookup"><span data-stu-id="64a85-159"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage"><strong>IFileSystemImage</strong></a></span></span></li>
<li><span data-ttu-id="64a85-160"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage2"><strong>IFileSystemImage2</strong></a></span><span class="sxs-lookup"><span data-stu-id="64a85-160"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage2"><strong>IFileSystemImage2</strong></a></span></span></li>
<li><span data-ttu-id="64a85-161"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage3"><strong>IFileSystemImage3</strong></a></span><span class="sxs-lookup"><span data-stu-id="64a85-161"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage3"><strong>IFileSystemImage3</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="64a85-162">CFileSystemImage</span><span class="sxs-lookup"><span data-stu-id="64a85-162">CFileSystemImage</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64a85-163">Contenitore del flusso di dati fornito dall'oggetto file system.</span><span class="sxs-lookup"><span data-stu-id="64a85-163">Container of the data stream provided by the file system object.</span></span>
<ul>
<li><span data-ttu-id="64a85-164"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimageresult"><strong>IFileSystemImageResult</strong></a></span><span class="sxs-lookup"><span data-stu-id="64a85-164"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimageresult"><strong>IFileSystemImageResult</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="64a85-165">FileSystemImageResult</span><span class="sxs-lookup"><span data-stu-id="64a85-165">FileSystemImageResult</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="64a85-166">Elemento della directory nell'immagine del file system.</span><span class="sxs-lookup"><span data-stu-id="64a85-166">Directory item in the file system image.</span></span>
<ul>
<li><span data-ttu-id="64a85-167"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem"><strong>Metodo IFsiDirectoryItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="64a85-167"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem"><strong>IFsiDirectoryItem</strong></a></span></span></li>
<li><span data-ttu-id="64a85-168"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem2"><strong>IFsiDirectoryItem2</strong></a></span><span class="sxs-lookup"><span data-stu-id="64a85-168"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem2"><strong>IFsiDirectoryItem2</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="64a85-169">FsiDirectoryItem</span><span class="sxs-lookup"><span data-stu-id="64a85-169">FsiDirectoryItem</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64a85-170">Elemento del file nell'immagine del file system.</span><span class="sxs-lookup"><span data-stu-id="64a85-170">File item in the file system image.</span></span>
<ul>
<li><span data-ttu-id="64a85-171"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsifileitem"><strong>IFsiFileItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="64a85-171"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsifileitem"><strong>IFsiFileItem</strong></a></span></span></li>
<li><span data-ttu-id="64a85-172"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsifileitem2"><strong>IFsiFileItem2</strong></a></span><span class="sxs-lookup"><span data-stu-id="64a85-172"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsifileitem2"><strong>IFsiFileItem2</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="64a85-173">FsiFileItem</span><span class="sxs-lookup"><span data-stu-id="64a85-173">FsiFileItem</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="64a85-174">Interfaccia contenente le proprietà comuni agli elementi di file e directory.</span><span class="sxs-lookup"><span data-stu-id="64a85-174">Interface containing properties common to both file and directory items.</span></span>
<ul>
<li><span data-ttu-id="64a85-175"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsiitem"><strong>IFsiItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="64a85-175"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsiitem"><strong>IFsiItem</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="64a85-176">FsiItem</span><span class="sxs-lookup"><span data-stu-id="64a85-176">FsiItem</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64a85-177">Creazione di un'immagine CD non ELABORAta.</span><span class="sxs-lookup"><span data-stu-id="64a85-177">RAW CD image creation.</span></span>
<ul>
<li><span data-ttu-id="64a85-178"><a href="/windows/desktop/api/imapi2/nn-imapi2-irawcdimagecreator"><strong>IRawCDImageCreator</strong></a></span><span class="sxs-lookup"><span data-stu-id="64a85-178"><a href="/windows/desktop/api/imapi2/nn-imapi2-irawcdimagecreator"><strong>IRawCDImageCreator</strong></a></span></span></li>
<li><span data-ttu-id="64a85-179"><a href="/windows/desktop/api/imapi2/nn-imapi2-irawcdimagetrackinfo"><strong>IRawCDImageTrackInfo</strong></a></span><span class="sxs-lookup"><span data-stu-id="64a85-179"><a href="/windows/desktop/api/imapi2/nn-imapi2-irawcdimagetrackinfo"><strong>IRawCDImageTrackInfo</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="64a85-180">MsftRawCDImageCreator</span><span class="sxs-lookup"><span data-stu-id="64a85-180">MsftRawCDImageCreator</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="64a85-181">Oggetto Stream Helper Object per concatenare più flussi.</span><span class="sxs-lookup"><span data-stu-id="64a85-181">Stream object helper object to concatenate multiple streams.</span></span>
<ul>
<li><span data-ttu-id="64a85-182"><a href="/windows/desktop/api/imapi2/nn-imapi2-istreamconcatenate"><strong>IStreamConcatenate</strong></a></span><span class="sxs-lookup"><span data-stu-id="64a85-182"><a href="/windows/desktop/api/imapi2/nn-imapi2-istreamconcatenate"><strong>IStreamConcatenate</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="64a85-183">MsftStreamConcatenate</span><span class="sxs-lookup"><span data-stu-id="64a85-183">MsftStreamConcatenate</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64a85-184">Flusso con interfoliazione da aggiungere all'immagine del disco.</span><span class="sxs-lookup"><span data-stu-id="64a85-184">Interleaved stream to add to the disc image.</span></span>
<ul>
<li><span data-ttu-id="64a85-185"><a href="/windows/desktop/api/imapi2/nn-imapi2-istreaminterleave"><strong>IStreamInterleave</strong></a></span><span class="sxs-lookup"><span data-stu-id="64a85-185"><a href="/windows/desktop/api/imapi2/nn-imapi2-istreaminterleave"><strong>IStreamInterleave</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="64a85-186">MsftStreamInterleave</span><span class="sxs-lookup"><span data-stu-id="64a85-186">MsftStreamInterleave</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="64a85-187">Flusso generato pseudo-casuale.</span><span class="sxs-lookup"><span data-stu-id="64a85-187">Pseudo-random generated stream.</span></span>
<ul>
<li><span data-ttu-id="64a85-188"><a href="/windows/desktop/api/imapi2/nn-imapi2-istreampseudorandombased"><strong>IStreamPseudoRandomBased</strong></a></span><span class="sxs-lookup"><span data-stu-id="64a85-188"><a href="/windows/desktop/api/imapi2/nn-imapi2-istreampseudorandombased"><strong>IStreamPseudoRandomBased</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="64a85-189">MsftStreamPrgn001</span><span class="sxs-lookup"><span data-stu-id="64a85-189">MsftStreamPrgn001</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64a85-190">L'oggetto di scripting <strong>MsftStreamZero</strong> non è implementato come interfaccia.</span><span class="sxs-lookup"><span data-stu-id="64a85-190">The <strong>MsftStreamZero</strong> scripting object is not implemented as an interface.</span></span></td>
<td><span data-ttu-id="64a85-191"><a href="msftstreamzero.md"><strong>MsftStreamZero</strong></a></span><span class="sxs-lookup"><span data-stu-id="64a85-191"><a href="msftstreamzero.md"><strong>MsftStreamZero</strong></a></span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="64a85-192">Nella tabella seguente sono elencate le interfacce helper.</span><span class="sxs-lookup"><span data-stu-id="64a85-192">The following table lists helper interfaces.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="64a85-193">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="64a85-193">Interface</span></span></td>
<td><span data-ttu-id="64a85-194">Oggetto</span><span class="sxs-lookup"><span data-stu-id="64a85-194">Object</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64a85-195">Raccolta di intervalli di settore in un'immagine file system.</span><span class="sxs-lookup"><span data-stu-id="64a85-195">Collection of sector ranges within a file system image.</span></span>
<ul>
<li><span data-ttu-id="64a85-196"><a href="/windows/desktop/api/imapi2/nn-imapi2-iblockrange"><strong>IBlockRange</strong></a></span><span class="sxs-lookup"><span data-stu-id="64a85-196"><a href="/windows/desktop/api/imapi2/nn-imapi2-iblockrange"><strong>IBlockRange</strong></a></span></span></li>
<li><span data-ttu-id="64a85-197"><a href="/windows/desktop/api/imapi2/nn-imapi2-iblockrangelist"><strong>IBlockRangeList</strong></a></span><span class="sxs-lookup"><span data-stu-id="64a85-197"><a href="/windows/desktop/api/imapi2/nn-imapi2-iblockrangelist"><strong>IBlockRangeList</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="64a85-198">Nessun oggetto corrispondente</span><span class="sxs-lookup"><span data-stu-id="64a85-198">No corresponding object</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="64a85-199">Supporto per la verifica delle ustioni.</span><span class="sxs-lookup"><span data-stu-id="64a85-199">Burn verification support.</span></span>
<ul>
<li><span data-ttu-id="64a85-200"><a href="/windows/desktop/api/imapi2/nn-imapi2-iburnverification"><strong>IBurnVerification</strong></a></span><span class="sxs-lookup"><span data-stu-id="64a85-200"><a href="/windows/desktop/api/imapi2/nn-imapi2-iburnverification"><strong>IBurnVerification</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="64a85-201">Nessun oggetto corrispondente</span><span class="sxs-lookup"><span data-stu-id="64a85-201">No corresponding object</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64a85-202">Enumeratore di FsiItems per le applicazioni C/C++.</span><span class="sxs-lookup"><span data-stu-id="64a85-202">Enumerator of FsiItems for C/C++ applications.</span></span>
<ul>
<li><span data-ttu-id="64a85-203"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumfsiitems"><strong>IEnumFsiItems</strong></a></span><span class="sxs-lookup"><span data-stu-id="64a85-203"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumfsiitems"><strong>IEnumFsiItems</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="64a85-204">EnumFsiItems</span><span class="sxs-lookup"><span data-stu-id="64a85-204">EnumFsiItems</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="64a85-205">Enumeratore di ProgressItems per le applicazioni C/C++.</span><span class="sxs-lookup"><span data-stu-id="64a85-205">Enumerator of ProgressItems for C/C++ applications.</span></span>
<ul>
<li><span data-ttu-id="64a85-206"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumprogressitems"><strong>IEnumProgressItems</strong></a></span><span class="sxs-lookup"><span data-stu-id="64a85-206"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumprogressitems"><strong>IEnumProgressItems</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="64a85-207">EnumProgressItems</span><span class="sxs-lookup"><span data-stu-id="64a85-207">EnumProgressItems</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="64a85-208"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsinamedstreams"><strong>IFsiNamedStreams</strong></a></span><span class="sxs-lookup"><span data-stu-id="64a85-208"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsinamedstreams"><strong>IFsiNamedStreams</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="64a85-209">FsiFileItem2</span><span class="sxs-lookup"><span data-stu-id="64a85-209">FsiFileItem2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="64a85-210">. supporto della verifica immagini ISO.</span><span class="sxs-lookup"><span data-stu-id="64a85-210">.iso image verification support.</span></span>
<ul>
<li><span data-ttu-id="64a85-211"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iisoimagemanager"><strong>IIsoImageManager</strong></a></span><span class="sxs-lookup"><span data-stu-id="64a85-211"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iisoimagemanager"><strong>IIsoImageManager</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="64a85-212">Nessun oggetto corrispondente</span><span class="sxs-lookup"><span data-stu-id="64a85-212">No corresponding object</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64a85-213">Supporto di più sessioni.</span><span class="sxs-lookup"><span data-stu-id="64a85-213">Multiple session support.</span></span>
<ul>
<li><span data-ttu-id="64a85-214"><a href="/windows/desktop/api/imapi2/nn-imapi2-imultisession"><strong>IMultisession</strong></a></span><span class="sxs-lookup"><span data-stu-id="64a85-214"><a href="/windows/desktop/api/imapi2/nn-imapi2-imultisession"><strong>IMultisession</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="64a85-215">Nessun oggetto corrispondente</span><span class="sxs-lookup"><span data-stu-id="64a85-215">No corresponding object</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="64a85-216">Supporto sequenziale per più sessioni.</span><span class="sxs-lookup"><span data-stu-id="64a85-216">Sequential multiple session support.</span></span>
<ul>
<li><span data-ttu-id="64a85-217"><a href="/windows/desktop/api/imapi2/nn-imapi2-imultisessionsequential"><strong>IMultisessionSequential</strong></a></span><span class="sxs-lookup"><span data-stu-id="64a85-217"><a href="/windows/desktop/api/imapi2/nn-imapi2-imultisessionsequential"><strong>IMultisessionSequential</strong></a></span></span></li>
<li><span data-ttu-id="64a85-218"><a href="/windows/desktop/api/imapi2/nn-imapi2-imultisessionsequential2"><strong>IMultisessionSequential2</strong></a></span><span class="sxs-lookup"><span data-stu-id="64a85-218"><a href="/windows/desktop/api/imapi2/nn-imapi2-imultisessionsequential2"><strong>IMultisessionSequential2</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="64a85-219">MsftMultisessionSequential</span><span class="sxs-lookup"><span data-stu-id="64a85-219">MsftMultisessionSequential</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64a85-220">Nome file e blocchi associati nell'immagine dei risultati.</span><span class="sxs-lookup"><span data-stu-id="64a85-220">File name and associated blocks in the result image.</span></span>
<ul>
<li><span data-ttu-id="64a85-221"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitem"><strong>IProgressItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="64a85-221"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitem"><strong>IProgressItem</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="64a85-222">ProgressItem</span><span class="sxs-lookup"><span data-stu-id="64a85-222">ProgressItem</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="64a85-223">Elenco di immagini dei risultati, suddivise per nome file e blocchi associati.</span><span class="sxs-lookup"><span data-stu-id="64a85-223">Result image listing, broken down by file name and associated blocks.</span></span>
<ul>
<li><span data-ttu-id="64a85-224"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitems"><strong>IProgressItems</strong></a></span><span class="sxs-lookup"><span data-stu-id="64a85-224"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitems"><strong>IProgressItems</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="64a85-225">ProgressItems</span><span class="sxs-lookup"><span data-stu-id="64a85-225">ProgressItems</span></span></td>
</tr>
</tbody>
</table>



 

 

 




