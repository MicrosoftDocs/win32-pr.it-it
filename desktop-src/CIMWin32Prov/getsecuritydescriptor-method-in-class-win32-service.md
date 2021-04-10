---
description: Restituisce il descrittore di sicurezza che controlla l'accesso al servizio.
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
ms.openlocfilehash: 5bf8dee49893a5a1d3b628e72b0b0746a6215fb0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049151"
---
# <a name="getsecuritydescriptor-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="915f7-103">Metodo GetSecurityDescriptor della classe Win32_Service (provider WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="915f7-103">GetSecurityDescriptor method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="915f7-104">Il metodo **GetSecurityDescriptor** restituisce il descrittore di sicurezza che controlla l'accesso al servizio.</span><span class="sxs-lookup"><span data-stu-id="915f7-104">The **GetSecurityDescriptor** method returns the security descriptor that controls access to the service.</span></span> <span data-ttu-id="915f7-105">Il descrittore viene restituito come un'istanza di [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span><span class="sxs-lookup"><span data-stu-id="915f7-105">The descriptor is returned as an instance of [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span>

## <a name="syntax"></a><span data-ttu-id="915f7-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="915f7-106">Syntax</span></span>


```mof
uint32 GetSecurityDescriptor(
  [out] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a><span data-ttu-id="915f7-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="915f7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="915f7-108">*Descrittore* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="915f7-108">*Descriptor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="915f7-109">Descrittore di sicurezza associato al servizio.</span><span class="sxs-lookup"><span data-stu-id="915f7-109">The security descriptor associated with the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="915f7-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="915f7-110">Return value</span></span>

<span data-ttu-id="915f7-111">Restituisce uno dei valori elencati nell'elenco seguente o un valore diverso per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="915f7-111">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="915f7-112">Per ulteriori codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="915f7-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="915f7-113">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="915f7-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="915f7-114">**Success**</span><span class="sxs-lookup"><span data-stu-id="915f7-114">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="915f7-115">0</span><span class="sxs-lookup"><span data-stu-id="915f7-115">0</span></span>

<span data-ttu-id="915f7-116">La richiesta è stata accettata.</span><span class="sxs-lookup"><span data-stu-id="915f7-116">The request was accepted.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="915f7-117">1</span><span class="sxs-lookup"><span data-stu-id="915f7-117">1</span></span>

<span data-ttu-id="915f7-118">La richiesta non è supportata.</span><span class="sxs-lookup"><span data-stu-id="915f7-118">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="915f7-119">**Accesso negato**</span><span class="sxs-lookup"><span data-stu-id="915f7-119">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="915f7-120">2</span><span class="sxs-lookup"><span data-stu-id="915f7-120">2</span></span>

<span data-ttu-id="915f7-121">L'utente non dispone dell'accesso necessario.</span><span class="sxs-lookup"><span data-stu-id="915f7-121">The user did not have the necessary access.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="915f7-122">3</span><span class="sxs-lookup"><span data-stu-id="915f7-122">3</span></span>

<span data-ttu-id="915f7-123">Impossibile arrestare il servizio perché altri servizi in esecuzione dipendono dal servizio.</span><span class="sxs-lookup"><span data-stu-id="915f7-123">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="915f7-124">4</span><span class="sxs-lookup"><span data-stu-id="915f7-124">4</span></span>

<span data-ttu-id="915f7-125">Il codice di controllo richiesto non è valido o non è accettabile per il servizio.</span><span class="sxs-lookup"><span data-stu-id="915f7-125">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="915f7-126">5</span><span class="sxs-lookup"><span data-stu-id="915f7-126">5</span></span>

<span data-ttu-id="915f7-127">Impossibile inviare il codice di controllo richiesto al servizio perché lo stato del servizio ([**Win32 \_ BaseService**](win32-baseservice.md).**Proprietà state** ) è uguale a 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="915f7-127">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="915f7-128">6</span><span class="sxs-lookup"><span data-stu-id="915f7-128">6</span></span>

<span data-ttu-id="915f7-129">Il servizio non è stato avviato.</span><span class="sxs-lookup"><span data-stu-id="915f7-129">The service has not been started.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="915f7-130">7</span><span class="sxs-lookup"><span data-stu-id="915f7-130">7</span></span>

<span data-ttu-id="915f7-131">Il servizio non ha risposto in tempo utile alla richiesta di avvio.</span><span class="sxs-lookup"><span data-stu-id="915f7-131">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="915f7-132">**Errore sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="915f7-132">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="915f7-133">8</span><span class="sxs-lookup"><span data-stu-id="915f7-133">8</span></span>

<span data-ttu-id="915f7-134">Errore sconosciuto durante l'avvio del servizio.</span><span class="sxs-lookup"><span data-stu-id="915f7-134">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="915f7-135">**Privilegio mancante**</span><span class="sxs-lookup"><span data-stu-id="915f7-135">**Privilege missing**</span></span>
</dt> <dd>

<span data-ttu-id="915f7-136">9</span><span class="sxs-lookup"><span data-stu-id="915f7-136">9</span></span>

<span data-ttu-id="915f7-137">Impossibile trovare il percorso di directory del file eseguibile del servizio.</span><span class="sxs-lookup"><span data-stu-id="915f7-137">The directory path to the service executable file was not found.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="915f7-138">10</span><span class="sxs-lookup"><span data-stu-id="915f7-138">10</span></span>

<span data-ttu-id="915f7-139">Il servizio è già in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="915f7-139">The service is already running.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="915f7-140">11</span><span class="sxs-lookup"><span data-stu-id="915f7-140">11</span></span>

<span data-ttu-id="915f7-141">Il database a cui aggiungere il nuovo servizio è bloccato.</span><span class="sxs-lookup"><span data-stu-id="915f7-141">The database to add a new service is locked.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="915f7-142">12</span><span class="sxs-lookup"><span data-stu-id="915f7-142">12</span></span>

<span data-ttu-id="915f7-143">Una dipendenza su cui si basa questo servizio è stata rimossa dal sistema.</span><span class="sxs-lookup"><span data-stu-id="915f7-143">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="915f7-144">13</span><span class="sxs-lookup"><span data-stu-id="915f7-144">13</span></span>

<span data-ttu-id="915f7-145">Impossibile trovare un servizio dipendente necessario.</span><span class="sxs-lookup"><span data-stu-id="915f7-145">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="915f7-146">14</span><span class="sxs-lookup"><span data-stu-id="915f7-146">14</span></span>

<span data-ttu-id="915f7-147">Il servizio è stato disabilitato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="915f7-147">The service has been disabled from the system.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="915f7-148">15</span><span class="sxs-lookup"><span data-stu-id="915f7-148">15</span></span>

<span data-ttu-id="915f7-149">Il servizio non dispone delle credenziali di autenticazione corrette per l'esecuzione nel sistema.</span><span class="sxs-lookup"><span data-stu-id="915f7-149">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="915f7-150">16</span><span class="sxs-lookup"><span data-stu-id="915f7-150">16</span></span>

<span data-ttu-id="915f7-151">Questo servizio verrà rimosso dal sistema.</span><span class="sxs-lookup"><span data-stu-id="915f7-151">This service is being removed from the system.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="915f7-152">17</span><span class="sxs-lookup"><span data-stu-id="915f7-152">17</span></span>

<span data-ttu-id="915f7-153">Il servizio non dispone di un thread di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="915f7-153">The service has no execution thread.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="915f7-154">18</span><span class="sxs-lookup"><span data-stu-id="915f7-154">18</span></span>

<span data-ttu-id="915f7-155">Il servizio ha dipendenze circolari all'avvio.</span><span class="sxs-lookup"><span data-stu-id="915f7-155">The service has circular dependencies when it starts.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="915f7-156">19</span><span class="sxs-lookup"><span data-stu-id="915f7-156">19</span></span>

<span data-ttu-id="915f7-157">Un servizio è in esecuzione con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="915f7-157">A service is running under the same name.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="915f7-158">20</span><span class="sxs-lookup"><span data-stu-id="915f7-158">20</span></span>

<span data-ttu-id="915f7-159">Il nome del servizio contiene caratteri non validi.</span><span class="sxs-lookup"><span data-stu-id="915f7-159">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="915f7-160">**Parametro non valido**</span><span class="sxs-lookup"><span data-stu-id="915f7-160">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="915f7-161">21</span><span class="sxs-lookup"><span data-stu-id="915f7-161">21</span></span>

<span data-ttu-id="915f7-162">Sono stati passati parametri non validi al servizio.</span><span class="sxs-lookup"><span data-stu-id="915f7-162">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="915f7-163">22</span><span class="sxs-lookup"><span data-stu-id="915f7-163">22</span></span>

<span data-ttu-id="915f7-164">L'account con cui viene eseguito il servizio non è valido o non dispone delle autorizzazioni necessarie per eseguire il servizio.</span><span class="sxs-lookup"><span data-stu-id="915f7-164">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="915f7-165">23</span><span class="sxs-lookup"><span data-stu-id="915f7-165">23</span></span>

<span data-ttu-id="915f7-166">Il servizio esiste già nel database dei servizi disponibili dal sistema.</span><span class="sxs-lookup"><span data-stu-id="915f7-166">The service exists in the database of services available from the system.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="915f7-167">24</span><span class="sxs-lookup"><span data-stu-id="915f7-167">24</span></span>

<span data-ttu-id="915f7-168">Il servizio è attualmente sospeso nel sistema.</span><span class="sxs-lookup"><span data-stu-id="915f7-168">The service is currently paused in the system.</span></span>

</dd> <dt>

<span data-ttu-id="915f7-169">**Altri**</span><span class="sxs-lookup"><span data-stu-id="915f7-169">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="915f7-170">22 4294967295</span><span class="sxs-lookup"><span data-stu-id="915f7-170">22 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="915f7-171">Commenti</span><span class="sxs-lookup"><span data-stu-id="915f7-171">Remarks</span></span>

<span data-ttu-id="915f7-172">L' [**istanza Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) rappresenta un tipo di dati di [**\_ \_ controllo del descrittore di sicurezza**](/windows/desktop/SecAuthZ/security-descriptor-control) e contiene un elenco di controllo di [*accesso discrezionale*](/windows/desktop/SecGloss/d-gly) (DACL) e un elenco di controllo di accesso di [*sistema*](/windows/desktop/SecGloss/s-gly) (SACL).</span><span class="sxs-lookup"><span data-stu-id="915f7-172">The [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance represents a [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) data type and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) and a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="915f7-173">Per altre informazioni, vedere [elenchi di controllo di accesso](/windows/desktop/SecAuthZ/access-control-lists).</span><span class="sxs-lookup"><span data-stu-id="915f7-173">For more information, see [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span></span>

<span data-ttu-id="915f7-174">Se **SeSecurityPrivilege** non viene concesso o abilitato quando si recupera un descrittore di sicurezza, nel descrittore di sicurezza restituito viene restituito solo l'elenco DACL.</span><span class="sxs-lookup"><span data-stu-id="915f7-174">If the **SeSecurityPrivilege** is not granted or enabled when getting a security descriptor, then only the DACL is returned in the returned security descriptor.</span></span> <span data-ttu-id="915f7-175">Per altre informazioni, vedere [**costanti Privilege**](/windows/desktop/WmiSdk/privilege-constants) ed [esecuzione di operazioni con privilegi](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="915f7-175">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants) and [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

## <a name="examples"></a><span data-ttu-id="915f7-176">Esempio</span><span class="sxs-lookup"><span data-stu-id="915f7-176">Examples</span></span>

<span data-ttu-id="915f7-177">Quando si recupera un descrittore di sicurezza in VBScript, assicurarsi di "sicurezza" ed eseguire come amministratore, come illustrato nel frammento di codice seguente.</span><span class="sxs-lookup"><span data-stu-id="915f7-177">When retrieving a security descriptor in VBScript, be sure to "Security" and run as as Admin, as shown in the following code snippet.</span></span> <span data-ttu-id="915f7-178">In caso contrario, il codice potrebbe generare un errore di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="915f7-178">Otherwise, your code may throw a permissions error.</span></span>


```VB
Set objWMIService = GetObject("winmgmts:" _
  & "{impersonationLevel=impersonate, (Security)}!\\" & strComputer & "\root\cimv2")
```



<span data-ttu-id="915f7-179">Analogamente, in VB.NET, assicurarsi di impostare "EnablePrivileges = true" ed eseguire l'applicazione come amministratore.</span><span class="sxs-lookup"><span data-stu-id="915f7-179">Similarly, in VB.NET, be sure to set "EnablePrivileges = True" and run the Application as Admin.</span></span>


```VB
Scope = New ManagementScope([String].Format("\\{0}\root\CIMV2", ComputerName), Nothing)
Scope.Options.EnablePrivileges = True
```



## <a name="requirements"></a><span data-ttu-id="915f7-180">Requisiti</span><span class="sxs-lookup"><span data-stu-id="915f7-180">Requirements</span></span>



| <span data-ttu-id="915f7-181">Requisito</span><span class="sxs-lookup"><span data-stu-id="915f7-181">Requirement</span></span> | <span data-ttu-id="915f7-182">Valore</span><span class="sxs-lookup"><span data-stu-id="915f7-182">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="915f7-183">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="915f7-183">Minimum supported client</span></span><br/> | <span data-ttu-id="915f7-184">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="915f7-184">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="915f7-185">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="915f7-185">Minimum supported server</span></span><br/> | <span data-ttu-id="915f7-186">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="915f7-186">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="915f7-187">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="915f7-187">Namespace</span></span><br/>                | <span data-ttu-id="915f7-188">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="915f7-188">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="915f7-189">MOF</span><span class="sxs-lookup"><span data-stu-id="915f7-189">MOF</span></span><br/>                      | <dl> <span data-ttu-id="915f7-190"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="915f7-190"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="915f7-191">DLL</span><span class="sxs-lookup"><span data-stu-id="915f7-191">DLL</span></span><br/>                      | <dl> <span data-ttu-id="915f7-192"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="915f7-192"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="915f7-193">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="915f7-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="915f7-194">**\_Servizio Win32**</span><span class="sxs-lookup"><span data-stu-id="915f7-194">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

[<span data-ttu-id="915f7-195">**Costanti Privilege**</span><span class="sxs-lookup"><span data-stu-id="915f7-195">**Privilege Constants**</span></span>](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[<span data-ttu-id="915f7-196">Oggetti descrittore di sicurezza WMI</span><span class="sxs-lookup"><span data-stu-id="915f7-196">WMI Security Descriptor Objects</span></span>](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[<span data-ttu-id="915f7-197">Modifica della sicurezza di accesso per gli oggetti a protezione diretta</span><span class="sxs-lookup"><span data-stu-id="915f7-197">Changing Access Security on Securable Objects</span></span>](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> <dt>

[<span data-ttu-id="915f7-198">Controllo dell'account utente e WMI</span><span class="sxs-lookup"><span data-stu-id="915f7-198">User Account Control and WMI</span></span>](/windows/desktop/WmiSdk/user-account-control-and-wmi)
</dt> </dl>

 

