---
title: Metodo StopService della classe Win32_Service (Sdoias. h) (servizio Terminal)
description: Inserisce il servizio, rappresentato dall' \_ oggetto TerminalService Win32, nello stato interrotto.
ms.assetid: 228711DC-369B-48B6-96EE-DF4026904E26
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo StopService
- Metodo StopService Servizi Desktop remoto, classe Win32_Service
- Classe Win32_Service Servizi Desktop remoto, metodo StopService
topic_type:
- apiref
api_name:
- Win32_Service.StopService
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e1b21db330bb9111b96fb244200845cb83b3153
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/26/2021
ms.locfileid: "106334052"
---
# <a name="stopservice-method-of-the-win32_service-class-sdoiash-for-the-terminal-service"></a><span data-ttu-id="27779-106">Metodo StopService della classe Win32_Service (Sdoias. h) per il servizio Terminal</span><span class="sxs-lookup"><span data-stu-id="27779-106">StopService method of the Win32_Service class (Sdoias.h) for the Terminal service</span></span>

<span data-ttu-id="27779-107">Il metodo della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **StopService** posiziona il servizio, rappresentato dall' [**oggetto \_ TerminalService Win32**](win32-terminalservice.md) , nello stato interrotto.</span><span class="sxs-lookup"><span data-stu-id="27779-107">The **StopService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method places the service, represented by the [**Win32\_TerminalService**](win32-terminalservice.md) object, in the stopped state.</span></span>

<span data-ttu-id="27779-108">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="27779-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="27779-109">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="27779-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="27779-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="27779-110">Syntax</span></span>


```mof
uint32 StopService();
```



## <a name="parameters"></a><span data-ttu-id="27779-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="27779-111">Parameters</span></span>

<span data-ttu-id="27779-112">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="27779-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="27779-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="27779-113">Return value</span></span>

<span data-ttu-id="27779-114">Restituisce uno dei valori elencati nell'elenco seguente o qualsiasi altro valore per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="27779-114">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="27779-115">Per ulteriori codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="27779-115">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="27779-116">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="27779-116">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="27779-117">**0**</span><span class="sxs-lookup"><span data-stu-id="27779-117">**0**</span></span>
</dt> <dd>

<span data-ttu-id="27779-118">La richiesta è stata accettata.</span><span class="sxs-lookup"><span data-stu-id="27779-118">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="27779-119">**1**</span><span class="sxs-lookup"><span data-stu-id="27779-119">**1**</span></span>
</dt> <dd>

<span data-ttu-id="27779-120">La richiesta non è supportata.</span><span class="sxs-lookup"><span data-stu-id="27779-120">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="27779-121">**2**</span><span class="sxs-lookup"><span data-stu-id="27779-121">**2**</span></span>
</dt> <dd>

<span data-ttu-id="27779-122">L'utente non dispone dell'accesso necessario.</span><span class="sxs-lookup"><span data-stu-id="27779-122">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="27779-123">**3**</span><span class="sxs-lookup"><span data-stu-id="27779-123">**3**</span></span>
</dt> <dd>

<span data-ttu-id="27779-124">Impossibile arrestare il servizio perché altri servizi in esecuzione dipendono dal servizio.</span><span class="sxs-lookup"><span data-stu-id="27779-124">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="27779-125">**4**</span><span class="sxs-lookup"><span data-stu-id="27779-125">**4**</span></span>
</dt> <dd>

<span data-ttu-id="27779-126">Il codice di controllo richiesto non è valido o non è accettabile per il servizio.</span><span class="sxs-lookup"><span data-stu-id="27779-126">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="27779-127">**5**</span><span class="sxs-lookup"><span data-stu-id="27779-127">**5**</span></span>
</dt> <dd>

<span data-ttu-id="27779-128">Impossibile inviare il codice di controllo richiesto al servizio perché lo stato del servizio ([**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**Proprietà state** ) è uguale a 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="27779-128">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="27779-129">**6**</span><span class="sxs-lookup"><span data-stu-id="27779-129">**6**</span></span>
</dt> <dd>

<span data-ttu-id="27779-130">Il servizio non è stato avviato.</span><span class="sxs-lookup"><span data-stu-id="27779-130">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="27779-131">**7**</span><span class="sxs-lookup"><span data-stu-id="27779-131">**7**</span></span>
</dt> <dd>

<span data-ttu-id="27779-132">Il servizio non ha risposto in tempo utile alla richiesta di avvio.</span><span class="sxs-lookup"><span data-stu-id="27779-132">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="27779-133">**8**</span><span class="sxs-lookup"><span data-stu-id="27779-133">**8**</span></span>
</dt> <dd>

<span data-ttu-id="27779-134">Errore sconosciuto durante l'avvio del servizio.</span><span class="sxs-lookup"><span data-stu-id="27779-134">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="27779-135">**9**</span><span class="sxs-lookup"><span data-stu-id="27779-135">**9**</span></span>
</dt> <dd>

<span data-ttu-id="27779-136">Impossibile trovare il percorso di directory del file eseguibile del servizio.</span><span class="sxs-lookup"><span data-stu-id="27779-136">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="27779-137">**10**</span><span class="sxs-lookup"><span data-stu-id="27779-137">**10**</span></span>
</dt> <dd>

<span data-ttu-id="27779-138">Il servizio è già in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="27779-138">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="27779-139">**11**</span><span class="sxs-lookup"><span data-stu-id="27779-139">**11**</span></span>
</dt> <dd>

<span data-ttu-id="27779-140">Il database a cui aggiungere il nuovo servizio è bloccato.</span><span class="sxs-lookup"><span data-stu-id="27779-140">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="27779-141">**12**</span><span class="sxs-lookup"><span data-stu-id="27779-141">**12**</span></span>
</dt> <dd>

<span data-ttu-id="27779-142">Una dipendenza su cui si basa questo servizio è stata rimossa dal sistema.</span><span class="sxs-lookup"><span data-stu-id="27779-142">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="27779-143">**13**</span><span class="sxs-lookup"><span data-stu-id="27779-143">**13**</span></span>
</dt> <dd>

<span data-ttu-id="27779-144">Impossibile trovare un servizio dipendente necessario.</span><span class="sxs-lookup"><span data-stu-id="27779-144">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="27779-145">**14**</span><span class="sxs-lookup"><span data-stu-id="27779-145">**14**</span></span>
</dt> <dd>

<span data-ttu-id="27779-146">Il servizio è stato disabilitato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="27779-146">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="27779-147">**15**</span><span class="sxs-lookup"><span data-stu-id="27779-147">**15**</span></span>
</dt> <dd>

<span data-ttu-id="27779-148">Il servizio non dispone delle credenziali di autenticazione corrette per l'esecuzione nel sistema.</span><span class="sxs-lookup"><span data-stu-id="27779-148">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="27779-149">**16**</span><span class="sxs-lookup"><span data-stu-id="27779-149">**16**</span></span>
</dt> <dd>

<span data-ttu-id="27779-150">Questo servizio verrà rimosso dal sistema.</span><span class="sxs-lookup"><span data-stu-id="27779-150">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="27779-151">**17**</span><span class="sxs-lookup"><span data-stu-id="27779-151">**17**</span></span>
</dt> <dd>

<span data-ttu-id="27779-152">Il servizio non dispone di un thread di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="27779-152">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="27779-153">**18**</span><span class="sxs-lookup"><span data-stu-id="27779-153">**18**</span></span>
</dt> <dd>

<span data-ttu-id="27779-154">Il servizio ha dipendenze circolari all'avvio.</span><span class="sxs-lookup"><span data-stu-id="27779-154">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="27779-155">**19**</span><span class="sxs-lookup"><span data-stu-id="27779-155">**19**</span></span>
</dt> <dd>

<span data-ttu-id="27779-156">Un servizio è in esecuzione con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="27779-156">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="27779-157">**20**</span><span class="sxs-lookup"><span data-stu-id="27779-157">**20**</span></span>
</dt> <dd>

<span data-ttu-id="27779-158">Il nome del servizio contiene caratteri non validi.</span><span class="sxs-lookup"><span data-stu-id="27779-158">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="27779-159">**21**</span><span class="sxs-lookup"><span data-stu-id="27779-159">**21**</span></span>
</dt> <dd>

<span data-ttu-id="27779-160">Sono stati passati parametri non validi al servizio.</span><span class="sxs-lookup"><span data-stu-id="27779-160">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="27779-161">**22**</span><span class="sxs-lookup"><span data-stu-id="27779-161">**22**</span></span>
</dt> <dd>

<span data-ttu-id="27779-162">L'account con cui viene eseguito il servizio non è valido o non dispone delle autorizzazioni necessarie per eseguire il servizio.</span><span class="sxs-lookup"><span data-stu-id="27779-162">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="27779-163">**23**</span><span class="sxs-lookup"><span data-stu-id="27779-163">**23**</span></span>
</dt> <dd>

<span data-ttu-id="27779-164">Il servizio esiste già nel database dei servizi disponibili dal sistema.</span><span class="sxs-lookup"><span data-stu-id="27779-164">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="27779-165">**24**</span><span class="sxs-lookup"><span data-stu-id="27779-165">**24**</span></span>
</dt> <dd>

<span data-ttu-id="27779-166">Il servizio è attualmente sospeso nel sistema.</span><span class="sxs-lookup"><span data-stu-id="27779-166">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="27779-167">Commenti</span><span class="sxs-lookup"><span data-stu-id="27779-167">Remarks</span></span>

<span data-ttu-id="27779-168">Dopo aver determinato i servizi che possono essere arrestati o sospesi, è possibile usare i metodi **StopService** e [**PauseService**](win32-terminalservice-pauseservice.md) per arrestare e sospendere i servizi.</span><span class="sxs-lookup"><span data-stu-id="27779-168">After you have determined which services can be stopped or paused, you can use the **StopService** and [**PauseService**](win32-terminalservice-pauseservice.md) methods to stop and pause services.</span></span> <span data-ttu-id="27779-169">La decisione di arrestare un servizio anziché sospenderla, o viceversa, dipende da diversi fattori, inclusi i seguenti:</span><span class="sxs-lookup"><span data-stu-id="27779-169">The decision to stop a service rather than pause it, or vice versa, depends on several factors, including the following:</span></span>

-   <span data-ttu-id="27779-170">Il servizio è in grado di essere sospeso?</span><span class="sxs-lookup"><span data-stu-id="27779-170">Is the service capable of being paused?</span></span> <span data-ttu-id="27779-171">In caso contrario, l'unica opzione è arresta il servizio.</span><span class="sxs-lookup"><span data-stu-id="27779-171">If not, your only option is the stop the service.</span></span>
-   <span data-ttu-id="27779-172">È necessario continuare a gestire le richieste client per chiunque si sia già connessi al servizio?</span><span class="sxs-lookup"><span data-stu-id="27779-172">Do you need to continue handling client requests for anyone already connected to the service?</span></span> <span data-ttu-id="27779-173">In tal caso, sospendere un servizio in genere consente di gestire i client esistenti negando l'accesso ai nuovi client.</span><span class="sxs-lookup"><span data-stu-id="27779-173">If so, pausing a service typically allows it to handle existing clients while denying access to new clients.</span></span> <span data-ttu-id="27779-174">Al contrario, quando si arresta un servizio, tutti i client vengono immediatamente disconnessi.</span><span class="sxs-lookup"><span data-stu-id="27779-174">By contrast, when you stop a service, all clients are immediately disconnected.</span></span>
-   <span data-ttu-id="27779-175">È necessario riconfigurare un servizio e fare in modo che le modifiche abbiano effetto immediato?</span><span class="sxs-lookup"><span data-stu-id="27779-175">Do you need to reconfigure a service and have the changes take effect immediately?</span></span> <span data-ttu-id="27779-176">Sebbene sia possibile modificare le proprietà del servizio mentre un servizio viene sospeso, la maggior parte di esse non diventano effettive fino a quando il servizio non viene effettivamente arrestato e riavviato.</span><span class="sxs-lookup"><span data-stu-id="27779-176">Although service properties can be changed while a service is paused, most of them do not take effect until the service is actually stopped and restarted.</span></span>

<span data-ttu-id="27779-177">Il codice di scripting necessario per arrestare un servizio è quasi identico al codice necessario per sospendere il servizio.</span><span class="sxs-lookup"><span data-stu-id="27779-177">The scripting code required to stop a service is almost identical to the code required to pause the service.</span></span>

<span data-ttu-id="27779-178">Se si tenta di arrestare un servizio che dispone di servizi dipendenti in esecuzione, il metodo **StopService** ha esito negativo con un valore restituito pari a 3.</span><span class="sxs-lookup"><span data-stu-id="27779-178">If you attempt to stop a service which has dependent services running, the **StopService** method fails with a return value of 3.</span></span> <span data-ttu-id="27779-179">I servizi dipendenti devono essere arrestati per primi.</span><span class="sxs-lookup"><span data-stu-id="27779-179">The dependent services must be stopped first.</span></span>

<span data-ttu-id="27779-180">Se si arresta un servizio, controllare immediatamente il [**\_ TerminalService Win32**](win32-terminalservice.md).**Proprietà state** , perché il valore può comunque visualizzare il servizio come in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="27779-180">If you stop a service, then immediately check the [**Win32\_TerminalService**](win32-terminalservice.md).**State** property, as the value may still show the service as running.</span></span>

## <a name="examples"></a><span data-ttu-id="27779-181">Esempio</span><span class="sxs-lookup"><span data-stu-id="27779-181">Examples</span></span>

<span data-ttu-id="27779-182">[Set-RemoteService](https://Gallery.TechNet.Microsoft.Com/79595ce9-bfc3-463e-9e84-d9e0b78590c1) PowerShell Sample imposta lo stato del servizio per i computer remoti.</span><span class="sxs-lookup"><span data-stu-id="27779-182">[The Set-RemoteService](https://Gallery.TechNet.Microsoft.Com/79595ce9-bfc3-463e-9e84-d9e0b78590c1) PowerShell sample Sets service state for remote machines.</span></span>

<span data-ttu-id="27779-183">L'esempio di [arresto di un servizio e del relativo VBScript dipendente](https://Gallery.TechNet.Microsoft.Com/ae07e623-2cbd-4983-b991-aa4d1e6e2732) interrompe un servizio e tutti i servizi dipendenti.</span><span class="sxs-lookup"><span data-stu-id="27779-183">The [Stop a Service and Its Dependents](https://Gallery.TechNet.Microsoft.Com/ae07e623-2cbd-4983-b991-aa4d1e6e2732) VBScript sample stops a service and all dependent services.</span></span>

## <a name="requirements"></a><span data-ttu-id="27779-184">Requisiti</span><span class="sxs-lookup"><span data-stu-id="27779-184">Requirements</span></span>



| <span data-ttu-id="27779-185">Requisito</span><span class="sxs-lookup"><span data-stu-id="27779-185">Requirement</span></span> | <span data-ttu-id="27779-186">Valore</span><span class="sxs-lookup"><span data-stu-id="27779-186">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="27779-187">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="27779-187">Minimum supported client</span></span><br/> | <span data-ttu-id="27779-188">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="27779-188">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="27779-189">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="27779-189">Minimum supported server</span></span><br/> | <span data-ttu-id="27779-190">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="27779-190">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="27779-191">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="27779-191">Namespace</span></span><br/>                | <span data-ttu-id="27779-192">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="27779-192">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="27779-193">Intestazione</span><span class="sxs-lookup"><span data-stu-id="27779-193">Header</span></span><br/>                   | <dl> <span data-ttu-id="27779-194"><dt>Sdoias. h</dt></span><span class="sxs-lookup"><span data-stu-id="27779-194"><dt>Sdoias.h</dt></span></span> </dl>     |
| <span data-ttu-id="27779-195">MOF</span><span class="sxs-lookup"><span data-stu-id="27779-195">MOF</span></span><br/>                      | <dl> <span data-ttu-id="27779-196"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="27779-196"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="27779-197">DLL</span><span class="sxs-lookup"><span data-stu-id="27779-197">DLL</span></span><br/>                      | <dl> <span data-ttu-id="27779-198"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="27779-198"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27779-199">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="27779-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27779-200">**\_Servizio Win32**</span><span class="sxs-lookup"><span data-stu-id="27779-200">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="27779-201">Classi del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="27779-201">Operating System Classes</span></span>](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[<span data-ttu-id="27779-202">**\_TerminalService Win32**</span><span class="sxs-lookup"><span data-stu-id="27779-202">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="27779-203">Attività WMI: Servizi</span><span class="sxs-lookup"><span data-stu-id="27779-203">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> <dt>

[<span data-ttu-id="27779-204">**PauseService**</span><span class="sxs-lookup"><span data-stu-id="27779-204">**PauseService**</span></span>](/windows/desktop/CIMWin32Prov/pauseservice-method-in-class-win32-systemdriver)
</dt> </dl>

 

