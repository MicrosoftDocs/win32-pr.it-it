---
title: Gestione di Zone DNS
description: Una zona DNS è un database di voci RR che corrisponde a parte dello spazio dei nomi gerarchico DNS. Le zone DNS vengono usate per delineare i server DNS autorevoli per la risoluzione delle query di risoluzione dei nomi per una determinata sezione della gerarchia DNS.
ms.assetid: d4aa94e0-36f7-4b97-8a0a-c677c8a826a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58c4cc991821f88076d3c3e9b2bfcbddc3ab662d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712424"
---
# <a name="managing-dns-zones"></a><span data-ttu-id="6549a-104">Gestione di Zone DNS</span><span class="sxs-lookup"><span data-stu-id="6549a-104">Managing DNS Zones</span></span>

<span data-ttu-id="6549a-105">Una zona DNS è un database di voci RR che corrisponde a parte dello spazio dei nomi gerarchico DNS.</span><span class="sxs-lookup"><span data-stu-id="6549a-105">A DNS zone is a database of RR entries that corresponds to part of the DNS hierarchical name space.</span></span> <span data-ttu-id="6549a-106">Le zone DNS vengono usate per delineare i server DNS autorevoli per la risoluzione delle query di risoluzione dei nomi per una determinata sezione della gerarchia DNS.</span><span class="sxs-lookup"><span data-stu-id="6549a-106">DNS zones are used to delineate which DNS Servers are authoritative for resolving name-resolution queries for a given section of the DNS hierarchy.</span></span>

## <a name="administration-steps"></a><span data-ttu-id="6549a-107">Procedura di amministrazione</span><span class="sxs-lookup"><span data-stu-id="6549a-107">Administration Steps</span></span>

<span data-ttu-id="6549a-108">Il provider WMI DNS consente l'amministrazione delle zone DNS dal server DNS autorevole stesso o da host remoti.</span><span class="sxs-lookup"><span data-stu-id="6549a-108">The DNS WMI Provider enables the administration of DNS zones from the authoritative DNS Server itself, or from remote hosts.</span></span> <span data-ttu-id="6549a-109">I passaggi generali necessari per amministrare una zona usando il provider WMI DNS sono:</span><span class="sxs-lookup"><span data-stu-id="6549a-109">The general steps necessary to administer a zone using the DNS WMI Provider are:</span></span>

-   <span data-ttu-id="6549a-110">Connessione al provider WMI DNS</span><span class="sxs-lookup"><span data-stu-id="6549a-110">Connecting to the DNS WMI Provider</span></span>
-   <span data-ttu-id="6549a-111">Recupero di un'istanza di zona</span><span class="sxs-lookup"><span data-stu-id="6549a-111">Getting a zone instance</span></span>
-   <span data-ttu-id="6549a-112">Elenco o modifica di una proprietà di zona o utilizzo di un metodo</span><span class="sxs-lookup"><span data-stu-id="6549a-112">Listing or modifying a zone property, or using a method</span></span>

<span data-ttu-id="6549a-113">Le attività seguenti sono collegate agli esempi di script associati:</span><span class="sxs-lookup"><span data-stu-id="6549a-113">The following tasks are linked to their associated scripting samples:</span></span>

-   [<span data-ttu-id="6549a-114">Creazione di una zona DNS</span><span class="sxs-lookup"><span data-stu-id="6549a-114">Creating a DNS Zone</span></span>](dns-wmi-provider-samples-managing-dns-zones.md)
-   [<span data-ttu-id="6549a-115">Modifica di una zona DNS</span><span class="sxs-lookup"><span data-stu-id="6549a-115">Modifying a DNS Zone</span></span>](dns-wmi-provider-samples-managing-dns-zones.md)
-   [<span data-ttu-id="6549a-116">Eliminazione di una zona DNS</span><span class="sxs-lookup"><span data-stu-id="6549a-116">Deleting a DNS Zone</span></span>](dns-wmi-provider-samples-managing-dns-zones.md)
-   [<span data-ttu-id="6549a-117">Aggiunta di un indirizzo IP di zona</span><span class="sxs-lookup"><span data-stu-id="6549a-117">Adding a Zone IP Address</span></span>](dns-wmi-provider-samples-managing-dns-zones.md)
-   [<span data-ttu-id="6549a-118">Eliminazione di un indirizzo IP di zona</span><span class="sxs-lookup"><span data-stu-id="6549a-118">Deleting a Zone IP Address</span></span>](dns-wmi-provider-samples-managing-dns-zones.md)
-   [<span data-ttu-id="6549a-119">Sospensione di una zona</span><span class="sxs-lookup"><span data-stu-id="6549a-119">Pausing a Zone</span></span>](dns-wmi-provider-samples-managing-dns-zones.md)
-   [<span data-ttu-id="6549a-120">Ripresa di una zona</span><span class="sxs-lookup"><span data-stu-id="6549a-120">Resuming a Zone</span></span>](dns-wmi-provider-samples-managing-dns-zones.md)
-   [<span data-ttu-id="6549a-121">Aggiornamento di una zona</span><span class="sxs-lookup"><span data-stu-id="6549a-121">Updating a Zone</span></span>](dns-wmi-provider-samples-managing-dns-zones.md)
-   [<span data-ttu-id="6549a-122">Ricaricamento di una zona</span><span class="sxs-lookup"><span data-stu-id="6549a-122">Reloading a Zone</span></span>](dns-wmi-provider-samples-managing-dns-zones.md)
-   [<span data-ttu-id="6549a-123">Aggiornamento di una zona</span><span class="sxs-lookup"><span data-stu-id="6549a-123">Refreshing a Zone</span></span>](dns-wmi-provider-samples-managing-dns-zones.md)

 

 




