---
description: Network Monitor offre tre funzioni per la selezione di una scheda di interfaccia di rete (NIC). Queste funzioni forniscono tre modi per enumerare un set di schede di rete e selezionare quello che si vuole usare. Nella tabella seguente sono elencate queste funzioni.
ms.assetid: fbf319bb-4e24-46e3-81bc-d407b26220fb
title: Selezione di una scheda di interfaccia di rete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8315a97cc8457d86614fc25c87c39b1b9794c7fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131191"
---
# <a name="selecting-a-network-interface-card"></a><span data-ttu-id="a74ae-105">Selezione di una scheda di interfaccia di rete</span><span class="sxs-lookup"><span data-stu-id="a74ae-105">Selecting a Network Interface Card</span></span>

<span data-ttu-id="a74ae-106">Network Monitor offre tre funzioni per la selezione di una scheda di interfaccia di rete (NIC).</span><span class="sxs-lookup"><span data-stu-id="a74ae-106">Network Monitor provides three functions for selecting a network interface card (NIC).</span></span> <span data-ttu-id="a74ae-107">Queste funzioni forniscono tre modi per enumerare un set di schede di rete e selezionare quello che si vuole usare.</span><span class="sxs-lookup"><span data-stu-id="a74ae-107">These functions provide three ways to enumerate a set of NICs and select the one you want to use.</span></span> <span data-ttu-id="a74ae-108">Nella tabella seguente sono elencate queste funzioni.</span><span class="sxs-lookup"><span data-stu-id="a74ae-108">The following table lists these functions.</span></span>



| <span data-ttu-id="a74ae-109">Funzione</span><span class="sxs-lookup"><span data-stu-id="a74ae-109">Function</span></span>                                                 | <span data-ttu-id="a74ae-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a74ae-110">Description</span></span>                                                                                                                                  |
|----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a74ae-111">**GetNPPBlobFromUI**</span><span class="sxs-lookup"><span data-stu-id="a74ae-111">**GetNPPBlobFromUI**</span></span>](getnppblobfromui.md)             | <span data-ttu-id="a74ae-112">Usa l'interfaccia utente di Network Monitor per visualizzare le schede NIC registrate e restituisce il BLOB di NPP che rappresenta la scheda di interfaccia di rete a cui si è interessati.</span><span class="sxs-lookup"><span data-stu-id="a74ae-112">Uses the Network Monitor UI to display the registered NICs and returns the NPP BLOB that represents the NIC you are interested in.</span></span>           |
| [<span data-ttu-id="a74ae-113">**GetNPPBlobTable**</span><span class="sxs-lookup"><span data-stu-id="a74ae-113">**GetNPPBlobTable**</span></span>](getnppblobtable.md)               | <span data-ttu-id="a74ae-114">Restituisce una tabella BLOB.</span><span class="sxs-lookup"><span data-stu-id="a74ae-114">Returns a BLOB table.</span></span> <span data-ttu-id="a74ae-115">L'applicazione deve enumerare la tabella e selezionare un BLOB di NPP.</span><span class="sxs-lookup"><span data-stu-id="a74ae-115">The application must enumerate the table and select an NPP BLOB.</span></span>                                                       |
| [<span data-ttu-id="a74ae-116">**SelectNPPBlobFromTable**</span><span class="sxs-lookup"><span data-stu-id="a74ae-116">**SelectNPPBlobFromTable**</span></span>](selectnppblobfromtable.md) | <span data-ttu-id="a74ae-117">Usa l'interfaccia Network Monitor per visualizzare i BLOB NPP specificati e restituisce il BLOB di NPP che rappresenta la scheda di interfaccia di rete a cui si è interessati.</span><span class="sxs-lookup"><span data-stu-id="a74ae-117">Uses the Network Monitor interface to display the supplied NPP BLOBs and returns the NPP BLOB that represents the NIC you are interested in.</span></span> |



 

<span data-ttu-id="a74ae-118">Ogni scheda di interfaccia di rete è rappresentata da un BLOB (Binary Large Object) di NPP.</span><span class="sxs-lookup"><span data-stu-id="a74ae-118">Each NIC is represented by an NPP binary large object (BLOB).</span></span> <span data-ttu-id="a74ae-119">Queste funzioni possono restituire un singolo BLOB NPP da quelli registrati nel computer, un singolo BLOB NPP da una tabella BLOB NPP specificata o una tabella di BLOB NPP che il chiamante deve usare per selezionare un BLOB specifico.</span><span class="sxs-lookup"><span data-stu-id="a74ae-119">These functions can return a single NPP BLOB from those registered on the computer, a single NPP BLOB from a supplied NPP BLOB table, or a table of NPP BLOBs that the caller must then use to select a specific BLOB.</span></span> <span data-ttu-id="a74ae-120">Nei primi due casi, quando si selezionano le schede NIC registrate o da una tabella BLOB NPP specificata, l'interfaccia utente di Network Monitor Visualizza le schede di interfaccia di rete che è possibile selezionare.</span><span class="sxs-lookup"><span data-stu-id="a74ae-120">In the first two cases, when selecting from the registered NICs or from a supplied NPP BLOB table, the Network Monitor UI displays the NICs you can select.</span></span>

> [!Note]  
> <span data-ttu-id="a74ae-121">Network Monitor usa una funzionalità denominata ricercatore NPP per enumerare le schede di rete registrate nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="a74ae-121">Network Monitor uses a feature called the NPP Finder to enumerate the NICs registered on the local computer.</span></span> <span data-ttu-id="a74ae-122">Il Finder di NPP è un componente di Npptools.dll.</span><span class="sxs-lookup"><span data-stu-id="a74ae-122">The NPP Finder is a component of Npptools.dll.</span></span>

 



| <span data-ttu-id="a74ae-123">Per informazioni su</span><span class="sxs-lookup"><span data-stu-id="a74ae-123">For information about</span></span>                            | <span data-ttu-id="a74ae-124">Vedere</span><span class="sxs-lookup"><span data-stu-id="a74ae-124">See</span></span>                                                                                                  |
|--------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a74ae-125">Selezione di una scheda di interfaccia di rete registrata nel computer locale</span><span class="sxs-lookup"><span data-stu-id="a74ae-125">Selecting a NIC registered on the local computer</span></span> | [<span data-ttu-id="a74ae-126">Selezione di una scheda di interfaccia di rete registrata</span><span class="sxs-lookup"><span data-stu-id="a74ae-126">Selecting a Registered NIC</span></span>](selecting-a-registered-nic.md)                                         |
| <span data-ttu-id="a74ae-127">Selezione di una scheda di interfaccia di rete da una tabella BLOB NPP specificata</span><span class="sxs-lookup"><span data-stu-id="a74ae-127">Selecting a NIC from a supplied NPP BLOB table</span></span>   | [<span data-ttu-id="a74ae-128">Selezione di una scheda di interfaccia di rete da una tabella BLOB NPP specificata</span><span class="sxs-lookup"><span data-stu-id="a74ae-128">Selecting a NIC from a Supplied NPP BLOB Table</span></span>](selecting-a-nic-from-a-supplied-npp-blob-table.md) |
| <span data-ttu-id="a74ae-129">Recupero di una tabella BLOB di NPP</span><span class="sxs-lookup"><span data-stu-id="a74ae-129">Retrieving an NPP BLOB table</span></span>                     | [<span data-ttu-id="a74ae-130">Selezione di una scheda di interfaccia di rete da una tabella BLOB NPP restituita</span><span class="sxs-lookup"><span data-stu-id="a74ae-130">Selecting a NIC from a Returned NPP BLOB table</span></span>](selecting-a-nic-from-a-returned-npp-blob-table.md) |



 

 

 



