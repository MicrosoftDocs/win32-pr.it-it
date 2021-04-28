---
description: "Metodo GetSecurityDescriptor della classe Win32_Service (provider WMI CIMWin32): restituisce il descrittore di sicurezza che controlla l'accesso al servizio."
ms.assetid: 99c8346e-e8d6-4f3c-bbdc-437dcf852b2a
ms.tgt_platform: multiple
title: Metodo GetSecurityDescriptor della classe Win32_Service (provider WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.GetSecurityDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 44c19f22cf57a811a7caebfbcc9bf4202c8d2ad7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096989"
---
# <a name="getsecuritydescriptor-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="f987b-103">Metodo GetSecurityDescriptor della classe Win32_Service (provider WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="f987b-103">GetSecurityDescriptor method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="f987b-104">Il **metodo GetSecurityDescriptor** restituisce il descrittore di sicurezza che controlla l'accesso al servizio.</span><span class="sxs-lookup"><span data-stu-id="f987b-104">The **GetSecurityDescriptor** method returns the security descriptor that controls access to the service.</span></span> <span data-ttu-id="f987b-105">Il descrittore viene restituito come istanza di [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span><span class="sxs-lookup"><span data-stu-id="f987b-105">The descriptor is returned as an instance of [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span>

## <a name="syntax"></a><span data-ttu-id="f987b-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f987b-106">Syntax</span></span>


```mof
uint32 GetSecurityDescriptor(
  [out] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a><span data-ttu-id="f987b-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="f987b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f987b-108">*Descrittore* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="f987b-108">*Descriptor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f987b-109">Descrittore di sicurezza associato al servizio.</span><span class="sxs-lookup"><span data-stu-id="f987b-109">The security descriptor associated with the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f987b-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f987b-110">Return value</span></span>

<span data-ttu-id="f987b-111">Restituisce uno dei valori elencati nell'elenco seguente o un valore diverso per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="f987b-111">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="f987b-112">Per altri codici di errore, vedere [**Costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="f987b-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="f987b-113">Per i valori **HRESULT** generali, vedere [Codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="f987b-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="f987b-114">**Success**</span><span class="sxs-lookup"><span data-stu-id="f987b-114">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="f987b-115">0</span><span class="sxs-lookup"><span data-stu-id="f987b-115">0</span></span>

<span data-ttu-id="f987b-116">La richiesta è stata accettata.</span><span class="sxs-lookup"><span data-stu-id="f987b-116">The request was accepted.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="f987b-117">1</span><span class="sxs-lookup"><span data-stu-id="f987b-117">1</span></span>

<span data-ttu-id="f987b-118">La richiesta non è supportata.</span><span class="sxs-lookup"><span data-stu-id="f987b-118">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="f987b-119">**Accesso negato**</span><span class="sxs-lookup"><span data-stu-id="f987b-119">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="f987b-120">2</span><span class="sxs-lookup"><span data-stu-id="f987b-120">2</span></span>

<span data-ttu-id="f987b-121">L'utente non dispone dell'accesso necessario.</span><span class="sxs-lookup"><span data-stu-id="f987b-121">The user did not have the necessary access.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="f987b-122">3</span><span class="sxs-lookup"><span data-stu-id="f987b-122">3</span></span>

<span data-ttu-id="f987b-123">Impossibile arrestare il servizio perché altri servizi in esecuzione dipendono dal servizio.</span><span class="sxs-lookup"><span data-stu-id="f987b-123">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="f987b-124">4</span><span class="sxs-lookup"><span data-stu-id="f987b-124">4</span></span>

<span data-ttu-id="f987b-125">Il codice di controllo richiesto non è valido o non è accettabile per il servizio.</span><span class="sxs-lookup"><span data-stu-id="f987b-125">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="f987b-126">5</span><span class="sxs-lookup"><span data-stu-id="f987b-126">5</span></span>

<span data-ttu-id="f987b-127">Impossibile inviare il codice di controllo richiesto al servizio perché lo stato del servizio ([**Win32 \_ BaseService**](win32-baseservice.md).**State** ) è uguale a 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="f987b-127">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="f987b-128">6</span><span class="sxs-lookup"><span data-stu-id="f987b-128">6</span></span>

<span data-ttu-id="f987b-129">Il servizio non è stato avviato.</span><span class="sxs-lookup"><span data-stu-id="f987b-129">The service has not been started.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="f987b-130">7</span><span class="sxs-lookup"><span data-stu-id="f987b-130">7</span></span>

<span data-ttu-id="f987b-131">Il servizio non ha risposto in tempo utile alla richiesta di avvio.</span><span class="sxs-lookup"><span data-stu-id="f987b-131">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="f987b-132">**Errore sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="f987b-132">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="f987b-133">8</span><span class="sxs-lookup"><span data-stu-id="f987b-133">8</span></span>

<span data-ttu-id="f987b-134">Errore sconosciuto durante l'avvio del servizio.</span><span class="sxs-lookup"><span data-stu-id="f987b-134">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="f987b-135">**Privilegio mancante**</span><span class="sxs-lookup"><span data-stu-id="f987b-135">**Privilege missing**</span></span>
</dt> <dd>

<span data-ttu-id="f987b-136">9</span><span class="sxs-lookup"><span data-stu-id="f987b-136">9</span></span>

<span data-ttu-id="f987b-137">Impossibile trovare il percorso della directory del file eseguibile del servizio.</span><span class="sxs-lookup"><span data-stu-id="f987b-137">The directory path to the service executable file was not found.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="f987b-138">10</span><span class="sxs-lookup"><span data-stu-id="f987b-138">10</span></span>

<span data-ttu-id="f987b-139">Il servizio è già in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="f987b-139">The service is already running.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="f987b-140">11</span><span class="sxs-lookup"><span data-stu-id="f987b-140">11</span></span>

<span data-ttu-id="f987b-141">Il database a cui aggiungere il nuovo servizio è bloccato.</span><span class="sxs-lookup"><span data-stu-id="f987b-141">The database to add a new service is locked.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="f987b-142">12</span><span class="sxs-lookup"><span data-stu-id="f987b-142">12</span></span>

<span data-ttu-id="f987b-143">Una dipendenza su cui si basa questo servizio è stata rimossa dal sistema.</span><span class="sxs-lookup"><span data-stu-id="f987b-143">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="f987b-144">13</span><span class="sxs-lookup"><span data-stu-id="f987b-144">13</span></span>

<span data-ttu-id="f987b-145">Impossibile trovare un servizio dipendente necessario.</span><span class="sxs-lookup"><span data-stu-id="f987b-145">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="f987b-146">14</span><span class="sxs-lookup"><span data-stu-id="f987b-146">14</span></span>

<span data-ttu-id="f987b-147">Il servizio è stato disabilitato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="f987b-147">The service has been disabled from the system.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="f987b-148">15</span><span class="sxs-lookup"><span data-stu-id="f987b-148">15</span></span>

<span data-ttu-id="f987b-149">Il servizio non dispone delle credenziali di autenticazione corrette per l'esecuzione nel sistema.</span><span class="sxs-lookup"><span data-stu-id="f987b-149">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="f987b-150">16</span><span class="sxs-lookup"><span data-stu-id="f987b-150">16</span></span>

<span data-ttu-id="f987b-151">Questo servizio viene rimosso dal sistema.</span><span class="sxs-lookup"><span data-stu-id="f987b-151">This service is being removed from the system.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="f987b-152">17</span><span class="sxs-lookup"><span data-stu-id="f987b-152">17</span></span>

<span data-ttu-id="f987b-153">Il servizio non ha thread di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="f987b-153">The service has no execution thread.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="f987b-154">18</span><span class="sxs-lookup"><span data-stu-id="f987b-154">18</span></span>

<span data-ttu-id="f987b-155">Il servizio ha dipendenze circolari all'avvio.</span><span class="sxs-lookup"><span data-stu-id="f987b-155">The service has circular dependencies when it starts.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="f987b-156">19</span><span class="sxs-lookup"><span data-stu-id="f987b-156">19</span></span>

<span data-ttu-id="f987b-157">Un servizio è in esecuzione con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="f987b-157">A service is running under the same name.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="f987b-158">20</span><span class="sxs-lookup"><span data-stu-id="f987b-158">20</span></span>

<span data-ttu-id="f987b-159">Il nome del servizio contiene caratteri non validi.</span><span class="sxs-lookup"><span data-stu-id="f987b-159">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="f987b-160">**Parametro non valido**</span><span class="sxs-lookup"><span data-stu-id="f987b-160">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="f987b-161">21</span><span class="sxs-lookup"><span data-stu-id="f987b-161">21</span></span>

<span data-ttu-id="f987b-162">Al servizio sono stati passati parametri non validi.</span><span class="sxs-lookup"><span data-stu-id="f987b-162">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="f987b-163">22</span><span class="sxs-lookup"><span data-stu-id="f987b-163">22</span></span>

<span data-ttu-id="f987b-164">L'account con cui viene eseguito il servizio non è valido o non dispone delle autorizzazioni per eseguire il servizio.</span><span class="sxs-lookup"><span data-stu-id="f987b-164">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="f987b-165">23</span><span class="sxs-lookup"><span data-stu-id="f987b-165">23</span></span>

<span data-ttu-id="f987b-166">Il servizio esiste già nel database dei servizi disponibili dal sistema.</span><span class="sxs-lookup"><span data-stu-id="f987b-166">The service exists in the database of services available from the system.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="f987b-167">24</span><span class="sxs-lookup"><span data-stu-id="f987b-167">24</span></span>

<span data-ttu-id="f987b-168">Il servizio è attualmente sospeso nel sistema.</span><span class="sxs-lookup"><span data-stu-id="f987b-168">The service is currently paused in the system.</span></span>

</dd> <dt>

<span data-ttu-id="f987b-169">**Altri**</span><span class="sxs-lookup"><span data-stu-id="f987b-169">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="f987b-170">22 4294967295</span><span class="sxs-lookup"><span data-stu-id="f987b-170">22 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f987b-171">Commenti</span><span class="sxs-lookup"><span data-stu-id="f987b-171">Remarks</span></span>

<span data-ttu-id="f987b-172">[**L'istanza \_ di Win32 SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) rappresenta un tipo di dati [**SECURITY \_ DESCRIPTOR \_ CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) e contiene un elenco di controllo di accesso discrezionale (DACL) e un elenco di controllo di accesso [*di*](/windows/desktop/SecGloss/s-gly) sistema (SACL). [](/windows/desktop/SecGloss/d-gly)</span><span class="sxs-lookup"><span data-stu-id="f987b-172">The [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance represents a [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) data type and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) and a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="f987b-173">Per altre informazioni, vedere [Elenchi di controllo di accesso](/windows/desktop/SecAuthZ/access-control-lists).</span><span class="sxs-lookup"><span data-stu-id="f987b-173">For more information, see [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span></span>

<span data-ttu-id="f987b-174">Se **SeSecurityPrivilege** non viene concesso o abilitato quando si recupera un descrittore di sicurezza, nel descrittore di sicurezza restituito viene restituito solo l'elenco DACL.</span><span class="sxs-lookup"><span data-stu-id="f987b-174">If the **SeSecurityPrivilege** is not granted or enabled when getting a security descriptor, then only the DACL is returned in the returned security descriptor.</span></span> <span data-ttu-id="f987b-175">Per altre informazioni, vedere [**Costanti dei privilegi**](/windows/desktop/WmiSdk/privilege-constants) ed Esecuzione di operazioni con [privilegi](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="f987b-175">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants) and [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

## <a name="examples"></a><span data-ttu-id="f987b-176">Esempio</span><span class="sxs-lookup"><span data-stu-id="f987b-176">Examples</span></span>

<span data-ttu-id="f987b-177">Quando si recupera un descrittore di sicurezza in VBScript, assicurarsi di "Sicurezza" ed eseguire come Amministratore, come illustrato nel frammento di codice seguente.</span><span class="sxs-lookup"><span data-stu-id="f987b-177">When retrieving a security descriptor in VBScript, be sure to "Security" and run as as Admin, as shown in the following code snippet.</span></span> <span data-ttu-id="f987b-178">In caso contrario, il codice potrebbe generare un errore di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="f987b-178">Otherwise, your code may throw a permissions error.</span></span>


```VB
Set objWMIService = GetObject("winmgmts:" _
  & "{impersonationLevel=impersonate, (Security)}!\\" & strComputer & "\root\cimv2")
```



<span data-ttu-id="f987b-179">Analogamente, in VB.NET assicurarsi di impostare "EnablePrivileges = True" ed eseguire l'applicazione come amministratore.</span><span class="sxs-lookup"><span data-stu-id="f987b-179">Similarly, in VB.NET, be sure to set "EnablePrivileges = True" and run the Application as Admin.</span></span>


```VB
Scope = New ManagementScope([String].Format("\\{0}\root\CIMV2", ComputerName), Nothing)
Scope.Options.EnablePrivileges = True
```



## <a name="requirements"></a><span data-ttu-id="f987b-180">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f987b-180">Requirements</span></span>



| <span data-ttu-id="f987b-181">Requisito</span><span class="sxs-lookup"><span data-stu-id="f987b-181">Requirement</span></span> | <span data-ttu-id="f987b-182">Valore</span><span class="sxs-lookup"><span data-stu-id="f987b-182">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f987b-183">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f987b-183">Minimum supported client</span></span><br/> | <span data-ttu-id="f987b-184">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f987b-184">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f987b-185">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f987b-185">Minimum supported server</span></span><br/> | <span data-ttu-id="f987b-186">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f987b-186">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f987b-187">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f987b-187">Namespace</span></span><br/>                | <span data-ttu-id="f987b-188">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="f987b-188">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f987b-189">MOF</span><span class="sxs-lookup"><span data-stu-id="f987b-189">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f987b-190"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="f987b-190"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f987b-191">DLL</span><span class="sxs-lookup"><span data-stu-id="f987b-191">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f987b-192"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f987b-192"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f987b-193">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f987b-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f987b-194">**Servizio \_ Win32**</span><span class="sxs-lookup"><span data-stu-id="f987b-194">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

[<span data-ttu-id="f987b-195">**Costanti dei privilegi**</span><span class="sxs-lookup"><span data-stu-id="f987b-195">**Privilege Constants**</span></span>](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[<span data-ttu-id="f987b-196">Oggetti descrittori di sicurezza WMI</span><span class="sxs-lookup"><span data-stu-id="f987b-196">WMI Security Descriptor Objects</span></span>](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[<span data-ttu-id="f987b-197">Modifica della sicurezza degli accessi per gli oggetti a protezione diretta</span><span class="sxs-lookup"><span data-stu-id="f987b-197">Changing Access Security on Securable Objects</span></span>](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> <dt>

[<span data-ttu-id="f987b-198">Controllo dell'account utente e WMI</span><span class="sxs-lookup"><span data-stu-id="f987b-198">User Account Control and WMI</span></span>](/windows/desktop/WmiSdk/user-account-control-and-wmi)
</dt> </dl>

 

