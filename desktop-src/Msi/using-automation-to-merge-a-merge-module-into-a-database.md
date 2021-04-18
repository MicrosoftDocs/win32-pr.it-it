---
description: I moduli unione forniscono un metodo standard per la distribuzione di componenti di Windows Installer condivisi e l'impostazione della logica per le applicazioni.
ms.assetid: 63ced106-12e3-4483-8bfe-22c54fe7a204
title: Utilizzo dell'automazione per unire un modulo merge in un database
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3e28b8cfc1716cdbb296fd0a1410787ae55bb62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308668"
---
# <a name="using-automation-to-merge-a-merge-module-into-a-database"></a><span data-ttu-id="770c2-103">Utilizzo dell'automazione per unire un modulo merge in un database</span><span class="sxs-lookup"><span data-stu-id="770c2-103">Using Automation to Merge a Merge Module into a Database</span></span>

<span data-ttu-id="770c2-104">I [moduli unione](merge-modules.md) forniscono un metodo standard per la distribuzione di [*componenti*](c-gly.md)di Windows Installer condivisi e l'impostazione della logica per le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="770c2-104">[Merge Modules](merge-modules.md) provide a standard method for you to deliver shared Windows Installer [*components*](c-gly.md), and setup logic to applications.</span></span>

<span data-ttu-id="770c2-105">I moduli merge devono essere Uniti in un pacchetto di installazione usando uno strumento di merge.</span><span class="sxs-lookup"><span data-stu-id="770c2-105">Merge modules must be merged into an installation package by using a merge tool.</span></span> <span data-ttu-id="770c2-106">La procedura consigliata consiste nell'ottenere uno strumento di merge distribuito liberamente oppure acquistare uno degli strumenti di merge disponibili da fornitori di software indipendenti. ad esempio, è possibile utilizzare [Mergemod.dll](merge-module-automation.md).</span><span class="sxs-lookup"><span data-stu-id="770c2-106">The best practice is to obtain a freely distributed merge tool, or purchase one of the merge tools that are available from independent software vendors, for example, you can use [Mergemod.dll](merge-module-automation.md).</span></span>

<span data-ttu-id="770c2-107">Nella procedura riportata di seguito viene illustrato come unire un modulo merge in un database Windows Installer utilizzando l' [automazione del modulo merge](merge-module-automation.md).</span><span class="sxs-lookup"><span data-stu-id="770c2-107">The following procedure shows you how to merge a merge module into a Windows Installer database by using [Merge Module Automation](merge-module-automation.md).</span></span>

<span data-ttu-id="770c2-108">**Per unire un modulo in un database**</span><span class="sxs-lookup"><span data-stu-id="770c2-108">**To merge a module into a database**</span></span>

1.  <span data-ttu-id="770c2-109">Aprire un file di log usando il metodo [**OpenLog**](merge-openlog.md) .</span><span class="sxs-lookup"><span data-stu-id="770c2-109">Open a log file by using the [**OpenLog**](merge-openlog.md) method.</span></span>

    <span data-ttu-id="770c2-110">Questo passaggio è necessario solo se è necessario creare un file di log o accodare un file di log esistente per il processo di merge.</span><span class="sxs-lookup"><span data-stu-id="770c2-110">This step is required only if you need to create a log file, or append an existing log file for the merge process.</span></span>

2.  <span data-ttu-id="770c2-111">Aprire il database di installazione con [estensione msi](windows-installer-file-extensions.md) utilizzando il metodo [**OpenDatabase**](merge-opendatabase.md) dell' [**oggetto merge**](merge-object.md).</span><span class="sxs-lookup"><span data-stu-id="770c2-111">Open the [.msi](windows-installer-file-extensions.md) installation database by using the [**OpenDatabase**](merge-opendatabase.md) method of the [**Merge Object**](merge-object.md).</span></span>

    <span data-ttu-id="770c2-112">Questo passaggio è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="770c2-112">This step is required.</span></span>

    <span data-ttu-id="770c2-113">Il database aperto è quello che si desidera ricevere per il modulo unione.</span><span class="sxs-lookup"><span data-stu-id="770c2-113">The database that you open is the one that you want to receive the merge module.</span></span>

3.  <span data-ttu-id="770c2-114">Aprire il modulo merge con [estensione MSM](windows-installer-file-extensions.md) usando il metodo [**ApriModulo**](merge-openmodule.md) .</span><span class="sxs-lookup"><span data-stu-id="770c2-114">Open the [.msm](windows-installer-file-extensions.md) merge module by using the [**OpenModule**](merge-openmodule.md) method.</span></span>

    <span data-ttu-id="770c2-115">Questo passaggio è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="770c2-115">This step is required.</span></span>

    <span data-ttu-id="770c2-116">Si tratta del modulo merge che viene unito nel database.</span><span class="sxs-lookup"><span data-stu-id="770c2-116">This is the merge module that is being merged into the database.</span></span> <span data-ttu-id="770c2-117">Prima di poter eseguire il merge di un modulo con un database di installazione, è necessario aprirlo.</span><span class="sxs-lookup"><span data-stu-id="770c2-117">A module must be opened before it can be merged with an installation database.</span></span>

4.  <span data-ttu-id="770c2-118">Unire il modulo nel database di installazione chiamando il metodo [**merge**](merge-object.md) o il metodo [**MergeEx**](merge-mergeex.md) .</span><span class="sxs-lookup"><span data-stu-id="770c2-118">Merge the module into the installation database by calling the [**Merge**](merge-object.md) method or [**MergeEx**](merge-mergeex.md) method.</span></span>

    <span data-ttu-id="770c2-119">Questo passaggio è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="770c2-119">This step is required.</span></span>

    <span data-ttu-id="770c2-120">Il metodo [**merge**](merge-object.md) o il metodo [**MergeEx**](merge-mergeex.md) può essere chiamato una sola volta per unire una combinazione specifica di file con [estensione msi](windows-installer-file-extensions.md) e MSM.</span><span class="sxs-lookup"><span data-stu-id="770c2-120">The [**Merge**](merge-object.md) method or [**MergeEx**](merge-mergeex.md) method can only be called one time to merge a specific combination of [.msi](windows-installer-file-extensions.md) and .msm files.</span></span>

    > [!Note]  
    > <span data-ttu-id="770c2-121">Il metodo [**MergeEx**](merge-mergeex.md) è disponibile solo in [Mergemod.dll versione 2,0](merge-module-automation.md) o successiva e solo quando si usa l'interfaccia [**IMsmMerge2**](/windows/desktop/api/Mergemod/nn-mergemod-imsmmerge2) .</span><span class="sxs-lookup"><span data-stu-id="770c2-121">The [**MergeEx**](merge-mergeex.md) method is only available in [Mergemod.dll version 2.0](merge-module-automation.md) or later, and only when using the [**IMsmMerge2**](/windows/desktop/api/Mergemod/nn-mergemod-imsmmerge2) interface.</span></span>

     

5.  <span data-ttu-id="770c2-122">Recuperare la proprietà Errors ed esaminare la raccolta di oggetti [**Error**](error-object.md) restituiti [**per i conflitti**](merge-errors.md) di merge o altri errori.</span><span class="sxs-lookup"><span data-stu-id="770c2-122">Retrieve the [**Errors**](merge-errors.md) property and examine the collection of [**Error**](error-object.md) objects it returns for merge conflicts or other errors.</span></span>

    <span data-ttu-id="770c2-123">È necessario risolvere gli eventuali errori.</span><span class="sxs-lookup"><span data-stu-id="770c2-123">You must resolve any errors.</span></span>

    <span data-ttu-id="770c2-124">Il recupero non è distruttivo e più istanze della raccolta errori possono essere recuperate leggendo ripetutamente la proprietà [**Errors**](merge-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="770c2-124">The retrieval is nondestructive, and multiple instances of the error collection can be retrieved by repeatedly reading the [**Errors**](merge-errors.md) property.</span></span>

6.  <span data-ttu-id="770c2-125">Associare i componenti del modulo merge alle funzionalità usando il metodo [**Connect**](merge-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="770c2-125">Associate the components of the merge module with the features by using the [**Connect**](merge-connect.md) method.</span></span>

    <span data-ttu-id="770c2-126">Questo passaggio è necessario solo se si dispone di funzionalità esistenti e si desidera aggiungere funzionalità da unire nel database di installazione.</span><span class="sxs-lookup"><span data-stu-id="770c2-126">This step is only required if you have existing features and you want to add features to merge into the installation database.</span></span>

    <span data-ttu-id="770c2-127">È necessario che esista una funzionalità prima di chiamare questo metodo.</span><span class="sxs-lookup"><span data-stu-id="770c2-127">A feature must exist before you call this method.</span></span> <span data-ttu-id="770c2-128">Per ulteriori informazioni, vedere [connessione di un modulo merge a più funzionalità](connecting-a-merge-module-to-multiple-features.md).</span><span class="sxs-lookup"><span data-stu-id="770c2-128">For more information, see [Connecting a Merge Module to Multiple Features](connecting-a-merge-module-to-multiple-features.md).</span></span>

7.  <span data-ttu-id="770c2-129">Se necessario, estrarre i file di origine dal modulo eseguendo una o più delle operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="770c2-129">If necessary, extract source files from the module by doing one or more of the following:</span></span>
    -   <span data-ttu-id="770c2-130">Usare [**ExtractFiles**](merge-extractfiles.md) o [**ExtractFilesEx**](merge-extractfilesex.md) per estrarre i file da un file CAB incorporato e quindi copiarli in una directory specificata.</span><span class="sxs-lookup"><span data-stu-id="770c2-130">Use [**ExtractFiles**](merge-extractfiles.md) or [**ExtractFilesEx**](merge-extractfilesex.md) to extract files from an embedded .cab file and then copy into a specified directory.</span></span>
        > [!Note]  
        > <span data-ttu-id="770c2-131">[**ExtractFilesEx**](merge-extractfilesex.md) richiede [Mergemod.dll versione 2,0](merge-module-automation.md) o successiva.</span><span class="sxs-lookup"><span data-stu-id="770c2-131">[**ExtractFilesEx**](merge-extractfilesex.md) requires [Mergemod.dll version 2.0](merge-module-automation.md) or later.</span></span>

         

    -   <span data-ttu-id="770c2-132">Utilizzare [**ExtractCAB**](merge-extractcab.md) per estrarre i file da un file con estensione cab incorporato e quindi salvarli in un file specificato.</span><span class="sxs-lookup"><span data-stu-id="770c2-132">Use [**ExtractCAB**](merge-extractcab.md) to extract files from an embedded .cab file, and then save in a specified file.</span></span>
    -   <span data-ttu-id="770c2-133">Usare [**CreateSourceImage**](merge-createsourceimage.md) per estrarre i file da un modulo e quindi, dopo il merge, copiarli in un'immagine di origine su disco.</span><span class="sxs-lookup"><span data-stu-id="770c2-133">Use [**CreateSourceImage**](merge-createsourceimage.md) to extract files from a module, and then after the merge, copy to a source image on disk.</span></span>
        > [!Note]  
        > <span data-ttu-id="770c2-134">[**CreateSourceImage**](merge-createsourceimage.md) è disponibile solo in [Mergemod.dll versione 2,0](merge-module-automation.md) o successiva.</span><span class="sxs-lookup"><span data-stu-id="770c2-134">[**CreateSourceImage**](merge-createsourceimage.md) is only available in [Mergemod.dll version 2.0](merge-module-automation.md) or later.</span></span>

         
8.  <span data-ttu-id="770c2-135">Chiudere il modulo Open merge corrente usando il metodo [**CloseModule**](merge-closemodule.md) .</span><span class="sxs-lookup"><span data-stu-id="770c2-135">Close the current open merge module by using the [**CloseModule**](merge-closemodule.md) method.</span></span>

    <span data-ttu-id="770c2-136">Questo passaggio è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="770c2-136">This step is required.</span></span>

9.  <span data-ttu-id="770c2-137">Chiudere il database di installazione aperto utilizzando il metodo [**ChiudiDatabase**](merge-closedatabase.md) .</span><span class="sxs-lookup"><span data-stu-id="770c2-137">Close the open installation database by using the [**CloseDatabase**](merge-closedatabase.md) method.</span></span>

    <span data-ttu-id="770c2-138">Questo passaggio è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="770c2-138">This step is required.</span></span>

    <span data-ttu-id="770c2-139">La chiusura di un database Cancella tutte le informazioni sulle dipendenze, ma non influisce sugli errori che non vengono recuperati.</span><span class="sxs-lookup"><span data-stu-id="770c2-139">Closing a database clears all dependency information, but does not affect any errors that are not retrieved.</span></span>

10. <span data-ttu-id="770c2-140">Chiudere il file di log corrente usando il metodo [**CloseLog**](merge-closelog.md) .</span><span class="sxs-lookup"><span data-stu-id="770c2-140">Close the current log file by using the [**CloseLog**](merge-closelog.md) method.</span></span>

    <span data-ttu-id="770c2-141">Questo passaggio è obbligatorio se si dispone di un file di log aperto.</span><span class="sxs-lookup"><span data-stu-id="770c2-141">This step is required if you have an open log file.</span></span>

<span data-ttu-id="770c2-142">Dopo che il modulo è stato unito al database usando [Mergemod.dll](merge-module-automation.md), è necessario aggiornare la [tabella dei supporti](media-table.md) per descrivere il layout dell'immagine di origine desiderato.</span><span class="sxs-lookup"><span data-stu-id="770c2-142">After the module has been merged into the database using [Mergemod.dll](merge-module-automation.md), the [Media Table](media-table.md) must be updated to describe the desired source image layout.</span></span> <span data-ttu-id="770c2-143">Il processo di merge fornito da Mergemod.dll non aggiorna la tabella dei supporti perché il consumer del modulo merge può selezionare diversi modi per creare il layout dell'immagine di origine.</span><span class="sxs-lookup"><span data-stu-id="770c2-143">The merge process provided by Mergemod.dll does not update the Media Table because the consumer of the merge module can select various ways to layout the source image.</span></span>

## <a name="related-topics"></a><span data-ttu-id="770c2-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="770c2-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="770c2-145">Versioni rilasciate, strumenti e ridistribuibili</span><span class="sxs-lookup"><span data-stu-id="770c2-145">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



