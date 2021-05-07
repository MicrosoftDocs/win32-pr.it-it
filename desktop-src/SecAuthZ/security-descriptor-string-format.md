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
# <a name="security-descriptor-string-format"></a>Formato stringa descrittore di sicurezza

Il **formato di stringa del descrittore di** sicurezza è un formato di testo per l'archiviazione o il trasporto di informazioni in un descrittore di sicurezza. Le [**funzioni ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) e [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) usano questo formato.

Il formato è una stringa con terminazione **Null** con token per indicare ognuno dei quattro componenti principali di un descrittore di sicurezza: owner (O:), primary group (G:), DACL (D:) e SACL (S:).

> [!Note]  
> [*Le voci di controllo di accesso*](/windows/desktop/SecGloss/a-gly) (ACE) e le voci ACE condizionali hanno formati diversi. Per le ACE, vedere [Stringhe ACE](ace-strings.md). Per le ACE condizionali, vedere [Linguaggio di definizione del descrittore di sicurezza per le ACE condizionali.](security-descriptor-definition-language-for-conditional-aces-.md)

 


```C++
O:owner_sid
G:group_sid
D:dacl_flags(string_ace1)(string_ace2)... (string_acen)
S:sacl_flags(string_ace1)(string_ace2)... (string_acen)
```



<dl> <dt>

<span id="owner_sid"></span><span id="OWNER_SID"></span>owner \_ sid
</dt> <dd>

Stringa [SID che](sid-strings.md) identifica il proprietario dell'oggetto.

</dd> <dt>

<span id="group_sid"></span><span id="GROUP_SID"></span>group \_ sid
</dt> <dd>

Stringa SID che identifica il gruppo primario dell'oggetto.

</dd> <dt>

<span id="dacl_flags"></span><span id="DACL_FLAGS"></span>flag \_ dacl
</dt> <dd>

Flag di controllo del descrittore di sicurezza che si applicano all'elenco DACL. Per una descrizione di questi flag di controllo, vedere la [**funzione SetSecurityDescriptorControl.**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorcontrol) La stringa flag dacl può essere una concatenazione di \_ zero o più stringhe seguenti.



| Control               | Costante in Sddl.h       | Significato                                       |
|-----------------------|--------------------------|-----------------------------------------------|
| "P"                   | SDDL \_ PROTECTED          | Il \_ flag SE DACL \_ PROTECTED è impostato.          |
| "AR"                  | SDDL \_ AUTO \_ INHERIT \_ REQ | Il \_ flag SE DACL \_ AUTO INHERIT \_ \_ REQ è impostato. |
| "AI"                  | SDDL \_ \_ EREDITATO AUTOMATICAMENTE    | Il \_ flag SE DACL \_ AUTO \_ INHERITED è impostato.    |
| "NO \_ ACCESS \_ CONTROL" | SDDL \_ NULL \_ ACL          | L'ACL è Null. **Windows Server 2008, Windows Vista e Windows Server 2003:** Non disponibile. |



 

</dd> <dt>

<span id="sacl_flags"></span><span id="SACL_FLAGS"></span>flag \_ sacl
</dt> <dd>

Flag di controllo del descrittore di sicurezza che si applicano all'elenco SACL. La stringa dei flag sacl \_ usa le stesse stringhe di bit di controllo della stringa dei flag dacl. \_

</dd> <dt>

<span id="string_ace"></span><span id="STRING_ACE"></span>string \_ ace
</dt> <dd>

Stringa che descrive una ACE nell'elenco DACL o SACL del descrittore di sicurezza. Per una descrizione del formato di stringa ACE, vedere [Stringhe ACE.](ace-strings.md) Ogni stringa ACE è racchiusa tra parentesi (()).

</dd> </dl>

I componenti non necessari possono essere omessi dalla stringa del descrittore di sicurezza. Ad esempio, se il flag SE DACL PRESENT non è impostato nel descrittore di sicurezza di \_ \_ input, [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) non include un componente D: nella stringa di output. È anche possibile usare i flag di bit [**SECURITY \_ INFORMATION**](security-information.md) per indicare i componenti da includere in una stringa del descrittore di sicurezza.

Il formato della stringa del descrittore di sicurezza non supporta **gli ACL NULL.**

Per indicare un elenco di controllo di accesso vuoto, la stringa del descrittore di sicurezza include il token D: o S: senza informazioni aggiuntive sulla stringa.

La stringa del descrittore di sicurezza archivia i bit [**SECURITY DESCRIPTOR CONTROL**](security-descriptor-control.md) in modi diversi. I bit SE DACL PRESENT o SE SACL PRESENT sono indicati dalla presenza del token D: o \_ \_ \_ \_ S: nella stringa. Altri bit che si applicano all'elenco DACL o a SACL vengono archiviati in flag dacl \_ e flag \_ sacl. I bit SE \_ OWNER \_ DEFAULTED, SE \_ GROUP \_ DEFAULTED, SE \_ DACL DEFAULTED e SE \_ SACL DEFAULTED non vengono \_ \_ archiviati in una stringa del descrittore di sicurezza. Il bit SE SELF RELATIVE non viene archiviato nella stringa, ma \_ \_ [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) imposta sempre questo bit nel descrittore di sicurezza di output.

Gli esempi seguenti illustrano le stringhe dei descrittori di sicurezza e le informazioni nei descrittori di sicurezza associati.

Stringa 1:


```C++
"O:AOG:DAD:(A;;RPWPCCDCLCSWRCWDWOGA;;;S-1-0-0)"
```



Descrittore di sicurezza 1:


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



Stringa 2:


```C++
"O:DAG:DAD:(A;;RPWPCCDCLCRCWOWDSDSW;;;SY)
(A;;RPWPCCDCLCRCWOWDSDSW;;;DA)
(OA;;CCDC;bf967aba-0de6-11d0-a285-00aa003049e2;;AO)
(OA;;CCDC;bf967a9c-0de6-11d0-a285-00aa003049e2;;AO)
(OA;;CCDC;6da8a4ff-0e52-11d0-a286-00aa003049e2;;AO)
(OA;;CCDC;bf967aa8-0de6-11d0-a285-00aa003049e2;;PO)
(A;;RPLCRC;;;AU)S:(AU;SAFA;WDWOSDWPCCDCSW;;;WD)"
```



Descrittore di sicurezza 2:


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Stringhe ACE](ace-strings.md)
</dt> <dt>

[Linguaggio di definizione del descrittore di sicurezza per le ACE condizionali](security-descriptor-definition-language-for-conditional-aces-.md)
</dt> </dl>

 

 
