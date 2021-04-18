---
description: Ottiene il descrittore di sicurezza per lo spazio dei nomi a cui è connesso l'utente. Questo metodo restituisce un descrittore di sicurezza in formato di matrice di byte binario. Se si scrive uno script, usare il metodo GetSecurityDescriptor.
ms.assetid: aeac1e7b-fcb8-4880-afd1-4950da37602b
ms.tgt_platform: multiple
title: Metodo ottenuto della classe __SystemSecurity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.GetSD
api_type:
- COM
api_location:
- All
ms.openlocfilehash: d471db22a9f15a38ab693ae72332e5e1893b5c55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313210"
---
# <a name="getsd-method-of-the-__systemsecurity-class"></a><span data-ttu-id="42b34-105">Metodo ottenuto della \_ \_ classe SystemSecurity</span><span class="sxs-lookup"><span data-stu-id="42b34-105">GetSD method of the \_\_SystemSecurity class</span></span>

<span data-ttu-id="42b34-106">Il metodo **getsd** ottiene il descrittore di sicurezza per lo spazio dei nomi a cui è connesso l'utente.</span><span class="sxs-lookup"><span data-stu-id="42b34-106">The **GetSD** method gets the security descriptor for the namespace to which the user is connected.</span></span> <span data-ttu-id="42b34-107">Questo metodo restituisce un descrittore di sicurezza in formato di matrice di byte binario.</span><span class="sxs-lookup"><span data-stu-id="42b34-107">This method returns a security descriptor in binary byte array format.</span></span> <span data-ttu-id="42b34-108">Se si scrive uno script, usare il metodo [**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md) .</span><span class="sxs-lookup"><span data-stu-id="42b34-108">If you are writing a script, use the [**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md) method.</span></span> <span data-ttu-id="42b34-109">Per ulteriori informazioni, vedere [protezione degli spazi dei nomi WMI](securing-wmi-namespaces.md) e [modifica della sicurezza di accesso per gli oggetti a protezione diretta](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="42b34-109">For more information, see [Securing WMI Namespaces](securing-wmi-namespaces.md) and [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span>

<span data-ttu-id="42b34-110">L'utente deve disporre dell' **autorizzazione \_ controllo lettura** .</span><span class="sxs-lookup"><span data-stu-id="42b34-110">The user must have the **READ\_CONTROL** permission.</span></span> <span data-ttu-id="42b34-111">Per impostazione predefinita, gli amministratori dispongono di tale autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="42b34-111">By default, administrators have that permission.</span></span> <span data-ttu-id="42b34-112">L'unica parte del descrittore di sicurezza effettivamente utilizzato è l'elenco di controllo di accesso discrezionale (DACL).</span><span class="sxs-lookup"><span data-stu-id="42b34-112">The only part of the security descriptor that is actually used is the discretionary access control list (DACL).</span></span> <span data-ttu-id="42b34-113">L'elenco DACL può contenere sia voci ACE ereditate che non ereditate.</span><span class="sxs-lookup"><span data-stu-id="42b34-113">The DACL can contain both inherited and non-inherited ACEs.</span></span> <span data-ttu-id="42b34-114">Sono consentite le voci ACE Deny e Allow.</span><span class="sxs-lookup"><span data-stu-id="42b34-114">Both deny and allow ACEs are permitted.</span></span>

<span data-ttu-id="42b34-115">Se si sta programmando in C++, è possibile modificare il descrittore di sicurezza binario usando [SDDL](/windows/desktop/SecAuthZ/security-descriptor-definition-language)e i metodi di conversione [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) e [**ConvertStringSecurityDescriptorToSecurityDescriptor ha**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora).</span><span class="sxs-lookup"><span data-stu-id="42b34-115">If you are programming in C++, you can manipulate the binary security descriptor using [SDDL](/windows/desktop/SecAuthZ/security-descriptor-definition-language), and the conversion methods [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) and [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora).</span></span>

## <a name="syntax"></a><span data-ttu-id="42b34-116">Sintassi</span><span class="sxs-lookup"><span data-stu-id="42b34-116">Syntax</span></span>


```mof
HRESULT GetSD(
  [out] uint8 SD[]
);
```



## <a name="parameters"></a><span data-ttu-id="42b34-117">Parametri</span><span class="sxs-lookup"><span data-stu-id="42b34-117">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42b34-118">*SD* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="42b34-118">*SD* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="42b34-119">Descrittore di sicurezza nel formato di matrice di byte binario.</span><span class="sxs-lookup"><span data-stu-id="42b34-119">Security descriptor in binary byte array format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42b34-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="42b34-120">Return value</span></span>

<span data-ttu-id="42b34-121">Questo metodo restituisce un valore **HRESULT** che indica lo stato della chiamata al metodo.</span><span class="sxs-lookup"><span data-stu-id="42b34-121">This method returns an **HRESULT** indicating the status of the method call.</span></span> <span data-ttu-id="42b34-122">Nell'elenco seguente sono elencati i valori restituiti che sono di importanza per **ottenere**.</span><span class="sxs-lookup"><span data-stu-id="42b34-122">The following list lists the return values that are of significance to **GetSD**.</span></span> <span data-ttu-id="42b34-123">Per gli script e le applicazioni Visual Basic, il risultato può essere ottenuto da [OutParameters. returnValue](parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="42b34-123">For scripting and Visual Basic applications, the result can be obtained from [OutParameters.ReturnValue](parsing-outparameters-objects.md).</span></span> <span data-ttu-id="42b34-124">Per altre informazioni, vedere [creazione di oggetti InParameters e analisi di oggetti OutParameters](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="42b34-124">For more information, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span>

<dl> <dt>

<span data-ttu-id="42b34-125">**\_OK**</span><span class="sxs-lookup"><span data-stu-id="42b34-125">**S\_OK**</span></span>
</dt> <dd>

<span data-ttu-id="42b34-126">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="42b34-126">Method executed successfully.</span></span>

</dd> <dt>

<span data-ttu-id="42b34-127">**accesso a WBEM \_ E \_ \_ negato**</span><span class="sxs-lookup"><span data-stu-id="42b34-127">**WBEM\_E\_ACCESS\_DENIED**</span></span>
</dt> <dd>

<span data-ttu-id="42b34-128">Il chiamante non dispone di diritti sufficienti per chiamare questo metodo.</span><span class="sxs-lookup"><span data-stu-id="42b34-128">Caller does not have sufficient rights to call this method.</span></span>

</dd> <dt>

<span data-ttu-id="42b34-129">**WBEM \_ E \_ metodo \_ disabilitato**</span><span class="sxs-lookup"><span data-stu-id="42b34-129">**WBEM\_E\_METHOD\_DISABLED**</span></span>
</dt> <dd>

<span data-ttu-id="42b34-130">Tentativo di eseguire questo metodo su un sistema non supportato.</span><span class="sxs-lookup"><span data-stu-id="42b34-130">Attempted to run this method on an unsupported system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="42b34-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="42b34-131">Remarks</span></span>

<span data-ttu-id="42b34-132">Per ulteriori informazioni sulla modifica della sicurezza dello spazio dei nomi a livello di programmazione o manuale, vedere [protezione degli spazi dei nomi WMI](securing-wmi-namespaces.md).</span><span class="sxs-lookup"><span data-stu-id="42b34-132">For more information about modifying namespace security programmatically or manually, see [Securing WMI Namespaces](securing-wmi-namespaces.md).</span></span>

## <a name="examples"></a><span data-ttu-id="42b34-133">Esempio</span><span class="sxs-lookup"><span data-stu-id="42b34-133">Examples</span></span>

<span data-ttu-id="42b34-134">Nello script seguente viene illustrato **come utilizzare il** metodo per ottenere il descrittore di sicurezza corrente per lo \\ spazio dei nomi Cimv2 radice e modificarlo nella matrice di byte visualizzata in **displayd**.</span><span class="sxs-lookup"><span data-stu-id="42b34-134">The following script shows you how to use **GetSD** to obtain the current security descriptor for the Root\\Cimv2 namespace and change it to the byte array shown in **DisplaySD**.</span></span>


```VB
Set objServices = GetObject("winmgmts:root\cimv2")
Set CimV2 = objServices.Get("__SystemSecurity=@")
ReturnValue = Cimv2.GetSD(arrSD)

If Err <> 0 Then
   WScript.Echo "Method returned error " & ReturnValue
End If

DisplaySD = "SD = {"
For I = Lbound(arrSD) To Ubound(arrSD)

   DisplaySD = DisplaySD & arrSD(I)

   If I <> Ubound(arrSD) Then
      DisplaySD = DisplaySD & ","
   End If

Next

DisplaySD = DisplaySD & "}"

WScript.Echo DisplaySD
```



## <a name="requirements"></a><span data-ttu-id="42b34-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="42b34-135">Requirements</span></span>



| <span data-ttu-id="42b34-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="42b34-136">Requirement</span></span> | <span data-ttu-id="42b34-137">Valore</span><span class="sxs-lookup"><span data-stu-id="42b34-137">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="42b34-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="42b34-138">Minimum supported client</span></span><br/> | <span data-ttu-id="42b34-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="42b34-139">Windows Vista</span></span><br/>       |
| <span data-ttu-id="42b34-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="42b34-140">Minimum supported server</span></span><br/> | <span data-ttu-id="42b34-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="42b34-141">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="42b34-142">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="42b34-142">Namespace</span></span><br/>                | <span data-ttu-id="42b34-143">Tutti gli spazi dei nomi WMI</span><span class="sxs-lookup"><span data-stu-id="42b34-143">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="42b34-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="42b34-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42b34-145">Classi di sistema WMI</span><span class="sxs-lookup"><span data-stu-id="42b34-145">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="42b34-146">**\_\_SystemSecurity**</span><span class="sxs-lookup"><span data-stu-id="42b34-146">**\_\_SystemSecurity**</span></span>](--systemsecurity.md)
</dt> <dt>

[<span data-ttu-id="42b34-147">Costanti di sicurezza WMI</span><span class="sxs-lookup"><span data-stu-id="42b34-147">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> <dt>

[<span data-ttu-id="42b34-148">**\_ACE Win32**</span><span class="sxs-lookup"><span data-stu-id="42b34-148">**Win32\_ACE**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[<span data-ttu-id="42b34-149">**\_\_SystemSecurity:: SetD**</span><span class="sxs-lookup"><span data-stu-id="42b34-149">**\_\_SystemSecurity::SetSD**</span></span>](--systemsecurity-setsd.md)
</dt> <dt>

[<span data-ttu-id="42b34-150">**Descrittore di sicurezza \_**</span><span class="sxs-lookup"><span data-stu-id="42b34-150">**Security\_Descriptor**</span></span>](/windows/desktop/api/winnt/ns-winnt-security_descriptor)
</dt> <dt>

[<span data-ttu-id="42b34-151">**\_SecurityDescriptor Win32**</span><span class="sxs-lookup"><span data-stu-id="42b34-151">**Win32\_SecurityDescriptor**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[<span data-ttu-id="42b34-152">Sicurezza degli spazi dei nomi WMI</span><span class="sxs-lookup"><span data-stu-id="42b34-152">Securing WMI Namespaces</span></span>](securing-wmi-namespaces.md)
</dt> </dl>

 

