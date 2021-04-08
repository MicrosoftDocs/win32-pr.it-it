---
title: Gestione dei gruppi
description: Per ulteriori informazioni sui gruppi in Active Directory Domain Services, vedere informazioni sui gruppi.
ms.assetid: 92e3800c-1e63-46cb-8b1b-bad8557ee311
ms.tgt_platform: multiple
keywords:
- Active Directory, utilizzo di, gruppi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3f8714737083a0204f32685578afa7a7ffbf1d7
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "104046357"
---
# <a name="managing-groups"></a><span data-ttu-id="7faf1-104">Gestione dei gruppi</span><span class="sxs-lookup"><span data-stu-id="7faf1-104">Managing Groups</span></span>

<span data-ttu-id="7faf1-105">Questa sezione include argomenti su come usare i gruppi in Active Directory Domain Services:</span><span class="sxs-lookup"><span data-stu-id="7faf1-105">This section includes topics about how to use groups in Active Directory Domain Services:</span></span>

-   [<span data-ttu-id="7faf1-106">Oggetti Group</span><span class="sxs-lookup"><span data-stu-id="7faf1-106">Group Objects</span></span>](group-objects.md)
-   [<span data-ttu-id="7faf1-107">Modalità di utilizzo di gruppi di sicurezza nel controllo di accesso</span><span class="sxs-lookup"><span data-stu-id="7faf1-107">How Security Groups are Used in Access Control</span></span>](how-security-groups-are-used-in-access-control.md)
-   [<span data-ttu-id="7faf1-108">Creazione di gruppi in un dominio</span><span class="sxs-lookup"><span data-stu-id="7faf1-108">Creating Groups in a Domain</span></span>](creating-groups-in-a-domain.md)
-   [<span data-ttu-id="7faf1-109">Aggiunta di membri a gruppi in un dominio</span><span class="sxs-lookup"><span data-stu-id="7faf1-109">Adding Members to Groups in a Domain</span></span>](adding-members-to-groups-in-a-domain.md)
-   [<span data-ttu-id="7faf1-110">Rimozione di membri da gruppi in un dominio</span><span class="sxs-lookup"><span data-stu-id="7faf1-110">Removing Members from Groups in a Domain</span></span>](removing-members-from-groups-in-a-domain.md)
-   [<span data-ttu-id="7faf1-111">Annidamento di un gruppo in un altro gruppo</span><span class="sxs-lookup"><span data-stu-id="7faf1-111">Nesting a Group in Another Group</span></span>](nesting-a-group-in-another-group.md)
-   [<span data-ttu-id="7faf1-112">Determinazione dell'appartenenza di un utente o di un gruppo a un gruppo</span><span class="sxs-lookup"><span data-stu-id="7faf1-112">Determining a User's or Group's Membership in a Group</span></span>](determining-a-userampaposs-or-groupampaposs-membership-in-a-group.md)
-   [<span data-ttu-id="7faf1-113">Enumerazione dei gruppi</span><span class="sxs-lookup"><span data-stu-id="7faf1-113">Enumerating Groups</span></span>](enumerating-groups.md)
-   [<span data-ttu-id="7faf1-114">Esecuzione di query per i gruppi in un dominio</span><span class="sxs-lookup"><span data-stu-id="7faf1-114">Querying for Groups in a Domain</span></span>](querying-for-groups-in-a-domain.md)
-   [<span data-ttu-id="7faf1-115">Modifica dell'ambito o del tipo di un gruppo</span><span class="sxs-lookup"><span data-stu-id="7faf1-115">Changing a Group's Scope or Type</span></span>](changing-a-groupampaposs-scope-or-type.md)
-   <span data-ttu-id="7faf1-116">Eliminazione di gruppi.</span><span class="sxs-lookup"><span data-stu-id="7faf1-116">Deleting Groups.</span></span> <span data-ttu-id="7faf1-117">Un gruppo viene eliminato allo stesso modo di qualsiasi altro oggetto in Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="7faf1-117">A group is deleted in the same was as any other object in Active Directory Domain Services.</span></span> <span data-ttu-id="7faf1-118">Per ulteriori informazioni sull'eliminazione di oggetti Active Directory, vedere [creazione ed eliminazione di oggetti in Active Directory Domain Services](creating-and-deleting-objects-in-active-directory-domain-services.md).</span><span class="sxs-lookup"><span data-stu-id="7faf1-118">For more information about deleting Active Directory objects, see [Creating and Deleting Objects in Active Directory Domain Services](creating-and-deleting-objects-in-active-directory-domain-services.md).</span></span>
-   <span data-ttu-id="7faf1-119">Gruppi spostati.</span><span class="sxs-lookup"><span data-stu-id="7faf1-119">Moving Groups.</span></span> <span data-ttu-id="7faf1-120">Un gruppo viene spostato allo stesso modo di qualsiasi altro oggetto Active Directory.</span><span class="sxs-lookup"><span data-stu-id="7faf1-120">A group is moved in the same was as any other Active Directory object.</span></span> <span data-ttu-id="7faf1-121">Per ulteriori informazioni, vedere la pagina relativa al [trasferimento di oggetti](moving-objects.md).</span><span class="sxs-lookup"><span data-stu-id="7faf1-121">For more information, see [Moving Objects](moving-objects.md).</span></span>
-   [<span data-ttu-id="7faf1-122">Recupero del nome del Account-Style di dominio di un gruppo</span><span class="sxs-lookup"><span data-stu-id="7faf1-122">Getting the Domain Account-Style Name of a Group</span></span>](getting-the-domain-account-style-name-of-a-group.md)
-   [<span data-ttu-id="7faf1-123">Gruppi su server membri e Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="7faf1-123">Groups on Member Servers and Windows 2000 Professional</span></span>](groups-on-member-servers-and-windows-2000-professional.md)
-   [<span data-ttu-id="7faf1-124">Quali sviluppatori di applicazioni e servizi devono conoscere sui gruppi</span><span class="sxs-lookup"><span data-stu-id="7faf1-124">What Application and Service Developers Need to Know About Groups</span></span>](what-application-and-service-developers-need-to-know-about-groups.md)

<span data-ttu-id="7faf1-125">Per ulteriori informazioni sui gruppi in Active Directory Domain Services, vedere [informazioni sui gruppi](https://www.microsoft.com/technet/prodtechnol/windowsserver2003/Library/ServerHelp/54af961b-28fa-461e-a32d-cf32697148ff.mspx).</span><span class="sxs-lookup"><span data-stu-id="7faf1-125">For more information about groups in Active Directory Domain Services, see [Understanding groups](https://www.microsoft.com/technet/prodtechnol/windowsserver2003/Library/ServerHelp/54af961b-28fa-461e-a32d-cf32697148ff.mspx).</span></span>

 

 




