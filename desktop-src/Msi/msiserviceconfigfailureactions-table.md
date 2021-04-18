---
description: La tabella MsiServiceConfigFailureActions elenca le operazioni da eseguire in seguito a un errore del servizio. Le operazioni specificate in questa tabella vengono eseguite la volta successiva che il sistema viene avviato.
ms.assetid: 7c450b74-1f91-4a1c-beee-646a407eb8a8
title: Tabella MsiServiceConfigFailureActions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae55d095e227611271de35d673289fc9eb5b174e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316262"
---
# <a name="msiserviceconfigfailureactions-table"></a><span data-ttu-id="a7581-104">Tabella MsiServiceConfigFailureActions</span><span class="sxs-lookup"><span data-stu-id="a7581-104">MsiServiceConfigFailureActions Table</span></span>

<span data-ttu-id="a7581-105">La tabella MsiServiceConfigFailureActions elenca le operazioni da eseguire in seguito a un errore del servizio.</span><span class="sxs-lookup"><span data-stu-id="a7581-105">The MsiServiceConfigFailureActions table lists operations to be run after a service fails.</span></span> <span data-ttu-id="a7581-106">Le operazioni specificate in questa tabella vengono eseguite la volta successiva che il sistema viene avviato.</span><span class="sxs-lookup"><span data-stu-id="a7581-106">The operations specified in this table run the next time the system is started.</span></span>

<span data-ttu-id="a7581-107">**[Windows Installer 4,5 o versioni precedenti](not-supported-in-windows-installer-4-5.md):** Non supportato.</span><span class="sxs-lookup"><span data-stu-id="a7581-107">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="a7581-108">Questa tabella è disponibile a partire da Windows Installer 5,0.</span><span class="sxs-lookup"><span data-stu-id="a7581-108">This table is available beginning with Windows Installer 5.0.</span></span>

<span data-ttu-id="a7581-109">La tabella MsiServiceConfigFailureActions include le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="a7581-109">The MsiServiceConfigFailureActions table has the following columns.</span></span>



| <span data-ttu-id="a7581-110">Colonna</span><span class="sxs-lookup"><span data-stu-id="a7581-110">Column</span></span>                         | <span data-ttu-id="a7581-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="a7581-111">Type</span></span>                         | <span data-ttu-id="a7581-112">Chiave</span><span class="sxs-lookup"><span data-stu-id="a7581-112">Key</span></span> | <span data-ttu-id="a7581-113">Nullable</span><span class="sxs-lookup"><span data-stu-id="a7581-113">Nullable</span></span> |
|--------------------------------|------------------------------|-----|----------|
| <span data-ttu-id="a7581-114">MsiServiceConfigFailureActions</span><span class="sxs-lookup"><span data-stu-id="a7581-114">MsiServiceConfigFailureActions</span></span> | [<span data-ttu-id="a7581-115">Identificatore</span><span class="sxs-lookup"><span data-stu-id="a7581-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="a7581-116">S</span><span class="sxs-lookup"><span data-stu-id="a7581-116">Y</span></span>   | <span data-ttu-id="a7581-117">N</span><span class="sxs-lookup"><span data-stu-id="a7581-117">N</span></span>        |
| <span data-ttu-id="a7581-118">Nome</span><span class="sxs-lookup"><span data-stu-id="a7581-118">Name</span></span>                           | [<span data-ttu-id="a7581-119">Formattato</span><span class="sxs-lookup"><span data-stu-id="a7581-119">Formatted</span></span>](formatted.md)   | <span data-ttu-id="a7581-120">N</span><span class="sxs-lookup"><span data-stu-id="a7581-120">N</span></span>   | <span data-ttu-id="a7581-121">N</span><span class="sxs-lookup"><span data-stu-id="a7581-121">N</span></span>        |
| <span data-ttu-id="a7581-122">Evento</span><span class="sxs-lookup"><span data-stu-id="a7581-122">Event</span></span>                          | [<span data-ttu-id="a7581-123">Integer</span><span class="sxs-lookup"><span data-stu-id="a7581-123">Integer</span></span>](integer.md)       | <span data-ttu-id="a7581-124">N</span><span class="sxs-lookup"><span data-stu-id="a7581-124">N</span></span>   | <span data-ttu-id="a7581-125">N</span><span class="sxs-lookup"><span data-stu-id="a7581-125">N</span></span>        |
| <span data-ttu-id="a7581-126">ResetPeriod</span><span class="sxs-lookup"><span data-stu-id="a7581-126">ResetPeriod</span></span>                    | [<span data-ttu-id="a7581-127">Integer</span><span class="sxs-lookup"><span data-stu-id="a7581-127">Integer</span></span>](integer.md)       | <span data-ttu-id="a7581-128">N</span><span class="sxs-lookup"><span data-stu-id="a7581-128">N</span></span>   | <span data-ttu-id="a7581-129">S</span><span class="sxs-lookup"><span data-stu-id="a7581-129">Y</span></span>        |
| <span data-ttu-id="a7581-130">RebootMessage</span><span class="sxs-lookup"><span data-stu-id="a7581-130">RebootMessage</span></span>                  | [<span data-ttu-id="a7581-131">Formattato</span><span class="sxs-lookup"><span data-stu-id="a7581-131">Formatted</span></span>](formatted.md)   | <span data-ttu-id="a7581-132">N</span><span class="sxs-lookup"><span data-stu-id="a7581-132">N</span></span>   | <span data-ttu-id="a7581-133">Y</span><span class="sxs-lookup"><span data-stu-id="a7581-133">Y</span></span>        |
| <span data-ttu-id="a7581-134">Comando</span><span class="sxs-lookup"><span data-stu-id="a7581-134">Command</span></span>                        | [<span data-ttu-id="a7581-135">Formattato</span><span class="sxs-lookup"><span data-stu-id="a7581-135">Formatted</span></span>](formatted.md)   | <span data-ttu-id="a7581-136">N</span><span class="sxs-lookup"><span data-stu-id="a7581-136">N</span></span>   | <span data-ttu-id="a7581-137">S</span><span class="sxs-lookup"><span data-stu-id="a7581-137">Y</span></span>        |
| <span data-ttu-id="a7581-138">Azioni</span><span class="sxs-lookup"><span data-stu-id="a7581-138">Actions</span></span>                        | [<span data-ttu-id="a7581-139">Text</span><span class="sxs-lookup"><span data-stu-id="a7581-139">Text</span></span>](text.md)             | <span data-ttu-id="a7581-140">N</span><span class="sxs-lookup"><span data-stu-id="a7581-140">N</span></span>   | <span data-ttu-id="a7581-141">S</span><span class="sxs-lookup"><span data-stu-id="a7581-141">Y</span></span>        |
| <span data-ttu-id="a7581-142">DelayActions</span><span class="sxs-lookup"><span data-stu-id="a7581-142">DelayActions</span></span>                   | [<span data-ttu-id="a7581-143">Text</span><span class="sxs-lookup"><span data-stu-id="a7581-143">Text</span></span>](text.md)             | <span data-ttu-id="a7581-144">N</span><span class="sxs-lookup"><span data-stu-id="a7581-144">N</span></span>   | <span data-ttu-id="a7581-145">S</span><span class="sxs-lookup"><span data-stu-id="a7581-145">Y</span></span>        |
| <span data-ttu-id="a7581-146">Componente\_</span><span class="sxs-lookup"><span data-stu-id="a7581-146">Component\_</span></span>                    | [<span data-ttu-id="a7581-147">Identificatore</span><span class="sxs-lookup"><span data-stu-id="a7581-147">Identifier</span></span>](identifier.md) | <span data-ttu-id="a7581-148">N</span><span class="sxs-lookup"><span data-stu-id="a7581-148">N</span></span>   | <span data-ttu-id="a7581-149">N</span><span class="sxs-lookup"><span data-stu-id="a7581-149">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="a7581-150">Colonne</span><span class="sxs-lookup"><span data-stu-id="a7581-150">Columns</span></span>

<dl> <dt>

<span data-ttu-id="a7581-151"><span id="MsiServiceConfigFailureActions"></span><span id="msiserviceconfigfailureactions"></span><span id="MSISERVICECONFIGFAILUREACTIONS"></span>MsiServiceConfigFailureActions</span><span class="sxs-lookup"><span data-stu-id="a7581-151"><span id="MsiServiceConfigFailureActions"></span><span id="msiserviceconfigfailureactions"></span><span id="MSISERVICECONFIGFAILUREACTIONS"></span>MsiServiceConfigFailureActions</span></span>
</dt> <dd>

<span data-ttu-id="a7581-152">Si tratta della chiave primaria di questa tabella che identifica un'azione non riuscita.</span><span class="sxs-lookup"><span data-stu-id="a7581-152">This is the primary key of this table that identifies a failure action.</span></span>

</dd> <dt>

<span data-ttu-id="a7581-153"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Nome</span><span class="sxs-lookup"><span data-stu-id="a7581-153"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="a7581-154">Questa colonna contiene il nome di un servizio che fa parte di questo pacchetto o che è già installato.</span><span class="sxs-lookup"><span data-stu-id="a7581-154">This column contains the name of a service that is a part of this package or that is already is installed.</span></span>

</dd> <dt>

<span data-ttu-id="a7581-155"><span id="Event"></span><span id="event"></span><span id="EVENT"></span>Evento</span><span class="sxs-lookup"><span data-stu-id="a7581-155"><span id="Event"></span><span id="event"></span><span id="EVENT"></span>Event</span></span>
</dt> <dd>

<span data-ttu-id="a7581-156">In questa colonna viene specificato quando modificare la configurazione del servizio.</span><span class="sxs-lookup"><span data-stu-id="a7581-156">This column specifies when to change the service's configuration.</span></span> <span data-ttu-id="a7581-157">I valori seguenti sono campi di bit che possono essere combinati per rappresentare più operazioni.</span><span class="sxs-lookup"><span data-stu-id="a7581-157">The following values are bit fields that can be combined to represent multiple operations.</span></span> <span data-ttu-id="a7581-158">Qualsiasi altro valore di campo di bit viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="a7581-158">Any other bit field values are ignored.</span></span>



| <span data-ttu-id="a7581-159">Costante</span><span class="sxs-lookup"><span data-stu-id="a7581-159">Constant</span></span>                                         | <span data-ttu-id="a7581-160">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a7581-160">Description</span></span>                                     |
|--------------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="a7581-161">**msidbServiceConfigEventInstall** 1</span><span class="sxs-lookup"><span data-stu-id="a7581-161">**msidbServiceConfigEventInstall** 1</span></span><br/>   | <span data-ttu-id="a7581-162">Modificare durante l'installazione del componente.</span><span class="sxs-lookup"><span data-stu-id="a7581-162">Change during installation of the component.</span></span>    |
| <span data-ttu-id="a7581-163">**msidbServiceConfigEventUninstall** 2</span><span class="sxs-lookup"><span data-stu-id="a7581-163">**msidbServiceConfigEventUninstall** 2</span></span><br/> | <span data-ttu-id="a7581-164">Modifica durante la disinstallazione del componente.</span><span class="sxs-lookup"><span data-stu-id="a7581-164">Change during uninstallation of the component.</span></span>  |
| <span data-ttu-id="a7581-165">**msidbServiceConfigEventReinstall** 4</span><span class="sxs-lookup"><span data-stu-id="a7581-165">**msidbServiceConfigEventReinstall** 4</span></span><br/> | <span data-ttu-id="a7581-166">Modificare durante la riinstallazione del componente.</span><span class="sxs-lookup"><span data-stu-id="a7581-166">Change during re-installation of the component.</span></span> |



 

</dd> <dt>

<span data-ttu-id="a7581-167"><span id="ResetPeriod"></span><span id="resetperiod"></span><span id="RESETPERIOD"></span>ResetPeriod</span><span class="sxs-lookup"><span data-stu-id="a7581-167"><span id="ResetPeriod"></span><span id="resetperiod"></span><span id="RESETPERIOD"></span>ResetPeriod</span></span>
</dt> <dd>

<span data-ttu-id="a7581-168">Periodo di reimpostazione in secondi del conteggio degli errori del servizio.</span><span class="sxs-lookup"><span data-stu-id="a7581-168">The reset period in seconds of service's failure count.</span></span> <span data-ttu-id="a7581-169">[Gestione controllo servizi](../services/service-control-manager.md) conta il numero di volte in cui ogni servizio ha avuto esito negativo dal momento dell'ultimo riavvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="a7581-169">The [Service Control Manager](../services/service-control-manager.md) (SCM) counts the number of times each service has failed since the system was last restarted.</span></span> <span data-ttu-id="a7581-170">Il conteggio viene reimpostato su zero se il servizio non ha esito negativo per il periodo di ripristino.</span><span class="sxs-lookup"><span data-stu-id="a7581-170">The count is reset to zero if the service does not fail for the reset period.</span></span> <span data-ttu-id="a7581-171">Quando il servizio non riesce per l'ennesima volta, il sistema esegue l'azione specificata nell'elemento \[ N-1 \] della matrice specificata nel campo Actions.</span><span class="sxs-lookup"><span data-stu-id="a7581-171">When the service fails for the Nth time, the system performs the action specified in the element \[N-1\] of the array specified in the Actions field.</span></span>

<span data-ttu-id="a7581-172">Lasciare vuoto il campo ResetPeriod per indicare che il numero di errori non deve mai essere reimpostato.</span><span class="sxs-lookup"><span data-stu-id="a7581-172">Leave ResetPeriod field empty to indicate that failure count should never be reset.</span></span>

</dd> <dt>

<span data-ttu-id="a7581-173"><span id="RebootMessage"></span><span id="rebootmessage"></span><span id="REBOOTMESSAGE"></span>RebootMessage</span><span class="sxs-lookup"><span data-stu-id="a7581-173"><span id="RebootMessage"></span><span id="rebootmessage"></span><span id="REBOOTMESSAGE"></span>RebootMessage</span></span>
</dt> <dd>

<span data-ttu-id="a7581-174">Il messaggio viene inviato agli utenti prima di riavviare il computer in risposta a un'azione di **\_ \_ riavvio dell'azione SC** specificata nella colonna azioni.</span><span class="sxs-lookup"><span data-stu-id="a7581-174">The message sent to users before restarting the computer in response to a **SC\_ACTION\_REBOOT** action specified in the Actions column.</span></span> <span data-ttu-id="a7581-175">È possibile utilizzare una stringa vuota "" per inviare il messaggio corrente invariato.</span><span class="sxs-lookup"><span data-stu-id="a7581-175">You can use an empty string, "", to send the current message unchanged.</span></span> <span data-ttu-id="a7581-176">È possibile utilizzare \[ ~ \] la sintassi del tipo di dati [formattato](formatted.md) per eliminare il messaggio corrente e non inviare alcun messaggio.</span><span class="sxs-lookup"><span data-stu-id="a7581-176">You can use \[~\] syntax of the [Formatted](formatted.md) data type to delete the current message and send no message.</span></span>

</dd> <dt>

<span data-ttu-id="a7581-177"><span id="Command"></span><span id="command"></span><span id="COMMAND"></span>Comando</span><span class="sxs-lookup"><span data-stu-id="a7581-177"><span id="Command"></span><span id="command"></span><span id="COMMAND"></span>Command</span></span>
</dt> <dd>

<span data-ttu-id="a7581-178">La riga di comando eseguita dal processo creato dalla funzione [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) in risposta a un'azione **del \_ \_ \_ comando di esecuzione di un'azione SC** specificata nella colonna azioni.</span><span class="sxs-lookup"><span data-stu-id="a7581-178">The command line run by the process created by the [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) function in response to a **SC\_ACTION\_RUN\_COMMAND** action specified in the Actions column.</span></span> <span data-ttu-id="a7581-179">Il nuovo processo viene eseguito con lo stesso account del servizio e solo se il campo dell'azione è **SC \_ Action \_ Run \_ Command**.</span><span class="sxs-lookup"><span data-stu-id="a7581-179">The new process runs under the same account as the service and only if the Action field is **SC\_ACTION\_RUN\_COMMAND**.</span></span> <span data-ttu-id="a7581-180">È possibile usare una stringa vuota, "", per usare la riga di comando corrente senza modifiche.</span><span class="sxs-lookup"><span data-stu-id="a7581-180">You can use an empty string, "", to use the current command line unchanged.</span></span> <span data-ttu-id="a7581-181">È possibile utilizzare la \[ ~ \] sintassi del tipo di dati [formattato](formatted.md) per eliminare la riga di comando corrente ed eseguire nessuna operazione quando il servizio ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="a7581-181">You can use \[~\] syntax of the [Formatted](formatted.md) data type to delete the current command line and run no operation when the service fails.</span></span>

</dd> <dt>

<span data-ttu-id="a7581-182"><span id="Actions"></span><span id="actions"></span><span id="ACTIONS"></span>Azioni</span><span class="sxs-lookup"><span data-stu-id="a7581-182"><span id="Actions"></span><span id="actions"></span><span id="ACTIONS"></span>Actions</span></span>
</dt> <dd>

<span data-ttu-id="a7581-183">Questo campo contiene una matrice di valori integer che specificano le azioni eseguite da SCM se il servizio ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="a7581-183">This field contains an array of integer values that specify the actions taken by the SCM if the service fails.</span></span> <span data-ttu-id="a7581-184">Separare i valori nella matrice in base a \[ ~ \] .</span><span class="sxs-lookup"><span data-stu-id="a7581-184">Separate the values in the array by \[~\].</span></span> <span data-ttu-id="a7581-185">Il valore integer nell'ennesimo elemento della matrice specifica l'azione eseguita quando il servizio ha esito negativo per l'ennesimo tempo.</span><span class="sxs-lookup"><span data-stu-id="a7581-185">The integer value in the Nth element of the array specifies the action performed when the service fails for the Nth time.</span></span> <span data-ttu-id="a7581-186">Ogni membro della matrice è uno dei valori interi seguenti.</span><span class="sxs-lookup"><span data-stu-id="a7581-186">Each member of the array is one of following integer values.</span></span>



| <span data-ttu-id="a7581-187">Costante</span><span class="sxs-lookup"><span data-stu-id="a7581-187">Constant</span></span>                                 | <span data-ttu-id="a7581-188">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a7581-188">Description</span></span>           |
|------------------------------------------|-----------------------|
| <span data-ttu-id="a7581-189">**SC \_ \_Nessuna azione** 0</span><span class="sxs-lookup"><span data-stu-id="a7581-189">**SC\_ACTION\_NONE** 0</span></span><br/>         | <span data-ttu-id="a7581-190">Nessuna azione.</span><span class="sxs-lookup"><span data-stu-id="a7581-190">No action.</span></span>            |
| <span data-ttu-id="a7581-191">**SC \_ AZIONE \_ riavvio** 2</span><span class="sxs-lookup"><span data-stu-id="a7581-191">**SC\_ACTION\_REBOOT** 2</span></span><br/>       | <span data-ttu-id="a7581-192">Riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="a7581-192">Restart the computer.</span></span> |
| <span data-ttu-id="a7581-193">**SC \_ \_Riavvio azione** 1</span><span class="sxs-lookup"><span data-stu-id="a7581-193">**SC\_ACTION\_RESTART** 1</span></span><br/>      | <span data-ttu-id="a7581-194">Riavviare il servizio.</span><span class="sxs-lookup"><span data-stu-id="a7581-194">Restart the service.</span></span>  |
| <span data-ttu-id="a7581-195">**SC \_ \_ \_ Comando Esegui azione** 3</span><span class="sxs-lookup"><span data-stu-id="a7581-195">**SC\_ACTION\_RUN\_COMMAND** 3</span></span><br/> | <span data-ttu-id="a7581-196">Eseguire un comando.</span><span class="sxs-lookup"><span data-stu-id="a7581-196">Run a command.</span></span>        |



 

</dd> <dt>

<span data-ttu-id="a7581-197"><span id="DelayActions"></span><span id="delayactions"></span><span id="DELAYACTIONS"></span>DelayActions</span><span class="sxs-lookup"><span data-stu-id="a7581-197"><span id="DelayActions"></span><span id="delayactions"></span><span id="DELAYACTIONS"></span>DelayActions</span></span>
</dt> <dd>

<span data-ttu-id="a7581-198">Questo campo contiene una matrice di valori integer che specifica il tempo in millisecondi di attesa prima di eseguire l'azione specificata nella colonna azione.</span><span class="sxs-lookup"><span data-stu-id="a7581-198">This field contains an array of integer values that specify the time in milliseconds to wait before performing the action specified in the Action column.</span></span> <span data-ttu-id="a7581-199">Separare i valori nella matrice in base a \[ ~ \] .</span><span class="sxs-lookup"><span data-stu-id="a7581-199">Separate the values in the array by \[~\].</span></span> <span data-ttu-id="a7581-200">Il numero di elementi nella matrice DelayActions deve essere uguale al numero di elementi nella matrice actions.</span><span class="sxs-lookup"><span data-stu-id="a7581-200">The number of elements in the DelayActions array must be equal to the number of elements in the Actions array.</span></span> <span data-ttu-id="a7581-201">L'ennesimo elemento della matrice DelayActions specifica il ritardo di tempo per l'ennesimo elemento della matrice di azioni.</span><span class="sxs-lookup"><span data-stu-id="a7581-201">The Nth element of the DelayActions array specifies the time delay for the nth element of the Actions array.</span></span>

</dd> <dt>

<span data-ttu-id="a7581-202"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_</span><span class="sxs-lookup"><span data-stu-id="a7581-202"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="a7581-203">Chiave esterna per la colonna uno della [tabella dei componenti](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="a7581-203">External key to column one of the [Component Table](component-table.md).</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="a7581-204">Convalida</span><span class="sxs-lookup"><span data-stu-id="a7581-204">Validation</span></span>

<dl>

[<span data-ttu-id="a7581-205">ICE102</span><span class="sxs-lookup"><span data-stu-id="a7581-205">ICE102</span></span>](ice-102.md)  
[<span data-ttu-id="a7581-206">ICE03</span><span class="sxs-lookup"><span data-stu-id="a7581-206">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="a7581-207">ICE06</span><span class="sxs-lookup"><span data-stu-id="a7581-207">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="a7581-208">ICE32</span><span class="sxs-lookup"><span data-stu-id="a7581-208">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="a7581-209">ICE45</span><span class="sxs-lookup"><span data-stu-id="a7581-209">ICE45</span></span>](ice45.md)  
[<span data-ttu-id="a7581-210">ICE46</span><span class="sxs-lookup"><span data-stu-id="a7581-210">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="a7581-211">ICE69</span><span class="sxs-lookup"><span data-stu-id="a7581-211">ICE69</span></span>](ice69.md)  
</dl>

 

 
