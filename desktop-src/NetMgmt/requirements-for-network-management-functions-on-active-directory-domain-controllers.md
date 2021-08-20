---
title: Requisiti per le funzioni di gestione di rete nei controller Dominio di Active Directory rete
description: Se si chiama una delle funzioni di gestione di rete elencate in questo argomento in un controller di dominio che esegue Active Directory, l'accesso a un oggetto a protezione diretta è consentito o negato in base all'elenco di controllo di accesso (ACL) per l'oggetto.
ms.assetid: 4dfb3180-3ca5-4e22-b7a1-4e6b132431fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67326708e2b3c83d1e41ace30c2813ccd2449193530fd4affca450d8a0538961
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117983260"
---
# <a name="requirements-for-network-management-functions-on-active-directory-domain-controllers"></a>Requisiti per le funzioni di gestione di rete nei controller Dominio di Active Directory rete

Se si chiama una delle funzioni di gestione di rete elencate in questo argomento in un controller di dominio che esegue Active Directory, l'accesso [a](/windows/desktop/SecAuthZ/securable-objects) un oggetto a protezione diretta è consentito o negato in base all'elenco di controllo di accesso [](/windows/desktop/SecAuthZ/access-control-lists) (ACL) per l'oggetto. Gli elenchi di controllo di accesso sono specificati nella directory .

Requisiti di accesso diversi si applicano alle query di informazioni e agli aggiornamenti delle informazioni.

## <a name="queries"></a>Query

Per le query, l'ACL predefinito consente a tutti gli utenti autenticati e ai membri del gruppo " Accesso compatibile con le versioni di[pre-Windows 2000](/windows/desktop/SecAuthZ/allowing-anonymous-access)" di leggere ed enumerare le informazioni. Sono interessate le funzioni elencate di seguito:

-   [**NetGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupenum), [**NetGroupGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetinfo), [**NetGroupGetUsers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetusers)
-   [**NetLocalGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupenum), [**NetLocalGroupGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetinfo), [**NetLocalGroupGetMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetmembers)
-   [**NetQueryDisplayInformation**](/windows/desktop/api/Lmaccess/nf-lmaccess-netquerydisplayinformation)
-   [**NetSessionGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netsessiongetinfo) (solo livelli 1 e 2)
-   [**NetShareEnum**](/windows/desktop/api/lmshare/nf-lmshare-netshareenum) (solo livelli 2 e 502)
-   [**NetUserEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserenum), [**NetUserGetGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetgroups), [**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo), [**NetUserGetLocalGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetlocalgroups), [**NetUserModalsGet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsget)
-   [**NetWkstaGetInfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstagetinfo), [ **NetWkstaUserEnum**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstauserenum)

L'accesso anonimo alle informazioni sui gruppi richiede che l'utente Anonimo venga aggiunto in modo esplicito al gruppo "Accesso compatibile con Windows 2000". Questo perché i token anonimi non includono il SID del gruppo Everyone.

**Windows 2000:** Per impostazione predefinita, il gruppo "Accesso Windows 2000" include Tutti come membro. Ciò consente l'accesso anonimo (accesso anonimo) alle informazioni se il sistema consente l'accesso anonimo. Gli amministratori possono rimuovere Everyone dal gruppo "Accesso Windows 2000" in qualsiasi momento. La rimozione di Everyone dal gruppo limita l'accesso alle informazioni solo agli utenti autenticati. Per altre informazioni sull'accesso anonimo, vedere [Id di sicurezza](/windows/desktop/SecAuthZ/security-identifiers) e [SID noti.](/windows/desktop/SecAuthZ/well-known-sids)

È possibile eseguire l'override dell'impostazione predefinita del sistema impostando la chiave seguente nel Registro di sistema sul valore 1:

**HKEY \_ LOCAL \_ MACHINE \\ SYSTEM \\ CurrentControlSet \\ Control \\ Lsa** \\ **EveryoneIncludesAnonymous** = 1

Per altre informazioni sull'accesso anonimo alle informazioni sui gruppi quando si chiamano queste due funzioni, vedere [**NetWkstaGetInfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstagetinfo) e [**NetWkstaUserEnum.**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstauserenum)

## <a name="updates"></a>Aggiornamenti

Per gli aggiornamenti, l'ACL predefinito consente solo agli amministratori di dominio e agli operatori account di scrivere informazioni. Un'eccezione è che gli utenti possono modificare la propria password e impostare il campo del commento \* \_ usri \_ usr. Un'altra eccezione è che gli operatori account non possono modificare gli account di amministrazione. Sono interessate le funzioni elencate di seguito:

-   [**NetGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadd), [**NetGroupAddUser**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadduser), [**NetGroupDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupdel), [**NetGroupDelUser**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupdeluser), [**NetGroupSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetinfo), [**NetGroupSetUsers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetusers)
-   [**NetLocalGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupadd), [**NetLocalGroupAddMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupaddmembers), [**NetLocalGroupDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupdel), [**NetLocalGroupDelMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupdelmembers), [**NetLocalGroupSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupsetinfo), [**NetLocalGroupSetMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupsetmembers)
-   [**NetMessageBufferSend**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagebuffersend)
-   [**NetUserAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd), [**NetUserChangePassword**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserchangepassword), [**NetUserDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserdel), [**NetUserModalsSet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsset), [**NetUserSetGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetgroups), [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo)

In genere, i chiamanti devono avere accesso in scrittura all'intero oggetto perché le chiamate a [**NetUserModalsSet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsset), [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo), [**NetGroupSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetinfo) e [**NetLocalGroupSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupsetinfo) riescano. Per un controllo di accesso più fine, è consigliabile usare ADSI. Per altre informazioni su ADSI, vedere [Interfacce del servizio Active Directory.](/windows/desktop/ADSI/active-directory-service-interfaces-adsi)

Per altre informazioni sul controllo dell'accesso agli oggetti a protezione diretta, vedere [Controllo](/windows/desktop/SecAuthZ/access-control)di accesso , [privilegi](/windows/desktop/SecAuthZ/privileges)e [oggetti a protezione diretta](/windows/desktop/SecAuthZ/securable-objects). Per altre informazioni sulla chiamata di funzioni che richiedono privilegi di amministratore, vedere [Esecuzione con privilegi speciali.](/windows/desktop/SecBP/running-with-special-privileges)

 

 