---
title: Metodo SetSecurityDescriptor della classe Win32_Service (Servizi Desktop remoto)
description: Scrive una versione aggiornata del descrittore di sicurezza che controlla l'accesso al servizio.
ms.assetid: 4F03B798-0912-4A0D-B31E-419662D5849B
ms.tgt_platform: multiple
keywords:
- Strumentazione gestione Windows di script, sicurezza
- Strumentazione gestione Windows di sicurezza, Scripting
- Servizi Desktop remoto del metodo SetSecurityDescriptor
- Metodo SetSecurityDescriptor Servizi Desktop remoto, classe Win32_Service
- Classe Win32_Service Servizi Desktop remoto, metodo SetSecurityDescriptor
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
ms.openlocfilehash: 19a21f9730b4c1c0ab7b3ccf662ddb2d95da2ee2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743487"
---
# <a name="setsecuritydescriptor-method-of-the-win32_service-class-remote-desktop-services"></a><span data-ttu-id="674cc-108">Metodo SetSecurityDescriptor della classe Win32_Service (Servizi Desktop remoto)</span><span class="sxs-lookup"><span data-stu-id="674cc-108">SetSecurityDescriptor method of the Win32_Service class (Remote Desktop Services)</span></span>

<span data-ttu-id="674cc-109">Il metodo **SetSecurityDescriptor** scrive una versione aggiornata del descrittore di sicurezza che controlla l'accesso al servizio.</span><span class="sxs-lookup"><span data-stu-id="674cc-109">The **SetSecurityDescriptor** method writes an updated version of the security descriptor that controls access to the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="674cc-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="674cc-110">Syntax</span></span>


```mof
uint32 SetSecurityDescriptor(
  [in] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a><span data-ttu-id="674cc-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="674cc-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="674cc-112">*Descrittore* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="674cc-112">*Descriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="674cc-113">Descrittore di sicurezza associato al servizio.</span><span class="sxs-lookup"><span data-stu-id="674cc-113">The security descriptor associated with the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="674cc-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="674cc-114">Return value</span></span>

<span data-ttu-id="674cc-115">Restituisce uno dei valori elencati nell'elenco seguente o un valore diverso per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="674cc-115">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="674cc-116">Per ulteriori codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="674cc-116">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="674cc-117">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="674cc-117">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="674cc-118">**0**</span><span class="sxs-lookup"><span data-stu-id="674cc-118">**0**</span></span>
</dt> <dd>

<span data-ttu-id="674cc-119">La richiesta è stata accettata.</span><span class="sxs-lookup"><span data-stu-id="674cc-119">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="674cc-120">**1**</span><span class="sxs-lookup"><span data-stu-id="674cc-120">**1**</span></span>
</dt> <dd>

<span data-ttu-id="674cc-121">La richiesta non è supportata.</span><span class="sxs-lookup"><span data-stu-id="674cc-121">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="674cc-122">**2**</span><span class="sxs-lookup"><span data-stu-id="674cc-122">**2**</span></span>
</dt> <dd>

<span data-ttu-id="674cc-123">L'utente non dispone dell'accesso necessario.</span><span class="sxs-lookup"><span data-stu-id="674cc-123">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="674cc-124">**3**</span><span class="sxs-lookup"><span data-stu-id="674cc-124">**3**</span></span>
</dt> <dd>

<span data-ttu-id="674cc-125">Impossibile arrestare il servizio perché altri servizi in esecuzione dipendono dal servizio.</span><span class="sxs-lookup"><span data-stu-id="674cc-125">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="674cc-126">**4**</span><span class="sxs-lookup"><span data-stu-id="674cc-126">**4**</span></span>
</dt> <dd>

<span data-ttu-id="674cc-127">Il codice di controllo richiesto non è valido o non è accettabile per il servizio.</span><span class="sxs-lookup"><span data-stu-id="674cc-127">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="674cc-128">**5**</span><span class="sxs-lookup"><span data-stu-id="674cc-128">**5**</span></span>
</dt> <dd>

<span data-ttu-id="674cc-129">Impossibile inviare il codice di controllo richiesto al servizio perché lo stato del servizio ([**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**Proprietà state** ) è uguale a 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="674cc-129">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="674cc-130">**6**</span><span class="sxs-lookup"><span data-stu-id="674cc-130">**6**</span></span>
</dt> <dd>

<span data-ttu-id="674cc-131">Il servizio non è stato avviato.</span><span class="sxs-lookup"><span data-stu-id="674cc-131">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="674cc-132">**7**</span><span class="sxs-lookup"><span data-stu-id="674cc-132">**7**</span></span>
</dt> <dd>

<span data-ttu-id="674cc-133">Il servizio non ha risposto in tempo utile alla richiesta di avvio.</span><span class="sxs-lookup"><span data-stu-id="674cc-133">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="674cc-134">**8**</span><span class="sxs-lookup"><span data-stu-id="674cc-134">**8**</span></span>
</dt> <dd>

<span data-ttu-id="674cc-135">Errore sconosciuto durante l'avvio del servizio.</span><span class="sxs-lookup"><span data-stu-id="674cc-135">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="674cc-136">**9**</span><span class="sxs-lookup"><span data-stu-id="674cc-136">**9**</span></span>
</dt> <dd>

<span data-ttu-id="674cc-137">Impossibile trovare il percorso di directory del file eseguibile del servizio.</span><span class="sxs-lookup"><span data-stu-id="674cc-137">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="674cc-138">**10**</span><span class="sxs-lookup"><span data-stu-id="674cc-138">**10**</span></span>
</dt> <dd>

<span data-ttu-id="674cc-139">Il servizio è già in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="674cc-139">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="674cc-140">**11**</span><span class="sxs-lookup"><span data-stu-id="674cc-140">**11**</span></span>
</dt> <dd>

<span data-ttu-id="674cc-141">Il database a cui aggiungere il nuovo servizio è bloccato.</span><span class="sxs-lookup"><span data-stu-id="674cc-141">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="674cc-142">**12**</span><span class="sxs-lookup"><span data-stu-id="674cc-142">**12**</span></span>
</dt> <dd>

<span data-ttu-id="674cc-143">Una dipendenza su cui si basa questo servizio è stata rimossa dal sistema.</span><span class="sxs-lookup"><span data-stu-id="674cc-143">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="674cc-144">**13**</span><span class="sxs-lookup"><span data-stu-id="674cc-144">**13**</span></span>
</dt> <dd>

<span data-ttu-id="674cc-145">Impossibile trovare un servizio dipendente necessario.</span><span class="sxs-lookup"><span data-stu-id="674cc-145">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="674cc-146">**14**</span><span class="sxs-lookup"><span data-stu-id="674cc-146">**14**</span></span>
</dt> <dd>

<span data-ttu-id="674cc-147">Il servizio è stato disabilitato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="674cc-147">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="674cc-148">**15**</span><span class="sxs-lookup"><span data-stu-id="674cc-148">**15**</span></span>
</dt> <dd>

<span data-ttu-id="674cc-149">Il servizio non dispone delle credenziali di autenticazione corrette per l'esecuzione nel sistema.</span><span class="sxs-lookup"><span data-stu-id="674cc-149">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="674cc-150">**16**</span><span class="sxs-lookup"><span data-stu-id="674cc-150">**16**</span></span>
</dt> <dd>

<span data-ttu-id="674cc-151">Questo servizio verrà rimosso dal sistema.</span><span class="sxs-lookup"><span data-stu-id="674cc-151">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="674cc-152">**17**</span><span class="sxs-lookup"><span data-stu-id="674cc-152">**17**</span></span>
</dt> <dd>

<span data-ttu-id="674cc-153">Il servizio non dispone di un thread di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="674cc-153">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="674cc-154">**18**</span><span class="sxs-lookup"><span data-stu-id="674cc-154">**18**</span></span>
</dt> <dd>

<span data-ttu-id="674cc-155">Il servizio ha dipendenze circolari all'avvio.</span><span class="sxs-lookup"><span data-stu-id="674cc-155">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="674cc-156">**19**</span><span class="sxs-lookup"><span data-stu-id="674cc-156">**19**</span></span>
</dt> <dd>

<span data-ttu-id="674cc-157">Un servizio è in esecuzione con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="674cc-157">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="674cc-158">**20**</span><span class="sxs-lookup"><span data-stu-id="674cc-158">**20**</span></span>
</dt> <dd>

<span data-ttu-id="674cc-159">Il nome del servizio contiene caratteri non validi.</span><span class="sxs-lookup"><span data-stu-id="674cc-159">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="674cc-160">**21**</span><span class="sxs-lookup"><span data-stu-id="674cc-160">**21**</span></span>
</dt> <dd>

<span data-ttu-id="674cc-161">Sono stati passati parametri non validi al servizio.</span><span class="sxs-lookup"><span data-stu-id="674cc-161">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="674cc-162">**22**</span><span class="sxs-lookup"><span data-stu-id="674cc-162">**22**</span></span>
</dt> <dd>

<span data-ttu-id="674cc-163">L'account con cui viene eseguito il servizio non è valido o non dispone delle autorizzazioni necessarie per eseguire il servizio.</span><span class="sxs-lookup"><span data-stu-id="674cc-163">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="674cc-164">**23**</span><span class="sxs-lookup"><span data-stu-id="674cc-164">**23**</span></span>
</dt> <dd>

<span data-ttu-id="674cc-165">Il servizio esiste già nel database dei servizi disponibili dal sistema.</span><span class="sxs-lookup"><span data-stu-id="674cc-165">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="674cc-166">**24**</span><span class="sxs-lookup"><span data-stu-id="674cc-166">**24**</span></span>
</dt> <dd>

<span data-ttu-id="674cc-167">Il servizio è attualmente sospeso nel sistema.</span><span class="sxs-lookup"><span data-stu-id="674cc-167">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="674cc-168">Commenti</span><span class="sxs-lookup"><span data-stu-id="674cc-168">Remarks</span></span>

<span data-ttu-id="674cc-169">L' [**istanza Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) rappresenta un tipo di dati di [**\_ \_ controllo del descrittore di sicurezza**](/windows/desktop/SecAuthZ/security-descriptor-control) e contiene un elenco di controllo di [*accesso discrezionale*](/windows/desktop/SecGloss/d-gly) (DACL) e un elenco di controllo di accesso di [*sistema*](/windows/desktop/SecGloss/s-gly) (SACL).</span><span class="sxs-lookup"><span data-stu-id="674cc-169">The [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance represents a [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) data type and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) and a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="674cc-170">Per altre informazioni, vedere [elenchi di controllo di accesso](/windows/desktop/SecAuthZ/access-control-lists).</span><span class="sxs-lookup"><span data-stu-id="674cc-170">For more information, see [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span></span>

<span data-ttu-id="674cc-171">Se **SeSecurityPrivilege** non viene concesso o abilitato quando si recupera un descrittore di sicurezza, nel descrittore di sicurezza restituito viene restituito solo l'elenco DACL.</span><span class="sxs-lookup"><span data-stu-id="674cc-171">If the **SeSecurityPrivilege** is not granted or enabled when getting a security descriptor, then only the DACL is returned in the returned security descriptor.</span></span> <span data-ttu-id="674cc-172">Per altre informazioni, vedere [**costanti Privilege**](/windows/desktop/WmiSdk/privilege-constants) ed [esecuzione di operazioni con privilegi](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="674cc-172">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants) and [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

<span data-ttu-id="674cc-173">È possibile aggiornare sia l'elenco DACL che l'elenco SACL nell'istanza [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) quando si chiama questo metodo, ma è anche possibile aggiornare solo l'elenco DACL o solo il SACL.</span><span class="sxs-lookup"><span data-stu-id="674cc-173">You can update both the DACL and the SACL in the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance when calling this method, but you also can update only the DACL or only the SACL.</span></span>

<span data-ttu-id="674cc-174">I valori seguenti nel [**\_ \_ controllo descrittore di sicurezza**](/windows/desktop/SecAuthZ/security-descriptor-control) determinano se l'elenco DACL, il SACL o entrambi vengono aggiornati.</span><span class="sxs-lookup"><span data-stu-id="674cc-174">The following values in [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) determine whether the DACL, the SACL, or both are updated.</span></span>

-   <span data-ttu-id="674cc-175">**\_elenco DACL se \_ presente**</span><span class="sxs-lookup"><span data-stu-id="674cc-175">**SE\_DACL\_PRESENT**</span></span>

    <span data-ttu-id="674cc-176">Indica che l'elenco DACL deve essere aggiornato.</span><span class="sxs-lookup"><span data-stu-id="674cc-176">Indicates that the DACL should be updated.</span></span> <span data-ttu-id="674cc-177">Se non è impostato, WMI conserva il valore originale del DACL.</span><span class="sxs-lookup"><span data-stu-id="674cc-177">If this is not set, then WMI preserves the original value of the DACL.</span></span>

-   <span data-ttu-id="674cc-178">**\_SACL se \_ presente**</span><span class="sxs-lookup"><span data-stu-id="674cc-178">**SE\_SACL\_PRESENT**</span></span>

    <span data-ttu-id="674cc-179">Indica che il SACL deve essere aggiornato.</span><span class="sxs-lookup"><span data-stu-id="674cc-179">Indicates that the SACL should be updated.</span></span> <span data-ttu-id="674cc-180">Se non è impostato, WMI conserva il valore originale del SACL.</span><span class="sxs-lookup"><span data-stu-id="674cc-180">If this is not set, then WMI preserves the original value of the SACL.</span></span> <span data-ttu-id="674cc-181">Per aggiornare il SACL, per l'account deve essere abilitato il privilegio **SeSecurityPrivilege** .</span><span class="sxs-lookup"><span data-stu-id="674cc-181">To update the SACL, the account must have the **SeSecurityPrivilege** privilege enabled.</span></span> <span data-ttu-id="674cc-182">Per gli script, il nome del privilegio è **SeSecurityPrivilege**.</span><span class="sxs-lookup"><span data-stu-id="674cc-182">For scripting, the privilege name is **SeSecurityPrivilege**.</span></span> <span data-ttu-id="674cc-183">Per altre informazioni, vedere [**costanti Privilege**](/windows/desktop/WmiSdk/privilege-constants).</span><span class="sxs-lookup"><span data-stu-id="674cc-183">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants).</span></span>

<span data-ttu-id="674cc-184">Se il Trustee del gruppo e le proprietà del trustee del proprietario non sono **null**, verranno aggiornati.</span><span class="sxs-lookup"><span data-stu-id="674cc-184">If the Group trustee and the Owner trustee properties are not **NULL**, then they are updated.</span></span> <span data-ttu-id="674cc-185">In caso contrario, WMI conserva i valori originali.</span><span class="sxs-lookup"><span data-stu-id="674cc-185">Otherwise, WMI preserves the original values.</span></span> <span data-ttu-id="674cc-186">Per ulteriori informazioni, vedere [oggetti del descrittore di sicurezza WMI](/windows/desktop/WmiSdk/wmi-security-descriptor-objects).</span><span class="sxs-lookup"><span data-stu-id="674cc-186">For more information, see [WMI Security Descriptor Objects](/windows/desktop/WmiSdk/wmi-security-descriptor-objects).</span></span>

<span data-ttu-id="674cc-187">Quando un nuovo SACL è **null** in una chiamata a questo metodo, il SACL del descrittore di sicurezza nell'oggetto a protezione diretta di destinazione viene lasciato invariato.</span><span class="sxs-lookup"><span data-stu-id="674cc-187">When a new SACL is **NULL** in a call this method, then the security descriptor SACL on the target securable object is left unchanged.</span></span>

## <a name="requirements"></a><span data-ttu-id="674cc-188">Requisiti</span><span class="sxs-lookup"><span data-stu-id="674cc-188">Requirements</span></span>



| <span data-ttu-id="674cc-189">Requisito</span><span class="sxs-lookup"><span data-stu-id="674cc-189">Requirement</span></span> | <span data-ttu-id="674cc-190">Valore</span><span class="sxs-lookup"><span data-stu-id="674cc-190">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="674cc-191">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="674cc-191">Minimum supported client</span></span><br/> | <span data-ttu-id="674cc-192">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="674cc-192">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="674cc-193">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="674cc-193">Minimum supported server</span></span><br/> | <span data-ttu-id="674cc-194">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="674cc-194">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="674cc-195">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="674cc-195">Namespace</span></span><br/>                | <span data-ttu-id="674cc-196">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="674cc-196">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="674cc-197">MOF</span><span class="sxs-lookup"><span data-stu-id="674cc-197">MOF</span></span><br/>                      | <dl> <span data-ttu-id="674cc-198"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="674cc-198"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="674cc-199">DLL</span><span class="sxs-lookup"><span data-stu-id="674cc-199">DLL</span></span><br/>                      | <dl> <span data-ttu-id="674cc-200"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="674cc-200"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="674cc-201">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="674cc-201">See also</span></span>

<dl> <dt>

[<span data-ttu-id="674cc-202">**\_Servizio Win32**</span><span class="sxs-lookup"><span data-stu-id="674cc-202">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="674cc-203">**\_TerminalService Win32**</span><span class="sxs-lookup"><span data-stu-id="674cc-203">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="674cc-204">**Costanti Privilege**</span><span class="sxs-lookup"><span data-stu-id="674cc-204">**Privilege Constants**</span></span>](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[<span data-ttu-id="674cc-205">Oggetti descrittore di sicurezza WMI</span><span class="sxs-lookup"><span data-stu-id="674cc-205">WMI Security Descriptor Objects</span></span>](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[<span data-ttu-id="674cc-206">Modifica della sicurezza di accesso per gli oggetti a protezione diretta</span><span class="sxs-lookup"><span data-stu-id="674cc-206">Changing Access Security on Securable Objects</span></span>](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> <dt>

[<span data-ttu-id="674cc-207">Controllo dell'account utente e WMI</span><span class="sxs-lookup"><span data-stu-id="674cc-207">User Account Control and WMI</span></span>](/windows/desktop/WmiSdk/user-account-control-and-wmi)
</dt> </dl>

 

