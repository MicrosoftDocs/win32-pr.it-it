---
title: Metodo GetSecurityDescriptor della classe Win32_Service (Servizi Desktop remoto)
description: "Metodo GetSecurityDescriptor della classe Win32_Service (Servizi Desktop remoto): restituisce il descrittore di sicurezza che controlla l'accesso al servizio."
ms.assetid: 9898091A-5BE2-42A0-BF81-13AB74696ACB
ms.tgt_platform: multiple
keywords:
- scripting Strumentazione gestione Windows , sicurezza
- sicurezza Strumentazione gestione Windows , scripting
- Metodo GetSecurityDescriptor Servizi Desktop remoto
- Il metodo GetSecurityDescriptor Servizi Desktop remoto , Win32_Service classe
- Win32_Service classe Servizi Desktop remoto, metodo GetSecurityDescriptor
topic_type:
- apiref
api_name:
- Win32_Service.GetSecurityDescriptor
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea5b8a9b945048f947aa273e1ccc1f4514469681
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090649"
---
# <a name="getsecuritydescriptor-method-of-the-win32_service-class-remote-desktop-services"></a><span data-ttu-id="4bd51-108">Metodo GetSecurityDescriptor della classe Win32_Service (Servizi Desktop remoto)</span><span class="sxs-lookup"><span data-stu-id="4bd51-108">GetSecurityDescriptor method of the Win32_Service class (Remote Desktop Services)</span></span>

<span data-ttu-id="4bd51-109">Il **metodo GetSecurityDescriptor** restituisce il descrittore di sicurezza che controlla l'accesso al servizio.</span><span class="sxs-lookup"><span data-stu-id="4bd51-109">The **GetSecurityDescriptor** method returns the security descriptor that controls access to the service.</span></span> <span data-ttu-id="4bd51-110">Il descrittore viene restituito come istanza di [**Win32 \_ SecurityDescriptor.**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)</span><span class="sxs-lookup"><span data-stu-id="4bd51-110">The descriptor is returned as an instance of [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span>

## <a name="syntax"></a><span data-ttu-id="4bd51-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4bd51-111">Syntax</span></span>


```mof
uint32 GetSecurityDescriptor(
  [out] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a><span data-ttu-id="4bd51-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="4bd51-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4bd51-113">*Descrittore* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="4bd51-113">*Descriptor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4bd51-114">Descrittore di sicurezza associato al servizio.</span><span class="sxs-lookup"><span data-stu-id="4bd51-114">The security descriptor associated with the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4bd51-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4bd51-115">Return value</span></span>

<span data-ttu-id="4bd51-116">Restituisce uno dei valori elencati nell'elenco seguente o un valore diverso per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="4bd51-116">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="4bd51-117">Per altri codici di errore, [**vedere Costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum.**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)</span><span class="sxs-lookup"><span data-stu-id="4bd51-117">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="4bd51-118">Per i valori **HRESULT** generali, vedere [Codici di errore di sistema.](/windows/desktop/Debug/system-error-codes)</span><span class="sxs-lookup"><span data-stu-id="4bd51-118">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="4bd51-119">**0**</span><span class="sxs-lookup"><span data-stu-id="4bd51-119">**0**</span></span>
</dt> <dd>

<span data-ttu-id="4bd51-120">La richiesta è stata accettata.</span><span class="sxs-lookup"><span data-stu-id="4bd51-120">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="4bd51-121">**1**</span><span class="sxs-lookup"><span data-stu-id="4bd51-121">**1**</span></span>
</dt> <dd>

<span data-ttu-id="4bd51-122">La richiesta non è supportata.</span><span class="sxs-lookup"><span data-stu-id="4bd51-122">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="4bd51-123">**2**</span><span class="sxs-lookup"><span data-stu-id="4bd51-123">**2**</span></span>
</dt> <dd>

<span data-ttu-id="4bd51-124">L'utente non aveva l'accesso necessario.</span><span class="sxs-lookup"><span data-stu-id="4bd51-124">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="4bd51-125">**3**</span><span class="sxs-lookup"><span data-stu-id="4bd51-125">**3**</span></span>
</dt> <dd>

<span data-ttu-id="4bd51-126">Impossibile arrestare il servizio perché altri servizi in esecuzione dipendono dal servizio.</span><span class="sxs-lookup"><span data-stu-id="4bd51-126">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="4bd51-127">**4**</span><span class="sxs-lookup"><span data-stu-id="4bd51-127">**4**</span></span>
</dt> <dd>

<span data-ttu-id="4bd51-128">Il codice di controllo richiesto non è valido o non è accettabile per il servizio.</span><span class="sxs-lookup"><span data-stu-id="4bd51-128">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="4bd51-129">**5**</span><span class="sxs-lookup"><span data-stu-id="4bd51-129">**5**</span></span>
</dt> <dd>

<span data-ttu-id="4bd51-130">Il codice di controllo richiesto non può essere inviato al servizio perché lo stato del servizio ([**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State)** è uguale a 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="4bd51-130">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="4bd51-131">**6**</span><span class="sxs-lookup"><span data-stu-id="4bd51-131">**6**</span></span>
</dt> <dd>

<span data-ttu-id="4bd51-132">Il servizio non è stato avviato.</span><span class="sxs-lookup"><span data-stu-id="4bd51-132">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="4bd51-133">**7**</span><span class="sxs-lookup"><span data-stu-id="4bd51-133">**7**</span></span>
</dt> <dd>

<span data-ttu-id="4bd51-134">Il servizio non ha risposto in tempo utile alla richiesta di avvio.</span><span class="sxs-lookup"><span data-stu-id="4bd51-134">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="4bd51-135">**8**</span><span class="sxs-lookup"><span data-stu-id="4bd51-135">**8**</span></span>
</dt> <dd>

<span data-ttu-id="4bd51-136">Errore sconosciuto durante l'avvio del servizio.</span><span class="sxs-lookup"><span data-stu-id="4bd51-136">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="4bd51-137">**9**</span><span class="sxs-lookup"><span data-stu-id="4bd51-137">**9**</span></span>
</dt> <dd>

<span data-ttu-id="4bd51-138">Impossibile trovare il percorso della directory del file eseguibile del servizio.</span><span class="sxs-lookup"><span data-stu-id="4bd51-138">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="4bd51-139">**10**</span><span class="sxs-lookup"><span data-stu-id="4bd51-139">**10**</span></span>
</dt> <dd>

<span data-ttu-id="4bd51-140">Il servizio è già in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="4bd51-140">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="4bd51-141">**11**</span><span class="sxs-lookup"><span data-stu-id="4bd51-141">**11**</span></span>
</dt> <dd>

<span data-ttu-id="4bd51-142">Il database a cui aggiungere il nuovo servizio è bloccato.</span><span class="sxs-lookup"><span data-stu-id="4bd51-142">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="4bd51-143">**12**</span><span class="sxs-lookup"><span data-stu-id="4bd51-143">**12**</span></span>
</dt> <dd>

<span data-ttu-id="4bd51-144">Una dipendenza su cui si basa questo servizio è stata rimossa dal sistema.</span><span class="sxs-lookup"><span data-stu-id="4bd51-144">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="4bd51-145">**13**</span><span class="sxs-lookup"><span data-stu-id="4bd51-145">**13**</span></span>
</dt> <dd>

<span data-ttu-id="4bd51-146">Impossibile trovare un servizio dipendente necessario.</span><span class="sxs-lookup"><span data-stu-id="4bd51-146">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="4bd51-147">**14**</span><span class="sxs-lookup"><span data-stu-id="4bd51-147">**14**</span></span>
</dt> <dd>

<span data-ttu-id="4bd51-148">Il servizio è stato disabilitato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="4bd51-148">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="4bd51-149">**15**</span><span class="sxs-lookup"><span data-stu-id="4bd51-149">**15**</span></span>
</dt> <dd>

<span data-ttu-id="4bd51-150">Il servizio non dispone delle credenziali di autenticazione corrette per l'esecuzione nel sistema.</span><span class="sxs-lookup"><span data-stu-id="4bd51-150">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="4bd51-151">**16**</span><span class="sxs-lookup"><span data-stu-id="4bd51-151">**16**</span></span>
</dt> <dd>

<span data-ttu-id="4bd51-152">Questo servizio viene rimosso dal sistema.</span><span class="sxs-lookup"><span data-stu-id="4bd51-152">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="4bd51-153">**17**</span><span class="sxs-lookup"><span data-stu-id="4bd51-153">**17**</span></span>
</dt> <dd>

<span data-ttu-id="4bd51-154">Il servizio non ha thread di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="4bd51-154">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="4bd51-155">**18**</span><span class="sxs-lookup"><span data-stu-id="4bd51-155">**18**</span></span>
</dt> <dd>

<span data-ttu-id="4bd51-156">Il servizio ha dipendenze circolari all'avvio.</span><span class="sxs-lookup"><span data-stu-id="4bd51-156">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="4bd51-157">**19**</span><span class="sxs-lookup"><span data-stu-id="4bd51-157">**19**</span></span>
</dt> <dd>

<span data-ttu-id="4bd51-158">Un servizio è in esecuzione con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="4bd51-158">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="4bd51-159">**20**</span><span class="sxs-lookup"><span data-stu-id="4bd51-159">**20**</span></span>
</dt> <dd>

<span data-ttu-id="4bd51-160">Il nome del servizio contiene caratteri non validi.</span><span class="sxs-lookup"><span data-stu-id="4bd51-160">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="4bd51-161">**21**</span><span class="sxs-lookup"><span data-stu-id="4bd51-161">**21**</span></span>
</dt> <dd>

<span data-ttu-id="4bd51-162">Al servizio sono stati passati parametri non validi.</span><span class="sxs-lookup"><span data-stu-id="4bd51-162">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="4bd51-163">**22**</span><span class="sxs-lookup"><span data-stu-id="4bd51-163">**22**</span></span>
</dt> <dd>

<span data-ttu-id="4bd51-164">L'account con cui viene eseguito il servizio non è valido o non dispone delle autorizzazioni per eseguire il servizio.</span><span class="sxs-lookup"><span data-stu-id="4bd51-164">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="4bd51-165">**23**</span><span class="sxs-lookup"><span data-stu-id="4bd51-165">**23**</span></span>
</dt> <dd>

<span data-ttu-id="4bd51-166">Il servizio esiste già nel database dei servizi disponibili dal sistema.</span><span class="sxs-lookup"><span data-stu-id="4bd51-166">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="4bd51-167">**24**</span><span class="sxs-lookup"><span data-stu-id="4bd51-167">**24**</span></span>
</dt> <dd>

<span data-ttu-id="4bd51-168">Il servizio è attualmente sospeso nel sistema.</span><span class="sxs-lookup"><span data-stu-id="4bd51-168">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4bd51-169">Commenti</span><span class="sxs-lookup"><span data-stu-id="4bd51-169">Remarks</span></span>

<span data-ttu-id="4bd51-170">[**L'istanza \_ di Win32 SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) rappresenta un tipo di dati [**SECURITY \_ DESCRIPTOR \_ CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) e contiene un elenco di controllo di accesso discrezionale (DACL) e un elenco di controllo di accesso [*di*](/windows/desktop/SecGloss/s-gly) sistema (SACL). [](/windows/desktop/SecGloss/d-gly)</span><span class="sxs-lookup"><span data-stu-id="4bd51-170">The [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance represents a [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) data type and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) and a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="4bd51-171">Per altre informazioni, vedere [Elenchi di controllo di accesso](/windows/desktop/SecAuthZ/access-control-lists).</span><span class="sxs-lookup"><span data-stu-id="4bd51-171">For more information, see [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span></span>

<span data-ttu-id="4bd51-172">Se **SeSecurityPrivilege** non viene concesso o abilitato quando si recupera un descrittore di sicurezza, nel descrittore di sicurezza restituito viene restituito solo l'elenco DACL.</span><span class="sxs-lookup"><span data-stu-id="4bd51-172">If the **SeSecurityPrivilege** is not granted or enabled when getting a security descriptor, then only the DACL is returned in the returned security descriptor.</span></span> <span data-ttu-id="4bd51-173">Per altre informazioni, vedere [**Costanti dei privilegi**](/windows/desktop/WmiSdk/privilege-constants) ed Esecuzione di operazioni con [privilegi](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="4bd51-173">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants) and [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

## <a name="examples"></a><span data-ttu-id="4bd51-174">Esempio</span><span class="sxs-lookup"><span data-stu-id="4bd51-174">Examples</span></span>

<span data-ttu-id="4bd51-175">Quando si recupera un descrittore di sicurezza in VBScript, assicurarsi di "Sicurezza" ed eseguire come Amministratore, come illustrato nel frammento di codice seguente.</span><span class="sxs-lookup"><span data-stu-id="4bd51-175">When retrieving a security descriptor in VBScript, be sure to "Security" and run as as Admin, as shown in the following code snippet.</span></span> <span data-ttu-id="4bd51-176">In caso contrario, il codice potrebbe generare un errore di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="4bd51-176">Otherwise, your code may throw a permissions error.</span></span>


```VB
Set objWMIService = GetObject("winmgmts:" _
  & "{impersonationLevel=impersonate, (Security)}!\\" & strComputer & "\root\cimv2")
```



<span data-ttu-id="4bd51-177">Analogamente, in VB.NET assicurarsi di impostare "EnablePrivileges = True" ed eseguire l'applicazione come amministratore.</span><span class="sxs-lookup"><span data-stu-id="4bd51-177">Similarly, in VB.NET, be sure to set "EnablePrivileges = True" and run the Application as Admin.</span></span>


```VB
Scope = New ManagementScope([String].Format("\\{0}\root\CIMV2", ComputerName), Nothing)
Scope.Options.EnablePrivileges = True
```



## <a name="requirements"></a><span data-ttu-id="4bd51-178">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4bd51-178">Requirements</span></span>



| <span data-ttu-id="4bd51-179">Requisito</span><span class="sxs-lookup"><span data-stu-id="4bd51-179">Requirement</span></span> | <span data-ttu-id="4bd51-180">Valore</span><span class="sxs-lookup"><span data-stu-id="4bd51-180">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4bd51-181">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4bd51-181">Minimum supported client</span></span><br/> | <span data-ttu-id="4bd51-182">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4bd51-182">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4bd51-183">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4bd51-183">Minimum supported server</span></span><br/> | <span data-ttu-id="4bd51-184">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4bd51-184">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4bd51-185">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4bd51-185">Namespace</span></span><br/>                | <span data-ttu-id="4bd51-186">TerminalServices \\ CIMv2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="4bd51-186">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="4bd51-187">MOF</span><span class="sxs-lookup"><span data-stu-id="4bd51-187">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4bd51-188"><dt>TSCfgWmi.mof</dt></span><span class="sxs-lookup"><span data-stu-id="4bd51-188"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="4bd51-189">DLL</span><span class="sxs-lookup"><span data-stu-id="4bd51-189">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4bd51-190"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4bd51-190"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4bd51-191">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4bd51-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bd51-192">**Servizio \_ Win32**</span><span class="sxs-lookup"><span data-stu-id="4bd51-192">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="4bd51-193">**Win32 \_ TerminalService**</span><span class="sxs-lookup"><span data-stu-id="4bd51-193">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="4bd51-194">**Costanti privilege**</span><span class="sxs-lookup"><span data-stu-id="4bd51-194">**Privilege Constants**</span></span>](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[<span data-ttu-id="4bd51-195">Oggetti descrittore di sicurezza WMI</span><span class="sxs-lookup"><span data-stu-id="4bd51-195">WMI Security Descriptor Objects</span></span>](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[<span data-ttu-id="4bd51-196">Modifica della sicurezza dell'accesso per gli oggetti a protezione diretta</span><span class="sxs-lookup"><span data-stu-id="4bd51-196">Changing Access Security on Securable Objects</span></span>](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> <dt>

[<span data-ttu-id="4bd51-197">Controllo dell'account utente e WMI</span><span class="sxs-lookup"><span data-stu-id="4bd51-197">User Account Control and WMI</span></span>](/windows/desktop/WmiSdk/user-account-control-and-wmi)
</dt> </dl>

 

