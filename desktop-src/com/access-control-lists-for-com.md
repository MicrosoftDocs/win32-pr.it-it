---
title: Elenchi di controllo di accesso per COM
description: Elenchi di controllo di accesso per COM
ms.assetid: ceb37563-7e7f-4704-b671-72ed65e3e102
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 811b6cdbca36ef75bb5ee3f185b0261967d736d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709262"
---
# <a name="access-control-lists-for-com"></a>Elenchi di controllo di accesso per COM

Windows Server XP Service Pack 2 (SP 2) e Windows Server 2003 Service Pack 1 (SP 1) introducono miglioramenti per la sicurezza per Distributed Component Object Model (DCOM). Uno di questi miglioramenti è costituito da diritti di accesso più specifici per l'utilizzo in elenchi di controllo di accesso (ACL). I diritti di accesso sono:

``` syntax
COM_RIGHTS_EXECUTE 1
COM_RIGHTS_EXECUTE_LOCAL 2
COM_RIGHTS_EXECUTE_REMOTE 4
COM_RIGHTS_ACTIVATE_LOCAL 8
COM_RIGHTS_ACTIVATE_REMOTE 16
```

Per garantire la compatibilità con le versioni precedenti, è possibile che esista un ACL nel formato utilizzato prima di Windows XP SP 2 e Windows Server 2003 SP 1, che utilizza solo i diritti di accesso COM Rights \_ \_ Execute oppure può esistere nel nuovo formato utilizzato in Windows XP SP 2 e windows Server 2003 SP 1, che utilizza \_ i diritti com \_ Execute insieme a una combinazione di \_ diritti com \_ Execute \_ local, com \_ Rights \_ Execute \_ remote, com \_ Rights \_ Activate \_ local e com \_ Rights \_ Activate \_ remote.

> [!Note]  
> \_L'esecuzione dei diritti com \_ deve essere sempre presente. l'assenza di questo diritto genera un descrittore di sicurezza non valido.

 

Non è necessario combinare il vecchio formato e il nuovo formato all'interno di un singolo ACL. tutte le voci di controllo di accesso (ACE) devono concedere solo \_ il \_ diritto di accesso Execute Rights Execute oppure tutti devono concedere i \_ diritti com \_ Execute insieme a una combinazione di \_ diritti com \_ Execute \_ local, com \_ Rights \_ Execute \_ remote, com \_ Rights \_ Activate \_ local e com \_ Rights \_ Activate \_ remote.

Di seguito è riportato un esempio di un ACL formattato in modo non corretto:

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

Si noti che la prima voce di controllo di accesso (ACE) concede solo i diritti com \_ \_ Execute (0x1), mentre la seconda voce ACE concede \_ i diritti com \_ Execute, \_ i diritti com \_ eseguono \_ local e com \_ Rights \_ Activate \_ local (0xB) e il terzo concede i \_ diritti com \_ Execute e com \_ Rights \_ Activate \_ local (0x9).

Per risolvere il problema, è necessario modificare la prima voce ACE in modo da concedere \_ diritti com \_ Execute in combinazione con uno degli altri quattro diritti di accesso. in caso contrario, è necessario modificare la seconda e la terza voce ACE per concedere solo l' \_ esecuzione dei diritti com \_ .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Miglioramenti della protezione DCOM in Windows XP Service Pack 2 e Windows Server 2003 Service Pack 1](dcom-security-enhancements-in-windows-xp-service-pack-2-and-windows-server-2003-service-pack-1.md)
</dt> <dt>

[Sicurezza in COM](security-in-com.md)
</dt> </dl>

 

 




