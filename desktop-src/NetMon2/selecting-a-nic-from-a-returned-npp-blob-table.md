---
description: Per selezionare una scheda di interfaccia di rete da una tabella BLOB NPP restituita da Network Monitor, chiamare la funzione GetNPPBlobTable. Questa funzione restituisce una tabella BLOB NPP, che può quindi essere enumerata dall'applicazione per selezionare la scheda di interfaccia di rete a cui si è interessati.
ms.assetid: 51428cc9-0b48-4da6-bbf6-b22798e01263
title: Selezione di una scheda di interfaccia di rete da una tabella BLOB NPP restituita
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08215bb647482ba8544d7eaa033dea7efd9a5ad1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881829"
---
# <a name="selecting-a-nic-from-a-returned-npp-blob-table"></a><span data-ttu-id="d91e9-104">Selezione di una scheda di interfaccia di rete da una tabella BLOB NPP restituita</span><span class="sxs-lookup"><span data-stu-id="d91e9-104">Selecting a NIC from a Returned NPP BLOB table</span></span>

<span data-ttu-id="d91e9-105">Per selezionare una scheda di interfaccia di rete da una tabella BLOB NPP restituita da Network Monitor, chiamare la funzione [**GetNPPBlobTable**](getnppblobtable.md) .</span><span class="sxs-lookup"><span data-stu-id="d91e9-105">To select a NIC from an NPP BLOB table returned by Network Monitor, call the [**GetNPPBlobTable**](getnppblobtable.md) function.</span></span> <span data-ttu-id="d91e9-106">Questa funzione restituisce una tabella BLOB NPP, che può quindi essere enumerata dall'applicazione per selezionare la scheda di interfaccia di rete a cui si è interessati.</span><span class="sxs-lookup"><span data-stu-id="d91e9-106">This function returns an NPP BLOB table, which can then be enumerated by your application to select the NIC you are interested in.</span></span>

<span data-ttu-id="d91e9-107">Quando si chiama questa funzione, è possibile restituire una tabella BLOB di tutte le schede di rete registrate nel computer locale o un set più piccolo di schede di rete filtrate.</span><span class="sxs-lookup"><span data-stu-id="d91e9-107">When you call this function you can return either a BLOB table of all the NICs registered on the local computer or a smaller set of filtered NICs.</span></span> <span data-ttu-id="d91e9-108">Per filtrare le schede di rete restituite, è possibile specificare un [*BLOB di filtro*](f.md) quando viene effettuata la chiamata.</span><span class="sxs-lookup"><span data-stu-id="d91e9-108">To filter the NICs that are returned, you can provide a [*filter BLOB*](f.md) when the call is made.</span></span>



| <span data-ttu-id="d91e9-109">Per informazioni su</span><span class="sxs-lookup"><span data-stu-id="d91e9-109">For information about</span></span>                                                       | <span data-ttu-id="d91e9-110">Vedere</span><span class="sxs-lookup"><span data-stu-id="d91e9-110">See</span></span>                                                                                                  |
|-----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d91e9-111">Come specificare un filtro che limita le NIC restituite in una tabella BLOB di NPP.</span><span class="sxs-lookup"><span data-stu-id="d91e9-111">How to specify a filter that limits the NICs returned in an NPP BLOB table.</span></span> | [<span data-ttu-id="d91e9-112">Specifica di un BLOB di filtro</span><span class="sxs-lookup"><span data-stu-id="d91e9-112">Specifying a Filter BLOB</span></span>](specifying-a-filter-blob.md)                                             |
| <span data-ttu-id="d91e9-113">Come selezionare una scheda di interfaccia di rete registrata in un computer locale.</span><span class="sxs-lookup"><span data-stu-id="d91e9-113">How to select a NIC registered on a local computer.</span></span>                         | [<span data-ttu-id="d91e9-114">Selezione di una scheda di interfaccia di rete registrata</span><span class="sxs-lookup"><span data-stu-id="d91e9-114">Selecting a Registered NIC</span></span>](selecting-a-registered-nic.md)                                         |
| <span data-ttu-id="d91e9-115">Come selezionare una scheda di interfaccia di rete da una tabella BLOB NPP specificata</span><span class="sxs-lookup"><span data-stu-id="d91e9-115">How to select a NIC from a supplied NPP BLOB table</span></span>                          | [<span data-ttu-id="d91e9-116">Selezione di una scheda di interfaccia di rete da una tabella BLOB NPP specificata</span><span class="sxs-lookup"><span data-stu-id="d91e9-116">Selecting a NIC from a Supplied NPP BLOB Table</span></span>](selecting-a-nic-from-a-supplied-npp-blob-table.md) |



 

 

 



