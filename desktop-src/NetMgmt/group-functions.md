---
title: Funzioni di gruppo
description: Un gruppo globale contiene gli account utente di un dominio raggruppati in un nome di account di gruppo.
ms.assetid: 2199258d-bde9-4fdb-b9c1-147616420fbe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7696755cd5f5cbe75de11d386cb238fa3bd5d35d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399547"
---
# <a name="group-functions"></a><span data-ttu-id="db166-103">Funzioni di gruppo</span><span class="sxs-lookup"><span data-stu-id="db166-103">Group Functions</span></span>

<span data-ttu-id="db166-104">Un *gruppo globale* contiene gli account utente di un dominio raggruppati in un nome di account di gruppo.</span><span class="sxs-lookup"><span data-stu-id="db166-104">A *global group* contains user accounts from one domain that are grouped together under one group account name.</span></span> <span data-ttu-id="db166-105">Un gruppo globale può contenere solo membri (utenti) del dominio in cui viene creato il gruppo globale; non può contenere gruppi locali.</span><span class="sxs-lookup"><span data-stu-id="db166-105">A global group can contain only members (users) from the domain where the global group is created; it cannot contain local groups.</span></span> <span data-ttu-id="db166-106">Un gruppo globale è disponibile all'interno del proprio dominio e all'interno di qualsiasi dominio trusting.</span><span class="sxs-lookup"><span data-stu-id="db166-106">A global group is available within its own domain and within any trusting domain.</span></span>

<span data-ttu-id="db166-107">Le funzioni del gruppo di gestione di rete controllano i gruppi globali.</span><span class="sxs-lookup"><span data-stu-id="db166-107">The network management group functions control global groups.</span></span> <span data-ttu-id="db166-108">Le funzioni di gruppo sono elencate di seguito.</span><span class="sxs-lookup"><span data-stu-id="db166-108">The group functions are listed following.</span></span>



| <span data-ttu-id="db166-109">Funzione</span><span class="sxs-lookup"><span data-stu-id="db166-109">Function</span></span>                                     | <span data-ttu-id="db166-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="db166-110">Description</span></span>                                                                       |
|----------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="db166-111">**NetGroupAdd**</span><span class="sxs-lookup"><span data-stu-id="db166-111">**NetGroupAdd**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadd)           | <span data-ttu-id="db166-112">Crea un gruppo globale.</span><span class="sxs-lookup"><span data-stu-id="db166-112">Creates a global group.</span></span>                                                           |
| [<span data-ttu-id="db166-113">**NetGroupAddUser**</span><span class="sxs-lookup"><span data-stu-id="db166-113">**NetGroupAddUser**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadduser)   | <span data-ttu-id="db166-114">Aggiunge un utente a un gruppo globale esistente.</span><span class="sxs-lookup"><span data-stu-id="db166-114">Adds one user to an existing global group.</span></span>                                        |
| [<span data-ttu-id="db166-115">**NetGroupDel**</span><span class="sxs-lookup"><span data-stu-id="db166-115">**NetGroupDel**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupdel)           | <span data-ttu-id="db166-116">Rimuove un gruppo globale indipendentemente dal fatto che il gruppo disponga di membri.</span><span class="sxs-lookup"><span data-stu-id="db166-116">Removes a global group whether or not the group has any members.</span></span>                  |
| [<span data-ttu-id="db166-117">**NetGroupDelUser**</span><span class="sxs-lookup"><span data-stu-id="db166-117">**NetGroupDelUser**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupdeluser)   | <span data-ttu-id="db166-118">Rimuove un nome utente da un gruppo globale.</span><span class="sxs-lookup"><span data-stu-id="db166-118">Removes one user name from a global group.</span></span>                                        |
| [<span data-ttu-id="db166-119">**NetGroupEnum**</span><span class="sxs-lookup"><span data-stu-id="db166-119">**NetGroupEnum**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupenum)         | <span data-ttu-id="db166-120">Elenca tutti i gruppi globali in un server.</span><span class="sxs-lookup"><span data-stu-id="db166-120">Lists all global groups on a server.</span></span>                                              |
| [<span data-ttu-id="db166-121">**NetGroupGetInfo**</span><span class="sxs-lookup"><span data-stu-id="db166-121">**NetGroupGetInfo**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetinfo)   | <span data-ttu-id="db166-122">Restituisce informazioni su un particolare gruppo globale.</span><span class="sxs-lookup"><span data-stu-id="db166-122">Returns information about a particular global group.</span></span>                              |
| [<span data-ttu-id="db166-123">**NetGroupGetUsers**</span><span class="sxs-lookup"><span data-stu-id="db166-123">**NetGroupGetUsers**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetusers) | <span data-ttu-id="db166-124">Elenca tutti i membri di un determinato gruppo globale.</span><span class="sxs-lookup"><span data-stu-id="db166-124">Lists all members of a particular global group.</span></span>                                   |
| [<span data-ttu-id="db166-125">**NetGroupSetInfo**</span><span class="sxs-lookup"><span data-stu-id="db166-125">**NetGroupSetInfo**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetinfo)   | <span data-ttu-id="db166-126">Imposta le informazioni generali su un gruppo globale.</span><span class="sxs-lookup"><span data-stu-id="db166-126">Sets general information about a global group.</span></span>                                    |
| [<span data-ttu-id="db166-127">**NetGroupSetUsers**</span><span class="sxs-lookup"><span data-stu-id="db166-127">**NetGroupSetUsers**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetusers) | <span data-ttu-id="db166-128">Assegna membri a un nuovo gruppo globale; sostituisce i membri di un gruppo esistente.</span><span class="sxs-lookup"><span data-stu-id="db166-128">Assigns members to a new global group; replaces the members of an existing group.</span></span> |



 

<span data-ttu-id="db166-129">Quando si chiama la funzione [**NetGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadd) per creare un gruppo globale, è necessario specificare un nome di gruppo.</span><span class="sxs-lookup"><span data-stu-id="db166-129">When you call the [**NetGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadd) function to create a global group, you must supply a group name.</span></span> <span data-ttu-id="db166-130">Inizialmente, un nuovo gruppo non dispone di membri.</span><span class="sxs-lookup"><span data-stu-id="db166-130">Initially, a new group has no members.</span></span>

<span data-ttu-id="db166-131">Gli account utente appartengono automaticamente agli specifici utenti del dominio del gruppo globale.</span><span class="sxs-lookup"><span data-stu-id="db166-131">User accounts automatically belong to the special global group Domain Users.</span></span> <span data-ttu-id="db166-132">L'appartenenza a questo gruppo è indirettamente controllata dalle funzioni [**NetUserAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd), [**NetUserDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserdel)e [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) .</span><span class="sxs-lookup"><span data-stu-id="db166-132">Membership in this group is indirectly controlled by the [**NetUserAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd), [**NetUserDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserdel), and [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) functions.</span></span>

<span data-ttu-id="db166-133">Le informazioni sull'account di gruppo globale sono disponibili ai livelli seguenti:</span><span class="sxs-lookup"><span data-stu-id="db166-133">Global group account information is available at the following levels:</span></span>

-   [<span data-ttu-id="db166-134">**Informazioni sul gruppo \_ \_ 0**</span><span class="sxs-lookup"><span data-stu-id="db166-134">**GROUP\_INFO\_0**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_0)
-   [<span data-ttu-id="db166-135">**Informazioni sul gruppo \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="db166-135">**GROUP\_INFO\_1**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_1)
-   [<span data-ttu-id="db166-136">**Informazioni sul gruppo \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="db166-136">**GROUP\_INFO\_2**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_2)
-   [<span data-ttu-id="db166-137">**Informazioni sul gruppo \_ \_ 3**</span><span class="sxs-lookup"><span data-stu-id="db166-137">**GROUP\_INFO\_3**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_3)
-   [<span data-ttu-id="db166-138">**Informazioni sul gruppo \_ \_ 1002**</span><span class="sxs-lookup"><span data-stu-id="db166-138">**GROUP\_INFO\_1002**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_1002)
-   [<span data-ttu-id="db166-139">**Informazioni sul gruppo \_ \_ 1005**</span><span class="sxs-lookup"><span data-stu-id="db166-139">**GROUP\_INFO\_1005**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_1005)

<span data-ttu-id="db166-140">I livelli 1002 e 1005 sono validi solo per la funzione [**NetGroupSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetinfo) .</span><span class="sxs-lookup"><span data-stu-id="db166-140">The 1002 and 1005 levels are valid only for the [**NetGroupSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetinfo) function.</span></span>

<span data-ttu-id="db166-141">Le informazioni sui membri del gruppo globale sono disponibili al livello di Informazioni seguente:</span><span class="sxs-lookup"><span data-stu-id="db166-141">Global group member information is available at the following information level:</span></span>

-   [<span data-ttu-id="db166-142">**Informazioni sugli utenti del gruppo \_ \_ \_ 0**</span><span class="sxs-lookup"><span data-stu-id="db166-142">**GROUP\_USERS\_INFO\_0**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-group_users_info_0)

<span data-ttu-id="db166-143">Per ulteriori informazioni, vedere la pagina relativa alle [funzioni del gruppo locale](local-group-functions.md)di gestione della rete.</span><span class="sxs-lookup"><span data-stu-id="db166-143">For more information, see the network management [Local Group Functions](local-group-functions.md).</span></span>

<span data-ttu-id="db166-144">Se si sta programmando per Active Directory, è possibile chiamare determinati metodi di Active Directory Service Interface (ADSI) per ottenere la stessa funzionalità che è possibile ottenere chiamando le funzioni del gruppo di gestione di rete.</span><span class="sxs-lookup"><span data-stu-id="db166-144">If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the network management group functions.</span></span> <span data-ttu-id="db166-145">Per ulteriori informazioni, vedere [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup).</span><span class="sxs-lookup"><span data-stu-id="db166-145">For more information, see [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup).</span></span>

 

 