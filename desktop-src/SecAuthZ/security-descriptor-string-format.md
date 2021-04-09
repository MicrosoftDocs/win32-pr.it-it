---
description: Il formato della stringa del descrittore di sicurezza è un formato di testo per l'archiviazione o il trasporto di informazioni in un descrittore di sicurezza.
ms.assetid: 0a226629-084c-40c5-bdd4-ad7355c807cf
title: Formato stringa descrittore di sicurezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f5182de796ee8d3c61f079d3704ab29ad552457
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879653"
---
# <a name="security-descriptor-string-format"></a><span data-ttu-id="b8bb1-103">Formato stringa descrittore di sicurezza</span><span class="sxs-lookup"><span data-stu-id="b8bb1-103">Security Descriptor String Format</span></span>

<span data-ttu-id="b8bb1-104">Il **formato della stringa del descrittore di sicurezza** è un formato di testo per l'archiviazione o il trasporto di informazioni in un descrittore di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="b8bb1-104">The **Security Descriptor String Format** is a text format for storing or transporting information in a security descriptor.</span></span> <span data-ttu-id="b8bb1-105">Le funzioni [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) e [**ConvertStringSecurityDescriptorToSecurityDescriptor ha**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) usano questo formato.</span><span class="sxs-lookup"><span data-stu-id="b8bb1-105">The [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) and [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) functions use this format.</span></span>

<span data-ttu-id="b8bb1-106">Il formato è una stringa con terminazione **null** con token per indicare ognuno dei quattro componenti principali di un descrittore di sicurezza: Owner (O:), gruppo primario (G:), DACL (D:) e SACL (S:).</span><span class="sxs-lookup"><span data-stu-id="b8bb1-106">The format is a **null**-terminated string with tokens to indicate each of the four main components of a security descriptor: owner (O:), primary group (G:), DACL (D:), and SACL (S:).</span></span>

> [!Note]  
> <span data-ttu-id="b8bb1-107">Le [*voci di controllo di accesso*](/windows/desktop/SecGloss/a-gly) (ACE) e gli assi condizionali hanno formati diversi.</span><span class="sxs-lookup"><span data-stu-id="b8bb1-107">[*Access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs) and conditional ACEs have differing formats.</span></span> <span data-ttu-id="b8bb1-108">Per le voci ACE, vedere [stringhe ACE](ace-strings.md).</span><span class="sxs-lookup"><span data-stu-id="b8bb1-108">For ACEs, see [ACE Strings](ace-strings.md).</span></span> <span data-ttu-id="b8bb1-109">Per le voci ACE condizionali, vedere [Security Descriptor Definition Language per le ACE condizionali](security-descriptor-definition-language-for-conditional-aces-.md).</span><span class="sxs-lookup"><span data-stu-id="b8bb1-109">For conditional ACEs, see [Security Descriptor Definition Language for Conditional ACEs](security-descriptor-definition-language-for-conditional-aces-.md).</span></span>

 


```C++
O:owner_sid
G:group_sid
D:dacl_flags(string_ace1)(string_ace2)... (string_acen)
S:sacl_flags(string_ace1)(string_ace2)... (string_acen)
```



<dl> <dt>

<span data-ttu-id="b8bb1-110"><span id="owner_sid"></span><span id="OWNER_SID"></span>\_SID proprietario</span><span class="sxs-lookup"><span data-stu-id="b8bb1-110"><span id="owner_sid"></span><span id="OWNER_SID"></span>owner\_sid</span></span>
</dt> <dd>

<span data-ttu-id="b8bb1-111">[Stringa SID](sid-strings.md) che identifica il proprietario dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b8bb1-111">A [SID string](sid-strings.md) that identifies the object's owner.</span></span>

</dd> <dt>

<span data-ttu-id="b8bb1-112"><span id="group_sid"></span><span id="GROUP_SID"></span>\_SID gruppo</span><span class="sxs-lookup"><span data-stu-id="b8bb1-112"><span id="group_sid"></span><span id="GROUP_SID"></span>group\_sid</span></span>
</dt> <dd>

<span data-ttu-id="b8bb1-113">Stringa SID che identifica il gruppo primario dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b8bb1-113">A SID string that identifies the object's primary group.</span></span>

</dd> <dt>

<span data-ttu-id="b8bb1-114"><span id="dacl_flags"></span><span id="DACL_FLAGS"></span>\_flag DACL</span><span class="sxs-lookup"><span data-stu-id="b8bb1-114"><span id="dacl_flags"></span><span id="DACL_FLAGS"></span>dacl\_flags</span></span>
</dt> <dd>

<span data-ttu-id="b8bb1-115">Flag di controllo del descrittore di sicurezza che si applicano a DACL.</span><span class="sxs-lookup"><span data-stu-id="b8bb1-115">Security descriptor control flags that apply to the DACL.</span></span> <span data-ttu-id="b8bb1-116">Per una descrizione di questi flag di controllo, vedere la funzione [**SetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorcontrol) .</span><span class="sxs-lookup"><span data-stu-id="b8bb1-116">For a description of these control flags, see the [**SetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorcontrol) function.</span></span> <span data-ttu-id="b8bb1-117">La \_ stringa dei flag DACL può essere una concatenazione di zero o più delle stringhe seguenti.</span><span class="sxs-lookup"><span data-stu-id="b8bb1-117">The dacl\_flags string can be a concatenation of zero or more of the following strings.</span></span>



| <span data-ttu-id="b8bb1-118">Control</span><span class="sxs-lookup"><span data-stu-id="b8bb1-118">Control</span></span>               | <span data-ttu-id="b8bb1-119">Costante in SDDL. h</span><span class="sxs-lookup"><span data-stu-id="b8bb1-119">Constant in Sddl.h</span></span>       | <span data-ttu-id="b8bb1-120">Significato</span><span class="sxs-lookup"><span data-stu-id="b8bb1-120">Meaning</span></span>                                       |
|-----------------------|--------------------------|-----------------------------------------------|
| <span data-ttu-id="b8bb1-121">P</span><span class="sxs-lookup"><span data-stu-id="b8bb1-121">"P"</span></span>                   | <span data-ttu-id="b8bb1-122">SDDL \_ protetto</span><span class="sxs-lookup"><span data-stu-id="b8bb1-122">SDDL\_PROTECTED</span></span>          | <span data-ttu-id="b8bb1-123">\_Viene impostato il flag se il DACL \_ è protetto.</span><span class="sxs-lookup"><span data-stu-id="b8bb1-123">The SE\_DACL\_PROTECTED flag is set.</span></span>          |
| <span data-ttu-id="b8bb1-124">AR</span><span class="sxs-lookup"><span data-stu-id="b8bb1-124">"AR"</span></span>                  | <span data-ttu-id="b8bb1-125">richiesta \_ di \_ ereditarietà automatica SDDL \_</span><span class="sxs-lookup"><span data-stu-id="b8bb1-125">SDDL\_AUTO\_INHERIT\_REQ</span></span> | <span data-ttu-id="b8bb1-126">Il \_ flag se DACL \_ auto \_ eredita automaticamente \_ è impostato.</span><span class="sxs-lookup"><span data-stu-id="b8bb1-126">The SE\_DACL\_AUTO\_INHERIT\_REQ flag is set.</span></span> |
| <span data-ttu-id="b8bb1-127">INTELLIGENZA artificiale</span><span class="sxs-lookup"><span data-stu-id="b8bb1-127">"AI"</span></span>                  | <span data-ttu-id="b8bb1-128">SDDL \_ automaticamente \_ ereditato</span><span class="sxs-lookup"><span data-stu-id="b8bb1-128">SDDL\_AUTO\_INHERITED</span></span>    | <span data-ttu-id="b8bb1-129">\_ \_ Viene impostato il flag if DACL auto \_ ereditato.</span><span class="sxs-lookup"><span data-stu-id="b8bb1-129">The SE\_DACL\_AUTO\_INHERITED flag is set.</span></span>    |
| <span data-ttu-id="b8bb1-130">"nessun \_ controllo di accesso \_ "</span><span class="sxs-lookup"><span data-stu-id="b8bb1-130">"NO\_ACCESS\_CONTROL"</span></span> | <span data-ttu-id="b8bb1-131">\_ACL null \_ SSDL</span><span class="sxs-lookup"><span data-stu-id="b8bb1-131">SSDL\_NULL\_ACL</span></span>          | <span data-ttu-id="b8bb1-132">L'ACL è null.</span><span class="sxs-lookup"><span data-stu-id="b8bb1-132">The ACL is null.</span></span>                              |



 

</dd> <dt>

<span data-ttu-id="b8bb1-133"><span id="sacl_flags"></span><span id="SACL_FLAGS"></span>\_flag SACL</span><span class="sxs-lookup"><span data-stu-id="b8bb1-133"><span id="sacl_flags"></span><span id="SACL_FLAGS"></span>sacl\_flags</span></span>
</dt> <dd>

<span data-ttu-id="b8bb1-134">Flag di controllo del descrittore di sicurezza che si applicano all'elenco SACL.</span><span class="sxs-lookup"><span data-stu-id="b8bb1-134">Security descriptor control flags that apply to the SACL.</span></span> <span data-ttu-id="b8bb1-135">La \_ stringa di flag SACL usa le stesse stringhe di bit del controllo della \_ stringa dei flag DACL.</span><span class="sxs-lookup"><span data-stu-id="b8bb1-135">The sacl\_flags string uses the same control bit strings as the dacl\_flags string.</span></span>

</dd> <dt>

<span data-ttu-id="b8bb1-136"><span id="string_ace"></span><span id="STRING_ACE"></span>\_ACE stringa</span><span class="sxs-lookup"><span data-stu-id="b8bb1-136"><span id="string_ace"></span><span id="STRING_ACE"></span>string\_ace</span></span>
</dt> <dd>

<span data-ttu-id="b8bb1-137">Stringa che descrive una voce ACE nel DACL o nel SACL del descrittore di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="b8bb1-137">A string that describes an ACE in the security descriptor's DACL or SACL.</span></span> <span data-ttu-id="b8bb1-138">Per una descrizione del formato di stringa ACE, vedere [stringhe ACE](ace-strings.md).</span><span class="sxs-lookup"><span data-stu-id="b8bb1-138">For a description of the ACE string format, see [ACE strings](ace-strings.md).</span></span> <span data-ttu-id="b8bb1-139">Ogni stringa ACE è racchiusa tra parentesi (()).</span><span class="sxs-lookup"><span data-stu-id="b8bb1-139">Each ACE string is enclosed in parentheses (()).</span></span>

</dd> </dl>

<span data-ttu-id="b8bb1-140">I componenti non necessari possono essere omessi dalla stringa del descrittore di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="b8bb1-140">Unneeded components can be omitted from the security descriptor string.</span></span> <span data-ttu-id="b8bb1-141">Se, ad esempio, il \_ flag di presenza DACL se \_ non è impostato nel descrittore di sicurezza di input, [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) non include un componente D: nella stringa di output.</span><span class="sxs-lookup"><span data-stu-id="b8bb1-141">For example, if the SE\_DACL\_PRESENT flag is not set in the input security descriptor, [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) does not include a D: component in the output string.</span></span> <span data-ttu-id="b8bb1-142">È anche possibile usare i flag di bit per [**\_ informazioni di sicurezza**](security-information.md) per indicare i componenti da includere in una stringa del descrittore di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="b8bb1-142">You can also use the [**SECURITY\_INFORMATION**](security-information.md) bit flags to indicate the components to include in a security descriptor string.</span></span>

<span data-ttu-id="b8bb1-143">Il formato della stringa del descrittore di sicurezza non supporta ACL **null** .</span><span class="sxs-lookup"><span data-stu-id="b8bb1-143">The security descriptor string format does not support **NULL** ACLs.</span></span>

<span data-ttu-id="b8bb1-144">Per indicare un ACL vuoto, la stringa del descrittore di sicurezza include il token D: o S: senza informazioni aggiuntive sulla stringa.</span><span class="sxs-lookup"><span data-stu-id="b8bb1-144">To denote an empty ACL, the security descriptor string includes the D: or S: token with no additional string information.</span></span>

<span data-ttu-id="b8bb1-145">La stringa del descrittore di sicurezza archivia i bit del [**controllo DEscrittore di sicurezza**](security-descriptor-control.md) in modi diversi.</span><span class="sxs-lookup"><span data-stu-id="b8bb1-145">The security descriptor string stores the [**SECURITY DESCRIPTOR CONTROL**](security-descriptor-control.md) bits in different ways.</span></span> <span data-ttu-id="b8bb1-146">I \_ bit del DACL se \_ presente o se i \_ SACL \_ presenti sono indicati dalla presenza del token D: o S: nella stringa.</span><span class="sxs-lookup"><span data-stu-id="b8bb1-146">The SE\_DACL\_PRESENT or SE\_SACL\_PRESENT bits are indicated by the presence of the D: or S: token in the string.</span></span> <span data-ttu-id="b8bb1-147">Altri bit che si applicano a DACL o SACL sono archiviati in \_ flag DACL e \_ flag SACL.</span><span class="sxs-lookup"><span data-stu-id="b8bb1-147">Other bits that apply to the DACL or SACL are stored in dacl\_flags and sacl\_flags.</span></span> <span data-ttu-id="b8bb1-148">Il proprietario SE è stato impostato come predefinito \_ \_ , se il \_ gruppo se \_ è impostato come predefinito, se \_ DACL \_ è impostato come predefinito e se \_ \_ il SACL è impostato come predefinito, i bit non vengono archiviati in una stringa descrittore</span><span class="sxs-lookup"><span data-stu-id="b8bb1-148">The SE\_OWNER\_DEFAULTED, SE\_GROUP\_DEFAULTED, SE\_DACL\_DEFAULTED, and SE\_SACL\_DEFAULTED bits are not stored in a security descriptor string.</span></span> <span data-ttu-id="b8bb1-149">Il \_ bit se self \_ relativa non è archiviato nella stringa, ma [**ConvertStringSecurityDescriptorToSecurityDescriptor ha**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) imposta sempre questo bit nel descrittore di sicurezza di output.</span><span class="sxs-lookup"><span data-stu-id="b8bb1-149">The SE\_SELF\_RELATIVE bit is not stored in the string, but [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) always sets this bit in the output security descriptor.</span></span>

<span data-ttu-id="b8bb1-150">Negli esempi seguenti vengono illustrate le stringhe del descrittore di sicurezza e le informazioni nei descrittori di sicurezza associati.</span><span class="sxs-lookup"><span data-stu-id="b8bb1-150">The following examples show security descriptor strings and the information in the associated security descriptors.</span></span>

<span data-ttu-id="b8bb1-151">Stringa 1:</span><span class="sxs-lookup"><span data-stu-id="b8bb1-151">String 1:</span></span>


```C++
"O:AOG:DAD:(A;;RPWPCCDCLCSWRCWDWOGA;;;S-1-0-0)"
```



<span data-ttu-id="b8bb1-152">Descrittore di sicurezza 1:</span><span class="sxs-lookup"><span data-stu-id="b8bb1-152">Security Descriptor 1:</span></span>


```C++
    Revision:  0x00000001
    Control:   0x0004
        SE_DACL_PRESENT
    Owner: (S-1-5-32-548)
    PrimaryGroup: (S-1-5-21-397955417-626881126-188441444-512)
DACL
    Revision: 0x02
    Size:     0x001c
    AceCount: 0x0001
    Ace[00]
        AceType:       0x00 (ACCESS_ALLOWED_ACE_TYPE)
        AceSize:       0x0014
        InheritFlags:  0x00
        Access Mask:   0x100e003f
                            READ_CONTROL
                            WRITE_DAC
                            WRITE_OWNER
                            GENERIC_ALL
                            Others(0x0000003f)
        Ace Sid      : (S-1-0-0)
SACL
    Not present
```



<span data-ttu-id="b8bb1-153">Stringa 2:</span><span class="sxs-lookup"><span data-stu-id="b8bb1-153">String 2:</span></span>


```C++
"O:DAG:DAD:(A;;RPWPCCDCLCRCWOWDSDSW;;;SY)
(A;;RPWPCCDCLCRCWOWDSDSW;;;DA)
(OA;;CCDC;bf967aba-0de6-11d0-a285-00aa003049e2;;AO)
(OA;;CCDC;bf967a9c-0de6-11d0-a285-00aa003049e2;;AO)
(OA;;CCDC;6da8a4ff-0e52-11d0-a286-00aa003049e2;;AO)
(OA;;CCDC;bf967aa8-0de6-11d0-a285-00aa003049e2;;PO)
(A;;RPLCRC;;;AU)S:(AU;SAFA;WDWOSDWPCCDCSW;;;WD)"
```



<span data-ttu-id="b8bb1-154">Descrittore di sicurezza 2:</span><span class="sxs-lookup"><span data-stu-id="b8bb1-154">Security Descriptor 2:</span></span>


```C++
    Revision:  0x00000001
    Control:   0x0014
        SE_DACL_PRESENT
        SE_SACL_PRESENT
    Owner: (S-1-5-21-397955417-626881126-188441444-512)
    PrimaryGroup: (S-1-5-21-397955417-626881126-188441444-512)
DACL
    Revision: 0x04
    Size:     0x0104
    AceCount: 0x0007
    Ace[00]
        AceType:       0x00 (ACCESS_ALLOWED_ACE_TYPE)
        AceSize:       0x0014
        InheritFlags:  0x00
        Access Mask:   0x000f003f
                            DELETE
                            READ_CONTROL
                            WRITE_DAC
                            WRITE_OWNER
                            Others(0x0000003f)
        Ace Sid:       (S-1-5-18)
    Ace[01]
        AceType:       0x00 (ACCESS_ALLOWED_ACE_TYPE)
        AceSize:       0x0024
        InheritFlags:  0x00
        Access Mask:   0x000f003f
                            DELETE
                            READ_CONTROL
                            WRITE_DAC
                            WRITE_OWNER
                            Others(0x0000003f)
        Ace Sid:       (S-1-5-21-397955417-626881126-188441444-512)
    Ace[02]
        AceType:       0x05 (ACCESS_ALLOWED_OBJECT_ACE_TYPE)
        AceSize:       0x002c
        InheritFlags:  0x00
        Access Mask:   0x00000003
                            Others(0x00000003)
        Flags:         0x00000001, ACE_OBJECT_TYPE_PRESENT
        ObjectType:    GUID_C_USER
        InhObjectType: GUID ptr is NULL
        Ace Sid:       (S-1-5-32-548)
    Ace[03]
        AceType:       0x05 (ACCESS_ALLOWED_OBJECT_ACE_TYPE)
        AceSize:       0x002c
        InheritFlags:  0x00
        Access Mask:   0x00000003
                            Others(0x00000003)
        Flags:         0x00000001, ACE_OBJECT_TYPE_PRESENT
        ObjectType:    GUID_C_GROUP
        InhObjectType: GUID ptr is NULL
        Ace Sid:       (S-1-5-32-548)
    Ace[04]
        AceType:       0x05 (ACCESS_ALLOWED_OBJECT_ACE_TYPE)
        AceSize:       0x002c
        InheritFlags:  0x00
        Access Mask:   0x00000003
                            Others(0x00000003)
        Flags:         0x00000001, ACE_OBJECT_TYPE_PRESENT
        ObjectType:    GUID_C_LOCALGROUP
        InhObjectType: GUID ptr is NULL
        Ace Sid:       (S-1-5-32-548)
    Ace[05]
        AceType:       0x05 (ACCESS_ALLOWED_OBJECT_ACE_TYPE)
        AceSize:       0x002c
        InheritFlags:  0x00
        Access Mask:   0x00000003
                            Others(0x00000003)
        Flags:         0x00000001, ACE_OBJECT_TYPE_PRESENT
        ObjectType:    GUID_C_PRINT_QUEUE
        InhObjectType: GUID ptr is NULL
        Ace Sid:       (S-1-5-32-550)
    Ace[06]
        AceType:       0x00 (ACCESS_ALLOWED_ACE_TYPE)
        AceSize:       0x0014
        InheritFlags:  0x00
        Access Mask:   0x00020014
                            READ_CONTROL
                            Others(0x00000014)
        Ace Sid:       (S-1-5-11)
    SACL
        Revision: 0x02
        Size:     0x001c
        AceCount: 0x0001
        Ace[00]
            AceType:       0x02 (SYSTEM_AUDIT_ACE_TYPE)
            AceSize:       0x0014
            InheritFlags:  0xc0
                SUCCESSFUL_ACCESS_ACE_FLAG
                FAILED_ACCESS_ACE_FLAG
            Access Mask:    0x000d002b
                                DELETE
                                WRITE_DAC
                                WRITE_OWNER
                                Others(0x0000002b)
            Ace Sid:       (S-1-1-0)
```



## <a name="related-topics"></a><span data-ttu-id="b8bb1-155">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b8bb1-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8bb1-156">Stringhe ACE</span><span class="sxs-lookup"><span data-stu-id="b8bb1-156">ACE Strings</span></span>](ace-strings.md)
</dt> <dt>

[<span data-ttu-id="b8bb1-157">Linguaggio di definizione del descrittore di sicurezza per le voci</span><span class="sxs-lookup"><span data-stu-id="b8bb1-157">Security Descriptor Definition Language for Conditional ACEs</span></span>](security-descriptor-definition-language-for-conditional-aces-.md)
</dt> </dl>

 

 
