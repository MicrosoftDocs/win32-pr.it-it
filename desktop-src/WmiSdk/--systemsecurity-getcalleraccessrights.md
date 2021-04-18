---
description: Imposta il parametro rights come bitmap con ogni bit corrispondente a un diritto di accesso.
ms.assetid: f28391a8-2b34-4234-bf1a-4688726b0b4b
ms.tgt_platform: multiple
title: Metodo GetCallerAccessRights della classe __SystemSecurity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.GetCallerAccessRights
api_type:
- COM
api_location:
- All
ms.openlocfilehash: c86ea3044411e33026ed6328fcfc227e615648b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315997"
---
# <a name="getcalleraccessrights-method-of-the-__systemsecurity-class"></a><span data-ttu-id="b28af-103">Metodo GetCallerAccessRights della \_ \_ classe SystemSecurity</span><span class="sxs-lookup"><span data-stu-id="b28af-103">GetCallerAccessRights method of the \_\_SystemSecurity class</span></span>

<span data-ttu-id="b28af-104">Il metodo **\_ \_ SystemSecurity:: GetCallerAccessRights** imposta il parametro *Rights* come bitmap con ogni bit corrispondente a un diritto di accesso.</span><span class="sxs-lookup"><span data-stu-id="b28af-104">The **\_\_SystemSecurity::GetCallerAccessRights** method sets the *rights* parameter as a bitmap with each bit corresponding to an access right.</span></span> <span data-ttu-id="b28af-105">Qualsiasi client può chiamare questo oggetto per determinare i diritti di cui dispone il client.</span><span class="sxs-lookup"><span data-stu-id="b28af-105">Any client can call this to determine which rights the client has.</span></span> <span data-ttu-id="b28af-106">Questo metodo è utile per i client che abilitano o disabilitano le funzionalità.</span><span class="sxs-lookup"><span data-stu-id="b28af-106">This method is useful for clients that enable or disable features.</span></span> <span data-ttu-id="b28af-107">Ad esempio, un'applicazione GUI potrebbe disabilitare un pulsante se l'utente attualmente connesso non dispone dei diritti di esecuzione del metodo.</span><span class="sxs-lookup"><span data-stu-id="b28af-107">For example, a GUI application might disable a button if the currently logged-on user does not have method execution rights.</span></span>

<span data-ttu-id="b28af-108">Qualsiasi client abilitato ha il diritto di chiamare **GetCallerAccessRights**, anche se tale client non dispone dei diritti generali di esecuzione del metodo.</span><span class="sxs-lookup"><span data-stu-id="b28af-108">Any enabled client has the right to call **GetCallerAccessRights**, even if that client does not have general method execution rights.</span></span>

## <a name="syntax"></a><span data-ttu-id="b28af-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b28af-109">Syntax</span></span>


```mof
HRESULT GetCallerAccessRights(
  [out] sint32 rights
);
```



## <a name="parameters"></a><span data-ttu-id="b28af-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="b28af-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b28af-111">*diritti* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="b28af-111">*rights* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b28af-112">Diritti di accesso del client.</span><span class="sxs-lookup"><span data-stu-id="b28af-112">Access rights of the client.</span></span> <span data-ttu-id="b28af-113">Per ulteriori informazioni, vedere [**\_ \_ SystemSecurity**](--systemsecurity.md) e le [costanti di sicurezza WMI](wmi-security-constants.md).</span><span class="sxs-lookup"><span data-stu-id="b28af-113">For more information, see [**\_\_SystemSecurity**](--systemsecurity.md) and [WMI Security Constants](wmi-security-constants.md).</span></span>

<dt>

<span id="WBEM_ENABLE"></span><span id="wbem_enable"></span>

<span data-ttu-id="b28af-114"><span id="WBEM_ENABLE"></span><span id="wbem_enable"></span>**WBEM \_ Abilita** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="b28af-114"><span id="WBEM_ENABLE"></span><span id="wbem_enable"></span>**WBEM\_ENABLE** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="b28af-115">Abilita l'account e concede le autorizzazioni di lettura dell'utente.</span><span class="sxs-lookup"><span data-stu-id="b28af-115">Enables the account and grants the user read permissions.</span></span> <span data-ttu-id="b28af-116">Questo è il diritto di accesso predefinito per tutti gli utenti.</span><span class="sxs-lookup"><span data-stu-id="b28af-116">This is the default access right for all users.</span></span>

</dd> <dt>

<span id="WBEM_METHOD_EXECUTE"></span><span id="wbem_method_execute"></span>

<span data-ttu-id="b28af-117"><span id="WBEM_METHOD_EXECUTE"></span><span id="wbem_method_execute"></span>**WBEM \_ METODO \_ Execute** (2 (0x2))</span><span class="sxs-lookup"><span data-stu-id="b28af-117"><span id="WBEM_METHOD_EXECUTE"></span><span id="wbem_method_execute"></span>**WBEM\_METHOD\_EXECUTE** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="b28af-118">Consente l'esecuzione di metodi.</span><span class="sxs-lookup"><span data-stu-id="b28af-118">Allows the execution of methods.</span></span>

> [!Note]  
> <span data-ttu-id="b28af-119">I provider possono eseguire ulteriori controlli di accesso.</span><span class="sxs-lookup"><span data-stu-id="b28af-119">Providers may perform additional access checks.</span></span>

 

</dd> <dt>

<span id="WBEM_FULL_WRITE_REP"></span><span id="wbem_full_write_rep"></span>

<span data-ttu-id="b28af-120"><span id="WBEM_FULL_WRITE_REP"></span><span id="wbem_full_write_rep"></span>**WBEM \_ \_ \_ Rep scrittura completa** (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="b28af-120"><span id="WBEM_FULL_WRITE_REP"></span><span id="wbem_full_write_rep"></span>**WBEM\_FULL\_WRITE\_REP** (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="b28af-121">Consente al chiamante, al contesto di sicurezza o all'utente di scrivere in classi e istanze ad eccezione delle classi di sistema.</span><span class="sxs-lookup"><span data-stu-id="b28af-121">Allows the caller, security context, or user to write to classes and instances except for system classes.</span></span>

</dd> <dt>

<span id="WBEM_PARTIAL_WRITE_REP"></span><span id="wbem_partial_write_rep"></span>

<span data-ttu-id="b28af-122"><span id="WBEM_PARTIAL_WRITE_REP"></span><span id="wbem_partial_write_rep"></span>**WBEM \_ \_ \_ Rep scrittura parziale** (8 (0x8))</span><span class="sxs-lookup"><span data-stu-id="b28af-122"><span id="WBEM_PARTIAL_WRITE_REP"></span><span id="wbem_partial_write_rep"></span>**WBEM\_PARTIAL\_WRITE\_REP** (8 (0x8))</span></span>


</dt> <dd>

<span data-ttu-id="b28af-123">Consente al chiamante, al contesto di sicurezza o all'utente di scrivere le istanze del provider ma non le classi statiche o le istanze statiche nel repository.</span><span class="sxs-lookup"><span data-stu-id="b28af-123">Allows the caller, security context, or user to write provider instances but not static classes or static instances to the repository.</span></span>

</dd> <dt>

<span id="WBEM_WRITE_PROVIDER"></span><span id="wbem_write_provider"></span>

<span data-ttu-id="b28af-124"><span id="WBEM_WRITE_PROVIDER"></span><span id="wbem_write_provider"></span>**WBEM \_ \_Provider di scrittura** (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="b28af-124"><span id="WBEM_WRITE_PROVIDER"></span><span id="wbem_write_provider"></span>**WBEM\_WRITE\_PROVIDER** (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="b28af-125">Consente al chiamante, al contesto di sicurezza o all'utente di scrivere classi e istanze nei provider.</span><span class="sxs-lookup"><span data-stu-id="b28af-125">Allows the caller, security context, or user to write classes and instances to providers.</span></span>

> [!Note]  
> <span data-ttu-id="b28af-126">I provider di rappresentazione possono eseguire ulteriori controlli di accesso.</span><span class="sxs-lookup"><span data-stu-id="b28af-126">Impersonating providers may do additional access checks.</span></span>

 

</dd> <dt>

<span id="WBEM_REMOTE_ACCESS"></span><span id="wbem_remote_access"></span>

<span data-ttu-id="b28af-127"><span id="WBEM_REMOTE_ACCESS"></span><span id="wbem_remote_access"></span>**WBEM \_ \_Accesso remoto** (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="b28af-127"><span id="WBEM_REMOTE_ACCESS"></span><span id="wbem_remote_access"></span>**WBEM\_REMOTE\_ACCESS** (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="b28af-128">Consente a un account utente di eseguire in modalità remota qualsiasi operazione consentita dalle autorizzazioni impostate da altri bit.</span><span class="sxs-lookup"><span data-stu-id="b28af-128">Allows a user account to remotely perform any operations allowed by the permissions set by other bits.</span></span>

</dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="b28af-129"><span id="READ_CONTROL"></span><span id="read_control"></span>**Leggi \_ CONTROLLO** (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="b28af-129"><span id="READ_CONTROL"></span><span id="read_control"></span>**READ\_CONTROL** (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="b28af-130">Consente l'accesso in lettura ai descrittori di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="b28af-130">Allows read access to the security descriptors.</span></span>

</dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="b28af-131"><span id="WRITE_DAC"></span><span id="write_dac"></span>**Scrivi \_ DAC** (262144 (0x40000))</span><span class="sxs-lookup"><span data-stu-id="b28af-131"><span id="WRITE_DAC"></span><span id="write_dac"></span>**WRITE\_DAC** (262144 (0x40000))</span></span>


</dt> <dd>

<span data-ttu-id="b28af-132">Consente l'accesso in scrittura agli elenchi di controllo di accesso discrezionale (DACL).</span><span class="sxs-lookup"><span data-stu-id="b28af-132">Allows write access to discretionary access control lists (DACL).</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b28af-133">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b28af-133">Return value</span></span>

<span data-ttu-id="b28af-134">Questo metodo restituisce un valore **HRESULT** che indica lo stato della chiamata al metodo.</span><span class="sxs-lookup"><span data-stu-id="b28af-134">This method returns an **HRESULT** that indicates the status of the method call.</span></span> <span data-ttu-id="b28af-135">Nell'elenco seguente sono elencati i valori restituiti significativi per [**Set9XUserList**](--systemsecurity-set9xuserlist.md).</span><span class="sxs-lookup"><span data-stu-id="b28af-135">The following list lists the return values that are of significance to [**Set9XUserList**](--systemsecurity-set9xuserlist.md).</span></span> <span data-ttu-id="b28af-136">Per gli script e le applicazioni Visual Basic, il risultato può essere ottenuto da [OutParameters. returnValue](parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="b28af-136">For scripting and Visual Basic applications, the result can be obtained from [OutParameters.ReturnValue](parsing-outparameters-objects.md).</span></span> <span data-ttu-id="b28af-137">Per altre informazioni, vedere [creazione di oggetti InParameters e analisi di oggetti OutParameters](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="b28af-137">For more information, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span>

<dl> <dt>

<span data-ttu-id="b28af-138">**WBEM \_ E \_ metodo \_ disabilitato**</span><span class="sxs-lookup"><span data-stu-id="b28af-138">**WBEM\_E\_METHOD\_DISABLED**</span></span>
</dt> <dd>

<span data-ttu-id="b28af-139">Questo metodo non è supportato nelle versioni supportate di Windows.</span><span class="sxs-lookup"><span data-stu-id="b28af-139">This method is not supported on supported versions of Windows.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b28af-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b28af-140">Requirements</span></span>



| <span data-ttu-id="b28af-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="b28af-141">Requirement</span></span> | <span data-ttu-id="b28af-142">Valore</span><span class="sxs-lookup"><span data-stu-id="b28af-142">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="b28af-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b28af-143">Minimum supported client</span></span><br/> | <span data-ttu-id="b28af-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b28af-144">Windows Vista</span></span><br/>       |
| <span data-ttu-id="b28af-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b28af-145">Minimum supported server</span></span><br/> | <span data-ttu-id="b28af-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b28af-146">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="b28af-147">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b28af-147">Namespace</span></span><br/>                | <span data-ttu-id="b28af-148">Tutti gli spazi dei nomi WMI</span><span class="sxs-lookup"><span data-stu-id="b28af-148">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="b28af-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b28af-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b28af-150">Classi di sistema WMI</span><span class="sxs-lookup"><span data-stu-id="b28af-150">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="b28af-151">**\_\_SystemSecurity**</span><span class="sxs-lookup"><span data-stu-id="b28af-151">**\_\_SystemSecurity**</span></span>](--systemsecurity.md)
</dt> <dt>

[<span data-ttu-id="b28af-152">**\_\_SystemSecurity:: GetSd**</span><span class="sxs-lookup"><span data-stu-id="b28af-152">**\_\_SystemSecurity::GetSD**</span></span>](--systemsecurity-getsd.md)
</dt> <dt>

[<span data-ttu-id="b28af-153">**\_\_SystemSecurity:: SetD**</span><span class="sxs-lookup"><span data-stu-id="b28af-153">**\_\_SystemSecurity::SetSD**</span></span>](--systemsecurity-setsd.md)
</dt> <dt>

[<span data-ttu-id="b28af-154">Costanti di sicurezza WMI</span><span class="sxs-lookup"><span data-stu-id="b28af-154">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> <dt>

[<span data-ttu-id="b28af-155">**\_ACE Win32**</span><span class="sxs-lookup"><span data-stu-id="b28af-155">**Win32\_ACE**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[<span data-ttu-id="b28af-156">**\_SecurityDescriptor Win32**</span><span class="sxs-lookup"><span data-stu-id="b28af-156">**Win32\_SecurityDescriptor**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[<span data-ttu-id="b28af-157">Sicurezza degli spazi dei nomi WMI</span><span class="sxs-lookup"><span data-stu-id="b28af-157">Securing WMI Namespaces</span></span>](securing-wmi-namespaces.md)
</dt> <dt>

<span data-ttu-id="b28af-158">Costanti di sicurezza WMI</span><span class="sxs-lookup"><span data-stu-id="b28af-158">WMI Security Constants</span></span>
</dt> </dl>

 

