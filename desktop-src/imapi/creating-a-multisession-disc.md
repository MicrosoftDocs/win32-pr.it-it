---
title: Creazione di un disco multisessione
ms.assetid: 327304c4-fdb9-47c6-9b19-49100b933590
description: 'Altre informazioni su: creazione di un disco a più sessioni'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2db17b8a16f46797fc0f6de2bf94850e3b3039bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485436"
---
# <a name="creating-a-multisession-disc"></a><span data-ttu-id="a0837-103">Creazione di un disco multisessione</span><span class="sxs-lookup"><span data-stu-id="a0837-103">Creating a Multisession Disc</span></span>

<span data-ttu-id="a0837-104">L'API per la creazione di [Immagini Master](about-imapi.md) (IMAPI) supporta l'aggiunta e la rimozione di file da e verso i seguenti tipi di dischi multisessione:</span><span class="sxs-lookup"><span data-stu-id="a0837-104">The [Image Mastering API](about-imapi.md) (IMAPI) supports the addition and removal of files to, or from, the following multisession disc types:</span></span>

-   <span data-ttu-id="a0837-105">CD-R/CD-RW</span><span class="sxs-lookup"><span data-stu-id="a0837-105">CD-R/CD-RW</span></span>
-   <span data-ttu-id="a0837-106">Single-Layer DVD + R/DVD-R</span><span class="sxs-lookup"><span data-stu-id="a0837-106">Single-Layer DVD+R/DVD-R</span></span>
-   <span data-ttu-id="a0837-107">DVD + R Dual Layer</span><span class="sxs-lookup"><span data-stu-id="a0837-107">DVD+R Dual Layer</span></span>
-   <span data-ttu-id="a0837-108">BD-R</span><span class="sxs-lookup"><span data-stu-id="a0837-108">BD-R</span></span>
-   <span data-ttu-id="a0837-109">DVD-RW/DVD + RW (**solo Windows 7**)</span><span class="sxs-lookup"><span data-stu-id="a0837-109">DVD-RW/DVD+RW (**Windows 7 Only**)</span></span>
-   <span data-ttu-id="a0837-110">DVD-RAM (**solo Windows 7**)</span><span class="sxs-lookup"><span data-stu-id="a0837-110">DVD-RAM (**Windows 7 Only**)</span></span>
-   <span data-ttu-id="a0837-111">BD-RE (**solo Windows 7**)</span><span class="sxs-lookup"><span data-stu-id="a0837-111">BD-RE (**Windows 7 Only**)</span></span>

<span data-ttu-id="a0837-112">La creazione di un disco a più sessioni con IMAPi prevede i passaggi seguenti.</span><span class="sxs-lookup"><span data-stu-id="a0837-112">Creation of a multisession disc using IMAPI consists of the following steps.</span></span> <span data-ttu-id="a0837-113">Ognuno di questi passaggi documentati contiene la parte pertinente dell'esempio di script completo Visual Basic disponibile nella sezione finale.</span><span class="sxs-lookup"><span data-stu-id="a0837-113">Each of these documented steps contains the relevant portion of the complete Visual Basic script example provided in the final section.</span></span>

## <a name="initializing-the-disc-recorder"></a><span data-ttu-id="a0837-114">Inizializzazione del registratore di dischi</span><span class="sxs-lookup"><span data-stu-id="a0837-114">Initializing the Disc Recorder</span></span>

<span data-ttu-id="a0837-115">Prima dell'inizializzazione del dispositivo, l'oggetto **MsftDiscMaster2** fornisce un'enumerazione dei dispositivi ottici nel sistema.</span><span class="sxs-lookup"><span data-stu-id="a0837-115">Prior to device initialization, the **MsftDiscMaster2** object provides an enumeration of the optical devices on the system.</span></span> <span data-ttu-id="a0837-116">L'interfaccia [**IDiscMaster2**](/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2) fornisce l'accesso a questa enumerazione del dispositivo per facilitare la posizione del dispositivo di registrazione appropriato.</span><span class="sxs-lookup"><span data-stu-id="a0837-116">The [**IDiscMaster2**](/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2) interface provides access to this device enumeration to facilitate the location of the appropriate recording device.</span></span> <span data-ttu-id="a0837-117">L'oggetto **MsftDiscMaster2** fornisce anche le notifiche degli eventi quando i dispositivi ottici vengono aggiunti o rimossi da un computer.</span><span class="sxs-lookup"><span data-stu-id="a0837-117">The **MsftDiscMaster2** object also provides event notifications when optical devices are added to or removed from a machine.</span></span>

<span data-ttu-id="a0837-118">Dopo aver individuato un registratore ottico e aver recuperato l'ID assegnato, creare un nuovo oggetto **MsftDiscMaster2** e inizializzare il registratore usando l'ID dispositivo specifico.</span><span class="sxs-lookup"><span data-stu-id="a0837-118">After locating an optical recorder and retrieving the ID assigned to it, create a new **MsftDiscMaster2** object and initialize the recorder using the specific device ID.</span></span>

<span data-ttu-id="a0837-119">L'interfaccia [**IDiscRecorder2**](/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2) consente di accedere alle informazioni di base sul dispositivo, ad esempio ID fornitore, ID prodotto, revisione del prodotto, nonché i metodi per estrarre i supporti o chiudere la barra.</span><span class="sxs-lookup"><span data-stu-id="a0837-119">The [**IDiscRecorder2**](/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2) interface provides access to basic device information such as vendor ID, product ID, product revision, as well as the methods to eject media or close the tray.</span></span>

> [!Note]  
> <span data-ttu-id="a0837-120">Le costanti e le dimensioni aggiuntive dichiarate nell'esempio seguente vengono usate in un secondo momento nello script di esempio completo presente nella sezione finale di questo documento.</span><span class="sxs-lookup"><span data-stu-id="a0837-120">The additional constants and dimensions declared in the following sample are used later in the complete sample script located in the final section of this document.</span></span> <span data-ttu-id="a0837-121">Questi elementi non sono necessari per l'operazione di inizializzazione di un registratore di dischi.</span><span class="sxs-lookup"><span data-stu-id="a0837-121">These elements are not required for the act of initializing a disc recorder.</span></span>

 


```VB
' **_ CD/DVD disc file system types
Const FsiFileSystemISO9660 = 1
Const FsiFileSystemJoliet  = 2
Const FsiFileSystemUDF102  = 4

WScript.Quit(Main)

Function Main
    Dim Index                ' Index to recording drive.
    Dim Recorder             ' Recorder object
    Dim Path                 ' Directory of files to add
    Dim Stream               ' Data stream for burning device
    
    Index = 0                ' First drive on the system
    Path = "G:\BurnDir"      ' Files to add to the disc

    ' Create a DiscMaster2 object to connect to optical drives.
    Dim DiscMaster
    Set DiscMaster = WScript.CreateObject("IMAPI2.MsftDiscMaster2")

    ' Create a DiscRecorder2 object for the specified burning device.
    Dim UniqueId
    set Recorder = WScript.CreateObject("IMAPI2.MsftDiscRecorder2")
    UniqueId = DiscMaster.Item(Index)
    Recorder.InitializeDiscRecorder(UniqueId)
```



## <a name="creating-a-data-writer"></a><span data-ttu-id="a0837-122">Creazione di un writer di dati</span><span class="sxs-lookup"><span data-stu-id="a0837-122">Creating a Data Writer</span></span>

<span data-ttu-id="a0837-123">L'oggetto _ *MsftDiscFormat2Data*\* fornisce il metodo di scrittura, le relative proprietà e le proprietà specifiche del supporto.</span><span class="sxs-lookup"><span data-stu-id="a0837-123">The _ *MsftDiscFormat2Data*\* object provides the writing method, its properties, as well as the media-specific properties.</span></span> <span data-ttu-id="a0837-124">L'interfaccia [**IDiscFormat2Data**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data) fornisce l'accesso a questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="a0837-124">The [**IDiscFormat2Data**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data) interface provides access to this object.</span></span>

<span data-ttu-id="a0837-125">La registrazione del disco viene associata al writer del formato utilizzando la proprietà [**IDiscFormat2Data::p UT \_ Recorder**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-put_recorder) .</span><span class="sxs-lookup"><span data-stu-id="a0837-125">The disc recorder binds to the format writer using the [**IDiscFormat2Data::put\_Recorder**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-put_recorder) property.</span></span> <span data-ttu-id="a0837-126">Dopo che il registratore è stato associato al writer di formato, è possibile eseguire query sui supporti e sulle proprietà specifiche della scrittura prima di scrivere l'immagine del risultato nel disco usando il metodo [**IDiscFormat2Data:: Write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) .</span><span class="sxs-lookup"><span data-stu-id="a0837-126">After the recorder is bound to the format writer, media and write-specific property queries can be performed prior to writing the result image to disc using the [**IDiscFormat2Data::Write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) method.</span></span>

> [!Note]  
> <span data-ttu-id="a0837-127">La stringa del nome client specificata nel codice di esempio riportato di seguito deve essere regolata in base alle esigenze dell'applicazione specifica.</span><span class="sxs-lookup"><span data-stu-id="a0837-127">The client name string specified in the sample code below should be adjusted as appropriate for the specific application.</span></span>

 


```VB
    ' Create a DiscFormat2Data object and set the recorder
    Dim DataWriter
    Set DataWriter = CreateObject ("IMAPI2.MsftDiscFormat2Data")
    DataWriter.Recorder = Recorder
    DataWriter.ClientName = "IMAPIv2 TEST"
```



## <a name="creating-the-file-system-object"></a><span data-ttu-id="a0837-128">Creazione dell'oggetto file System</span><span class="sxs-lookup"><span data-stu-id="a0837-128">Creating the File System Object</span></span>

<span data-ttu-id="a0837-129">Per registrare una nuova sessione, prima di tutto è necessario generare un'immagine di masterizzazione.</span><span class="sxs-lookup"><span data-stu-id="a0837-129">In order to record a new session, a burn image must be generated for it first.</span></span> <span data-ttu-id="a0837-130">Un'immagine Burn per i formati **ISO9660**, **Joliet** e **UDF** è costituita da file System di singoli file e directory.</span><span class="sxs-lookup"><span data-stu-id="a0837-130">A burn image for **ISO9660**, **Joliet** and **UDF** formats consist of file systems of individual files and directories.</span></span> <span data-ttu-id="a0837-131">L'oggetto **MsftFileSystemImage** è l'oggetto file system contenente i file e le directory da collocare sul supporto ottico.</span><span class="sxs-lookup"><span data-stu-id="a0837-131">The **MsftFileSystemImage** object is the file system object that contains the files and directories to be placed on the optical media.</span></span> <span data-ttu-id="a0837-132">L'interfaccia [**IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) fornisce l'accesso all'oggetto file System e alle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="a0837-132">The [**IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) interface provides access to the file system object and settings.</span></span>


```VB
    ' Create a new file system image object
    Dim FSI
    Set FSI = CreateObject("IMAPI2FS.MsftFileSystemImage")
```



## <a name="importing-a-file-system"></a><span data-ttu-id="a0837-133">Importazione di un file System</span><span class="sxs-lookup"><span data-stu-id="a0837-133">Importing a File System</span></span>

<span data-ttu-id="a0837-134">Prima di procedere, verificare che il disco non sia vuoto controllando la proprietà [**IDiscFormat2:: Get \_ MediaHeuristicallyBlank**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2-get_mediaheuristicallyblank) .</span><span class="sxs-lookup"><span data-stu-id="a0837-134">Before proceeding, ensure that the disc is not blank by checking the [**IDiscFormat2::get\_MediaHeuristicallyBlank**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2-get_mediaheuristicallyblank) property.</span></span>

<span data-ttu-id="a0837-135">Dopo aver creato l'oggetto **MsftFileSystemImage** , la proprietà [**IFileSystemImage::p UT \_ MultisessionInterfaces**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_multisessioninterfaces) deve essere inizializzata prima di una chiamata al metodo [**IFileSystemImage:: ImportFileSystem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importfilesystem) o [**IFileSystemImage:: ImportSpecificFileSystem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importspecificfilesystem) per importare il file System dall'ultima sessione registrata.</span><span class="sxs-lookup"><span data-stu-id="a0837-135">After creating the **MsftFileSystemImage** object, the [**IFileSystemImage::put\_MultisessionInterfaces**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_multisessioninterfaces) property should be initialized prior to a call to either the [**IFileSystemImage::ImportFileSystem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importfilesystem) or [**IFileSystemImage::ImportSpecificFileSystem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importspecificfilesystem) method to import the file system from the last recorded session.</span></span> <span data-ttu-id="a0837-136">Questi metodi compileranno automaticamente l'oggetto **MsftFileSystemImage** con le informazioni che descrivono i file e le directory precedentemente registrati.</span><span class="sxs-lookup"><span data-stu-id="a0837-136">These methods will automatically populate the **MsftFileSystemImage** object with information describing the previously recorded files and directories.</span></span>

> [!Note]  
> <span data-ttu-id="a0837-137">La proprietà [**IFileSystemImage::p UT \_ MultisessionInterfaces**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_multisessioninterfaces) viene in genere inizializzata con le interfacce multisessione fornite dal writer di dati tramite la proprietà [**IDiscFormat2Data:: Get \_ MultisessionInterfaces**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_multisessioninterfaces) .</span><span class="sxs-lookup"><span data-stu-id="a0837-137">The [**IFileSystemImage::put\_MultisessionInterfaces**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_multisessioninterfaces) property is typically initialized with the multisession interfaces provided by the data writer via the [**IDiscFormat2Data::get\_MultisessionInterfaces**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_multisessioninterfaces) property.</span></span>

 

<span data-ttu-id="a0837-138">Il tentativo di impostare la proprietà **IFileSystemImage::p UT \_ MultisessionInterfaces** avrà esito negativo se IMAPI non supporta la multisessione per il supporto attualmente inserito o se non è possibile accodare il supporto per altri motivi, ad esempio perché è chiuso.</span><span class="sxs-lookup"><span data-stu-id="a0837-138">Attempts to set the **IFileSystemImage::put\_MultisessionInterfaces** property will fail if IMAPI does not support multisession for the currently inserted media or the media cannot be appended for some other reason (e.g. because it is closed).</span></span>

<span data-ttu-id="a0837-139">Se la sessione Burn precedente conteneva più di un tipo di file system, il metodo [**IFileSystemImage:: ImportFileSystem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importfilesystem) importerà le informazioni del tipo di file System più avanzato presente.</span><span class="sxs-lookup"><span data-stu-id="a0837-139">If the previous burn session contained more than one file system type, the [**IFileSystemImage::ImportFileSystem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importfilesystem) method will import information from the most advanced file system type present.</span></span> <span data-ttu-id="a0837-140">Ad esempio, nell'esempio fornito in questo argomento, UDF è il file system importato.</span><span class="sxs-lookup"><span data-stu-id="a0837-140">For example, in the example provided in this topic, UDF is the imported file system.</span></span> <span data-ttu-id="a0837-141">Tuttavia, l'utilizzo del metodo [**IFileSystemImage:: ImportSpecificFileSystem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importspecificfilesystem) consente la selezione specifica del file System da importare.</span><span class="sxs-lookup"><span data-stu-id="a0837-141">However, use of the [**IFileSystemImage::ImportSpecificFileSystem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importspecificfilesystem) method allows the specific selection of the file system to import.</span></span>

> [!Note]  
> <span data-ttu-id="a0837-142">Il metodo [**IFileSystemImage:: IdentifyFileSystemsOnDisc**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-identifyfilesystemsondisc) può essere usato per determinare quali file System sono disponibili nel disco.</span><span class="sxs-lookup"><span data-stu-id="a0837-142">The [**IFileSystemImage::IdentifyFileSystemsOnDisc**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-identifyfilesystemsondisc) method can be used to determine which file systems are available on the disc.</span></span>

 


```VB
    ' Import the last session, if the disc is not empty, or initialize
    ' the file system, if the disc is empty
    If Not DataWriter.MediaHeuristicallyBlank _
    Then
        On Error Resume Next
        FSI.MultisessionInterfaces = DataWriter.MultisessionInterfaces
        If Err.Number <> 0 _
        Then
            WScript.Echo "Multisession is not supported for this disc"
            Main = 1
            Exit Function
        End If
        On Error Goto 0

        WScript.Echo "Importing data from the previous session..."
        FSI.ImportFileSystem()
    Else 
        FSI.ChooseImageDefaults(Recorder)
    End If
```



## <a name="adding-or-removing-files-to-the-file-system"></a><span data-ttu-id="a0837-143">Aggiunta o rimozione di file nel file System</span><span class="sxs-lookup"><span data-stu-id="a0837-143">Adding or Removing Files to the File System</span></span>

<span data-ttu-id="a0837-144">Dopo aver creato l'oggetto file system e aver importato i file system dalla sessione precedente, chiamare i metodi [**IFileSystemImage:: CreateFileItem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createfileitem) e [**IFileSystemImage:: CreateDirectoryItem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createdirectoryitem) per creare nuovi oggetti di file e directory, rispettivamente.</span><span class="sxs-lookup"><span data-stu-id="a0837-144">After creating the file system object and importing the file system from the previous session, call the [**IFileSystemImage::CreateFileItem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createfileitem) and [**IFileSystemImage::CreateDirectoryItem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createdirectoryitem) methods to create new file and directory objects, respectively.</span></span> <span data-ttu-id="a0837-145">Gli oggetti file e directory forniscono dettagli specifici sui file e le directory.</span><span class="sxs-lookup"><span data-stu-id="a0837-145">The file and directory objects provide specific details about the files and directories.</span></span> <span data-ttu-id="a0837-146">In alternativa, è possibile usare il metodo [**metodo IFsiDirectoryItem:: AddTree**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-addtree) di un oggetto directory, rappresentato tramite l'interfaccia [**metodo IFsiDirectoryItem**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem) , per aggiungere file e directory esistenti da un altro dispositivo di archiviazione (ad esempio un disco rigido).</span><span class="sxs-lookup"><span data-stu-id="a0837-146">Alternatively, the [**IFsiDirectoryItem::AddTree**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-addtree) method of a directory object, represented via the [**IFsiDirectoryItem**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem) interface, can be used to add existing files and directories from another storage device (i.e. a hard drive).</span></span>

<span data-ttu-id="a0837-147">Il metodo di aggiornamento del gestore eventi disponibile per [**IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) identifica il file corrente da aggiungere all'immagine file System, il numero di settori già copiati e il numero totale di settori da copiare.</span><span class="sxs-lookup"><span data-stu-id="a0837-147">The event handler update method available for [**IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) identifies the current file being added to the file system image, the number of sectors already copied, and the total number of sectors to be copied.</span></span>

<span data-ttu-id="a0837-148">Per rimuovere i file e le directory esistenti dalla file system, usare i metodi [**metodo IFsiDirectoryItem:: Remove**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-remove) e [**metodo IFsiDirectoryItem:: RemoveTree**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-removetree) degli oggetti directory rappresentati tramite l'interfaccia [**metodo IFsiDirectoryItem**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem) .</span><span class="sxs-lookup"><span data-stu-id="a0837-148">To remove existing files and directories from the file system, use the [**IFsiDirectoryItem::Remove**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-remove) and [**IFsiDirectoryItem::RemoveTree**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-removetree) methods of the directory objects represented via the [**IFsiDirectoryItem**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem) interface.</span></span> <span data-ttu-id="a0837-149">La proprietà [**IFileSystemImage:: Get \_ root**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_root) viene utilizzata per ottenere un puntatore alla directory radice del file System e l'interfaccia **metodo IFsiDirectoryItem** per attraversare l'albero di directory.</span><span class="sxs-lookup"><span data-stu-id="a0837-149">The [**IFileSystemImage::get\_Root**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_root) property is used to get a pointer to the root directory of the file system and the **IFsiDirectoryItem** interface to traverse through the directory tree.</span></span>

> [!Note]  
> <span data-ttu-id="a0837-150">I file e le directory rimossi tramite i metodi [**metodo IFsiDirectoryItem:: Remove**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-remove) e [**metodo IFsiDirectoryItem:: RemoveTree**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-removetree) non vengono rimossi fisicamente dal disco e il software avanzato può recuperare facilmente le informazioni eliminate.</span><span class="sxs-lookup"><span data-stu-id="a0837-150">Files and directories removed via the [**IFsiDirectoryItem::Remove**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-remove) and [**IFsiDirectoryItem::RemoveTree**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-removetree) methods are not physically removed from the disc, and advanced software can easily recover the deleted information.</span></span>

 


```VB
    ' Add the directory and its contents to the file system 
    WScript.Echo "Adding " & Path & " directory to the disc..."
    FSI.Root.AddTree Path, false
```



## <a name="constructing-a-file-system-image"></a><span data-ttu-id="a0837-151">Creazione di un'immagine del file System</span><span class="sxs-lookup"><span data-stu-id="a0837-151">Constructing a File System Image</span></span>

<span data-ttu-id="a0837-152">Il passaggio finale consiste nel chiamare [**IFileSystemImage:: CreateResultImage**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createresultimage) per creare un flusso di dati per l'immagine Burn e fornire l'accesso tramite l'interfaccia [**IFileSystemImageResult**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimageresult) .</span><span class="sxs-lookup"><span data-stu-id="a0837-152">The final step is to call [**IFileSystemImage::CreateResultImage**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createresultimage) to create a data stream for the burn image and provide access to it through the [**IFileSystemImageResult**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimageresult) interface.</span></span> <span data-ttu-id="a0837-153">Questo flusso di dati può essere fornito direttamente al metodo [**IDiscFormat2Data:: Write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) oppure deve essere salvato in un file per un uso successivo.</span><span class="sxs-lookup"><span data-stu-id="a0837-153">This data stream can either be provided directly to the [**IDiscFormat2Data::Write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) method or be saved to a file for later use.</span></span>


```VB
    ' Create an image from the file system image object
    Dim Result
    Set Result = FSI.CreateResultImage()
    Stream = Result.ImageStream
```



## <a name="example-summary"></a><span data-ttu-id="a0837-154">Riepilogo di esempio</span><span class="sxs-lookup"><span data-stu-id="a0837-154">Example Summary</span></span>

<span data-ttu-id="a0837-155">Nell'esempio di script Visual Basic riportato di seguito viene illustrato come utilizzare gli oggetti IMAPi per creare dischi multisessione.</span><span class="sxs-lookup"><span data-stu-id="a0837-155">The following Visual Basic script example shows how to use IMAPI objects to create multisession discs.</span></span> <span data-ttu-id="a0837-156">Nell'esempio viene creata una nuova sessione e viene aggiunta una directory al disco. Per semplicità, il codice non esegue un controllo degli errori esteso e presuppone quanto segue:</span><span class="sxs-lookup"><span data-stu-id="a0837-156">The example creates a new session and adds a directory to the disc. For the sake of simplicity, the code does not perform extensive error checking, and assumes the following:</span></span>

-   <span data-ttu-id="a0837-157">Nel sistema è installato un dispositivo disco compatibile.</span><span class="sxs-lookup"><span data-stu-id="a0837-157">A compatible disc device is installed on the system.</span></span>
-   <span data-ttu-id="a0837-158">Il dispositivo disco è la prima unità nel sistema.</span><span class="sxs-lookup"><span data-stu-id="a0837-158">The disc device is the first drive on the system.</span></span>
-   <span data-ttu-id="a0837-159">Viene inserito un disco compatibile nel dispositivo disco.</span><span class="sxs-lookup"><span data-stu-id="a0837-159">A compatible disc is inserted in the disc device.</span></span>
-   <span data-ttu-id="a0837-160">I file da aggiungere al disco si trovano in "g: \\ burndir".</span><span class="sxs-lookup"><span data-stu-id="a0837-160">Files to add to the disc are located in "g:\\burndir".</span></span>

<span data-ttu-id="a0837-161">È possibile aggiungere allo script funzionalità aggiuntive, ad esempio il controllo completo degli errori, la compatibilità di dispositivi e supporti, la notifica degli eventi e il calcolo dello spazio disponibile sul disco.</span><span class="sxs-lookup"><span data-stu-id="a0837-161">Additional functionality such as extensive error checking, device and media compatibility, event notification, and calculation of free space on the disc can be added to the script.</span></span>


```VB
' This script adds data files from a single directory tree to a
' disc (a new session is added, if the disc already contains data)

' Copyright (C) Microsoft. All rights reserved.

Option Explicit

' **_ CD/DVD disc file system types
Const FsiFileSystemISO9660 = 1
Const FsiFileSystemJoliet  = 2
Const FsiFileSystemUDF102  = 4

WScript.Quit(Main)

Function Main
    Dim Index                ' Index to recording drive.
    Dim Recorder             ' Recorder object
    Dim Path                 ' Directory of files to add
    Dim Stream               ' Data stream for burning device
    
    Index = 0                ' First drive on the system
    Path = "G:\BurnDir"      ' Files to add to the disc

    ' Create a DiscMaster2 object to connect to optical drives.
    Dim DiscMaster
    Set DiscMaster = WScript.CreateObject("IMAPI2.MsftDiscMaster2")

    ' Create a DiscRecorder2 object for the specified burning device.
    Dim UniqueId
    set Recorder = WScript.CreateObject("IMAPI2.MsftDiscRecorder2")
    UniqueId = DiscMaster.Item(Index)
    Recorder.InitializeDiscRecorder(UniqueId)

    ' Create a DiscFormat2Data object and set the recorder
    Dim DataWriter
    Set DataWriter = CreateObject ("IMAPI2.MsftDiscFormat2Data")
    DataWriter.Recorder = Recorder
    DataWriter.ClientName = "IMAPIv2 TEST"

    ' Create a new file system image object
    Dim FSI
    Set FSI = CreateObject("IMAPI2FS.MsftFileSystemImage")

    ' Import the last session, if the disc is not empty, or initialize
    ' the file system, if the disc is empty
    If Not DataWriter.MediaHeuristicallyBlank _
    Then
        On Error Resume Next
        FSI.MultisessionInterfaces = DataWriter.MultisessionInterfaces
        If Err.Number <> 0 _
        Then
            WScript.Echo "Multisession is not supported for this disc"
            Main = 1
            Exit Function
        End If
        On Error Goto 0

        WScript.Echo "Importing data from the previous session..."
        FSI.ImportFileSystem()
    Else 
        FSI.ChooseImageDefaults(Recorder)
    End If

    ' Add the directory and its contents to the file system 
    WScript.Echo "Adding " & Path & " directory to the disc..."
    FSI.Root.AddTree Path, false

    ' Create an image from the file system image object
    Dim Result
    Set Result = FSI.CreateResultImage()
    Stream = Result.ImageStream
    
    ' Write stream to disc using the specified recorder
    WScript.Echo "Writing content to the disc..."
    DataWriter.Write(Stream)

    WScript.Echo "Finished writing content."
    Main = 0
End Function

```



## <a name="related-topics"></a><span data-ttu-id="a0837-162">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a0837-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0837-163">Uso di IMAPi</span><span class="sxs-lookup"><span data-stu-id="a0837-163">Using IMAPI</span></span>](using-imapi.md)
</dt> <dt>

[<span data-ttu-id="a0837-164">_ *IStream*\*</span><span class="sxs-lookup"><span data-stu-id="a0837-164">_ *IStream*\*</span></span>](/windows/desktop/api/objidl/nn-objidl-istream)
</dt> <dt>

[<span data-ttu-id="a0837-165">**IDiscMaster2**</span><span class="sxs-lookup"><span data-stu-id="a0837-165">**IDiscMaster2**</span></span>](/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2)
</dt> <dt>

[<span data-ttu-id="a0837-166">**IDiscFormat2Data**</span><span class="sxs-lookup"><span data-stu-id="a0837-166">**IDiscFormat2Data**</span></span>](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data)
</dt> <dt>

[<span data-ttu-id="a0837-167">**IFileSystemImage**</span><span class="sxs-lookup"><span data-stu-id="a0837-167">**IFileSystemImage**</span></span>](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage)
</dt> </dl>

 

 
