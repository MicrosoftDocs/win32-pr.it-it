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
# <a name="requirements-for-network-management-functions-on-servers-and-workstations"></a><span data-ttu-id="772d5-103">Requisiti per le funzioni di gestione della rete su server e workstation</span><span class="sxs-lookup"><span data-stu-id="772d5-103">Requirements for Network Management Functions on Servers and Workstations</span></span>

<span data-ttu-id="772d5-104">Se si chiama una delle funzioni di gestione di rete elencate in questo argomento su un server o una workstation, i requisiti di accesso diversi si applicano alle query di informazioni e agli aggiornamenti delle informazioni.</span><span class="sxs-lookup"><span data-stu-id="772d5-104">If you call one of the network management functions listed in this topic on a server or workstation, different access requirements apply to information queries and information updates.</span></span>

## <a name="queries"></a><span data-ttu-id="772d5-105">Query</span><span class="sxs-lookup"><span data-stu-id="772d5-105">Queries</span></span>

<span data-ttu-id="772d5-106">Se si chiama una delle funzioni seguenti per eseguire una query su un server o una workstation, per impostazione predefinita tutti gli utenti autenticati possono leggere ed enumerare le informazioni.</span><span class="sxs-lookup"><span data-stu-id="772d5-106">If you call one of the following functions to perform a query on a server or workstation, by default, all authenticated users can read and enumerate the information.</span></span>

-   <span data-ttu-id="772d5-107">[**NetGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupenum), [**NetGroupGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetinfo), [**NetGroupGetUsers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetusers)</span><span class="sxs-lookup"><span data-stu-id="772d5-107">[**NetGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupenum), [**NetGroupGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetinfo), [**NetGroupGetUsers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetusers)</span></span>
-   <span data-ttu-id="772d5-108">[**NetLocalGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupenum), [**NetLocalGroupGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetinfo), [**NetLocalGroupGetMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetmembers)</span><span class="sxs-lookup"><span data-stu-id="772d5-108">[**NetLocalGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupenum), [**NetLocalGroupGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetinfo), [**NetLocalGroupGetMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetmembers)</span></span>
-   [<span data-ttu-id="772d5-109">**NetQueryDisplayInformation**</span><span class="sxs-lookup"><span data-stu-id="772d5-109">**NetQueryDisplayInformation**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netquerydisplayinformation)
-   <span data-ttu-id="772d5-110">[**NetSessionGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netsessiongetinfo) (solo livelli 1 e 2)</span><span class="sxs-lookup"><span data-stu-id="772d5-110">[**NetSessionGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netsessiongetinfo) (levels 1 and 2 only)</span></span>
-   <span data-ttu-id="772d5-111">[**NetShareEnum**](/windows/desktop/api/lmshare/nf-lmshare-netshareenum) (solo livelli 2 e 502)</span><span class="sxs-lookup"><span data-stu-id="772d5-111">[**NetShareEnum**](/windows/desktop/api/lmshare/nf-lmshare-netshareenum) (levels 2 and 502 only)</span></span>
-   <span data-ttu-id="772d5-112">[**NetUserEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserenum), [**NetUserGetGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetgroups), [**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo), [**funzione NetUserGetLocalGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetlocalgroups), [**NetUserModalsGet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsget)</span><span class="sxs-lookup"><span data-stu-id="772d5-112">[**NetUserEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserenum), [**NetUserGetGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetgroups), [**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo), [**NetUserGetLocalGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetlocalgroups), [**NetUserModalsGet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsget)</span></span>
-   <span data-ttu-id="772d5-113">[**NetWkstaGetInfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstagetinfo), [ **NetWkstaUserEnum**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstauserenum)</span><span class="sxs-lookup"><span data-stu-id="772d5-113">[**NetWkstaGetInfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstagetinfo), [**NetWkstaUserEnum**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstauserenum)</span></span>

<span data-ttu-id="772d5-114">Di seguito sono riportate informazioni aggiuntive sull'accesso anonimo durante la lettura e l'enumerazione delle informazioni.</span><span class="sxs-lookup"><span data-stu-id="772d5-114">Following is additional information about anonymous access when reading and enumerating information.</span></span>

<span data-ttu-id="772d5-115">**Windows Server 2003 e Windows XP:** L'accesso anonimo alle informazioni è possibile se l'impostazione dei criteri EveryoneIncludesAnonymous consente l'accesso anonimo.</span><span class="sxs-lookup"><span data-stu-id="772d5-115">**Windows Server 2003 and Windows XP:** Anonymous access to information is possible if the EveryoneIncludesAnonymous policy setting allows anonymous access.</span></span>

<span data-ttu-id="772d5-116">**Windows 2000:** L'accesso anonimo a oggetti a protezione diretta è possibile se l'impostazione dei criteri RestrictAnonymous consente l'accesso anonimo.</span><span class="sxs-lookup"><span data-stu-id="772d5-116">**Windows 2000:** Anonymous access to securable objects is possible if the RestrictAnonymous policy setting allows anonymous access.</span></span> <span data-ttu-id="772d5-117">È possibile limitare l'accesso anonimo impostando la chiave seguente nel registro di sistema sul valore 1.</span><span class="sxs-lookup"><span data-stu-id="772d5-117">You can restrict anonymous access by setting the following key in the registry to the value 1.</span></span>

<span data-ttu-id="772d5-118">**HKEY \_ \_Controllo CurrentControlSet di sistema del computer locale \\ \\ \\ \\ LSA** \\ **RestrictAnonymous** = 1</span><span class="sxs-lookup"><span data-stu-id="772d5-118">**HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Control\\Lsa**\\**RestrictAnonymous** = 1</span></span>

<span data-ttu-id="772d5-119">Per ulteriori informazioni, vedere l'articolo seguente della Microsoft Knowledge Base:</span><span class="sxs-lookup"><span data-stu-id="772d5-119">For more information, see the following article in the Microsoft Knowledge Base:</span></span>

<span data-ttu-id="772d5-120">ID articolo: [Q246261](https://support.microsoft.com/kb/246261)</span><span class="sxs-lookup"><span data-stu-id="772d5-120">ARTICLE ID: [Q246261](https://support.microsoft.com/kb/246261)</span></span>

<span data-ttu-id="772d5-121">TITLE: come usare il valore del registro di sistema RestrictAnonymous.</span><span class="sxs-lookup"><span data-stu-id="772d5-121">TITLE: How to use the RestrictAnonymous registry Value.</span></span>

## <a name="updates"></a><span data-ttu-id="772d5-122">Aggiornamenti</span><span class="sxs-lookup"><span data-stu-id="772d5-122">Updates</span></span>

<span data-ttu-id="772d5-123">Per impostazione predefinita, solo gli amministratori e gli utenti esperti possono scrivere informazioni.</span><span class="sxs-lookup"><span data-stu-id="772d5-123">By default, only Administrators and Power Users can write information.</span></span>

<span data-ttu-id="772d5-124">Per ulteriori informazioni sul controllo dell'accesso agli oggetti a protezione diretta, vedere [controllo di accesso](/windows/desktop/SecAuthZ/access-control), [privilegi](/windows/desktop/SecAuthZ/privileges)e [oggetti a protezione diretta](/windows/desktop/SecAuthZ/securable-objects).</span><span class="sxs-lookup"><span data-stu-id="772d5-124">For more information about controlling access to securable objects, see [Access Control](/windows/desktop/SecAuthZ/access-control), [Privileges](/windows/desktop/SecAuthZ/privileges), and [Securable Objects](/windows/desktop/SecAuthZ/securable-objects).</span></span> <span data-ttu-id="772d5-125">Per ulteriori informazioni sulla chiamata di funzioni che richiedono privilegi di amministratore, vedere [esecuzione con privilegi speciali](/windows/desktop/SecBP/running-with-special-privileges).</span><span class="sxs-lookup"><span data-stu-id="772d5-125">For more information about calling functions that require administrator privileges, see [Running with Special Privileges](/windows/desktop/SecBP/running-with-special-privileges).</span></span>

 

 