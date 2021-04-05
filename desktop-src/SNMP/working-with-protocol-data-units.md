---
title: Utilizzo delle unità dati del protocollo
description: Il Simple Network Management Protocol (SNMP) Invia le richieste e le risposte dell'operazione come messaggi SNMP.
ms.assetid: 0928981c-4d60-4583-9eef-8127e05b1ba8
keywords:
- Utilizzo di SNMP (Protocol Data Unit)
- Unità dati protocollo SNMP, utilizzo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e40f36fa28f7ff17974d79f4f8ac29b8b6130b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045033"
---
# <a name="working-with-protocol-data-units"></a><span data-ttu-id="58086-105">Utilizzo delle unità dati del protocollo</span><span class="sxs-lookup"><span data-stu-id="58086-105">Working with Protocol Data Units</span></span>

<span data-ttu-id="58086-106">Il Simple Network Management Protocol (SNMP) Invia le richieste e le risposte dell'operazione come messaggi SNMP.</span><span class="sxs-lookup"><span data-stu-id="58086-106">The Simple Network Management Protocol (SNMP) sends operation requests and responses as SNMP messages.</span></span> <span data-ttu-id="58086-107">Un messaggio SNMP è un'unità dati del protocollo SNMP, oltre a elementi di intestazione del messaggio aggiuntivi definiti dalla relativa RFC.</span><span class="sxs-lookup"><span data-stu-id="58086-107">An SNMP message is an SNMP protocol data unit (PDU) plus additional message header elements defined by the relevant RFC.</span></span> <span data-ttu-id="58086-108">Una PDU include un elenco di associazioni variabili.</span><span class="sxs-lookup"><span data-stu-id="58086-108">A PDU includes a variable binding list.</span></span>

<span data-ttu-id="58086-109">La struttura di una PDU è limitata all'implementazione di Microsoft WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="58086-109">The structure of a PDU is restricted to the Microsoft WinSNMP implementation.</span></span> <span data-ttu-id="58086-110">Un'applicazione WinSNMP può accedere a una PDU con un handle del tipo **HSNMP \_ PDU**.</span><span class="sxs-lookup"><span data-stu-id="58086-110">A WinSNMP application can access a PDU with a handle of the type **HSNMP\_PDU**.</span></span> <span data-ttu-id="58086-111">L'applicazione WinSNMP deve creare una PDU prima di chiamare la funzione [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) o la funzione [**SnmpEncodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg) .</span><span class="sxs-lookup"><span data-stu-id="58086-111">The WinSNMP application must create a PDU before it calls the [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) function or the [**SnmpEncodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg) function.</span></span>

<span data-ttu-id="58086-112">L'applicazione può estrarre e aggiornare gli elementi dati di una PDU e rilasciare le risorse allocate per PDU.</span><span class="sxs-lookup"><span data-stu-id="58086-112">The application can extract and update the data elements of a PDU, and release resources allocated for PDUs.</span></span> <span data-ttu-id="58086-113">Per eseguire queste operazioni, l'applicazione usa le [funzioni PDU](winsnmp-functions.md)WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="58086-113">To perform these operations, the application uses the WinSNMP [PDU functions](winsnmp-functions.md).</span></span> <span data-ttu-id="58086-114">La tabella seguente elenca gli argomenti che illustrano l'uso di PDU nell'ambiente di programmazione WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="58086-114">The following table lists topics that discuss working with PDUs in the WinSNMP programming environment.</span></span>



| <span data-ttu-id="58086-115">Argomento</span><span class="sxs-lookup"><span data-stu-id="58086-115">Topic</span></span>                                                                        | <span data-ttu-id="58086-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="58086-116">Description</span></span>                                                        |
|------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="58086-117">Creazione di una PDU</span><span class="sxs-lookup"><span data-stu-id="58086-117">Creating a PDU</span></span>](creating-a-pdu.md)                                         | <span data-ttu-id="58086-118">Viene descritto come creare una PDU.</span><span class="sxs-lookup"><span data-stu-id="58086-118">Describes how to create a PDU.</span></span>                                     |
| [<span data-ttu-id="58086-119">Aggiornamento di una PDU</span><span class="sxs-lookup"><span data-stu-id="58086-119">Updating a PDU</span></span>](updating-a-pdu.md)                                         | <span data-ttu-id="58086-120">Viene descritto come recuperare e aggiornare i campi PDU.</span><span class="sxs-lookup"><span data-stu-id="58086-120">Describes how to retrieve and update PDU fields.</span></span>                   |
| [<span data-ttu-id="58086-121">Duplicazione di una PDU</span><span class="sxs-lookup"><span data-stu-id="58086-121">Duplicating a PDU</span></span>](duplicating-a-pdu.md)                                   | <span data-ttu-id="58086-122">Viene descritto come duplicare una PDU.</span><span class="sxs-lookup"><span data-stu-id="58086-122">Describes how to duplicate a PDU.</span></span>                                  |
| [<span data-ttu-id="58086-123">Convalida di una PDU</span><span class="sxs-lookup"><span data-stu-id="58086-123">Validating a PDU</span></span>](validating-a-pdu.md)                                     | <span data-ttu-id="58086-124">Viene descritta la convalida di una PDU.</span><span class="sxs-lookup"><span data-stu-id="58086-124">Describes the validation of a PDU.</span></span>                                 |
| [<span data-ttu-id="58086-125">PDU di risposta e richiesta corrispondenti</span><span class="sxs-lookup"><span data-stu-id="58086-125">Matching Response and Request PDUs</span></span>](matching-response-and-request-pdus.md) | <span data-ttu-id="58086-126">Viene descritto il processo di corrispondenza di una PDU di risposta a un PDU della richiesta.</span><span class="sxs-lookup"><span data-stu-id="58086-126">Describes the process of matching a response PDU to a request PDU.</span></span> |



 

<span data-ttu-id="58086-127">Per ulteriori informazioni, vedere [utilizzo di elenchi di associazione variabili](working-with-variable-binding-lists.md) e di [oggetti handle di risorsa](resource-handle-objects.md).</span><span class="sxs-lookup"><span data-stu-id="58086-127">For more information, see [Working with Variable Binding Lists](working-with-variable-binding-lists.md) and [Resource Handle Objects](resource-handle-objects.md).</span></span>

 

 




