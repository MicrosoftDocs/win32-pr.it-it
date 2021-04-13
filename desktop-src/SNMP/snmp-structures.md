---
title: Strutture SNMP
description: Nella tabella seguente sono elencate le strutture utilizzate con SNMP.
ms.assetid: b6dacc85-893d-4825-93df-729333b491b3
keywords:
- SNMP di strutture SNMP
- Strutture SNMP, SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f254dfebeb3d468add8871d4b6f28f268341e9ea
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399599"
---
# <a name="snmp-structures"></a><span data-ttu-id="262b6-105">Strutture SNMP</span><span class="sxs-lookup"><span data-stu-id="262b6-105">SNMP Structures</span></span>

<span data-ttu-id="262b6-106">\[SNMP è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="262b6-106">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="262b6-107">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="262b6-107">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="262b6-108">Usare invece [gestione remota Windows](/windows/desktop/WinRM/portal), ovvero l'implementazione Microsoft di WS-Man.\]</span><span class="sxs-lookup"><span data-stu-id="262b6-108">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="262b6-109">Nella tabella seguente sono elencate le strutture utilizzate con SNMP.</span><span class="sxs-lookup"><span data-stu-id="262b6-109">The following table lists structures that are used with SNMP.</span></span>



| <span data-ttu-id="262b6-110">Struttura SNMP</span><span class="sxs-lookup"><span data-stu-id="262b6-110">SNMP Structure</span></span>                                         | <span data-ttu-id="262b6-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="262b6-111">Description</span></span>                                                                                             |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="262b6-112">**AsnAny**</span><span class="sxs-lookup"><span data-stu-id="262b6-112">**AsnAny**</span></span>](/windows/desktop/api/Snmp/ns-snmp-asnany)                           | <span data-ttu-id="262b6-113">Descrive il tipo e il valore di una variabile SNMP specificata.</span><span class="sxs-lookup"><span data-stu-id="262b6-113">Describes the type and value of a specified SNMP variable.</span></span>                                              |
| <span data-ttu-id="262b6-114">[**AsnCounter64**](/previous-versions/windows/desktop/legacy/aa377953(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="262b6-114">[**AsnCounter64**](/previous-versions/windows/desktop/legacy/aa377953(v=vs.85))</span></span>               | <span data-ttu-id="262b6-115">Contiene un contatore a 64 bit specificato da due valori che descrivono i bit di ordine inferiore e di ordine superiore.</span><span class="sxs-lookup"><span data-stu-id="262b6-115">Contains a 64-bit counter that is specified by two values describing its low-order and high-order bits.</span></span> |
| [<span data-ttu-id="262b6-116">**AsnObjectIdentifier**</span><span class="sxs-lookup"><span data-stu-id="262b6-116">**AsnObjectIdentifier**</span></span>](/windows/desktop/api/Snmp/ns-snmp-asnobjectidentifier) | <span data-ttu-id="262b6-117">Descrive un identificatore di oggetto (OID).</span><span class="sxs-lookup"><span data-stu-id="262b6-117">Describes an object identifier (OID).</span></span>                                                                   |
| [<span data-ttu-id="262b6-118">**AsnOctetString**</span><span class="sxs-lookup"><span data-stu-id="262b6-118">**AsnOctetString**</span></span>](/windows/desktop/api/Snmp/ns-snmp-asnoctetstring)           | <span data-ttu-id="262b6-119">Rappresenta una stringa di ottetti, in genere in valori di byte.</span><span class="sxs-lookup"><span data-stu-id="262b6-119">Represents a string of octets, usually in byte values.</span></span>                                                  |
| [<span data-ttu-id="262b6-120">**SnmpVarBind**</span><span class="sxs-lookup"><span data-stu-id="262b6-120">**SnmpVarBind**</span></span>](/windows/desktop/api/Snmp/ns-snmp-snmpvarbind)                 | <span data-ttu-id="262b6-121">Descrive un'associazione di variabile SNMP.</span><span class="sxs-lookup"><span data-stu-id="262b6-121">Describes an SNMP variable binding.</span></span>                                                                     |
| [<span data-ttu-id="262b6-122">**SnmpVarBindList**</span><span class="sxs-lookup"><span data-stu-id="262b6-122">**SnmpVarBindList**</span></span>](/windows/desktop/api/Snmp/ns-snmp-snmpvarbindlist)         | <span data-ttu-id="262b6-123">Contiene un elenco di associazioni di variabili SNMP.</span><span class="sxs-lookup"><span data-stu-id="262b6-123">Contains a list of SNMP variable bindings.</span></span>                                                              |



 

 

 