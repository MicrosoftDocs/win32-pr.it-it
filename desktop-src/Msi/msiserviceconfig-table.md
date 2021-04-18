---
description: La tabella MsiServiceConfig configura un servizio installato o installato dal pacchetto corrente.
ms.assetid: 0d9fd005-9326-4a18-8496-35b5d1927f47
title: Tabella MsiServiceConfig
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 357b6787e56d52a893dd1a118a3e2fcbc13379e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316263"
---
# <a name="msiserviceconfig-table"></a><span data-ttu-id="8ce94-103">Tabella MsiServiceConfig</span><span class="sxs-lookup"><span data-stu-id="8ce94-103">MsiServiceConfig Table</span></span>

<span data-ttu-id="8ce94-104">La tabella MsiServiceConfig configura un servizio installato o installato dal pacchetto corrente.</span><span class="sxs-lookup"><span data-stu-id="8ce94-104">The MsiServiceConfig table configures a service that is installed or being installed by the current package.</span></span>

<span data-ttu-id="8ce94-105">**[Windows Installer 4,5 o versioni precedenti](not-supported-in-windows-installer-4-5.md):** Non supportato.</span><span class="sxs-lookup"><span data-stu-id="8ce94-105">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="8ce94-106">Questa tabella è disponibile a partire da Windows Installer 5,0.</span><span class="sxs-lookup"><span data-stu-id="8ce94-106">This table is available beginning with Windows Installer 5.0.</span></span>

<span data-ttu-id="8ce94-107">La tabella MsiServiceConfig include le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="8ce94-107">The MsiServiceConfig table has the following columns.</span></span>



| <span data-ttu-id="8ce94-108">Colonna</span><span class="sxs-lookup"><span data-stu-id="8ce94-108">Column</span></span>           | <span data-ttu-id="8ce94-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="8ce94-109">Type</span></span>                         | <span data-ttu-id="8ce94-110">Chiave</span><span class="sxs-lookup"><span data-stu-id="8ce94-110">Key</span></span> | <span data-ttu-id="8ce94-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="8ce94-111">Nullable</span></span> |
|------------------|------------------------------|-----|----------|
| <span data-ttu-id="8ce94-112">MsiServiceConfig</span><span class="sxs-lookup"><span data-stu-id="8ce94-112">MsiServiceConfig</span></span> | [<span data-ttu-id="8ce94-113">Identificatore</span><span class="sxs-lookup"><span data-stu-id="8ce94-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="8ce94-114">S</span><span class="sxs-lookup"><span data-stu-id="8ce94-114">Y</span></span>   | <span data-ttu-id="8ce94-115">N</span><span class="sxs-lookup"><span data-stu-id="8ce94-115">N</span></span>        |
| <span data-ttu-id="8ce94-116">Nome</span><span class="sxs-lookup"><span data-stu-id="8ce94-116">Name</span></span>             | [<span data-ttu-id="8ce94-117">Formattato</span><span class="sxs-lookup"><span data-stu-id="8ce94-117">Formatted</span></span>](formatted.md)   | <span data-ttu-id="8ce94-118">N</span><span class="sxs-lookup"><span data-stu-id="8ce94-118">N</span></span>   | <span data-ttu-id="8ce94-119">N</span><span class="sxs-lookup"><span data-stu-id="8ce94-119">N</span></span>        |
| <span data-ttu-id="8ce94-120">Evento</span><span class="sxs-lookup"><span data-stu-id="8ce94-120">Event</span></span>            | [<span data-ttu-id="8ce94-121">Integer</span><span class="sxs-lookup"><span data-stu-id="8ce94-121">Integer</span></span>](integer.md)       | <span data-ttu-id="8ce94-122">N</span><span class="sxs-lookup"><span data-stu-id="8ce94-122">N</span></span>   | <span data-ttu-id="8ce94-123">N</span><span class="sxs-lookup"><span data-stu-id="8ce94-123">N</span></span>        |
| <span data-ttu-id="8ce94-124">TipoConfigurazione</span><span class="sxs-lookup"><span data-stu-id="8ce94-124">ConfigType</span></span>       | [<span data-ttu-id="8ce94-125">Integer</span><span class="sxs-lookup"><span data-stu-id="8ce94-125">Integer</span></span>](integer.md)       | <span data-ttu-id="8ce94-126">N</span><span class="sxs-lookup"><span data-stu-id="8ce94-126">N</span></span>   | <span data-ttu-id="8ce94-127">N</span><span class="sxs-lookup"><span data-stu-id="8ce94-127">N</span></span>        |
| <span data-ttu-id="8ce94-128">Argomento</span><span class="sxs-lookup"><span data-stu-id="8ce94-128">Argument</span></span>         | [<span data-ttu-id="8ce94-129">Formattato</span><span class="sxs-lookup"><span data-stu-id="8ce94-129">Formatted</span></span>](formatted.md)   | <span data-ttu-id="8ce94-130">N</span><span class="sxs-lookup"><span data-stu-id="8ce94-130">N</span></span>   | <span data-ttu-id="8ce94-131">S</span><span class="sxs-lookup"><span data-stu-id="8ce94-131">Y</span></span>        |
| <span data-ttu-id="8ce94-132">Componente\_</span><span class="sxs-lookup"><span data-stu-id="8ce94-132">Component\_</span></span>      | [<span data-ttu-id="8ce94-133">Identificatore</span><span class="sxs-lookup"><span data-stu-id="8ce94-133">Identifier</span></span>](identifier.md) | <span data-ttu-id="8ce94-134">N</span><span class="sxs-lookup"><span data-stu-id="8ce94-134">N</span></span>   | <span data-ttu-id="8ce94-135">N</span><span class="sxs-lookup"><span data-stu-id="8ce94-135">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="8ce94-136">Colonne</span><span class="sxs-lookup"><span data-stu-id="8ce94-136">Columns</span></span>

<dl> <dt>

<span data-ttu-id="8ce94-137"><span id="MsiServiceConfig"></span><span id="msiserviceconfig"></span><span id="MSISERVICECONFIG"></span>MsiServiceConfig</span><span class="sxs-lookup"><span data-stu-id="8ce94-137"><span id="MsiServiceConfig"></span><span id="msiserviceconfig"></span><span id="MSISERVICECONFIG"></span>MsiServiceConfig</span></span>
</dt> <dd>

<span data-ttu-id="8ce94-138">Si tratta della chiave primaria della tabella.</span><span class="sxs-lookup"><span data-stu-id="8ce94-138">This is the primary key of this table.</span></span>

</dd> <dt>

<span data-ttu-id="8ce94-139"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Nome</span><span class="sxs-lookup"><span data-stu-id="8ce94-139"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="8ce94-140">Questa colonna contiene il nome di un servizio che fa parte di questo pacchetto o che è già installato.</span><span class="sxs-lookup"><span data-stu-id="8ce94-140">This column contains the name of a service that is a part of this package or that is already is installed.</span></span>

</dd> <dt>

<span data-ttu-id="8ce94-141"><span id="Event"></span><span id="event"></span><span id="EVENT"></span>Evento</span><span class="sxs-lookup"><span data-stu-id="8ce94-141"><span id="Event"></span><span id="event"></span><span id="EVENT"></span>Event</span></span>
</dt> <dd>

<span data-ttu-id="8ce94-142">In questa colonna viene specificato quando modificare la configurazione del servizio.</span><span class="sxs-lookup"><span data-stu-id="8ce94-142">This column specifies when to change the service configuration.</span></span> <span data-ttu-id="8ce94-143">È possibile combinare i valori seguenti per rappresentare più operazioni.</span><span class="sxs-lookup"><span data-stu-id="8ce94-143">The following values can be combined to represent multiple operations.</span></span> <span data-ttu-id="8ce94-144">Tutti i valori inclusi non vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="8ce94-144">Any values included other than these are ignored.</span></span>



| <span data-ttu-id="8ce94-145">Costante</span><span class="sxs-lookup"><span data-stu-id="8ce94-145">Constant</span></span>                                         | <span data-ttu-id="8ce94-146">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8ce94-146">Description</span></span>                                              |
|--------------------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="8ce94-147">**msidbServiceConfigEventInstall** 1</span><span class="sxs-lookup"><span data-stu-id="8ce94-147">**msidbServiceConfigEventInstall** 1</span></span><br/>   | <span data-ttu-id="8ce94-148">Esegue l'azione durante l'installazione del componente.</span><span class="sxs-lookup"><span data-stu-id="8ce94-148">Takes the action during installation of the component.</span></span>   |
| <span data-ttu-id="8ce94-149">**msidbServiceConfigEventUninstall** 2</span><span class="sxs-lookup"><span data-stu-id="8ce94-149">**msidbServiceConfigEventUninstall** 2</span></span><br/> | <span data-ttu-id="8ce94-150">Esegue l'azione durante la disinstallazione del componente.</span><span class="sxs-lookup"><span data-stu-id="8ce94-150">Takes the action during uninstallation of the component.</span></span> |
| <span data-ttu-id="8ce94-151">**msidbServiceConfigEventReinstall** 4</span><span class="sxs-lookup"><span data-stu-id="8ce94-151">**msidbServiceConfigEventReinstall** 4</span></span><br/> | <span data-ttu-id="8ce94-152">Esegue l'azione durante la reinstallazione del componente.</span><span class="sxs-lookup"><span data-stu-id="8ce94-152">Takes the action during reinstallation of the component.</span></span> |



 

</dd> <dt>

<span data-ttu-id="8ce94-153"><span id="ConfigType"></span><span id="configtype"></span><span id="CONFIGTYPE"></span>ConfigType</span><span class="sxs-lookup"><span data-stu-id="8ce94-153"><span id="ConfigType"></span><span id="configtype"></span><span id="CONFIGTYPE"></span>ConfigType</span></span>
</dt> <dd>

<span data-ttu-id="8ce94-154">Il valore in questo campo, combinato con il valore nel campo arguments, specifica la modifica da apportare alla configurazione del servizio.</span><span class="sxs-lookup"><span data-stu-id="8ce94-154">The value in this field, combined with the value in the Arguments field, specify what change to make to the service configuration.</span></span> <span data-ttu-id="8ce94-155">La modifica specificata viene applicata alla successiva avvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="8ce94-155">The specified change takes effect the next time the system is started.</span></span>



| <span data-ttu-id="8ce94-156">File di configurazione</span><span class="sxs-lookup"><span data-stu-id="8ce94-156">Config</span></span>                                                      | <span data-ttu-id="8ce94-157">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8ce94-157">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ce94-158">**Servizio \_ di CONFIGURAZIONE \_ \_ \_ avvio automatico ritardato** 3</span><span class="sxs-lookup"><span data-stu-id="8ce94-158">**SERVICE\_CONFIG\_DELAYED\_AUTO\_START** 3</span></span><br/>       | <span data-ttu-id="8ce94-159">Configurare il tempo di attesa di un [servizio di avvio automatico](../services/automatically-starting-services.md).</span><span class="sxs-lookup"><span data-stu-id="8ce94-159">Configure the time delay of an [auto-start service](../services/automatically-starting-services.md).</span></span> <br/> <span data-ttu-id="8ce94-160">Immettere 1 nel campo argument per avviare il servizio dopo altri servizi di avvio automatico, oltre a un ritardo di tempo.</span><span class="sxs-lookup"><span data-stu-id="8ce94-160">Enter 1 in the Argument field to start the service after other auto-start services plus a time delay.</span></span> <br/> <span data-ttu-id="8ce94-161">Immettere 0 nel campo argument per disattivare il ritardo del servizio di avvio automatico.</span><span class="sxs-lookup"><span data-stu-id="8ce94-161">Enter 0 in the Argument field to turn off the auto-start service delay.</span></span><br/> <span data-ttu-id="8ce94-162">Si applica solo ai servizi o ai servizi di avvio automatico installati da questo pacchetto **con \_ \_ avvio automatico del servizio** nel campo StartType della [tabella ServiceInstall](serviceinstall-table.md).</span><span class="sxs-lookup"><span data-stu-id="8ce94-162">Applies only to installed auto-start services or services installed by this package with **SERVICE\_AUTO\_START** in the StartType field of the [ServiceInstall table](serviceinstall-table.md).</span></span><br/>                                                                         |
| <span data-ttu-id="8ce94-163">**Servizio \_ di CONFIGURARE \_ i \_ privilegi richiesti \_ informazioni** 6</span><span class="sxs-lookup"><span data-stu-id="8ce94-163">**SERVICE\_CONFIG\_REQUIRED\_PRIVILEGES\_INFO** 6</span></span><br/> | <span data-ttu-id="8ce94-164">Modificare l'elenco dei privilegi richiesti dal servizio.</span><span class="sxs-lookup"><span data-stu-id="8ce94-164">Change the list of privileges required by the service.</span></span><br/> <span data-ttu-id="8ce94-165">Immettere un elenco di privilegi richiesti nel campo argomento.</span><span class="sxs-lookup"><span data-stu-id="8ce94-165">Enter a list of requested privileges in the Argument field.</span></span> <span data-ttu-id="8ce94-166">Il valore stringa [formattato](formatted.md) nel campo argument elenca le [**costanti Privilege**](../secauthz/privilege-constants.md) per i privilegi richiesti.</span><span class="sxs-lookup"><span data-stu-id="8ce94-166">The [Formatted](formatted.md) string value in the Argument field lists the [**Privilege Constants**](../secauthz/privilege-constants.md) for the requested privileges.</span></span> <span data-ttu-id="8ce94-167">È possibile utilizzare la \[ ~ \] sintassi della stringa [formattata](formatted.md) per inserire un carattere null.</span><span class="sxs-lookup"><span data-stu-id="8ce94-167">You can use the \[~\] syntax of the [Formatted](formatted.md) string to insert a null character.</span></span> <span data-ttu-id="8ce94-168">Separare le costanti Privilege nell'elenco in base a \[ ~ \] .</span><span class="sxs-lookup"><span data-stu-id="8ce94-168">Separate the privilege constants in the list by \[~\].</span></span><br/>                                                                                                                              |
| <span data-ttu-id="8ce94-169">**Servizio \_ di \_ \_ \_ Informazioni SID servizio di configurazione** 5</span><span class="sxs-lookup"><span data-stu-id="8ce94-169">**SERVICE\_CONFIG\_SERVICE\_SID\_INFO** 5</span></span><br/>         | <span data-ttu-id="8ce94-170">Aggiungere un tipo di SID del servizio al token di processo che contiene il servizio.</span><span class="sxs-lookup"><span data-stu-id="8ce94-170">Add a service SID type to the process token containing this service.</span></span><br/> <span data-ttu-id="8ce94-171">Immettere nel campo argomento un tipo di SID del servizio valido per la struttura delle [**\_ \_ informazioni del SID**](/windows/win32/api/winsvc/ns-winsvc-service_sid_info) del servizio: tipo di SID del servizio **\_ \_ \_ None** (0x00), **tipo di SID del servizio con \_ \_ \_ restrizioni** (0x03) o **tipo di SID del servizio senza \_ \_ \_ restrizioni** (0x01).</span><span class="sxs-lookup"><span data-stu-id="8ce94-171">Enter in the Argument field a valid service SID type for the [**SERVICE\_SID\_INFO**](/windows/win32/api/winsvc/ns-winsvc-service_sid_info) structure: **SERVICE\_SID\_TYPE\_NONE** (0x00), **SERVICE\_SID\_TYPE\_RESTRICTED** (0x03), or **SERVICE\_SID\_TYPE\_UNRESTRICTED** (0x01).</span></span> <br/>                                                                                                                                                                                                                                              |
| <span data-ttu-id="8ce94-172">**Servizio \_ di \_ \_ Informazioni di prespegnimento configurazione** 7</span><span class="sxs-lookup"><span data-stu-id="8ce94-172">**SERVICE\_CONFIG\_PRESHUTDOWN\_INFO** 7</span></span><br/>          | <span data-ttu-id="8ce94-173">Configurare la durata di attesa di [Gestione controllo servizi](../services/service-control-manager.md) prima di procedere con altre operazioni di arresto.</span><span class="sxs-lookup"><span data-stu-id="8ce94-173">Configure the length of the time the [Service Control Manager](../services/service-control-manager.md) (SCM) waits before proceeding with other shutdown operations.</span></span> <span data-ttu-id="8ce94-174">Il servizio SCM attende questo periodo di tempo dopo l'invio della notifica di **\_ \_ prechiusura del controllo del servizio** al servizio.</span><span class="sxs-lookup"><span data-stu-id="8ce94-174">The SCM waits for this period of time after sending the **SERVICE\_CONTROL\_PRESHUTDOWN** notification to the service.</span></span> <br/> <span data-ttu-id="8ce94-175">Immettere la lunghezza del ritardo di tempo, in millisecondi, nel campo argomento.</span><span class="sxs-lookup"><span data-stu-id="8ce94-175">Enter the time delay length, in milliseconds, in the Argument field.</span></span> <span data-ttu-id="8ce94-176">Lasciare vuoto il campo argomento per reimpostare il ritardo di tempo sul valore predefinito di 3 minuti.</span><span class="sxs-lookup"><span data-stu-id="8ce94-176">Leave the Argument field empty to reset the time delay to the default of 3 minutes.</span></span> <br/>                                                                                                                               |
| <span data-ttu-id="8ce94-177">**Servizio \_ di \_ \_ \_ Flag azioni errore configurazione** 4</span><span class="sxs-lookup"><span data-stu-id="8ce94-177">**SERVICE\_CONFIG\_FAILURE\_ACTIONS\_FLAG** 4</span></span><br/>     | <span data-ttu-id="8ce94-178">Configurare quando eseguire le azioni di errore per il servizio.</span><span class="sxs-lookup"><span data-stu-id="8ce94-178">Configure when to run the failure actions for this service.</span></span> <span data-ttu-id="8ce94-179">Questa impostazione viene ignorata se il servizio non dispone di azioni di errore configurate.</span><span class="sxs-lookup"><span data-stu-id="8ce94-179">This setting is ignored if the service has no configured failure actions.</span></span><br/> <span data-ttu-id="8ce94-180">Immettere 0 per eseguire le azioni solo se il servizio termina senza Reporting **Service \_ interrotto**.</span><span class="sxs-lookup"><span data-stu-id="8ce94-180">Enter 0 to run the actions only if the service terminates without reporting **SERVICE\_STOPPED**.</span></span><br/> <span data-ttu-id="8ce94-181">Immettere 1 per eseguire le azioni se il servizio termina il servizio di Reporting **\_ interrotto** e il membro **dwWin32ExitCode** della struttura [**\_ dello stato del servizio**](/windows/win32/api/winsvc/ns-winsvc-service_status) non ha **\_ esito positivo**.</span><span class="sxs-lookup"><span data-stu-id="8ce94-181">Enter 1 to run the actions if the service terminates reporting **SERVICE\_STOPPED** and the **dwWin32ExitCode** member of [**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status) structure is not **ERROR\_SUCCESS**.</span></span> <span data-ttu-id="8ce94-182">Le azioni di errore configurate vengono inoltre eseguite se il servizio termina senza Reporting **Service \_ interrotto**.</span><span class="sxs-lookup"><span data-stu-id="8ce94-182">Configured failure actions are also run if the service terminates without reporting **SERVICE\_STOPPED**.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="8ce94-183"><span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>Argomento</span><span class="sxs-lookup"><span data-stu-id="8ce94-183"><span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>Argument</span></span>
</dt> <dd>

<span data-ttu-id="8ce94-184">Il valore in questo campo, combinato con il valore nel campo ConfigType, specifica la modifica da apportare alla configurazione del servizio.</span><span class="sxs-lookup"><span data-stu-id="8ce94-184">The value in this field, combined with the value in the ConfigType field, specify what change to make to the service configuration.</span></span> <span data-ttu-id="8ce94-185">La modifica specificata viene applicata alla successiva avvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="8ce94-185">The specified change takes effect the next time the system is started.</span></span>

</dd> <dt>

<span data-ttu-id="8ce94-186"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_</span><span class="sxs-lookup"><span data-stu-id="8ce94-186"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="8ce94-187">Chiave esterna per la colonna componente della [tabella dei componenti](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="8ce94-187">External key to the Component column of the [Component Table](component-table.md).</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="8ce94-188">Convalida</span><span class="sxs-lookup"><span data-stu-id="8ce94-188">Validation</span></span>

<dl>

[<span data-ttu-id="8ce94-189">ICE102</span><span class="sxs-lookup"><span data-stu-id="8ce94-189">ICE102</span></span>](ice-102.md)  
[<span data-ttu-id="8ce94-190">ICE03</span><span class="sxs-lookup"><span data-stu-id="8ce94-190">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="8ce94-191">ICE06</span><span class="sxs-lookup"><span data-stu-id="8ce94-191">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="8ce94-192">ICE32</span><span class="sxs-lookup"><span data-stu-id="8ce94-192">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="8ce94-193">ICE45</span><span class="sxs-lookup"><span data-stu-id="8ce94-193">ICE45</span></span>](ice45.md)  
[<span data-ttu-id="8ce94-194">ICE46</span><span class="sxs-lookup"><span data-stu-id="8ce94-194">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="8ce94-195">ICE69</span><span class="sxs-lookup"><span data-stu-id="8ce94-195">ICE69</span></span>](ice69.md)  
</dl>

 

 
