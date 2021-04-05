---
title: Requisiti per le funzioni di gestione della rete nei controller di Dominio di Active Directory
description: Se si chiama una delle funzioni di gestione di rete elencate in questo argomento in un controller di dominio che esegue Active Directory, l'accesso a un oggetto a protezione diretta è consentito o negato in base all'elenco di controllo di accesso (ACL) per l'oggetto.
ms.assetid: 4dfb3180-3ca5-4e22-b7a1-4e6b132431fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8c6b646290ef6352a529a37243a6ea30c8b0d39
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872634"
---
# <a name="requirements-for-network-management-functions-on-active-directory-domain-controllers"></a>Requisiti per le funzioni di gestione della rete nei controller di Dominio di Active Directory

Se si chiama una delle funzioni di gestione di rete elencate in questo argomento in un controller di dominio che esegue Active Directory, l'accesso a un [oggetto a protezione diretta](/windows/desktop/SecAuthZ/securable-objects) è consentito o negato in base all' [elenco di controllo di accesso](/windows/desktop/SecAuthZ/access-control-lists) (ACL) per l'oggetto. Gli ACL vengono specificati nella directory.

Requisiti di accesso diversi si applicano alle query di informazioni e agli aggiornamenti delle informazioni.

## <a name="queries"></a>Query

Per le query, l'ACL predefinito consente a tutti gli utenti autenticati e ai membri del gruppo "[Accesso compatibile precedente a Windows 2000](/windows/desktop/SecAuthZ/allowing-anonymous-access)" di leggere ed enumerare le informazioni. Sono interessate le funzioni elencate di seguito:

-   [**NetGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupenum), [**NetGroupGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetinfo), [**NetGroupGetUsers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetusers)
-   [**NetLocalGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupenum), [**NetLocalGroupGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetinfo), [**NetLocalGroupGetMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetmembers)
-   [**NetQueryDisplayInformation**](/windows/desktop/api/Lmaccess/nf-lmaccess-netquerydisplayinformation)
-   [**NetSessionGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netsessiongetinfo) (solo livelli 1 e 2)
-   [**NetShareEnum**](/windows/desktop/api/lmshare/nf-lmshare-netshareenum) (solo livelli 2 e 502)
-   [**NetUserEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserenum), [**NetUserGetGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetgroups), [**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo), [**funzione NetUserGetLocalGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetlocalgroups), [**NetUserModalsGet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsget)
-   [**NetWkstaGetInfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstagetinfo), [ **NetWkstaUserEnum**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstauserenum)

Per l'accesso anonimo alle informazioni sul gruppo è necessario che l'utente anonimo venga aggiunto esplicitamente al gruppo "accesso compatibile precedente a Windows 2000". Questo perché i token anonimi non includono il SID del gruppo Everyone.

**Windows 2000:** Per impostazione predefinita, il gruppo "accesso compatibile precedente a Windows 2000" include tutti gli utenti come membri. Questo consente l'accesso anonimo (accesso anonimo) alle informazioni se il sistema consente l'accesso anonimo. Gli amministratori possono rimuovere tutti gli utenti dal gruppo "accesso compatibile precedente a Windows 2000" in qualsiasi momento. La rimozione di tutti dal gruppo limita l'accesso alle informazioni solo agli utenti autenticati. Per ulteriori informazioni sull'accesso anonimo, vedere [ID di sicurezza](/windows/desktop/SecAuthZ/security-identifiers) e [SID noti](/windows/desktop/SecAuthZ/well-known-sids).

È possibile eseguire l'override dell'impostazione predefinita del sistema impostando la chiave seguente nel registro di sistema sul valore 1:

**HKEY \_ \_Controllo CurrentControlSet di sistema del computer locale \\ \\ \\ \\ LSA** \\ **EveryoneIncludesAnonymous** = 1

Per ulteriori informazioni sull'accesso anonimo alle informazioni sul gruppo quando si chiamano queste due funzioni, vedere [**NetWkstaGetInfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstagetinfo) e [**NetWkstaUserEnum**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstauserenum) .

## <a name="updates"></a>Aggiornamenti

Per gli aggiornamenti, l'ACL predefinito consente solo agli amministratori di dominio e agli operatori di account di scrivere le informazioni. Un'eccezione è che gli utenti possono modificare la propria password e impostare il \* \_ campo del commento usr usri \_ . Un'altra eccezione è che gli operatori account non possono modificare gli account di amministrazione. Sono interessate le funzioni elencate di seguito:

-   [**NetGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadd), [**NetGroupAddUser**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadduser), [**NetGroupDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupdel), [**NetGroupDelUser**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupdeluser), [**NetGroupSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetinfo), [**NetGroupSetUsers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetusers)
-   [**NetLocalGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupadd), [**NetlocalgroupAddMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupaddmembers), [**NetLocalGroupDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupdel), [**NetLocalGroupDelMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupdelmembers), [**NetLocalGroupSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupsetinfo), [**NetLocalGroupSetMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupsetmembers)
-   [**NetMessageBufferSend**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagebuffersend)
-   [**NetUserAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd), [**NetUserChangePassword**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserchangepassword), [**NetUserDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserdel), [**NetUserModalsSet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsset), [**NetUserSetGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetgroups), [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo)

In genere, i chiamanti devono avere accesso in scrittura all'intero oggetto per le chiamate a [**NetUserModalsSet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsset), [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo), [**NetGroupSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetinfo) e [**NetLocalGroupSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupsetinfo) per avere esito positivo. Per un controllo di accesso più preciso, è consigliabile utilizzare ADSI. Per ulteriori informazioni su ADSI, vedere [Active Directory interfacce del servizio](/windows/desktop/ADSI/active-directory-service-interfaces-adsi).

Per ulteriori informazioni sul controllo dell'accesso agli oggetti a protezione diretta, vedere [controllo di accesso](/windows/desktop/SecAuthZ/access-control), [privilegi](/windows/desktop/SecAuthZ/privileges)e [oggetti a protezione diretta](/windows/desktop/SecAuthZ/securable-objects). Per ulteriori informazioni sulla chiamata di funzioni che richiedono privilegi di amministratore, vedere [esecuzione con privilegi speciali](/windows/desktop/SecBP/running-with-special-privileges).

 

 