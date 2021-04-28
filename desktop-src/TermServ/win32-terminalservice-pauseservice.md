---
title: Metodo PauseService della classe Win32_Service (Servizi Desktop remoto)
description: 'Metodo PauseService della classe Win32_Service (Servizi Desktop remoto): tenta di posizionare il servizio nello stato sospeso.'
ms.assetid: 101987F6-FBAB-4E79-B1FA-346B1EF58DE1
ms.tgt_platform: multiple
keywords:
- Metodo PauseService Servizi Desktop remoto
- Metodo PauseService Servizi Desktop remoto , Win32_Service classe
- Win32_Service classe Servizi Desktop remoto , metodo PauseService
topic_type:
- apiref
api_name:
- Win32_Service.PauseService
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d7c9847f363d9bc6d1743da6189d2c4290c00dd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090599"
---
# <a name="pauseservice-method-of-the-win32_service-class-remote-desktop-services"></a><span data-ttu-id="e0ca9-106">Metodo PauseService della classe Win32_Service (Servizi Desktop remoto)</span><span class="sxs-lookup"><span data-stu-id="e0ca9-106">PauseService method of the Win32_Service class (Remote Desktop Services)</span></span>

<span data-ttu-id="e0ca9-107">Il metodo della classe [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **PauseService** tenta di posizionare il servizio nello stato sospeso.</span><span class="sxs-lookup"><span data-stu-id="e0ca9-107">The **PauseService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to place the service in the paused state.</span></span>

<span data-ttu-id="e0ca9-108">Questo argomento usa Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="e0ca9-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="e0ca9-109">Per altre informazioni sull'uso di questo metodo, vedere [Chiamata di un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="e0ca9-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="e0ca9-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e0ca9-110">Syntax</span></span>


```mof
uint32 PauseService();
```



## <a name="parameters"></a><span data-ttu-id="e0ca9-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="e0ca9-111">Parameters</span></span>

<span data-ttu-id="e0ca9-112">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="e0ca9-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e0ca9-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e0ca9-113">Return value</span></span>

<span data-ttu-id="e0ca9-114">Restituisce uno dei valori elencati nell'elenco seguente o qualsiasi altro valore per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="e0ca9-114">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="e0ca9-115">Per altri codici di errore, vedere [**Costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="e0ca9-115">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="e0ca9-116">Per i valori **HRESULT** generali, vedere [Codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="e0ca9-116">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="e0ca9-117">**0**</span><span class="sxs-lookup"><span data-stu-id="e0ca9-117">**0**</span></span>
</dt> <dd>

<span data-ttu-id="e0ca9-118">La richiesta è stata accettata.</span><span class="sxs-lookup"><span data-stu-id="e0ca9-118">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="e0ca9-119">**1**</span><span class="sxs-lookup"><span data-stu-id="e0ca9-119">**1**</span></span>
</dt> <dd>

<span data-ttu-id="e0ca9-120">La richiesta non è supportata.</span><span class="sxs-lookup"><span data-stu-id="e0ca9-120">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="e0ca9-121">**2**</span><span class="sxs-lookup"><span data-stu-id="e0ca9-121">**2**</span></span>
</dt> <dd>

<span data-ttu-id="e0ca9-122">L'utente non dispone dell'accesso necessario.</span><span class="sxs-lookup"><span data-stu-id="e0ca9-122">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="e0ca9-123">**3**</span><span class="sxs-lookup"><span data-stu-id="e0ca9-123">**3**</span></span>
</dt> <dd>

<span data-ttu-id="e0ca9-124">Impossibile arrestare il servizio perché altri servizi in esecuzione dipendono dal servizio.</span><span class="sxs-lookup"><span data-stu-id="e0ca9-124">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="e0ca9-125">**4**</span><span class="sxs-lookup"><span data-stu-id="e0ca9-125">**4**</span></span>
</dt> <dd>

<span data-ttu-id="e0ca9-126">Il codice di controllo richiesto non è valido o non è accettabile per il servizio.</span><span class="sxs-lookup"><span data-stu-id="e0ca9-126">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="e0ca9-127">**5**</span><span class="sxs-lookup"><span data-stu-id="e0ca9-127">**5**</span></span>
</dt> <dd>

<span data-ttu-id="e0ca9-128">Impossibile inviare il codice di controllo richiesto al servizio perché lo stato del servizio ([**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** ) è uguale a 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="e0ca9-128">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="e0ca9-129">**6**</span><span class="sxs-lookup"><span data-stu-id="e0ca9-129">**6**</span></span>
</dt> <dd>

<span data-ttu-id="e0ca9-130">Il servizio non è stato avviato.</span><span class="sxs-lookup"><span data-stu-id="e0ca9-130">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="e0ca9-131">**7**</span><span class="sxs-lookup"><span data-stu-id="e0ca9-131">**7**</span></span>
</dt> <dd>

<span data-ttu-id="e0ca9-132">Il servizio non ha risposto in tempo utile alla richiesta di avvio.</span><span class="sxs-lookup"><span data-stu-id="e0ca9-132">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="e0ca9-133">**8**</span><span class="sxs-lookup"><span data-stu-id="e0ca9-133">**8**</span></span>
</dt> <dd>

<span data-ttu-id="e0ca9-134">Errore sconosciuto durante l'avvio del servizio.</span><span class="sxs-lookup"><span data-stu-id="e0ca9-134">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="e0ca9-135">**9**</span><span class="sxs-lookup"><span data-stu-id="e0ca9-135">**9**</span></span>
</dt> <dd>

<span data-ttu-id="e0ca9-136">Impossibile trovare il percorso della directory del file eseguibile del servizio.</span><span class="sxs-lookup"><span data-stu-id="e0ca9-136">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="e0ca9-137">**10**</span><span class="sxs-lookup"><span data-stu-id="e0ca9-137">**10**</span></span>
</dt> <dd>

<span data-ttu-id="e0ca9-138">Il servizio è già in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="e0ca9-138">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="e0ca9-139">**11**</span><span class="sxs-lookup"><span data-stu-id="e0ca9-139">**11**</span></span>
</dt> <dd>

<span data-ttu-id="e0ca9-140">Il database a cui aggiungere il nuovo servizio è bloccato.</span><span class="sxs-lookup"><span data-stu-id="e0ca9-140">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="e0ca9-141">**12**</span><span class="sxs-lookup"><span data-stu-id="e0ca9-141">**12**</span></span>
</dt> <dd>

<span data-ttu-id="e0ca9-142">Una dipendenza su cui si basa questo servizio è stata rimossa dal sistema.</span><span class="sxs-lookup"><span data-stu-id="e0ca9-142">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="e0ca9-143">**13**</span><span class="sxs-lookup"><span data-stu-id="e0ca9-143">**13**</span></span>
</dt> <dd>

<span data-ttu-id="e0ca9-144">Impossibile trovare un servizio dipendente necessario.</span><span class="sxs-lookup"><span data-stu-id="e0ca9-144">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="e0ca9-145">**14**</span><span class="sxs-lookup"><span data-stu-id="e0ca9-145">**14**</span></span>
</dt> <dd>

<span data-ttu-id="e0ca9-146">Il servizio è stato disabilitato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="e0ca9-146">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="e0ca9-147">**15**</span><span class="sxs-lookup"><span data-stu-id="e0ca9-147">**15**</span></span>
</dt> <dd>

<span data-ttu-id="e0ca9-148">Il servizio non dispone delle credenziali di autenticazione corrette per l'esecuzione nel sistema.</span><span class="sxs-lookup"><span data-stu-id="e0ca9-148">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="e0ca9-149">**16**</span><span class="sxs-lookup"><span data-stu-id="e0ca9-149">**16**</span></span>
</dt> <dd>

<span data-ttu-id="e0ca9-150">Questo servizio viene rimosso dal sistema.</span><span class="sxs-lookup"><span data-stu-id="e0ca9-150">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="e0ca9-151">**17**</span><span class="sxs-lookup"><span data-stu-id="e0ca9-151">**17**</span></span>
</dt> <dd>

<span data-ttu-id="e0ca9-152">Il servizio non ha thread di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="e0ca9-152">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="e0ca9-153">**18**</span><span class="sxs-lookup"><span data-stu-id="e0ca9-153">**18**</span></span>
</dt> <dd>

<span data-ttu-id="e0ca9-154">Il servizio presenta dipendenze circolari all'avvio.</span><span class="sxs-lookup"><span data-stu-id="e0ca9-154">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="e0ca9-155">**19**</span><span class="sxs-lookup"><span data-stu-id="e0ca9-155">**19**</span></span>
</dt> <dd>

<span data-ttu-id="e0ca9-156">Un servizio viene eseguito con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="e0ca9-156">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="e0ca9-157">**20**</span><span class="sxs-lookup"><span data-stu-id="e0ca9-157">**20**</span></span>
</dt> <dd>

<span data-ttu-id="e0ca9-158">Il nome del servizio contiene caratteri non validi.</span><span class="sxs-lookup"><span data-stu-id="e0ca9-158">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="e0ca9-159">**21**</span><span class="sxs-lookup"><span data-stu-id="e0ca9-159">**21**</span></span>
</dt> <dd>

<span data-ttu-id="e0ca9-160">Al servizio sono stati passati parametri non validi.</span><span class="sxs-lookup"><span data-stu-id="e0ca9-160">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="e0ca9-161">**22**</span><span class="sxs-lookup"><span data-stu-id="e0ca9-161">**22**</span></span>
</dt> <dd>

<span data-ttu-id="e0ca9-162">L'account con cui viene eseguito il servizio non è valido o non dispone delle autorizzazioni per eseguire il servizio.</span><span class="sxs-lookup"><span data-stu-id="e0ca9-162">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="e0ca9-163">**23**</span><span class="sxs-lookup"><span data-stu-id="e0ca9-163">**23**</span></span>
</dt> <dd>

<span data-ttu-id="e0ca9-164">Il servizio esiste già nel database dei servizi disponibili dal sistema.</span><span class="sxs-lookup"><span data-stu-id="e0ca9-164">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="e0ca9-165">**24**</span><span class="sxs-lookup"><span data-stu-id="e0ca9-165">**24**</span></span>
</dt> <dd>

<span data-ttu-id="e0ca9-166">Il servizio è attualmente sospeso nel sistema.</span><span class="sxs-lookup"><span data-stu-id="e0ca9-166">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e0ca9-167">Commenti</span><span class="sxs-lookup"><span data-stu-id="e0ca9-167">Remarks</span></span>

<span data-ttu-id="e0ca9-168">Dopo aver determinato quali servizi possono essere arrestati o sospesi, è possibile usare i [**metodi StopService**](win32-terminalservice-stopservice.md) e **PauseService** per arrestare e sospendere i servizi.</span><span class="sxs-lookup"><span data-stu-id="e0ca9-168">After you have determined which services can be stopped or paused, you can use the [**StopService**](win32-terminalservice-stopservice.md) and **PauseService** methods to stop and pause services.</span></span> <span data-ttu-id="e0ca9-169">La decisione di arrestare un servizio anziché sospenderlo o viceversa dipende da diversi fattori, tra cui:</span><span class="sxs-lookup"><span data-stu-id="e0ca9-169">The decision to stop a service rather than pause it, or vice versa, depends on several factors, including the following:</span></span>

-   <span data-ttu-id="e0ca9-170">Il servizio è in grado di essere sospeso?</span><span class="sxs-lookup"><span data-stu-id="e0ca9-170">Is the service capable of being paused?</span></span> <span data-ttu-id="e0ca9-171">In caso contrario, l'unica opzione è arrestare il servizio.</span><span class="sxs-lookup"><span data-stu-id="e0ca9-171">If not, your only option is the stop the service.</span></span>
-   <span data-ttu-id="e0ca9-172">È necessario continuare a gestire le richieste client per chiunque sia già connesso al servizio?</span><span class="sxs-lookup"><span data-stu-id="e0ca9-172">Do you need to continue handling client requests for anyone already connected to the service?</span></span> <span data-ttu-id="e0ca9-173">In tal caso, la sospensione di un servizio consente in genere di gestire i client esistenti negando l'accesso ai nuovi client.</span><span class="sxs-lookup"><span data-stu-id="e0ca9-173">If so, pausing a service typically allows it to handle existing clients while denying access to new clients.</span></span> <span data-ttu-id="e0ca9-174">Al contrario, quando si arresta un servizio, tutti i client vengono disconnessi immediatamente.</span><span class="sxs-lookup"><span data-stu-id="e0ca9-174">By contrast, when you stop a service, all clients are immediately disconnected.</span></span>
-   <span data-ttu-id="e0ca9-175">È necessario riconfigurare un servizio e impostare immediatamente l'applicazione delle modifiche?</span><span class="sxs-lookup"><span data-stu-id="e0ca9-175">Do you need to reconfigure a service and have the changes take effect immediately?</span></span> <span data-ttu-id="e0ca9-176">Sebbene le proprietà del servizio possano essere modificate durante la sospensione di un servizio, la maggior parte di esse non ha effetto fino a quando il servizio non viene effettivamente arrestato e riavviato.</span><span class="sxs-lookup"><span data-stu-id="e0ca9-176">Although service properties can be changed while a service is paused, most of them do not take effect until the service is actually stopped and restarted.</span></span>

<span data-ttu-id="e0ca9-177">Il codice di scripting necessario per arrestare un servizio è quasi identico al codice necessario per sospendere il servizio.</span><span class="sxs-lookup"><span data-stu-id="e0ca9-177">The scripting code required to stop a service is almost identical to the code required to pause the service.</span></span>

## <a name="examples"></a><span data-ttu-id="e0ca9-178">Esempio</span><span class="sxs-lookup"><span data-stu-id="e0ca9-178">Examples</span></span>

<span data-ttu-id="e0ca9-179">[L'esempio VBScript Pause Services Running Under a Specific Account](https://Gallery.TechNet.Microsoft.Com/12a256dd-39da-4690-b3f0-f0adccaf25f1) Sospende tutti i servizi in esecuzione con l'ipotetico account del servizio Netsvc.</span><span class="sxs-lookup"><span data-stu-id="e0ca9-179">The [Pause Services Running Under a Specific Account](https://Gallery.TechNet.Microsoft.Com/12a256dd-39da-4690-b3f0-f0adccaf25f1) VBScript sample Pauses all services running under the hypothetical service account Netsvc.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0ca9-180">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e0ca9-180">Requirements</span></span>



| <span data-ttu-id="e0ca9-181">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0ca9-181">Requirement</span></span> | <span data-ttu-id="e0ca9-182">Valore</span><span class="sxs-lookup"><span data-stu-id="e0ca9-182">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e0ca9-183">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e0ca9-183">Minimum supported client</span></span><br/> | <span data-ttu-id="e0ca9-184">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e0ca9-184">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e0ca9-185">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e0ca9-185">Minimum supported server</span></span><br/> | <span data-ttu-id="e0ca9-186">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e0ca9-186">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e0ca9-187">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e0ca9-187">Namespace</span></span><br/>                | <span data-ttu-id="e0ca9-188">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="e0ca9-188">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="e0ca9-189">MOF</span><span class="sxs-lookup"><span data-stu-id="e0ca9-189">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e0ca9-190"><dt>TSCfgWmi.mof</dt></span><span class="sxs-lookup"><span data-stu-id="e0ca9-190"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="e0ca9-191">DLL</span><span class="sxs-lookup"><span data-stu-id="e0ca9-191">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e0ca9-192"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0ca9-192"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0ca9-193">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e0ca9-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0ca9-194">**Servizio \_ Win32**</span><span class="sxs-lookup"><span data-stu-id="e0ca9-194">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="e0ca9-195">Classi del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="e0ca9-195">Operating System Classes</span></span>](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[<span data-ttu-id="e0ca9-196">**Win32 \_ TerminalService**</span><span class="sxs-lookup"><span data-stu-id="e0ca9-196">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="e0ca9-197">Attività WMI: Servizi</span><span class="sxs-lookup"><span data-stu-id="e0ca9-197">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> <dt>

[<span data-ttu-id="e0ca9-198">**StopService**</span><span class="sxs-lookup"><span data-stu-id="e0ca9-198">**StopService**</span></span>](/windows/desktop/CIMWin32Prov/stopservice-method-in-class-win32-service)
</dt> </dl>

 

