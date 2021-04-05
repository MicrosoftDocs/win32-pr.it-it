---
description: Il formato del disco rigido virtuale (VHD) è una specifica del formato di immagine disponibile pubblicamente che consente di incapsulare il disco rigido in un singolo file per l'uso da parte del sistema operativo come disco virtuale in tutti gli stessi modi in cui vengono usati i dischi rigidi fisici.
MS-HAID: vhd.about\_vhd
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Informazioni su VHD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29ea37851360e70c1108e0715a47c77163c2c2fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751522"
---
# <a name="span-idvhdabout_vhdspanabout-vhd"></a><span data-ttu-id="e3453-103"><span id="vhd.about_vhd"></span>Informazioni su VHD</span><span class="sxs-lookup"><span data-stu-id="e3453-103"><span id="vhd.about_vhd"></span>About VHD</span></span>

<span data-ttu-id="e3453-104">Il formato del disco rigido virtuale (VHD) è una [specifica](https://download.microsoft.com/download/f/f/e/ffef50a5-07dd-4cf8-aaa3-442c0673a029/Virtual%20Hard%20Disk%20Format%20Spec_10_18_06.doc) del formato di immagine disponibile pubblicamente che consente di incapsulare il disco rigido in un singolo file per l'uso da parte del sistema operativo come *disco virtuale* in tutti gli stessi modi in cui vengono usati i dischi rigidi fisici.</span><span class="sxs-lookup"><span data-stu-id="e3453-104">The Virtual Hard Disk (VHD) format is a publicly-available image format [specification](https://download.microsoft.com/download/f/f/e/ffef50a5-07dd-4cf8-aaa3-442c0673a029/Virtual%20Hard%20Disk%20Format%20Spec_10_18_06.doc) that allows encapsulation of the hard disk into an individual file for use by the operating system as a *virtual disk* in all the same ways physical hard disks are used.</span></span> <span data-ttu-id="e3453-105">Questi dischi virtuali sono in grado di ospitare file System nativi (NTFS, FAT, exFAT e UDF), supportando al tempo stesso le operazioni standard su disco e file.</span><span class="sxs-lookup"><span data-stu-id="e3453-105">These virtual disks are capable of hosting native file systems (NTFS, FAT, exFAT, and UDFS) while supporting standard disk and file operations.</span></span> <span data-ttu-id="e3453-106">Il supporto delle API VHD consente la gestione dei dischi virtuali.</span><span class="sxs-lookup"><span data-stu-id="e3453-106">VHD API support allows management of the virtual disks.</span></span> <span data-ttu-id="e3453-107">I dischi virtuali creati con l'API VHD possono fungere da dischi di avvio.</span><span class="sxs-lookup"><span data-stu-id="e3453-107">Virtual disks created with the VHD API can function as boot disks.</span></span>

<span data-ttu-id="e3453-108">Un esempio di come vengono usati i file VHD è la funzionalità [Hyper-V](https://www.microsoft.com/windowsserver2008/en/us/hyperv.aspx) in Windows 7, windows Server 2008, Virtual Server e Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="e3453-108">An example of how VHD files are used is the [Hyper-V](https://www.microsoft.com/windowsserver2008/en/us/hyperv.aspx) feature in Windows 7, Windows Server 2008, Virtual Server, and Windows Virtual PC.</span></span> <span data-ttu-id="e3453-109">Questi prodotti usano l'API del disco rigido virtuale per contenere l'immagine del sistema operativo Windows usata da una macchina virtuale come disco di avvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="e3453-109">These products use the VHD API to contain the Windows operating system image utilized by a virtual machine as its system boot disk.</span></span>

<span data-ttu-id="e3453-110">Il Software Development Kit (SDK) di Microsoft Windows integra il supporto VHD nativo per l'utilizzo di dischi virtuali, semplificando la creazione, la gestione e la distribuzione di immagini di Windows in file VHD tramite gli strumenti di gestione o il supporto API della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="e3453-110">The Microsoft Windows Software Development Kit (SDK) integrates Native VHD support for working with virtual disks, making it easier for developers and administrators to create, manage, and deploy Windows images in VHD files using either the platform API support or management tools.</span></span> <span data-ttu-id="e3453-111">Non è necessario installare applicazioni separate o implementare un parser di formato VHD per abilitare queste operazioni.</span><span class="sxs-lookup"><span data-stu-id="e3453-111">It is not necessary to install separate applications or implement a VHD format parser to enable these operations.</span></span> <span data-ttu-id="e3453-112">Queste API consentono l'uso generico di dischi virtuali indipendenti da qualsiasi altra tecnologia di virtualizzazione.</span><span class="sxs-lookup"><span data-stu-id="e3453-112">These APIs allow for generic use of virtual disks independent of any other virtualization technologies.</span></span>

## <a name="span-idterminologyspanspan-idterminologyspanspan-idterminologyspanterminology"></a><span data-ttu-id="e3453-113"><span id="Terminology"></span><span id="terminology"></span><span id="TERMINOLOGY"></span>Terminologia</span><span class="sxs-lookup"><span data-stu-id="e3453-113"><span id="Terminology"></span><span id="terminology"></span><span id="TERMINOLOGY"></span>Terminology</span></span>

<span data-ttu-id="e3453-114">Il termine *Archivio di backup* viene usato per fare riferimento al file fisico presente sul disco rigido effettivo.</span><span class="sxs-lookup"><span data-stu-id="e3453-114">The term *backing store* is used to refer to the physical file that exists on the actual hard disk.</span></span> <span data-ttu-id="e3453-115">L'archivio di backup è rappresentato da un *file di immagine VHD*.</span><span class="sxs-lookup"><span data-stu-id="e3453-115">The backing store is represented by a *VHD image file*.</span></span>

<span data-ttu-id="e3453-116">I termini *dinamici*, *espandibili* e *sparse* vengono spesso usati in modo interscambiabile quando si fa riferimento a dischi virtuali espandibili dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="e3453-116">The terms *dynamic*, *expandable*, and *sparse* are often used interchangeably when referring to dynamically expandable virtual disks.</span></span> <span data-ttu-id="e3453-117">Per la tecnologia VHD, questi termini sono identici.</span><span class="sxs-lookup"><span data-stu-id="e3453-117">For VHD technology, these terms are identical.</span></span>

## <a name="span-idvhd_system_features_overviewspanspan-idvhd_system_features_overviewspanspan-idvhd_system_features_overviewspanvhd-system-features-overview"></a><span data-ttu-id="e3453-118"><span id="VHD_System_Features_Overview"></span><span id="vhd_system_features_overview"></span><span id="VHD_SYSTEM_FEATURES_OVERVIEW"></span>Panoramica delle funzionalità del sistema VHD</span><span class="sxs-lookup"><span data-stu-id="e3453-118"><span id="VHD_System_Features_Overview"></span><span id="vhd_system_features_overview"></span><span id="VHD_SYSTEM_FEATURES_OVERVIEW"></span>VHD System Features Overview</span></span>

<span data-ttu-id="e3453-119">Il diagramma seguente presenta una panoramica delle funzionalità del disco rigido virtuale e delle relative relazioni.</span><span class="sxs-lookup"><span data-stu-id="e3453-119">The following diagram presents an overview of the VHD features and their relationships.</span></span>

![diagramma di blocco VHD](images/vhd.png)

<span data-ttu-id="e3453-121">Di seguito è riportata una spiegazione riepilogativa delle funzionalità descritte in precedenza.</span><span class="sxs-lookup"><span data-stu-id="e3453-121">The following is a summary explanation of the previously described features.</span></span>

<span data-ttu-id="e3453-122">API Windows native in modalità utente:</span><span class="sxs-lookup"><span data-stu-id="e3453-122">User Mode Native Windows APIs:</span></span>

-   <span data-ttu-id="e3453-123">VirtDisk.dll libreria comune per le API di gestione del disco rigido virtuale.</span><span class="sxs-lookup"><span data-stu-id="e3453-123">VirtDisk.dll - Common library for VHD management APIs.</span></span>

<span data-ttu-id="e3453-124">Wrapper di gestione specifici del dominio in modalità utente:</span><span class="sxs-lookup"><span data-stu-id="e3453-124">User Mode Domain-specific Management Wrappers:</span></span>

-   <span data-ttu-id="e3453-125">[API del disco rigido virtuale VDS](/windows/desktop/VDS/about-vds) : wrapper del modello a oggetti VDS per le API Windows del disco rigido virtuale.</span><span class="sxs-lookup"><span data-stu-id="e3453-125">[VDS VHD APIs](/windows/desktop/VDS/about-vds) - VDS Object Model wrappers for the VHD Windows APIs.</span></span>

<span data-ttu-id="e3453-126">Driver in modalità kernel:</span><span class="sxs-lookup"><span data-stu-id="e3453-126">Kernel Mode Drivers:</span></span>

-   <span data-ttu-id="e3453-127">Enumeratore unità virtuale VDrvRoot.sys-root.</span><span class="sxs-lookup"><span data-stu-id="e3453-127">VDrvRoot.sys - Root virtual drive enumerator.</span></span>
-   <span data-ttu-id="e3453-128">Gestione delle dipendenze del volume annidato in FsDepends.sys.</span><span class="sxs-lookup"><span data-stu-id="e3453-128">FsDepends.sys - Nested volume dependency management.</span></span>
-   <span data-ttu-id="e3453-129">Parser Vhdmp.sys-VHD e provider di proprietà di dipendenza.</span><span class="sxs-lookup"><span data-stu-id="e3453-129">Vhdmp.sys - VHD parser and dependency property provider.</span></span>

<span data-ttu-id="e3453-130">La documentazione dell'SDK in questa sezione descrive le API native di Windows VHD in modalità utente.</span><span class="sxs-lookup"><span data-stu-id="e3453-130">The SDK documentation in this section covers the user-mode native Windows VHD APIs.</span></span>

## <a name="span-idvirtual_disk_typesspanspan-idvirtual_disk_typesspanspan-idvirtual_disk_typesspanvirtual-disk-types"></a><span data-ttu-id="e3453-131"><span id="Virtual_Disk_Types"></span><span id="virtual_disk_types"></span><span id="VIRTUAL_DISK_TYPES"></span>Tipi di dischi virtuali</span><span class="sxs-lookup"><span data-stu-id="e3453-131"><span id="Virtual_Disk_Types"></span><span id="virtual_disk_types"></span><span id="VIRTUAL_DISK_TYPES"></span>Virtual Disk Types</span></span>

<span data-ttu-id="e3453-132">Ci sono alcune considerazioni per l'uso dei dischi virtuali e i tipi di dischi virtuali disponibili:</span><span class="sxs-lookup"><span data-stu-id="e3453-132">There are considerations for using virtual disks, and what types of virtual disks are available:</span></span>

-   <span data-ttu-id="e3453-133">**Corretto**: il file di immagine del disco rigido virtuale è preallocato nell'archivio di backup per le dimensioni massime richieste.</span><span class="sxs-lookup"><span data-stu-id="e3453-133">**Fixed**—The VHD image file is pre-allocated on the backing store for the maximum size requested.</span></span>
-   <span data-ttu-id="e3453-134">**Espandibile**, noto anche come "dinamico", "espandibile in modo dinamico" e "sparse", il file di immagine VHD usa solo lo spazio disponibile nell'archivio di backup in base alle esigenze per archiviare i dati effettivi attualmente contenuti nel disco virtuale.</span><span class="sxs-lookup"><span data-stu-id="e3453-134">**Expandable**—Also known as "dynamic", "dynamically expandable", and "sparse", the VHD image file uses only as much space on the backing store as needed to store the actual data the virtual disk currently contains.</span></span> <span data-ttu-id="e3453-135">Quando si crea questo tipo di disco virtuale, l'API VHD non verifica lo spazio disponibile sul disco fisico in base alle dimensioni massime richieste. è pertanto possibile creare correttamente un disco virtuale dinamico con dimensioni massime maggiori dello spazio libero su disco fisico disponibile.</span><span class="sxs-lookup"><span data-stu-id="e3453-135">When creating this type of virtual disk, the VHD API does not test for free space on the physical disk based on the maximum size requested, therefore it is possible to successfully create a dynamic virtual disk with a maximum size larger than the available physical disk free space.</span></span> <span data-ttu-id="e3453-136">Per ulteriori informazioni, vedere [**ExpandVirtualDisk**](/windows/win32/api/virtdisk/nf-virtdisk-expandvirtualdisk).</span><span class="sxs-lookup"><span data-stu-id="e3453-136">For more information, see [**ExpandVirtualDisk**](/windows/win32/api/virtdisk/nf-virtdisk-expandvirtualdisk).</span></span>
    <span data-ttu-id="e3453-137">**Nota**  Le dimensioni massime di un disco virtuale dinamico sono di 2.040 GB.</span><span class="sxs-lookup"><span data-stu-id="e3453-137">**Note**  The maximum size of a dynamic virtual disk is 2,040 GB.</span></span>

     

-   <span data-ttu-id="e3453-138">**Differenze: un** disco virtuale padre viene utilizzato come base di questo tipo, con tutte le scritture successive scritte nel disco virtuale come differenze rispetto al nuovo file di immagine del disco rigido virtuale differenze e il file di immagine VHD padre non viene modificato.</span><span class="sxs-lookup"><span data-stu-id="e3453-138">**Differencing**—A parent virtual disk is used as the basis of this type, with any subsequent writes written to the virtual disk as differences to the new differencing VHD image file, and the parent VHD image file is not modified.</span></span> <span data-ttu-id="e3453-139">Ad esempio, se si dispone di un disco virtuale del sistema operativo di avvio del sistema con installazione pulita come padre e si designa il disco virtuale differenze come disco virtuale corrente per il sistema, il sistema operativo del disco virtuale padre rimane nello stato originale per il ripristino rapido o per creare rapidamente altre immagini di avvio basate su dischi virtuali differenze aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="e3453-139">For example, if you have a clean-install system boot operating system virtual disk as a parent and designate the differencing virtual disk as the current virtual disk for the system to use, then the operating system on the parent virtual disk stays in its original state for quick recovery or for quickly creating more boot images based on additional differencing virtual disks.</span></span> <span data-ttu-id="e3453-140">Per ulteriori informazioni, vedere [**MergeVirtualDisk**](/windows/win32/api/virtdisk/nf-virtdisk-mergevirtualdisk).</span><span class="sxs-lookup"><span data-stu-id="e3453-140">For more information, see [**MergeVirtualDisk**](/windows/win32/api/virtdisk/nf-virtdisk-mergevirtualdisk).</span></span>
    <span data-ttu-id="e3453-141">**Nota**  Le dimensioni massime di un disco virtuale differenze sono di 2.040 GB.</span><span class="sxs-lookup"><span data-stu-id="e3453-141">**Note**  The maximum size of a differencing virtual disk is 2,040 GB.</span></span>

     

<span data-ttu-id="e3453-142">Tutti i tipi di dischi virtuali hanno una dimensione minima di 3 MB.</span><span class="sxs-lookup"><span data-stu-id="e3453-142">All virtual disk types have a minimum size of 3 MB.</span></span>

## <a name="span-idrelated_topicsspanrelated-topics"></a><span data-ttu-id="e3453-143"><span id="related_topics"></span>Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e3453-143"><span id="related_topics"></span>Related topics</span></span>

[<span data-ttu-id="e3453-144">Informazioni su VDS</span><span class="sxs-lookup"><span data-stu-id="e3453-144">About VDS</span></span>](/windows/desktop/VDS/about-vds)

[<span data-ttu-id="e3453-145">Riferimento al disco rigido virtuale</span><span class="sxs-lookup"><span data-stu-id="e3453-145">VHD Reference</span></span>](vhd-reference.md)

[<span data-ttu-id="e3453-146">Specifica del formato immagine del disco rigido virtuale</span><span class="sxs-lookup"><span data-stu-id="e3453-146">Virtual Hard Disk Image Format Specification</span></span>](https://download.microsoft.com/download/f/f/e/ffef50a5-07dd-4cf8-aaa3-442c0673a029/Virtual%20Hard%20Disk%20Format%20Spec_10_18_06.doc)

 

 
