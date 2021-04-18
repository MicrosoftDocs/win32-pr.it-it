---
description: Le tabelle seguenti sono necessarie in un modulo merge standard.
ms.assetid: 2af6cea0-6d93-4aa5-a708-d305f11986ef
title: Tabelle di database del modulo merge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17a58240c589297cf2540625bc12180252efa42d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316265"
---
# <a name="merge-module-database-tables"></a><span data-ttu-id="16e98-103">Tabelle di database del modulo merge</span><span class="sxs-lookup"><span data-stu-id="16e98-103">Merge Module Database Tables</span></span>

<span data-ttu-id="16e98-104">Le tabelle seguenti sono necessarie in un modulo merge standard.</span><span class="sxs-lookup"><span data-stu-id="16e98-104">The following tables are required in a standard merge module.</span></span>



| <span data-ttu-id="16e98-105">Nome tabella</span><span class="sxs-lookup"><span data-stu-id="16e98-105">Table name</span></span>                                       | <span data-ttu-id="16e98-106">Commento</span><span class="sxs-lookup"><span data-stu-id="16e98-106">Comment</span></span>                                                                                          |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="16e98-107">Componente</span><span class="sxs-lookup"><span data-stu-id="16e98-107">Component</span></span>](component-table.md)                 | <span data-ttu-id="16e98-108">NECESSARIA</span><span class="sxs-lookup"><span data-stu-id="16e98-108">(REQUIRED)</span></span>                                                                                       |
| [<span data-ttu-id="16e98-109">Directory</span><span class="sxs-lookup"><span data-stu-id="16e98-109">Directory</span></span>](directory-table.md)                 | <span data-ttu-id="16e98-110">NECESSARIA</span><span class="sxs-lookup"><span data-stu-id="16e98-110">(REQUIRED)</span></span>                                                                                       |
| [<span data-ttu-id="16e98-111">FeatureComponents</span><span class="sxs-lookup"><span data-stu-id="16e98-111">FeatureComponents</span></span>](featurecomponents-table.md) | <span data-ttu-id="16e98-112">NECESSARIA</span><span class="sxs-lookup"><span data-stu-id="16e98-112">(REQUIRED)</span></span>                                                                                       |
| [<span data-ttu-id="16e98-113">File</span><span class="sxs-lookup"><span data-stu-id="16e98-113">File</span></span>](file-table.md)                           | <span data-ttu-id="16e98-114">NECESSARIA</span><span class="sxs-lookup"><span data-stu-id="16e98-114">(REQUIRED)</span></span>                                                                                       |
| [<span data-ttu-id="16e98-115">ModuleSignature</span><span class="sxs-lookup"><span data-stu-id="16e98-115">ModuleSignature</span></span>](modulesignature-table.md)     | <span data-ttu-id="16e98-116">NECESSARIA Unito nel database del programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="16e98-116">(REQUIRED) Merged into the installer database.</span></span> <span data-ttu-id="16e98-117">Elenca le informazioni che identificano un modulo merge.</span><span class="sxs-lookup"><span data-stu-id="16e98-117">Lists the information identifying a merge module.</span></span> |
| [<span data-ttu-id="16e98-118">ModuleComponents</span><span class="sxs-lookup"><span data-stu-id="16e98-118">ModuleComponents</span></span>](modulecomponents-table.md)   | <span data-ttu-id="16e98-119">NECESSARIA Unito nel database del programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="16e98-119">(REQUIRED) Merged into the installer database.</span></span> <span data-ttu-id="16e98-120">Elenca tutti i componenti del modulo merge.</span><span class="sxs-lookup"><span data-stu-id="16e98-120">Lists all the components in the merge module.</span></span>     |



 

<span data-ttu-id="16e98-121">Le tabelle seguenti si verificano solo nei moduli merge o in altri database del programma di installazione che sono già stati combinati con un modulo merge.</span><span class="sxs-lookup"><span data-stu-id="16e98-121">The following tables only occur in merge modules or other installer databases that have already been combined with a merge module.</span></span>



| <span data-ttu-id="16e98-122">Nome tabella</span><span class="sxs-lookup"><span data-stu-id="16e98-122">Table name</span></span>                                     | <span data-ttu-id="16e98-123">Commento</span><span class="sxs-lookup"><span data-stu-id="16e98-123">Comment</span></span>                                                                                                     |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="16e98-124">ModuleDependency</span><span class="sxs-lookup"><span data-stu-id="16e98-124">ModuleDependency</span></span>](moduledependency-table.md) | <span data-ttu-id="16e98-125">Unito nel database del programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="16e98-125">Merged into the installer database.</span></span> <span data-ttu-id="16e98-126">Elenca altri moduli merge richiesti da questo modulo merge.</span><span class="sxs-lookup"><span data-stu-id="16e98-126">Lists other merge modules required by this merge module.</span></span>                |
| [<span data-ttu-id="16e98-127">ModuleExclusion</span><span class="sxs-lookup"><span data-stu-id="16e98-127">ModuleExclusion</span></span>](moduleexclusion-table.md)   | <span data-ttu-id="16e98-128">Unito nel database del programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="16e98-128">Merged into the installer database.</span></span> <span data-ttu-id="16e98-129">Elenca altri moduli merge che non sono compatibili con questo modulo unione.</span><span class="sxs-lookup"><span data-stu-id="16e98-129">Lists other merge modules that are incompatible with this merge module.</span></span> |



 

<span data-ttu-id="16e98-130">Le tabelle ModuleSequence seguenti si verificano solo nei moduli unione.</span><span class="sxs-lookup"><span data-stu-id="16e98-130">The following ModuleSequence tables only occur in merge modules.</span></span>



| <span data-ttu-id="16e98-131">Nome tabella</span><span class="sxs-lookup"><span data-stu-id="16e98-131">Table name</span></span>                                                             | <span data-ttu-id="16e98-132">Commento</span><span class="sxs-lookup"><span data-stu-id="16e98-132">Comment</span></span>                                                                                   |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="16e98-133">ModuleAdminUISequence</span><span class="sxs-lookup"><span data-stu-id="16e98-133">ModuleAdminUISequence</span></span>](moduleadminuisequence-table.md)               | <span data-ttu-id="16e98-134">Unisce le azioni nella [tabella AdminUISequence](adminuisequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="16e98-134">Merges actions into the [AdminUISequence table](adminuisequence-table.md).</span></span>               |
| [<span data-ttu-id="16e98-135">ModuleAdminExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="16e98-135">ModuleAdminExecuteSequence</span></span>](moduleadminexecutesequence-table.md)     | <span data-ttu-id="16e98-136">Unisce le azioni nella [tabella AdminExecuteSequence](adminexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="16e98-136">Merges actions into the [AdminExecuteSequence table](adminexecutesequence-table.md).</span></span>     |
| [<span data-ttu-id="16e98-137">ModuleAdvtUISequence</span><span class="sxs-lookup"><span data-stu-id="16e98-137">ModuleAdvtUISequence</span></span>](moduleadvtuisequence-table.md)                 | <span data-ttu-id="16e98-138">Non usare questa tabella.</span><span class="sxs-lookup"><span data-stu-id="16e98-138">Do not use this table.</span></span> <span data-ttu-id="16e98-139">Per informazioni dettagliate, vedere [tabella AdvtUISequence](advtuisequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="16e98-139">For details, see [AdvtUISequence table](advtuisequence-table.md).</span></span> |
| [<span data-ttu-id="16e98-140">ModuleAdvtExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="16e98-140">ModuleAdvtExecuteSequence</span></span>](moduleadvtexecutesequence-table.md)       | <span data-ttu-id="16e98-141">Unisce le azioni nella [tabella AdvtExecuteSequence](advtexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="16e98-141">Merges actions into the [AdvtExecuteSequence table](advtexecutesequence-table.md).</span></span>       |
| [<span data-ttu-id="16e98-142">ModuleIgnoreTable</span><span class="sxs-lookup"><span data-stu-id="16e98-142">ModuleIgnoreTable</span></span>](moduleignoretable-table.md)                       | <span data-ttu-id="16e98-143">Elenca le tabelle del modulo che non sono unite nel file con estensione msi.</span><span class="sxs-lookup"><span data-stu-id="16e98-143">Lists tables in the module that are not merged into the .msi file.</span></span>                        |
| [<span data-ttu-id="16e98-144">ModuleInstallUISequence</span><span class="sxs-lookup"><span data-stu-id="16e98-144">ModuleInstallUISequence</span></span>](moduleinstalluisequence-table.md)           | <span data-ttu-id="16e98-145">Unisce le azioni nella [tabella InstallUISequence](installuisequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="16e98-145">Merges actions into the [InstallUISequence table](installuisequence-table.md).</span></span>           |
| [<span data-ttu-id="16e98-146">ModuleInstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="16e98-146">ModuleInstallExecuteSequence</span></span>](moduleinstallexecutesequence-table.md) | <span data-ttu-id="16e98-147">Unisce le azioni nella [tabella InstallExecuteSequence](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="16e98-147">Merges actions into the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> |



 

<span data-ttu-id="16e98-148">Le tabelle seguenti sono necessarie in ogni modulo merge configurabile.</span><span class="sxs-lookup"><span data-stu-id="16e98-148">The following tables are required in every configurable merge module.</span></span> <span data-ttu-id="16e98-149">Per creare un modulo merge configurabile, è necessario Mergemod.dll 2,0 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="16e98-149">Mergemod.dll 2.0 or later is required to create configurable merge module.</span></span> <span data-ttu-id="16e98-150">Per informazioni dettagliate, vedere [moduli merge configurabili](configurable-merge-modules.md).</span><span class="sxs-lookup"><span data-stu-id="16e98-150">For details, see [Configurable Merge Modules](configurable-merge-modules.md).</span></span>



| <span data-ttu-id="16e98-151">Nome tabella</span><span class="sxs-lookup"><span data-stu-id="16e98-151">Table name</span></span>                                                 | <span data-ttu-id="16e98-152">Commento</span><span class="sxs-lookup"><span data-stu-id="16e98-152">Comment</span></span>                                                                                                                                                                                          |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="16e98-153">Tabella ModuleSubstitution</span><span class="sxs-lookup"><span data-stu-id="16e98-153">ModuleSubstitution Table</span></span>](modulesubstitution-table.md)   | <span data-ttu-id="16e98-154">NECESSARIA Questa tabella non viene unita nel database di installazione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="16e98-154">(REQUIRED) This table is not merged into the target installation database.</span></span> <span data-ttu-id="16e98-155">Specifica i campi configurabili nel database di destinazione e fornisce un modello per la configurazione di ogni campo.</span><span class="sxs-lookup"><span data-stu-id="16e98-155">Specifies the configurable fields in the target database and provides a template for the configuration of each field.</span></span> |
| [<span data-ttu-id="16e98-156">Tabella ModuleConfiguration</span><span class="sxs-lookup"><span data-stu-id="16e98-156">ModuleConfiguration Table</span></span>](moduleconfiguration-table.md) | <span data-ttu-id="16e98-157">NECESSARIA Questa tabella non viene unita nel database di installazione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="16e98-157">(REQUIRED) This table is not merged into the target installation database.</span></span> <span data-ttu-id="16e98-158">Identifica gli attributi configurabili del modulo.</span><span class="sxs-lookup"><span data-stu-id="16e98-158">Identifies the configurable attributes of the module.</span></span>                                                                 |



 

<span data-ttu-id="16e98-159">Le tabelle del programma di installazione seguenti non possono essere presenti in un modulo merge standard.</span><span class="sxs-lookup"><span data-stu-id="16e98-159">The following installer tables cannot occur in a standard merge module.</span></span>

-   [<span data-ttu-id="16e98-160">BBControl</span><span class="sxs-lookup"><span data-stu-id="16e98-160">BBControl</span></span>](bbcontrol-table.md)
-   [<span data-ttu-id="16e98-161">Billboard</span><span class="sxs-lookup"><span data-stu-id="16e98-161">Billboard</span></span>](billboard-table.md)
-   [<span data-ttu-id="16e98-162">CCPSearch</span><span class="sxs-lookup"><span data-stu-id="16e98-162">CCPSearch</span></span>](ccpsearch-table.md)
-   [<span data-ttu-id="16e98-163">Error (Errore) (Error (Errore)e)</span><span class="sxs-lookup"><span data-stu-id="16e98-163">Error</span></span>](error-table.md)
-   [<span data-ttu-id="16e98-164">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="16e98-164">Feature</span></span>](feature-table.md)
-   [<span data-ttu-id="16e98-165">Tabella LaunchCondition</span><span class="sxs-lookup"><span data-stu-id="16e98-165">LaunchCondition table</span></span>](launchcondition-table.md)
-   [<span data-ttu-id="16e98-166">Supporti</span><span class="sxs-lookup"><span data-stu-id="16e98-166">Media</span></span>](media-table.md)
-   [<span data-ttu-id="16e98-167">Patch</span><span class="sxs-lookup"><span data-stu-id="16e98-167">Patch</span></span>](patch-table.md)
-   [<span data-ttu-id="16e98-168">Aggiornamento</span><span class="sxs-lookup"><span data-stu-id="16e98-168">Upgrade</span></span>](upgrade-table.md)

<span data-ttu-id="16e98-169">Le tabelle del programma di installazione seguenti sono facoltative nei moduli unione.</span><span class="sxs-lookup"><span data-stu-id="16e98-169">The following installer tables are optional in merge modules.</span></span>

-   [<span data-ttu-id="16e98-170">ActionText</span><span class="sxs-lookup"><span data-stu-id="16e98-170">ActionText</span></span>](actiontext-table.md)
-   [<span data-ttu-id="16e98-171">AdminExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="16e98-171">AdminExecuteSequence</span></span>](adminexecutesequence-table.md)
-   [<span data-ttu-id="16e98-172">AdminUISequence</span><span class="sxs-lookup"><span data-stu-id="16e98-172">AdminUISequence</span></span>](adminuisequence-table.md)
-   [<span data-ttu-id="16e98-173">AdvtExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="16e98-173">AdvtExecuteSequence</span></span>](advtexecutesequence-table.md)
-   [<span data-ttu-id="16e98-174">AdvtUISequence</span><span class="sxs-lookup"><span data-stu-id="16e98-174">AdvtUISequence</span></span>](advtuisequence-table.md)
-   [<span data-ttu-id="16e98-175">AppId</span><span class="sxs-lookup"><span data-stu-id="16e98-175">AppId</span></span>](appid-table.md)
-   [<span data-ttu-id="16e98-176">AppSearch</span><span class="sxs-lookup"><span data-stu-id="16e98-176">AppSearch</span></span>](appsearch-table.md)
-   [<span data-ttu-id="16e98-177">Azione BindImage sul</span><span class="sxs-lookup"><span data-stu-id="16e98-177">BindImage</span></span>](bindimage-table.md)
-   [<span data-ttu-id="16e98-178">CheckBox</span><span class="sxs-lookup"><span data-stu-id="16e98-178">CheckBox</span></span>](checkbox-table.md)
-   [<span data-ttu-id="16e98-179">Classe</span><span class="sxs-lookup"><span data-stu-id="16e98-179">Class</span></span>](class-table.md)
-   [<span data-ttu-id="16e98-180">ComboBox</span><span class="sxs-lookup"><span data-stu-id="16e98-180">ComboBox</span></span>](combobox-table.md)
-   [<span data-ttu-id="16e98-181">CompLocator</span><span class="sxs-lookup"><span data-stu-id="16e98-181">CompLocator</span></span>](complocator-table.md)
-   [<span data-ttu-id="16e98-182">Controllo</span><span class="sxs-lookup"><span data-stu-id="16e98-182">Control</span></span>](control-table.md)
-   [<span data-ttu-id="16e98-183">ControlCondition</span><span class="sxs-lookup"><span data-stu-id="16e98-183">ControlCondition</span></span>](controlcondition-table.md)
-   [<span data-ttu-id="16e98-184">CreateFolder</span><span class="sxs-lookup"><span data-stu-id="16e98-184">CreateFolder</span></span>](createfolder-table.md)
-   [<span data-ttu-id="16e98-185">CustomAction</span><span class="sxs-lookup"><span data-stu-id="16e98-185">CustomAction</span></span>](customaction-table.md)
-   [<span data-ttu-id="16e98-186">Finestra di dialogo</span><span class="sxs-lookup"><span data-stu-id="16e98-186">Dialog</span></span>](dialog-table.md)
-   [<span data-ttu-id="16e98-187">DrLocator</span><span class="sxs-lookup"><span data-stu-id="16e98-187">DrLocator</span></span>](drlocator-table.md)
-   [<span data-ttu-id="16e98-188">DuplicateFile</span><span class="sxs-lookup"><span data-stu-id="16e98-188">DuplicateFile</span></span>](duplicatefile-table.md)
-   [<span data-ttu-id="16e98-189">Environment</span><span class="sxs-lookup"><span data-stu-id="16e98-189">Environment</span></span>](environment-table.md)
-   [<span data-ttu-id="16e98-190">EventMapping</span><span class="sxs-lookup"><span data-stu-id="16e98-190">EventMapping</span></span>](eventmapping-table.md)
-   [<span data-ttu-id="16e98-191">Estensione</span><span class="sxs-lookup"><span data-stu-id="16e98-191">Extension</span></span>](extension-table.md)
-   [<span data-ttu-id="16e98-192">Carattere</span><span class="sxs-lookup"><span data-stu-id="16e98-192">Font</span></span>](font-table.md)
-   [<span data-ttu-id="16e98-193">Icona</span><span class="sxs-lookup"><span data-stu-id="16e98-193">Icon</span></span>](icon-table.md)
-   [<span data-ttu-id="16e98-194">IniFile</span><span class="sxs-lookup"><span data-stu-id="16e98-194">IniFile</span></span>](inifile-table.md)
-   [<span data-ttu-id="16e98-195">IniLocator</span><span class="sxs-lookup"><span data-stu-id="16e98-195">IniLocator</span></span>](inilocator-table.md)
-   [<span data-ttu-id="16e98-196">InstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="16e98-196">InstallExecuteSequence</span></span>](installexecutesequence-table.md)
-   [<span data-ttu-id="16e98-197">InstallUISequence</span><span class="sxs-lookup"><span data-stu-id="16e98-197">InstallUISequence</span></span>](installuisequence-table.md)
-   [<span data-ttu-id="16e98-198">ListBox</span><span class="sxs-lookup"><span data-stu-id="16e98-198">ListBox</span></span>](listbox-table.md)
-   [<span data-ttu-id="16e98-199">ListView</span><span class="sxs-lookup"><span data-stu-id="16e98-199">ListView</span></span>](listview-table.md)
-   [<span data-ttu-id="16e98-200">MIME</span><span class="sxs-lookup"><span data-stu-id="16e98-200">MIME</span></span>](mime-table.md)
-   [<span data-ttu-id="16e98-201">MoveFile</span><span class="sxs-lookup"><span data-stu-id="16e98-201">MoveFile</span></span>](movefile-table.md)
-   [<span data-ttu-id="16e98-202">ODBCAttribute</span><span class="sxs-lookup"><span data-stu-id="16e98-202">ODBCAttribute</span></span>](odbcattribute-table.md)
-   [<span data-ttu-id="16e98-203">ODBCDataSource</span><span class="sxs-lookup"><span data-stu-id="16e98-203">ODBCDataSource</span></span>](odbcdatasource-table.md)
-   [<span data-ttu-id="16e98-204">ODBCDriver</span><span class="sxs-lookup"><span data-stu-id="16e98-204">ODBCDriver</span></span>](odbcdriver-table.md)
-   [<span data-ttu-id="16e98-205">ODBCSourceAttribute</span><span class="sxs-lookup"><span data-stu-id="16e98-205">ODBCSourceAttribute</span></span>](odbcsourceattribute-table.md)
-   [<span data-ttu-id="16e98-206">ODBCTranslator</span><span class="sxs-lookup"><span data-stu-id="16e98-206">ODBCTranslator</span></span>](odbctranslator-table.md)
-   [<span data-ttu-id="16e98-207">Tabella ProgID</span><span class="sxs-lookup"><span data-stu-id="16e98-207">ProgID Table</span></span>](progid-table.md)
-   [<span data-ttu-id="16e98-208">Proprietà</span><span class="sxs-lookup"><span data-stu-id="16e98-208">Property</span></span>](property-table.md)
-   [<span data-ttu-id="16e98-209">PublishComponent</span><span class="sxs-lookup"><span data-stu-id="16e98-209">PublishComponent</span></span>](publishcomponent-table.md)
-   [<span data-ttu-id="16e98-210">RadioButton</span><span class="sxs-lookup"><span data-stu-id="16e98-210">RadioButton</span></span>](radiobutton-table.md)
-   [<span data-ttu-id="16e98-211">Tabella del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="16e98-211">Registry Table</span></span>](registry-table.md)
-   [<span data-ttu-id="16e98-212">RegLocator</span><span class="sxs-lookup"><span data-stu-id="16e98-212">RegLocator</span></span>](reglocator-table.md)
-   [<span data-ttu-id="16e98-213">RemoveFile</span><span class="sxs-lookup"><span data-stu-id="16e98-213">RemoveFile</span></span>](removefile-table.md)
-   [<span data-ttu-id="16e98-214">RemoveIniFile</span><span class="sxs-lookup"><span data-stu-id="16e98-214">RemoveIniFile</span></span>](removeinifile-table.md)
-   [<span data-ttu-id="16e98-215">RemoveRegistry</span><span class="sxs-lookup"><span data-stu-id="16e98-215">RemoveRegistry</span></span>](removeregistry-table.md)
-   [<span data-ttu-id="16e98-216">ReserveCost</span><span class="sxs-lookup"><span data-stu-id="16e98-216">ReserveCost</span></span>](reservecost-table.md)
-   [<span data-ttu-id="16e98-217">SelfReg</span><span class="sxs-lookup"><span data-stu-id="16e98-217">SelfReg</span></span>](selfreg-table.md)
-   [<span data-ttu-id="16e98-218">ServiceControl</span><span class="sxs-lookup"><span data-stu-id="16e98-218">ServiceControl</span></span>](servicecontrol-table.md)
-   [<span data-ttu-id="16e98-219">ServiceInstall</span><span class="sxs-lookup"><span data-stu-id="16e98-219">ServiceInstall</span></span>](serviceinstall-table.md)
-   [<span data-ttu-id="16e98-220">Scelte rapide</span><span class="sxs-lookup"><span data-stu-id="16e98-220">Shortcut</span></span>](shortcut-table.md)
-   [<span data-ttu-id="16e98-221">Firma</span><span class="sxs-lookup"><span data-stu-id="16e98-221">Signature</span></span>](signature-table.md)
-   [<span data-ttu-id="16e98-222">TextStyle</span><span class="sxs-lookup"><span data-stu-id="16e98-222">TextStyle</span></span>](textstyle-table.md)
-   [<span data-ttu-id="16e98-223">TypeLib</span><span class="sxs-lookup"><span data-stu-id="16e98-223">TypeLib</span></span>](typelib-table.md)
-   [<span data-ttu-id="16e98-224">UIText</span><span class="sxs-lookup"><span data-stu-id="16e98-224">UIText</span></span>](uitext-table.md)
-   [<span data-ttu-id="16e98-225">Verbo</span><span class="sxs-lookup"><span data-stu-id="16e98-225">Verb</span></span>](verb-table.md)

 

 



