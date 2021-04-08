---
title: Attività di programmazione WinSNMP
description: Nella tabella seguente sono riepilogate le procedure di programmazione di base che è necessario eseguire per codificare un'applicazione WinSNMP e gli argomenti che forniscono informazioni su tali attività.
ms.assetid: 70c24042-bf44-4484-8e5e-d117e2ba28d5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d75fa8d2ad223fbd8f71eff78c7cd232ddc492a9
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/11/2020
ms.locfileid: "103857981"
---
# <a name="winsnmp-programming-tasks"></a><span data-ttu-id="11f5b-103">Attività di programmazione WinSNMP</span><span class="sxs-lookup"><span data-stu-id="11f5b-103">WinSNMP Programming Tasks</span></span>

<span data-ttu-id="11f5b-104">Nella tabella seguente sono riepilogate le procedure di programmazione di base che è necessario eseguire per codificare un'applicazione WinSNMP e gli argomenti che forniscono informazioni su tali attività.</span><span class="sxs-lookup"><span data-stu-id="11f5b-104">The following table summarizes the basic programming procedures that you must perform to code a WinSNMP application, and the topics that provide information about these tasks.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="11f5b-105">Attività di programmazione</span><span class="sxs-lookup"><span data-stu-id="11f5b-105">Programming task</span></span></th>
<th><span data-ttu-id="11f5b-106">Funzioni e argomenti correlati alle attività</span><span class="sxs-lookup"><span data-stu-id="11f5b-106">Task-related function and topics</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="11f5b-107">Aprire l'applicazione WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="11f5b-107">Open the WinSNMP application.</span></span></td>
<td><span data-ttu-id="11f5b-108">Usare <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup"><strong>SnmpStartup</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="11f5b-108">Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup"><strong>SnmpStartup</strong></a>.</span></span> <span data-ttu-id="11f5b-109">Vedere <a href="opening-and-closing-a-winsnmp-application.md">apertura e chiusura di un'applicazione WinSNMP</a>.</span><span class="sxs-lookup"><span data-stu-id="11f5b-109">See <a href="opening-and-closing-a-winsnmp-application.md">Opening and Closing a WinSNMP Application</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="11f5b-110">Aprire una o più sessioni di WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="11f5b-110">Open one or more WinSNMP sessions.</span></span></td>
<td><span data-ttu-id="11f5b-111">Usare <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession"><strong>SnmpCreateSession</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="11f5b-111">Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession"><strong>SnmpCreateSession</strong></a>.</span></span> <span data-ttu-id="11f5b-112">Vedere <a href="opening-and-closing-a-winsnmp-session.md">apertura e chiusura di una sessione WinSNMP</a>.</span><span class="sxs-lookup"><span data-stu-id="11f5b-112">See <a href="opening-and-closing-a-winsnmp-session.md">Opening and Closing a WinSNMP Session</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="11f5b-113">Eseguire la registrazione per ricevere trap o notifiche.</span><span class="sxs-lookup"><span data-stu-id="11f5b-113">Register to receive traps or notifications.</span></span></td>
<td><span data-ttu-id="11f5b-114">Usare <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister"><strong>SnmpRegister</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="11f5b-114">Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister"><strong>SnmpRegister</strong></a>.</span></span> <span data-ttu-id="11f5b-115">Vedere <a href="managing-traps-and-notifications.md">gestione di trap e notifiche</a>.</span><span class="sxs-lookup"><span data-stu-id="11f5b-115">See <a href="managing-traps-and-notifications.md">Managing Traps and Notifications</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="11f5b-116">Creare uno o più elenchi di associazioni variabili per l'integrazione in una PDU.</span><span class="sxs-lookup"><span data-stu-id="11f5b-116">Create one or more variable binding lists for incorporation in a PDU.</span></span></td>
<td><span data-ttu-id="11f5b-117">Usare <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl"><strong>SnmpCreateVbl</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl"><strong>SnmpDuplicateVbl</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetvb"><strong>SnmpSetVb</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="11f5b-117">Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl"><strong>SnmpCreateVbl</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl"><strong>SnmpDuplicateVbl</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetvb"><strong>SnmpSetVb</strong></a>.</span></span> <span data-ttu-id="11f5b-118">Vedere <a href="working-with-variable-binding-lists.md">utilizzo degli elenchi di associazioni variabili</a>.</span><span class="sxs-lookup"><span data-stu-id="11f5b-118">See <a href="working-with-variable-binding-lists.md">Working with Variable Binding Lists</a>.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="11f5b-119">È possibile che l'applicazione debba chiamare altre <a href="winsnmp-functions.md">funzioni di associazione variabili</a> per creare l'elenco di associazioni variabili.</span><span class="sxs-lookup"><span data-stu-id="11f5b-119">The application may need to call other <a href="winsnmp-functions.md">variable binding functions</a> to create the variable binding list.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="11f5b-120">Creare uno o più PDU per la trasmissione e l'elaborazione.</span><span class="sxs-lookup"><span data-stu-id="11f5b-120">Create one or more PDUs for transmission and processing.</span></span></td>
<td><span data-ttu-id="11f5b-121">Usare <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu"><strong>SnmpCreatePDU</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata"><strong>SnmpSetPduData</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatepdu"><strong>SnmpDuplicatePDU</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="11f5b-121">Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu"><strong>SnmpCreatePDU</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata"><strong>SnmpSetPduData</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatepdu"><strong>SnmpDuplicatePDU</strong></a>.</span></span> <span data-ttu-id="11f5b-122">Vedere <a href="working-with-protocol-data-units.md">utilizzo delle unità dati del protocollo</a>.</span><span class="sxs-lookup"><span data-stu-id="11f5b-122">See <a href="working-with-protocol-data-units.md">Working with Protocol Data Units</a>.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="11f5b-123">Per creare la PDU, potrebbe essere necessario che l'applicazione chiami altre <a href="winsnmp-functions.md">funzioni PDU</a> e <a href="winsnmp-functions.md">funzioni di utilità</a> WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="11f5b-123">The application may need to call other <a href="winsnmp-functions.md">PDU functions</a> and WinSNMP <a href="winsnmp-functions.md">utility functions</a> to create the PDU.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="11f5b-124">Inviare una o più richieste di operazione SNMP.</span><span class="sxs-lookup"><span data-stu-id="11f5b-124">Submit one or more SNMP operation requests.</span></span></td>
<td><span data-ttu-id="11f5b-125">Usare <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg"><strong>SnmpSendMsg</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="11f5b-125">Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg"><strong>SnmpSendMsg</strong></a>.</span></span> <span data-ttu-id="11f5b-126">Vedere <a href="sending-snmp-messages.md">invio di messaggi SNMP</a>.</span><span class="sxs-lookup"><span data-stu-id="11f5b-126">See <a href="sending-snmp-messages.md">Sending SNMP Messages</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="11f5b-127">Recuperare la risposta alla richiesta dell'operazione SNMP.</span><span class="sxs-lookup"><span data-stu-id="11f5b-127">Retrieve the response to the SNMP operation request.</span></span></td>
<td><span data-ttu-id="11f5b-128">Usare <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg"><strong>SnmpRecvMsg</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="11f5b-128">Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg"><strong>SnmpRecvMsg</strong></a>.</span></span> <span data-ttu-id="11f5b-129">Vedere <a href="receiving-snmp-messages.md">ricezione di messaggi SNMP</a>.</span><span class="sxs-lookup"><span data-stu-id="11f5b-129">See <a href="receiving-snmp-messages.md">Receiving SNMP Messages</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="11f5b-130">Elaborare la risposta alla richiesta.</span><span class="sxs-lookup"><span data-stu-id="11f5b-130">Process the request response.</span></span></td>
<td><span data-ttu-id="11f5b-131">Usare la logica specifica dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="11f5b-131">Use application-specific logic.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="11f5b-132">Chiudere ogni sessione WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="11f5b-132">Close each WinSNMP session.</span></span></td>
<td><span data-ttu-id="11f5b-133">Usare <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose"><strong>SnmpClose</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="11f5b-133">Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose"><strong>SnmpClose</strong></a>.</span></span> <span data-ttu-id="11f5b-134">Vedere <a href="opening-and-closing-a-winsnmp-session.md">apertura e chiusura di una sessione WinSNMP</a>.</span><span class="sxs-lookup"><span data-stu-id="11f5b-134">See <a href="opening-and-closing-a-winsnmp-session.md">Opening and Closing a WinSNMP Session</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="11f5b-135">Chiudere l'applicazione WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="11f5b-135">Close the WinSNMP application.</span></span></td>
<td><span data-ttu-id="11f5b-136">Usare <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup"><strong>SnmpCleanup</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="11f5b-136">Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup"><strong>SnmpCleanup</strong></a>.</span></span> <span data-ttu-id="11f5b-137">Vedere <a href="opening-and-closing-a-winsnmp-application.md">apertura e chiusura di un'applicazione WinSNMP</a>.</span><span class="sxs-lookup"><span data-stu-id="11f5b-137">See <a href="opening-and-closing-a-winsnmp-application.md">Opening and Closing a WinSNMP Application</a>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="11f5b-138">Gli argomenti seguenti contengono informazioni aggiuntive su altri concetti di programmazione generali specifici per l'ambiente WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="11f5b-138">The following topics contain additional information about other general programming concepts specific to the WinSNMP environment.</span></span>



|                                                                    |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="11f5b-139">Attività di programmazione generali</span><span class="sxs-lookup"><span data-stu-id="11f5b-139">General programming tasks</span></span>](general-winsnmp-programming-tasks.md) | <span data-ttu-id="11f5b-140">[Gestione degli identificatori di oggetto](managing-object-identifiers.md)che[liberano descrittori WinSNMP](freeing-winsnmp-descriptors.md)</span><span class="sxs-lookup"><span data-stu-id="11f5b-140">[Managing Object Identifiers](managing-object-identifiers.md)[Freeing WinSNMP Descriptors](freeing-winsnmp-descriptors.md)</span></span><br/> [<span data-ttu-id="11f5b-141">Impostazione della modalità di conversione dell'entità e del contesto</span><span class="sxs-lookup"><span data-stu-id="11f5b-141">Setting the Entity and Context Translation Mode</span></span>](setting-the-entity-and-context-translation-mode.md)<br/> [<span data-ttu-id="11f5b-142">Gestione dei criteri di ritrasmissione</span><span class="sxs-lookup"><span data-stu-id="11f5b-142">Managing the Retransmission Policy</span></span>](managing-the-retransmission-policy.md)<br/> [<span data-ttu-id="11f5b-143">Scrittura di applicazioni WinSNMP con più thread</span><span class="sxs-lookup"><span data-stu-id="11f5b-143">Writing WinSNMP Applications with Multiple Threads</span></span>](writing-winsnmp-applications-with-multiple-threads.md)<br/> [<span data-ttu-id="11f5b-144">Registrazione di un'applicazione agente SNMP</span><span class="sxs-lookup"><span data-stu-id="11f5b-144">Registering an SNMP Agent Application</span></span>](registering-an-snmp-agent-application.md)<br/> |



 

<span data-ttu-id="11f5b-145">Inoltre, è possibile che l'applicazione WinSNMP debba incorporare le chiamate alle funzioni WinSNMP seguenti: [**SnmpFreeVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl), [**SnmpFreeEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity), [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor), [**SnmpFreeContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext)e [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu).</span><span class="sxs-lookup"><span data-stu-id="11f5b-145">In addition, the WinSNMP application may need to incorporate calls to the following WinSNMP functions: [**SnmpFreeVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl), [**SnmpFreeEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity), [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor), [**SnmpFreeContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext), and [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu).</span></span> <span data-ttu-id="11f5b-146">Ciò consente all'implementazione di Microsoft WinSNMP di liberare oggetti di memoria WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="11f5b-146">This enables the Microsoft WinSNMP implementation to free WinSNMP memory objects.</span></span> <span data-ttu-id="11f5b-147">Come regola generale, l'applicazione WinSNMP deve liberare tutte le risorse allocate come risultato di una chiamata a una funzione WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="11f5b-147">As a general rule, the WinSNMP application should free all resources allocated as the result of a call to a WinSNMP function.</span></span> <span data-ttu-id="11f5b-148">Per ulteriori informazioni sulla deallocazione delle risorse, vedere [allocazione di oggetti memoria WinSNMP](allocating-winsnmp-memory-objects.md).</span><span class="sxs-lookup"><span data-stu-id="11f5b-148">For additional information about deallocating resources, see [Allocating WinSNMP Memory Objects](allocating-winsnmp-memory-objects.md).</span></span>

 

 





