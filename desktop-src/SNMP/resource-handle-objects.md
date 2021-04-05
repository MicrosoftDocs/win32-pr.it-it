---
title: Oggetti handle di risorsa
description: La struttura di un oggetto risorsa è limitata all'implementazione di Microsoft WinSNMP. Un'applicazione WinSNMP può accedere a un oggetto risorsa con un handle.
ms.assetid: c70a03b1-afac-4f1a-81e7-7f31430f5655
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef1afe5e6488190f95961bff7ce37f7b719d076d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713060"
---
# <a name="resource-handle-objects"></a><span data-ttu-id="463ac-104">Oggetti handle di risorsa</span><span class="sxs-lookup"><span data-stu-id="463ac-104">Resource Handle Objects</span></span>

<span data-ttu-id="463ac-105">La struttura di un oggetto risorsa è limitata all'implementazione di Microsoft WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="463ac-105">The structure of a resource object is restricted to the Microsoft WinSNMP implementation.</span></span> <span data-ttu-id="463ac-106">Un'applicazione WinSNMP può accedere a un oggetto risorsa con un handle.</span><span class="sxs-lookup"><span data-stu-id="463ac-106">A WinSNMP application can access a resource object with a handle.</span></span>

<span data-ttu-id="463ac-107">L'implementazione può allocare uno dei seguenti tipi di handle di risorse per un'applicazione WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="463ac-107">The implementation can allocate one of the following types of resource handles for a WinSNMP application.</span></span>

| <span data-ttu-id="463ac-108">Tipo di handle</span><span class="sxs-lookup"><span data-stu-id="463ac-108">Handle type</span></span>        | <span data-ttu-id="463ac-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="463ac-109">Description</span></span>                       |
|--------------------|-----------------------------------|
| <span data-ttu-id="463ac-110">**\_sessione HSNMP**</span><span class="sxs-lookup"><span data-stu-id="463ac-110">**HSNMP\_SESSION**</span></span> | <span data-ttu-id="463ac-111">Handle per una sessione WinSNMP</span><span class="sxs-lookup"><span data-stu-id="463ac-111">Handle to a WinSNMP session</span></span>       |
| <span data-ttu-id="463ac-112">**\_entità HSNMP**</span><span class="sxs-lookup"><span data-stu-id="463ac-112">**HSNMP\_ENTITY**</span></span>  | <span data-ttu-id="463ac-113">Handle per un'entità SNMP</span><span class="sxs-lookup"><span data-stu-id="463ac-113">Handle to an SNMP entity</span></span>          |
| <span data-ttu-id="463ac-114">**\_contesto HSNMP**</span><span class="sxs-lookup"><span data-stu-id="463ac-114">**HSNMP\_CONTEXT**</span></span> | <span data-ttu-id="463ac-115">Handle per un contesto WinSNMP</span><span class="sxs-lookup"><span data-stu-id="463ac-115">Handle to a WinSNMP context</span></span>       |
| <span data-ttu-id="463ac-116">**\_PDU HSNMP**</span><span class="sxs-lookup"><span data-stu-id="463ac-116">**HSNMP\_PDU**</span></span>     | <span data-ttu-id="463ac-117">Handle per un'unità dati del protocollo</span><span class="sxs-lookup"><span data-stu-id="463ac-117">Handle to a protocol data unit</span></span>    |
| <span data-ttu-id="463ac-118">**\_VBL HSNMP**</span><span class="sxs-lookup"><span data-stu-id="463ac-118">**HSNMP\_VBL**</span></span>     | <span data-ttu-id="463ac-119">Handle per un elenco di associazioni variabili</span><span class="sxs-lookup"><span data-stu-id="463ac-119">Handle to a variable binding list</span></span> |



 

<span data-ttu-id="463ac-120">Un'applicazione WinSNMP può richiedere che l'implementazione crei o elimini gli handle di risorsa, ma l'implementazione esegue l'operazione.</span><span class="sxs-lookup"><span data-stu-id="463ac-120">A WinSNMP application can request that the implementation create or delete resource handles, but the implementation performs the operation.</span></span> <span data-ttu-id="463ac-121">Per ulteriori informazioni su come liberare le singole risorse, vedere le funzioni [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor), [**SnmpFreeVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl), [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu), [**SnmpFreeEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity)e [**SnmpFreeContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext) .</span><span class="sxs-lookup"><span data-stu-id="463ac-121">For additional information about freeing individual resources, see the [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor), [**SnmpFreeVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl), [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu), [**SnmpFreeEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity), and [**SnmpFreeContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext) functions.</span></span>

 

 




