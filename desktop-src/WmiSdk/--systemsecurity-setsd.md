---
description: Imposta il descrittore di sicurezza per lo spazio dei nomi a cui è connesso un utente. Questo metodo richiede un descrittore di sicurezza in formato di matrice di byte binario. Se si scrive uno script, usare il metodo SetSecurityDescriptor.
ms.assetid: 049f8722-1674-4c4f-9300-09b1cc1412fb
ms.tgt_platform: multiple
title: Metodo SetD della classe __SystemSecurity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.SetSD
api_type:
- COM
api_location:
- All
ms.openlocfilehash: 21f09a412a662cec8629fa9237d8dbb5902426c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313208"
---
# <a name="setsd-method-of-the-__systemsecurity-class"></a><span data-ttu-id="f0c06-105">Metodo SetD della \_ \_ classe SystemSecurity</span><span class="sxs-lookup"><span data-stu-id="f0c06-105">SetSD method of the \_\_SystemSecurity class</span></span>

<span data-ttu-id="f0c06-106">Il metodo **SetD** imposta il descrittore di sicurezza per lo spazio dei nomi a cui un utente è connesso.</span><span class="sxs-lookup"><span data-stu-id="f0c06-106">The **SetSD** method sets the security descriptor for the namespace to which a user is connected.</span></span> <span data-ttu-id="f0c06-107">Questo metodo richiede un descrittore di sicurezza in formato di matrice di byte binario.</span><span class="sxs-lookup"><span data-stu-id="f0c06-107">This method requires a security descriptor in binary byte array format.</span></span> <span data-ttu-id="f0c06-108">Se si scrive uno script, usare il metodo [**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class---systemsecurity.md) .</span><span class="sxs-lookup"><span data-stu-id="f0c06-108">If you are writing a script, use the [**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class---systemsecurity.md) method.</span></span> <span data-ttu-id="f0c06-109">Per ulteriori informazioni, vedere [protezione degli spazi dei nomi WMI](securing-wmi-namespaces.md) e [modifica della sicurezza di accesso per gli oggetti a protezione diretta](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="f0c06-109">For more information, see [Securing WMI Namespaces](securing-wmi-namespaces.md) and [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span>

<span data-ttu-id="f0c06-110">Se si sta programmando in C++, è possibile modificare il descrittore di sicurezza binario usando [SDDL](/windows/desktop/SecAuthZ/security-descriptor-definition-language)e i metodi di conversione [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) e [**ConvertStringSecurityDescriptorToSecurityDescriptor ha**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora).</span><span class="sxs-lookup"><span data-stu-id="f0c06-110">If you are programming in C++, you can manipulate the binary security descriptor using [SDDL](/windows/desktop/SecAuthZ/security-descriptor-definition-language), and the conversion methods [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) and [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora).</span></span>

<span data-ttu-id="f0c06-111">Un utente deve disporre dell'autorizzazione per la **scrittura dell' \_ applicazione livello dati** e, per impostazione predefinita, un amministratore dispone di tale autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="f0c06-111">A user must have the **WRITE\_DAC** permission, and by default, an administrator has that permission.</span></span> <span data-ttu-id="f0c06-112">L'unica parte del descrittore di sicurezza utilizzata è la voce di controllo di accesso (ACE) non ereditata nell'elenco di controllo di accesso discrezionale (DACL).</span><span class="sxs-lookup"><span data-stu-id="f0c06-112">The only part of the security descriptor that is used is the noninherited access control entry (ACE) in the discretionary access control list (DACL).</span></span> <span data-ttu-id="f0c06-113">Impostando il flag di **\_ ereditarietà del contenitore** nelle voci ACE, il descrittore di sicurezza interessa gli spazi dei nomi figlio.</span><span class="sxs-lookup"><span data-stu-id="f0c06-113">By setting the **CONTAINER\_INHERIT** flag in the ACEs, the security descriptor affects child namespaces.</span></span> <span data-ttu-id="f0c06-114">Sono consentite entrambe le voci ACE Allow e Deny.</span><span class="sxs-lookup"><span data-stu-id="f0c06-114">Both allow and deny ACEs are permitted.</span></span>

> [!Note]  
> <span data-ttu-id="f0c06-115">Poiché le voci ACE Deny e allow sono entrambe consentite in un DACL, l'ordine delle voci ACE è importante.</span><span class="sxs-lookup"><span data-stu-id="f0c06-115">Because deny and allow ACEs are both permitted in a DACL, the order of ACEs is important.</span></span> <span data-ttu-id="f0c06-116">Per ulteriori informazioni, vedere [ordinamento delle voci ACE in un DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).</span><span class="sxs-lookup"><span data-stu-id="f0c06-116">For more information, see [Ordering of ACEs in a DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="f0c06-117">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f0c06-117">Syntax</span></span>


```mof
HRESULT SetSD(
  [in] uint8 SD[]
);
```



## <a name="parameters"></a><span data-ttu-id="f0c06-118">Parametri</span><span class="sxs-lookup"><span data-stu-id="f0c06-118">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0c06-119">*SD* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f0c06-119">*SD* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0c06-120">Matrice di byte che costituisce il descrittore di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="f0c06-120">Byte array that makes up the security descriptor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0c06-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f0c06-121">Return value</span></span>

<span data-ttu-id="f0c06-122">Restituisce un valore **HRESULT** che indica lo stato di una chiamata al metodo.</span><span class="sxs-lookup"><span data-stu-id="f0c06-122">Returns an **HRESULT** that indicates the status of a method call.</span></span> <span data-ttu-id="f0c06-123">Per gli script e le applicazioni Visual Basic, il risultato può essere ottenuto da [OutParameters. returnValue](parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="f0c06-123">For scripting and Visual Basic applications, the result can be obtained from [OutParameters.ReturnValue](parsing-outparameters-objects.md).</span></span> <span data-ttu-id="f0c06-124">Per altre informazioni, vedere [creazione di oggetti InParameters e analisi di oggetti OutParameters](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="f0c06-124">For more information, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span>

<span data-ttu-id="f0c06-125">Nell'elenco seguente sono elencati i valori restituiti significativi per i **set**.</span><span class="sxs-lookup"><span data-stu-id="f0c06-125">The following list lists the return values that are significant to **SetSD**.</span></span>

<dl> <dt>

<span data-ttu-id="f0c06-126">**\_OK**</span><span class="sxs-lookup"><span data-stu-id="f0c06-126">**S\_OK**</span></span>
</dt> <dd>

<span data-ttu-id="f0c06-127">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="f0c06-127">Method executed successfully.</span></span>

</dd> <dt>

<span data-ttu-id="f0c06-128">**accesso a WBEM \_ E \_ \_ negato**</span><span class="sxs-lookup"><span data-stu-id="f0c06-128">**WBEM\_E\_ACCESS\_DENIED**</span></span>
</dt> <dd>

<span data-ttu-id="f0c06-129">Il chiamante non dispone di diritti sufficienti per chiamare questo metodo.</span><span class="sxs-lookup"><span data-stu-id="f0c06-129">Caller does not have sufficient rights to call this method.</span></span>

</dd> <dt>

<span data-ttu-id="f0c06-130">**WBEM \_ E \_ metodo \_ disabilitato**</span><span class="sxs-lookup"><span data-stu-id="f0c06-130">**WBEM\_E\_METHOD\_DISABLED**</span></span>
</dt> <dd>

<span data-ttu-id="f0c06-131">Tentativo di eseguire questo metodo su un sistema operativo che non lo supporta.</span><span class="sxs-lookup"><span data-stu-id="f0c06-131">Attempted to run this method on OS that does not support it.</span></span>

</dd> <dt>

<span data-ttu-id="f0c06-132">**\_oggetto WBEM E \_ non valido \_**</span><span class="sxs-lookup"><span data-stu-id="f0c06-132">**WBEM\_E\_INVALID\_OBJECT**</span></span>
</dt> <dd>

<span data-ttu-id="f0c06-133">SD non supera i test di validità di base.</span><span class="sxs-lookup"><span data-stu-id="f0c06-133">SD does not pass basic validity tests.</span></span>

</dd> <dt>

<span data-ttu-id="f0c06-134">**\_parametro WBEM E \_ non valido \_**</span><span class="sxs-lookup"><span data-stu-id="f0c06-134">**WBEM\_E\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="f0c06-135">SD non è valido a causa di uno dei seguenti elementi:</span><span class="sxs-lookup"><span data-stu-id="f0c06-135">SD is not valid due to one of the following:</span></span>

-   <span data-ttu-id="f0c06-136">DACL mancante.</span><span class="sxs-lookup"><span data-stu-id="f0c06-136">DACL is missing.</span></span>
-   <span data-ttu-id="f0c06-137">DACL non valido.</span><span class="sxs-lookup"><span data-stu-id="f0c06-137">DACL is not valid.</span></span>
-   <span data-ttu-id="f0c06-138">Per ACE è stato impostato il flag del Rep per la **\_ \_ \_ scrittura completa WBEM** e il flag **del \_ \_ provider** di scrittura WBEM **\_ parzialmente \_ \_** o WBEM non è impostato.</span><span class="sxs-lookup"><span data-stu-id="f0c06-138">ACE has the **WBEM\_FULL\_WRITE\_REP** flag set, and the **WBEM\_PARTIAL\_WRITE\_REP** or **WBEM\_WRITE\_PROVIDER** flag is not set.</span></span>
-   <span data-ttu-id="f0c06-139">Il flag ACE ereditato da ACE è impostato **\_ solo \_** se il **contenitore eredita il flag \_ \_ ACE** .</span><span class="sxs-lookup"><span data-stu-id="f0c06-139">ACE has the **INHERIT\_ONLY\_ACE** flag set without the **CONTAINER\_INHERIT\_ACE** flag.</span></span>
-   <span data-ttu-id="f0c06-140">Per ACE è impostato un bit di accesso sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="f0c06-140">ACE has an unknown access bit set.</span></span>
-   <span data-ttu-id="f0c06-141">La voce ACE contiene un flag impostato che non è presente nella tabella.</span><span class="sxs-lookup"><span data-stu-id="f0c06-141">ACE has a flag set that is not in the table.</span></span>
-   <span data-ttu-id="f0c06-142">ACE ha un tipo non presente nella tabella.</span><span class="sxs-lookup"><span data-stu-id="f0c06-142">ACE has a type that is not in the table.</span></span>
-   <span data-ttu-id="f0c06-143">Proprietario e gruppo mancanti da SD.</span><span class="sxs-lookup"><span data-stu-id="f0c06-143">The owner and group are missing from the SD.</span></span>

<span data-ttu-id="f0c06-144">Per ulteriori informazioni sui flag ACE (Access Control Entry), vedere [costanti di sicurezza WMI](wmi-security-constants.md).</span><span class="sxs-lookup"><span data-stu-id="f0c06-144">For more information about the access control entry (ACE) flags, see [WMI Security Constants](wmi-security-constants.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f0c06-145">Commenti</span><span class="sxs-lookup"><span data-stu-id="f0c06-145">Remarks</span></span>

<span data-ttu-id="f0c06-146">Per ulteriori informazioni sulla modifica della sicurezza dello spazio dei nomi a livello di programmazione o manuale, vedere [protezione degli spazi dei nomi WMI](securing-wmi-namespaces.md).</span><span class="sxs-lookup"><span data-stu-id="f0c06-146">For more information about modifying namespace security programmatically or manually, see [Securing WMI Namespaces](securing-wmi-namespaces.md).</span></span>

## <a name="examples"></a><span data-ttu-id="f0c06-147">Esempio</span><span class="sxs-lookup"><span data-stu-id="f0c06-147">Examples</span></span>

<span data-ttu-id="f0c06-148">Nello script seguente viene illustrato come utilizzare **SetD** per impostare il descrittore di sicurezza dello spazio dei nomi per lo spazio dei nomi radice e modificarlo nella matrice di byte mostrata in *strSD*.</span><span class="sxs-lookup"><span data-stu-id="f0c06-148">The following script shows how to use **SetSD** to set the namespace security descriptor for the root namespace and change it to the byte array shown in *strSD*.</span></span>


```VB
' Hard-coded security descriptor
strSD = array( 1, 0, 4,129,72, 0, 0, 0, _ 
              88, 0, 0,  0, 0, 0, 0, 0, _
              20, 0, 0,  0, 2, 0,52, 0, _
               2, 0, 0,  0, 0, 2,24, 0, _
              63, 0, 6,  0, 1, 2, 0, 0, _
               0, 0, 0,  5,32, 0, 0, 0, _
              32, 2, 0,  0, 0, 2,20, 0, _
              63, 0, 6,  0, 1, 1, 0, 0, _
               0, 0, 0,  1, 0, 0, 0, 0, _
               1, 2, 0,  0, 0, 0, 0, 5, _
              32, 0, 0,  0,32, 2, 0, 0, _
               1, 2, 0,  0, 0, 0, 0, 5, _
              32, 0, 0,  0,32, 2, 0, 0)

' Connect to WMI and the root namespace.
Set oSvc = CreateObject( _
                         "WbemScripting.SWbemLocator"). _
                         ConnectServer(,"Root\Cimv2")

' Get the single __SystemSecurity object in this namespace.
Set oSecurity = oSvc.Get("__SystemSecurity=@")

' Change the namespace security.
nReturn = oSecurity.SetSD(strSD)
WScript.Echo "ReturnValue " & nReturn
```



<span data-ttu-id="f0c06-149">Nell'esempio di codice C# riportato di seguito viene usato System. Security. AccessControl. RawSecurityDescriptor per enumerare, inserire e rimuovere nuovi oggetti CommonAce in RawSecurityDescriptor. DiscretionaryAcl, quindi convertirli nuovamente in una matrice di byte per salvarli tramite SetD.</span><span class="sxs-lookup"><span data-stu-id="f0c06-149">The following C# code sample uses the System.Security.AccessControl.RawSecurityDescriptor to enumerate, insert and remove new CommonAce objects in RawSecurityDescriptor.DiscretionaryAcl and then convert it back to an byte array to save it via SetSD.</span></span> <span data-ttu-id="f0c06-150">È possibile recuperare un oggetto SecurityIdentifier usando NTAccount e translate.</span><span class="sxs-lookup"><span data-stu-id="f0c06-150">An SecurityIdentifier can be retrieved by using NTAccount and Translate.</span></span>


```CSharp
 byte[] sdValueByteArray = new Byte[0];

            string accountName = "My User or Group";

            AceFlags aceFlags = AceFlags.ContainerInherit;

            int accessRights = 131107; // Search for Namespace Access Rights Constants and build an Flags enum

            RawSecurityDescriptor rawSecurityDescriptor = new RawSecurityDescriptor(sdValueByteArray, 0);

            NTAccount ntAccount = new NTAccount(accountName);

            IdentityReference identityReference = ntAccount.Translate(typeof(SecurityIdentifier));

            if (identityReference == null)

            {

                string message = string.Format("The IdentityReference of NTAccount '{0}' is null.", accountName);

                throw new Exception(message);

            }

            SecurityIdentifier securityIdentifier = identityReference as SecurityIdentifier;

            if (securityIdentifier == null)

            {

                string message = "The IdentityReference of NTAccount '{0}' is not an SecurityIdentifier.";

                throw new Exception(message);

            }

            CommonAce commonAce;

            foreach (GenericAce genericAce in rawSecurityDescriptor.DiscretionaryAcl)

            {

                commonAce = genericAce as CommonAce;

                if (commonAce == null)

                {

                    continue;

                }

                if (commonAce.SecurityIdentifier.Value.Equals(securityIdentifier.Value, StringComparison.OrdinalIgnoreCase))

                {

                    return;

                }

            }

            commonAce = new CommonAce(aceFlags, AceQualifier.AccessAllowed, (int)accessRights, securityIdentifier, false, null);

            rawSecurityDescriptor.DiscretionaryAcl.InsertAce(rawSecurityDescriptor.DiscretionaryAcl.Count, commonAce);

```



## <a name="requirements"></a><span data-ttu-id="f0c06-151">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f0c06-151">Requirements</span></span>



| <span data-ttu-id="f0c06-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0c06-152">Requirement</span></span> | <span data-ttu-id="f0c06-153">Valore</span><span class="sxs-lookup"><span data-stu-id="f0c06-153">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="f0c06-154">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f0c06-154">Minimum supported client</span></span><br/> | <span data-ttu-id="f0c06-155">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f0c06-155">Windows Vista</span></span><br/>       |
| <span data-ttu-id="f0c06-156">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f0c06-156">Minimum supported server</span></span><br/> | <span data-ttu-id="f0c06-157">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f0c06-157">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="f0c06-158">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f0c06-158">Namespace</span></span><br/>                | <span data-ttu-id="f0c06-159">Tutti gli spazi dei nomi WMI</span><span class="sxs-lookup"><span data-stu-id="f0c06-159">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="f0c06-160">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f0c06-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0c06-161">Classi di sistema WMI</span><span class="sxs-lookup"><span data-stu-id="f0c06-161">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="f0c06-162">**\_\_SystemSecurity**</span><span class="sxs-lookup"><span data-stu-id="f0c06-162">**\_\_SystemSecurity**</span></span>](--systemsecurity.md)
</dt> <dt>

[<span data-ttu-id="f0c06-163">**\_\_SystemSecurity:: GetSd**</span><span class="sxs-lookup"><span data-stu-id="f0c06-163">**\_\_SystemSecurity::GetSD**</span></span>](--systemsecurity-getsd.md)
</dt> <dt>

[<span data-ttu-id="f0c06-164">Costanti di sicurezza WMI</span><span class="sxs-lookup"><span data-stu-id="f0c06-164">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> <dt>

[<span data-ttu-id="f0c06-165">**\_ACE Win32**</span><span class="sxs-lookup"><span data-stu-id="f0c06-165">**Win32\_ACE**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[<span data-ttu-id="f0c06-166">**\_SecurityDescriptor Win32**</span><span class="sxs-lookup"><span data-stu-id="f0c06-166">**Win32\_SecurityDescriptor**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[<span data-ttu-id="f0c06-167">Sicurezza degli spazi dei nomi WMI</span><span class="sxs-lookup"><span data-stu-id="f0c06-167">Securing WMI Namespaces</span></span>](securing-wmi-namespaces.md)
</dt> </dl>

 

