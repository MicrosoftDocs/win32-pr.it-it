---
description: Restituisce il descrittore di sicurezza che controlla l'accesso alla stampante.
ms.assetid: c12ca35c-07b3-41ad-98c4-48ee584059d1
ms.tgt_platform: multiple
title: Metodo GetSecurityDescriptor della classe Win32_Printer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.GetSecurityDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c74d79430d15fa136c6edeb2a6e77e79e76b02ca
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304682"
---
# <a name="getsecuritydescriptor-method-of-the-win32_printer-class"></a><span data-ttu-id="7374d-103">Metodo GetSecurityDescriptor della \_ classe Printer Win32</span><span class="sxs-lookup"><span data-stu-id="7374d-103">GetSecurityDescriptor method of the Win32\_Printer class</span></span>

<span data-ttu-id="7374d-104">Il metodo **GetSecurityDescriptor** restituisce il descrittore di sicurezza che controlla l'accesso alla stampante.</span><span class="sxs-lookup"><span data-stu-id="7374d-104">The **GetSecurityDescriptor** method returns the security descriptor that controls access to the printer.</span></span> <span data-ttu-id="7374d-105">Il descrittore viene restituito come un'istanza di [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span><span class="sxs-lookup"><span data-stu-id="7374d-105">The descriptor is returned as an instance of [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span> <span data-ttu-id="7374d-106">Per ulteriori informazioni, vedere [modifica della sicurezza di accesso per gli oggetti a protezione diretta](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects).</span><span class="sxs-lookup"><span data-stu-id="7374d-106">For more information, see [Changing Access Security on Securable Objects](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects).</span></span>

<span data-ttu-id="7374d-107">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="7374d-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="7374d-108">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="7374d-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="7374d-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7374d-109">Syntax</span></span>


```mof
uint32 GetSecurityDescriptor(
  [out] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a><span data-ttu-id="7374d-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="7374d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7374d-111">*Descrittore* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="7374d-111">*Descriptor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7374d-112">Descrittore di sicurezza associato alla stampante.</span><span class="sxs-lookup"><span data-stu-id="7374d-112">The security descriptor associated with the printer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7374d-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7374d-113">Return value</span></span>

<span data-ttu-id="7374d-114">Restituisce uno dei valori elencati nell'elenco seguente o un valore diverso per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="7374d-114">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="7374d-115">Per ulteriori codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="7374d-115">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="7374d-116">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="7374d-116">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="7374d-117">**0**</span><span class="sxs-lookup"><span data-stu-id="7374d-117">**0**</span></span>
</dt> <dd>

<span data-ttu-id="7374d-118">Operazione completata.</span><span class="sxs-lookup"><span data-stu-id="7374d-118">Successful completion.</span></span>

</dd> <dt>

<span data-ttu-id="7374d-119">**2**</span><span class="sxs-lookup"><span data-stu-id="7374d-119">**2**</span></span>
</dt> <dd>

<span data-ttu-id="7374d-120">L'utente non ha accesso alle informazioni richieste.</span><span class="sxs-lookup"><span data-stu-id="7374d-120">The user does not have access to the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="7374d-121">**8**</span><span class="sxs-lookup"><span data-stu-id="7374d-121">**8**</span></span>
</dt> <dd>

<span data-ttu-id="7374d-122">Errore sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="7374d-122">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="7374d-123">**9**</span><span class="sxs-lookup"><span data-stu-id="7374d-123">**9**</span></span>
</dt> <dd>

<span data-ttu-id="7374d-124">L'utente non dispone di privilegi sufficienti per eseguire il metodo.</span><span class="sxs-lookup"><span data-stu-id="7374d-124">The user does not have adequate privileges to execute the method.</span></span>

</dd> <dt>

<span data-ttu-id="7374d-125">**21**</span><span class="sxs-lookup"><span data-stu-id="7374d-125">**21**</span></span>
</dt> <dd>

<span data-ttu-id="7374d-126">Un parametro specificato nella chiamata al metodo non è valido.</span><span class="sxs-lookup"><span data-stu-id="7374d-126">A parameter specified in the method call is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7374d-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="7374d-127">Remarks</span></span>

<span data-ttu-id="7374d-128">L' [**istanza Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) rappresenta un tipo di dati di [**\_ \_ controllo del descrittore di sicurezza**](/windows/desktop/SecAuthZ/security-descriptor-control) e contiene un elenco di controllo di [*accesso discrezionale*](/windows/desktop/SecGloss/d-gly) (DACL) e un elenco di controllo di accesso di [*sistema*](/windows/desktop/SecGloss/s-gly) (SACL).</span><span class="sxs-lookup"><span data-stu-id="7374d-128">The [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance represents a [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) data type and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) and a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="7374d-129">Per altre informazioni, vedere [elenchi di controllo di accesso](/windows/desktop/SecAuthZ/access-control-lists).</span><span class="sxs-lookup"><span data-stu-id="7374d-129">For more information, see [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span></span>

<span data-ttu-id="7374d-130">Se **SeSecurityPrivilege** non viene concesso o abilitato quando si recupera un descrittore di sicurezza, nel descrittore di sicurezza restituito viene restituito solo l'elenco DACL.</span><span class="sxs-lookup"><span data-stu-id="7374d-130">If the **SeSecurityPrivilege** is not granted or enabled when getting a security descriptor, then only the DACL is returned in the returned security descriptor.</span></span> <span data-ttu-id="7374d-131">Per altre informazioni, vedere [**costanti Privilege**](/windows/desktop/WmiSdk/privilege-constants) ed [esecuzione di operazioni con privilegi](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="7374d-131">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants) and [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

## <a name="examples"></a><span data-ttu-id="7374d-132">Esempio</span><span class="sxs-lookup"><span data-stu-id="7374d-132">Examples</span></span>

<span data-ttu-id="7374d-133">Nell'esempio di codice VBScript seguente sono elencate le stampanti collegate al computer locale e viene ottenuto il descrittore di sicurezza per ogni stampante.</span><span class="sxs-lookup"><span data-stu-id="7374d-133">The following VBScript code example lists the printers attached to the local computer and gets the security descriptor for each printer.</span></span> <span data-ttu-id="7374d-134">Quindi, le [*voci di controllo*](/windows/desktop/SecGloss/a-gly) di accesso (ACE) nell'elenco di controllo di [*accesso discrezionale*](/windows/desktop/SecGloss/d-gly) (DACL) vengono estratte per determinare quali utenti hanno accesso alla stampante.</span><span class="sxs-lookup"><span data-stu-id="7374d-134">Then the [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACE) in the [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) are extracted to determine which users have access to the printer.</span></span>


```VB
SE_DACL_PRESENT = &h4
ACCESS_ALLOWED_ACE_TYPE = &h0
ACCESS_DENIED_ACE_TYPE  = &h1

strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate, (Security)}!\\" & strComputer & "\root\cimv2")

Set objWMIService = GetObject("winmgmts:")
Set colInstalledPrinters =  objWMIService.ExecQuery _
    ("Select * from Win32_Printer")

For Each objPrinter in colInstalledPrinters
   Wscript.Echo "Name: " & objPrinter.Name 
' Get security descriptor for printer
    Return = objPrinter.GetSecurityDescriptor( objSD )
    If ( return <> 0 ) Then
 WScript.Echo "Could not get security descriptor: " & Return
 wscript.Quit Return
    End If
' Extract the security descriptor flags
    intControlFlags = objSD.ControlFlags
    If intControlFlags AND SE_DACL_PRESENT Then
' Get the ACE entries from security descriptor
        arrACEs = objSD.DACL
    For Each objACE in arrACEs
' Get all the trustees and determine which have access to printer
        WScript.Echo objACE.Trustee.Domain & "\" & objACE.Trustee.Name
        If objACE.AceType = ACCESS_ALLOWED_ACE_TYPE Then
            WScript.Echo vbTab & "User has access to printer"
        ElseIf objACE.AceType = ACCESS_DENIED_ACE_TYPE Then
            WScript.Echo vbTab & "User does not have access to the printer"
        End If
    Next
    Else
    WScript.Echo "No DACL found in security descriptor"
End If
Next
```



## <a name="requirements"></a><span data-ttu-id="7374d-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7374d-135">Requirements</span></span>



| <span data-ttu-id="7374d-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="7374d-136">Requirement</span></span> | <span data-ttu-id="7374d-137">Valore</span><span class="sxs-lookup"><span data-stu-id="7374d-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7374d-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7374d-138">Minimum supported client</span></span><br/> | <span data-ttu-id="7374d-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7374d-139">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="7374d-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7374d-140">Minimum supported server</span></span><br/> | <span data-ttu-id="7374d-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7374d-141">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="7374d-142">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7374d-142">Namespace</span></span><br/>                | <span data-ttu-id="7374d-143">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="7374d-143">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="7374d-144">MOF</span><span class="sxs-lookup"><span data-stu-id="7374d-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7374d-145"><dt>Win32 \_ Printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7374d-145"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="7374d-146">DLL</span><span class="sxs-lookup"><span data-stu-id="7374d-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7374d-147"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7374d-147"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="7374d-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7374d-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7374d-149">**\_Stampante Win32**</span><span class="sxs-lookup"><span data-stu-id="7374d-149">**Win32\_Printer**</span></span>](win32-printer.md)
</dt> <dt>

[<span data-ttu-id="7374d-150">**Costanti Privilege**</span><span class="sxs-lookup"><span data-stu-id="7374d-150">**Privilege Constants**</span></span>](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[<span data-ttu-id="7374d-151">Oggetti descrittore di sicurezza WMI</span><span class="sxs-lookup"><span data-stu-id="7374d-151">WMI Security Descriptor Objects</span></span>](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[<span data-ttu-id="7374d-152">Modifica della sicurezza di accesso per gli oggetti a protezione diretta</span><span class="sxs-lookup"><span data-stu-id="7374d-152">Changing Access Security on Securable Objects</span></span>](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> </dl>

 

