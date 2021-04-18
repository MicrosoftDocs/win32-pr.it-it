---
title: Metodo ChangeStartMode della classe Win32_Service (Servizi Desktop remoto)
description: Modifica la modalità di avvio di un \_ TerminalService Win32.
ms.assetid: 4F4B8CFC-B38C-47C6-A2BA-D498EC2B7F55
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo ChangeStartMode
- Metodo ChangeStartMode Servizi Desktop remoto, classe Win32_Service
- Classe Win32_Service Servizi Desktop remoto, metodo ChangeStartMode
topic_type:
- apiref
api_name:
- Win32_Service.ChangeStartMode
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a46c6b72fbb070dac32b2b6990a217068c77da9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301514"
---
# <a name="changestartmode-method-of-the-win32_service-class-remote-desktop-services"></a><span data-ttu-id="b1bef-106">Metodo ChangeStartMode della classe Win32_Service (Servizi Desktop remoto)</span><span class="sxs-lookup"><span data-stu-id="b1bef-106">ChangeStartMode method of the Win32_Service class (Remote Desktop Services)</span></span>

<span data-ttu-id="b1bef-107">Il metodo della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **ChangeStartMode** modifica la modalità di avvio di un [**\_ TerminalService Win32**](win32-terminalservice.md).</span><span class="sxs-lookup"><span data-stu-id="b1bef-107">The **ChangeStartMode** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method modifies the start mode of a [**Win32\_TerminalService**](win32-terminalservice.md).</span></span>

<span data-ttu-id="b1bef-108">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="b1bef-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="b1bef-109">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="b1bef-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="b1bef-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b1bef-110">Syntax</span></span>


```mof
uint32 ChangeStartMode(
  [in] string StartMode
);
```



## <a name="parameters"></a><span data-ttu-id="b1bef-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="b1bef-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1bef-112">*StartMode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b1bef-112">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1bef-113">Modalità di avvio del servizio di base di Windows.</span><span class="sxs-lookup"><span data-stu-id="b1bef-113">Start mode of the Windows base service.</span></span>

<dt>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>

<span data-ttu-id="b1bef-114"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Boot**</span><span class="sxs-lookup"><span data-stu-id="b1bef-114"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Boot**</span></span>


</dt> <dd>

<span data-ttu-id="b1bef-115">Driver di dispositivo avviato dal caricatore del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="b1bef-115">Device driver started by the operating system loader.</span></span> <span data-ttu-id="b1bef-116">Questo valore è valido solo per i servizi del driver.</span><span class="sxs-lookup"><span data-stu-id="b1bef-116">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span data-ttu-id="b1bef-117"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**Sistema**</span><span class="sxs-lookup"><span data-stu-id="b1bef-117"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System**</span></span>


</dt> <dd>

<span data-ttu-id="b1bef-118">Driver di dispositivo avviato dal processo di inizializzazione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="b1bef-118">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="b1bef-119">Questo valore è valido solo per i servizi del driver.</span><span class="sxs-lookup"><span data-stu-id="b1bef-119">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="b1bef-120"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automatico**</span><span class="sxs-lookup"><span data-stu-id="b1bef-120"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automatic**</span></span>


</dt> <dd>

<span data-ttu-id="b1bef-121">Servizio da avviare automaticamente da Gestione controllo servizi durante l'avvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="b1bef-121">Service to be started automatically by the Service Control Manager during system startup.</span></span>

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="b1bef-122"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manuale**</span><span class="sxs-lookup"><span data-stu-id="b1bef-122"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manual**</span></span>


</dt> <dd>

<span data-ttu-id="b1bef-123">Servizio che deve essere avviato da Gestione controllo servizi quando un processo chiama il metodo [**StartService**](win32-terminalservice-startservice.md) .</span><span class="sxs-lookup"><span data-stu-id="b1bef-123">Service to be started by the Service Control Manager when a process calls the [**StartService**](win32-terminalservice-startservice.md) method.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="b1bef-124"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato**</span><span class="sxs-lookup"><span data-stu-id="b1bef-124"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled**</span></span>


</dt> <dd>

<span data-ttu-id="b1bef-125">Servizio che non può più essere avviato.</span><span class="sxs-lookup"><span data-stu-id="b1bef-125">Service that can no longer be started.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1bef-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b1bef-126">Return value</span></span>

<span data-ttu-id="b1bef-127">Restituisce uno dei valori elencati nell'elenco seguente o qualsiasi altro valore per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="b1bef-127">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="b1bef-128">Per ulteriori codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="b1bef-128">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="b1bef-129">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="b1bef-129">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="b1bef-130">**0**</span><span class="sxs-lookup"><span data-stu-id="b1bef-130">**0**</span></span>
</dt> <dd>

<span data-ttu-id="b1bef-131">La richiesta è stata accettata.</span><span class="sxs-lookup"><span data-stu-id="b1bef-131">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="b1bef-132">**1**</span><span class="sxs-lookup"><span data-stu-id="b1bef-132">**1**</span></span>
</dt> <dd>

<span data-ttu-id="b1bef-133">La richiesta non è supportata.</span><span class="sxs-lookup"><span data-stu-id="b1bef-133">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="b1bef-134">**2**</span><span class="sxs-lookup"><span data-stu-id="b1bef-134">**2**</span></span>
</dt> <dd>

<span data-ttu-id="b1bef-135">L'utente non dispone dell'accesso necessario.</span><span class="sxs-lookup"><span data-stu-id="b1bef-135">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="b1bef-136">**3**</span><span class="sxs-lookup"><span data-stu-id="b1bef-136">**3**</span></span>
</dt> <dd>

<span data-ttu-id="b1bef-137">Impossibile arrestare il servizio perché altri servizi in esecuzione dipendono dal servizio.</span><span class="sxs-lookup"><span data-stu-id="b1bef-137">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="b1bef-138">**4**</span><span class="sxs-lookup"><span data-stu-id="b1bef-138">**4**</span></span>
</dt> <dd>

<span data-ttu-id="b1bef-139">Il codice di controllo richiesto non è valido o non è accettabile per il servizio.</span><span class="sxs-lookup"><span data-stu-id="b1bef-139">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="b1bef-140">**5**</span><span class="sxs-lookup"><span data-stu-id="b1bef-140">**5**</span></span>
</dt> <dd>

<span data-ttu-id="b1bef-141">Impossibile inviare il codice di controllo richiesto al servizio perché lo stato del servizio ([**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**Proprietà state** ) è uguale a 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="b1bef-141">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="b1bef-142">**6**</span><span class="sxs-lookup"><span data-stu-id="b1bef-142">**6**</span></span>
</dt> <dd>

<span data-ttu-id="b1bef-143">Il servizio non è stato avviato.</span><span class="sxs-lookup"><span data-stu-id="b1bef-143">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="b1bef-144">**7**</span><span class="sxs-lookup"><span data-stu-id="b1bef-144">**7**</span></span>
</dt> <dd>

<span data-ttu-id="b1bef-145">Il servizio non ha risposto in tempo utile alla richiesta di avvio.</span><span class="sxs-lookup"><span data-stu-id="b1bef-145">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="b1bef-146">**8**</span><span class="sxs-lookup"><span data-stu-id="b1bef-146">**8**</span></span>
</dt> <dd>

<span data-ttu-id="b1bef-147">Errore sconosciuto durante l'avvio del servizio.</span><span class="sxs-lookup"><span data-stu-id="b1bef-147">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="b1bef-148">**9**</span><span class="sxs-lookup"><span data-stu-id="b1bef-148">**9**</span></span>
</dt> <dd>

<span data-ttu-id="b1bef-149">Impossibile trovare il percorso di directory del file eseguibile del servizio.</span><span class="sxs-lookup"><span data-stu-id="b1bef-149">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="b1bef-150">**10**</span><span class="sxs-lookup"><span data-stu-id="b1bef-150">**10**</span></span>
</dt> <dd>

<span data-ttu-id="b1bef-151">Il servizio è già in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="b1bef-151">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="b1bef-152">**11**</span><span class="sxs-lookup"><span data-stu-id="b1bef-152">**11**</span></span>
</dt> <dd>

<span data-ttu-id="b1bef-153">Il database a cui aggiungere il nuovo servizio è bloccato.</span><span class="sxs-lookup"><span data-stu-id="b1bef-153">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="b1bef-154">**12**</span><span class="sxs-lookup"><span data-stu-id="b1bef-154">**12**</span></span>
</dt> <dd>

<span data-ttu-id="b1bef-155">Una dipendenza su cui si basa questo servizio è stata rimossa dal sistema.</span><span class="sxs-lookup"><span data-stu-id="b1bef-155">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="b1bef-156">**13**</span><span class="sxs-lookup"><span data-stu-id="b1bef-156">**13**</span></span>
</dt> <dd>

<span data-ttu-id="b1bef-157">Impossibile trovare un servizio dipendente necessario.</span><span class="sxs-lookup"><span data-stu-id="b1bef-157">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="b1bef-158">**14**</span><span class="sxs-lookup"><span data-stu-id="b1bef-158">**14**</span></span>
</dt> <dd>

<span data-ttu-id="b1bef-159">Il servizio è stato disabilitato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="b1bef-159">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="b1bef-160">**15**</span><span class="sxs-lookup"><span data-stu-id="b1bef-160">**15**</span></span>
</dt> <dd>

<span data-ttu-id="b1bef-161">Il servizio non dispone delle credenziali di autenticazione corrette per l'esecuzione nel sistema.</span><span class="sxs-lookup"><span data-stu-id="b1bef-161">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="b1bef-162">**16**</span><span class="sxs-lookup"><span data-stu-id="b1bef-162">**16**</span></span>
</dt> <dd>

<span data-ttu-id="b1bef-163">Questo servizio verrà rimosso dal sistema.</span><span class="sxs-lookup"><span data-stu-id="b1bef-163">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="b1bef-164">**17**</span><span class="sxs-lookup"><span data-stu-id="b1bef-164">**17**</span></span>
</dt> <dd>

<span data-ttu-id="b1bef-165">Il servizio non dispone di un thread di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="b1bef-165">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="b1bef-166">**18**</span><span class="sxs-lookup"><span data-stu-id="b1bef-166">**18**</span></span>
</dt> <dd>

<span data-ttu-id="b1bef-167">Il servizio ha dipendenze circolari all'avvio.</span><span class="sxs-lookup"><span data-stu-id="b1bef-167">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="b1bef-168">**19**</span><span class="sxs-lookup"><span data-stu-id="b1bef-168">**19**</span></span>
</dt> <dd>

<span data-ttu-id="b1bef-169">Un servizio è in esecuzione con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="b1bef-169">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="b1bef-170">**20**</span><span class="sxs-lookup"><span data-stu-id="b1bef-170">**20**</span></span>
</dt> <dd>

<span data-ttu-id="b1bef-171">Il nome del servizio contiene caratteri non validi.</span><span class="sxs-lookup"><span data-stu-id="b1bef-171">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="b1bef-172">**21**</span><span class="sxs-lookup"><span data-stu-id="b1bef-172">**21**</span></span>
</dt> <dd>

<span data-ttu-id="b1bef-173">Sono stati passati parametri non validi al servizio.</span><span class="sxs-lookup"><span data-stu-id="b1bef-173">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="b1bef-174">**22**</span><span class="sxs-lookup"><span data-stu-id="b1bef-174">**22**</span></span>
</dt> <dd>

<span data-ttu-id="b1bef-175">L'account con cui viene eseguito il servizio non è valido o non dispone delle autorizzazioni necessarie per eseguire il servizio.</span><span class="sxs-lookup"><span data-stu-id="b1bef-175">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="b1bef-176">**23**</span><span class="sxs-lookup"><span data-stu-id="b1bef-176">**23**</span></span>
</dt> <dd>

<span data-ttu-id="b1bef-177">Il servizio esiste già nel database dei servizi disponibili dal sistema.</span><span class="sxs-lookup"><span data-stu-id="b1bef-177">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="b1bef-178">**24**</span><span class="sxs-lookup"><span data-stu-id="b1bef-178">**24**</span></span>
</dt> <dd>

<span data-ttu-id="b1bef-179">Il servizio è attualmente sospeso nel sistema.</span><span class="sxs-lookup"><span data-stu-id="b1bef-179">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="b1bef-180">Esempio</span><span class="sxs-lookup"><span data-stu-id="b1bef-180">Examples</span></span>

<span data-ttu-id="b1bef-181">La seguente [modifica StartMode di un esempio di servizio](https://Gallery.TechNet.Microsoft.Com/6d0f06ed-f840-4228-ad2d-e16ebe6a3aed) PowerShell, Estratto dalla raccolta TechNet, modifica la modalità di avvio di un servizio.</span><span class="sxs-lookup"><span data-stu-id="b1bef-181">The following [Change StartMode of a Service](https://Gallery.TechNet.Microsoft.Com/6d0f06ed-f840-4228-ad2d-e16ebe6a3aed) PowerShell sample, pulled from TechNet Gallery, changes the start mode of a service.</span></span>


```PowerShell
$wmi = get-wmiobject -class win32_service -namespace root\cimv2 -computername lisbon | 
where-object { $_.name -eq 'bits' } 
 
$rtn = $wmi.changestartmode("manual") 
if($rtn.returnvalue -eq 0) { "success" } 
ELSE 
  { " $($rtn.returnvalue) was reported" }
```



## <a name="requirements"></a><span data-ttu-id="b1bef-182">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b1bef-182">Requirements</span></span>



| <span data-ttu-id="b1bef-183">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1bef-183">Requirement</span></span> | <span data-ttu-id="b1bef-184">Valore</span><span class="sxs-lookup"><span data-stu-id="b1bef-184">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1bef-185">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b1bef-185">Minimum supported client</span></span><br/> | <span data-ttu-id="b1bef-186">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b1bef-186">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b1bef-187">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b1bef-187">Minimum supported server</span></span><br/> | <span data-ttu-id="b1bef-188">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b1bef-188">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b1bef-189">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b1bef-189">Namespace</span></span><br/>                | <span data-ttu-id="b1bef-190">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="b1bef-190">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="b1bef-191">MOF</span><span class="sxs-lookup"><span data-stu-id="b1bef-191">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b1bef-192"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b1bef-192"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="b1bef-193">DLL</span><span class="sxs-lookup"><span data-stu-id="b1bef-193">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b1bef-194"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b1bef-194"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1bef-195">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b1bef-195">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1bef-196">**\_Servizio Win32**</span><span class="sxs-lookup"><span data-stu-id="b1bef-196">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="b1bef-197">Classi del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="b1bef-197">Operating System Classes</span></span>](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[<span data-ttu-id="b1bef-198">**\_TerminalService Win32**</span><span class="sxs-lookup"><span data-stu-id="b1bef-198">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="b1bef-199">Attività WMI: Servizi</span><span class="sxs-lookup"><span data-stu-id="b1bef-199">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

