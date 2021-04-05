---
title: Duplicazione di una PDU
description: La funzione SnmpDuplicatePdu Duplica una PDU, allocando la memoria necessaria. Per rilasciare le risorse allocate da SnmpDuplicatePdu per una nuova PDU, un'applicazione WinSNMP deve chiamare la funzione SnmpFreePdu.
ms.assetid: 371e566b-0577-4089-b081-17085c9587fd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acd860d84ac102f2c2cdd1132476b3279e640f9f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711737"
---
# <a name="duplicating-a-pdu"></a><span data-ttu-id="be018-104">Duplicazione di una PDU</span><span class="sxs-lookup"><span data-stu-id="be018-104">Duplicating a PDU</span></span>

<span data-ttu-id="be018-105">La funzione [**SnmpDuplicatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatepdu) Duplica una PDU, allocando la memoria necessaria.</span><span class="sxs-lookup"><span data-stu-id="be018-105">The [**SnmpDuplicatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatepdu) function duplicates a PDU, allocating any necessary memory.</span></span> <span data-ttu-id="be018-106">Per rilasciare le risorse allocate da **SnmpDuplicatePdu** per una nuova PDU, un'applicazione WinSNMP deve chiamare la funzione [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu) .</span><span class="sxs-lookup"><span data-stu-id="be018-106">To release resources allocated by **SnmpDuplicatePdu** for a new PDU, a WinSNMP application must call the [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu) function.</span></span>

 

 




