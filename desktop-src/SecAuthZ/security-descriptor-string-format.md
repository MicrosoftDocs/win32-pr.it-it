---
description: Il formato di stringa del descrittore di sicurezza è un formato di testo per l'archiviazione o il trasporto di informazioni in un descrittore di sicurezza.
ms.assetid: 0a226629-084c-40c5-bdd4-ad7355c807cf
title: Formato stringa descrittore di sicurezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d7fd6e9e2387deee63b5046086ed167a29fa54b
ms.sourcegitcommit: 07ba02719c9779e082b108ae74f9699fb0236c34
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/06/2021
ms.locfileid: "108644203"
---
# <a name="security-descriptor-string-format"></a><span data-ttu-id="f8e75-103">Formato stringa descrittore di sicurezza</span><span class="sxs-lookup"><span data-stu-id="f8e75-103">Security Descriptor String Format</span></span>

<span data-ttu-id="f8e75-104">Il **formato di stringa del descrittore di** sicurezza è un formato di testo per l'archiviazione o il trasporto di informazioni in un descrittore di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="f8e75-104">The **Security Descriptor String Format** is a text format for storing or transporting information in a security descriptor.</span></span> <span data-ttu-id="f8e75-105">Le [**funzioni ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) e [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) usano questo formato.</span><span class="sxs-lookup"><span data-stu-id="f8e75-105">The [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) and [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) functions use this format.</span></span>

<span data-ttu-id="f8e75-106">Il formato è una stringa con terminazione **Null** con token per indicare ognuno dei quattro componenti principali di un descrittore di sicurezza: owner (O:), primary group (G:), DACL (D:) e SACL (S:).</span><span class="sxs-lookup"><span data-stu-id="f8e75-106">The format is a **null**-terminated string with tokens to indicate each of the four main components of a security descriptor: owner (O:), primary group (G:), DACL (D:), and SACL (S:).</span></span>

> [!Note]  
> <span data-ttu-id="f8e75-107">[*Le voci di controllo di accesso*](/windows/desktop/SecGloss/a-gly) (ACE) e le voci ACE condizionali hanno formati diversi.</span><span class="sxs-lookup"><span data-stu-id="f8e75-107">[*Access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs) and conditional ACEs have differing formats.</span></span> <span data-ttu-id="f8e75-108">Per le ACE, vedere [Stringhe ACE](ace-strings.md).</span><span class="sxs-lookup"><span data-stu-id="f8e75-108">For ACEs, see [ACE Strings](ace-strings.md).</span></span> <span data-ttu-id="f8e75-109">Per le ACE condizionali, vedere [Linguaggio di definizione del descrittore di sicurezza per le ACE condizionali.](security-descriptor-definition-language-for-conditional-aces-.md)</span><span class="sxs-lookup"><span data-stu-id="f8e75-109">For conditional ACEs, see [Security Descriptor Definition Language for Conditional ACEs](security-descriptor-definition-language-for-conditional-aces-.md).</span></span>

 


```C++
O:owner_sid
G:group_sid
D:dacl_flags(string_ace1)(string_ace2)... (string_acen)
S:sacl_flags(string_ace1)(string_ace2)... (string_acen)
```



<dl> <dt>

<span data-ttu-id="f8e75-110"><span id="owner_sid"></span><span id="OWNER_SID"></span>owner \_ sid</span><span class="sxs-lookup"><span data-stu-id="f8e75-110"><span id="owner_sid"></span><span id="OWNER_SID"></span>owner\_sid</span></span>
</dt> <dd>

<span data-ttu-id="f8e75-111">Stringa [SID che](sid-strings.md) identifica il proprietario dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f8e75-111">A [SID string](sid-strings.md) that identifies the object's owner.</span></span>

</dd> <dt>

<span data-ttu-id="f8e75-112"><span id="group_sid"></span><span id="GROUP_SID"></span>group \_ sid</span><span class="sxs-lookup"><span data-stu-id="f8e75-112"><span id="group_sid"></span><span id="GROUP_SID"></span>group\_sid</span></span>
</dt> <dd>

<span data-ttu-id="f8e75-113">Stringa SID che identifica il gruppo primario dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f8e75-113">A SID string that identifies the object's primary group.</span></span>

</dd> <dt>

<span data-ttu-id="f8e75-114"><span id="dacl_flags"></span><span id="DACL_FLAGS"></span>flag \_ dacl</span><span class="sxs-lookup"><span data-stu-id="f8e75-114"><span id="dacl_flags"></span><span id="DACL_FLAGS"></span>dacl\_flags</span></span>
</dt> <dd>

<span data-ttu-id="f8e75-115">Flag di controllo del descrittore di sicurezza che si applicano all'elenco DACL.</span><span class="sxs-lookup"><span data-stu-id="f8e75-115">Security descriptor control flags that apply to the DACL.</span></span> <span data-ttu-id="f8e75-116">Per una descrizione di questi flag di controllo, vedere la [**funzione SetSecurityDescriptorControl.**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorcontrol)</span><span class="sxs-lookup"><span data-stu-id="f8e75-116">For a description of these control flags, see the [**SetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorcontrol) function.</span></span> <span data-ttu-id="f8e75-117">La stringa flag dacl può essere una concatenazione di \_ zero o più stringhe seguenti.</span><span class="sxs-lookup"><span data-stu-id="f8e75-117">The dacl\_flags string can be a concatenation of zero or more of the following strings.</span></span>



| <span data-ttu-id="f8e75-118">Control</span><span class="sxs-lookup"><span data-stu-id="f8e75-118">Control</span></span>               | <span data-ttu-id="f8e75-119">Costante in Sddl.h</span><span class="sxs-lookup"><span data-stu-id="f8e75-119">Constant in Sddl.h</span></span>       | <span data-ttu-id="f8e75-120">Significato</span><span class="sxs-lookup"><span data-stu-id="f8e75-120">Meaning</span></span>                                       |
|-----------------------|--------------------------|-----------------------------------------------|
| <span data-ttu-id="f8e75-121">"P"</span><span class="sxs-lookup"><span data-stu-id="f8e75-121">"P"</span></span>                   | <span data-ttu-id="f8e75-122">SDDL \_ PROTECTED</span><span class="sxs-lookup"><span data-stu-id="f8e75-122">SDDL\_PROTECTED</span></span>          | <span data-ttu-id="f8e75-123">Il \_ flag SE DACL \_ PROTECTED è impostato.</span><span class="sxs-lookup"><span data-stu-id="f8e75-123">The SE\_DACL\_PROTECTED flag is set.</span></span>          |
| <span data-ttu-id="f8e75-124">"AR"</span><span class="sxs-lookup"><span data-stu-id="f8e75-124">"AR"</span></span>                  | <span data-ttu-id="f8e75-125">SDDL \_ AUTO \_ INHERIT \_ REQ</span><span class="sxs-lookup"><span data-stu-id="f8e75-125">SDDL\_AUTO\_INHERIT\_REQ</span></span> | <span data-ttu-id="f8e75-126">Il \_ flag SE DACL \_ AUTO INHERIT \_ \_ REQ è impostato.</span><span class="sxs-lookup"><span data-stu-id="f8e75-126">The SE\_DACL\_AUTO\_INHERIT\_REQ flag is set.</span></span> |
| <span data-ttu-id="f8e75-127">"AI"</span><span class="sxs-lookup"><span data-stu-id="f8e75-127">"AI"</span></span>                  | <span data-ttu-id="f8e75-128">SDDL \_ \_ EREDITATO AUTOMATICAMENTE</span><span class="sxs-lookup"><span data-stu-id="f8e75-128">SDDL\_AUTO\_INHERITED</span></span>    | <span data-ttu-id="f8e75-129">Il \_ flag SE DACL \_ AUTO \_ INHERITED è impostato.</span><span class="sxs-lookup"><span data-stu-id="f8e75-129">The SE\_DACL\_AUTO\_INHERITED flag is set.</span></span>    |
| <span data-ttu-id="f8e75-130">"NO \_ ACCESS \_ CONTROL"</span><span class="sxs-lookup"><span data-stu-id="f8e75-130">"NO\_ACCESS\_CONTROL"</span></span> | <span data-ttu-id="f8e75-131">SDDL \_ NULL \_ ACL</span><span class="sxs-lookup"><span data-stu-id="f8e75-131">SDDL\_NULL\_ACL</span></span>          | <span data-ttu-id="f8e75-132">L'ACL è Null.</span><span class="sxs-lookup"><span data-stu-id="f8e75-132">The ACL is null.</span></span> <span data-ttu-id="f8e75-133">**Windows Server 2008, Windows Vista e Windows Server 2003:** Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="f8e75-133">**Windows Server 2008, Windows Vista and Windows Server 2003:** Not available.</span></span> |



 

</dd> <dt>

<span data-ttu-id="f8e75-134"><span id="sacl_flags"></span><span id="SACL_FLAGS"></span>flag \_ sacl</span><span class="sxs-lookup"><span data-stu-id="f8e75-134"><span id="sacl_flags"></span><span id="SACL_FLAGS"></span>sacl\_flags</span></span>
</dt> <dd>

<span data-ttu-id="f8e75-135">Flag di controllo del descrittore di sicurezza che si applicano all'elenco SACL.</span><span class="sxs-lookup"><span data-stu-id="f8e75-135">Security descriptor control flags that apply to the SACL.</span></span> <span data-ttu-id="f8e75-136">La stringa dei flag sacl \_ usa le stesse stringhe di bit di controllo della stringa dei flag dacl. \_</span><span class="sxs-lookup"><span data-stu-id="f8e75-136">The sacl\_flags string uses the same control bit strings as the dacl\_flags string.</span></span>

</dd> <dt>

<span data-ttu-id="f8e75-137"><span id="string_ace"></span><span id="STRING_ACE"></span>string \_ ace</span><span class="sxs-lookup"><span data-stu-id="f8e75-137"><span id="string_ace"></span><span id="STRING_ACE"></span>string\_ace</span></span>
</dt> <dd>

<span data-ttu-id="f8e75-138">Stringa che descrive una ACE nell'elenco DACL o SACL del descrittore di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="f8e75-138">A string that describes an ACE in the security descriptor's DACL or SACL.</span></span> <span data-ttu-id="f8e75-139">Per una descrizione del formato di stringa ACE, vedere [Stringhe ACE.](ace-strings.md)</span><span class="sxs-lookup"><span data-stu-id="f8e75-139">For a description of the ACE string format, see [ACE strings](ace-strings.md).</span></span> <span data-ttu-id="f8e75-140">Ogni stringa ACE è racchiusa tra parentesi (()).</span><span class="sxs-lookup"><span data-stu-id="f8e75-140">Each ACE string is enclosed in parentheses (()).</span></span>

</dd> </dl>

<span data-ttu-id="f8e75-141">I componenti non necessari possono essere omessi dalla stringa del descrittore di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="f8e75-141">Unneeded components can be omitted from the security descriptor string.</span></span> <span data-ttu-id="f8e75-142">Ad esempio, se il flag SE DACL PRESENT non è impostato nel descrittore di sicurezza di \_ \_ input, [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) non include un componente D: nella stringa di output.</span><span class="sxs-lookup"><span data-stu-id="f8e75-142">For example, if the SE\_DACL\_PRESENT flag is not set in the input security descriptor, [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) does not include a D: component in the output string.</span></span> <span data-ttu-id="f8e75-143">È anche possibile usare i flag di bit [**SECURITY \_ INFORMATION**](security-information.md) per indicare i componenti da includere in una stringa del descrittore di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="f8e75-143">You can also use the [**SECURITY\_INFORMATION**](security-information.md) bit flags to indicate the components to include in a security descriptor string.</span></span>

<span data-ttu-id="f8e75-144">Il formato della stringa del descrittore di sicurezza non supporta **gli ACL NULL.**</span><span class="sxs-lookup"><span data-stu-id="f8e75-144">The security descriptor string format does not support **NULL** ACLs.</span></span>

<span data-ttu-id="f8e75-145">Per indicare un elenco di controllo di accesso vuoto, la stringa del descrittore di sicurezza include il token D: o S: senza informazioni aggiuntive sulla stringa.</span><span class="sxs-lookup"><span data-stu-id="f8e75-145">To denote an empty ACL, the security descriptor string includes the D: or S: token with no additional string information.</span></span>

<span data-ttu-id="f8e75-146">La stringa del descrittore di sicurezza archivia i bit [**SECURITY DESCRIPTOR CONTROL**](security-descriptor-control.md) in modi diversi.</span><span class="sxs-lookup"><span data-stu-id="f8e75-146">The security descriptor string stores the [**SECURITY DESCRIPTOR CONTROL**](security-descriptor-control.md) bits in different ways.</span></span> <span data-ttu-id="f8e75-147">I bit SE DACL PRESENT o SE SACL PRESENT sono indicati dalla presenza del token D: o \_ \_ \_ \_ S: nella stringa.</span><span class="sxs-lookup"><span data-stu-id="f8e75-147">The SE\_DACL\_PRESENT or SE\_SACL\_PRESENT bits are indicated by the presence of the D: or S: token in the string.</span></span> <span data-ttu-id="f8e75-148">Altri bit che si applicano all'elenco DACL o a SACL vengono archiviati in flag dacl \_ e flag \_ sacl.</span><span class="sxs-lookup"><span data-stu-id="f8e75-148">Other bits that apply to the DACL or SACL are stored in dacl\_flags and sacl\_flags.</span></span> <span data-ttu-id="f8e75-149">I bit SE \_ OWNER \_ DEFAULTED, SE \_ GROUP \_ DEFAULTED, SE \_ DACL DEFAULTED e SE \_ SACL DEFAULTED non vengono \_ \_ archiviati in una stringa del descrittore di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="f8e75-149">The SE\_OWNER\_DEFAULTED, SE\_GROUP\_DEFAULTED, SE\_DACL\_DEFAULTED, and SE\_SACL\_DEFAULTED bits are not stored in a security descriptor string.</span></span> <span data-ttu-id="f8e75-150">Il bit SE SELF RELATIVE non viene archiviato nella stringa, ma \_ \_ [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) imposta sempre questo bit nel descrittore di sicurezza di output.</span><span class="sxs-lookup"><span data-stu-id="f8e75-150">The SE\_SELF\_RELATIVE bit is not stored in the string, but [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) always sets this bit in the output security descriptor.</span></span>

<span data-ttu-id="f8e75-151">Gli esempi seguenti illustrano le stringhe dei descrittori di sicurezza e le informazioni nei descrittori di sicurezza associati.</span><span class="sxs-lookup"><span data-stu-id="f8e75-151">The following examples show security descriptor strings and the information in the associated security descriptors.</span></span>

<span data-ttu-id="f8e75-152">Stringa 1:</span><span class="sxs-lookup"><span data-stu-id="f8e75-152">String 1:</span></span>


```C++
"O:AOG:DAD:(A;;RPWPCCDCLCSWRCWDWOGA;;;S-1-0-0)"
```



<span data-ttu-id="f8e75-153">Descrittore di sicurezza 1:</span><span class="sxs-lookup"><span data-stu-id="f8e75-153">Security Descriptor 1:</span></span>


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



<span data-ttu-id="f8e75-154">Stringa 2:</span><span class="sxs-lookup"><span data-stu-id="f8e75-154">String 2:</span></span>


```C++
"O:DAG:DAD:(A;;RPWPCCDCLCRCWOWDSDSW;;;SY)
(A;;RPWPCCDCLCRCWOWDSDSW;;;DA)
(OA;;CCDC;bf967aba-0de6-11d0-a285-00aa003049e2;;AO)
(OA;;CCDC;bf967a9c-0de6-11d0-a285-00aa003049e2;;AO)
(OA;;CCDC;6da8a4ff-0e52-11d0-a286-00aa003049e2;;AO)
(OA;;CCDC;bf967aa8-0de6-11d0-a285-00aa003049e2;;PO)
(A;;RPLCRC;;;AU)S:(AU;SAFA;WDWOSDWPCCDCSW;;;WD)"
```



<span data-ttu-id="f8e75-155">Descrittore di sicurezza 2:</span><span class="sxs-lookup"><span data-stu-id="f8e75-155">Security Descriptor 2:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="f8e75-156">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f8e75-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f8e75-157">Stringhe ACE</span><span class="sxs-lookup"><span data-stu-id="f8e75-157">ACE Strings</span></span>](ace-strings.md)
</dt> <dt>

[<span data-ttu-id="f8e75-158">Linguaggio di definizione del descrittore di sicurezza per le ACE condizionali</span><span class="sxs-lookup"><span data-stu-id="f8e75-158">Security Descriptor Definition Language for Conditional ACEs</span></span>](security-descriptor-definition-language-for-conditional-aces-.md)
</dt> </dl>

 

 
