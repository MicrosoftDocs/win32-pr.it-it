---
description: Scrive una versione aggiornata del descrittore di sicurezza che controlla l'accesso alla stampante.
ms.assetid: 6a709043-473e-4b24-8b52-6c68b670ebcf
ms.tgt_platform: multiple
title: Metodo SetSecurityDescriptor della classe Win32_Printer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.SetSecurityDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1572919d0ac0b5c18a6fc5084636c52b9b3ea1c6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225792"
---
# <a name="setsecuritydescriptor-method-of-the-win32_printer-class"></a><span data-ttu-id="b0f5a-103">Metodo SetSecurityDescriptor della \_ classe Printer Win32</span><span class="sxs-lookup"><span data-stu-id="b0f5a-103">SetSecurityDescriptor method of the Win32\_Printer class</span></span>

<span data-ttu-id="b0f5a-104">Il metodo **SetSecurityDescriptor** scrive una versione aggiornata del descrittore di sicurezza che controlla l'accesso alla stampante.</span><span class="sxs-lookup"><span data-stu-id="b0f5a-104">The **SetSecurityDescriptor** method writes an updated version of the security descriptor that controls access to the printer.</span></span> <span data-ttu-id="b0f5a-105">Il descrittore di sicurezza è un'istanza della classe [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .</span><span class="sxs-lookup"><span data-stu-id="b0f5a-105">The security descriptor is an instance of the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class.</span></span> <span data-ttu-id="b0f5a-106">Per ulteriori informazioni, vedere [modifica della sicurezza di accesso per gli oggetti a protezione diretta](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects).</span><span class="sxs-lookup"><span data-stu-id="b0f5a-106">For more information, see [Changing Access Security on Securable Objects](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects).</span></span>

<span data-ttu-id="b0f5a-107">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="b0f5a-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="b0f5a-108">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="b0f5a-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="b0f5a-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b0f5a-109">Syntax</span></span>


```mof
uint32 SetSecurityDescriptor(
  [in] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a><span data-ttu-id="b0f5a-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="b0f5a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0f5a-111">*Descrittore* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b0f5a-111">*Descriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0f5a-112">Descrittore di sicurezza associato alla stampante.</span><span class="sxs-lookup"><span data-stu-id="b0f5a-112">The security descriptor that is associated with the printer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0f5a-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b0f5a-113">Return value</span></span>

<span data-ttu-id="b0f5a-114">Restituisce uno dei valori elencati nell'elenco seguente o un valore diverso per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="b0f5a-114">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="b0f5a-115">Per ulteriori codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="b0f5a-115">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="b0f5a-116">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="b0f5a-116">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="b0f5a-117">**0**</span><span class="sxs-lookup"><span data-stu-id="b0f5a-117">**0**</span></span>
</dt> <dd>

<span data-ttu-id="b0f5a-118">Operazione completata.</span><span class="sxs-lookup"><span data-stu-id="b0f5a-118">Successful completion.</span></span>

</dd> <dt>

<span data-ttu-id="b0f5a-119">**2**</span><span class="sxs-lookup"><span data-stu-id="b0f5a-119">**2**</span></span>
</dt> <dd>

<span data-ttu-id="b0f5a-120">L'utente non ha accesso alle informazioni richieste.</span><span class="sxs-lookup"><span data-stu-id="b0f5a-120">The user does not have access to the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="b0f5a-121">**8**</span><span class="sxs-lookup"><span data-stu-id="b0f5a-121">**8**</span></span>
</dt> <dd>

<span data-ttu-id="b0f5a-122">Errore sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="b0f5a-122">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="b0f5a-123">**9**</span><span class="sxs-lookup"><span data-stu-id="b0f5a-123">**9**</span></span>
</dt> <dd>

<span data-ttu-id="b0f5a-124">L'utente non dispone di privilegi sufficienti per eseguire il metodo.</span><span class="sxs-lookup"><span data-stu-id="b0f5a-124">The user does not have adequate privileges to execute the method.</span></span>

</dd> <dt>

<span data-ttu-id="b0f5a-125">**21**</span><span class="sxs-lookup"><span data-stu-id="b0f5a-125">**21**</span></span>
</dt> <dd>

<span data-ttu-id="b0f5a-126">Un parametro specificato nella chiamata al metodo non è valido.</span><span class="sxs-lookup"><span data-stu-id="b0f5a-126">A parameter specified in the method call is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b0f5a-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="b0f5a-127">Remarks</span></span>

<span data-ttu-id="b0f5a-128">L' [**istanza Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) rappresenta un tipo di dati di [**\_ \_ controllo del descrittore di sicurezza**](/windows/desktop/SecAuthZ/security-descriptor-control) e contiene un elenco di controllo di [*accesso discrezionale*](/windows/desktop/SecGloss/d-gly) (DACL) e un elenco di controllo di accesso di [*sistema*](/windows/desktop/SecGloss/s-gly) (SACL).</span><span class="sxs-lookup"><span data-stu-id="b0f5a-128">The [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance represents a [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) data type and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) and a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="b0f5a-129">Per altre informazioni, vedere [elenchi di controllo di accesso](/windows/desktop/SecAuthZ/access-control-lists).</span><span class="sxs-lookup"><span data-stu-id="b0f5a-129">For more information, see [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span></span>

<span data-ttu-id="b0f5a-130">Se **SeSecurityPrivilege** non viene concesso o abilitato quando si recupera un descrittore di sicurezza, nel descrittore di sicurezza restituito viene restituito solo l'elenco DACL.</span><span class="sxs-lookup"><span data-stu-id="b0f5a-130">If the **SeSecurityPrivilege** is not granted or enabled when getting a security descriptor, then only the DACL is returned in the returned security descriptor.</span></span> <span data-ttu-id="b0f5a-131">Per altre informazioni, vedere [**costanti Privilege**](/windows/desktop/WmiSdk/privilege-constants) ed [esecuzione di operazioni con privilegi](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="b0f5a-131">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants) and [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

<span data-ttu-id="b0f5a-132">È possibile aggiornare sia l'elenco DACL che l'elenco SACL nell'istanza [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) quando si chiama questo metodo, ma è anche possibile aggiornare solo l'elenco DACL o solo il SACL.</span><span class="sxs-lookup"><span data-stu-id="b0f5a-132">You can update both the DACL and the SACL in the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance when calling this method, but you can also update only the DACL or only the SACL.</span></span>

<span data-ttu-id="b0f5a-133">I valori seguenti nel [**\_ \_ controllo descrittore di sicurezza**](/windows/desktop/SecAuthZ/security-descriptor-control) determinano se l'elenco DACL, il SACL o entrambi vengono aggiornati.</span><span class="sxs-lookup"><span data-stu-id="b0f5a-133">The following values in [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) determine whether the DACL, the SACL, or both are updated.</span></span>

-   <span data-ttu-id="b0f5a-134">**\_elenco DACL se \_ presente**</span><span class="sxs-lookup"><span data-stu-id="b0f5a-134">**SE\_DACL\_PRESENT**</span></span>

    <span data-ttu-id="b0f5a-135">Indica che l'elenco DACL deve essere aggiornato.</span><span class="sxs-lookup"><span data-stu-id="b0f5a-135">Indicates that the DACL should be updated.</span></span> <span data-ttu-id="b0f5a-136">Se non è impostato, WMI conserva il valore originale del DACL.</span><span class="sxs-lookup"><span data-stu-id="b0f5a-136">If this is not set then WMI preserves the original value of the DACL.</span></span>

-   <span data-ttu-id="b0f5a-137">**\_SACL se \_ presente**</span><span class="sxs-lookup"><span data-stu-id="b0f5a-137">**SE\_SACL\_PRESENT**</span></span>

    <span data-ttu-id="b0f5a-138">Indica che il SACL deve essere aggiornato.</span><span class="sxs-lookup"><span data-stu-id="b0f5a-138">Indicates that the SACL should be updated.</span></span> <span data-ttu-id="b0f5a-139">Se non è impostato, WMI conserva il valore originale del SACL.</span><span class="sxs-lookup"><span data-stu-id="b0f5a-139">If this is not set, then WMI preserves the original value of the SACL.</span></span> <span data-ttu-id="b0f5a-140">Per aggiornare il SACL, per l'account deve essere abilitato il privilegio **SeSecurityPrivilege** .</span><span class="sxs-lookup"><span data-stu-id="b0f5a-140">To update the SACL, the account must have the **SeSecurityPrivilege** privilege enabled.</span></span> <span data-ttu-id="b0f5a-141">Per gli script, il nome del privilegio è **SeSecurityPrivilege**.</span><span class="sxs-lookup"><span data-stu-id="b0f5a-141">For scripting, the privilege name is **SeSecurityPrivilege**.</span></span> <span data-ttu-id="b0f5a-142">Per altre informazioni, vedere [**costanti Privilege**](/windows/desktop/WmiSdk/privilege-constants).</span><span class="sxs-lookup"><span data-stu-id="b0f5a-142">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants).</span></span>

<span data-ttu-id="b0f5a-143">Se il Trustee del gruppo e le proprietà del trustee del proprietario non sono **null**, verranno aggiornati.</span><span class="sxs-lookup"><span data-stu-id="b0f5a-143">If the Group trustee and the Owner trustee properties are not **NULL**, then they are updated.</span></span> <span data-ttu-id="b0f5a-144">In caso contrario, WMI conserva i valori originali.</span><span class="sxs-lookup"><span data-stu-id="b0f5a-144">Otherwise, WMI preserves the original values.</span></span> <span data-ttu-id="b0f5a-145">Per ulteriori informazioni, vedere [oggetti del descrittore di sicurezza WMI](/windows/desktop/WmiSdk/wmi-security-descriptor-objects).</span><span class="sxs-lookup"><span data-stu-id="b0f5a-145">For more information, see [WMI Security Descriptor Objects](/windows/desktop/WmiSdk/wmi-security-descriptor-objects).</span></span>

<span data-ttu-id="b0f5a-146">Quando un nuovo SACL è **null** in una chiamata a questo metodo, il SACL del descrittore di sicurezza nell'oggetto a protezione diretta di destinazione viene lasciato invariato.</span><span class="sxs-lookup"><span data-stu-id="b0f5a-146">When a new SACL is **NULL** in a call to this method, then the security descriptor SACL on the target securable object is left unchanged.</span></span>

## <a name="examples"></a><span data-ttu-id="b0f5a-147">Esempio</span><span class="sxs-lookup"><span data-stu-id="b0f5a-147">Examples</span></span>

<span data-ttu-id="b0f5a-148">L'esempio di PowerShell [Copy-ACLToPrinter](https://Gallery.TechNet.Microsoft.Com/Copy-ACLToPrinter-2d66ce19) sostituisce le autorizzazioni (ACL) da una stampante a un'altra.</span><span class="sxs-lookup"><span data-stu-id="b0f5a-148">The [Copy-ACLToPrinter](https://Gallery.TechNet.Microsoft.Com/Copy-ACLToPrinter-2d66ce19) PowerShell sample Replace the permissions (ACL) from one printer to another.</span></span>

<span data-ttu-id="b0f5a-149">Nell'esempio di codice PowerShell seguente viene descritto come impostare il descrittore di sicurezza per una stampante.</span><span class="sxs-lookup"><span data-stu-id="b0f5a-149">The following PowerShell code sample describes how to set the security descriptor for a printer.</span></span>


```PowerShell
# Specify the user or group
$user = "everyone"

# create instances of necessary classes
$SD = ([WMIClass] "Win32_SecurityDescriptor").CreateInstance()
$ace = ([WMIClass] "Win32_Ace").CreateInstance()
$Trustee = ([WMIClass] "Win32_Trustee").CreateInstance()

# Translate a name of user or group to SID
$SID = (new-object security.principal.ntaccount $user).translate([security.principal.securityidentifier])

# Get binary form from SID and byte Array
[byte[]] $SIDArray = ,0 * $SID.BinaryLength
$SID.GetBinaryForm($SIDArray,0)

# Fill Trustee object parameters
$Trustee.Name = $user
$Trustee.SID = $SIDArray

# Set AccessMask which can contain following values:
# Takeownership - 524288
# ReadPermissions - 131072
# ChangePermissions - 262144
# ManageDocuments - 983088
# ManagePrinters - 983052
# Print + ReadPermissions - 131080
$ace.AccessMask = 983052

# Set AceType. Can be 0 (Allow), or 1 (Deny), or 2 (System Audit)
$ace.AceType = 0
$ace.AceFlags = 0  

# Write Win32_Trustee object to Win32_Ace Trustee property
$ace.Trustee = $Trustee

# Write Win32_Ace and Win32_Trustee objects to SecurityDescriptor object
$SD.DACL = $ace

# Set SE_DACL_PRESENT control flag
$SD.ControlFlags = 0x0004

# Get printer object. For example 'CutePDF Writer' printer object
$Printer = gwmi win32_printer -filter "name = 'CutePDF Writer'"

# Enable SeSecurityPrivilege privilegies
$Printer.psbase.Scope.Options.EnablePrivileges = $true

# Invoke SetSecurityDescriptor method and write new ACE to specified
# printer ACL.
$Printer.SetSecurityDescriptor($SD)
```



## <a name="requirements"></a><span data-ttu-id="b0f5a-150">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b0f5a-150">Requirements</span></span>



| <span data-ttu-id="b0f5a-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0f5a-151">Requirement</span></span> | <span data-ttu-id="b0f5a-152">Valore</span><span class="sxs-lookup"><span data-stu-id="b0f5a-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0f5a-153">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b0f5a-153">Minimum supported client</span></span><br/> | <span data-ttu-id="b0f5a-154">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b0f5a-154">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="b0f5a-155">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b0f5a-155">Minimum supported server</span></span><br/> | <span data-ttu-id="b0f5a-156">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b0f5a-156">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="b0f5a-157">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b0f5a-157">Namespace</span></span><br/>                | <span data-ttu-id="b0f5a-158">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="b0f5a-158">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="b0f5a-159">MOF</span><span class="sxs-lookup"><span data-stu-id="b0f5a-159">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b0f5a-160"><dt>Win32 \_ Printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b0f5a-160"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="b0f5a-161">DLL</span><span class="sxs-lookup"><span data-stu-id="b0f5a-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b0f5a-162"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b0f5a-162"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="b0f5a-163">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b0f5a-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0f5a-164">**\_Stampante Win32**</span><span class="sxs-lookup"><span data-stu-id="b0f5a-164">**Win32\_Printer**</span></span>](win32-printer.md)
</dt> <dt>

[<span data-ttu-id="b0f5a-165">**Costanti Privilege**</span><span class="sxs-lookup"><span data-stu-id="b0f5a-165">**Privilege Constants**</span></span>](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[<span data-ttu-id="b0f5a-166">Oggetti descrittore di sicurezza WMI</span><span class="sxs-lookup"><span data-stu-id="b0f5a-166">WMI Security Descriptor Objects</span></span>](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[<span data-ttu-id="b0f5a-167">Modifica della sicurezza di accesso per gli oggetti a protezione diretta</span><span class="sxs-lookup"><span data-stu-id="b0f5a-167">Changing Access Security on Securable Objects</span></span>](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> </dl>

 

