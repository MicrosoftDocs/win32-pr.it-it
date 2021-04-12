---
title: Masterizzazione di un'immagine del disco
description: La creazione di un disco con IMAPi è costituita dai passaggi seguenti per creare un'immagine di file system contenente le directory e i file per la scrittura del disco. Configurare un registratore di dischi per comunicare con il dispositivo ottico. Creare un writer di dati e masterizzare l'immagine su disco.
ms.assetid: f2eee14e-695d-4678-b3c1-b521ab4d4a7e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6e3086f728ca0b0826a001d26841edcfe07c6a1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337191"
---
# <a name="burning-a-disc-image"></a><span data-ttu-id="6d4c2-103">Masterizzazione di un'immagine del disco</span><span class="sxs-lookup"><span data-stu-id="6d4c2-103">Burning a Disc Image</span></span>

<span data-ttu-id="6d4c2-104">La Master (Burning a Disk) con IMAPi prevede i passaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="6d4c2-104">Mastering (burning a disc) using IMAPI consists of the following steps:</span></span>

1.  <span data-ttu-id="6d4c2-105">Costruire un'immagine di file system contenente le directory e i file da scrivere nel disco.</span><span class="sxs-lookup"><span data-stu-id="6d4c2-105">Construct a file system image that contains the directories and files to write disc.</span></span>
2.  <span data-ttu-id="6d4c2-106">[Configurare un registratore di dischi](#set-up-a-disc-recorder) per comunicare con il dispositivo ottico.</span><span class="sxs-lookup"><span data-stu-id="6d4c2-106">[Set up a disc recorder](#set-up-a-disc-recorder) to communicate with the optical device.</span></span>
3.  <span data-ttu-id="6d4c2-107">[Creare un writer di dati](#create-a-data-writer-and-write-the-burn-image) e masterizzare l'immagine su disco.</span><span class="sxs-lookup"><span data-stu-id="6d4c2-107">[Create a data writer](#create-a-data-writer-and-write-the-burn-image) and burn the image to disc.</span></span>

<span data-ttu-id="6d4c2-108">Per un esempio in cui viene bruciata un'immagine del disco, vedere l' [esempio VBScript](#vbscript-example).</span><span class="sxs-lookup"><span data-stu-id="6d4c2-108">For an example that burns a disc image, see [VBScript example](#vbscript-example).</span></span>

## <a name="construct-a-burn-image"></a><span data-ttu-id="6d4c2-109">Costruire un'immagine di masterizzazione</span><span class="sxs-lookup"><span data-stu-id="6d4c2-109">Construct a burn image</span></span>

<span data-ttu-id="6d4c2-110">Un'immagine Burn è un flusso di dati pronto per essere scritto su supporti ottici.</span><span class="sxs-lookup"><span data-stu-id="6d4c2-110">A burn image is a data stream that is ready to be written to optical media.</span></span> <span data-ttu-id="6d4c2-111">L'immagine Burn per i formati ISO9660, Joliet e UDF è costituita da una file system di singoli file e directory.</span><span class="sxs-lookup"><span data-stu-id="6d4c2-111">The burn image for ISO9660, Joliet and UDF formats consists of a file system of individual files and directories.</span></span> <span data-ttu-id="6d4c2-112">L'oggetto **CFileSystemImage** è l'oggetto file System che include i file e le directory da collocare sul supporto ottico.</span><span class="sxs-lookup"><span data-stu-id="6d4c2-112">The **CFileSystemImage** object is the file system object that holds the files and directories to place on the optical media.</span></span> <span data-ttu-id="6d4c2-113">L'interfaccia [**IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) fornisce l'accesso all'oggetto file System e alle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="6d4c2-113">The [**IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) interface provides access to the file system object and settings.</span></span>

<span data-ttu-id="6d4c2-114">Dopo aver creato l'oggetto file system, chiamare i metodi [**IFileSystemImage:: CreateFileItem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createfileitem) e [**IFileSystemImage:: CreateDirectoryItem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createdirectoryitem) per creare rispettivamente gli oggetti file e directory.</span><span class="sxs-lookup"><span data-stu-id="6d4c2-114">After creating the file system object, call the [**IFileSystemImage::CreateFileItem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createfileitem) and [**IFileSystemImage::CreateDirectoryItem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createdirectoryitem) methods to create the file and directory objects, respectively.</span></span> <span data-ttu-id="6d4c2-115">È possibile utilizzare gli oggetti file e directory per fornire dettagli specifici sul file e sulla directory.</span><span class="sxs-lookup"><span data-stu-id="6d4c2-115">The file and directory objects can be used to provide specific details about the file and directory.</span></span> <span data-ttu-id="6d4c2-116">I metodi del gestore eventi disponibili per [**IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) possono identificare il file corrente da aggiungere all'immagine file System, il numero di settori già copiati e il numero totale di settori da copiare.</span><span class="sxs-lookup"><span data-stu-id="6d4c2-116">The event handler methods available for [**IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) can identify the current file being added to the file system image, the number of sectors already copied, and the total number of sectors to be copied.</span></span>

<span data-ttu-id="6d4c2-117">Facoltativamente, un'immagine di avvio può essere collegata al file system usando la proprietà [**IFileSystemImage::p UT \_ BootImageOptions**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_bootimageoptions) .</span><span class="sxs-lookup"><span data-stu-id="6d4c2-117">Optionally, a boot image can be attached to the file system using the [**IFileSystemImage::put\_BootImageOptions**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_bootimageoptions) property.</span></span> <span data-ttu-id="6d4c2-118">Per un esempio, vedere [aggiunta di un'immagine di avvio](adding-a-boot-image.md).</span><span class="sxs-lookup"><span data-stu-id="6d4c2-118">For an example, see [Adding a Boot Image](adding-a-boot-image.md).</span></span>

<span data-ttu-id="6d4c2-119">Infine, chiamare [**IFileSystemImage:: CreateResultImage**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createresultimage) per creare un flusso di dati e fornire l'accesso tramite [**IFileSystemImageResult**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimageresult).</span><span class="sxs-lookup"><span data-stu-id="6d4c2-119">Finally, call [**IFileSystemImage::CreateResultImage**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createresultimage) to create a data stream and provides access through [**IFileSystemImageResult**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimageresult).</span></span> <span data-ttu-id="6d4c2-120">Il nuovo flusso di dati può quindi essere fornito direttamente al metodo [**IDiscFormat2Data:: Write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) oppure essere salvato in un file per un uso successivo.</span><span class="sxs-lookup"><span data-stu-id="6d4c2-120">The new data stream can then be provided directly to the [**IDiscFormat2Data::Write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) method or be saved to a file for later use.</span></span>

## <a name="set-up-a-disc-recorder"></a><span data-ttu-id="6d4c2-121">Configurare un registratore di dischi</span><span class="sxs-lookup"><span data-stu-id="6d4c2-121">Set up a disc recorder</span></span>

<span data-ttu-id="6d4c2-122">L'oggetto **MsftDiscMaster2** fornisce un'enumerazione dei dispositivi ottici nel sistema.</span><span class="sxs-lookup"><span data-stu-id="6d4c2-122">The **MsftDiscMaster2** object provides an enumeration of the optical devices on the system.</span></span> <span data-ttu-id="6d4c2-123">L'interfaccia [**IDiscMaster2**](/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2) fornisce l'accesso all'enumerazione dei dispositivi risultante.</span><span class="sxs-lookup"><span data-stu-id="6d4c2-123">The [**IDiscMaster2**](/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2) interface provides access to the resultant device enumeration.</span></span> <span data-ttu-id="6d4c2-124">Attraversare le enumerazioni per individuare un dispositivo di registrazione appropriato.</span><span class="sxs-lookup"><span data-stu-id="6d4c2-124">Traverse the enumerations to locate an appropriate recording device.</span></span> <span data-ttu-id="6d4c2-125">L'oggetto **MsftDiscMaster2** fornisce anche le notifiche degli eventi quando i dispositivi ottici vengono aggiunti o eliminati da un computer.</span><span class="sxs-lookup"><span data-stu-id="6d4c2-125">The **MsftDiscMaster2** object also provides event notifications when optical devices are added to or deleted from a computer.</span></span>

<span data-ttu-id="6d4c2-126">Dopo aver individuato un registratore ottico e aver recuperato il relativo ID, creare un oggetto **MsftDiscRecorder2** e inizializzare il registratore usando l'ID del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6d4c2-126">After finding an optical recorder and retrieving its ID, create an **MsftDiscRecorder2** object and initialize the recorder using the device ID.</span></span> <span data-ttu-id="6d4c2-127">L'interfaccia [**IDiscRecorder2**](/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2) fornisce l'accesso all'oggetto registratore, oltre ad alcune informazioni di base sul dispositivo, ad esempio ID fornitore, ID prodotto, revisione del prodotto e metodi per estrarre il supporto e chiudere la barra.</span><span class="sxs-lookup"><span data-stu-id="6d4c2-127">The [**IDiscRecorder2**](/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2) interface provides access to the recorder object as well as some basic device information such as vendor ID, product ID, product revision, and methods to eject the media and close the tray.</span></span>

## <a name="create-a-data-writer-and-write-the-burn-image"></a><span data-ttu-id="6d4c2-128">Creare un writer di dati e scrivere l'immagine di masterizzazione</span><span class="sxs-lookup"><span data-stu-id="6d4c2-128">Create a data writer and write the burn image</span></span>

<span data-ttu-id="6d4c2-129">L'oggetto **MsftDiscFormat2Data** fornisce il metodo di scrittura, le proprietà relative alla funzione Write e alle proprietà specifiche del supporto.</span><span class="sxs-lookup"><span data-stu-id="6d4c2-129">The **MsftDiscFormat2Data** object provides the writing method, the properties about the write function and media-specific properties.</span></span> <span data-ttu-id="6d4c2-130">L'interfaccia [**IDiscFormat2Data**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data) fornisce l'accesso all'oggetto **MsftDiscFormat2Data** .</span><span class="sxs-lookup"><span data-stu-id="6d4c2-130">The [**IDiscFormat2Data**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data) interface provides access to the **MsftDiscFormat2Data** object.</span></span>

<span data-ttu-id="6d4c2-131">La registrazione del disco è collegata al writer del formato usando la proprietà [**IDiscFormat2Data::p UT \_ Recorder**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-put_recorder) .</span><span class="sxs-lookup"><span data-stu-id="6d4c2-131">The disc recorder links to the format writer using the [**IDiscFormat2Data::put\_Recorder**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-put_recorder) property.</span></span> <span data-ttu-id="6d4c2-132">Dopo che il registratore è stato associato al writer di formato, è possibile eseguire query relative ai supporti e aggiornare le proprietà specifiche della scrittura prima di scrivere l'immagine del risultato in un disco usando il metodo [**IDiscFormat2Data:: Write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) .</span><span class="sxs-lookup"><span data-stu-id="6d4c2-132">After the recorder is bound to the format writer, you can perform queries regarding the media and update write-specific properties before writing the result image to disc using the [**IDiscFormat2Data::Write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) method.</span></span>

<span data-ttu-id="6d4c2-133">Altre interfacce di scrittura del formato fornite da IMAPi funzionano in modo analogo; le interfacce aggiuntive per la scrittura di formati includono:</span><span class="sxs-lookup"><span data-stu-id="6d4c2-133">Other format writing interfaces provided by IMAPI work similarly; additional format writing interfaces include:</span></span>

-   <span data-ttu-id="6d4c2-134">[**IDiscFormat2Erase**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase) Cancella i supporti ottici riscrivibili.</span><span class="sxs-lookup"><span data-stu-id="6d4c2-134">[**IDiscFormat2Erase**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase) erases rewritable optical media.</span></span>
-   <span data-ttu-id="6d4c2-135">[**IDiscFormat2RawCD**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd) scrive un'immagine non elaborata in un supporto ottico.</span><span class="sxs-lookup"><span data-stu-id="6d4c2-135">[**IDiscFormat2RawCD**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd) writes a raw image to optical media.</span></span>
-   <span data-ttu-id="6d4c2-136">[**IDiscFormat2TrackAtOnce**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonce) scrive tracce audio su supporti ottici.</span><span class="sxs-lookup"><span data-stu-id="6d4c2-136">[**IDiscFormat2TrackAtOnce**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonce) writes audio tracks to optical media.</span></span>

> [!Note]  
> <span data-ttu-id="6d4c2-137">È possibile che si verifichi una transizione di stato dell'alimentazione durante un'operazione di masterizzazione, ad esempio la disconnessione dell'utente o la sospensione del sistema, che comporta l'interruzione del processo di masterizzazione e la possibile perdita di dati.</span><span class="sxs-lookup"><span data-stu-id="6d4c2-137">It is possible for a power state transition to take place during a burn operation (i.e. user log-off or system suspend) which leads to the interruption of the burn process and possible data loss.</span></span> <span data-ttu-id="6d4c2-138">Per considerazioni sulla programmazione, vedere [Impedisci la disconnessione o la sospensione durante un'ustione](preventing-logoff-or-suspend-during-a-burn.md).</span><span class="sxs-lookup"><span data-stu-id="6d4c2-138">For programming considerations, see [Preventing Logoff or Suspend During a Burn](preventing-logoff-or-suspend-during-a-burn.md).</span></span>

 

## <a name="vbscript-example"></a><span data-ttu-id="6d4c2-139">Esempio di VBScript</span><span class="sxs-lookup"><span data-stu-id="6d4c2-139">VBScript example</span></span>

<span data-ttu-id="6d4c2-140">Questo esempio di script Mostra come usare gli oggetti IMAPi per masterizzare supporti ottici; in particolare, scrivere una directory in un disco vuoto. Il codice non contiene alcun controllo degli errori e presuppone quanto segue:</span><span class="sxs-lookup"><span data-stu-id="6d4c2-140">This script example shows how to use the IMAPI objects to burn optical media; more specifically, write a directory to a blank disc. The code contains no error checking, and assumes the following:</span></span>

-   <span data-ttu-id="6d4c2-141">Nel sistema è installato un dispositivo disco compatibile.</span><span class="sxs-lookup"><span data-stu-id="6d4c2-141">A compatible disc device is installed on the system.</span></span>
-   <span data-ttu-id="6d4c2-142">Il dispositivo disco è la seconda unità del sistema.</span><span class="sxs-lookup"><span data-stu-id="6d4c2-142">The disc device is the second drive on the system.</span></span>
-   <span data-ttu-id="6d4c2-143">Viene inserito un disco compatibile nel dispositivo disco.</span><span class="sxs-lookup"><span data-stu-id="6d4c2-143">A compatible disc is inserted in the disc device.</span></span>
-   <span data-ttu-id="6d4c2-144">Il disco è vuoto.</span><span class="sxs-lookup"><span data-stu-id="6d4c2-144">The disc is blank.</span></span>
-   <span data-ttu-id="6d4c2-145">I file da scrivere sul disco si trovano in "g: \\ burndir".</span><span class="sxs-lookup"><span data-stu-id="6d4c2-145">Files to write to disc are located in "g:\\burndir".</span></span>

<span data-ttu-id="6d4c2-146">A questo script è possibile aggiungere funzionalità aggiuntive, ad esempio il controllo degli errori, la compatibilità di dispositivi e supporti, la notifica degli eventi e il calcolo dello spazio disponibile sul disco.</span><span class="sxs-lookup"><span data-stu-id="6d4c2-146">Additional functionality such as error checking, device and media compatibility, event notification, and calculating free space on the disc can be added to this script.</span></span>


```VB
' This script burns data files to disc in a single session 
' using files from a single directory tree.
 
' Copyright (C) Microsoft Corp. 2006

Option Explicit

' *** CD/DVD disc file system types
Const FsiFileSystemISO9660 = 1
Const FsiFileSystemJoliet  = 2
Const FsiFileSystemUDF102  = 4

WScript.Quit(Main)

Function Main
    Dim Index                ' Index to recording drive.
    Dim Recorder             ' Recorder object
    Dim Path                 ' Directory of files to burn
    Dim Stream               ' Data stream for burning device
    
    Index = 1                ' Second drive on the system
    Path = "g:\BurnDir"      ' Files to transfer to disc

    ' Create a DiscMaster2 object to connect to optical drives.
    Dim g_DiscMaster
    Set g_DiscMaster = WScript.CreateObject("IMAPI2.MsftDiscMaster2")

    ' Create a DiscRecorder object for the specified burning device.
    Dim uniqueId
    set recorder = WScript.CreateObject("IMAPI2.MsftDiscRecorder2")
    uniqueId = g_DiscMaster.Item(index)
    recorder.InitializeDiscRecorder( uniqueId )

    ' Create an image stream for a specified directory.
    Dim FSI                  ' Disc file system
    Dim Dir                  ' Root directory of the disc file system
    Dim dataWriter    
        
    ' Create a new file system image and retrieve root directory
    Set FSI = CreateObject("IMAPI2FS.MsftFileSystemImage")
    Set Dir = FSI.Root

    'Create the new disc format and set the recorder
    Set dataWriter = CreateObject ("IMAPI2.MsftDiscFormat2Data")
    dataWriter.recorder = Recorder
    dataWriter.ClientName = "IMAPIv2 TEST"

    FSI.ChooseImageDefaults(recorder)
        
    ' Add the directory and its contents to the file system 
    Dir.AddTree Path, false
        
    ' Create an image from the file system
    Dim result
    Set result = FSI.CreateResultImage()
    Stream = result.ImageStream
    
    ' Write stream to disc using the specified recorder.
    WScript.Echo "Writing content to disc..."
    dataWriter.write(Stream)

    WScript.Echo "----- Finished writing content -----"
    Main = 0
End Function

```



## <a name="related-topics"></a><span data-ttu-id="6d4c2-147">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6d4c2-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d4c2-148">Uso di IMAPi</span><span class="sxs-lookup"><span data-stu-id="6d4c2-148">Using IMAPI</span></span>](using-imapi.md)
</dt> <dt>

[<span data-ttu-id="6d4c2-149">**IDiscFormat2Data**</span><span class="sxs-lookup"><span data-stu-id="6d4c2-149">**IDiscFormat2Data**</span></span>](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data)
</dt> <dt>

[<span data-ttu-id="6d4c2-150">**IDiscFormat2Erase**</span><span class="sxs-lookup"><span data-stu-id="6d4c2-150">**IDiscFormat2Erase**</span></span>](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase)
</dt> <dt>

[<span data-ttu-id="6d4c2-151">**IDiscFormat2RawCD**</span><span class="sxs-lookup"><span data-stu-id="6d4c2-151">**IDiscFormat2RawCD**</span></span>](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd)
</dt> <dt>

[<span data-ttu-id="6d4c2-152">**IDiscFormat2TrackAtOnce**</span><span class="sxs-lookup"><span data-stu-id="6d4c2-152">**IDiscFormat2TrackAtOnce**</span></span>](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonce)
</dt> <dt>

[<span data-ttu-id="6d4c2-153">**IDiscMaster2**</span><span class="sxs-lookup"><span data-stu-id="6d4c2-153">**IDiscMaster2**</span></span>](/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2)
</dt> <dt>

[<span data-ttu-id="6d4c2-154">**IDiscRecorder2**</span><span class="sxs-lookup"><span data-stu-id="6d4c2-154">**IDiscRecorder2**</span></span>](/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2)
</dt> <dt>

[<span data-ttu-id="6d4c2-155">**IFileSystemImage**</span><span class="sxs-lookup"><span data-stu-id="6d4c2-155">**IFileSystemImage**</span></span>](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage)
</dt> <dt>

[<span data-ttu-id="6d4c2-156">**IStream**</span><span class="sxs-lookup"><span data-stu-id="6d4c2-156">**IStream**</span></span>](/windows/desktop/api/objidl/nn-objidl-istream)
</dt> </dl>

 

 