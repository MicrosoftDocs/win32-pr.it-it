---
description: Nella procedura riportata di seguito vengono descritti i passaggi generali per la creazione di moduli unione.
ms.assetid: 4b3871c0-f452-4935-9ee3-78b0ac847e67
title: Creazione di moduli unione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ece67151872a8d065d321c6adaae660be643ad8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227205"
---
# <a name="authoring-merge-modules"></a><span data-ttu-id="ba332-103">Creazione di moduli unione</span><span class="sxs-lookup"><span data-stu-id="ba332-103">Authoring Merge Modules</span></span>

<span data-ttu-id="ba332-104">Nella procedura riportata di seguito vengono descritti i passaggi generali per la creazione di moduli unione.</span><span class="sxs-lookup"><span data-stu-id="ba332-104">The following procedure describes the general steps to authoring merge modules.</span></span>

<span data-ttu-id="ba332-105">**Per creare un nuovo modulo merge**</span><span class="sxs-lookup"><span data-stu-id="ba332-105">**To create a new merge module**</span></span>

1.  <span data-ttu-id="ba332-106">Ottenere uno strumento software che è possibile utilizzare per modificare il database del modulo merge.</span><span class="sxs-lookup"><span data-stu-id="ba332-106">Obtain a software tool you can use to edit the merge module database.</span></span>
2.  <span data-ttu-id="ba332-107">Ottenere un database del modulo merge vuoto.</span><span class="sxs-lookup"><span data-stu-id="ba332-107">Obtain a blank merge module database.</span></span>
3.  <span data-ttu-id="ba332-108">Generare un [GUID](guid.md) per il modulo unione.</span><span class="sxs-lookup"><span data-stu-id="ba332-108">Generate a [GUID](guid.md) for the merge module.</span></span> <span data-ttu-id="ba332-109">È necessario utilizzare questo GUID quando si creano le chiavi primarie delle tabelle di database nel modulo merge.</span><span class="sxs-lookup"><span data-stu-id="ba332-109">You need to use this GUID when authoring the primary keys of database tables in the merge module.</span></span>
4.  <span data-ttu-id="ba332-110">Aggiungere un record alla [tabella dei componenti](component-table.md) per ogni componente recapitato dall'Unione.</span><span class="sxs-lookup"><span data-stu-id="ba332-110">Add a record to the [Component table](component-table.md) for each component delivered by the merge.</span></span> <span data-ttu-id="ba332-111">In ogni modulo merge è necessaria una tabella di componenti.</span><span class="sxs-lookup"><span data-stu-id="ba332-111">A Component table is required in every merge module.</span></span> <span data-ttu-id="ba332-112">Si noti che i moduli merge operano con i componenti e non con le funzionalità di.</span><span class="sxs-lookup"><span data-stu-id="ba332-112">Note that merge modules operate with components and not with features.</span></span> <span data-ttu-id="ba332-113">In alcuni casi, tuttavia, potrebbe essere necessario che una voce della tabella di database faccia riferimento a una funzionalità.</span><span class="sxs-lookup"><span data-stu-id="ba332-113">In certain cases, however, a database table entry may need to reference a feature.</span></span> <span data-ttu-id="ba332-114">Per informazioni dettagliate, vedere [riferimento alle funzionalità nei moduli unione](referencing-features-in-merge-modules.md).</span><span class="sxs-lookup"><span data-stu-id="ba332-114">For details, see [Referencing Features in Merge Modules](referencing-features-in-merge-modules.md).</span></span>
5.  <span data-ttu-id="ba332-115">Aggiungere una [tabella di directory](directory-table.md) al modulo merge che specifica il layout delle directory che il modulo merge aggiunge al database di destinazione.</span><span class="sxs-lookup"><span data-stu-id="ba332-115">Add a [Directory table](directory-table.md) to the merge module that specifies the layout of directories the merge module adds to the target database.</span></span> <span data-ttu-id="ba332-116">In ogni modulo merge è necessaria una tabella di directory.</span><span class="sxs-lookup"><span data-stu-id="ba332-116">A Directory table is required in every merge module.</span></span>
6.  <span data-ttu-id="ba332-117">Importare una [tabella FeatureComponents](featurecomponents-table.md) vuota nel database del modulo merge.</span><span class="sxs-lookup"><span data-stu-id="ba332-117">Import a blank [FeatureComponents table](featurecomponents-table.md) into the merge module database.</span></span> <span data-ttu-id="ba332-118">Questa tabella vuota fornisce linee guida per lo strumento di merge nei casi in cui il file con estensione msi non contiene la propria tabella FeatureComponents.</span><span class="sxs-lookup"><span data-stu-id="ba332-118">This empty table provides a guideline for the merge tool in cases where the .msi file does not contain its own FeatureComponents table.</span></span>
7.  <span data-ttu-id="ba332-119">Raccogliere tutti i file recapitati da questo modulo merge e creare il file CAB [MergeModule.CABinet](mergemodule-cabinet.md) .</span><span class="sxs-lookup"><span data-stu-id="ba332-119">Collect all the files delivered by this merge module and create the [MergeModule.CABinet](mergemodule-cabinet.md) cabinet file.</span></span> <span data-ttu-id="ba332-120">Aggiungere il file CAB al modulo merge come flusso all'interno del file. msm.</span><span class="sxs-lookup"><span data-stu-id="ba332-120">Add the cabinet to the merge module as a stream inside the .msm file.</span></span>
8.  <span data-ttu-id="ba332-121">Aggiungere un record alla tabella file per ogni file archiviato in MergeModule.CABinet.</span><span class="sxs-lookup"><span data-stu-id="ba332-121">Add a record to the File table for every file stored in MergeModule.CABinet.</span></span>
9.  <span data-ttu-id="ba332-122">Aggiungere le informazioni necessarie per identificare il modulo merge nella [tabella ModuleSignature](modulesignature-table.md).</span><span class="sxs-lookup"><span data-stu-id="ba332-122">Add the information necessary to identify the merge module in the [ModuleSignature table](modulesignature-table.md).</span></span> <span data-ttu-id="ba332-123">Ogni modulo merge richiede una tabella ModuleSignature.</span><span class="sxs-lookup"><span data-stu-id="ba332-123">Every merge module requires a ModuleSignature table.</span></span>
10. <span data-ttu-id="ba332-124">Elenca i componenti del modulo merge nella [tabella ModuleComponents](modulecomponents-table.md).</span><span class="sxs-lookup"><span data-stu-id="ba332-124">List the components in the merge module in the [ModuleComponents table](modulecomponents-table.md).</span></span> <span data-ttu-id="ba332-125">Ogni modulo merge richiede una tabella ModuleComponents.</span><span class="sxs-lookup"><span data-stu-id="ba332-125">Every merge module requires a ModuleComponents table.</span></span>
11. <span data-ttu-id="ba332-126">Aggiungere le tabelle di sequenza dei moduli merge al file MSM solo se il modulo merge deve modificare le [*tabelle di sequenza*](s-gly.md) del database di installazione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="ba332-126">Add merge module sequence tables to the .msm file only if the merge module needs to modify the [*sequence tables*](s-gly.md) of the target installation database.</span></span>
12. <span data-ttu-id="ba332-127">Aggiungere una \_ tabella di convalida al modulo merge.</span><span class="sxs-lookup"><span data-stu-id="ba332-127">Add a \_Validation table to the merge module.</span></span> <span data-ttu-id="ba332-128">Un modulo merge richiede una \_ tabella di convalida per il superamento della convalida.</span><span class="sxs-lookup"><span data-stu-id="ba332-128">A merge module requires a \_Validation table to pass validation.</span></span>
13. <span data-ttu-id="ba332-129">I moduli merge richiedono un'interfaccia utente solo in rari casi.</span><span class="sxs-lookup"><span data-stu-id="ba332-129">Merge modules require a user interface in only rare cases.</span></span> <span data-ttu-id="ba332-130">Non è consigliabile includere un'interfaccia utente con un modulo merge.</span><span class="sxs-lookup"><span data-stu-id="ba332-130">Including a UI with a merge module is not recommended.</span></span> <span data-ttu-id="ba332-131">Nei casi in cui è necessaria un'interfaccia utente, le tabelle dell'interfaccia utente possono essere unite nel file con estensione msi come le altre tabelle.</span><span class="sxs-lookup"><span data-stu-id="ba332-131">In cases where a user interface is required, the UI tables can be merged into the .msi file the same as other tables.</span></span>
14. <span data-ttu-id="ba332-132">Aggiungere le informazioni del registro di sistema alle tabelle del registro di sistema appropriate nel database del modulo merge.</span><span class="sxs-lookup"><span data-stu-id="ba332-132">Add registry information to the appropriate registry tables in the merge module database.</span></span> <span data-ttu-id="ba332-133">Aggiungere le informazioni del registro di sistema per le librerie dei tipi, le classi, le estensioni e i verbi nelle tabelle [typelib](typelib-table.md), [Class](class-table.md), [AppID](appid-table.md), [ProgID](progid-table.md), [Extension](extension-table.md), [Verb](verb-table.md)o [MIME](mime-table.md) .</span><span class="sxs-lookup"><span data-stu-id="ba332-133">Add registry information for type libraries, classes, extensions, and verbs into the [TypeLib](typelib-table.md), [Class](class-table.md), [AppId](appid-table.md), [ProgId](progid-table.md), [Extension](extension-table.md), [Verb](verb-table.md), or [MIME](mime-table.md) tables.</span></span> <span data-ttu-id="ba332-134">Tutte le altre informazioni del registro di sistema possono essere inserite nella [tabella del registro di sistema](registry-table.md).</span><span class="sxs-lookup"><span data-stu-id="ba332-134">All other registry information can go into the [Registry table](registry-table.md).</span></span> <span data-ttu-id="ba332-135">Non è consigliabile usare la tabella SelfReg.</span><span class="sxs-lookup"><span data-stu-id="ba332-135">The use of the SelfReg table is not recommended.</span></span>
15. <span data-ttu-id="ba332-136">Aggiungere le informazioni di riepilogo al [flusso di informazioni di riepilogo del modulo unione](merge-module-summary-information-stream-reference.md).</span><span class="sxs-lookup"><span data-stu-id="ba332-136">Add the summary information to the [Merge Module Summary Information Stream](merge-module-summary-information-stream-reference.md).</span></span>
16. <span data-ttu-id="ba332-137">Prima di tentare l'installazione, eseguire la convalida su tutti i moduli unione.</span><span class="sxs-lookup"><span data-stu-id="ba332-137">Run validation on all merge modules before attempting to install.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ba332-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ba332-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba332-139">Recupero di database del modulo merge vuoti</span><span class="sxs-lookup"><span data-stu-id="ba332-139">Obtaining Blank Merge Module Databases</span></span>](obtaining-blank-merge-module-databases.md)
</dt> <dt>

[<span data-ttu-id="ba332-140">Recupero di strumenti di creazione di moduli merge</span><span class="sxs-lookup"><span data-stu-id="ba332-140">Obtaining Merge Module Authoring Tools</span></span>](obtaining-merge-module-authoring-tools.md)
</dt> <dt>

[<span data-ttu-id="ba332-141">Denominazione di chiavi primarie nei database del modulo merge</span><span class="sxs-lookup"><span data-stu-id="ba332-141">Naming Primary Keys in Merge Module Databases</span></span>](naming-primary-keys-in-merge-module-databases.md)
</dt> <dt>

[<span data-ttu-id="ba332-142">Creazione di tabelle di componenti del modulo merge</span><span class="sxs-lookup"><span data-stu-id="ba332-142">Authoring Merge Module Component Tables</span></span>](authoring-merge-module-component-tables.md)
</dt> <dt>

[<span data-ttu-id="ba332-143">Creazione di tabelle di directory del modulo merge</span><span class="sxs-lookup"><span data-stu-id="ba332-143">Authoring Merge Module Directory Tables</span></span>](authoring-merge-module-directory-tables.md)
</dt> <dt>

[<span data-ttu-id="ba332-144">Creazione di tabelle FeatureComponents del modulo merge</span><span class="sxs-lookup"><span data-stu-id="ba332-144">Authoring Merge Module FeatureComponents Tables</span></span>](authoring-merge-module-featurecomponents-tables.md)
</dt> <dt>

[<span data-ttu-id="ba332-145">Generazione di MergeModule.CABfile CAB inet</span><span class="sxs-lookup"><span data-stu-id="ba332-145">Generating MergeModule.CABinet Cabinet Files</span></span>](generating-mergemodule-cabinet-cabinet-files.md)
</dt> <dt>

[<span data-ttu-id="ba332-146">Creazione di tabelle di file del modulo merge</span><span class="sxs-lookup"><span data-stu-id="ba332-146">Authoring Merge Module File Tables</span></span>](authoring-merge-module-file-tables.md)
</dt> <dt>

[<span data-ttu-id="ba332-147">Creazione di tabelle ModuleSignature</span><span class="sxs-lookup"><span data-stu-id="ba332-147">Authoring ModuleSignature Tables</span></span>](authoring-modulesignature-tables.md)
</dt> <dt>

[<span data-ttu-id="ba332-148">Creazione di tabelle ModuleComponents</span><span class="sxs-lookup"><span data-stu-id="ba332-148">Authoring ModuleComponents Tables</span></span>](authoring-modulecomponents-tables.md)
</dt> <dt>

[<span data-ttu-id="ba332-149">Creazione di tabelle di sequenza del modulo merge</span><span class="sxs-lookup"><span data-stu-id="ba332-149">Authoring Merge Module Sequence Tables</span></span>](authoring-merge-module-sequence-tables.md)
</dt> <dt>

[<span data-ttu-id="ba332-150">Convalida di moduli merge</span><span class="sxs-lookup"><span data-stu-id="ba332-150">Validating Merge Modules</span></span>](validating-merge-modules.md)
</dt> <dt>

[<span data-ttu-id="ba332-151">Creazione di interfacce utente nei moduli merge</span><span class="sxs-lookup"><span data-stu-id="ba332-151">Authoring User Interfaces in Merge Modules</span></span>](authoring-user-interfaces-in-merge-modules.md)
</dt> <dt>

[<span data-ttu-id="ba332-152">Creazione di tabelle del registro di sistema del modulo merge</span><span class="sxs-lookup"><span data-stu-id="ba332-152">Authoring Merge Module Registry Tables</span></span>](authoring-merge-module-registry-tables.md)
</dt> <dt>

[<span data-ttu-id="ba332-153">Creazione di flussi di informazioni di riepilogo del modulo merge</span><span class="sxs-lookup"><span data-stu-id="ba332-153">Authoring Merge Module Summary Information Streams</span></span>](authoring-merge-module-summary-information-streams.md)
</dt> <dt>

[<span data-ttu-id="ba332-154">Riferimento al flusso di informazioni di riepilogo del modulo merge</span><span class="sxs-lookup"><span data-stu-id="ba332-154">Merge Module Summary Information Stream Reference</span></span>](merge-module-summary-information-stream-reference.md)
</dt> <dt>

<span data-ttu-id="ba332-155">Convalida di moduli merge</span><span class="sxs-lookup"><span data-stu-id="ba332-155">Validating Merge Modules</span></span>
</dt> <dt>

[<span data-ttu-id="ba332-156">Uso di moduli unione a 64 bit</span><span class="sxs-lookup"><span data-stu-id="ba332-156">Using 64-bit Merge Modules</span></span>](using-64-bit-merge-modules.md)
</dt> </dl>

 

 



