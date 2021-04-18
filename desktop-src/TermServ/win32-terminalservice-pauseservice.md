---
title: Metodo PauseService della classe Win32_Service (Servizi Desktop remoto)
description: Esegue un tentativo di sospensione del servizio.
ms.assetid: 101987F6-FBAB-4E79-B1FA-346B1EF58DE1
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo PauseService
- Metodo PauseService Servizi Desktop remoto, classe Win32_Service
- Classe Win32_Service Servizi Desktop remoto, metodo PauseService
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
ms.openlocfilehash: 69951a77530b3aff89148b08e19f3a7c4da8f5b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301290"
---
# <a name="pauseservice-method-of-the-win32_service-class-remote-desktop-services"></a><span data-ttu-id="3cb83-106">Metodo PauseService della classe Win32_Service (Servizi Desktop remoto)</span><span class="sxs-lookup"><span data-stu-id="3cb83-106">PauseService method of the Win32_Service class (Remote Desktop Services)</span></span>

<span data-ttu-id="3cb83-107">Il metodo della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **PauseService** tenta di collocare il servizio nello stato sospeso.</span><span class="sxs-lookup"><span data-stu-id="3cb83-107">The **PauseService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to place the service in the paused state.</span></span>

<span data-ttu-id="3cb83-108">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="3cb83-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="3cb83-109">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="3cb83-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="3cb83-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3cb83-110">Syntax</span></span>


```mof
uint32 PauseService();
```



## <a name="parameters"></a><span data-ttu-id="3cb83-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="3cb83-111">Parameters</span></span>

<span data-ttu-id="3cb83-112">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="3cb83-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3cb83-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3cb83-113">Return value</span></span>

<span data-ttu-id="3cb83-114">Restituisce uno dei valori elencati nell'elenco seguente o qualsiasi altro valore per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="3cb83-114">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="3cb83-115">Per ulteriori codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="3cb83-115">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="3cb83-116">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="3cb83-116">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="3cb83-117">**0**</span><span class="sxs-lookup"><span data-stu-id="3cb83-117">**0**</span></span>
</dt> <dd>

<span data-ttu-id="3cb83-118">La richiesta è stata accettata.</span><span class="sxs-lookup"><span data-stu-id="3cb83-118">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="3cb83-119">**1**</span><span class="sxs-lookup"><span data-stu-id="3cb83-119">**1**</span></span>
</dt> <dd>

<span data-ttu-id="3cb83-120">La richiesta non è supportata.</span><span class="sxs-lookup"><span data-stu-id="3cb83-120">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="3cb83-121">**2**</span><span class="sxs-lookup"><span data-stu-id="3cb83-121">**2**</span></span>
</dt> <dd>

<span data-ttu-id="3cb83-122">L'utente non dispone dell'accesso necessario.</span><span class="sxs-lookup"><span data-stu-id="3cb83-122">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="3cb83-123">**3**</span><span class="sxs-lookup"><span data-stu-id="3cb83-123">**3**</span></span>
</dt> <dd>

<span data-ttu-id="3cb83-124">Impossibile arrestare il servizio perché altri servizi in esecuzione dipendono dal servizio.</span><span class="sxs-lookup"><span data-stu-id="3cb83-124">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="3cb83-125">**4**</span><span class="sxs-lookup"><span data-stu-id="3cb83-125">**4**</span></span>
</dt> <dd>

<span data-ttu-id="3cb83-126">Il codice di controllo richiesto non è valido o non è accettabile per il servizio.</span><span class="sxs-lookup"><span data-stu-id="3cb83-126">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="3cb83-127">**5**</span><span class="sxs-lookup"><span data-stu-id="3cb83-127">**5**</span></span>
</dt> <dd>

<span data-ttu-id="3cb83-128">Impossibile inviare il codice di controllo richiesto al servizio perché lo stato del servizio ([**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**Proprietà state** ) è uguale a 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="3cb83-128">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="3cb83-129">**6**</span><span class="sxs-lookup"><span data-stu-id="3cb83-129">**6**</span></span>
</dt> <dd>

<span data-ttu-id="3cb83-130">Il servizio non è stato avviato.</span><span class="sxs-lookup"><span data-stu-id="3cb83-130">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="3cb83-131">**7**</span><span class="sxs-lookup"><span data-stu-id="3cb83-131">**7**</span></span>
</dt> <dd>

<span data-ttu-id="3cb83-132">Il servizio non ha risposto in tempo utile alla richiesta di avvio.</span><span class="sxs-lookup"><span data-stu-id="3cb83-132">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="3cb83-133">**8**</span><span class="sxs-lookup"><span data-stu-id="3cb83-133">**8**</span></span>
</dt> <dd>

<span data-ttu-id="3cb83-134">Errore sconosciuto durante l'avvio del servizio.</span><span class="sxs-lookup"><span data-stu-id="3cb83-134">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="3cb83-135">**9**</span><span class="sxs-lookup"><span data-stu-id="3cb83-135">**9**</span></span>
</dt> <dd>

<span data-ttu-id="3cb83-136">Impossibile trovare il percorso di directory del file eseguibile del servizio.</span><span class="sxs-lookup"><span data-stu-id="3cb83-136">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="3cb83-137">**10**</span><span class="sxs-lookup"><span data-stu-id="3cb83-137">**10**</span></span>
</dt> <dd>

<span data-ttu-id="3cb83-138">Il servizio è già in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="3cb83-138">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="3cb83-139">**11**</span><span class="sxs-lookup"><span data-stu-id="3cb83-139">**11**</span></span>
</dt> <dd>

<span data-ttu-id="3cb83-140">Il database a cui aggiungere il nuovo servizio è bloccato.</span><span class="sxs-lookup"><span data-stu-id="3cb83-140">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="3cb83-141">**12**</span><span class="sxs-lookup"><span data-stu-id="3cb83-141">**12**</span></span>
</dt> <dd>

<span data-ttu-id="3cb83-142">Una dipendenza su cui si basa questo servizio è stata rimossa dal sistema.</span><span class="sxs-lookup"><span data-stu-id="3cb83-142">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="3cb83-143">**13**</span><span class="sxs-lookup"><span data-stu-id="3cb83-143">**13**</span></span>
</dt> <dd>

<span data-ttu-id="3cb83-144">Impossibile trovare un servizio dipendente necessario.</span><span class="sxs-lookup"><span data-stu-id="3cb83-144">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="3cb83-145">**14**</span><span class="sxs-lookup"><span data-stu-id="3cb83-145">**14**</span></span>
</dt> <dd>

<span data-ttu-id="3cb83-146">Il servizio è stato disabilitato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="3cb83-146">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="3cb83-147">**15**</span><span class="sxs-lookup"><span data-stu-id="3cb83-147">**15**</span></span>
</dt> <dd>

<span data-ttu-id="3cb83-148">Il servizio non dispone delle credenziali di autenticazione corrette per l'esecuzione nel sistema.</span><span class="sxs-lookup"><span data-stu-id="3cb83-148">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="3cb83-149">**16**</span><span class="sxs-lookup"><span data-stu-id="3cb83-149">**16**</span></span>
</dt> <dd>

<span data-ttu-id="3cb83-150">Questo servizio verrà rimosso dal sistema.</span><span class="sxs-lookup"><span data-stu-id="3cb83-150">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="3cb83-151">**17**</span><span class="sxs-lookup"><span data-stu-id="3cb83-151">**17**</span></span>
</dt> <dd>

<span data-ttu-id="3cb83-152">Il servizio non dispone di un thread di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="3cb83-152">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="3cb83-153">**18**</span><span class="sxs-lookup"><span data-stu-id="3cb83-153">**18**</span></span>
</dt> <dd>

<span data-ttu-id="3cb83-154">Il servizio ha dipendenze circolari all'avvio.</span><span class="sxs-lookup"><span data-stu-id="3cb83-154">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="3cb83-155">**19**</span><span class="sxs-lookup"><span data-stu-id="3cb83-155">**19**</span></span>
</dt> <dd>

<span data-ttu-id="3cb83-156">Un servizio è in esecuzione con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="3cb83-156">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="3cb83-157">**20**</span><span class="sxs-lookup"><span data-stu-id="3cb83-157">**20**</span></span>
</dt> <dd>

<span data-ttu-id="3cb83-158">Il nome del servizio contiene caratteri non validi.</span><span class="sxs-lookup"><span data-stu-id="3cb83-158">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="3cb83-159">**21**</span><span class="sxs-lookup"><span data-stu-id="3cb83-159">**21**</span></span>
</dt> <dd>

<span data-ttu-id="3cb83-160">Sono stati passati parametri non validi al servizio.</span><span class="sxs-lookup"><span data-stu-id="3cb83-160">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="3cb83-161">**22**</span><span class="sxs-lookup"><span data-stu-id="3cb83-161">**22**</span></span>
</dt> <dd>

<span data-ttu-id="3cb83-162">L'account con cui viene eseguito il servizio non è valido o non dispone delle autorizzazioni necessarie per eseguire il servizio.</span><span class="sxs-lookup"><span data-stu-id="3cb83-162">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="3cb83-163">**23**</span><span class="sxs-lookup"><span data-stu-id="3cb83-163">**23**</span></span>
</dt> <dd>

<span data-ttu-id="3cb83-164">Il servizio esiste già nel database dei servizi disponibili dal sistema.</span><span class="sxs-lookup"><span data-stu-id="3cb83-164">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="3cb83-165">**24**</span><span class="sxs-lookup"><span data-stu-id="3cb83-165">**24**</span></span>
</dt> <dd>

<span data-ttu-id="3cb83-166">Il servizio è attualmente sospeso nel sistema.</span><span class="sxs-lookup"><span data-stu-id="3cb83-166">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3cb83-167">Commenti</span><span class="sxs-lookup"><span data-stu-id="3cb83-167">Remarks</span></span>

<span data-ttu-id="3cb83-168">Dopo aver determinato i servizi che possono essere arrestati o sospesi, è possibile usare i metodi [**StopService**](win32-terminalservice-stopservice.md) e **PauseService** per arrestare e sospendere i servizi.</span><span class="sxs-lookup"><span data-stu-id="3cb83-168">After you have determined which services can be stopped or paused, you can use the [**StopService**](win32-terminalservice-stopservice.md) and **PauseService** methods to stop and pause services.</span></span> <span data-ttu-id="3cb83-169">La decisione di arrestare un servizio anziché sospenderla, o viceversa, dipende da diversi fattori, inclusi i seguenti:</span><span class="sxs-lookup"><span data-stu-id="3cb83-169">The decision to stop a service rather than pause it, or vice versa, depends on several factors, including the following:</span></span>

-   <span data-ttu-id="3cb83-170">Il servizio è in grado di essere sospeso?</span><span class="sxs-lookup"><span data-stu-id="3cb83-170">Is the service capable of being paused?</span></span> <span data-ttu-id="3cb83-171">In caso contrario, l'unica opzione è arresta il servizio.</span><span class="sxs-lookup"><span data-stu-id="3cb83-171">If not, your only option is the stop the service.</span></span>
-   <span data-ttu-id="3cb83-172">È necessario continuare a gestire le richieste client per chiunque si sia già connessi al servizio?</span><span class="sxs-lookup"><span data-stu-id="3cb83-172">Do you need to continue handling client requests for anyone already connected to the service?</span></span> <span data-ttu-id="3cb83-173">In tal caso, sospendere un servizio in genere consente di gestire i client esistenti negando l'accesso ai nuovi client.</span><span class="sxs-lookup"><span data-stu-id="3cb83-173">If so, pausing a service typically allows it to handle existing clients while denying access to new clients.</span></span> <span data-ttu-id="3cb83-174">Al contrario, quando si arresta un servizio, tutti i client vengono immediatamente disconnessi.</span><span class="sxs-lookup"><span data-stu-id="3cb83-174">By contrast, when you stop a service, all clients are immediately disconnected.</span></span>
-   <span data-ttu-id="3cb83-175">È necessario riconfigurare un servizio e fare in modo che le modifiche abbiano effetto immediato?</span><span class="sxs-lookup"><span data-stu-id="3cb83-175">Do you need to reconfigure a service and have the changes take effect immediately?</span></span> <span data-ttu-id="3cb83-176">Sebbene sia possibile modificare le proprietà del servizio mentre un servizio viene sospeso, la maggior parte di esse non diventano effettive fino a quando il servizio non viene effettivamente arrestato e riavviato.</span><span class="sxs-lookup"><span data-stu-id="3cb83-176">Although service properties can be changed while a service is paused, most of them do not take effect until the service is actually stopped and restarted.</span></span>

<span data-ttu-id="3cb83-177">Il codice di scripting necessario per arrestare un servizio è quasi identico al codice necessario per sospendere il servizio.</span><span class="sxs-lookup"><span data-stu-id="3cb83-177">The scripting code required to stop a service is almost identical to the code required to pause the service.</span></span>

## <a name="examples"></a><span data-ttu-id="3cb83-178">Esempio</span><span class="sxs-lookup"><span data-stu-id="3cb83-178">Examples</span></span>

<span data-ttu-id="3cb83-179">L'esempio di [sospensione dei servizi in esecuzione in un account VBScript specifico](https://Gallery.TechNet.Microsoft.Com/12a256dd-39da-4690-b3f0-f0adccaf25f1) mette in pausa tutti i servizi in esecuzione con l'ipotetico account del servizio NETSVC.</span><span class="sxs-lookup"><span data-stu-id="3cb83-179">The [Pause Services Running Under a Specific Account](https://Gallery.TechNet.Microsoft.Com/12a256dd-39da-4690-b3f0-f0adccaf25f1) VBScript sample Pauses all services running under the hypothetical service account Netsvc.</span></span>

## <a name="requirements"></a><span data-ttu-id="3cb83-180">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3cb83-180">Requirements</span></span>



| <span data-ttu-id="3cb83-181">Requisito</span><span class="sxs-lookup"><span data-stu-id="3cb83-181">Requirement</span></span> | <span data-ttu-id="3cb83-182">Valore</span><span class="sxs-lookup"><span data-stu-id="3cb83-182">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3cb83-183">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3cb83-183">Minimum supported client</span></span><br/> | <span data-ttu-id="3cb83-184">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3cb83-184">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3cb83-185">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3cb83-185">Minimum supported server</span></span><br/> | <span data-ttu-id="3cb83-186">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3cb83-186">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3cb83-187">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3cb83-187">Namespace</span></span><br/>                | <span data-ttu-id="3cb83-188">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="3cb83-188">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="3cb83-189">MOF</span><span class="sxs-lookup"><span data-stu-id="3cb83-189">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3cb83-190"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3cb83-190"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="3cb83-191">DLL</span><span class="sxs-lookup"><span data-stu-id="3cb83-191">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3cb83-192"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3cb83-192"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3cb83-193">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3cb83-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3cb83-194">**\_Servizio Win32**</span><span class="sxs-lookup"><span data-stu-id="3cb83-194">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="3cb83-195">Classi del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="3cb83-195">Operating System Classes</span></span>](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[<span data-ttu-id="3cb83-196">**\_TerminalService Win32**</span><span class="sxs-lookup"><span data-stu-id="3cb83-196">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="3cb83-197">Attività WMI: Servizi</span><span class="sxs-lookup"><span data-stu-id="3cb83-197">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> <dt>

[<span data-ttu-id="3cb83-198">**StopService**</span><span class="sxs-lookup"><span data-stu-id="3cb83-198">**StopService**</span></span>](/windows/desktop/CIMWin32Prov/stopservice-method-in-class-win32-service)
</dt> </dl>

 

