---
description: Per riprodurre il pacchetto di patch di esempio, è necessario uno strumento software in grado di creare e modificare un pacchetto di patch Windows Installer.
ms.assetid: 0653d8f6-89b0-4c56-ae51-3c7cb7df2909
title: Creazione di un file delle proprietà di creazione patch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2775f8521731b43264df315ae05a874e37dd3ffc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319439"
---
# <a name="creating-a-patch-creation-properties-file"></a><span data-ttu-id="fbdef-103">Creazione di un file delle proprietà di creazione patch</span><span class="sxs-lookup"><span data-stu-id="fbdef-103">Creating a Patch Creation Properties File</span></span>

<span data-ttu-id="fbdef-104">Per riprodurre il pacchetto di patch di esempio, è necessario uno strumento software in grado di creare e modificare un pacchetto di patch Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="fbdef-104">To reproduce the sample patch package, you need a software tool capable of creating and editing a Windows Installer patch package.</span></span> <span data-ttu-id="fbdef-105">Sono disponibili diversi strumenti per la creazione di pacchetti di patch da fornitori di software indipendenti.</span><span class="sxs-lookup"><span data-stu-id="fbdef-105">Several patch package creation tools are available from independent software vendors.</span></span> <span data-ttu-id="fbdef-106">Nell'esempio descritto nelle sezioni seguenti viene usato un editor di database Windows Installer denominato ORCA per creare un file delle proprietà di creazione patch (estensione PCP).</span><span class="sxs-lookup"><span data-stu-id="fbdef-106">The example discussed in the following sections uses a Windows Installer database editor called Orca to author a patch creation properties file (.pcp extension).</span></span> <span data-ttu-id="fbdef-107">Il file. PCP può essere usato con le utilità [Msimsp.exe](msimsp-exe.md) e [Patchwiz.dll](patchwiz-dll.md) per generare un pacchetto di patch Windows Installer (estensione msp).</span><span class="sxs-lookup"><span data-stu-id="fbdef-107">The .pcp file may be used with the utilities [Msimsp.exe](msimsp-exe.md) and [Patchwiz.dll](patchwiz-dll.md) to generate a Windows Installer patch package (.msp extension).</span></span> <span data-ttu-id="fbdef-108">Orca, Msimsp.exe e Patchwiz.dll sono disponibili nei [componenti di Windows SDK per gli sviluppatori Windows Installer](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="fbdef-108">Orca, Msimsp.exe, and Patchwiz.dll are provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

<span data-ttu-id="fbdef-109">Con l'SDK viene fornito anche un file di proprietà di creazione patch vuota, template. PCP.</span><span class="sxs-lookup"><span data-stu-id="fbdef-109">A blank patch creation properties file, template.pcp, is also provided with the SDK.</span></span> <span data-ttu-id="fbdef-110">Creare una copia di template. PCP e rinominare la copia MNP2000. PCP.</span><span class="sxs-lookup"><span data-stu-id="fbdef-110">Make a copy of template.pcp and rename this copy MNP2000.pcp.</span></span> <span data-ttu-id="fbdef-111">Utilizzare Orca o un altro editor di database per immettere i dati seguenti nella tabella Properties di MNP2000. PCP.</span><span class="sxs-lookup"><span data-stu-id="fbdef-111">Use Orca or another database editor to enter the following data into the Properties table of MNP2000.pcp.</span></span> <span data-ttu-id="fbdef-112">La tabella Properties contiene le impostazioni globali per il pacchetto di patch.</span><span class="sxs-lookup"><span data-stu-id="fbdef-112">The Properties table contains global settings for the patch package.</span></span>

[<span data-ttu-id="fbdef-113">Tabella delle proprietà</span><span class="sxs-lookup"><span data-stu-id="fbdef-113">Properties Table</span></span>](properties-table-patchwiz-dll-.md)



| <span data-ttu-id="fbdef-114">Nome</span><span class="sxs-lookup"><span data-stu-id="fbdef-114">Name</span></span>                               | <span data-ttu-id="fbdef-115">Valore</span><span class="sxs-lookup"><span data-stu-id="fbdef-115">Value</span></span>                                  |
|------------------------------------|----------------------------------------|
| <span data-ttu-id="fbdef-116">AllowProductCodeMismatches</span><span class="sxs-lookup"><span data-stu-id="fbdef-116">AllowProductCodeMismatches</span></span>         | <span data-ttu-id="fbdef-117">1</span><span class="sxs-lookup"><span data-stu-id="fbdef-117">1</span></span>                                      |
| <span data-ttu-id="fbdef-118">AllowProductVersionMajorMismatches</span><span class="sxs-lookup"><span data-stu-id="fbdef-118">AllowProductVersionMajorMismatches</span></span> | <span data-ttu-id="fbdef-119">1</span><span class="sxs-lookup"><span data-stu-id="fbdef-119">1</span></span>                                      |
| <span data-ttu-id="fbdef-120">ApiPatchingSymbolFlags</span><span class="sxs-lookup"><span data-stu-id="fbdef-120">ApiPatchingSymbolFlags</span></span>             | <span data-ttu-id="fbdef-121">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fbdef-121">0x00000000</span></span>                             |
| <span data-ttu-id="fbdef-122">DontRemoveTempFolderWhenFinished</span><span class="sxs-lookup"><span data-stu-id="fbdef-122">DontRemoveTempFolderWhenFinished</span></span>   | <span data-ttu-id="fbdef-123">1</span><span class="sxs-lookup"><span data-stu-id="fbdef-123">1</span></span>                                      |
| <span data-ttu-id="fbdef-124">IncludeWholeFilesOnly</span><span class="sxs-lookup"><span data-stu-id="fbdef-124">IncludeWholeFilesOnly</span></span>              | <span data-ttu-id="fbdef-125">0</span><span class="sxs-lookup"><span data-stu-id="fbdef-125">0</span></span>                                      |
| <span data-ttu-id="fbdef-126">ListOfPatchGUIDsToReplace</span><span class="sxs-lookup"><span data-stu-id="fbdef-126">ListOfPatchGUIDsToReplace</span></span>          |                                        |
| <span data-ttu-id="fbdef-127">ListOfTargetProductCodes</span><span class="sxs-lookup"><span data-stu-id="fbdef-127">ListOfTargetProductCodes</span></span>           | \*                                     |
| <span data-ttu-id="fbdef-128">PatchGUID</span><span class="sxs-lookup"><span data-stu-id="fbdef-128">PatchGUID</span></span>                          | <span data-ttu-id="fbdef-129">{5406B219-A1AC-4BC4-8695-72292C8195AC}</span><span class="sxs-lookup"><span data-stu-id="fbdef-129">{5406B219-A1AC-4BC4-8695-72292C8195AC}</span></span> |
| <span data-ttu-id="fbdef-130">PatchOutputPath</span><span class="sxs-lookup"><span data-stu-id="fbdef-130">PatchOutputPath</span></span>                    | <span data-ttu-id="fbdef-131">c: \\ output. msp</span><span class="sxs-lookup"><span data-stu-id="fbdef-131">c:\\output.msp</span></span>                         |
| <span data-ttu-id="fbdef-132">PatchSourceList</span><span class="sxs-lookup"><span data-stu-id="fbdef-132">PatchSourceList</span></span>                    | <span data-ttu-id="fbdef-133">PatchSourceList</span><span class="sxs-lookup"><span data-stu-id="fbdef-133">PatchSourceList</span></span>                        |



 

<span data-ttu-id="fbdef-134">Utilizzare l'editor di database per immettere i dati seguenti nella tabella ImageFamilies di MNP2000. PCP.</span><span class="sxs-lookup"><span data-stu-id="fbdef-134">Use the database editor to enter the following data into the ImageFamilies table of MNP2000.pcp.</span></span> <span data-ttu-id="fbdef-135">La tabella ImageFamilies contiene informazioni da aggiungere alla [tabella media](media-table.md) durante l'applicazione di patch.</span><span class="sxs-lookup"><span data-stu-id="fbdef-135">The ImageFamilies table contains information to be added to the [Media table](media-table.md) during patching.</span></span>

[<span data-ttu-id="fbdef-136">Tabella ImageFamilies</span><span class="sxs-lookup"><span data-stu-id="fbdef-136">ImageFamilies Table</span></span>](imagefamilies-table-patchwiz-dll-.md)



| <span data-ttu-id="fbdef-137">Famiglia</span><span class="sxs-lookup"><span data-stu-id="fbdef-137">Family</span></span>  | <span data-ttu-id="fbdef-138">MediaSrcPropName</span><span class="sxs-lookup"><span data-stu-id="fbdef-138">MediaSrcPropName</span></span> | <span data-ttu-id="fbdef-139">MediaDiskId</span><span class="sxs-lookup"><span data-stu-id="fbdef-139">MediaDiskId</span></span> | <span data-ttu-id="fbdef-140">FileSequenceStart</span><span class="sxs-lookup"><span data-stu-id="fbdef-140">FileSequenceStart</span></span> | <span data-ttu-id="fbdef-141">DiskPrompt</span><span class="sxs-lookup"><span data-stu-id="fbdef-141">DiskPrompt</span></span> | <span data-ttu-id="fbdef-142">VolumeLabel</span><span class="sxs-lookup"><span data-stu-id="fbdef-142">VolumeLabel</span></span> |
|---------|------------------|-------------|-------------------|------------|-------------|
| <span data-ttu-id="fbdef-143">MNPapps</span><span class="sxs-lookup"><span data-stu-id="fbdef-143">MNPapps</span></span> | <span data-ttu-id="fbdef-144">MNPSrcPropName</span><span class="sxs-lookup"><span data-stu-id="fbdef-144">MNPSrcPropName</span></span>   | <span data-ttu-id="fbdef-145">2</span><span class="sxs-lookup"><span data-stu-id="fbdef-145">2</span></span>           | <span data-ttu-id="fbdef-146">1000</span><span class="sxs-lookup"><span data-stu-id="fbdef-146">1000</span></span>              |            |             |



 

<span data-ttu-id="fbdef-147">Immettere i dati seguenti nella tabella UpgradedImages di MNP2000. PCP.</span><span class="sxs-lookup"><span data-stu-id="fbdef-147">Enter the following data into the UpgradedImages table of MNP2000.pcp.</span></span> <span data-ttu-id="fbdef-148">La tabella UpgradedImages contiene informazioni sull'immagine aggiornata creata durante la [pianificazione di una patch di aggiornamento di piccole dimensioni](planning-a-small-update-patch.md).</span><span class="sxs-lookup"><span data-stu-id="fbdef-148">The UpgradedImages table contains information about the Upgraded image you created in [Planning a Small Update Patch](planning-a-small-update-patch.md).</span></span>

[<span data-ttu-id="fbdef-149">Tabella UpgradedImages</span><span class="sxs-lookup"><span data-stu-id="fbdef-149">UpgradedImages Table</span></span>](upgradedimages-table-patchwiz-dll-.md)



| <span data-ttu-id="fbdef-150">Aggiornato</span><span class="sxs-lookup"><span data-stu-id="fbdef-150">Upgraded</span></span>   | <span data-ttu-id="fbdef-151">PercorsoMSI</span><span class="sxs-lookup"><span data-stu-id="fbdef-151">MsiPath</span></span>                                           | <span data-ttu-id="fbdef-152">PatchMsiPath</span><span class="sxs-lookup"><span data-stu-id="fbdef-152">PatchMsiPath</span></span> | <span data-ttu-id="fbdef-153">SymbolPaths</span><span class="sxs-lookup"><span data-stu-id="fbdef-153">SymbolPaths</span></span> | <span data-ttu-id="fbdef-154">Famiglia</span><span class="sxs-lookup"><span data-stu-id="fbdef-154">Family</span></span>  |
|------------|---------------------------------------------------|--------------|-------------|---------|
| <span data-ttu-id="fbdef-155">MNP \_ fisso</span><span class="sxs-lookup"><span data-stu-id="fbdef-155">MNP\_fixed</span></span> | <span data-ttu-id="fbdef-156">C: \\ Nota \_ patch del programma di installazione \\ \\ aggiornata \\MNP2000.msi</span><span class="sxs-lookup"><span data-stu-id="fbdef-156">C:\\Note\_Installer\\Patch\\Upgraded\\MNP2000.msi</span></span> |              |             | <span data-ttu-id="fbdef-157">MNPapps</span><span class="sxs-lookup"><span data-stu-id="fbdef-157">MNPapps</span></span> |



 

<span data-ttu-id="fbdef-158">Immettere i dati seguenti nella tabella TargetImages di MNP2000. PCP.</span><span class="sxs-lookup"><span data-stu-id="fbdef-158">Enter the following data into the TargetImages table of MNP2000.pcp.</span></span> <span data-ttu-id="fbdef-159">La tabella TargetImages contiene informazioni sull'immagine di destinazione.</span><span class="sxs-lookup"><span data-stu-id="fbdef-159">The TargetImages table contains information about the Target image.</span></span>

[<span data-ttu-id="fbdef-160">Tabella TargetImages</span><span class="sxs-lookup"><span data-stu-id="fbdef-160">TargetImages Table</span></span>](targetimages-table-patchwiz-dll-.md)



| <span data-ttu-id="fbdef-161">Destinazione</span><span class="sxs-lookup"><span data-stu-id="fbdef-161">Target</span></span>     | <span data-ttu-id="fbdef-162">PercorsoMSI</span><span class="sxs-lookup"><span data-stu-id="fbdef-162">MsiPath</span></span>                                         | <span data-ttu-id="fbdef-163">SymbolPaths</span><span class="sxs-lookup"><span data-stu-id="fbdef-163">SymbolPaths</span></span> | <span data-ttu-id="fbdef-164">Aggiornato</span><span class="sxs-lookup"><span data-stu-id="fbdef-164">Upgraded</span></span>   | <span data-ttu-id="fbdef-165">JSON</span><span class="sxs-lookup"><span data-stu-id="fbdef-165">Order</span></span> | <span data-ttu-id="fbdef-166">ProductValidateFlags</span><span class="sxs-lookup"><span data-stu-id="fbdef-166">ProductValidateFlags</span></span> | <span data-ttu-id="fbdef-167">IgnoreMissingSrcFiles</span><span class="sxs-lookup"><span data-stu-id="fbdef-167">IgnoreMissingSrcFiles</span></span> |
|------------|-------------------------------------------------|-------------|------------|-------|----------------------|-----------------------|
| <span data-ttu-id="fbdef-168">\_Errore MNP</span><span class="sxs-lookup"><span data-stu-id="fbdef-168">MNP\_error</span></span> | <span data-ttu-id="fbdef-169">C: \\ Nota la \_ destinazione della patch del programma di installazione \\ \\ \\MNP2000.msi</span><span class="sxs-lookup"><span data-stu-id="fbdef-169">C:\\Note\_Installer\\Patch\\Target\\MNP2000.msi</span></span> |             | <span data-ttu-id="fbdef-170">MNP \_ fisso</span><span class="sxs-lookup"><span data-stu-id="fbdef-170">MNP\_fixed</span></span> | <span data-ttu-id="fbdef-171">1</span><span class="sxs-lookup"><span data-stu-id="fbdef-171">1</span></span>     |                      | <span data-ttu-id="fbdef-172">0</span><span class="sxs-lookup"><span data-stu-id="fbdef-172">0</span></span>                     |



 

<span data-ttu-id="fbdef-173">Per il pacchetto di patch di esempio, lasciare vuote le seguenti tabelle in MNP2000. PCP.</span><span class="sxs-lookup"><span data-stu-id="fbdef-173">For the sample patch package, leave the following tables in MNP2000.pcp blank.</span></span>

[<span data-ttu-id="fbdef-174">\_Tabella UpgradedFiles OptionalData</span><span class="sxs-lookup"><span data-stu-id="fbdef-174">UpgradedFiles\_OptionalData Table</span></span>](upgradedfiles-optionaldata-table-patchwiz-dll-.md)

[<span data-ttu-id="fbdef-175">Tabella FamilyFileRanges</span><span class="sxs-lookup"><span data-stu-id="fbdef-175">FamilyFileRanges Table</span></span>](familyfileranges-table-patchwiz-dll-.md)

[<span data-ttu-id="fbdef-176">\_Tabella TargetFiles OptionalData</span><span class="sxs-lookup"><span data-stu-id="fbdef-176">TargetFiles\_OptionalData Table</span></span>](targetfiles-optionaldata-table-patchwiz-dll-.md)

[<span data-ttu-id="fbdef-177">Tabella ExternalFiles</span><span class="sxs-lookup"><span data-stu-id="fbdef-177">ExternalFiles Table</span></span>](externalfiles-table-patchwiz-dll-.md)

[<span data-ttu-id="fbdef-178">Tabella UpgradedFilesToIgnore</span><span class="sxs-lookup"><span data-stu-id="fbdef-178">UpgradedFilesToIgnore Table</span></span>](upgradedfilestoignore-table-patchwiz-dll-.md)

[<span data-ttu-id="fbdef-179">Continua</span><span class="sxs-lookup"><span data-stu-id="fbdef-179">Continue</span></span>](generating-a-patch-package.md)

 

 



