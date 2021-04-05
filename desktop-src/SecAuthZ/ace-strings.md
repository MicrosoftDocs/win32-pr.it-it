---
description: Vengono illustrate le stringhe utilizzate in una voce di controllo di accesso.
ms.assetid: 82c99170-784b-4724-a25b-2f2e8a2e0225
title: Stringhe ACE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a35bde18a1ca3ac416faa42e3b693e26305beb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756186"
---
# <a name="ace-strings"></a><span data-ttu-id="ad1e9-103">Stringhe ACE</span><span class="sxs-lookup"><span data-stu-id="ad1e9-103">ACE Strings</span></span>

<span data-ttu-id="ad1e9-104">Il [linguaggio SDDL (Security Descriptor Definition Language](security-descriptor-definition-language.md) ) utilizza stringhe ACE nei componenti DACL e SACL di una stringa del [*descrittore di sicurezza*](/windows/desktop/SecGloss/s-gly) .</span><span class="sxs-lookup"><span data-stu-id="ad1e9-104">The [security descriptor definition language](security-descriptor-definition-language.md) (SDDL) uses ACE strings in the DACL and SACL components of a [*security descriptor*](/windows/desktop/SecGloss/s-gly) string.</span></span>

<span data-ttu-id="ad1e9-105">Come illustrato negli esempi di [formato della stringa del descrittore di sicurezza](security-descriptor-string-format.md) , ogni voce ACE in una stringa del descrittore di sicurezza è racchiusa tra parentesi.</span><span class="sxs-lookup"><span data-stu-id="ad1e9-105">As shown in the [Security Descriptor String Format](security-descriptor-string-format.md) examples, each ACE in a security descriptor string is enclosed in parentheses.</span></span> <span data-ttu-id="ad1e9-106">I campi della voce ACE sono nell'ordine seguente e sono separati da punti e virgola (;).</span><span class="sxs-lookup"><span data-stu-id="ad1e9-106">The fields of the ACE are in the following order and are separated by semicolons (;).</span></span>

> [!Note]  
> <span data-ttu-id="ad1e9-107">È disponibile un formato diverso per le [*voci di controllo di accesso*](/windows/desktop/SecGloss/a-gly) condizionale (ACE) rispetto ad altri tipi ACE.</span><span class="sxs-lookup"><span data-stu-id="ad1e9-107">There is a different format for conditional [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs) than other ACE types.</span></span> <span data-ttu-id="ad1e9-108">Per le voci ACE condizionali, vedere [Security Descriptor Definition Language per le ACE condizionali](security-descriptor-definition-language-for-conditional-aces-.md).</span><span class="sxs-lookup"><span data-stu-id="ad1e9-108">For conditional ACEs, see [Security Descriptor Definition Language for Conditional ACEs](security-descriptor-definition-language-for-conditional-aces-.md).</span></span>

 

``` syntax
ace_type;ace_flags;rights;object_guid;inherit_object_guid;account_sid;(resource_attribute)
```

## <a name="fields"></a><span data-ttu-id="ad1e9-109">Campi</span><span class="sxs-lookup"><span data-stu-id="ad1e9-109">Fields</span></span>

<dl> <dt>

<span data-ttu-id="ad1e9-110"><span id="ace_type"></span><span id="ACE_TYPE"></span>**\_tipo ACE**</span><span class="sxs-lookup"><span data-stu-id="ad1e9-110"><span id="ace_type"></span><span id="ACE_TYPE"></span>**ace\_type**</span></span>
</dt> <dd>

<span data-ttu-id="ad1e9-111">Stringa che indica il valore del membro **AceType** della struttura dell' [**\_ intestazione ACE**](/windows/desktop/api/Winnt/ns-winnt-ace_header) .</span><span class="sxs-lookup"><span data-stu-id="ad1e9-111">A string that indicates the value of the **AceType** member of the [**ACE\_HEADER**](/windows/desktop/api/Winnt/ns-winnt-ace_header) structure.</span></span> <span data-ttu-id="ad1e9-112">La stringa di tipo ACE può essere una delle stringhe seguenti definite in SDDL. h.</span><span class="sxs-lookup"><span data-stu-id="ad1e9-112">The ACE type string can be one of the following strings defined in Sddl.h.</span></span>



| <span data-ttu-id="ad1e9-113">Stringa di tipo ACE</span><span class="sxs-lookup"><span data-stu-id="ad1e9-113">ACE type string</span></span> | <span data-ttu-id="ad1e9-114">Costante in SDDL. h</span><span class="sxs-lookup"><span data-stu-id="ad1e9-114">Constant in Sddl.h</span></span>                      | <span data-ttu-id="ad1e9-115">Valore AceType</span><span class="sxs-lookup"><span data-stu-id="ad1e9-115">AceType value</span></span>                                                                                                                                                      |
|-----------------|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad1e9-116">"A"</span><span class="sxs-lookup"><span data-stu-id="ad1e9-116">"A"</span></span>             | <span data-ttu-id="ad1e9-117">\_accesso SDDL \_ consentito</span><span class="sxs-lookup"><span data-stu-id="ad1e9-117">SDDL\_ACCESS\_ALLOWED</span></span>                   | <span data-ttu-id="ad1e9-118">\_ \_ tipo ACE consentito per l'accesso \_</span><span class="sxs-lookup"><span data-stu-id="ad1e9-118">ACCESS\_ALLOWED\_ACE\_TYPE</span></span>                                                                                                                                         |
| <span data-ttu-id="ad1e9-119">"D"</span><span class="sxs-lookup"><span data-stu-id="ad1e9-119">"D"</span></span>             | <span data-ttu-id="ad1e9-120">\_accesso SDDL \_ negato</span><span class="sxs-lookup"><span data-stu-id="ad1e9-120">SDDL\_ACCESS\_DENIED</span></span>                    | <span data-ttu-id="ad1e9-121">\_ \_ tipo ACE accesso \_ negato</span><span class="sxs-lookup"><span data-stu-id="ad1e9-121">ACCESS\_DENIED\_ACE\_TYPE</span></span>                                                                                                                                          |
| <span data-ttu-id="ad1e9-122">OA</span><span class="sxs-lookup"><span data-stu-id="ad1e9-122">"OA"</span></span>            | <span data-ttu-id="ad1e9-123">\_ \_ accesso agli oggetti SDDL \_ consentito</span><span class="sxs-lookup"><span data-stu-id="ad1e9-123">SDDL\_OBJECT\_ACCESS\_ALLOWED</span></span>           | <span data-ttu-id="ad1e9-124">\_ \_ \_ tipo ACE oggetto consentito \_ Access</span><span class="sxs-lookup"><span data-stu-id="ad1e9-124">ACCESS\_ALLOWED\_OBJECT\_ACE\_TYPE</span></span>                                                                                                                                 |
| <span data-ttu-id="ad1e9-125">OD</span><span class="sxs-lookup"><span data-stu-id="ad1e9-125">"OD"</span></span>            | <span data-ttu-id="ad1e9-126">\_ \_ accesso agli oggetti SDDL \_ negato</span><span class="sxs-lookup"><span data-stu-id="ad1e9-126">SDDL\_OBJECT\_ACCESS\_DENIED</span></span>            | <span data-ttu-id="ad1e9-127">ACCESSO \_ negato \_ \_ tipo ACE \_ oggetto</span><span class="sxs-lookup"><span data-stu-id="ad1e9-127">ACCESS\_DENIED\_OBJECT\_ACE\_TYPE</span></span>                                                                                                                                  |
| <span data-ttu-id="ad1e9-128">Au</span><span class="sxs-lookup"><span data-stu-id="ad1e9-128">"AU"</span></span>            | <span data-ttu-id="ad1e9-129">\_controllo SDDL</span><span class="sxs-lookup"><span data-stu-id="ad1e9-129">SDDL\_AUDIT</span></span>                             | <span data-ttu-id="ad1e9-130">\_ \_ tipo ACE controllo \_ sistema</span><span class="sxs-lookup"><span data-stu-id="ad1e9-130">SYSTEM\_AUDIT\_ACE\_TYPE</span></span>                                                                                                                                           |
| <span data-ttu-id="ad1e9-131">"AL"</span><span class="sxs-lookup"><span data-stu-id="ad1e9-131">"AL"</span></span>            | <span data-ttu-id="ad1e9-132">\_allarme SDDL</span><span class="sxs-lookup"><span data-stu-id="ad1e9-132">SDDL\_ALARM</span></span>                             | <span data-ttu-id="ad1e9-133">\_ \_ tipo ACE allarme \_ sistema</span><span class="sxs-lookup"><span data-stu-id="ad1e9-133">SYSTEM\_ALARM\_ACE\_TYPE</span></span>                                                                                                                                           |
| <span data-ttu-id="ad1e9-134">UNITÀ organizzativa</span><span class="sxs-lookup"><span data-stu-id="ad1e9-134">"OU"</span></span>            | <span data-ttu-id="ad1e9-135">\_controllo oggetto \_ SDDL</span><span class="sxs-lookup"><span data-stu-id="ad1e9-135">SDDL\_OBJECT\_AUDIT</span></span>                     | <span data-ttu-id="ad1e9-136">\_ \_ \_ tipo ACE oggetto controllo \_ di sistema</span><span class="sxs-lookup"><span data-stu-id="ad1e9-136">SYSTEM\_AUDIT\_OBJECT\_ACE\_TYPE</span></span>                                                                                                                                   |
| <span data-ttu-id="ad1e9-137">OL</span><span class="sxs-lookup"><span data-stu-id="ad1e9-137">"OL"</span></span>            | <span data-ttu-id="ad1e9-138">\_allarme oggetto \_ SDDL</span><span class="sxs-lookup"><span data-stu-id="ad1e9-138">SDDL\_OBJECT\_ALARM</span></span>                     | <span data-ttu-id="ad1e9-139">\_ \_ \_ tipo ACE oggetto allarme \_ sistema</span><span class="sxs-lookup"><span data-stu-id="ad1e9-139">SYSTEM\_ALARM\_OBJECT\_ACE\_TYPE</span></span>                                                                                                                                   |
| <span data-ttu-id="ad1e9-140">ML</span><span class="sxs-lookup"><span data-stu-id="ad1e9-140">"ML"</span></span>            | <span data-ttu-id="ad1e9-141">\_etichetta SDDL obbligatoria \_</span><span class="sxs-lookup"><span data-stu-id="ad1e9-141">SDDL\_MANDATORY\_LABEL</span></span>                  | <span data-ttu-id="ad1e9-142">\_ \_ \_ tipo ACE etichetta obbligatoria \_ del sistema</span><span class="sxs-lookup"><span data-stu-id="ad1e9-142">SYSTEM\_MANDATORY\_LABEL\_ACE\_TYPE</span></span>                                                                                                                                |
| <span data-ttu-id="ad1e9-143">XA</span><span class="sxs-lookup"><span data-stu-id="ad1e9-143">"XA"</span></span>            | <span data-ttu-id="ad1e9-144">\_accesso callback \_ SDDL \_ consentito</span><span class="sxs-lookup"><span data-stu-id="ad1e9-144">SDDL\_CALLBACK\_ACCESS\_ALLOWED</span></span>         | <span data-ttu-id="ad1e9-145">ACCESSO \_ consentito \_ \_ tipo ACE \_ **di callback windows vista e Windows Server 2003:** non disponibile.</span><span class="sxs-lookup"><span data-stu-id="ad1e9-145">ACCESS\_ALLOWED\_CALLBACK\_ACE\_TYPE **Windows Vista and Windows Server 2003:** Not available.</span></span><br/>                                                           |
| <span data-ttu-id="ad1e9-146">XD</span><span class="sxs-lookup"><span data-stu-id="ad1e9-146">"XD"</span></span>            | <span data-ttu-id="ad1e9-147">\_accesso callback \_ SDDL \_ negato</span><span class="sxs-lookup"><span data-stu-id="ad1e9-147">SDDL\_CALLBACK\_ACCESS\_DENIED</span></span>          | <span data-ttu-id="ad1e9-148">ACCESSO \_ negato \_ \_ tipo ACE \_ **di callback windows vista e Windows Server 2003:** non disponibile.</span><span class="sxs-lookup"><span data-stu-id="ad1e9-148">ACCESS\_DENIED\_CALLBACK\_ACE\_TYPE **Windows Vista and Windows Server 2003:** Not available.</span></span><br/>                                                            |
| <span data-ttu-id="ad1e9-149">RA</span><span class="sxs-lookup"><span data-stu-id="ad1e9-149">"RA"</span></span>            | <span data-ttu-id="ad1e9-150">\_attributo risorsa \_ SDDL</span><span class="sxs-lookup"><span data-stu-id="ad1e9-150">SDDL\_RESOURCE\_ATTRIBUTE</span></span>               | <span data-ttu-id="ad1e9-151">\_ \_ Tipo ACE attributo risorsa di sistema \_ \_ **Windows Server 2008 R2, windows 7, Windows Server 2008, windows vista e Windows Server 2003:** non disponibile.</span><span class="sxs-lookup"><span data-stu-id="ad1e9-151">SYSTEM\_RESOURCE\_ATTRIBUTE\_ACE\_TYPE **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista and Windows Server 2003:** Not available.</span></span><br/> |
| <span data-ttu-id="ad1e9-152">SP</span><span class="sxs-lookup"><span data-stu-id="ad1e9-152">"SP"</span></span>            | <span data-ttu-id="ad1e9-153">\_ \_ ID criterio con ambito \_ SDDL</span><span class="sxs-lookup"><span data-stu-id="ad1e9-153">SDDL\_SCOPED\_POLICY\_ID</span></span>                | <span data-ttu-id="ad1e9-154">\_ \_ ID dei criteri con ambito di sistema \_ \_ \_ -tipo ACE **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista e Windows Server 2003:** non disponibile.</span><span class="sxs-lookup"><span data-stu-id="ad1e9-154">SYSTEM\_SCOPED\_POLICY\_ID\_ACE\_TYPE **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista and Windows Server 2003:** Not available.</span></span><br/>  |
| <span data-ttu-id="ad1e9-155">Xu</span><span class="sxs-lookup"><span data-stu-id="ad1e9-155">"XU"</span></span>            | <span data-ttu-id="ad1e9-156">\_controllo callback \_ SDDL</span><span class="sxs-lookup"><span data-stu-id="ad1e9-156">SDDL\_CALLBACK\_AUDIT</span></span>                   | <span data-ttu-id="ad1e9-157">\_ \_ Tipo ACE di callback controllo di sistema \_ \_ **Windows Server 2008 R2, windows 7, Windows Server 2008, windows vista e Windows Server 2003:** non disponibile.</span><span class="sxs-lookup"><span data-stu-id="ad1e9-157">SYSTEM\_AUDIT\_CALLBACK\_ACE\_TYPE **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista and Windows Server 2003:** Not available.</span></span><br/>     |
| <span data-ttu-id="ad1e9-158">ZA</span><span class="sxs-lookup"><span data-stu-id="ad1e9-158">"ZA"</span></span>            | <span data-ttu-id="ad1e9-159">\_ \_ accesso agli oggetti di callback SDDL \_ \_ consentito</span><span class="sxs-lookup"><span data-stu-id="ad1e9-159">SDDL\_CALLBACK\_OBJECT\_ACCESS\_ALLOWED</span></span> | <span data-ttu-id="ad1e9-160">ACCESSO \_ consentito \_ di \_ tipo ACE di CALLBACK \_ **Windows Server 2008 R2, windows 7, Windows Server 2008, windows vista e Windows Server 2003:** non disponibile.</span><span class="sxs-lookup"><span data-stu-id="ad1e9-160">ACCESS\_ALLOWED\_CALLBACK\_ACE\_TYPE **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista and Windows Server 2003:** Not available.</span></span><br/>   |



 

> [!Note]  
> <span data-ttu-id="ad1e9-161">Se **il \_ tipo ACE** è \_ \_ \_ un tipo ACE oggetto consentito \_ e nessun GUID **oggetto \_** né GUID **\_ \_ oggetto ereditano** un [**GUID**](/windows/win32/api/guiddef/ns-guiddef-guid) specificato, [**ConvertStringSecurityDescriptorToSecurityDescriptor ha**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) converte **il \_ tipo ACE** per accedere al \_ \_ tipo ACE consentito \_ .</span><span class="sxs-lookup"><span data-stu-id="ad1e9-161">If **ace\_type** is ACCESS\_ALLOWED\_OBJECT\_ACE\_TYPE and neither **object\_guid** nor **inherit\_object\_guid** has a [**GUID**](/windows/win32/api/guiddef/ns-guiddef-guid) specified, then [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) converts **ace\_type** to ACCESS\_ALLOWED\_ACE\_TYPE.</span></span>

 

</dd> <dt>

<span data-ttu-id="ad1e9-162"><span id="ace_flags"></span><span id="ACE_FLAGS"></span>**\_flag ACE**</span><span class="sxs-lookup"><span data-stu-id="ad1e9-162"><span id="ace_flags"></span><span id="ACE_FLAGS"></span>**ace\_flags**</span></span>
</dt> <dd>

<span data-ttu-id="ad1e9-163">Stringa che indica il valore del membro **AceFlags** della struttura dell' [**\_ intestazione ACE**](/windows/desktop/api/Winnt/ns-winnt-ace_header) .</span><span class="sxs-lookup"><span data-stu-id="ad1e9-163">A string that indicates the value of the **AceFlags** member of the [**ACE\_HEADER**](/windows/desktop/api/Winnt/ns-winnt-ace_header) structure.</span></span> <span data-ttu-id="ad1e9-164">La stringa di flag ACE può essere una concatenazione delle stringhe seguenti definite in SDDL. h.</span><span class="sxs-lookup"><span data-stu-id="ad1e9-164">The ACE flags string can be a concatenation of the following strings defined in Sddl.h.</span></span>



| <span data-ttu-id="ad1e9-165">Stringa flag ACE</span><span class="sxs-lookup"><span data-stu-id="ad1e9-165">ACE flags string</span></span> | <span data-ttu-id="ad1e9-166">Costante in SDDL. h</span><span class="sxs-lookup"><span data-stu-id="ad1e9-166">Constant in Sddl.h</span></span>       | <span data-ttu-id="ad1e9-167">Valore AceFlag</span><span class="sxs-lookup"><span data-stu-id="ad1e9-167">AceFlag value</span></span>                 |
|------------------|--------------------------|-------------------------------|
| <span data-ttu-id="ad1e9-168">Ci</span><span class="sxs-lookup"><span data-stu-id="ad1e9-168">"CI"</span></span>             | <span data-ttu-id="ad1e9-169">\_eredita il contenitore SDDL \_</span><span class="sxs-lookup"><span data-stu-id="ad1e9-169">SDDL\_CONTAINER\_INHERIT</span></span> | <span data-ttu-id="ad1e9-170">il contenitore \_ eredita \_ ACE</span><span class="sxs-lookup"><span data-stu-id="ad1e9-170">CONTAINER\_INHERIT\_ACE</span></span>       |
| <span data-ttu-id="ad1e9-171">OI</span><span class="sxs-lookup"><span data-stu-id="ad1e9-171">"OI"</span></span>             | <span data-ttu-id="ad1e9-172">\_oggetto SDDL \_ ereditato</span><span class="sxs-lookup"><span data-stu-id="ad1e9-172">SDDL\_OBJECT\_INHERIT</span></span>    | <span data-ttu-id="ad1e9-173">OGGETTO che \_ eredita \_ ACE</span><span class="sxs-lookup"><span data-stu-id="ad1e9-173">OBJECT\_INHERIT\_ACE</span></span>          |
| <span data-ttu-id="ad1e9-174">NP</span><span class="sxs-lookup"><span data-stu-id="ad1e9-174">"NP"</span></span>             | <span data-ttu-id="ad1e9-175">SDDL \_ senza \_ propagazione</span><span class="sxs-lookup"><span data-stu-id="ad1e9-175">SDDL\_NO\_PROPAGATE</span></span>      | <span data-ttu-id="ad1e9-176">Nessuna \_ propagazione \_ eredita \_ ACE</span><span class="sxs-lookup"><span data-stu-id="ad1e9-176">NO\_PROPAGATE\_INHERIT\_ACE</span></span>   |
| <span data-ttu-id="ad1e9-177">Io</span><span class="sxs-lookup"><span data-stu-id="ad1e9-177">"IO"</span></span>             | <span data-ttu-id="ad1e9-178">\_solo SDDL eredita \_</span><span class="sxs-lookup"><span data-stu-id="ad1e9-178">SDDL\_INHERIT\_ONLY</span></span>      | <span data-ttu-id="ad1e9-179">EREDITA \_ solo \_ ACE</span><span class="sxs-lookup"><span data-stu-id="ad1e9-179">INHERIT\_ONLY\_ACE</span></span>            |
| <span data-ttu-id="ad1e9-180">"ID"</span><span class="sxs-lookup"><span data-stu-id="ad1e9-180">"ID"</span></span>             | <span data-ttu-id="ad1e9-181">SDDL \_ ereditato</span><span class="sxs-lookup"><span data-stu-id="ad1e9-181">SDDL\_INHERITED</span></span>          | <span data-ttu-id="ad1e9-182">Ace EREDITAta \_</span><span class="sxs-lookup"><span data-stu-id="ad1e9-182">INHERITED\_ACE</span></span>                |
| <span data-ttu-id="ad1e9-183">SA</span><span class="sxs-lookup"><span data-stu-id="ad1e9-183">"SA"</span></span>             | <span data-ttu-id="ad1e9-184">\_controllo SDDL \_ riuscito</span><span class="sxs-lookup"><span data-stu-id="ad1e9-184">SDDL\_AUDIT\_SUCCESS</span></span>     | <span data-ttu-id="ad1e9-185">\_ \_ flag ACE di accesso riuscito \_</span><span class="sxs-lookup"><span data-stu-id="ad1e9-185">SUCCESSFUL\_ACCESS\_ACE\_FLAG</span></span> |
| <span data-ttu-id="ad1e9-186">FA</span><span class="sxs-lookup"><span data-stu-id="ad1e9-186">"FA"</span></span>             | <span data-ttu-id="ad1e9-187">\_errore di controllo SDDL \_</span><span class="sxs-lookup"><span data-stu-id="ad1e9-187">SDDL\_AUDIT\_FAILURE</span></span>     | <span data-ttu-id="ad1e9-188">\_ \_ flag ACE di accesso non riuscito \_</span><span class="sxs-lookup"><span data-stu-id="ad1e9-188">FAILED\_ACCESS\_ACE\_FLAG</span></span>     |



 

</dd> <dt>

<span data-ttu-id="ad1e9-189"><span id="rights"></span><span id="RIGHTS"></span>**diritti**</span><span class="sxs-lookup"><span data-stu-id="ad1e9-189"><span id="rights"></span><span id="RIGHTS"></span>**rights**</span></span>
</dt> <dd>

<span data-ttu-id="ad1e9-190">Stringa che indica i [diritti di accesso](access-rights-and-access-masks.md) controllati dalla voce ACE.</span><span class="sxs-lookup"><span data-stu-id="ad1e9-190">A string that indicates the [access rights](access-rights-and-access-masks.md) controlled by the ACE.</span></span> <span data-ttu-id="ad1e9-191">Questa stringa può essere una rappresentazione di stringa esadecimale dei diritti di accesso, ad esempio "0x7800003F", oppure può essere una concatenazione delle stringhe seguenti.</span><span class="sxs-lookup"><span data-stu-id="ad1e9-191">This string can be a hexadecimal string representation of the access rights, such as "0x7800003F", or it can be a concatenation of the following strings.</span></span>



### <a name="generic-access-rights"></a><span data-ttu-id="ad1e9-192">Diritti di accesso generici</span><span class="sxs-lookup"><span data-stu-id="ad1e9-192">Generic access rights</span></span>

| <span data-ttu-id="ad1e9-193">Stringa dei diritti di accesso</span><span class="sxs-lookup"><span data-stu-id="ad1e9-193">Access rights string</span></span> | <span data-ttu-id="ad1e9-194">Costante in SDDL. h</span><span class="sxs-lookup"><span data-stu-id="ad1e9-194">Constant in Sddl.h</span></span> | <span data-ttu-id="ad1e9-195">Valore di accesso a destra</span><span class="sxs-lookup"><span data-stu-id="ad1e9-195">Access right value</span></span> |
|----------------------|--------------------|--------------------|
| <span data-ttu-id="ad1e9-196">GA</span><span class="sxs-lookup"><span data-stu-id="ad1e9-196">"GA"</span></span>                 | <span data-ttu-id="ad1e9-197">\_ \_ tutti i Generic SDDL</span><span class="sxs-lookup"><span data-stu-id="ad1e9-197">SDDL\_GENERIC\_ALL</span></span> | <span data-ttu-id="ad1e9-198">tutti GENERIci \_</span><span class="sxs-lookup"><span data-stu-id="ad1e9-198">GENERIC\_ALL</span></span>       |
| <span data-ttu-id="ad1e9-199">GR</span><span class="sxs-lookup"><span data-stu-id="ad1e9-199">"GR"</span></span>                 | <span data-ttu-id="ad1e9-200">\_lettura generica SDDL \_</span><span class="sxs-lookup"><span data-stu-id="ad1e9-200">SDDL\_GENERIC\_READ</span></span> | <span data-ttu-id="ad1e9-201">lettura GENERIca \_</span><span class="sxs-lookup"><span data-stu-id="ad1e9-201">GENERIC\_READ</span></span>     |
| <span data-ttu-id="ad1e9-202">GW</span><span class="sxs-lookup"><span data-stu-id="ad1e9-202">"GW"</span></span>                 | <span data-ttu-id="ad1e9-203">\_scrittura generica SDDL \_</span><span class="sxs-lookup"><span data-stu-id="ad1e9-203">SDDL\_GENERIC\_WRITE</span></span> | <span data-ttu-id="ad1e9-204">scrittura GENERIca \_</span><span class="sxs-lookup"><span data-stu-id="ad1e9-204">GENERIC\_WRITE</span></span> |
| <span data-ttu-id="ad1e9-205">GX</span><span class="sxs-lookup"><span data-stu-id="ad1e9-205">"GX"</span></span>                 | <span data-ttu-id="ad1e9-206">\_esecuzione generica SDDL \_</span><span class="sxs-lookup"><span data-stu-id="ad1e9-206">SDDL\_GENERIC\_EXECUTE</span></span> | <span data-ttu-id="ad1e9-207">esecuzione GENERIca \_</span><span class="sxs-lookup"><span data-stu-id="ad1e9-207">GENERIC\_EXECUTE</span></span> |


### <a name="standard-access-rights"></a><span data-ttu-id="ad1e9-208">Diritti di accesso standard</span><span class="sxs-lookup"><span data-stu-id="ad1e9-208">Standard access rights</span></span>

| <span data-ttu-id="ad1e9-209">Stringa dei diritti di accesso</span><span class="sxs-lookup"><span data-stu-id="ad1e9-209">Access rights string</span></span> | <span data-ttu-id="ad1e9-210">Costante in SDDL. h</span><span class="sxs-lookup"><span data-stu-id="ad1e9-210">Constant in Sddl.h</span></span> | <span data-ttu-id="ad1e9-211">Valore di accesso a destra</span><span class="sxs-lookup"><span data-stu-id="ad1e9-211">Access right value</span></span> |
|----------------------|--------------------|--------------------|
| <span data-ttu-id="ad1e9-212">RC</span><span class="sxs-lookup"><span data-stu-id="ad1e9-212">"RC"</span></span>                 | <span data-ttu-id="ad1e9-213">\_controllo di lettura SDDL \_</span><span class="sxs-lookup"><span data-stu-id="ad1e9-213">SDDL\_READ\_CONTROL</span></span> | <span data-ttu-id="ad1e9-214">controllo di lettura \_</span><span class="sxs-lookup"><span data-stu-id="ad1e9-214">READ\_CONTROL</span></span>      |
| <span data-ttu-id="ad1e9-215">SD</span><span class="sxs-lookup"><span data-stu-id="ad1e9-215">"SD"</span></span>                 | <span data-ttu-id="ad1e9-216">\_eliminazione standard \_ SDDL</span><span class="sxs-lookup"><span data-stu-id="ad1e9-216">SDDL\_STANDARD\_DELETE</span></span> | <span data-ttu-id="ad1e9-217">DELETE</span><span class="sxs-lookup"><span data-stu-id="ad1e9-217">DELETE</span></span>          |
| <span data-ttu-id="ad1e9-218">WD</span><span class="sxs-lookup"><span data-stu-id="ad1e9-218">"WD"</span></span>                 | <span data-ttu-id="ad1e9-219">\_DAC scrittura \_ SDDL</span><span class="sxs-lookup"><span data-stu-id="ad1e9-219">SDDL\_WRITE\_DAC</span></span> | <span data-ttu-id="ad1e9-220">Scrivi \_ DAC</span><span class="sxs-lookup"><span data-stu-id="ad1e9-220">WRITE\_DAC</span></span>            |
| <span data-ttu-id="ad1e9-221">Wo</span><span class="sxs-lookup"><span data-stu-id="ad1e9-221">"WO"</span></span>                 | <span data-ttu-id="ad1e9-222">\_proprietario scrittura \_ SDDL</span><span class="sxs-lookup"><span data-stu-id="ad1e9-222">SDDL\_WRITE\_OWNER</span></span> | <span data-ttu-id="ad1e9-223">Scrivi \_ proprietario</span><span class="sxs-lookup"><span data-stu-id="ad1e9-223">WRITE\_OWNER</span></span>        |

### <a name="directory-service-object-access-rights"></a><span data-ttu-id="ad1e9-224">Diritti di accesso agli oggetti del servizio directory</span><span class="sxs-lookup"><span data-stu-id="ad1e9-224">Directory service object access rights</span></span>

| <span data-ttu-id="ad1e9-225">Stringa dei diritti di accesso</span><span class="sxs-lookup"><span data-stu-id="ad1e9-225">Access rights string</span></span> | <span data-ttu-id="ad1e9-226">Costante in SDDL. h</span><span class="sxs-lookup"><span data-stu-id="ad1e9-226">Constant in Sddl.h</span></span> | <span data-ttu-id="ad1e9-227">Valore di accesso a destra</span><span class="sxs-lookup"><span data-stu-id="ad1e9-227">Access right value</span></span> |
|----------------------|--------------------|--------------------|
| <span data-ttu-id="ad1e9-228">RP</span><span class="sxs-lookup"><span data-stu-id="ad1e9-228">"RP"</span></span>                 | <span data-ttu-id="ad1e9-229">\_proprietà di lettura SDDL \_</span><span class="sxs-lookup"><span data-stu-id="ad1e9-229">SDDL\_READ\_PROPERTY</span></span> | <span data-ttu-id="ad1e9-230">ADS \_ Rights \_ DS \_ Read \_ prop</span><span class="sxs-lookup"><span data-stu-id="ad1e9-230">ADS\_RIGHT\_DS\_READ\_PROP</span></span> |
| <span data-ttu-id="ad1e9-231">WP</span><span class="sxs-lookup"><span data-stu-id="ad1e9-231">"WP"</span></span>                 | <span data-ttu-id="ad1e9-232">\_Proprietà scrittura \_ SDDL</span><span class="sxs-lookup"><span data-stu-id="ad1e9-232">SDDL\_WRITE\_PROPERTY</span></span> | <span data-ttu-id="ad1e9-233">ADS \_ Rights \_ Write DS- \_ \_ prop</span><span class="sxs-lookup"><span data-stu-id="ad1e9-233">ADS\_RIGHT\_DS\_WRITE\_PROP</span></span> |
| <span data-ttu-id="ad1e9-234">CC</span><span class="sxs-lookup"><span data-stu-id="ad1e9-234">"CC"</span></span>                 | <span data-ttu-id="ad1e9-235">SDDL \_ Crea \_ figlio</span><span class="sxs-lookup"><span data-stu-id="ad1e9-235">SDDL\_CREATE\_CHILD</span></span> | <span data-ttu-id="ad1e9-236">ADS \_ Rights \_ DS \_ creazione \_ figlio</span><span class="sxs-lookup"><span data-stu-id="ad1e9-236">ADS\_RIGHT\_DS\_CREATE\_CHILD</span></span> |
| <span data-ttu-id="ad1e9-237">DC</span><span class="sxs-lookup"><span data-stu-id="ad1e9-237">"DC"</span></span>                 | <span data-ttu-id="ad1e9-238">\_eliminazione \_ elemento figlio SDDL</span><span class="sxs-lookup"><span data-stu-id="ad1e9-238">SDDL\_DELETE\_CHILD</span></span> | <span data-ttu-id="ad1e9-239">ADS \_ Rights \_ DS \_ Delete \_ figlio</span><span class="sxs-lookup"><span data-stu-id="ad1e9-239">ADS\_RIGHT\_DS\_DELETE\_CHILD</span></span> |
| <span data-ttu-id="ad1e9-240">LC</span><span class="sxs-lookup"><span data-stu-id="ad1e9-240">"LC"</span></span>                 | <span data-ttu-id="ad1e9-241">\_elenco \_ elementi figlio SDDL</span><span class="sxs-lookup"><span data-stu-id="ad1e9-241">SDDL\_LIST\_CHILDREN</span></span> | <span data-ttu-id="ad1e9-242">elenco degli annunci \_ giusti \_ ACTRL \_ DS \_</span><span class="sxs-lookup"><span data-stu-id="ad1e9-242">ADS\_RIGHT\_ACTRL\_DS\_LIST</span></span> |
| <span data-ttu-id="ad1e9-243">SW</span><span class="sxs-lookup"><span data-stu-id="ad1e9-243">"SW"</span></span>                 | <span data-ttu-id="ad1e9-244">\_scrittura automatica \_ SDDL</span><span class="sxs-lookup"><span data-stu-id="ad1e9-244">SDDL\_SELF\_WRITE</span></span>    | <span data-ttu-id="ad1e9-245">\_autonomi \_ DS \_ giusti</span><span class="sxs-lookup"><span data-stu-id="ad1e9-245">ADS\_RIGHT\_DS\_SELF</span></span> |
| <span data-ttu-id="ad1e9-246">LO</span><span class="sxs-lookup"><span data-stu-id="ad1e9-246">"LO"</span></span>                  | <span data-ttu-id="ad1e9-247">\_oggetto elenco \_ SDDL</span><span class="sxs-lookup"><span data-stu-id="ad1e9-247">SDDL\_LIST\_OBJECT</span></span> | <span data-ttu-id="ad1e9-248">\_ \_ \_ oggetto elenco DS destro \_ ADS</span><span class="sxs-lookup"><span data-stu-id="ad1e9-248">ADS\_RIGHT\_DS\_LIST\_OBJECT</span></span> |
| <span data-ttu-id="ad1e9-249">DT</span><span class="sxs-lookup"><span data-stu-id="ad1e9-249">"DT"</span></span>                 | <span data-ttu-id="ad1e9-250">\_Elimina \_ albero SDDL</span><span class="sxs-lookup"><span data-stu-id="ad1e9-250">SDDL\_DELETE\_TREE</span></span> | <span data-ttu-id="ad1e9-251">\_albero di \_ \_ eliminazione DS destro Ads \_</span><span class="sxs-lookup"><span data-stu-id="ad1e9-251">ADS\_RIGHT\_DS\_DELETE\_TREE</span></span> |
| <span data-ttu-id="ad1e9-252">CR</span><span class="sxs-lookup"><span data-stu-id="ad1e9-252">"CR"</span></span>                  | <span data-ttu-id="ad1e9-253">\_ \_ accesso al controllo SDDL</span><span class="sxs-lookup"><span data-stu-id="ad1e9-253">SDDL\_CONTROL\_ACCESS</span></span> | <span data-ttu-id="ad1e9-254">\_ \_ \_ accesso al controllo DS Rights Ads \_</span><span class="sxs-lookup"><span data-stu-id="ad1e9-254">ADS\_RIGHT\_DS\_CONTROL\_ACCESS</span></span> |

### <a name="file-access-rights"></a><span data-ttu-id="ad1e9-255">Diritti di accesso ai file</span><span class="sxs-lookup"><span data-stu-id="ad1e9-255">File access rights</span></span>

| <span data-ttu-id="ad1e9-256">Stringa dei diritti di accesso</span><span class="sxs-lookup"><span data-stu-id="ad1e9-256">Access rights string</span></span> | <span data-ttu-id="ad1e9-257">Costante in SDDL. h</span><span class="sxs-lookup"><span data-stu-id="ad1e9-257">Constant in Sddl.h</span></span> | <span data-ttu-id="ad1e9-258">Valore di accesso a destra</span><span class="sxs-lookup"><span data-stu-id="ad1e9-258">Access right value</span></span> |
|----------------------|--------------------|--------------------|
| <span data-ttu-id="ad1e9-259">FA</span><span class="sxs-lookup"><span data-stu-id="ad1e9-259">"FA"</span></span>                 | <span data-ttu-id="ad1e9-260">\_ \_ tutti i file SDDL</span><span class="sxs-lookup"><span data-stu-id="ad1e9-260">SDDL\_FILE\_ALL</span></span>    | <span data-ttu-id="ad1e9-261">\_accesso a tutti i file \_</span><span class="sxs-lookup"><span data-stu-id="ad1e9-261">FILE\_ALL\_ACCESS</span></span>   |
| <span data-ttu-id="ad1e9-262">FR</span><span class="sxs-lookup"><span data-stu-id="ad1e9-262">"FR"</span></span>                 | <span data-ttu-id="ad1e9-263">\_lettura file \_ SDDL</span><span class="sxs-lookup"><span data-stu-id="ad1e9-263">SDDL\_FILE\_READ</span></span>   | <span data-ttu-id="ad1e9-264">\_lettura file generica \_</span><span class="sxs-lookup"><span data-stu-id="ad1e9-264">FILE\_GENERIC\_READ</span></span> |
| <span data-ttu-id="ad1e9-265">FW</span><span class="sxs-lookup"><span data-stu-id="ad1e9-265">"FW"</span></span>                 | <span data-ttu-id="ad1e9-266">\_scrittura file \_ SDDL</span><span class="sxs-lookup"><span data-stu-id="ad1e9-266">SDDL\_FILE\_WRITE</span></span>  | <span data-ttu-id="ad1e9-267">\_scrittura generica file \_</span><span class="sxs-lookup"><span data-stu-id="ad1e9-267">FILE\_GENERIC\_WRITE</span></span> |
| <span data-ttu-id="ad1e9-268">FX</span><span class="sxs-lookup"><span data-stu-id="ad1e9-268">"FX"</span></span>                 | <span data-ttu-id="ad1e9-269">\_esecuzione file \_ SDDL</span><span class="sxs-lookup"><span data-stu-id="ad1e9-269">SDDL\_FILE\_EXECUTE</span></span> | <span data-ttu-id="ad1e9-270">\_esecuzione generica file \_</span><span class="sxs-lookup"><span data-stu-id="ad1e9-270">FILE\_GENERIC\_EXECUTE</span></span> |


### <a name="registry-key-access-rights"></a><span data-ttu-id="ad1e9-271">Diritti di accesso alla chiave del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="ad1e9-271">Registry key access rights</span></span>

| <span data-ttu-id="ad1e9-272">Stringa dei diritti di accesso</span><span class="sxs-lookup"><span data-stu-id="ad1e9-272">Access rights string</span></span> | <span data-ttu-id="ad1e9-273">Costante in SDDL. h</span><span class="sxs-lookup"><span data-stu-id="ad1e9-273">Constant in Sddl.h</span></span> | <span data-ttu-id="ad1e9-274">Valore di accesso a destra</span><span class="sxs-lookup"><span data-stu-id="ad1e9-274">Access right value</span></span> |
|----------------------|--------------------|--------------------|
| <span data-ttu-id="ad1e9-275">Ka</span><span class="sxs-lookup"><span data-stu-id="ad1e9-275">"KA"</span></span>                 | <span data-ttu-id="ad1e9-276">\_chiave SDDL \_ All</span><span class="sxs-lookup"><span data-stu-id="ad1e9-276">SDDL\_KEY\_ALL</span></span>     | <span data-ttu-id="ad1e9-277">CHIAVE \_ tutti gli \_ accessi</span><span class="sxs-lookup"><span data-stu-id="ad1e9-277">KEY\_ALL\_ACCESS</span></span>   |
| <span data-ttu-id="ad1e9-278">KR</span><span class="sxs-lookup"><span data-stu-id="ad1e9-278">"KR"</span></span>                 | <span data-ttu-id="ad1e9-279">\_lettura chiave \_ SDDL</span><span class="sxs-lookup"><span data-stu-id="ad1e9-279">SDDL\_KEY\_READ</span></span>    | <span data-ttu-id="ad1e9-280">\_lettura chiave</span><span class="sxs-lookup"><span data-stu-id="ad1e9-280">KEY\_READ</span></span>          |
| <span data-ttu-id="ad1e9-281">KW</span><span class="sxs-lookup"><span data-stu-id="ad1e9-281">"KW"</span></span>                 | <span data-ttu-id="ad1e9-282">\_scrittura chiave \_ SDDL</span><span class="sxs-lookup"><span data-stu-id="ad1e9-282">SDDL\_KEY\_WRITE</span></span>   | <span data-ttu-id="ad1e9-283">\_scrittura chiave</span><span class="sxs-lookup"><span data-stu-id="ad1e9-283">KEY\_WRITE</span></span>         |
| <span data-ttu-id="ad1e9-284">Kx</span><span class="sxs-lookup"><span data-stu-id="ad1e9-284">"KX"</span></span>                 | <span data-ttu-id="ad1e9-285">\_esecuzione della chiave SDDL \_</span><span class="sxs-lookup"><span data-stu-id="ad1e9-285">SDDL\_KEY\_EXECUTE</span></span> | <span data-ttu-id="ad1e9-286">esecuzione della chiave \_</span><span class="sxs-lookup"><span data-stu-id="ad1e9-286">KEY\_EXECUTE</span></span>       |

### <a name="mandatory-label-rights"></a><span data-ttu-id="ad1e9-287">Diritti etichetta obbligatoria</span><span class="sxs-lookup"><span data-stu-id="ad1e9-287">Mandatory label rights</span></span>

| <span data-ttu-id="ad1e9-288">Stringa dei diritti di accesso</span><span class="sxs-lookup"><span data-stu-id="ad1e9-288">Access rights string</span></span> | <span data-ttu-id="ad1e9-289">Costante in SDDL. h</span><span class="sxs-lookup"><span data-stu-id="ad1e9-289">Constant in Sddl.h</span></span> | <span data-ttu-id="ad1e9-290">Valore di accesso a destra</span><span class="sxs-lookup"><span data-stu-id="ad1e9-290">Access right value</span></span> |
|----------------------|--------------------|--------------------|
| <span data-ttu-id="ad1e9-291">Nr</span><span class="sxs-lookup"><span data-stu-id="ad1e9-291">"NR"</span></span>                 | <span data-ttu-id="ad1e9-292">SDDL \_ Nessuna \_ lettura \_</span><span class="sxs-lookup"><span data-stu-id="ad1e9-292">SDDL\_NO\_READ\_UP</span></span> | <span data-ttu-id="ad1e9-293">\_etichetta obbligatoria \_ sistema \_ senza \_ lettura \_</span><span class="sxs-lookup"><span data-stu-id="ad1e9-293">SYSTEM\_MANDATORY\_LABEL\_NO\_READ\_UP</span></span> |
| <span data-ttu-id="ad1e9-294">NW</span><span class="sxs-lookup"><span data-stu-id="ad1e9-294">"NW"</span></span>                 | <span data-ttu-id="ad1e9-295">SDDL \_ senza \_ scrittura \_</span><span class="sxs-lookup"><span data-stu-id="ad1e9-295">SDDL\_NO\_WRITE\_UP</span></span> | <span data-ttu-id="ad1e9-296">\_etichetta obbligatoria \_ sistema \_ senza \_ scrittura \_</span><span class="sxs-lookup"><span data-stu-id="ad1e9-296">SYSTEM\_MANDATORY\_LABEL\_NO\_WRITE\_UP</span></span> |
| <span data-ttu-id="ad1e9-297">NX</span><span class="sxs-lookup"><span data-stu-id="ad1e9-297">"NX"</span></span>                 | <span data-ttu-id="ad1e9-298">SDDL \_ Nessuna \_ esecuzione \_</span><span class="sxs-lookup"><span data-stu-id="ad1e9-298">SDDL\_NO\_EXECUTE\_UP</span></span> | <span data-ttu-id="ad1e9-299">\_etichetta obbligatoria del sistema \_ \_ Nessuna \_ esecuzione \_</span><span class="sxs-lookup"><span data-stu-id="ad1e9-299">SYSTEM\_MANDATORY\_LABEL\_NO\_EXECUTE\_UP</span></span> |
</dd> <dt>

<span data-ttu-id="ad1e9-300"><span id="object_guid"></span><span id="OBJECT_GUID"></span>**\_GUID oggetto**</span><span class="sxs-lookup"><span data-stu-id="ad1e9-300"><span id="object_guid"></span><span id="OBJECT_GUID"></span>**object\_guid**</span></span>
</dt> <dd>

<span data-ttu-id="ad1e9-301">Rappresentazione in forma di stringa di un GUID che indica il valore del membro **ObjectType** di una struttura Ace specifica dell'oggetto, ad esempio [**Access \_ allowed \_ Object \_ ACE**](/windows/desktop/api/Winnt/ns-winnt-access_allowed_object_ace).</span><span class="sxs-lookup"><span data-stu-id="ad1e9-301">A string representation of a GUID that indicates the value of the **ObjectType** member of an object-specific ACE structure, such as [**ACCESS\_ALLOWED\_OBJECT\_ACE**](/windows/desktop/api/Winnt/ns-winnt-access_allowed_object_ace).</span></span> <span data-ttu-id="ad1e9-302">La stringa GUID usa il formato restituito dalla funzione [**UuidToString**](/windows/desktop/api/rpcdce/nf-rpcdce-uuidtostring) .</span><span class="sxs-lookup"><span data-stu-id="ad1e9-302">The GUID string uses the format returned by the [**UuidToString**](/windows/desktop/api/rpcdce/nf-rpcdce-uuidtostring) function.</span></span>

<span data-ttu-id="ad1e9-303">Nella tabella seguente sono elencati alcuni GUID oggetto usati comunemente.</span><span class="sxs-lookup"><span data-stu-id="ad1e9-303">The following table lists some commonly used object GUIDs.</span></span>



| <span data-ttu-id="ad1e9-304">Diritti e GUID</span><span class="sxs-lookup"><span data-stu-id="ad1e9-304">Rights and GUID</span></span>                         | <span data-ttu-id="ad1e9-305">Autorizzazione</span><span class="sxs-lookup"><span data-stu-id="ad1e9-305">Permission</span></span>      |
|-----------------------------------------|-----------------|
| <span data-ttu-id="ad1e9-306">CR; ab721a53-1e2f-11D0-9819-00aa0040529b</span><span class="sxs-lookup"><span data-stu-id="ad1e9-306">CR;ab721a53-1e2f-11d0-9819-00aa0040529b</span></span> | <span data-ttu-id="ad1e9-307">Cambia password</span><span class="sxs-lookup"><span data-stu-id="ad1e9-307">Change password</span></span> |
| <span data-ttu-id="ad1e9-308">CR; 00299570-246d-11D0-A768-00aa006e0529</span><span class="sxs-lookup"><span data-stu-id="ad1e9-308">CR;00299570-246d-11d0-a768-00aa006e0529</span></span> | <span data-ttu-id="ad1e9-309">Reimposta password</span><span class="sxs-lookup"><span data-stu-id="ad1e9-309">Reset password</span></span>  |



 

</dd> <dt>

<span data-ttu-id="ad1e9-310"><span id="inherit_object_guid"></span><span id="INHERIT_OBJECT_GUID"></span>**eredita \_ \_ GUID oggetto**</span><span class="sxs-lookup"><span data-stu-id="ad1e9-310"><span id="inherit_object_guid"></span><span id="INHERIT_OBJECT_GUID"></span>**inherit\_object\_guid**</span></span>
</dt> <dd>

<span data-ttu-id="ad1e9-311">Rappresentazione in forma di stringa di un GUID che indica il valore del membro **InheritedObjectType** di una struttura Ace specifica dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ad1e9-311">A string representation of a GUID that indicates the value of the **InheritedObjectType** member of an object-specific ACE structure.</span></span> <span data-ttu-id="ad1e9-312">La stringa GUID usa il formato [**UuidToString**](/windows/desktop/api/rpcdce/nf-rpcdce-uuidtostring) .</span><span class="sxs-lookup"><span data-stu-id="ad1e9-312">The GUID string uses the [**UuidToString**](/windows/desktop/api/rpcdce/nf-rpcdce-uuidtostring) format.</span></span>

</dd> <dt>

<span data-ttu-id="ad1e9-313"><span id="account_sid"></span><span id="ACCOUNT_SID"></span>**SID dell'account \_**</span><span class="sxs-lookup"><span data-stu-id="ad1e9-313"><span id="account_sid"></span><span id="ACCOUNT_SID"></span>**account\_sid**</span></span>
</dt> <dd>

<span data-ttu-id="ad1e9-314">[Stringa SID](sid-strings.md) che identifica il [trustee](trustees.md) della voce ACE.</span><span class="sxs-lookup"><span data-stu-id="ad1e9-314">[SID string](sid-strings.md) that identifies the [trustee](trustees.md) of the ACE.</span></span>

</dd> <dt>

<span data-ttu-id="ad1e9-315"><span id="resource_attribute"></span><span id="RESOURCE_ATTRIBUTE"></span>**\_attributo Resource**</span><span class="sxs-lookup"><span data-stu-id="ad1e9-315"><span id="resource_attribute"></span><span id="RESOURCE_ATTRIBUTE"></span>**resource\_attribute**</span></span>
</dt> <dd>

<span data-ttu-id="ad1e9-316">\[FACOLTATIVO \] l'attributo della risorsa \_ è solo per le voci ACE della risorsa ed è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="ad1e9-316">\[OPTIONAL\] The resource\_attribute is only for resource ACEs and is optional.</span></span> <span data-ttu-id="ad1e9-317">Stringa che indica il tipo di dati.</span><span class="sxs-lookup"><span data-stu-id="ad1e9-317">A string that indicates the data type.</span></span> <span data-ttu-id="ad1e9-318">Il tipo di dati ACE dell'attributo di risorsa può essere uno dei tipi di dati seguenti definiti in SDDL. h.</span><span class="sxs-lookup"><span data-stu-id="ad1e9-318">The resource attribute ace data type can be one of the following data types defined in Sddl.h.</span></span>

<span data-ttu-id="ad1e9-319">Il \# segno "" è sinonimo di "0" negli attributi delle risorse.</span><span class="sxs-lookup"><span data-stu-id="ad1e9-319">The "\#" sign is synonymous with "0" in resource attributes.</span></span> <span data-ttu-id="ad1e9-320">Ad esempio, D:AI (XA; OICI; FA;;; WD; (OctetStringType = = \# 1 \# 2 \# 3 \# \# )) equivale a e interpretato come D:ai (XA; OICI; fa;;; WD; (OctetStringType = = \# 01020300)).</span><span class="sxs-lookup"><span data-stu-id="ad1e9-320">For example, D:AI(XA;OICI;FA;;;WD;(OctetStringType==\#1\#2\#3\#\#)) is equivalent to and interpreted as D:AI(XA;OICI;FA;;;WD;(OctetStringType==\#01020300)).</span></span>

<span data-ttu-id="ad1e9-321">**Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista e Windows server 2003:** Gli attributi della risorsa non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="ad1e9-321">**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista and Windows Server 2003:** Resource attributes are not available.</span></span>



| <span data-ttu-id="ad1e9-322">Stringa tipo di dati Ace attributo risorsa</span><span class="sxs-lookup"><span data-stu-id="ad1e9-322">Resource attribute ace data type string</span></span> | <span data-ttu-id="ad1e9-323">Costante in SDDL. h</span><span class="sxs-lookup"><span data-stu-id="ad1e9-323">Constant in Sddl.h</span></span> | <span data-ttu-id="ad1e9-324">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="ad1e9-324">Data type</span></span>        |
|-----------------------------------------|--------------------|------------------|
| <span data-ttu-id="ad1e9-325">TI</span><span class="sxs-lookup"><span data-stu-id="ad1e9-325">"TI"</span></span>                                    | <span data-ttu-id="ad1e9-326">SDDL \_ int</span><span class="sxs-lookup"><span data-stu-id="ad1e9-326">SDDL\_INT</span></span>          | <span data-ttu-id="ad1e9-327">Intero con segno</span><span class="sxs-lookup"><span data-stu-id="ad1e9-327">Signed integer</span></span>   |
| <span data-ttu-id="ad1e9-328">TU</span><span class="sxs-lookup"><span data-stu-id="ad1e9-328">"TU"</span></span>                                    | <span data-ttu-id="ad1e9-329">SDDL \_ uint</span><span class="sxs-lookup"><span data-stu-id="ad1e9-329">SDDL\_UINT</span></span>         | <span data-ttu-id="ad1e9-330">Intero senza segno</span><span class="sxs-lookup"><span data-stu-id="ad1e9-330">Unsigned integer</span></span> |
| <span data-ttu-id="ad1e9-331">TS</span><span class="sxs-lookup"><span data-stu-id="ad1e9-331">"TS"</span></span>                                    | <span data-ttu-id="ad1e9-332">\_WSTRING SDDL</span><span class="sxs-lookup"><span data-stu-id="ad1e9-332">SDDL\_WSTRING</span></span>      | <span data-ttu-id="ad1e9-333">Stringa estesa</span><span class="sxs-lookup"><span data-stu-id="ad1e9-333">Wide string</span></span>      |
| <span data-ttu-id="ad1e9-334">TD</span><span class="sxs-lookup"><span data-stu-id="ad1e9-334">"TD"</span></span>                                    | <span data-ttu-id="ad1e9-335">\_SID SDDL</span><span class="sxs-lookup"><span data-stu-id="ad1e9-335">SDDL\_SID</span></span>          | <span data-ttu-id="ad1e9-336">SID</span><span class="sxs-lookup"><span data-stu-id="ad1e9-336">SID</span></span>              |
| <span data-ttu-id="ad1e9-337">TX</span><span class="sxs-lookup"><span data-stu-id="ad1e9-337">"TX"</span></span>                                    | <span data-ttu-id="ad1e9-338">\_BLOB SDDL</span><span class="sxs-lookup"><span data-stu-id="ad1e9-338">SDDL\_BLOB</span></span>         | <span data-ttu-id="ad1e9-339">Stringa ottetto</span><span class="sxs-lookup"><span data-stu-id="ad1e9-339">Octet string</span></span>     |
| <span data-ttu-id="ad1e9-340">TB</span><span class="sxs-lookup"><span data-stu-id="ad1e9-340">"TB"</span></span>                                    | <span data-ttu-id="ad1e9-341">\_valore booleano SDDL</span><span class="sxs-lookup"><span data-stu-id="ad1e9-341">SDDL\_BOOLEAN</span></span>      | <span data-ttu-id="ad1e9-342">Boolean</span><span class="sxs-lookup"><span data-stu-id="ad1e9-342">Boolean</span></span>          |



 

</dd> </dl>

<span data-ttu-id="ad1e9-343">Nell'esempio seguente viene illustrata una stringa ACE per una voce ACE consentita per l'accesso.</span><span class="sxs-lookup"><span data-stu-id="ad1e9-343">The following example shows an ACE string for an access-allowed ACE.</span></span> <span data-ttu-id="ad1e9-344">Non si tratta di una voce ACE specifica dell'oggetto, quindi non contiene alcuna informazione **nel \_ GUID oggetto** e eredita i campi **\_ \_ GUID oggetto** .</span><span class="sxs-lookup"><span data-stu-id="ad1e9-344">It is not an object-specific ACE, so it has no information in the **object\_guid** and **inherit\_object\_guid** fields.</span></span> <span data-ttu-id="ad1e9-345">Anche il campo dei **\_ flag ACE** è vuoto, a indicare che non è stato impostato nessuno dei flag ACE.</span><span class="sxs-lookup"><span data-stu-id="ad1e9-345">The **ace\_flags** field is also empty, which indicates that none of the ACE flags are set.</span></span>


```C++
(A;;RPWPCCDCLCSWRCWDWOGA;;;S-1-1-0)
```



<span data-ttu-id="ad1e9-346">La stringa ACE illustrata sopra descrive le informazioni ACE seguenti.</span><span class="sxs-lookup"><span data-stu-id="ad1e9-346">The ACE string shown above describes the following ACE information.</span></span>


```C++
AceType:       0x00 (ACCESS_ALLOWED_ACE_TYPE)
AceFlags:      0x00
Access Mask:   0x100e003f
                    READ_CONTROL
                    WRITE_DAC
                    WRITE_OWNER
                    GENERIC_ALL
                    Other access rights(0x0000003f)
Ace Sid      : (S-1-1-0)
```



<span data-ttu-id="ad1e9-347">Nell'esempio seguente viene illustrato un file classificato con attestazioni di risorse per Windows e Structured Query Language (SQL) con segretezza impostata su un livello aziendale elevato.</span><span class="sxs-lookup"><span data-stu-id="ad1e9-347">The following example shows a file classified with resource claims for Windows and Structured Query Language (SQL) with Secrecy set to High Business Impact.</span></span>


```C++
(RA;CI;;;;S-1-1-0; ("Project",TS,0,"Windows","SQL")) 
(RA;CI;;;;S-1-1-0; ("Secrecy",TU,0,3))
```



<span data-ttu-id="ad1e9-348">La stringa ACE illustrata sopra descrive le informazioni ACE seguenti.</span><span class="sxs-lookup"><span data-stu-id="ad1e9-348">The ACE string shown above describes the following ACE information.</span></span>


```C++
AceType:       0x12 (SYSTEM_RESOURCE_ATTRIBUTE_ACE_TYPE)
AceFlags:      0x1  (SDDL_CONTAINER_INHERIT)
Access Mask:   0x0
Ace Sid      : (S-1-1-0)
Resource Attributes: Project has the strings Windows and SQL, Secrecy has the unsigned int value of 3
```



<span data-ttu-id="ad1e9-349">Per altre informazioni, vedere [formato stringa del descrittore di sicurezza](security-descriptor-string-format.md) e [stringhe SID](sid-strings.md).</span><span class="sxs-lookup"><span data-stu-id="ad1e9-349">For more information, see [Security Descriptor String Format](security-descriptor-string-format.md) and [SID Strings](sid-strings.md).</span></span> <span data-ttu-id="ad1e9-350">Per le voci ACE condizionali, vedere [Security Descriptor Definition Language per le ACE condizionali](security-descriptor-definition-language-for-conditional-aces-.md).</span><span class="sxs-lookup"><span data-stu-id="ad1e9-350">For conditional ACEs, see [Security Descriptor Definition Language for Conditional ACEs](security-descriptor-definition-language-for-conditional-aces-.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ad1e9-351">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ad1e9-351">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="ad1e9-352">[\[MS-DTYP \] : Security Descriptor Description Language](/openspecs/windows_protocols/ms-dtyp/4f4251cc-23b6-44b6-93ba-69688422cb06)</span><span class="sxs-lookup"><span data-stu-id="ad1e9-352">[\[MS-DTYP\]: Security Descriptor Description Language](/openspecs/windows_protocols/ms-dtyp/4f4251cc-23b6-44b6-93ba-69688422cb06)</span></span>
</dt> </dl>

