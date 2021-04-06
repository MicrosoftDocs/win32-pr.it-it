---
title: Partizioni di directory applicative
description: In Windows Server 2003 Active Directory Domain Services supportano le partizioni di directory applicative.
ms.assetid: 55c47803-c1ee-4888-bb19-103374ec9719
ms.tgt_platform: multiple
keywords:
- Active Directory partizioni di Active Directory
- Active Directory per le partizioni di directory applicative usando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63a8e035231aa24569b6fad6d5a7e0e62eaa5a30
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104046559"
---
# <a name="application-directory-partitions"></a><span data-ttu-id="6f3c6-105">Partizioni di directory applicative</span><span class="sxs-lookup"><span data-stu-id="6f3c6-105">Application Directory Partitions</span></span>

<span data-ttu-id="6f3c6-106">In Windows Server 2003 Active Directory Domain Services supportano le partizioni di directory applicative.</span><span class="sxs-lookup"><span data-stu-id="6f3c6-106">In Windows Server 2003, Active Directory Domain Services support application directory partitions.</span></span> <span data-ttu-id="6f3c6-107">Una partizione di directory applicativa può contenere una gerarchia di qualsiasi tipo di oggetti, ad eccezione delle entità di sicurezza, e può essere configurata per la replica in qualsiasi set di controller di dominio nella foresta.</span><span class="sxs-lookup"><span data-stu-id="6f3c6-107">An application directory partition can contain a hierarchy of any type of objects, except security principals, and can be configured to replicate to any set of domain controllers in the forest.</span></span> <span data-ttu-id="6f3c6-108">A differenza di una partizione di dominio, non è necessario eseguire la replica di una partizione di directory applicativa a tutti i controller di dominio in un dominio e la partizione può essere replicata nei controller di dominio in domini diversi della foresta.</span><span class="sxs-lookup"><span data-stu-id="6f3c6-108">Unlike a domain partition, an application directory partition is not required to replicate to all domain controllers in a domain and the partition can replicate to domain controllers in different domains of the forest.</span></span> <span data-ttu-id="6f3c6-109">Per ulteriori informazioni sulle partizioni di directory applicative, vedere [informazioni sulle partizioni di directory applicative](about-application-directory-partitions.md).</span><span class="sxs-lookup"><span data-stu-id="6f3c6-109">For more information about application directory partitions, see [About Application Directory Partitions](about-application-directory-partitions.md).</span></span>

<span data-ttu-id="6f3c6-110">È possibile creare una partizione di directory applicativa.</span><span class="sxs-lookup"><span data-stu-id="6f3c6-110">An application directory partition can be created.</span></span> <span data-ttu-id="6f3c6-111">modificato ed eliminato mediante le operazioni standard ADSI, LDAP e [System. DirectoryServices](/dotnet/api/system.directoryservices) .</span><span class="sxs-lookup"><span data-stu-id="6f3c6-111">modified and deleted using standard ADSI, LDAP and [System.DirectoryServices](/dotnet/api/system.directoryservices) operations.</span></span> <span data-ttu-id="6f3c6-112">Il contesto di sicurezza necessario per creare e modificare una partizione di directory applicativa è identico a quello per la creazione di una partizione di dominio.</span><span class="sxs-lookup"><span data-stu-id="6f3c6-112">The security context required to create and modify an application directory partition is the same as that for creating a domain partition.</span></span>

<span data-ttu-id="6f3c6-113">Negli argomenti seguenti viene descritto come utilizzare le partizioni di directory applicative:</span><span class="sxs-lookup"><span data-stu-id="6f3c6-113">The following topics describe how to work with application directory partitions:</span></span>

-   [<span data-ttu-id="6f3c6-114">Replica della partizione di directory applicativa</span><span class="sxs-lookup"><span data-stu-id="6f3c6-114">Application Directory Partition Replication</span></span>](application-directory-partition-replication.md)
-   [<span data-ttu-id="6f3c6-115">Sicurezza della partizione di directory applicativa</span><span class="sxs-lookup"><span data-stu-id="6f3c6-115">Application Directory Partition Security</span></span>](application-directory-partition-security.md)
-   [<span data-ttu-id="6f3c6-116">Creazione di una partizione di directory applicativa</span><span class="sxs-lookup"><span data-stu-id="6f3c6-116">Creating an Application Directory Partition</span></span>](creating-an-application-directory-partition.md)
-   [<span data-ttu-id="6f3c6-117">Eliminazione di una partizione di directory applicativa</span><span class="sxs-lookup"><span data-stu-id="6f3c6-117">Deleting an Application Directory Partition</span></span>](deleting-an-application-directory-partition.md)
-   [<span data-ttu-id="6f3c6-118">Enumerazione delle partizioni di directory applicative in una foresta</span><span class="sxs-lookup"><span data-stu-id="6f3c6-118">Enumerating Application Directory Partitions in a Forest</span></span>](enumerating-application-directory-partitions-in-a-forest.md)
-   [<span data-ttu-id="6f3c6-119">Individuazione di un server host partizione di directory applicativa</span><span class="sxs-lookup"><span data-stu-id="6f3c6-119">Locating an Application Directory Partition Host Server</span></span>](locating-an-application-directory-partition-host-server.md)
-   [<span data-ttu-id="6f3c6-120">Aggiunta o eliminazione di una replica della partizione di directory applicativa</span><span class="sxs-lookup"><span data-stu-id="6f3c6-120">Adding or Deleting an Application Directory Partition Replica</span></span>](adding-or-deleting-an-application-directory-partition-replica.md)
-   [<span data-ttu-id="6f3c6-121">Enumerazione delle repliche di una partizione di directory applicativa</span><span class="sxs-lookup"><span data-stu-id="6f3c6-121">Enumerating Replicas of an Application Directory Partition</span></span>](enumerating-replicas-of-an-application-directory-partition.md)
-   [<span data-ttu-id="6f3c6-122">Modifica della configurazione della partizione di directory applicativa</span><span class="sxs-lookup"><span data-stu-id="6f3c6-122">Modifying Application Directory Partition Configuration</span></span>](modifying-application-directory-partition-configuration.md)

 

 