---
title: Elenchi di controllo di accesso per COM
description: Elenchi di controllo di accesso per COM
ms.assetid: ceb37563-7e7f-4704-b671-72ed65e3e102
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e50e1641691b1a2812e861a95c5bc0f7eac8f0f8af67d41b18287c07253b8d51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118551355"
---
# <a name="access-control-lists-for-com"></a>Elenchi di controllo di accesso per COM

Windows Server XP Service Pack 2 (SP 2) e Windows Server 2003 Service Pack 1 (SP 1) introducono miglioramenti per la sicurezza per Distributed Component Object Model (DCOM). Uno di questi miglioramenti è l'uso di diritti di accesso più specifici negli elenchi di controllo di accesso (ACL). I diritti di accesso sono:

``` syntax
COM_RIGHTS_EXECUTE 1
COM_RIGHTS_EXECUTE_LOCAL 2
COM_RIGHTS_EXECUTE_REMOTE 4
COM_RIGHTS_ACTIVATE_LOCAL 8
COM_RIGHTS_ACTIVATE_REMOTE 16
```

Per garantire la compatibilità con le versioni precedenti, Un ACL può esistere nel formato usato prima di Windows XP SP 2 e Windows Server 2003 SP 1, che usa solo il diritto di accesso COM RIGHTS EXECUTE, oppure può esistere nel nuovo formato usato in Windows XP SP 2 e \_ Windows Server 2003 SP 1, che usa COM RIGHTS EXECUTE insieme a una combinazione di \_ COM RIGHTS EXECUTE \_ \_ \_ \_ \_ LOCAL, COM RIGHTS EXECUTE REMOTE, COM RIGHTS ACTIVATE LOCAL e \_ COM RIGHTS \_ ACTIVATE \_ \_ \_ \_ \_ \_ \_ REMOTE.

> [!Note]  
> COM \_ RIGHTS EXECUTE deve essere sempre \_ presente. L'assenza di questo diritto genera un descrittore di sicurezza non valido.

 

Non è necessario combinare il formato precedente e il nuovo formato all'interno di un singolo ACL. Tutte le voci di controllo di accesso (ACE) devono concedere solo il diritto di accesso COM RIGHTS EXECUTE oppure tutte devono concedere COM RIGHTS EXECUTE insieme a una combinazione di \_ \_ COM RIGHTS EXECUTE \_ \_ \_ \_ \_ LOCAL, COM RIGHTS EXECUTE REMOTE, COM RIGHTS ACTIVATE LOCAL e \_ COM RIGHTS \_ ACTIVATE \_ \_ \_ \_ \_ \_ \_ REMOTE.

Di seguito è riportato un esempio di ACL formattato in modo non corretto:

``` syntax
Revision 1
Sbz1 0
Control 0x8004
    SE_DACL_PRESENT
    SE_SELF_RELATIVE
Owner: S-1-5-21-1597522630-148096252-1166023319-500 (no name mapped)
Group: S-1-5-21-1597522630-148096252-1166023319-500 (no name mapped)
DACL:
    AclRevision 2
    Sbz1 0
    AclSize 128
    AceCount 4
    Sbz2 0
    Ace[0]
        AceType 0: ACCESS_ALLOWED_ACE_TYPE
        AceFlags 0
        AceSize 36
        AccessMask 0x1
        S-1-5-21-1597522630-148096252-1166023319-500 (no name mapped)
    Ace[1]
        AceType 0: ACCESS_ALLOWED_ACE_TYPE
        AceFlags 0
        AceSize 20
        AccessMask 0xb
        S-1-5-18 (Well Known Group: NT AUTHORITY\SYSTEM)
    Ace[2]
        AceType 0: ACCESS_ALLOWED_ACE_TYPE
        AceFlags 0
        AceSize 20
        AccessMask 0x9
        S-1-5-11 (Well Known Group: NT AUTHORITY\Authenticated Users)
SACL:
    (null)
```

Si noti che la prima voce di controllo di accesso concede solo COM RIGHTS EXECUTE (0x1), mentre la seconda concede COM RIGHTS EXECUTE, COM RIGHTS EXECUTE LOCAL e COM RIGHTS ACTIVATE LOCAL (0xb) e la terza concede COM RIGHTS EXECUTE e \_ \_ COM RIGHTS ACTIVATE \_ \_ \_ \_ LOCAL \_ \_ \_ \_ \_ \_ \_ \_ \_ (0x9).

Per risolvere questo problema, è necessario modificare la prima ACE per concedere COM RIGHTS EXECUTE in combinazione con uno degli altri quattro diritti di accesso. In caso contrario, la seconda e la terza ACE devono essere modificate per concedere solo \_ \_ COM RIGHTS \_ \_ EXECUTE.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Miglioramenti della sicurezza DCOM in Windows XP Service Pack 2 e Windows Server 2003 Service Pack 1](dcom-security-enhancements-in-windows-xp-service-pack-2-and-windows-server-2003-service-pack-1.md)
</dt> <dt>

[Sicurezza in COM](security-in-com.md)
</dt> </dl>

 

 




