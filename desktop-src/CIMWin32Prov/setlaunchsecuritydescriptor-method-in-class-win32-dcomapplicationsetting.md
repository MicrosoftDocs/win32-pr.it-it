---
description: Aggiorna il descrittore di sicurezza di avvio dell'applicazione DCOM con un nuovo descrittore di sicurezza definito da un'istanza di una \_ classe Win32 securityDescriptor.
ms.assetid: 72245d22-1a0a-4069-b5d6-9d59e4de4aab
ms.tgt_platform: multiple
title: Metodo SetLaunchSecurityDescriptor della classe Win32_DCOMApplicationSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DCOMApplicationSetting.SetLaunchSecurityDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4a99919246d7b36aa265d36ae0f75e8347ea6a25
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877957"
---
# <a name="setlaunchsecuritydescriptor-method-of-the-win32_dcomapplicationsetting-class"></a><span data-ttu-id="82d08-103">Metodo SetLaunchSecurityDescriptor della \_ classe DCOMApplicationSetting Win32</span><span class="sxs-lookup"><span data-stu-id="82d08-103">SetLaunchSecurityDescriptor method of the Win32\_DCOMApplicationSetting class</span></span>

<span data-ttu-id="82d08-104">Il metodo **SetLaunchSecurityDescriptor** aggiorna il descrittore di sicurezza di avvio dell'applicazione DCOM con un nuovo descrittore di sicurezza definito da un'istanza di una classe [**\_ securityDescriptor Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .</span><span class="sxs-lookup"><span data-stu-id="82d08-104">The **SetLaunchSecurityDescriptor** method updates the launch security descriptor of the DCOM application with a new security descriptor that is defined by an instance of a [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class.</span></span> <span data-ttu-id="82d08-105">Questo descrittore di sicurezza controlla chi può avviare l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="82d08-105">This security descriptor controls who is allowed to launch the application.</span></span> <span data-ttu-id="82d08-106">L'account che esegue lo script o l'applicazione che chiama questo metodo deve avere i privilegi **SeSecurityPrivilege** e **SeRestorePrivilege** .</span><span class="sxs-lookup"><span data-stu-id="82d08-106">The account running the script or application that calls this method must have the **SeSecurityPrivilege** and **SeRestorePrivilege** privileges.</span></span> <span data-ttu-id="82d08-107">Per ulteriori informazioni, vedere [modifica della sicurezza di accesso per gli oggetti a protezione diretta](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects).</span><span class="sxs-lookup"><span data-stu-id="82d08-107">For more information, see [Changing Access Security on Securable Objects](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects).</span></span>

## <a name="syntax"></a><span data-ttu-id="82d08-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="82d08-108">Syntax</span></span>


```mof
uint32 SetLaunchSecurityDescriptor(
  [in] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a><span data-ttu-id="82d08-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="82d08-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82d08-110">*Descrittore* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="82d08-110">*Descriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82d08-111">Descrittore di sicurezza da impostare che controlla chi può avviare l'applicazione DCOM.</span><span class="sxs-lookup"><span data-stu-id="82d08-111">The security descriptor to set that controls who can start the DCOM application.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82d08-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="82d08-112">Return value</span></span>

<span data-ttu-id="82d08-113">Restituisce uno dei valori elencati nell'elenco seguente o un valore diverso per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="82d08-113">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="82d08-114">Per ulteriori informazioni, vedere [codici restituiti WMI](/windows/desktop/WmiSdk/wmi-return-codes) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="82d08-114">For more information, see [WMI Return Codes](/windows/desktop/WmiSdk/wmi-return-codes) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

<dl> <dt>

<span data-ttu-id="82d08-115">**Success**</span><span class="sxs-lookup"><span data-stu-id="82d08-115">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="82d08-116">0</span><span class="sxs-lookup"><span data-stu-id="82d08-116">0</span></span>

<span data-ttu-id="82d08-117">Operazione completata.</span><span class="sxs-lookup"><span data-stu-id="82d08-117">Successful completion.</span></span>

</dd> <dt>

<span data-ttu-id="82d08-118">**2**</span><span class="sxs-lookup"><span data-stu-id="82d08-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="82d08-119">L'utente non ha accesso alle informazioni richieste.</span><span class="sxs-lookup"><span data-stu-id="82d08-119">The user does not have access to the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="82d08-120">**8**</span><span class="sxs-lookup"><span data-stu-id="82d08-120">**8**</span></span>
</dt> <dd>

<span data-ttu-id="82d08-121">Errore sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="82d08-121">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="82d08-122">**9**</span><span class="sxs-lookup"><span data-stu-id="82d08-122">**9**</span></span>
</dt> <dd>

<span data-ttu-id="82d08-123">L'utente non dispone di privilegi sufficienti per eseguire il metodo.</span><span class="sxs-lookup"><span data-stu-id="82d08-123">The user does not have adequate privileges to execute the method.</span></span>

</dd> <dt>

<span data-ttu-id="82d08-124">**21**</span><span class="sxs-lookup"><span data-stu-id="82d08-124">**21**</span></span>
</dt> <dd>

<span data-ttu-id="82d08-125">Un parametro specificato nella chiamata al metodo non è valido.</span><span class="sxs-lookup"><span data-stu-id="82d08-125">A parameter specified in the method call is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="82d08-126">**Altri**</span><span class="sxs-lookup"><span data-stu-id="82d08-126">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="82d08-127">1 4294967295</span><span class="sxs-lookup"><span data-stu-id="82d08-127">1 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="82d08-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="82d08-128">Remarks</span></span>

<span data-ttu-id="82d08-129">L' [**istanza Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) rappresenta un tipo di dati di [**\_ \_ controllo del descrittore di sicurezza**](/windows/desktop/SecAuthZ/security-descriptor-control) e contiene un elenco di controllo di [*accesso discrezionale*](/windows/desktop/SecGloss/d-gly) (DACL) e un elenco di controllo di accesso di [*sistema*](/windows/desktop/SecGloss/s-gly) (SACL).</span><span class="sxs-lookup"><span data-stu-id="82d08-129">The [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance represents a [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) data type and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) and a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="82d08-130">Per altre informazioni, vedere [elenchi di controllo di accesso](/windows/desktop/SecAuthZ/access-control-lists).</span><span class="sxs-lookup"><span data-stu-id="82d08-130">For more information, see [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span></span>

<span data-ttu-id="82d08-131">Se **SeSecurityPrivilege** non viene concesso o abilitato quando si recupera un descrittore di sicurezza, nel descrittore di sicurezza restituito viene restituito solo l'elenco DACL.</span><span class="sxs-lookup"><span data-stu-id="82d08-131">If the **SeSecurityPrivilege** is not granted or enabled when getting a security descriptor, then only the DACL is returned in the returned security descriptor.</span></span> <span data-ttu-id="82d08-132">Per altre informazioni, vedere [**costanti Privilege**](/windows/desktop/WmiSdk/privilege-constants) ed [esecuzione di operazioni con privilegi](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="82d08-132">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants) and [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

<span data-ttu-id="82d08-133">È possibile aggiornare sia l'elenco DACL che l'elenco SACL nell'istanza [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) quando si chiama questo metodo, ma è anche possibile aggiornare solo l'elenco DACL o solo il SACL.</span><span class="sxs-lookup"><span data-stu-id="82d08-133">You can update both the DACL and the SACL in the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance when calling this method, but you also can update only the DACL or only the SACL.</span></span>

<span data-ttu-id="82d08-134">I valori seguenti nel [**\_ \_ controllo descrittore di sicurezza**](/windows/desktop/SecAuthZ/security-descriptor-control) determinano se l'elenco DACL, il SACL o entrambi vengono aggiornati.</span><span class="sxs-lookup"><span data-stu-id="82d08-134">The following values in [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) determine whether the DACL, the SACL, or both are updated.</span></span>

-   <span data-ttu-id="82d08-135">**\_elenco DACL se \_ presente**</span><span class="sxs-lookup"><span data-stu-id="82d08-135">**SE\_DACL\_PRESENT**</span></span>

    <span data-ttu-id="82d08-136">Indica che l'elenco DACL deve essere aggiornato.</span><span class="sxs-lookup"><span data-stu-id="82d08-136">Indicates that the DACL should be updated.</span></span> <span data-ttu-id="82d08-137">Se non è impostato, WMI conserva il valore originale del DACL.</span><span class="sxs-lookup"><span data-stu-id="82d08-137">If this is not set, then WMI preserves the original value of the DACL.</span></span>

-   <span data-ttu-id="82d08-138">**\_SACL se \_ presente**</span><span class="sxs-lookup"><span data-stu-id="82d08-138">**SE\_SACL\_PRESENT**</span></span>

    <span data-ttu-id="82d08-139">Indica che il SACL deve essere aggiornato.</span><span class="sxs-lookup"><span data-stu-id="82d08-139">Indicates that the SACL should be updated.</span></span> <span data-ttu-id="82d08-140">Se non è impostato, WMI conserva il valore originale del SACL.</span><span class="sxs-lookup"><span data-stu-id="82d08-140">If this is not set, then WMI preserves the original value of the SACL.</span></span> <span data-ttu-id="82d08-141">Per aggiornare il SACL, per l'account deve essere abilitato il privilegio **SeSecurityPrivilege** .</span><span class="sxs-lookup"><span data-stu-id="82d08-141">To update the SACL, the account must have the **SeSecurityPrivilege** privilege enabled.</span></span> <span data-ttu-id="82d08-142">Per gli script, il nome del privilegio è **SeSecurityPrivilege**.</span><span class="sxs-lookup"><span data-stu-id="82d08-142">For scripting, the privilege name is **SeSecurityPrivilege**.</span></span> <span data-ttu-id="82d08-143">Per altre informazioni, vedere [**costanti Privilege**](/windows/desktop/WmiSdk/privilege-constants).</span><span class="sxs-lookup"><span data-stu-id="82d08-143">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants).</span></span>

<span data-ttu-id="82d08-144">Se il Trustee del gruppo e le proprietà del trustee del proprietario non sono **null**, verranno aggiornati.</span><span class="sxs-lookup"><span data-stu-id="82d08-144">If the Group trustee and the Owner trustee properties are not **NULL**, then they are updated.</span></span> <span data-ttu-id="82d08-145">In caso contrario, WMI conserva i valori originali.</span><span class="sxs-lookup"><span data-stu-id="82d08-145">Otherwise, WMI preserves the original values.</span></span> <span data-ttu-id="82d08-146">Per ulteriori informazioni, vedere [oggetti del descrittore di sicurezza WMI](/windows/desktop/WmiSdk/wmi-security-descriptor-objects).</span><span class="sxs-lookup"><span data-stu-id="82d08-146">For more information, see [WMI Security Descriptor Objects](/windows/desktop/WmiSdk/wmi-security-descriptor-objects).</span></span>

<span data-ttu-id="82d08-147">Quando un nuovo SACL è **null** in una chiamata a questo metodo, il SACL del descrittore di sicurezza nell'oggetto a protezione diretta di destinazione viene lasciato invariato.</span><span class="sxs-lookup"><span data-stu-id="82d08-147">When a new SACL is **NULL** in a call to this method, then the security descriptor SACL on the target securable object is left unchanged.</span></span>

## <a name="requirements"></a><span data-ttu-id="82d08-148">Requisiti</span><span class="sxs-lookup"><span data-stu-id="82d08-148">Requirements</span></span>



| <span data-ttu-id="82d08-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="82d08-149">Requirement</span></span> | <span data-ttu-id="82d08-150">Valore</span><span class="sxs-lookup"><span data-stu-id="82d08-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="82d08-151">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="82d08-151">Minimum supported client</span></span><br/> | <span data-ttu-id="82d08-152">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="82d08-152">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="82d08-153">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="82d08-153">Minimum supported server</span></span><br/> | <span data-ttu-id="82d08-154">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="82d08-154">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="82d08-155">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="82d08-155">Namespace</span></span><br/>                | <span data-ttu-id="82d08-156">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="82d08-156">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="82d08-157">MOF</span><span class="sxs-lookup"><span data-stu-id="82d08-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="82d08-158"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="82d08-158"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="82d08-159">DLL</span><span class="sxs-lookup"><span data-stu-id="82d08-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="82d08-160"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="82d08-160"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82d08-161">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="82d08-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82d08-162">**\_DCOMApplicationSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="82d08-162">**Win32\_DCOMApplicationSetting**</span></span>](win32-dcomapplicationsetting.md)
</dt> <dt>

[<span data-ttu-id="82d08-163">**Costanti Privilege**</span><span class="sxs-lookup"><span data-stu-id="82d08-163">**Privilege Constants**</span></span>](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[<span data-ttu-id="82d08-164">Oggetti descrittore di sicurezza WMI</span><span class="sxs-lookup"><span data-stu-id="82d08-164">WMI Security Descriptor Objects</span></span>](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[<span data-ttu-id="82d08-165">Modifica della sicurezza di accesso per gli oggetti a protezione diretta</span><span class="sxs-lookup"><span data-stu-id="82d08-165">Changing Access Security on Securable Objects</span></span>](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> </dl>

 

