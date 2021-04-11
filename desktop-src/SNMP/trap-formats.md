---
title: Formati trap
description: Il formato di Trap PDU è diverso da quello di altre PDU. Anche il formato di trap SNMPv1 e trap SNMPv2C è diverso.
ms.assetid: 2d2b4520-28b7-4a2e-8dee-456e17d9d6f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e87adc3222808fcc7e81904ade07c09afa13bc6d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044369"
---
# <a name="trap-formats"></a><span data-ttu-id="da9ac-104">Formati trap</span><span class="sxs-lookup"><span data-stu-id="da9ac-104">Trap Formats</span></span>

<span data-ttu-id="da9ac-105">Il formato di Trap PDU è diverso da quello di altre PDU.</span><span class="sxs-lookup"><span data-stu-id="da9ac-105">The format of trap PDUs is different than that of other PDUs.</span></span> <span data-ttu-id="da9ac-106">Anche il formato di trap SNMPv1 e trap SNMPv2C è diverso.</span><span class="sxs-lookup"><span data-stu-id="da9ac-106">The format of SNMPv1 traps and SNMPv2C traps is also different.</span></span>

<span data-ttu-id="da9ac-107">In SNMPv2C Framework il formato di Trap PDU è un elenco di associazioni variabili di *n* voci di binding variabili organizzate nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="da9ac-107">Under the SNMPv2C framework, the PDU trap format is a variable binding list of *n* variable binding entries organized in the following manner:</span></span>

-   <span data-ttu-id="da9ac-108">La prima voce di associazione variabile contiene un timestamp.</span><span class="sxs-lookup"><span data-stu-id="da9ac-108">The first variable binding entry contains a time-stamp.</span></span>
-   <span data-ttu-id="da9ac-109">La seconda voce di associazione variabile è un identificatore di oggetto che identifica la trap.</span><span class="sxs-lookup"><span data-stu-id="da9ac-109">The second variable binding entry is an object identifier that identifies the trap.</span></span>
-   <span data-ttu-id="da9ac-110">Le terze e *n* voci di associazione variabili, se presenti, contengono informazioni aggiuntive associate al trap.</span><span class="sxs-lookup"><span data-stu-id="da9ac-110">The third through *n* variable binding entries, if present, contain additional information associated with the trap.</span></span>

<span data-ttu-id="da9ac-111">In SNMPv1 Framework il formato di Trap PDU è il seguente.</span><span class="sxs-lookup"><span data-stu-id="da9ac-111">Under the SNMPv1 framework, the PDU trap format is as follows.</span></span>

| <span data-ttu-id="da9ac-112">Campo</span><span class="sxs-lookup"><span data-stu-id="da9ac-112">Field</span></span>                      | <span data-ttu-id="da9ac-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="da9ac-113">Description</span></span>                                                      |
|----------------------------|------------------------------------------------------------------|
| <span data-ttu-id="da9ac-114">Connettori</span><span class="sxs-lookup"><span data-stu-id="da9ac-114">enterprise</span></span>                 | <span data-ttu-id="da9ac-115">Identifica il tipo di dispositivo che ha generato la trap.</span><span class="sxs-lookup"><span data-stu-id="da9ac-115">Identifies the type of device that generated the trap.</span></span>           |
| <span data-ttu-id="da9ac-116">Agent-addr</span><span class="sxs-lookup"><span data-stu-id="da9ac-116">agent-addr</span></span>                 | <span data-ttu-id="da9ac-117">Identifica l'indirizzo IP del dispositivo che ha generato la trap.</span><span class="sxs-lookup"><span data-stu-id="da9ac-117">Identifies the IP address of the device that generated the trap.</span></span> |
| <span data-ttu-id="da9ac-118">Trap/Trap generico</span><span class="sxs-lookup"><span data-stu-id="da9ac-118">generic-trap/specific-trap</span></span> | <span data-ttu-id="da9ac-119">Identifica un tipo trap predefinito.</span><span class="sxs-lookup"><span data-stu-id="da9ac-119">Identifies a predefined trap type.</span></span>                               |
| <span data-ttu-id="da9ac-120">timestamp</span><span class="sxs-lookup"><span data-stu-id="da9ac-120">time-stamp</span></span>                 | <span data-ttu-id="da9ac-121">Identifica il momento in cui è stata generata la trap.</span><span class="sxs-lookup"><span data-stu-id="da9ac-121">Identifies when the trap was generated.</span></span>                          |
| <span data-ttu-id="da9ac-122">associazioni di variabili</span><span class="sxs-lookup"><span data-stu-id="da9ac-122">variable-bindings</span></span>          | <span data-ttu-id="da9ac-123">Contiene informazioni aggiuntive associate al trap.</span><span class="sxs-lookup"><span data-stu-id="da9ac-123">Contains additional information associated with the trap.</span></span>        |



 

<span data-ttu-id="da9ac-124">La funzione [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) restituisce sempre un messaggio nel formato SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="da9ac-124">The [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) function always returns a message in the SNMPv2C format.</span></span> <span data-ttu-id="da9ac-125">Se il messaggio contiene il tipo di **operazione \_ \_ trap SNMP PDU**, l'applicazione può leggere le voci di associazione variabili del messaggio e recuperare le informazioni associate alla trap.</span><span class="sxs-lookup"><span data-stu-id="da9ac-125">If the message contains the operation type **SNMP\_PDU\_TRAP**, the application can read the variable binding entries of the message and retrieve the information associated with the trap.</span></span>

 

 




