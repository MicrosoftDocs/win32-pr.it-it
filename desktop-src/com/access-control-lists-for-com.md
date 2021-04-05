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
# <a name="access-control-lists-for-com"></a><span data-ttu-id="6a3e9-103">Elenchi di controllo di accesso per COM</span><span class="sxs-lookup"><span data-stu-id="6a3e9-103">Access Control Lists for COM</span></span>

<span data-ttu-id="6a3e9-104">Windows Server XP Service Pack 2 (SP 2) e Windows Server 2003 Service Pack 1 (SP 1) introducono miglioramenti per la sicurezza per Distributed Component Object Model (DCOM).</span><span class="sxs-lookup"><span data-stu-id="6a3e9-104">Windows Server XP Service Pack 2 (SP 2) and Windows Server 2003 Service Pack 1 (SP 1) introduce security enhancements for the Distributed Component Object Model (DCOM).</span></span> <span data-ttu-id="6a3e9-105">Uno di questi miglioramenti è costituito da diritti di accesso più specifici per l'utilizzo in elenchi di controllo di accesso (ACL).</span><span class="sxs-lookup"><span data-stu-id="6a3e9-105">One of these enhancements is more specific access rights for use in access control lists (ACLs).</span></span> <span data-ttu-id="6a3e9-106">I diritti di accesso sono:</span><span class="sxs-lookup"><span data-stu-id="6a3e9-106">The access rights are:</span></span>

``` syntax
COM_RIGHTS_EXECUTE 1
COM_RIGHTS_EXECUTE_LOCAL 2
COM_RIGHTS_EXECUTE_REMOTE 4
COM_RIGHTS_ACTIVATE_LOCAL 8
COM_RIGHTS_ACTIVATE_REMOTE 16
```

<span data-ttu-id="6a3e9-107">Per garantire la compatibilità con le versioni precedenti, è possibile che esista un ACL nel formato utilizzato prima di Windows XP SP 2 e Windows Server 2003 SP 1, che utilizza solo i diritti di accesso COM Rights \_ \_ Execute oppure può esistere nel nuovo formato utilizzato in Windows XP SP 2 e windows Server 2003 SP 1, che utilizza \_ i diritti com \_ Execute insieme a una combinazione di \_ diritti com \_ Execute \_ local, com \_ Rights \_ Execute \_ remote, com \_ Rights \_ Activate \_ local e com \_ Rights \_ Activate \_ remote.</span><span class="sxs-lookup"><span data-stu-id="6a3e9-107">To provide backward compatibility, an ACL may exist in the format used before Windows XP SP 2 and Windows Server 2003 SP 1, which uses only the access right COM\_RIGHTS\_EXECUTE, or it may exist in the new format used in Windows XP SP 2 and Windows Server 2003 SP 1, which uses COM\_RIGHTS\_EXECUTE together with a combination of COM\_RIGHTS\_EXECUTE\_LOCAL, COM\_RIGHTS\_EXECUTE\_REMOTE, COM\_RIGHTS\_ACTIVATE\_LOCAL, and COM\_RIGHTS\_ACTIVATE\_REMOTE.</span></span>

> [!Note]  
> <span data-ttu-id="6a3e9-108">\_L'esecuzione dei diritti com \_ deve essere sempre presente. l'assenza di questo diritto genera un descrittore di sicurezza non valido.</span><span class="sxs-lookup"><span data-stu-id="6a3e9-108">COM\_RIGHTS\_EXECUTE must always be present; the absence of this right generates an invalid security descriptor.</span></span>

 

<span data-ttu-id="6a3e9-109">Non è necessario combinare il vecchio formato e il nuovo formato all'interno di un singolo ACL. tutte le voci di controllo di accesso (ACE) devono concedere solo \_ il \_ diritto di accesso Execute Rights Execute oppure tutti devono concedere i \_ diritti com \_ Execute insieme a una combinazione di \_ diritti com \_ Execute \_ local, com \_ Rights \_ Execute \_ remote, com \_ Rights \_ Activate \_ local e com \_ Rights \_ Activate \_ remote.</span><span class="sxs-lookup"><span data-stu-id="6a3e9-109">You must not mix the old format and the new format within a single ACL; either all access control entries (ACEs) must grant only the COM\_RIGHTS\_EXECUTE access right, or they all must grant COM\_RIGHTS\_EXECUTE together with a combination of COM\_RIGHTS\_EXECUTE\_LOCAL, COM\_RIGHTS\_EXECUTE\_REMOTE, COM\_RIGHTS\_ACTIVATE\_LOCAL, and COM\_RIGHTS\_ACTIVATE\_REMOTE.</span></span>

<span data-ttu-id="6a3e9-110">Di seguito è riportato un esempio di un ACL formattato in modo non corretto:</span><span class="sxs-lookup"><span data-stu-id="6a3e9-110">The following is an example of an incorrectly formatted ACL:</span></span>

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

<span data-ttu-id="6a3e9-111">Si noti che la prima voce di controllo di accesso (ACE) concede solo i diritti com \_ \_ Execute (0x1), mentre la seconda voce ACE concede \_ i diritti com \_ Execute, \_ i diritti com \_ eseguono \_ local e com \_ Rights \_ Activate \_ local (0xB) e il terzo concede i \_ diritti com \_ Execute e com \_ Rights \_ Activate \_ local (0x9).</span><span class="sxs-lookup"><span data-stu-id="6a3e9-111">Note that the first access control entry (ACE) grants COM\_RIGHTS\_EXECUTE (0x1) only, while the second ACE grants COM\_RIGHTS\_EXECUTE, COM\_RIGHTS\_EXECUTE\_LOCAL, and COM\_RIGHTS\_ACTIVATE\_LOCAL (0xb), and the third grants COM\_RIGHTS\_EXECUTE and COM\_RIGHTS\_ACTIVATE\_LOCAL (0x9).</span></span>

<span data-ttu-id="6a3e9-112">Per risolvere il problema, è necessario modificare la prima voce ACE in modo da concedere \_ diritti com \_ Execute in combinazione con uno degli altri quattro diritti di accesso. in caso contrario, è necessario modificare la seconda e la terza voce ACE per concedere solo l' \_ esecuzione dei diritti com \_ .</span><span class="sxs-lookup"><span data-stu-id="6a3e9-112">To correct this, the first ACE should be changed to grant COM\_RIGHTS\_EXECUTE in combination with one of the other four access rights, or else the second and third ACEs should be changed to grant only COM\_RIGHTS\_EXECUTE.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6a3e9-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6a3e9-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a3e9-114">Miglioramenti della protezione DCOM in Windows XP Service Pack 2 e Windows Server 2003 Service Pack 1</span><span class="sxs-lookup"><span data-stu-id="6a3e9-114">DCOM Security Enhancements in Windows XP Service Pack 2 and Windows Server 2003 Service Pack 1</span></span>](dcom-security-enhancements-in-windows-xp-service-pack-2-and-windows-server-2003-service-pack-1.md)
</dt> <dt>

[<span data-ttu-id="6a3e9-115">Sicurezza in COM</span><span class="sxs-lookup"><span data-stu-id="6a3e9-115">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 




