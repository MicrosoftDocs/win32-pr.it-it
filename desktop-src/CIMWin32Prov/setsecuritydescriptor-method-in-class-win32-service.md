---
description: Scrive una versione aggiornata del descrittore di sicurezza che controlla l'accesso al servizio.
ms.assetid: c1745b69-f355-4b4c-9e58-6a76c230f498
ms.tgt_platform: multiple
title: Metodo SetSecurityDescriptor della classe Win32_Service (provider WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.SetSecurityDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 82c08f9c560a1d8e419d9a8f6474f8ea9db4e541
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305279"
---
# <a name="setsecuritydescriptor-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="c3c2e-103">Metodo SetSecurityDescriptor della classe Win32_Service (provider WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="c3c2e-103">SetSecurityDescriptor method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="c3c2e-104">Il metodo **SetSecurityDescriptor** scrive una versione aggiornata del descrittore di sicurezza che controlla l'accesso al servizio.</span><span class="sxs-lookup"><span data-stu-id="c3c2e-104">The **SetSecurityDescriptor** method writes an updated version of the security descriptor that controls access to the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3c2e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c3c2e-105">Syntax</span></span>


```mof
uint32 SetSecurityDescriptor(
  [in] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a><span data-ttu-id="c3c2e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c3c2e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3c2e-107">*Descrittore* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c3c2e-107">*Descriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3c2e-108">Descrittore di sicurezza associato al servizio.</span><span class="sxs-lookup"><span data-stu-id="c3c2e-108">The security descriptor associated with the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3c2e-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c3c2e-109">Return value</span></span>

<span data-ttu-id="c3c2e-110">Restituisce uno dei valori elencati nell'elenco seguente o un valore diverso per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="c3c2e-110">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="c3c2e-111">Per ulteriori codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="c3c2e-111">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="c3c2e-112">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="c3c2e-112">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="c3c2e-113">**Success**</span><span class="sxs-lookup"><span data-stu-id="c3c2e-113">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="c3c2e-114">0</span><span class="sxs-lookup"><span data-stu-id="c3c2e-114">0</span></span>

<span data-ttu-id="c3c2e-115">La richiesta è stata accettata.</span><span class="sxs-lookup"><span data-stu-id="c3c2e-115">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="c3c2e-116">**1**</span><span class="sxs-lookup"><span data-stu-id="c3c2e-116">**1**</span></span>
</dt> <dd>

<span data-ttu-id="c3c2e-117">La richiesta non è supportata.</span><span class="sxs-lookup"><span data-stu-id="c3c2e-117">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="c3c2e-118">**Accesso negato**</span><span class="sxs-lookup"><span data-stu-id="c3c2e-118">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="c3c2e-119">2</span><span class="sxs-lookup"><span data-stu-id="c3c2e-119">2</span></span>

<span data-ttu-id="c3c2e-120">L'utente non dispone dell'accesso necessario.</span><span class="sxs-lookup"><span data-stu-id="c3c2e-120">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="c3c2e-121">**3**</span><span class="sxs-lookup"><span data-stu-id="c3c2e-121">**3**</span></span>
</dt> <dd>

<span data-ttu-id="c3c2e-122">Impossibile arrestare il servizio perché altri servizi in esecuzione dipendono dal servizio.</span><span class="sxs-lookup"><span data-stu-id="c3c2e-122">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="c3c2e-123">**4**</span><span class="sxs-lookup"><span data-stu-id="c3c2e-123">**4**</span></span>
</dt> <dd>

<span data-ttu-id="c3c2e-124">Il codice di controllo richiesto non è valido o non è accettabile per il servizio.</span><span class="sxs-lookup"><span data-stu-id="c3c2e-124">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="c3c2e-125">**5**</span><span class="sxs-lookup"><span data-stu-id="c3c2e-125">**5**</span></span>
</dt> <dd>

<span data-ttu-id="c3c2e-126">Impossibile inviare il codice di controllo richiesto al servizio perché lo stato del servizio ([**Win32 \_ BaseService**](win32-baseservice.md).**Proprietà state** ) è uguale a 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="c3c2e-126">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="c3c2e-127">**6**</span><span class="sxs-lookup"><span data-stu-id="c3c2e-127">**6**</span></span>
</dt> <dd>

<span data-ttu-id="c3c2e-128">Il servizio non è stato avviato.</span><span class="sxs-lookup"><span data-stu-id="c3c2e-128">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="c3c2e-129">**7**</span><span class="sxs-lookup"><span data-stu-id="c3c2e-129">**7**</span></span>
</dt> <dd>

<span data-ttu-id="c3c2e-130">Il servizio non ha risposto in tempo utile alla richiesta di avvio.</span><span class="sxs-lookup"><span data-stu-id="c3c2e-130">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="c3c2e-131">**Errore sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="c3c2e-131">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="c3c2e-132">8</span><span class="sxs-lookup"><span data-stu-id="c3c2e-132">8</span></span>

<span data-ttu-id="c3c2e-133">Errore sconosciuto durante l'avvio del servizio.</span><span class="sxs-lookup"><span data-stu-id="c3c2e-133">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="c3c2e-134">**Privilegio mancante**</span><span class="sxs-lookup"><span data-stu-id="c3c2e-134">**Privilege missing**</span></span>
</dt> <dd>

<span data-ttu-id="c3c2e-135">9</span><span class="sxs-lookup"><span data-stu-id="c3c2e-135">9</span></span>

<span data-ttu-id="c3c2e-136">Impossibile trovare il percorso di directory del file eseguibile del servizio.</span><span class="sxs-lookup"><span data-stu-id="c3c2e-136">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="c3c2e-137">**10**</span><span class="sxs-lookup"><span data-stu-id="c3c2e-137">**10**</span></span>
</dt> <dd>

<span data-ttu-id="c3c2e-138">Il servizio è già in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="c3c2e-138">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="c3c2e-139">**11**</span><span class="sxs-lookup"><span data-stu-id="c3c2e-139">**11**</span></span>
</dt> <dd>

<span data-ttu-id="c3c2e-140">Il database a cui aggiungere il nuovo servizio è bloccato.</span><span class="sxs-lookup"><span data-stu-id="c3c2e-140">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="c3c2e-141">**12**</span><span class="sxs-lookup"><span data-stu-id="c3c2e-141">**12**</span></span>
</dt> <dd>

<span data-ttu-id="c3c2e-142">Una dipendenza su cui si basa questo servizio è stata rimossa dal sistema.</span><span class="sxs-lookup"><span data-stu-id="c3c2e-142">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="c3c2e-143">**13**</span><span class="sxs-lookup"><span data-stu-id="c3c2e-143">**13**</span></span>
</dt> <dd>

<span data-ttu-id="c3c2e-144">Impossibile trovare un servizio dipendente necessario.</span><span class="sxs-lookup"><span data-stu-id="c3c2e-144">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="c3c2e-145">**14**</span><span class="sxs-lookup"><span data-stu-id="c3c2e-145">**14**</span></span>
</dt> <dd>

<span data-ttu-id="c3c2e-146">Il servizio è stato disabilitato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="c3c2e-146">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="c3c2e-147">**15**</span><span class="sxs-lookup"><span data-stu-id="c3c2e-147">**15**</span></span>
</dt> <dd>

<span data-ttu-id="c3c2e-148">Il servizio non dispone delle credenziali di autenticazione corrette per l'esecuzione nel sistema.</span><span class="sxs-lookup"><span data-stu-id="c3c2e-148">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="c3c2e-149">**16**</span><span class="sxs-lookup"><span data-stu-id="c3c2e-149">**16**</span></span>
</dt> <dd>

<span data-ttu-id="c3c2e-150">Questo servizio verrà rimosso dal sistema.</span><span class="sxs-lookup"><span data-stu-id="c3c2e-150">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="c3c2e-151">**17**</span><span class="sxs-lookup"><span data-stu-id="c3c2e-151">**17**</span></span>
</dt> <dd>

<span data-ttu-id="c3c2e-152">Il servizio non dispone di un thread di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="c3c2e-152">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="c3c2e-153">**18**</span><span class="sxs-lookup"><span data-stu-id="c3c2e-153">**18**</span></span>
</dt> <dd>

<span data-ttu-id="c3c2e-154">Il servizio ha dipendenze circolari all'avvio.</span><span class="sxs-lookup"><span data-stu-id="c3c2e-154">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="c3c2e-155">**19**</span><span class="sxs-lookup"><span data-stu-id="c3c2e-155">**19**</span></span>
</dt> <dd>

<span data-ttu-id="c3c2e-156">Un servizio è in esecuzione con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="c3c2e-156">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="c3c2e-157">**20**</span><span class="sxs-lookup"><span data-stu-id="c3c2e-157">**20**</span></span>
</dt> <dd>

<span data-ttu-id="c3c2e-158">Il nome del servizio contiene caratteri non validi.</span><span class="sxs-lookup"><span data-stu-id="c3c2e-158">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="c3c2e-159">**Parametro non valido**</span><span class="sxs-lookup"><span data-stu-id="c3c2e-159">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="c3c2e-160">21</span><span class="sxs-lookup"><span data-stu-id="c3c2e-160">21</span></span>

<span data-ttu-id="c3c2e-161">Sono stati passati parametri non validi al servizio.</span><span class="sxs-lookup"><span data-stu-id="c3c2e-161">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="c3c2e-162">**22**</span><span class="sxs-lookup"><span data-stu-id="c3c2e-162">**22**</span></span>
</dt> <dd>

<span data-ttu-id="c3c2e-163">L'account con cui viene eseguito il servizio non è valido o non dispone delle autorizzazioni necessarie per eseguire il servizio.</span><span class="sxs-lookup"><span data-stu-id="c3c2e-163">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="c3c2e-164">**23**</span><span class="sxs-lookup"><span data-stu-id="c3c2e-164">**23**</span></span>
</dt> <dd>

<span data-ttu-id="c3c2e-165">Il servizio esiste già nel database dei servizi disponibili dal sistema.</span><span class="sxs-lookup"><span data-stu-id="c3c2e-165">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="c3c2e-166">**24**</span><span class="sxs-lookup"><span data-stu-id="c3c2e-166">**24**</span></span>
</dt> <dd>

<span data-ttu-id="c3c2e-167">Il servizio è attualmente sospeso nel sistema.</span><span class="sxs-lookup"><span data-stu-id="c3c2e-167">The service is currently paused in the system.</span></span>

</dd> <dt>

<span data-ttu-id="c3c2e-168">**Altri**</span><span class="sxs-lookup"><span data-stu-id="c3c2e-168">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="c3c2e-169">22 4294967295</span><span class="sxs-lookup"><span data-stu-id="c3c2e-169">22 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c3c2e-170">Commenti</span><span class="sxs-lookup"><span data-stu-id="c3c2e-170">Remarks</span></span>

<span data-ttu-id="c3c2e-171">L' [**istanza Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) rappresenta un tipo di dati di [**\_ \_ controllo del descrittore di sicurezza**](/windows/desktop/SecAuthZ/security-descriptor-control) e contiene un elenco di controllo di [*accesso discrezionale*](/windows/desktop/SecGloss/d-gly) (DACL) e un elenco di controllo di accesso di [*sistema*](/windows/desktop/SecGloss/s-gly) (SACL).</span><span class="sxs-lookup"><span data-stu-id="c3c2e-171">The [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance represents a [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) data type and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) and a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="c3c2e-172">Per altre informazioni, vedere [elenchi di controllo di accesso](/windows/desktop/SecAuthZ/access-control-lists).</span><span class="sxs-lookup"><span data-stu-id="c3c2e-172">For more information, see [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span></span>

<span data-ttu-id="c3c2e-173">Se **SeSecurityPrivilege** non viene concesso o abilitato quando si recupera un descrittore di sicurezza, nel descrittore di sicurezza restituito viene restituito solo l'elenco DACL.</span><span class="sxs-lookup"><span data-stu-id="c3c2e-173">If the **SeSecurityPrivilege** is not granted or enabled when getting a security descriptor, then only the DACL is returned in the returned security descriptor.</span></span> <span data-ttu-id="c3c2e-174">Per altre informazioni, vedere [**costanti Privilege**](/windows/desktop/WmiSdk/privilege-constants) ed [esecuzione di operazioni con privilegi](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="c3c2e-174">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants) and [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

<span data-ttu-id="c3c2e-175">È possibile aggiornare sia l'elenco DACL che l'elenco SACL nell'istanza [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) quando si chiama questo metodo, ma è anche possibile aggiornare solo l'elenco DACL o solo il SACL.</span><span class="sxs-lookup"><span data-stu-id="c3c2e-175">You can update both the DACL and the SACL in the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance when calling this method, but you also can update only the DACL or only the SACL.</span></span>

<span data-ttu-id="c3c2e-176">I valori seguenti nel [**\_ \_ controllo descrittore di sicurezza**](/windows/desktop/SecAuthZ/security-descriptor-control) determinano se l'elenco DACL, il SACL o entrambi vengono aggiornati.</span><span class="sxs-lookup"><span data-stu-id="c3c2e-176">The following values in [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) determine whether the DACL, the SACL, or both are updated.</span></span>

-   <span data-ttu-id="c3c2e-177">**\_elenco DACL se \_ presente**</span><span class="sxs-lookup"><span data-stu-id="c3c2e-177">**SE\_DACL\_PRESENT**</span></span>

    <span data-ttu-id="c3c2e-178">Indica che l'elenco DACL deve essere aggiornato.</span><span class="sxs-lookup"><span data-stu-id="c3c2e-178">Indicates that the DACL should be updated.</span></span> <span data-ttu-id="c3c2e-179">Se non è impostato, WMI conserva il valore originale del DACL.</span><span class="sxs-lookup"><span data-stu-id="c3c2e-179">If this is not set, then WMI preserves the original value of the DACL.</span></span>

-   <span data-ttu-id="c3c2e-180">**\_SACL se \_ presente**</span><span class="sxs-lookup"><span data-stu-id="c3c2e-180">**SE\_SACL\_PRESENT**</span></span>

    <span data-ttu-id="c3c2e-181">Indica che il SACL deve essere aggiornato.</span><span class="sxs-lookup"><span data-stu-id="c3c2e-181">Indicates that the SACL should be updated.</span></span> <span data-ttu-id="c3c2e-182">Se non è impostato, WMI conserva il valore originale del SACL.</span><span class="sxs-lookup"><span data-stu-id="c3c2e-182">If this is not set, then WMI preserves the original value of the SACL.</span></span> <span data-ttu-id="c3c2e-183">Per aggiornare il SACL, per l'account deve essere abilitato il privilegio **SeSecurityPrivilege** .</span><span class="sxs-lookup"><span data-stu-id="c3c2e-183">To update the SACL, the account must have the **SeSecurityPrivilege** privilege enabled.</span></span> <span data-ttu-id="c3c2e-184">Per gli script, il nome del privilegio è **SeSecurityPrivilege**.</span><span class="sxs-lookup"><span data-stu-id="c3c2e-184">For scripting, the privilege name is **SeSecurityPrivilege**.</span></span> <span data-ttu-id="c3c2e-185">Per altre informazioni, vedere [**costanti Privilege**](/windows/desktop/WmiSdk/privilege-constants).</span><span class="sxs-lookup"><span data-stu-id="c3c2e-185">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants).</span></span>

<span data-ttu-id="c3c2e-186">Se il Trustee del gruppo e le proprietà del trustee del proprietario non sono **null**, verranno aggiornati.</span><span class="sxs-lookup"><span data-stu-id="c3c2e-186">If the Group trustee and the Owner trustee properties are not **NULL**, then they are updated.</span></span> <span data-ttu-id="c3c2e-187">In caso contrario, WMI conserva i valori originali.</span><span class="sxs-lookup"><span data-stu-id="c3c2e-187">Otherwise, WMI preserves the original values.</span></span> <span data-ttu-id="c3c2e-188">Per ulteriori informazioni, vedere [oggetti del descrittore di sicurezza WMI](/windows/desktop/WmiSdk/wmi-security-descriptor-objects).</span><span class="sxs-lookup"><span data-stu-id="c3c2e-188">For more information, see [WMI Security Descriptor Objects](/windows/desktop/WmiSdk/wmi-security-descriptor-objects).</span></span>

<span data-ttu-id="c3c2e-189">Quando un nuovo SACL è **null** in una chiamata a questo metodo, il SACL del descrittore di sicurezza nell'oggetto a protezione diretta di destinazione viene lasciato invariato.</span><span class="sxs-lookup"><span data-stu-id="c3c2e-189">When a new SACL is **NULL** in a call this method, then the security descriptor SACL on the target securable object is left unchanged.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3c2e-190">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c3c2e-190">Requirements</span></span>



| <span data-ttu-id="c3c2e-191">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3c2e-191">Requirement</span></span> | <span data-ttu-id="c3c2e-192">Valore</span><span class="sxs-lookup"><span data-stu-id="c3c2e-192">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c3c2e-193">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c3c2e-193">Minimum supported client</span></span><br/> | <span data-ttu-id="c3c2e-194">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c3c2e-194">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c3c2e-195">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c3c2e-195">Minimum supported server</span></span><br/> | <span data-ttu-id="c3c2e-196">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c3c2e-196">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c3c2e-197">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c3c2e-197">Namespace</span></span><br/>                | <span data-ttu-id="c3c2e-198">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="c3c2e-198">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c3c2e-199">MOF</span><span class="sxs-lookup"><span data-stu-id="c3c2e-199">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c3c2e-200"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c3c2e-200"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c3c2e-201">DLL</span><span class="sxs-lookup"><span data-stu-id="c3c2e-201">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c3c2e-202"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c3c2e-202"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3c2e-203">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c3c2e-203">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3c2e-204">**\_Servizio Win32**</span><span class="sxs-lookup"><span data-stu-id="c3c2e-204">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

[<span data-ttu-id="c3c2e-205">**Costanti Privilege**</span><span class="sxs-lookup"><span data-stu-id="c3c2e-205">**Privilege Constants**</span></span>](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[<span data-ttu-id="c3c2e-206">Oggetti descrittore di sicurezza WMI</span><span class="sxs-lookup"><span data-stu-id="c3c2e-206">WMI Security Descriptor Objects</span></span>](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[<span data-ttu-id="c3c2e-207">Modifica della sicurezza di accesso per gli oggetti a protezione diretta</span><span class="sxs-lookup"><span data-stu-id="c3c2e-207">Changing Access Security on Securable Objects</span></span>](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> <dt>

[<span data-ttu-id="c3c2e-208">Controllo dell'account utente e WMI</span><span class="sxs-lookup"><span data-stu-id="c3c2e-208">User Account Control and WMI</span></span>](/windows/desktop/WmiSdk/user-account-control-and-wmi)
</dt> </dl>

 

