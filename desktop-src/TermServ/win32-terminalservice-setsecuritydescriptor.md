---
title: Metodo SetSecurityDescriptor della classe Win32_Service (Servizi Desktop remoto)
description: "Metodo SetSecurityDescriptor della classe Win32_Service (Servizi Desktop remoto): scrive una versione aggiornata del descrittore di sicurezza che controlla l'accesso al servizio."
ms.assetid: 4F03B798-0912-4A0D-B31E-419662D5849B
ms.tgt_platform: multiple
keywords:
- scripting Strumentazione gestione Windows , sicurezza
- sicurezza Strumentazione gestione Windows , scripting
- Metodo SetSecurityDescriptor Servizi Desktop remoto
- Metodo SetSecurityDescriptor Servizi Desktop remoto , Win32_Service classe
- Win32_Service classe Servizi Desktop remoto, metodo SetSecurityDescriptor
topic_type:
- apiref
api_name:
- Win32_Service.SetSecurityDescriptor
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb2dd7e43041c05b1c294181f8bd01548ed76d87
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114494"
---
# <a name="setsecuritydescriptor-method-of-the-win32_service-class-remote-desktop-services"></a><span data-ttu-id="de8ee-108">Metodo SetSecurityDescriptor della classe Win32_Service (Servizi Desktop remoto)</span><span class="sxs-lookup"><span data-stu-id="de8ee-108">SetSecurityDescriptor method of the Win32_Service class (Remote Desktop Services)</span></span>

<span data-ttu-id="de8ee-109">Il **metodo SetSecurityDescriptor** scrive una versione aggiornata del descrittore di sicurezza che controlla l'accesso al servizio.</span><span class="sxs-lookup"><span data-stu-id="de8ee-109">The **SetSecurityDescriptor** method writes an updated version of the security descriptor that controls access to the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="de8ee-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="de8ee-110">Syntax</span></span>


```mof
uint32 SetSecurityDescriptor(
  [in] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a><span data-ttu-id="de8ee-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="de8ee-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de8ee-112">*Descrittore* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="de8ee-112">*Descriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de8ee-113">Descrittore di sicurezza associato al servizio.</span><span class="sxs-lookup"><span data-stu-id="de8ee-113">The security descriptor associated with the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de8ee-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="de8ee-114">Return value</span></span>

<span data-ttu-id="de8ee-115">Restituisce uno dei valori elencati nell'elenco seguente o un valore diverso per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="de8ee-115">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="de8ee-116">Per altri codici di errore, vedere [**Costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="de8ee-116">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="de8ee-117">Per i valori **HRESULT** generali, vedere [Codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="de8ee-117">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="de8ee-118">**0**</span><span class="sxs-lookup"><span data-stu-id="de8ee-118">**0**</span></span>
</dt> <dd>

<span data-ttu-id="de8ee-119">La richiesta è stata accettata.</span><span class="sxs-lookup"><span data-stu-id="de8ee-119">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="de8ee-120">**1**</span><span class="sxs-lookup"><span data-stu-id="de8ee-120">**1**</span></span>
</dt> <dd>

<span data-ttu-id="de8ee-121">La richiesta non è supportata.</span><span class="sxs-lookup"><span data-stu-id="de8ee-121">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="de8ee-122">**2**</span><span class="sxs-lookup"><span data-stu-id="de8ee-122">**2**</span></span>
</dt> <dd>

<span data-ttu-id="de8ee-123">L'utente non dispone dell'accesso necessario.</span><span class="sxs-lookup"><span data-stu-id="de8ee-123">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="de8ee-124">**3**</span><span class="sxs-lookup"><span data-stu-id="de8ee-124">**3**</span></span>
</dt> <dd>

<span data-ttu-id="de8ee-125">Impossibile arrestare il servizio perché altri servizi in esecuzione dipendono dal servizio.</span><span class="sxs-lookup"><span data-stu-id="de8ee-125">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="de8ee-126">**4**</span><span class="sxs-lookup"><span data-stu-id="de8ee-126">**4**</span></span>
</dt> <dd>

<span data-ttu-id="de8ee-127">Il codice di controllo richiesto non è valido o non è accettabile per il servizio.</span><span class="sxs-lookup"><span data-stu-id="de8ee-127">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="de8ee-128">**5**</span><span class="sxs-lookup"><span data-stu-id="de8ee-128">**5**</span></span>
</dt> <dd>

<span data-ttu-id="de8ee-129">Impossibile inviare il codice di controllo richiesto al servizio perché lo stato del servizio ([**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** ) è uguale a 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="de8ee-129">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="de8ee-130">**6**</span><span class="sxs-lookup"><span data-stu-id="de8ee-130">**6**</span></span>
</dt> <dd>

<span data-ttu-id="de8ee-131">Il servizio non è stato avviato.</span><span class="sxs-lookup"><span data-stu-id="de8ee-131">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="de8ee-132">**7**</span><span class="sxs-lookup"><span data-stu-id="de8ee-132">**7**</span></span>
</dt> <dd>

<span data-ttu-id="de8ee-133">Il servizio non ha risposto in tempo utile alla richiesta di avvio.</span><span class="sxs-lookup"><span data-stu-id="de8ee-133">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="de8ee-134">**8**</span><span class="sxs-lookup"><span data-stu-id="de8ee-134">**8**</span></span>
</dt> <dd>

<span data-ttu-id="de8ee-135">Errore sconosciuto durante l'avvio del servizio.</span><span class="sxs-lookup"><span data-stu-id="de8ee-135">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="de8ee-136">**9**</span><span class="sxs-lookup"><span data-stu-id="de8ee-136">**9**</span></span>
</dt> <dd>

<span data-ttu-id="de8ee-137">Impossibile trovare il percorso della directory del file eseguibile del servizio.</span><span class="sxs-lookup"><span data-stu-id="de8ee-137">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="de8ee-138">**10**</span><span class="sxs-lookup"><span data-stu-id="de8ee-138">**10**</span></span>
</dt> <dd>

<span data-ttu-id="de8ee-139">Il servizio è già in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="de8ee-139">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="de8ee-140">**11**</span><span class="sxs-lookup"><span data-stu-id="de8ee-140">**11**</span></span>
</dt> <dd>

<span data-ttu-id="de8ee-141">Il database a cui aggiungere il nuovo servizio è bloccato.</span><span class="sxs-lookup"><span data-stu-id="de8ee-141">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="de8ee-142">**12**</span><span class="sxs-lookup"><span data-stu-id="de8ee-142">**12**</span></span>
</dt> <dd>

<span data-ttu-id="de8ee-143">Una dipendenza su cui si basa questo servizio è stata rimossa dal sistema.</span><span class="sxs-lookup"><span data-stu-id="de8ee-143">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="de8ee-144">**13**</span><span class="sxs-lookup"><span data-stu-id="de8ee-144">**13**</span></span>
</dt> <dd>

<span data-ttu-id="de8ee-145">Impossibile trovare un servizio dipendente necessario.</span><span class="sxs-lookup"><span data-stu-id="de8ee-145">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="de8ee-146">**14**</span><span class="sxs-lookup"><span data-stu-id="de8ee-146">**14**</span></span>
</dt> <dd>

<span data-ttu-id="de8ee-147">Il servizio è stato disabilitato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="de8ee-147">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="de8ee-148">**15**</span><span class="sxs-lookup"><span data-stu-id="de8ee-148">**15**</span></span>
</dt> <dd>

<span data-ttu-id="de8ee-149">Il servizio non dispone delle credenziali di autenticazione corrette per l'esecuzione nel sistema.</span><span class="sxs-lookup"><span data-stu-id="de8ee-149">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="de8ee-150">**16**</span><span class="sxs-lookup"><span data-stu-id="de8ee-150">**16**</span></span>
</dt> <dd>

<span data-ttu-id="de8ee-151">Questo servizio viene rimosso dal sistema.</span><span class="sxs-lookup"><span data-stu-id="de8ee-151">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="de8ee-152">**17**</span><span class="sxs-lookup"><span data-stu-id="de8ee-152">**17**</span></span>
</dt> <dd>

<span data-ttu-id="de8ee-153">Il servizio non ha thread di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="de8ee-153">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="de8ee-154">**18**</span><span class="sxs-lookup"><span data-stu-id="de8ee-154">**18**</span></span>
</dt> <dd>

<span data-ttu-id="de8ee-155">Il servizio ha dipendenze circolari all'avvio.</span><span class="sxs-lookup"><span data-stu-id="de8ee-155">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="de8ee-156">**19**</span><span class="sxs-lookup"><span data-stu-id="de8ee-156">**19**</span></span>
</dt> <dd>

<span data-ttu-id="de8ee-157">Un servizio è in esecuzione con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="de8ee-157">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="de8ee-158">**20**</span><span class="sxs-lookup"><span data-stu-id="de8ee-158">**20**</span></span>
</dt> <dd>

<span data-ttu-id="de8ee-159">Il nome del servizio contiene caratteri non validi.</span><span class="sxs-lookup"><span data-stu-id="de8ee-159">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="de8ee-160">**21**</span><span class="sxs-lookup"><span data-stu-id="de8ee-160">**21**</span></span>
</dt> <dd>

<span data-ttu-id="de8ee-161">Al servizio sono stati passati parametri non validi.</span><span class="sxs-lookup"><span data-stu-id="de8ee-161">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="de8ee-162">**22**</span><span class="sxs-lookup"><span data-stu-id="de8ee-162">**22**</span></span>
</dt> <dd>

<span data-ttu-id="de8ee-163">L'account con cui viene eseguito il servizio non è valido o non dispone delle autorizzazioni per eseguire il servizio.</span><span class="sxs-lookup"><span data-stu-id="de8ee-163">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="de8ee-164">**23**</span><span class="sxs-lookup"><span data-stu-id="de8ee-164">**23**</span></span>
</dt> <dd>

<span data-ttu-id="de8ee-165">Il servizio esiste già nel database dei servizi disponibili dal sistema.</span><span class="sxs-lookup"><span data-stu-id="de8ee-165">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="de8ee-166">**24**</span><span class="sxs-lookup"><span data-stu-id="de8ee-166">**24**</span></span>
</dt> <dd>

<span data-ttu-id="de8ee-167">Il servizio è attualmente sospeso nel sistema.</span><span class="sxs-lookup"><span data-stu-id="de8ee-167">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="de8ee-168">Commenti</span><span class="sxs-lookup"><span data-stu-id="de8ee-168">Remarks</span></span>

<span data-ttu-id="de8ee-169">[**L'istanza \_ di Win32 SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) rappresenta un tipo di dati [**SECURITY \_ DESCRIPTOR \_ CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) e contiene un elenco di controllo di accesso discrezionale (DACL) e un elenco di controllo di accesso [*di*](/windows/desktop/SecGloss/s-gly) sistema (SACL). [](/windows/desktop/SecGloss/d-gly)</span><span class="sxs-lookup"><span data-stu-id="de8ee-169">The [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance represents a [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) data type and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) and a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="de8ee-170">Per altre informazioni, vedere [Elenchi di controllo di accesso](/windows/desktop/SecAuthZ/access-control-lists).</span><span class="sxs-lookup"><span data-stu-id="de8ee-170">For more information, see [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span></span>

<span data-ttu-id="de8ee-171">Se **SeSecurityPrivilege** non viene concesso o abilitato quando si recupera un descrittore di sicurezza, nel descrittore di sicurezza restituito viene restituito solo l'elenco DACL.</span><span class="sxs-lookup"><span data-stu-id="de8ee-171">If the **SeSecurityPrivilege** is not granted or enabled when getting a security descriptor, then only the DACL is returned in the returned security descriptor.</span></span> <span data-ttu-id="de8ee-172">Per altre informazioni, vedere [**Costanti dei privilegi**](/windows/desktop/WmiSdk/privilege-constants) ed Esecuzione di operazioni con [privilegi](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="de8ee-172">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants) and [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

<span data-ttu-id="de8ee-173">È possibile aggiornare sia l'elenco DACL che l'elenco SACL nell'istanza [**\_ di Win32 SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) quando si chiama questo metodo, ma è anche possibile aggiornare solo l'elenco DACL o solo l'elenco SACL.</span><span class="sxs-lookup"><span data-stu-id="de8ee-173">You can update both the DACL and the SACL in the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance when calling this method, but you also can update only the DACL or only the SACL.</span></span>

<span data-ttu-id="de8ee-174">I valori seguenti in [**SECURITY \_ DESCRIPTOR \_ CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) determinano se l'elenco DACL, il SACL o entrambi vengono aggiornati.</span><span class="sxs-lookup"><span data-stu-id="de8ee-174">The following values in [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) determine whether the DACL, the SACL, or both are updated.</span></span>

-   <span data-ttu-id="de8ee-175">**SE \_ DACL \_ PRESENT**</span><span class="sxs-lookup"><span data-stu-id="de8ee-175">**SE\_DACL\_PRESENT**</span></span>

    <span data-ttu-id="de8ee-176">Indica che l'elenco DACL deve essere aggiornato.</span><span class="sxs-lookup"><span data-stu-id="de8ee-176">Indicates that the DACL should be updated.</span></span> <span data-ttu-id="de8ee-177">Se non è impostato, WMI mantiene il valore originale dell'elenco DACL.</span><span class="sxs-lookup"><span data-stu-id="de8ee-177">If this is not set, then WMI preserves the original value of the DACL.</span></span>

-   <span data-ttu-id="de8ee-178">**SE \_ SACL \_ PRESENT**</span><span class="sxs-lookup"><span data-stu-id="de8ee-178">**SE\_SACL\_PRESENT**</span></span>

    <span data-ttu-id="de8ee-179">Indica che l'elenco di controllo di accesso condiviso deve essere aggiornato.</span><span class="sxs-lookup"><span data-stu-id="de8ee-179">Indicates that the SACL should be updated.</span></span> <span data-ttu-id="de8ee-180">Se non è impostato, WMI mantiene il valore originale dell'elenco di controllo di accesso condiviso.</span><span class="sxs-lookup"><span data-stu-id="de8ee-180">If this is not set, then WMI preserves the original value of the SACL.</span></span> <span data-ttu-id="de8ee-181">Per aggiornare il SACL, l'account deve avere il **privilegio SeSecurityPrivilege** abilitato.</span><span class="sxs-lookup"><span data-stu-id="de8ee-181">To update the SACL, the account must have the **SeSecurityPrivilege** privilege enabled.</span></span> <span data-ttu-id="de8ee-182">Per gli script, il nome del privilegio è **SeSecurityPrivilege**.</span><span class="sxs-lookup"><span data-stu-id="de8ee-182">For scripting, the privilege name is **SeSecurityPrivilege**.</span></span> <span data-ttu-id="de8ee-183">Per altre informazioni, vedere [**Costanti dei privilegi**](/windows/desktop/WmiSdk/privilege-constants).</span><span class="sxs-lookup"><span data-stu-id="de8ee-183">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants).</span></span>

<span data-ttu-id="de8ee-184">Se le proprietà Trustee e Owner trustee del gruppo non sono **NULL,** vengono aggiornate.</span><span class="sxs-lookup"><span data-stu-id="de8ee-184">If the Group trustee and the Owner trustee properties are not **NULL**, then they are updated.</span></span> <span data-ttu-id="de8ee-185">In caso contrario, WMI mantiene i valori originali.</span><span class="sxs-lookup"><span data-stu-id="de8ee-185">Otherwise, WMI preserves the original values.</span></span> <span data-ttu-id="de8ee-186">Per altre informazioni, vedere [Oggetti descrittori di sicurezza WMI](/windows/desktop/WmiSdk/wmi-security-descriptor-objects).</span><span class="sxs-lookup"><span data-stu-id="de8ee-186">For more information, see [WMI Security Descriptor Objects](/windows/desktop/WmiSdk/wmi-security-descriptor-objects).</span></span>

<span data-ttu-id="de8ee-187">Quando un nuovo SACL è **NULL** in una chiamata a questo metodo, il SACL del descrittore di sicurezza nell'oggetto a protezione diretta di destinazione rimane invariato.</span><span class="sxs-lookup"><span data-stu-id="de8ee-187">When a new SACL is **NULL** in a call this method, then the security descriptor SACL on the target securable object is left unchanged.</span></span>

## <a name="requirements"></a><span data-ttu-id="de8ee-188">Requisiti</span><span class="sxs-lookup"><span data-stu-id="de8ee-188">Requirements</span></span>



| <span data-ttu-id="de8ee-189">Requisito</span><span class="sxs-lookup"><span data-stu-id="de8ee-189">Requirement</span></span> | <span data-ttu-id="de8ee-190">Valore</span><span class="sxs-lookup"><span data-stu-id="de8ee-190">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="de8ee-191">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="de8ee-191">Minimum supported client</span></span><br/> | <span data-ttu-id="de8ee-192">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="de8ee-192">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="de8ee-193">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="de8ee-193">Minimum supported server</span></span><br/> | <span data-ttu-id="de8ee-194">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="de8ee-194">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="de8ee-195">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="de8ee-195">Namespace</span></span><br/>                | <span data-ttu-id="de8ee-196">TerminalServices \\ CIMv2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="de8ee-196">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="de8ee-197">MOF</span><span class="sxs-lookup"><span data-stu-id="de8ee-197">MOF</span></span><br/>                      | <dl> <span data-ttu-id="de8ee-198"><dt>TSCfgWmi.mof</dt></span><span class="sxs-lookup"><span data-stu-id="de8ee-198"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="de8ee-199">DLL</span><span class="sxs-lookup"><span data-stu-id="de8ee-199">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de8ee-200"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="de8ee-200"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de8ee-201">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="de8ee-201">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de8ee-202">**Servizio \_ Win32**</span><span class="sxs-lookup"><span data-stu-id="de8ee-202">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="de8ee-203">**Win32 \_ TerminalService**</span><span class="sxs-lookup"><span data-stu-id="de8ee-203">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="de8ee-204">**Costanti dei privilegi**</span><span class="sxs-lookup"><span data-stu-id="de8ee-204">**Privilege Constants**</span></span>](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[<span data-ttu-id="de8ee-205">Oggetti descrittori di sicurezza WMI</span><span class="sxs-lookup"><span data-stu-id="de8ee-205">WMI Security Descriptor Objects</span></span>](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[<span data-ttu-id="de8ee-206">Modifica della sicurezza degli accessi per gli oggetti a protezione diretta</span><span class="sxs-lookup"><span data-stu-id="de8ee-206">Changing Access Security on Securable Objects</span></span>](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> <dt>

[<span data-ttu-id="de8ee-207">Controllo dell'account utente e WMI</span><span class="sxs-lookup"><span data-stu-id="de8ee-207">User Account Control and WMI</span></span>](/windows/desktop/WmiSdk/user-account-control-and-wmi)
</dt> </dl>

 

