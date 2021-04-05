---
title: Installazione del gestore di file e flussi
description: Installazione del gestore di file e flussi
ms.assetid: 8d007ea4-b75a-4b3f-965f-8091fcd4cb2f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be94137df69ed35b57b1b8fbeb5c9640dd7636d6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713597"
---
# <a name="file-and-stream-handler-installation"></a><span data-ttu-id="67e67-103">Installazione del gestore di file e flussi</span><span class="sxs-lookup"><span data-stu-id="67e67-103">File and Stream Handler Installation</span></span>

<span data-ttu-id="67e67-104">La libreria AVIFile usa i gestori di flussi e file installati per la lettura e la scrittura di file e flussi AVI.</span><span class="sxs-lookup"><span data-stu-id="67e67-104">The AVIFile library uses installed stream and file handlers for reading and writing AVI files and streams.</span></span> <span data-ttu-id="67e67-105">Un gestore viene installato quando risiede nella directory di sistema di Windows e il registro di sistema contiene le informazioni seguenti necessarie per descrivere e identificare un gestore:</span><span class="sxs-lookup"><span data-stu-id="67e67-105">A handler is installed when it resides in the Windows SYSTEM directory and the registry contains the following information needed to describe and identify a handler:</span></span>

-   <span data-ttu-id="67e67-106">Identificatore di classe a 16 byte per il gestore</span><span class="sxs-lookup"><span data-stu-id="67e67-106">The 16-byte class identifier for the handler</span></span>
-   <span data-ttu-id="67e67-107">Breve descrizione del gestore</span><span class="sxs-lookup"><span data-stu-id="67e67-107">A brief description of the handler</span></span>
-   <span data-ttu-id="67e67-108">Nome del file che contiene il gestore</span><span class="sxs-lookup"><span data-stu-id="67e67-108">The name of the file containing the handler</span></span>
-   <span data-ttu-id="67e67-109">Estensione di file che un gestore di file può elaborare</span><span class="sxs-lookup"><span data-stu-id="67e67-109">The file extension that a file handler can process</span></span>
-   <span data-ttu-id="67e67-110">Accesso ai file e altre proprietà associate a un gestore di file</span><span class="sxs-lookup"><span data-stu-id="67e67-110">File-access and other properties associated with a file handler</span></span>
-   <span data-ttu-id="67e67-111">Codici di quattro caratteri che identificano i tipi di flusso che possono essere elaborati da un gestore di flusso</span><span class="sxs-lookup"><span data-stu-id="67e67-111">Four-character codes identifying stream types that a stream handler can process</span></span>

<span data-ttu-id="67e67-112">La libreria AVIFile esegue una query nel registro di sistema per i gestori esterni a un'applicazione durante l'apertura di file e l'accesso ai flussi.</span><span class="sxs-lookup"><span data-stu-id="67e67-112">The AVIFile library queries the registry for handlers that are external to an application when opening files and accessing streams.</span></span> <span data-ttu-id="67e67-113">Il risultato di una query eseguita correttamente restituisce il nome file di un gestore in grado di elaborare il tipo di file o di flusso specificato nella query.</span><span class="sxs-lookup"><span data-stu-id="67e67-113">The result of a successful query returns the filename of a handler that can process the file or stream type specified in the query.</span></span> <span data-ttu-id="67e67-114">Il registro di sistema elenca ogni gestore creando tre voci il cui formato è il seguente:</span><span class="sxs-lookup"><span data-stu-id="67e67-114">The registry lists each handler by creating three entries that have the following form:</span></span>


```C++
[HKEY_CLASSES_ROOT\Clsid\{00010023-0000-0000-C000-000000000046}] 
@="Wave File reader/writer" 
[HKEY_CLASSES_ROOT\Clsid\{00010023-0000-0000-C000- 
000000000046}\InprocServer32] 
@="wavefile.dll" 
"ThreadingModel"="Apartment" 
[HKEY_CLASSES_ROOT\Clsid\{00010023-0000-0000-C000- 
000000000046}\AVIFile] 
@="3" 
 
```



<span data-ttu-id="67e67-115">Queste voci sono costituite dalle parti seguenti.</span><span class="sxs-lookup"><span data-stu-id="67e67-115">These entries consist of the following parts.</span></span>



| <span data-ttu-id="67e67-116">Parte</span><span class="sxs-lookup"><span data-stu-id="67e67-116">Part</span></span>                                   | <span data-ttu-id="67e67-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="67e67-117">Description</span></span>                                                                                                                                                                              |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67e67-118">HKEY\_CLASSI\_RADICE</span><span class="sxs-lookup"><span data-stu-id="67e67-118">HKEY\_CLASSES\_ROOT</span></span>                    | <span data-ttu-id="67e67-119">Identifica la voce radice del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="67e67-119">Identifies the root entry of the registry.</span></span>                                                                                                                                               |
| <span data-ttu-id="67e67-120">CLSID</span><span class="sxs-lookup"><span data-stu-id="67e67-120">Clsid</span></span>                                  | <span data-ttu-id="67e67-121">Identifica questa voce come identificatore di classe.</span><span class="sxs-lookup"><span data-stu-id="67e67-121">Identifies this entry as a class identifier.</span></span>                                                                                                                                             |
| <span data-ttu-id="67e67-122">{00010023-0000-0000-C000-000000000046}</span><span class="sxs-lookup"><span data-stu-id="67e67-122">{00010023-0000-0000-C000-000000000046}</span></span> | <span data-ttu-id="67e67-123">Specifica un identificatore di interfaccia (IID) o un identificatore di classe.</span><span class="sxs-lookup"><span data-stu-id="67e67-123">Specifies an interface identifier (IID) or class identifier.</span></span> <span data-ttu-id="67e67-124">Questo valore è un identificatore univoco a 16 byte.</span><span class="sxs-lookup"><span data-stu-id="67e67-124">This value is a unique 16-byte identifier.</span></span> <span data-ttu-id="67e67-125">L'identificatore può anche essere definito GUID o UUID in altri manuali.</span><span class="sxs-lookup"><span data-stu-id="67e67-125">(The identifier might also be referred to as a GUID or a UUID in other manuals.)</span></span> |
| <span data-ttu-id="67e67-126">Lettura/scrittura file Wave</span><span class="sxs-lookup"><span data-stu-id="67e67-126">Wave File reader/writer</span></span>                | <span data-ttu-id="67e67-127">Specifica una stringa per descrivere il gestore.</span><span class="sxs-lookup"><span data-stu-id="67e67-127">Specifies a string to describe the handler.</span></span> <span data-ttu-id="67e67-128">Questa stringa può essere visualizzata nelle finestre di dialogo per la selezione di gestori di file e flussi.</span><span class="sxs-lookup"><span data-stu-id="67e67-128">This string can be displayed in dialog boxes for selecting stream and file handlers.</span></span>                                                         |
| <span data-ttu-id="67e67-129">InProcServer32</span><span class="sxs-lookup"><span data-stu-id="67e67-129">InProcServer32</span></span>                         | <span data-ttu-id="67e67-130">Specifica il file (in questo esempio WAVEFILE.DLL) che può essere caricato per gestire questa classe.</span><span class="sxs-lookup"><span data-stu-id="67e67-130">Specifies the file (in this example, WAVEFILE.DLL) that can be loaded to handle this class.</span></span>                                                                                              |
| <span data-ttu-id="67e67-131">AVIFile</span><span class="sxs-lookup"><span data-stu-id="67e67-131">AVIFile</span></span>                                | <span data-ttu-id="67e67-132">Specifica le proprietà di un gestore di file.</span><span class="sxs-lookup"><span data-stu-id="67e67-132">Specifies the properties of a file handler.</span></span> <span data-ttu-id="67e67-133">In questo esempio, il gestore può leggere e scrivere in un file AVI.</span><span class="sxs-lookup"><span data-stu-id="67e67-133">In this example, the handler can read and write to an AVI file.</span></span>                                                                              |



 

<span data-ttu-id="67e67-134">Un gestore di file può avere una o più proprietà archiviate nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="67e67-134">A file handler can have one or more of its properties stored in the registry.</span></span> <span data-ttu-id="67e67-135">Le costanti seguenti identificano le proprietà attualmente associate a un file.</span><span class="sxs-lookup"><span data-stu-id="67e67-135">The following constants identify the properties currently associated with a file.</span></span>



| <span data-ttu-id="67e67-136">Costante</span><span class="sxs-lookup"><span data-stu-id="67e67-136">Constant</span></span>                        | <span data-ttu-id="67e67-137">Descrizione</span><span class="sxs-lookup"><span data-stu-id="67e67-137">Description</span></span>                                                          |
|---------------------------------|----------------------------------------------------------------------|
| <span data-ttu-id="67e67-138">\_CANACCEPTNONRGB AVIFILEHANDLER</span><span class="sxs-lookup"><span data-stu-id="67e67-138">AVIFILEHANDLER\_CANACCEPTNONRGB</span></span> | <span data-ttu-id="67e67-139">Indica che un gestore di file può elaborare dati di immagini diversi da RGB.</span><span class="sxs-lookup"><span data-stu-id="67e67-139">Indicates that a file handler can process image data other than RGB.</span></span> |
| <span data-ttu-id="67e67-140">AVIFILEHANDLER \_ CANREAD</span><span class="sxs-lookup"><span data-stu-id="67e67-140">AVIFILEHANDLER\_CANREAD</span></span>         | <span data-ttu-id="67e67-141">Indica che un gestore di file può aprire un file con accesso in lettura.</span><span class="sxs-lookup"><span data-stu-id="67e67-141">Indicates that a file handler can open a file with read access.</span></span>      |
| <span data-ttu-id="67e67-142">\_CANWRITE AVIFILEHANDLER</span><span class="sxs-lookup"><span data-stu-id="67e67-142">AVIFILEHANDLER\_CANWRITE</span></span>        | <span data-ttu-id="67e67-143">Indica che un gestore di file può aprire un file con accesso in scrittura.</span><span class="sxs-lookup"><span data-stu-id="67e67-143">Indicates that a file handler can open a file with write access.</span></span>     |



 

<span data-ttu-id="67e67-144">Quando si crea un gestore di file o flussi, è possibile ottenere un nuovo identificatore eseguendo UUIDGEN.EXE.</span><span class="sxs-lookup"><span data-stu-id="67e67-144">When creating a file or stream handler, you can obtain a new identifier by running UUIDGEN.EXE.</span></span> <span data-ttu-id="67e67-145">Usare sempre UUIDGEN.EXE per creare un nuovo identificatore.</span><span class="sxs-lookup"><span data-stu-id="67e67-145">Always use UUIDGEN.EXE to create a new identifier.</span></span> <span data-ttu-id="67e67-146">Il numero esadecimale a 16 byte creato da questo eseguibile identificherà in modo univoco il gestore.</span><span class="sxs-lookup"><span data-stu-id="67e67-146">The 16-byte hexadecimal number created by this executable will uniquely identify your handler.</span></span>

<span data-ttu-id="67e67-147">La libreria AVIFile usa voci aggiuntive nel registro di sistema per identificare un identificatore di classe basato sull'estensione di file che un gestore di file può elaborare o su un codice di quattro caratteri che un gestore di file o flussi può elaborare.</span><span class="sxs-lookup"><span data-stu-id="67e67-147">The AVIFile library uses additional entries in the registry to identify a class identifier based on the file extension that a file handler can process or a four-character code that a file or stream handler can process.</span></span> <span data-ttu-id="67e67-148">Ad esempio, le voci seguenti associano un identificatore di classe all'estensione di file. WAV e il codice a quattro caratteri "WAVE":</span><span class="sxs-lookup"><span data-stu-id="67e67-148">For example, the following entries associate a class identifier with the file extension .WAV and the four-character code "WAVE":</span></span>


```C++
[HKEY_CLASSES_ROOT\AVIFile\Extensions\WAV] 
@="{00010023-0000-0000-C000-000000000046}" 
[HKEY_CLASSES_ROOT\AVIFile\RIFFHandlers\WAVE] 
@="{00010023-0000-0000-C000-000000000046}" 
 
```



<span data-ttu-id="67e67-149">Queste voci sono costituite dalle parti seguenti.</span><span class="sxs-lookup"><span data-stu-id="67e67-149">These entries consist of the following parts.</span></span>



| <span data-ttu-id="67e67-150">Parte</span><span class="sxs-lookup"><span data-stu-id="67e67-150">Part</span></span>                                   | <span data-ttu-id="67e67-151">Descrizione</span><span class="sxs-lookup"><span data-stu-id="67e67-151">Description</span></span>                                                                                       |
|----------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67e67-152">HKEY\_CLASSI\_RADICE</span><span class="sxs-lookup"><span data-stu-id="67e67-152">HKEY\_CLASSES\_ROOT</span></span>                    | <span data-ttu-id="67e67-153">Identifica la voce radice del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="67e67-153">Identifies the root entry of the registry.</span></span>                                                        |
| <span data-ttu-id="67e67-154">AVIFile</span><span class="sxs-lookup"><span data-stu-id="67e67-154">AVIFile</span></span>                                | <span data-ttu-id="67e67-155">Identifica questa voce come una voce utilizzata da AVIFile.</span><span class="sxs-lookup"><span data-stu-id="67e67-155">Identifies this entry as an entry used by AVIFile.</span></span>                                                |
| <span data-ttu-id="67e67-156">Estensioni</span><span class="sxs-lookup"><span data-stu-id="67e67-156">Extensions</span></span>                             | <span data-ttu-id="67e67-157">Specifica l'estensione di file (in questo esempio,. WAV) che un gestore di file può elaborare.</span><span class="sxs-lookup"><span data-stu-id="67e67-157">Specifies the file extension (in this example, .WAV) that a file handler can process.</span></span>             |
| <span data-ttu-id="67e67-158">RIFFHandlers</span><span class="sxs-lookup"><span data-stu-id="67e67-158">RIFFHandlers</span></span>                           | <span data-ttu-id="67e67-159">Specifica il codice di quattro caratteri, in questo esempio "WAVE", che può essere elaborato da un gestore di file o flussi.</span><span class="sxs-lookup"><span data-stu-id="67e67-159">Specifies the four-character code (in this example, "WAVE") a file or stream handler can process.</span></span> |
| <span data-ttu-id="67e67-160">{00010023-0000-0000-C000-000000000046}</span><span class="sxs-lookup"><span data-stu-id="67e67-160">{00010023-0000-0000-C000-000000000046}</span></span> | <span data-ttu-id="67e67-161">Specifica un identificatore di interfaccia (IID) o un identificatore di classe.</span><span class="sxs-lookup"><span data-stu-id="67e67-161">Specifies an interface identifier (IID) or class identifier.</span></span>                                      |



 

<span data-ttu-id="67e67-162">Se si distribuisce il gestore di flussi o file senza un'applicazione di installazione per installarlo nel sistema dell'utente, è necessario includere un. REG file in modo che l'utente possa installare il gestore.</span><span class="sxs-lookup"><span data-stu-id="67e67-162">If you distribute your stream or file handler without a setup application to install it in the user's system, you must include a .REG file so the user can install the handler.</span></span> <span data-ttu-id="67e67-163">L'utente userà l'editor del registro di sistema per creare le voci del registro di sistema per il gestore di file o di flusso.</span><span class="sxs-lookup"><span data-stu-id="67e67-163">The user will use the registry editor to create registry entries for your stream or file handler.</span></span>

<span data-ttu-id="67e67-164">Nell'esempio seguente viene illustrato il contenuto di un oggetto tipico. File REG.</span><span class="sxs-lookup"><span data-stu-id="67e67-164">The following example shows the contents of a typical .REG file.</span></span> <span data-ttu-id="67e67-165">La prima voce nell'esempio seguente è la stringa descrittiva per il gestore.</span><span class="sxs-lookup"><span data-stu-id="67e67-165">The first entry in the following example is the descriptive string for the handler.</span></span> <span data-ttu-id="67e67-166">La seconda voce identifica il file contenente il gestore.</span><span class="sxs-lookup"><span data-stu-id="67e67-166">The second entry identifies the file containing the handler.</span></span> <span data-ttu-id="67e67-167">La terza voce identifica le proprietà del gestore di file, in questo caso l'accesso in sola lettura ai file.</span><span class="sxs-lookup"><span data-stu-id="67e67-167">The third entry identifies the properties of the file handler (in this case, read-only access to files).</span></span> <span data-ttu-id="67e67-168">La quarta voce associa il tipo di file elaborato dal gestore, in questo caso i file con un. Estensione del nome file JPG) con l'identificatore di classe.</span><span class="sxs-lookup"><span data-stu-id="67e67-168">The fourth entry associates the type of file the handler processes (in this case, files with a .JPG filename extension) with the class identifier.</span></span>


```C++
[HKEY_CLASSES_ROOT\Clsid\{5C2B8200-E2C8-1068-B1CA-6066188C6002}] 
@="JFIF (JPEG) Files" 
[HKEY_CLASSES_ROOT\Clsid\{5C2B8200-E2C8-1068-B1CA-6066188C6002}]\InprocServer32] 
@="jfiffile.dll" 
[HKEY_CLASSES_ROOT\AVIFile\Extensions\JPG] 
@="{5C2B8200-E2C8-1068-B1CA-6066188C6002}" 
 
```



<span data-ttu-id="67e67-169">Quando si crea questo file, salvarlo con un. REG Extension per identificarlo come file di aggiornamento per il registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="67e67-169">When creating this file, save it with a .REG extension to identify it as an update file for the registry.</span></span> <span data-ttu-id="67e67-170">Sostituire anche un IID univoco per il codice a 16 byte usato nell'esempio.</span><span class="sxs-lookup"><span data-stu-id="67e67-170">Also, substitute a unique IID for the 16-byte code used in the example.</span></span>

 

 




