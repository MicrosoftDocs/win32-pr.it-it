---
description: Per generare un pacchetto di patch, è consigliabile utilizzare uno strumento per la creazione di patch, ad esempio Msimsp.exe e Patchwiz.dll.
ms.assetid: aca3bbd2-440a-405f-bddc-5f9cc831b811
title: Patchwiz.dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6dc1135a9e2c09bb8a96e041f77bae39f0057ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234025"
---
# <a name="patchwizdll"></a><span data-ttu-id="297f0-103">Patchwiz.dll</span><span class="sxs-lookup"><span data-stu-id="297f0-103">Patchwiz.dll</span></span>

<span data-ttu-id="297f0-104">Per generare un pacchetto di patch, è consigliabile utilizzare uno strumento per la creazione di patch, ad esempio [Msimsp.exe](msimsp-exe.md) e Patchwiz.dll.</span><span class="sxs-lookup"><span data-stu-id="297f0-104">To generate a patch package, it is recommended that you use a patch creation tool such as [Msimsp.exe](msimsp-exe.md) and Patchwiz.dll.</span></span> <span data-ttu-id="297f0-105">Patchwiz.dll versione 4,0 è compatibile con i pacchetti e le patch creati usando le versioni precedenti del Patchwiz.dll.</span><span class="sxs-lookup"><span data-stu-id="297f0-105">Patchwiz.dll version 4.0 is compatible with packages and patches that were authored using earlier versions of the Patchwiz.dll.</span></span> <span data-ttu-id="297f0-106">Lo strumento Patchwiz.dll è disponibile solo nei [componenti Windows SDK per Windows Installer sviluppatori](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="297f0-106">The Patchwiz.dll tool is only available in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

<span data-ttu-id="297f0-107">Patchwiz.dll versione 4,0 include una nuova funzione, [UiCreatePatchPackageEx (Patchwiz.dll)](uicreatepatchpackageex--patchwiz-dll-.md), che estende la funzionalità di [UiCreatePatchPackage (Patchwiz.dll)](uicreatepatchpackage-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="297f0-107">Patchwiz.dll version 4.0 has one new function, [UiCreatePatchPackageEx (Patchwiz.dll)](uicreatepatchpackageex--patchwiz-dll-.md), that extends the functionality of [UiCreatePatchPackage (Patchwiz.dll)](uicreatepatchpackage-patchwiz-dll-.md).</span></span> <span data-ttu-id="297f0-108">Queste funzioni accettano un file delle proprietà di creazione della patch (file con estensione PCP) e generano un [pacchetto di patch](patch-packages.md)del programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="297f0-108">These functions take a patch creation properties file (.pcp file) and generate an installer [Patch Package](patch-packages.md).</span></span>

<span data-ttu-id="297f0-109">Il file con estensione PCP è un file di database binario con lo stesso formato di un database di Windows Installer (file con estensione msi), ma con uno schema di database diverso.</span><span class="sxs-lookup"><span data-stu-id="297f0-109">The .pcp file is a binary database file with the same format as a Windows Installer database (.msi file), but with a different database schema.</span></span> <span data-ttu-id="297f0-110">È pertanto possibile creare un file con estensione PCP utilizzando gli stessi strumenti utilizzati per un database del programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="297f0-110">Therefore a .pcp file can be authored by using the same tools used for an installer database.</span></span>

<span data-ttu-id="297f0-111">È possibile creare un file con estensione PCP usando un editor di tabelle, ad esempio [Orca.exe](orca-exe.md) per immettere le informazioni nel database vuoto. PCP fornito con Windows Installer SDK, template. PCP.</span><span class="sxs-lookup"><span data-stu-id="297f0-111">You can create a .pcp file by using a table editor such as [Orca.exe](orca-exe.md) to enter information into the blank .pcp database provided with the Windows Installer SDK, Template.pcp.</span></span> <span data-ttu-id="297f0-112">Per ulteriori informazioni, vedere [un esempio di patch per l'aggiornamento di piccole dimensioni](a-small-update-patching-example.md).</span><span class="sxs-lookup"><span data-stu-id="297f0-112">For more information, see [A Small Update Patching Example](a-small-update-patching-example.md).</span></span>

<span data-ttu-id="297f0-113">Le tabelle di database seguenti sono necessarie in ogni file. PCP:</span><span class="sxs-lookup"><span data-stu-id="297f0-113">The following database tables are required in every .pcp file:</span></span>

-   [<span data-ttu-id="297f0-114">Tabella Properties (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="297f0-114">Properties Table (Patchwiz.dll)</span></span>](properties-table-patchwiz-dll-.md)
-   [<span data-ttu-id="297f0-115">Tabella ImageFamilies (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="297f0-115">ImageFamilies Table (Patchwiz.dll)</span></span>](imagefamilies-table-patchwiz-dll-.md)
-   [<span data-ttu-id="297f0-116">Tabella UpgradedImages (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="297f0-116">UpgradedImages Table (Patchwiz.dll)</span></span>](upgradedimages-table-patchwiz-dll-.md)
-   [<span data-ttu-id="297f0-117">Tabella TargetImages (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="297f0-117">TargetImages Table (Patchwiz.dll)</span></span>](targetimages-table-patchwiz-dll-.md)

<span data-ttu-id="297f0-118">Le tabelle di database seguenti sono facoltative:</span><span class="sxs-lookup"><span data-stu-id="297f0-118">The following database tables are optional:</span></span>

-   [<span data-ttu-id="297f0-119">\_Tabella UpgradedFiles OptionalData (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="297f0-119">UpgradedFiles\_OptionalData Table (Patchwiz.dll)</span></span>](upgradedfiles-optionaldata-table-patchwiz-dll-.md)
-   [<span data-ttu-id="297f0-120">Tabella FamilyFileRanges (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="297f0-120">FamilyFileRanges Table (Patchwiz.dll)</span></span>](familyfileranges-table-patchwiz-dll-.md)
-   [<span data-ttu-id="297f0-121">\_Tabella TargetFiles OptionalData (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="297f0-121">TargetFiles\_OptionalData Table (Patchwiz.dll)</span></span>](targetfiles-optionaldata-table-patchwiz-dll-.md)
-   [<span data-ttu-id="297f0-122">Tabella ExternalFiles (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="297f0-122">ExternalFiles Table (Patchwiz.dll)</span></span>](externalfiles-table-patchwiz-dll-.md)
-   [<span data-ttu-id="297f0-123">Tabella UpgradedFilesToIgnore (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="297f0-123">UpgradedFilesToIgnore Table (Patchwiz.dll)</span></span>](upgradedfilestoignore-table-patchwiz-dll-.md)

<span data-ttu-id="297f0-124">La tabella seguente è obbligatoria nei file. PCP con MinimumRequiredMsiVersion uguale a 300 nella tabella [Properties](properties-table-patchwiz-dll-.md) .</span><span class="sxs-lookup"><span data-stu-id="297f0-124">The following table is required in .pcp files that have a MinimumRequiredMsiVersion equal to 300 in the [Properties](properties-table-patchwiz-dll-.md) table.</span></span>

-   [<span data-ttu-id="297f0-125">Tabella PatchMetadata (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="297f0-125">PatchMetadata Table (Patchwiz.dll)</span></span>](patchmetadata-table--patchwiz-dll-.md)

> [!Note]  
> <span data-ttu-id="297f0-126">La tabella è facoltativa se MinimumRequiredMsiVersion non è uguale a 300.</span><span class="sxs-lookup"><span data-stu-id="297f0-126">The table is optional if MinimumRequiredMsiVersion is not equal to 300.</span></span>

 

<span data-ttu-id="297f0-127">La versione di Patchwiz.dll rilasciata con Windows Installer 3,0 è in grado di generare automaticamente informazioni di sequenziazione delle patch e di aggiungerle alla [tabella MsiPatchSequence](msipatchsequence-table.md) di una nuova patch.</span><span class="sxs-lookup"><span data-stu-id="297f0-127">The version of Patchwiz.dll released with Windows Installer 3.0 can automatically generate patch sequencing information and add it to the [MsiPatchSequence Table](msipatchsequence-table.md) of a new patch.</span></span> <span data-ttu-id="297f0-128">La [tabella PatchSequence](patchsequence-table--patchwiz-dll-.md) può essere utilizzata per aggiungere manualmente le informazioni di sequenziazione della patch alla tabella MsiPatchSequence.</span><span class="sxs-lookup"><span data-stu-id="297f0-128">The [PatchSequence Table](patchsequence-table--patchwiz-dll-.md) can be used to manually add patch sequencing information the MsiPatchSequence Table.</span></span> <span data-ttu-id="297f0-129">Per ulteriori informazioni, vedere [generazione di informazioni sulla sequenza di patch](generating-patch-sequence-information---patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="297f0-129">For more information, see [Generating Patch Sequence Information](generating-patch-sequence-information---patchwiz-dll-.md).</span></span>

<span data-ttu-id="297f0-130">A partire da Patchwiz.dll versione 2,0, è possibile aumentare la velocità della creazione di patch successiva usando [patch Information Caching (Patchwiz.dll)](patch-information-caching-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="297f0-130">Beginning with Patchwiz.dll version 2.0, you can increase the speed of subsequent patch creation by using [Patch Information Caching (Patchwiz.dll)](patch-information-caching-patchwiz-dll-.md).</span></span>

<span data-ttu-id="297f0-131">L'uso di simboli pubblici per i file binari di destinazione e di aggiornamento delle immagini può ridurre le dimensioni di una dimensione di circa una metà.</span><span class="sxs-lookup"><span data-stu-id="297f0-131">Using public symbols for your target and upgrade image binaries can reduce binary patch sizes by approximately one half.</span></span> <span data-ttu-id="297f0-132">Per ulteriori informazioni, vedere [utilizzo di simboli per ridurre le dimensioni della patch binaria](using-symbols-to-reduce-binary-patch-size.md).</span><span class="sxs-lookup"><span data-stu-id="297f0-132">For more information, see [Using Symbols to Reduce Binary Patch Size](using-symbols-to-reduce-binary-patch-size.md).</span></span>

<span data-ttu-id="297f0-133">È possibile specificare che alcune aree del file di destinazione vengano mantenute da sovrascrivere durante l'applicazione di patch e che le informazioni contenute in tali aree vengano mantenute.</span><span class="sxs-lookup"><span data-stu-id="297f0-133">You can specify that certain regions of the target file be preserved from being overwritten during patching and that the information in those regions be retained.</span></span> <span data-ttu-id="297f0-134">Per ulteriori informazioni, vedere applicazione [di patch alle aree selezionate di un file](patching-selected-regions-of-a-file.md).</span><span class="sxs-lookup"><span data-stu-id="297f0-134">For more information, see [Patching Selected Regions of a File](patching-selected-regions-of-a-file.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="297f0-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="297f0-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="297f0-136">Versioni rilasciate, strumenti e ridistribuibili</span><span class="sxs-lookup"><span data-stu-id="297f0-136">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



