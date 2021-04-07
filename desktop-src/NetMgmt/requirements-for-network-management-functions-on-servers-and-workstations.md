---
title: Requisiti per le funzioni di gestione della rete su server e workstation
description: Se si chiama una delle funzioni di gestione di rete elencate in questo argomento su un server o una workstation, i requisiti di accesso diversi si applicano alle query di informazioni e agli aggiornamenti delle informazioni.
ms.assetid: 05ff1771-8058-4c86-8f45-735bf41dc128
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b06e516aa06465c67966cc076a0ca524d4ae4003
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872869"
---
# <a name="requirements-for-network-management-functions-on-servers-and-workstations"></a>Requisiti per le funzioni di gestione della rete su server e workstation

Se si chiama una delle funzioni di gestione di rete elencate in questo argomento su un server o una workstation, i requisiti di accesso diversi si applicano alle query di informazioni e agli aggiornamenti delle informazioni.

## <a name="queries"></a>Query

Se si chiama una delle funzioni seguenti per eseguire una query su un server o una workstation, per impostazione predefinita tutti gli utenti autenticati possono leggere ed enumerare le informazioni.

-   [**NetGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupenum), [**NetGroupGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetinfo), [**NetGroupGetUsers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetusers)
-   [**NetLocalGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupenum), [**NetLocalGroupGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetinfo), [**NetLocalGroupGetMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetmembers)
-   [**NetQueryDisplayInformation**](/windows/desktop/api/Lmaccess/nf-lmaccess-netquerydisplayinformation)
-   [**NetSessionGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netsessiongetinfo) (solo livelli 1 e 2)
-   [**NetShareEnum**](/windows/desktop/api/lmshare/nf-lmshare-netshareenum) (solo livelli 2 e 502)
-   [**NetUserEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserenum), [**NetUserGetGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetgroups), [**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo), [**funzione NetUserGetLocalGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetlocalgroups), [**NetUserModalsGet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsget)
-   [**NetWkstaGetInfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstagetinfo), [ **NetWkstaUserEnum**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstauserenum)

Di seguito sono riportate informazioni aggiuntive sull'accesso anonimo durante la lettura e l'enumerazione delle informazioni.

**Windows Server 2003 e Windows XP:** L'accesso anonimo alle informazioni è possibile se l'impostazione dei criteri EveryoneIncludesAnonymous consente l'accesso anonimo.

**Windows 2000:** L'accesso anonimo a oggetti a protezione diretta è possibile se l'impostazione dei criteri RestrictAnonymous consente l'accesso anonimo. È possibile limitare l'accesso anonimo impostando la chiave seguente nel registro di sistema sul valore 1.

**HKEY \_ \_Controllo CurrentControlSet di sistema del computer locale \\ \\ \\ \\ LSA** \\ **RestrictAnonymous** = 1

Per ulteriori informazioni, vedere l'articolo seguente della Microsoft Knowledge Base:

ID articolo: [Q246261](https://support.microsoft.com/kb/246261)

TITLE: come usare il valore del registro di sistema RestrictAnonymous.

## <a name="updates"></a>Aggiornamenti

Per impostazione predefinita, solo gli amministratori e gli utenti esperti possono scrivere informazioni.

Per ulteriori informazioni sul controllo dell'accesso agli oggetti a protezione diretta, vedere [controllo di accesso](/windows/desktop/SecAuthZ/access-control), [privilegi](/windows/desktop/SecAuthZ/privileges)e [oggetti a protezione diretta](/windows/desktop/SecAuthZ/securable-objects). Per ulteriori informazioni sulla chiamata di funzioni che richiedono privilegi di amministratore, vedere [esecuzione con privilegi speciali](/windows/desktop/SecBP/running-with-special-privileges).

 

 