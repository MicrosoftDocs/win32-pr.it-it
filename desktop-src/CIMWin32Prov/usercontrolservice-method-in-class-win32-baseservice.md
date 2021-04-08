---
description: Tenta di inviare un codice di controllo definito dall'utente a un servizio.
ms.assetid: d181dbf8-e1ad-47b2-9e64-4aabc77e64bd
ms.tgt_platform: multiple
title: Metodo UserControlService della classe Win32_BaseService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BaseService.UserControlService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 55647524c8ba561716441976fe6654b933e1900b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878242"
---
# <a name="usercontrolservice-method-of-the-win32_baseservice-class"></a><span data-ttu-id="fa04a-103">Metodo UserControlService della \_ classe BaseService Win32</span><span class="sxs-lookup"><span data-stu-id="fa04a-103">UserControlService method of the Win32\_BaseService class</span></span>

<span data-ttu-id="fa04a-104">Il metodo della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) tenta di inviare un codice di controllo definito dall'utente a un servizio.</span><span class="sxs-lookup"><span data-stu-id="fa04a-104">The [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to send a user-defined control code to a service.</span></span>

<span data-ttu-id="fa04a-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="fa04a-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="fa04a-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="fa04a-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="fa04a-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fa04a-107">Syntax</span></span>


```mof
uint32 UserControlService(
  [in] uint8 ControlCode
);
```



## <a name="parameters"></a><span data-ttu-id="fa04a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="fa04a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa04a-109">*ControlCode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fa04a-109">*ControlCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa04a-110">Valore che specifica un comando di controllo per un servizio.</span><span class="sxs-lookup"><span data-stu-id="fa04a-110">Value that specifies a control command to a service.</span></span> <span data-ttu-id="fa04a-111">Ad esempio, un comando di controllo è un comando "pausa" o "continua".</span><span class="sxs-lookup"><span data-stu-id="fa04a-111">For example a control command is a "pause" or "continue" command.</span></span> <span data-ttu-id="fa04a-112">Il valore può essere un codice predefinito oppure un valore e un'azione definiti dal servizio.</span><span class="sxs-lookup"><span data-stu-id="fa04a-112">The value can be a predefined code, or a value and action that the service defines.</span></span> <span data-ttu-id="fa04a-113">Di seguito sono riportati i codici di controllo predefiniti:</span><span class="sxs-lookup"><span data-stu-id="fa04a-113">The following are the predefined control codes:</span></span>

<dt>

<span id="SERVICE_CONTROL_CONTINUE"></span><span id="service_control_continue"></span>

<span data-ttu-id="fa04a-114"><span id="SERVICE_CONTROL_CONTINUE"></span><span id="service_control_continue"></span>**controllo del servizio \_ \_ continua**</span><span class="sxs-lookup"><span data-stu-id="fa04a-114"><span id="SERVICE_CONTROL_CONTINUE"></span><span id="service_control_continue"></span>**SERVICE\_CONTROL\_CONTINUE**</span></span>


</dt> <dd>

<span data-ttu-id="fa04a-115">Notifica a un servizio sospeso di essere ripreso.</span><span class="sxs-lookup"><span data-stu-id="fa04a-115">Notifies a paused service to resume.</span></span>

</dd> <dt>

<span id="SERVICE_CONTROL_INTERROGATE"></span><span id="service_control_interrogate"></span>

<span data-ttu-id="fa04a-116"><span id="SERVICE_CONTROL_INTERROGATE"></span><span id="service_control_interrogate"></span>**\_ \_ interrogazione controllo servizio**</span><span class="sxs-lookup"><span data-stu-id="fa04a-116"><span id="SERVICE_CONTROL_INTERROGATE"></span><span id="service_control_interrogate"></span>**SERVICE\_CONTROL\_INTERROGATE**</span></span>


</dt> <dd>

<span data-ttu-id="fa04a-117">Notifica a un servizio di segnalare le informazioni sullo stato corrente a gestione controllo servizi.</span><span class="sxs-lookup"><span data-stu-id="fa04a-117">Notifies a service to report the current status information to the service control manager.</span></span>

</dd> <dt>

<span id="SERVICE_CONTROL_NETBINDADD"></span><span id="service_control_netbindadd"></span>

<span data-ttu-id="fa04a-118"><span id="SERVICE_CONTROL_NETBINDADD"></span><span id="service_control_netbindadd"></span>**controllo del servizio \_ \_ NETBINDADD**</span><span class="sxs-lookup"><span data-stu-id="fa04a-118"><span id="SERVICE_CONTROL_NETBINDADD"></span><span id="service_control_netbindadd"></span>**SERVICE\_CONTROL\_NETBINDADD**</span></span>


</dt> <dd>

<span data-ttu-id="fa04a-119">Notifica a un servizio di rete la presenza di un nuovo componente per l'associazione.</span><span class="sxs-lookup"><span data-stu-id="fa04a-119">Notifies a network service that there is a new component for binding.</span></span>

</dd> <dt>

<span id="SERVICE_CONTROL_NETBINDDISABLE"></span><span id="service_control_netbinddisable"></span>

<span data-ttu-id="fa04a-120"><span id="SERVICE_CONTROL_NETBINDDISABLE"></span><span id="service_control_netbinddisable"></span>**controllo del servizio \_ \_ NETBINDDISABLE**</span><span class="sxs-lookup"><span data-stu-id="fa04a-120"><span id="SERVICE_CONTROL_NETBINDDISABLE"></span><span id="service_control_netbinddisable"></span>**SERVICE\_CONTROL\_NETBINDDISABLE**</span></span>


</dt> <dd>

<span data-ttu-id="fa04a-121">Notifica a un servizio di rete che una delle associazioni è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="fa04a-121">Notifies a network service that one of its bindings is disabled.</span></span>

</dd> <dt>

<span id="SERVICE_CONTROL_NETBINDENABLE"></span><span id="service_control_netbindenable"></span>

<span data-ttu-id="fa04a-122"><span id="SERVICE_CONTROL_NETBINDENABLE"></span><span id="service_control_netbindenable"></span>**controllo del servizio \_ \_ NETBINDENABLE**</span><span class="sxs-lookup"><span data-stu-id="fa04a-122"><span id="SERVICE_CONTROL_NETBINDENABLE"></span><span id="service_control_netbindenable"></span>**SERVICE\_CONTROL\_NETBINDENABLE**</span></span>


</dt> <dd>

<span data-ttu-id="fa04a-123">Notifica a un servizio di rete che è abilitata un'associazione disabilitata.</span><span class="sxs-lookup"><span data-stu-id="fa04a-123">Notifies a network service that a disabled binding is enabled.</span></span>

</dd> <dt>

<span id="SERVICE_CONTROL_NETBINDREMOVE"></span><span id="service_control_netbindremove"></span>

<span data-ttu-id="fa04a-124"><span id="SERVICE_CONTROL_NETBINDREMOVE"></span><span id="service_control_netbindremove"></span>**controllo del servizio \_ \_ NETBINDREMOVE**</span><span class="sxs-lookup"><span data-stu-id="fa04a-124"><span id="SERVICE_CONTROL_NETBINDREMOVE"></span><span id="service_control_netbindremove"></span>**SERVICE\_CONTROL\_NETBINDREMOVE**</span></span>


</dt> <dd>

<span data-ttu-id="fa04a-125">Notifica a un servizio di rete che un componente per l'associazione è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="fa04a-125">Notifies a network service that a component for binding has been removed.</span></span>

</dd> <dt>

<span id="SERVICE_CONTROL_PARAMCHANGE"></span><span id="service_control_paramchange"></span>

<span data-ttu-id="fa04a-126"><span id="SERVICE_CONTROL_PARAMCHANGE"></span><span id="service_control_paramchange"></span>**controllo del servizio \_ \_ PARAMCHANGE**</span><span class="sxs-lookup"><span data-stu-id="fa04a-126"><span id="SERVICE_CONTROL_PARAMCHANGE"></span><span id="service_control_paramchange"></span>**SERVICE\_CONTROL\_PARAMCHANGE**</span></span>


</dt> <dd>

<span data-ttu-id="fa04a-127">Notifica a un servizio che i parametri di avvio vengono modificati.</span><span class="sxs-lookup"><span data-stu-id="fa04a-127">Notifies a service that its startup parameters are changed.</span></span>

</dd> <dt>

<span id="SERVICE_CONTROL_PAUSE"></span><span id="service_control_pause"></span>

<span data-ttu-id="fa04a-128"><span id="SERVICE_CONTROL_PAUSE"></span><span id="service_control_pause"></span>**\_sospensione del controllo del servizio \_**</span><span class="sxs-lookup"><span data-stu-id="fa04a-128"><span id="SERVICE_CONTROL_PAUSE"></span><span id="service_control_pause"></span>**SERVICE\_CONTROL\_PAUSE**</span></span>


</dt> <dd>

<span data-ttu-id="fa04a-129">Notifica a un servizio di sospendere.</span><span class="sxs-lookup"><span data-stu-id="fa04a-129">Notifies a service to pause.</span></span>

</dd> <dt>

<span id="SERVICE_CONTROL_STOP"></span><span id="service_control_stop"></span>

<span data-ttu-id="fa04a-130"><span id="SERVICE_CONTROL_STOP"></span><span id="service_control_stop"></span>**\_arresto del controllo del servizio \_**</span><span class="sxs-lookup"><span data-stu-id="fa04a-130"><span id="SERVICE_CONTROL_STOP"></span><span id="service_control_stop"></span>**SERVICE\_CONTROL\_STOP**</span></span>


</dt> <dd>

<span data-ttu-id="fa04a-131">Notifica a un servizio di arrestare.</span><span class="sxs-lookup"><span data-stu-id="fa04a-131">Notifies a service to stop.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa04a-132">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fa04a-132">Return value</span></span>

<span data-ttu-id="fa04a-133">Restituisce uno dei valori elencati nell'elenco seguente o un valore diverso per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="fa04a-133">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="fa04a-134">**Success**</span><span class="sxs-lookup"><span data-stu-id="fa04a-134">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="fa04a-135">0</span><span class="sxs-lookup"><span data-stu-id="fa04a-135">0</span></span>

<span data-ttu-id="fa04a-136">La richiesta è stata accettata.</span><span class="sxs-lookup"><span data-stu-id="fa04a-136">The request is accepted.</span></span>

</dd> <dt>

<span data-ttu-id="fa04a-137">**Non supportato**</span><span class="sxs-lookup"><span data-stu-id="fa04a-137">**Not Supported**</span></span>
</dt> <dd>

<span data-ttu-id="fa04a-138">1</span><span class="sxs-lookup"><span data-stu-id="fa04a-138">1</span></span>

<span data-ttu-id="fa04a-139">La richiesta non è supportata.</span><span class="sxs-lookup"><span data-stu-id="fa04a-139">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="fa04a-140">**Accesso negato**</span><span class="sxs-lookup"><span data-stu-id="fa04a-140">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="fa04a-141">2</span><span class="sxs-lookup"><span data-stu-id="fa04a-141">2</span></span>

<span data-ttu-id="fa04a-142">L'utente non dispone dei diritti di accesso necessari.</span><span class="sxs-lookup"><span data-stu-id="fa04a-142">The user does not have the necessary access rights.</span></span>

</dd> <dt>

<span data-ttu-id="fa04a-143">**Servizi dipendenti in esecuzione**</span><span class="sxs-lookup"><span data-stu-id="fa04a-143">**Dependent Services Running**</span></span>
</dt> <dd>

<span data-ttu-id="fa04a-144">3</span><span class="sxs-lookup"><span data-stu-id="fa04a-144">3</span></span>

<span data-ttu-id="fa04a-145">Impossibile arrestare il servizio perché altri servizi in esecuzione dipendono dal servizio.</span><span class="sxs-lookup"><span data-stu-id="fa04a-145">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="fa04a-146">**Controllo del servizio non valido**</span><span class="sxs-lookup"><span data-stu-id="fa04a-146">**Invalid Service Control**</span></span>
</dt> <dd>

<span data-ttu-id="fa04a-147">4</span><span class="sxs-lookup"><span data-stu-id="fa04a-147">4</span></span>

<span data-ttu-id="fa04a-148">Il codice di controllo richiesto non è valido o non è accettabile per il servizio.</span><span class="sxs-lookup"><span data-stu-id="fa04a-148">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="fa04a-149">**Il servizio non può accettare il controllo**</span><span class="sxs-lookup"><span data-stu-id="fa04a-149">**Service Cannot Accept Control**</span></span>
</dt> <dd>

<span data-ttu-id="fa04a-150">5</span><span class="sxs-lookup"><span data-stu-id="fa04a-150">5</span></span>

<span data-ttu-id="fa04a-151">Impossibile inviare il codice di controllo richiesto al servizio perché lo stato del servizio ([**Win32 \_ BaseService**](win32-baseservice.md).**Proprietà state** ) è uguale a 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="fa04a-151">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="fa04a-152">**Servizio non attivo**</span><span class="sxs-lookup"><span data-stu-id="fa04a-152">**Service Not Active**</span></span>
</dt> <dd>

<span data-ttu-id="fa04a-153">6</span><span class="sxs-lookup"><span data-stu-id="fa04a-153">6</span></span>

<span data-ttu-id="fa04a-154">Servizio non avviato.</span><span class="sxs-lookup"><span data-stu-id="fa04a-154">The service has not started.</span></span>

</dd> <dt>

<span data-ttu-id="fa04a-155">**Timeout richiesta servizio**</span><span class="sxs-lookup"><span data-stu-id="fa04a-155">**Service Request Timeout**</span></span>
</dt> <dd>

<span data-ttu-id="fa04a-156">7</span><span class="sxs-lookup"><span data-stu-id="fa04a-156">7</span></span>

<span data-ttu-id="fa04a-157">Il servizio non risponde alla richiesta di avvio rapidamente.</span><span class="sxs-lookup"><span data-stu-id="fa04a-157">The service does not respond to the start request quickly.</span></span>

</dd> <dt>

<span data-ttu-id="fa04a-158">**Errore sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="fa04a-158">**Unknown Failure**</span></span>
</dt> <dd>

<span data-ttu-id="fa04a-159">8</span><span class="sxs-lookup"><span data-stu-id="fa04a-159">8</span></span>

<span data-ttu-id="fa04a-160">Processo interattivo.</span><span class="sxs-lookup"><span data-stu-id="fa04a-160">Interactive process.</span></span>

</dd> <dt>

<span data-ttu-id="fa04a-161">**Percorso non trovato**</span><span class="sxs-lookup"><span data-stu-id="fa04a-161">**Path Not Found**</span></span>
</dt> <dd>

<span data-ttu-id="fa04a-162">9</span><span class="sxs-lookup"><span data-stu-id="fa04a-162">9</span></span>

<span data-ttu-id="fa04a-163">Impossibile trovare il percorso di directory del file eseguibile del servizio.</span><span class="sxs-lookup"><span data-stu-id="fa04a-163">The directory path to the service executable file is not found.</span></span>

</dd> <dt>

<span data-ttu-id="fa04a-164">**Servizio già in esecuzione**</span><span class="sxs-lookup"><span data-stu-id="fa04a-164">**Service Already Running**</span></span>
</dt> <dd>

<span data-ttu-id="fa04a-165">10</span><span class="sxs-lookup"><span data-stu-id="fa04a-165">10</span></span>

<span data-ttu-id="fa04a-166">Il servizio è già in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="fa04a-166">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="fa04a-167">**Database del servizio bloccato**</span><span class="sxs-lookup"><span data-stu-id="fa04a-167">**Service Database Locked**</span></span>
</dt> <dd>

<span data-ttu-id="fa04a-168">11</span><span class="sxs-lookup"><span data-stu-id="fa04a-168">11</span></span>

<span data-ttu-id="fa04a-169">Il database a cui aggiungere il nuovo servizio è bloccato.</span><span class="sxs-lookup"><span data-stu-id="fa04a-169">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="fa04a-170">**Dipendenza servizio eliminata**</span><span class="sxs-lookup"><span data-stu-id="fa04a-170">**Service Dependency Deleted**</span></span>
</dt> <dd>

<span data-ttu-id="fa04a-171">12</span><span class="sxs-lookup"><span data-stu-id="fa04a-171">12</span></span>

<span data-ttu-id="fa04a-172">Una dipendenza su cui si basa questo servizio viene rimossa dal sistema.</span><span class="sxs-lookup"><span data-stu-id="fa04a-172">A dependency that this service relies on is removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="fa04a-173">**Errore di dipendenza del servizio**</span><span class="sxs-lookup"><span data-stu-id="fa04a-173">**Service Dependency Failure**</span></span>
</dt> <dd>

<span data-ttu-id="fa04a-174">13</span><span class="sxs-lookup"><span data-stu-id="fa04a-174">13</span></span>

<span data-ttu-id="fa04a-175">Il servizio non trova il servizio necessario da un servizio dipendente.</span><span class="sxs-lookup"><span data-stu-id="fa04a-175">The service does not find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="fa04a-176">**Servizio disabilitato**</span><span class="sxs-lookup"><span data-stu-id="fa04a-176">**Service Disabled**</span></span>
</dt> <dd>

<span data-ttu-id="fa04a-177">14</span><span class="sxs-lookup"><span data-stu-id="fa04a-177">14</span></span>

<span data-ttu-id="fa04a-178">Il servizio è disabilitato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="fa04a-178">The service is disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="fa04a-179">**Accesso al servizio non riuscito**</span><span class="sxs-lookup"><span data-stu-id="fa04a-179">**Service Logon Failed**</span></span>
</dt> <dd>

<span data-ttu-id="fa04a-180">15</span><span class="sxs-lookup"><span data-stu-id="fa04a-180">15</span></span>

<span data-ttu-id="fa04a-181">Il servizio non dispone delle credenziali di autenticazione corrette per l'esecuzione nel sistema.</span><span class="sxs-lookup"><span data-stu-id="fa04a-181">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="fa04a-182">**Servizio contrassegnato per l'eliminazione**</span><span class="sxs-lookup"><span data-stu-id="fa04a-182">**Service Marked For Deletion**</span></span>
</dt> <dd>

<span data-ttu-id="fa04a-183">16</span><span class="sxs-lookup"><span data-stu-id="fa04a-183">16</span></span>

<span data-ttu-id="fa04a-184">Il servizio verrà rimosso dal sistema.</span><span class="sxs-lookup"><span data-stu-id="fa04a-184">The service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="fa04a-185">**Servizio senza thread**</span><span class="sxs-lookup"><span data-stu-id="fa04a-185">**Service No Thread**</span></span>
</dt> <dd>

<span data-ttu-id="fa04a-186">17</span><span class="sxs-lookup"><span data-stu-id="fa04a-186">17</span></span>

<span data-ttu-id="fa04a-187">Nessun thread di esecuzione per il servizio.</span><span class="sxs-lookup"><span data-stu-id="fa04a-187">There is no execution thread for the service.</span></span>

</dd> <dt>

<span data-ttu-id="fa04a-188">**Stato dipendenza circolare**</span><span class="sxs-lookup"><span data-stu-id="fa04a-188">**Status Circular Dependency**</span></span>
</dt> <dd>

<span data-ttu-id="fa04a-189">18</span><span class="sxs-lookup"><span data-stu-id="fa04a-189">18</span></span>

<span data-ttu-id="fa04a-190">All'avvio del servizio sono state rilevate dipendenze circolari.</span><span class="sxs-lookup"><span data-stu-id="fa04a-190">There are circular dependencies when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="fa04a-191">**Stato nome duplicato**</span><span class="sxs-lookup"><span data-stu-id="fa04a-191">**Status Duplicate Name**</span></span>
</dt> <dd>

<span data-ttu-id="fa04a-192">19</span><span class="sxs-lookup"><span data-stu-id="fa04a-192">19</span></span>

<span data-ttu-id="fa04a-193">È presente un servizio in esecuzione con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="fa04a-193">There is a service running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="fa04a-194">**Stato nome non valido**</span><span class="sxs-lookup"><span data-stu-id="fa04a-194">**Status Invalid Name**</span></span>
</dt> <dd>

<span data-ttu-id="fa04a-195">20</span><span class="sxs-lookup"><span data-stu-id="fa04a-195">20</span></span>

<span data-ttu-id="fa04a-196">Il nome del servizio contiene caratteri non validi.</span><span class="sxs-lookup"><span data-stu-id="fa04a-196">There are invalid characters in the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="fa04a-197">**Stato parametro non valido**</span><span class="sxs-lookup"><span data-stu-id="fa04a-197">**Status Invalid Parameter**</span></span>
</dt> <dd>

<span data-ttu-id="fa04a-198">21</span><span class="sxs-lookup"><span data-stu-id="fa04a-198">21</span></span>

<span data-ttu-id="fa04a-199">Sono stati passati parametri non validi al servizio.</span><span class="sxs-lookup"><span data-stu-id="fa04a-199">Invalid parameters have passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="fa04a-200">**Stato account del servizio non valido**</span><span class="sxs-lookup"><span data-stu-id="fa04a-200">**Status Invalid Service Account**</span></span>
</dt> <dd>

<span data-ttu-id="fa04a-201">22</span><span class="sxs-lookup"><span data-stu-id="fa04a-201">22</span></span>

<span data-ttu-id="fa04a-202">L'account con cui viene eseguito il servizio non è valido o non dispone delle autorizzazioni per eseguire il servizio.</span><span class="sxs-lookup"><span data-stu-id="fa04a-202">The account that this service runs under is not valid or does not have the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="fa04a-203">**Il servizio stato esiste**</span><span class="sxs-lookup"><span data-stu-id="fa04a-203">**Status Service Exists**</span></span>
</dt> <dd>

<span data-ttu-id="fa04a-204">23</span><span class="sxs-lookup"><span data-stu-id="fa04a-204">23</span></span>

<span data-ttu-id="fa04a-205">Il servizio esiste già nel database dei servizi disponibili dal sistema.</span><span class="sxs-lookup"><span data-stu-id="fa04a-205">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="fa04a-206">**Servizio già sospeso**</span><span class="sxs-lookup"><span data-stu-id="fa04a-206">**Service Already Paused**</span></span>
</dt> <dd>

<span data-ttu-id="fa04a-207">24</span><span class="sxs-lookup"><span data-stu-id="fa04a-207">24</span></span>

<span data-ttu-id="fa04a-208">Il servizio è attualmente sospeso nel sistema.</span><span class="sxs-lookup"><span data-stu-id="fa04a-208">The service is currently paused in the system.</span></span>

</dd> <dt>

<span data-ttu-id="fa04a-209">**Altri**</span><span class="sxs-lookup"><span data-stu-id="fa04a-209">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="fa04a-210">25 4294967295</span><span class="sxs-lookup"><span data-stu-id="fa04a-210">25 4294967295</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fa04a-211">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fa04a-211">Requirements</span></span>



| <span data-ttu-id="fa04a-212">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa04a-212">Requirement</span></span> | <span data-ttu-id="fa04a-213">Valore</span><span class="sxs-lookup"><span data-stu-id="fa04a-213">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fa04a-214">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fa04a-214">Minimum supported client</span></span><br/> | <span data-ttu-id="fa04a-215">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fa04a-215">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fa04a-216">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fa04a-216">Minimum supported server</span></span><br/> | <span data-ttu-id="fa04a-217">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fa04a-217">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fa04a-218">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="fa04a-218">Namespace</span></span><br/>                | <span data-ttu-id="fa04a-219">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="fa04a-219">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="fa04a-220">MOF</span><span class="sxs-lookup"><span data-stu-id="fa04a-220">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fa04a-221"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fa04a-221"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="fa04a-222">DLL</span><span class="sxs-lookup"><span data-stu-id="fa04a-222">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa04a-223"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa04a-223"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa04a-224">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fa04a-224">See also</span></span>

<dl> <dt>

<span data-ttu-id="fa04a-225">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fa04a-225">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="fa04a-226">**\_BaseService Win32**</span><span class="sxs-lookup"><span data-stu-id="fa04a-226">**Win32\_BaseService**</span></span>](win32-baseservice.md)
</dt> </dl>

 

