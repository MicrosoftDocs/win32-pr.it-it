---
description: "WMI include costanti di sicurezza usate per il controllo dell'accesso allo spazio dei nomi da \\_ \\_ SystemSecurity:: GetCallerAccessRights."
ms.assetid: 2e905078-d510-4417-8acb-a6ff535d9d0b
ms.tgt_platform: multiple
title: Costanti dei diritti di accesso allo spazio dei nomi (Wbemcli. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WBEM_ENABLE
- WBEM_METHOD_EXECUTE
- WBEM_FULL_WRITE_REP
- WBEM_PARTIAL_WRITE_REP
- WBEM_WRITE_PROVIDER
- WBEM_REMOTE_ACCESS
api_type:
- HeaderDef
api_location:
- Wbemcli.h
ms.openlocfilehash: 469e036b7cd385fa2ac2bae23e0da081288b536b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049342"
---
# <a name="namespace-access-rights-constants"></a><span data-ttu-id="1b68c-103">Costanti dei diritti di accesso allo spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="1b68c-103">Namespace Access Rights Constants</span></span>

<span data-ttu-id="1b68c-104">WMI include costanti di sicurezza usate per il controllo dell'accesso allo spazio dei nomi da [**\_ \_ SystemSecurity:: GetCallerAccessRights**](--systemsecurity-getcalleraccessrights.md).</span><span class="sxs-lookup"><span data-stu-id="1b68c-104">WMI has security constants used for namespace access checking by [**\_\_SystemSecurity::GetCallerAccessRights**](--systemsecurity-getcalleraccessrights.md).</span></span> <span data-ttu-id="1b68c-105">Per informazioni di sicurezza sugli elenchi di controllo di accesso (ACL, DACL o SACL), vedere [elenchi di controllo di accesso (ACL)](/windows/desktop/SecAuthZ/access-control-lists) e [**diritti di accesso standard**](/windows/desktop/SecAuthZ/standard-access-rights).</span><span class="sxs-lookup"><span data-stu-id="1b68c-105">For security information about access control lists (ACLs, DACLs, or SACLs), see [Access Control Lists (ACLs)](/windows/desktop/SecAuthZ/access-control-lists) and [**Standard Access Rights**](/windows/desktop/SecAuthZ/standard-access-rights).</span></span> <span data-ttu-id="1b68c-106">Queste costanti sono definite nell'enumerazione **flag di \_ sicurezza \_ WBEM** .</span><span class="sxs-lookup"><span data-stu-id="1b68c-106">These constants are defined in the **WBEM\_SECURITY\_FLAGS** enumeration.</span></span>

<dl> <dt>

<span data-ttu-id="1b68c-107"><span id="WBEM_ENABLE"></span><span id="wbem_enable"></span>**\_Abilitazione di WBEM**</span><span class="sxs-lookup"><span data-stu-id="1b68c-107"><span id="WBEM_ENABLE"></span><span id="wbem_enable"></span>**WBEM\_ENABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b68c-108">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="1b68c-108">1 (0x1)</span></span>
</dt> <dt>



<span data-ttu-id="1b68c-109">Abilita l'account e concede le autorizzazioni di lettura dell'utente.</span><span class="sxs-lookup"><span data-stu-id="1b68c-109">Enables the account and grants the user read permissions.</span></span> <span data-ttu-id="1b68c-110">Si tratta di un diritto di accesso predefinito per tutti gli utenti e corrisponde all'autorizzazione Abilita account per la scheda sicurezza del [*controllo WMI*](gloss-w.md).</span><span class="sxs-lookup"><span data-stu-id="1b68c-110">This is a default access right for all users and corresponds to the Enable Account permission on the Security tab of the [*WMI Control*](gloss-w.md).</span></span> <span data-ttu-id="1b68c-111">Per ulteriori informazioni, vedere [impostazione della sicurezza dello spazio dei nomi con il controllo WMI](setting-namespace-security-with-the-wmi-control.md).</span><span class="sxs-lookup"><span data-stu-id="1b68c-111">For more information, see [Setting Namespace Security with the WMI Control](setting-namespace-security-with-the-wmi-control.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b68c-112"><span id="WBEM_METHOD_EXECUTE"></span><span id="wbem_method_execute"></span>**\_esecuzione del metodo WBEM \_**</span><span class="sxs-lookup"><span data-stu-id="1b68c-112"><span id="WBEM_METHOD_EXECUTE"></span><span id="wbem_method_execute"></span>**WBEM\_METHOD\_EXECUTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b68c-113">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="1b68c-113">2 (0x2)</span></span>
</dt> <dt>



<span data-ttu-id="1b68c-114">Consente l'esecuzione di metodi.</span><span class="sxs-lookup"><span data-stu-id="1b68c-114">Allows the execution of methods.</span></span> <span data-ttu-id="1b68c-115">I provider possono eseguire ulteriori controlli di accesso.</span><span class="sxs-lookup"><span data-stu-id="1b68c-115">Providers can perform additional access checks.</span></span> <span data-ttu-id="1b68c-116">Si tratta di un diritto di accesso predefinito per tutti gli utenti e corrisponde all'autorizzazione Execute Methods nella scheda sicurezza del controllo WMI.</span><span class="sxs-lookup"><span data-stu-id="1b68c-116">This is a default access right for all users and corresponds to the Execute Methods permission on the Security tab of the WMI Control.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b68c-117"><span id="WBEM_FULL_WRITE_REP"></span><span id="wbem_full_write_rep"></span>**\_ \_ Rep scrittura completa \_ WBEM**</span><span class="sxs-lookup"><span data-stu-id="1b68c-117"><span id="WBEM_FULL_WRITE_REP"></span><span id="wbem_full_write_rep"></span>**WBEM\_FULL\_WRITE\_REP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b68c-118">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="1b68c-118">4 (0x4)</span></span>
</dt> <dt>



<span data-ttu-id="1b68c-119">Consente a un account utente di scrivere nelle classi del repository WMI e delle istanze di.</span><span class="sxs-lookup"><span data-stu-id="1b68c-119">Allows a user account to write to classes in the WMI repository as well as instances.</span></span> <span data-ttu-id="1b68c-120">Un utente non può scrivere in classi di sistema.</span><span class="sxs-lookup"><span data-stu-id="1b68c-120">A user cannot write to system classes.</span></span> <span data-ttu-id="1b68c-121">Solo i membri del gruppo Administrators dispongono di questa autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="1b68c-121">Only members of the Administrators group have this permission.</span></span> <span data-ttu-id="1b68c-122">**WBEM \_ Il \_ \_ rep di scrittura completo** corrisponde all'autorizzazione di scrittura completa nella scheda sicurezza del controllo WMI.</span><span class="sxs-lookup"><span data-stu-id="1b68c-122">**WBEM\_FULL\_WRITE\_REP** corresponds to the Full Write permission on the Security tab of the WMI Control.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b68c-123"><span id="WBEM_PARTIAL_WRITE_REP"></span><span id="wbem_partial_write_rep"></span>**\_ \_ Rep scrittura parziale \_ WBEM**</span><span class="sxs-lookup"><span data-stu-id="1b68c-123"><span id="WBEM_PARTIAL_WRITE_REP"></span><span id="wbem_partial_write_rep"></span>**WBEM\_PARTIAL\_WRITE\_REP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b68c-124">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="1b68c-124">8 (0x8)</span></span>
</dt> <dt>



<span data-ttu-id="1b68c-125">Consente di scrivere i dati solo nelle istanze, non nelle classi.</span><span class="sxs-lookup"><span data-stu-id="1b68c-125">Allows you to write data to instances only, not classes.</span></span> <span data-ttu-id="1b68c-126">Un utente non può scrivere classi nel [*repository WMI*](gloss-w.md).</span><span class="sxs-lookup"><span data-stu-id="1b68c-126">A user cannot write classes to the [*WMI repository*](gloss-w.md).</span></span> <span data-ttu-id="1b68c-127">Solo i membri del gruppo Administrators dispongono di questo diritto.</span><span class="sxs-lookup"><span data-stu-id="1b68c-127">Only members of the Administrators group have this right.</span></span> <span data-ttu-id="1b68c-128">**WBEM \_ Il \_ \_ rep di scrittura parziale** corrisponde all'autorizzazione di scrittura parziale nella scheda sicurezza del controllo WMI.</span><span class="sxs-lookup"><span data-stu-id="1b68c-128">**WBEM\_PARTIAL\_WRITE\_REP** corresponds to the Partial Write permission on the Security tab of the WMI Control.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b68c-129"><span id="WBEM_WRITE_PROVIDER"></span><span id="wbem_write_provider"></span>**\_provider di scrittura WBEM \_**</span><span class="sxs-lookup"><span data-stu-id="1b68c-129"><span id="WBEM_WRITE_PROVIDER"></span><span id="wbem_write_provider"></span>**WBEM\_WRITE\_PROVIDER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b68c-130">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="1b68c-130">16 (0x10)</span></span>
</dt> <dt>



<span data-ttu-id="1b68c-131">Consente di scrivere classi e istanze nei provider.</span><span class="sxs-lookup"><span data-stu-id="1b68c-131">Allows writing classes and instances to providers.</span></span> <span data-ttu-id="1b68c-132">Si noti che i provider possono eseguire ulteriori controlli di accesso durante la rappresentazione di un utente.</span><span class="sxs-lookup"><span data-stu-id="1b68c-132">Note that providers can do additional access checks when impersonating a user.</span></span> <span data-ttu-id="1b68c-133">Si tratta di un diritto di accesso predefinito per tutti gli utenti e corrisponde all'autorizzazione di scrittura del provider nella scheda sicurezza del controllo WMI.</span><span class="sxs-lookup"><span data-stu-id="1b68c-133">This is a default access right for all users and corresponds to the Provider Write permission on the Security tab of the WMI Control.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b68c-134"><span id="WBEM_REMOTE_ACCESS"></span><span id="wbem_remote_access"></span>**\_accesso remoto \_ WBEM**</span><span class="sxs-lookup"><span data-stu-id="1b68c-134"><span id="WBEM_REMOTE_ACCESS"></span><span id="wbem_remote_access"></span>**WBEM\_REMOTE\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b68c-135">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="1b68c-135">32 (0x20)</span></span>
</dt> <dt>



<span data-ttu-id="1b68c-136">Consente a un account utente di eseguire in modalità remota qualsiasi operazione consentita dalle autorizzazioni descritte in precedenza.</span><span class="sxs-lookup"><span data-stu-id="1b68c-136">Allows a user account to remotely perform any operations allowed by the permissions described above.</span></span> <span data-ttu-id="1b68c-137">Solo i membri del gruppo Administrators dispongono di questo diritto.</span><span class="sxs-lookup"><span data-stu-id="1b68c-137">Only members of the Administrators group have this right.</span></span> <span data-ttu-id="1b68c-138">**WBEM \_ \_Accesso remoto** corrisponde all'autorizzazione Abilita remoto nella scheda sicurezza del controllo WMI.</span><span class="sxs-lookup"><span data-stu-id="1b68c-138">**WBEM\_REMOTE\_ACCESS** corresponds to the Remote Enable permission on the Security tab of the WMI Control.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1b68c-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1b68c-139">Requirements</span></span>



| <span data-ttu-id="1b68c-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b68c-140">Requirement</span></span> | <span data-ttu-id="1b68c-141">Valore</span><span class="sxs-lookup"><span data-stu-id="1b68c-141">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1b68c-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1b68c-142">Minimum supported client</span></span><br/> | <span data-ttu-id="1b68c-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1b68c-143">Windows Vista</span></span><br/>                                                             |
| <span data-ttu-id="1b68c-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1b68c-144">Minimum supported server</span></span><br/> | <span data-ttu-id="1b68c-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1b68c-145">Windows Server 2008</span></span><br/>                                                       |
| <span data-ttu-id="1b68c-146">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1b68c-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b68c-147"><dt>Wbemcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b68c-147"><dt>Wbemcli.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b68c-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1b68c-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b68c-149">Costanti di sicurezza WMI</span><span class="sxs-lookup"><span data-stu-id="1b68c-149">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> <dt>

[<span data-ttu-id="1b68c-150">Sicurezza degli spazi dei nomi WMI</span><span class="sxs-lookup"><span data-stu-id="1b68c-150">Securing WMI Namespaces</span></span>](securing-wmi-namespaces.md)
</dt> <dt>

[<span data-ttu-id="1b68c-151">Accesso agli spazi dei nomi WMI</span><span class="sxs-lookup"><span data-stu-id="1b68c-151">Access to WMI Namespaces</span></span>](access-to-wmi-namespaces.md)
</dt> <dt>

[<span data-ttu-id="1b68c-152">Oggetti descrittore di sicurezza WMI</span><span class="sxs-lookup"><span data-stu-id="1b68c-152">WMI Security Descriptor Objects</span></span>](wmi-security-descriptor-objects.md)
</dt> <dt>

[<span data-ttu-id="1b68c-153">Modifica della sicurezza di accesso per gli oggetti a protezione diretta</span><span class="sxs-lookup"><span data-stu-id="1b68c-153">Changing Access Security on Securable Objects</span></span>](changing-access-security-on-securable-objects.md)
</dt> </dl>

 

