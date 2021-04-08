---
description: La tabella ServiceControl viene utilizzata per controllare i servizi installati o disinstallati. Nota i servizi che si basano sulla presenza di un assembly nella global assembly cache (GAC) non possono essere installati o avviati utilizzando le tabelle ServiceInstall e ServiceControl.
ms.assetid: c51cd9bd-3c55-4eec-ab67-172765adc51c
title: Tabella ServiceControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c2abd123e937673694dffd53773a16fcbd704c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757625"
---
# <a name="servicecontrol-table"></a><span data-ttu-id="aa2b7-103">Tabella ServiceControl</span><span class="sxs-lookup"><span data-stu-id="aa2b7-103">ServiceControl Table</span></span>

<span data-ttu-id="aa2b7-104">La tabella ServiceControl viene utilizzata per controllare i servizi installati o disinstallati.</span><span class="sxs-lookup"><span data-stu-id="aa2b7-104">The ServiceControl table is used to control installed or uninstalled services.</span></span>

> [!Note]  
> <span data-ttu-id="aa2b7-105">I servizi che si basano sulla presenza di un [assembly](assemblies.md) nella global assembly cache (GAC) non possono essere installati o avviati utilizzando le tabelle [ServiceInstall](serviceinstall-table.md) e ServiceControl.</span><span class="sxs-lookup"><span data-stu-id="aa2b7-105">Services that rely on the presence of an [assembly](assemblies.md) in the Global Assembly Cache (GAC) cannot be installed or started using the [ServiceInstall](serviceinstall-table.md) and ServiceControl tables.</span></span> <span data-ttu-id="aa2b7-106">Se è necessario avviare un servizio che dipende da un assembly nella GAC, è necessario utilizzare un'azione personalizzata sequenziata dopo l' [azione InstallFinalize](installfinalize-action.md) o un' [azione personalizzata di commit](commit-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="aa2b7-106">If you need to start a service that depends on an assembly in the GAC, you must use a custom action sequenced after the [InstallFinalize action](installfinalize-action.md) or a [commit custom action](commit-custom-actions.md).</span></span> <span data-ttu-id="aa2b7-107">Per informazioni sull'installazione degli assembly nella GAC, vedere [installazione degli assembly nella global assembly cache](installation-of-assemblies-to-the-global-assembly-cache.md).</span><span class="sxs-lookup"><span data-stu-id="aa2b7-107">For information about installing assemblies to the GAC see [Installation of Assemblies to the Global Assembly Cache](installation-of-assemblies-to-the-global-assembly-cache.md).</span></span>

 

<span data-ttu-id="aa2b7-108">La tabella ServiceControl include le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="aa2b7-108">The ServiceControl table has the following columns.</span></span>



| <span data-ttu-id="aa2b7-109">Colonna</span><span class="sxs-lookup"><span data-stu-id="aa2b7-109">Column</span></span>         | <span data-ttu-id="aa2b7-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="aa2b7-110">Type</span></span>                         | <span data-ttu-id="aa2b7-111">Chiave</span><span class="sxs-lookup"><span data-stu-id="aa2b7-111">Key</span></span> | <span data-ttu-id="aa2b7-112">Nullable</span><span class="sxs-lookup"><span data-stu-id="aa2b7-112">Nullable</span></span> |
|----------------|------------------------------|-----|----------|
| <span data-ttu-id="aa2b7-113">ServiceControl</span><span class="sxs-lookup"><span data-stu-id="aa2b7-113">ServiceControl</span></span> | [<span data-ttu-id="aa2b7-114">Identificatore</span><span class="sxs-lookup"><span data-stu-id="aa2b7-114">Identifier</span></span>](identifier.md) | <span data-ttu-id="aa2b7-115">S</span><span class="sxs-lookup"><span data-stu-id="aa2b7-115">Y</span></span>   | <span data-ttu-id="aa2b7-116">N</span><span class="sxs-lookup"><span data-stu-id="aa2b7-116">N</span></span>        |
| <span data-ttu-id="aa2b7-117">Nome</span><span class="sxs-lookup"><span data-stu-id="aa2b7-117">Name</span></span>           | [<span data-ttu-id="aa2b7-118">Formattato</span><span class="sxs-lookup"><span data-stu-id="aa2b7-118">Formatted</span></span>](formatted.md)   | <span data-ttu-id="aa2b7-119">N</span><span class="sxs-lookup"><span data-stu-id="aa2b7-119">N</span></span>   | <span data-ttu-id="aa2b7-120">N</span><span class="sxs-lookup"><span data-stu-id="aa2b7-120">N</span></span>        |
| <span data-ttu-id="aa2b7-121">Evento</span><span class="sxs-lookup"><span data-stu-id="aa2b7-121">Event</span></span>          | [<span data-ttu-id="aa2b7-122">Integer</span><span class="sxs-lookup"><span data-stu-id="aa2b7-122">Integer</span></span>](integer.md)       | <span data-ttu-id="aa2b7-123">N</span><span class="sxs-lookup"><span data-stu-id="aa2b7-123">N</span></span>   | <span data-ttu-id="aa2b7-124">N</span><span class="sxs-lookup"><span data-stu-id="aa2b7-124">N</span></span>        |
| <span data-ttu-id="aa2b7-125">Argomenti</span><span class="sxs-lookup"><span data-stu-id="aa2b7-125">Arguments</span></span>      | [<span data-ttu-id="aa2b7-126">Formattato</span><span class="sxs-lookup"><span data-stu-id="aa2b7-126">Formatted</span></span>](formatted.md)   | <span data-ttu-id="aa2b7-127">N</span><span class="sxs-lookup"><span data-stu-id="aa2b7-127">N</span></span>   | <span data-ttu-id="aa2b7-128">S</span><span class="sxs-lookup"><span data-stu-id="aa2b7-128">Y</span></span>        |
| <span data-ttu-id="aa2b7-129">Attesa</span><span class="sxs-lookup"><span data-stu-id="aa2b7-129">Wait</span></span>           | [<span data-ttu-id="aa2b7-130">Integer</span><span class="sxs-lookup"><span data-stu-id="aa2b7-130">Integer</span></span>](integer.md)       | <span data-ttu-id="aa2b7-131">N</span><span class="sxs-lookup"><span data-stu-id="aa2b7-131">N</span></span>   | <span data-ttu-id="aa2b7-132">S</span><span class="sxs-lookup"><span data-stu-id="aa2b7-132">Y</span></span>        |
| <span data-ttu-id="aa2b7-133">Componente\_</span><span class="sxs-lookup"><span data-stu-id="aa2b7-133">Component\_</span></span>    | [<span data-ttu-id="aa2b7-134">Identificatore</span><span class="sxs-lookup"><span data-stu-id="aa2b7-134">Identifier</span></span>](identifier.md) | <span data-ttu-id="aa2b7-135">N</span><span class="sxs-lookup"><span data-stu-id="aa2b7-135">N</span></span>   | <span data-ttu-id="aa2b7-136">N</span><span class="sxs-lookup"><span data-stu-id="aa2b7-136">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="aa2b7-137">Colonne</span><span class="sxs-lookup"><span data-stu-id="aa2b7-137">Columns</span></span>

<dl> <dt>

<span data-ttu-id="aa2b7-138"><span id="ServiceControl"></span><span id="servicecontrol"></span><span id="SERVICECONTROL"></span>ServiceControl</span><span class="sxs-lookup"><span data-stu-id="aa2b7-138"><span id="ServiceControl"></span><span id="servicecontrol"></span><span id="SERVICECONTROL"></span>ServiceControl</span></span>
</dt> <dd>

<span data-ttu-id="aa2b7-139">Si tratta della chiave primaria della tabella.</span><span class="sxs-lookup"><span data-stu-id="aa2b7-139">This is the primary key of this table.</span></span>

</dd> <dt>

<span data-ttu-id="aa2b7-140"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Nome</span><span class="sxs-lookup"><span data-stu-id="aa2b7-140"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="aa2b7-141">Questa colonna è la stringa che denomina il servizio.</span><span class="sxs-lookup"><span data-stu-id="aa2b7-141">This column is the string naming the service.</span></span> <span data-ttu-id="aa2b7-142">Questa colonna può essere utilizzata per controllare un servizio non installato.</span><span class="sxs-lookup"><span data-stu-id="aa2b7-142">This column can be used to control a service that is not installed.</span></span>

</dd> <dt>

<span data-ttu-id="aa2b7-143"><span id="Event"></span><span id="event"></span><span id="EVENT"></span>Evento</span><span class="sxs-lookup"><span data-stu-id="aa2b7-143"><span id="Event"></span><span id="event"></span><span id="EVENT"></span>Event</span></span>
</dt> <dd>

<span data-ttu-id="aa2b7-144">Questa colonna contiene le operazioni da eseguire sul servizio denominato.</span><span class="sxs-lookup"><span data-stu-id="aa2b7-144">This column contains the operations to be performed on the named service.</span></span> <span data-ttu-id="aa2b7-145">Si noti che quando si arresta un servizio, vengono arrestati anche tutti i servizi che dipendono da tale servizio.</span><span class="sxs-lookup"><span data-stu-id="aa2b7-145">Note that when stopping a service, all services that depend on that service are also stopped.</span></span> <span data-ttu-id="aa2b7-146">Quando si elimina un servizio che esegue, il programma di installazione interrompe il servizio.</span><span class="sxs-lookup"><span data-stu-id="aa2b7-146">When deleting a service that is running, the installer stops the service.</span></span>

<span data-ttu-id="aa2b7-147">I valori in questo campo sono campi di bit che possono essere combinati in un singolo valore che rappresenta diverse operazioni.</span><span class="sxs-lookup"><span data-stu-id="aa2b7-147">The values in this field are bit fields that can be combined into a single value that represents several operations.</span></span>

<span data-ttu-id="aa2b7-148">I valori seguenti vengono utilizzati solo durante un'installazione.</span><span class="sxs-lookup"><span data-stu-id="aa2b7-148">The following values are only used during an installation.</span></span>



| <span data-ttu-id="aa2b7-149">Costante</span><span class="sxs-lookup"><span data-stu-id="aa2b7-149">Constant</span></span>                           | <span data-ttu-id="aa2b7-150">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="aa2b7-150">Hexadecimal</span></span> | <span data-ttu-id="aa2b7-151">Decimal</span><span class="sxs-lookup"><span data-stu-id="aa2b7-151">Decimal</span></span> | <span data-ttu-id="aa2b7-152">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aa2b7-152">Description</span></span>                                                                        |
|------------------------------------|-------------|---------|------------------------------------------------------------------------------------|
| <span data-ttu-id="aa2b7-153">**msidbServiceControlEventStart**</span><span class="sxs-lookup"><span data-stu-id="aa2b7-153">**msidbServiceControlEventStart**</span></span>  | <span data-ttu-id="aa2b7-154">0x001</span><span class="sxs-lookup"><span data-stu-id="aa2b7-154">0x001</span></span>       | <span data-ttu-id="aa2b7-155">1</span><span class="sxs-lookup"><span data-stu-id="aa2b7-155">1</span></span>       | <span data-ttu-id="aa2b7-156">Avvia il servizio durante l' [azione StartServices](startservices-action.md).</span><span class="sxs-lookup"><span data-stu-id="aa2b7-156">Starts the service during the [StartServices action](startservices-action.md).</span></span>    |
| <span data-ttu-id="aa2b7-157">**msidbServiceControlEventStop**</span><span class="sxs-lookup"><span data-stu-id="aa2b7-157">**msidbServiceControlEventStop**</span></span>   | <span data-ttu-id="aa2b7-158">0x002</span><span class="sxs-lookup"><span data-stu-id="aa2b7-158">0x002</span></span>       | <span data-ttu-id="aa2b7-159">2</span><span class="sxs-lookup"><span data-stu-id="aa2b7-159">2</span></span>       | <span data-ttu-id="aa2b7-160">Arresta il servizio durante l' [azione StopServices](stopservices-action.md).</span><span class="sxs-lookup"><span data-stu-id="aa2b7-160">Stops the service during the [StopServices action](stopservices-action.md).</span></span>       |
| <span data-ttu-id="aa2b7-161">(nessuna)</span><span class="sxs-lookup"><span data-stu-id="aa2b7-161">(none)</span></span>                             | <span data-ttu-id="aa2b7-162">0x004</span><span class="sxs-lookup"><span data-stu-id="aa2b7-162">0x004</span></span>       | <span data-ttu-id="aa2b7-163">4</span><span class="sxs-lookup"><span data-stu-id="aa2b7-163">4</span></span>       | <reserved>                                                                   |
| <span data-ttu-id="aa2b7-164">**msidbServiceControlEventDelete**</span><span class="sxs-lookup"><span data-stu-id="aa2b7-164">**msidbServiceControlEventDelete**</span></span> | <span data-ttu-id="aa2b7-165">0x008</span><span class="sxs-lookup"><span data-stu-id="aa2b7-165">0x008</span></span>       | <span data-ttu-id="aa2b7-166">8</span><span class="sxs-lookup"><span data-stu-id="aa2b7-166">8</span></span>       | <span data-ttu-id="aa2b7-167">Elimina il servizio durante l' [azione DeleteServices](deleteservices-action.md).</span><span class="sxs-lookup"><span data-stu-id="aa2b7-167">Deletes the service during the [DeleteServices action](deleteservices-action.md).</span></span> |



 

<span data-ttu-id="aa2b7-168">I valori seguenti vengono utilizzati solo durante una disinstallazione.</span><span class="sxs-lookup"><span data-stu-id="aa2b7-168">The following values are only used during an uninstall.</span></span>



| <span data-ttu-id="aa2b7-169">Costante</span><span class="sxs-lookup"><span data-stu-id="aa2b7-169">Constant</span></span>                                    | <span data-ttu-id="aa2b7-170">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="aa2b7-170">Hexadecimal</span></span> | <span data-ttu-id="aa2b7-171">Decimal</span><span class="sxs-lookup"><span data-stu-id="aa2b7-171">Decimal</span></span> | <span data-ttu-id="aa2b7-172">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aa2b7-172">Description</span></span>                                                                        |
|---------------------------------------------|-------------|---------|------------------------------------------------------------------------------------|
| <span data-ttu-id="aa2b7-173">**msidbServiceControlEventUninstallStart**</span><span class="sxs-lookup"><span data-stu-id="aa2b7-173">**msidbServiceControlEventUninstallStart**</span></span>  | <span data-ttu-id="aa2b7-174">0x010</span><span class="sxs-lookup"><span data-stu-id="aa2b7-174">0x010</span></span>       | <span data-ttu-id="aa2b7-175">16</span><span class="sxs-lookup"><span data-stu-id="aa2b7-175">16</span></span>      | <span data-ttu-id="aa2b7-176">Avvia il servizio durante l' [azione StartServices](startservices-action.md).</span><span class="sxs-lookup"><span data-stu-id="aa2b7-176">Starts the service during the [StartServices action](startservices-action.md).</span></span>    |
| <span data-ttu-id="aa2b7-177">**msidbServiceControlEventUninstallStop**</span><span class="sxs-lookup"><span data-stu-id="aa2b7-177">**msidbServiceControlEventUninstallStop**</span></span>   | <span data-ttu-id="aa2b7-178">0x020</span><span class="sxs-lookup"><span data-stu-id="aa2b7-178">0x020</span></span>       | <span data-ttu-id="aa2b7-179">32</span><span class="sxs-lookup"><span data-stu-id="aa2b7-179">32</span></span>      | <span data-ttu-id="aa2b7-180">Arresta il servizio durante l' [azione StopServices](stopservices-action.md).</span><span class="sxs-lookup"><span data-stu-id="aa2b7-180">Stops the service during the [StopServices action](stopservices-action.md).</span></span>       |
| <span data-ttu-id="aa2b7-181">(nessuna)</span><span class="sxs-lookup"><span data-stu-id="aa2b7-181">(none)</span></span>                                      | <span data-ttu-id="aa2b7-182">0x040</span><span class="sxs-lookup"><span data-stu-id="aa2b7-182">0x040</span></span>       | <span data-ttu-id="aa2b7-183">64</span><span class="sxs-lookup"><span data-stu-id="aa2b7-183">64</span></span>      | <reserved>                                                                   |
| <span data-ttu-id="aa2b7-184">**msidbServiceControlEventUninstallDelete**</span><span class="sxs-lookup"><span data-stu-id="aa2b7-184">**msidbServiceControlEventUninstallDelete**</span></span> | <span data-ttu-id="aa2b7-185">0x080</span><span class="sxs-lookup"><span data-stu-id="aa2b7-185">0x080</span></span>       | <span data-ttu-id="aa2b7-186">128</span><span class="sxs-lookup"><span data-stu-id="aa2b7-186">128</span></span>     | <span data-ttu-id="aa2b7-187">Elimina il servizio durante l' [azione DeleteServices](deleteservices-action.md).</span><span class="sxs-lookup"><span data-stu-id="aa2b7-187">Deletes the service during the [DeleteServices action](deleteservices-action.md).</span></span> |



 

</dd> <dt>

<span data-ttu-id="aa2b7-188"><span id="Arguments"></span><span id="arguments"></span><span id="ARGUMENTS"></span>Argomenti</span><span class="sxs-lookup"><span data-stu-id="aa2b7-188"><span id="Arguments"></span><span id="arguments"></span><span id="ARGUMENTS"></span>Arguments</span></span>
</dt> <dd>

<span data-ttu-id="aa2b7-189">Elenco di argomenti per l'avvio dei servizi.</span><span class="sxs-lookup"><span data-stu-id="aa2b7-189">A list of arguments for starting services.</span></span> <span data-ttu-id="aa2b7-190">Gli argomenti sono separati da caratteri null \[ ~ \] .</span><span class="sxs-lookup"><span data-stu-id="aa2b7-190">The arguments are separated by null characters \[~\].</span></span> <span data-ttu-id="aa2b7-191">Ad esempio, l'elenco di argomenti uno, due e tre è elencato come: uno \[ ~ \] due \[ ~ \] tre.</span><span class="sxs-lookup"><span data-stu-id="aa2b7-191">For example, the list of arguments One, Two, and Three are listed as: One\[~\]Two\[~\]Three.</span></span>

</dd> <dt>

<span data-ttu-id="aa2b7-192"><span id="Wait"></span><span id="wait"></span><span id="WAIT"></span>Attendere</span><span class="sxs-lookup"><span data-stu-id="aa2b7-192"><span id="Wait"></span><span id="wait"></span><span id="WAIT"></span>Wait</span></span>
</dt> <dd>

<span data-ttu-id="aa2b7-193">Se si lascia il campo null o si immette un valore pari a 1, il programma di installazione attenderà un massimo di 30 secondi per il completamento del servizio prima di procedere.</span><span class="sxs-lookup"><span data-stu-id="aa2b7-193">Leaving this field null or entering a value of 1 causes the installer to wait a maximum of 30 seconds for the service to complete before proceeding.</span></span> <span data-ttu-id="aa2b7-194">L'attesa può essere usata per consentire un ulteriore tempo a un evento critico per restituire un errore di errore.</span><span class="sxs-lookup"><span data-stu-id="aa2b7-194">The wait can be used to allow additional time for a critical event to return a failure error.</span></span> <span data-ttu-id="aa2b7-195">Il valore 0 in questo campo significa attendere solo che il gestore di controllo del servizio (SCM) segnali che questo servizio è in uno stato in sospeso prima di continuare con l'installazione.</span><span class="sxs-lookup"><span data-stu-id="aa2b7-195">A value of 0 in this field means to wait only until the service control manager (SCM) reports that this service is in a pending state before continuing with the installation.</span></span>

</dd> <dt>

<span data-ttu-id="aa2b7-196"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_</span><span class="sxs-lookup"><span data-stu-id="aa2b7-196"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="aa2b7-197">Chiave esterna per la colonna uno della [tabella dei componenti](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="aa2b7-197">External key to column one of the [Component Table](component-table.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aa2b7-198">Commenti</span><span class="sxs-lookup"><span data-stu-id="aa2b7-198">Remarks</span></span>

<span data-ttu-id="aa2b7-199">Le azioni [StartServices](startservices-action.md), [StopServices](stopservices-action.md)e [DeleteServices](deleteservices-action.md) nelle [*tabelle di sequenza*](s-gly.md) elaborano le informazioni contenute in questa tabella.</span><span class="sxs-lookup"><span data-stu-id="aa2b7-199">The [StartServices](startservices-action.md), [StopServices](stopservices-action.md), and [DeleteServices](deleteservices-action.md) actions in [*sequence tables*](s-gly.md) process the information in this table.</span></span> <span data-ttu-id="aa2b7-200">Per informazioni sull'utilizzo di *tabelle di sequenza*, vedere [utilizzo di una tabella di sequenza](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="aa2b7-200">For information about using *sequence tables*, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

<span data-ttu-id="aa2b7-201">Utilizzare la colonna nome per avviare, arrestare o eliminare i servizi che vengono sostituiti dall'installazione di o che dipendono da un nuovo servizio installato.</span><span class="sxs-lookup"><span data-stu-id="aa2b7-201">Use the Name column to start, stop, or delete services that are being replaced by the installation or that are dependent upon a new service that is being installed.</span></span> <span data-ttu-id="aa2b7-202">Ad esempio, l'immissione di un servizio nella colonna ServiceControl può associare il servizio a un componente nella \_ colonna Component.</span><span class="sxs-lookup"><span data-stu-id="aa2b7-202">For example, entering MyService into the ServiceControl column can tie this service to MyComponent in the Component\_ column.</span></span> <span data-ttu-id="aa2b7-203">Se il campo di bit nella colonna evento è impostato su Avvia durante l'installazione, il programma di installazione avvia il servizio durante l'installazione di componente.</span><span class="sxs-lookup"><span data-stu-id="aa2b7-203">If the bit field in the Event column is set for start while installing, then the installer starts MyService when installing MyComponent.</span></span>

## <a name="validation"></a><span data-ttu-id="aa2b7-204">Convalida</span><span class="sxs-lookup"><span data-stu-id="aa2b7-204">Validation</span></span>

<dl>

[<span data-ttu-id="aa2b7-205">ICE03</span><span class="sxs-lookup"><span data-stu-id="aa2b7-205">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="aa2b7-206">ICE06</span><span class="sxs-lookup"><span data-stu-id="aa2b7-206">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="aa2b7-207">ICE32</span><span class="sxs-lookup"><span data-stu-id="aa2b7-207">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="aa2b7-208">ICE45</span><span class="sxs-lookup"><span data-stu-id="aa2b7-208">ICE45</span></span>](ice45.md)  
[<span data-ttu-id="aa2b7-209">ICE46</span><span class="sxs-lookup"><span data-stu-id="aa2b7-209">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="aa2b7-210">ICE69</span><span class="sxs-lookup"><span data-stu-id="aa2b7-210">ICE69</span></span>](ice69.md)  
</dl>

 

 



