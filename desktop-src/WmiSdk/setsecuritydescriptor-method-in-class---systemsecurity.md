---
description: Scrive una versione aggiornata del descrittore di sicurezza che controlla l'accesso allo spazio dei nomi WMI a cui si è connessi. Il descrittore di sicurezza è rappresentato da un'istanza di \_ \_ securityDescriptor.
ms.assetid: e92430fd-61b1-4986-88dc-b85f502f62e6
ms.tgt_platform: multiple
title: Metodo SetSecurityDescriptor della classe __SystemSecurity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.SetSecurityDescriptor
api_type:
- COM
api_location:
- All
ms.openlocfilehash: fcdc192801b839451cee256f57090780818d2046
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314578"
---
# <a name="setsecuritydescriptor-method-of-the-__systemsecurity-class"></a><span data-ttu-id="d8382-104">Metodo SetSecurityDescriptor della \_ \_ classe SystemSecurity</span><span class="sxs-lookup"><span data-stu-id="d8382-104">SetSecurityDescriptor method of the \_\_SystemSecurity class</span></span>

<span data-ttu-id="d8382-105">Il metodo [**SetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/setsecuritydescriptor-method-in-class-win32-printer) scrive una versione aggiornata del descrittore di sicurezza che controlla l'accesso allo spazio dei nomi WMI a cui si è connessi.</span><span class="sxs-lookup"><span data-stu-id="d8382-105">The [**SetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/setsecuritydescriptor-method-in-class-win32-printer) method writes an updated version of the security descriptor that controls access to the WMI namespace to which you are connected.</span></span> <span data-ttu-id="d8382-106">Il descrittore di sicurezza è rappresentato da un'istanza di [**\_ \_ securityDescriptor**](--securitydescriptor.md).</span><span class="sxs-lookup"><span data-stu-id="d8382-106">The security descriptor is represented by an instance of [**\_\_SecurityDescriptor**](--securitydescriptor.md).</span></span> <span data-ttu-id="d8382-107">Per ulteriori informazioni, vedere [modifica della sicurezza di accesso per gli oggetti a protezione diretta](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="d8382-107">For more information, see [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d8382-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d8382-108">Syntax</span></span>


```mof
uint32 SetSecurityDescriptor(
  [in] __SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a><span data-ttu-id="d8382-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="d8382-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8382-110">*Descrittore* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d8382-110">*Descriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8382-111">Descrittore di sicurezza associato allo spazio dei nomi WMI.</span><span class="sxs-lookup"><span data-stu-id="d8382-111">The security descriptor associated with the WMI Namespace.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8382-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d8382-112">Return value</span></span>

<span data-ttu-id="d8382-113">Restituisce uno dei valori elencati nell'elenco seguente o un valore diverso per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="d8382-113">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="d8382-114">Per ulteriori informazioni, vedere [codici restituiti WMI](wmi-return-codes.md) o [**WbemErrorEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="d8382-114">For more information, see [WMI Return Codes](wmi-return-codes.md) or [**WbemErrorEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

<dl> <dt>

<span data-ttu-id="d8382-115">**0**</span><span class="sxs-lookup"><span data-stu-id="d8382-115">**0**</span></span>
</dt> <dd>

<span data-ttu-id="d8382-116">Operazione completata.</span><span class="sxs-lookup"><span data-stu-id="d8382-116">Successful completion.</span></span>

</dd> <dt>

<span data-ttu-id="d8382-117">**2**</span><span class="sxs-lookup"><span data-stu-id="d8382-117">**2**</span></span>
</dt> <dd>

<span data-ttu-id="d8382-118">L'utente non ha accesso alle informazioni richieste.</span><span class="sxs-lookup"><span data-stu-id="d8382-118">The user does not have access to the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="d8382-119">**8**</span><span class="sxs-lookup"><span data-stu-id="d8382-119">**8**</span></span>
</dt> <dd>

<span data-ttu-id="d8382-120">Errore sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="d8382-120">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="d8382-121">**9**</span><span class="sxs-lookup"><span data-stu-id="d8382-121">**9**</span></span>
</dt> <dd>

<span data-ttu-id="d8382-122">L'utente non dispone di privilegi sufficienti per eseguire il metodo.</span><span class="sxs-lookup"><span data-stu-id="d8382-122">The user does not have adequate privileges to execute the method.</span></span>

</dd> <dt>

<span data-ttu-id="d8382-123">**21**</span><span class="sxs-lookup"><span data-stu-id="d8382-123">**21**</span></span>
</dt> <dd>

<span data-ttu-id="d8382-124">Un parametro specificato nella chiamata al metodo non è valido.</span><span class="sxs-lookup"><span data-stu-id="d8382-124">A parameter specified in the method call is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d8382-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="d8382-125">Remarks</span></span>

<span data-ttu-id="d8382-126">L' [**istanza Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) rappresenta un tipo di dati di [**\_ \_ controllo del descrittore di sicurezza**](/windows/desktop/SecAuthZ/security-descriptor-control) e contiene un elenco di controllo di [*accesso discrezionale*](/windows/desktop/SecGloss/d-gly) (DACL) e un elenco di controllo di accesso di [*sistema*](/windows/desktop/SecGloss/a-gly) (SACL).</span><span class="sxs-lookup"><span data-stu-id="d8382-126">The [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance represents a [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) data type and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) and a [*System Access Control List*](/windows/desktop/SecGloss/a-gly) (SACL).</span></span> <span data-ttu-id="d8382-127">Per altre informazioni, vedere [elenchi di controllo di accesso](/windows/desktop/SecAuthZ/access-control-lists).</span><span class="sxs-lookup"><span data-stu-id="d8382-127">For more information, see [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span></span>

<span data-ttu-id="d8382-128">Se **SeSecurityPrivilege** non viene concesso o abilitato quando si recupera un descrittore di sicurezza, nel descrittore di sicurezza restituito viene restituito solo l'elenco DACL.</span><span class="sxs-lookup"><span data-stu-id="d8382-128">If the **SeSecurityPrivilege** is not granted or enabled when getting a security descriptor, then only the DACL is returned in the returned security descriptor.</span></span> <span data-ttu-id="d8382-129">Per altre informazioni, vedere [**costanti Privilege**](privilege-constants.md) ed [esecuzione di operazioni con privilegi](executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="d8382-129">For more information, see [**Privilege Constants**](privilege-constants.md) and [Executing Privileged Operations](executing-privileged-operations.md).</span></span>

<span data-ttu-id="d8382-130">È possibile aggiornare sia l'elenco DACL che l'elenco SACL nell'istanza [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) quando si chiama questo metodo, ma è anche possibile aggiornare solo l'elenco DACL o solo il SACL.</span><span class="sxs-lookup"><span data-stu-id="d8382-130">You can update both the DACL and the SACL in the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance when calling this method, but you also can update only the DACL or only the SACL.</span></span>

<span data-ttu-id="d8382-131">I valori seguenti nel [**\_ \_ controllo descrittore di sicurezza**](/windows/desktop/SecAuthZ/security-descriptor-control) determinano se l'elenco DACL o il SACL o entrambi sono aggiornati.</span><span class="sxs-lookup"><span data-stu-id="d8382-131">The following values in [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) determine whether the DACL or the SACL or both are updated.</span></span>

-   <span data-ttu-id="d8382-132">**\_elenco DACL se \_ presente**</span><span class="sxs-lookup"><span data-stu-id="d8382-132">**SE\_DACL\_PRESENT**</span></span>

    <span data-ttu-id="d8382-133">Indica che l'elenco DACL deve essere aggiornato.</span><span class="sxs-lookup"><span data-stu-id="d8382-133">Indicates that the DACL should be updated.</span></span> <span data-ttu-id="d8382-134">Se non è impostato, WMI conserva il valore originale del DACL.</span><span class="sxs-lookup"><span data-stu-id="d8382-134">If this is not set then WMI preserves the original value of the DACL.</span></span>

-   <span data-ttu-id="d8382-135">**\_SACL se \_ presente**</span><span class="sxs-lookup"><span data-stu-id="d8382-135">**SE\_SACL\_PRESENT**</span></span>

    <span data-ttu-id="d8382-136">Indica che il SACL deve essere aggiornato.</span><span class="sxs-lookup"><span data-stu-id="d8382-136">Indicates that the SACL should be updated.</span></span> <span data-ttu-id="d8382-137">Se non è impostato, WMI conserva il valore originale del SACL.</span><span class="sxs-lookup"><span data-stu-id="d8382-137">If this is not set then WMI preserves the original value of the SACL.</span></span> <span data-ttu-id="d8382-138">Per aggiornare il SACL, per l'account deve essere abilitato il privilegio **SeSecurityPrivilege** .</span><span class="sxs-lookup"><span data-stu-id="d8382-138">To update the SACL, the account must have the **SeSecurityPrivilege** privilege enabled.</span></span> <span data-ttu-id="d8382-139">Per gli script, il nome del privilegio è **SeSecurityPrivilege**.</span><span class="sxs-lookup"><span data-stu-id="d8382-139">For scripting, the privilege name is **SeSecurityPrivilege**.</span></span> <span data-ttu-id="d8382-140">Per altre informazioni, vedere [**costanti Privilege**](privilege-constants.md).</span><span class="sxs-lookup"><span data-stu-id="d8382-140">For more information, see [**Privilege Constants**](privilege-constants.md).</span></span>

<span data-ttu-id="d8382-141">Se il Trustee del gruppo e le proprietà del trustee del proprietario non sono **null**, verranno aggiornati.</span><span class="sxs-lookup"><span data-stu-id="d8382-141">If the Group trustee and the Owner trustee properties are not **NULL**, then they are updated.</span></span> <span data-ttu-id="d8382-142">In caso contrario, WMI conserva i valori originali.</span><span class="sxs-lookup"><span data-stu-id="d8382-142">Otherwise, WMI preserves the original values.</span></span> <span data-ttu-id="d8382-143">Per ulteriori informazioni, vedere [oggetti del descrittore di sicurezza WMI](wmi-security-descriptor-objects.md).</span><span class="sxs-lookup"><span data-stu-id="d8382-143">For more information, see [WMI Security Descriptor Objects](wmi-security-descriptor-objects.md).</span></span>

<span data-ttu-id="d8382-144">Quando un nuovo SACL è **null** in una chiamata a questo metodo, il SACL del descrittore di sicurezza nell'oggetto a protezione diretta di destinazione viene lasciato invariato.</span><span class="sxs-lookup"><span data-stu-id="d8382-144">When a new SACL is **NULL** in a call this method, then the security descriptor SACL on the target securable object is left unchanged.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8382-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d8382-145">Requirements</span></span>



| <span data-ttu-id="d8382-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8382-146">Requirement</span></span> | <span data-ttu-id="d8382-147">Valore</span><span class="sxs-lookup"><span data-stu-id="d8382-147">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="d8382-148">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d8382-148">Minimum supported client</span></span><br/> | <span data-ttu-id="d8382-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d8382-149">Windows Vista</span></span><br/>       |
| <span data-ttu-id="d8382-150">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d8382-150">Minimum supported server</span></span><br/> | <span data-ttu-id="d8382-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d8382-151">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="d8382-152">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d8382-152">Namespace</span></span><br/>                | <span data-ttu-id="d8382-153">Tutti gli spazi dei nomi WMI</span><span class="sxs-lookup"><span data-stu-id="d8382-153">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="d8382-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d8382-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8382-155">**\_\_SystemSecurity**</span><span class="sxs-lookup"><span data-stu-id="d8382-155">**\_\_SystemSecurity**</span></span>](--systemsecurity.md)
</dt> <dt>

[<span data-ttu-id="d8382-156">Impostazione di descrittori di sicurezza spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d8382-156">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> </dl>

 

