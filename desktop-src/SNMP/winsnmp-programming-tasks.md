---
title: Attività di programmazione WinSNMP
description: La tabella seguente riepiloga le procedure di programmazione di base che è necessario eseguire per codificare un'applicazione WinSNMP e gli argomenti che forniscono informazioni su queste attività.
ms.assetid: 70c24042-bf44-4484-8e5e-d117e2ba28d5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7543a0fef8fff3f2ef1672ee29d72b0f82b75af7
ms.sourcegitcommit: 5a78723ad484955ac91a23cf282cf9c176c1eab6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/22/2021
ms.locfileid: "114436621"
---
# <a name="winsnmp-programming-tasks"></a>Attività di programmazione WinSNMP

La tabella seguente riepiloga le procedure di programmazione di base che è necessario eseguire per codificare un'applicazione WinSNMP e gli argomenti che forniscono informazioni su queste attività.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Attività di programmazione</th>
<th>Argomenti e funzioni correlate alle attività</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Aprire l'applicazione WinSNMP.</td>
<td>Usare <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup"><strong>SnmpStartup</strong></a>. Vedere <a href="opening-and-closing-a-winsnmp-application.md">Apertura e chiusura di un'applicazione WinSNMP</a>.<br/></td>
</tr>
<tr class="even">
<td>Aprire una o più sessioni WinSNMP.</td>
<td>Usare <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession"><strong>SnmpCreateSession</strong></a>. Vedere <a href="opening-and-closing-a-winsnmp-session.md">Apertura e chiusura di una sessione WinSNMP</a>.<br/></td>
</tr>
<tr class="odd">
<td>Registrarsi per ricevere trap o notifiche.</td>
<td>Usare <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister"><strong>SnmpRegister</strong></a>. Vedere <a href="managing-traps-and-notifications.md">Gestione di trap e notifiche</a>.<br/></td>
</tr>
<tr class="even">
<td>Creare uno o più elenchi di associazioni di variabili per l'incorporamento in una PDU.</td>
<td>Usare <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl"><strong>SnmpCreateVbl</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl"><strong>SnmpDuplicateVbl</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetvb"><strong>SnmpSetVb</strong></a>. Vedere <a href="working-with-variable-binding-lists.md">Uso degli elenchi di associazioni di variabili</a>.<br/>
<blockquote>
[!Note]<br />
L'applicazione potrebbe dover chiamare altre funzioni di <a href="winsnmp-functions.md">associazione di variabili per</a> creare l'elenco di associazioni delle variabili.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>Creare uno o più PDU per la trasmissione e l'elaborazione.</td>
<td>Usare <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu"><strong>SnmpCreatePDU</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata"><strong>SnmpSetPduData</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatepdu"><strong>SnmpDuplicatePDU</strong></a>. Vedere <a href="working-with-protocol-data-units.md">Uso delle unità dati del protocollo</a>.<br/>
<blockquote>
[!Note]<br />
L'applicazione potrebbe dover chiamare altre <a href="winsnmp-functions.md">funzioni PDU e</a> funzioni di utilità WinSNMP <a href="winsnmp-functions.md"></a> per creare la PDU.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Inviare una o più richieste di operazioni SNMP.</td>
<td>Usare <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg"><strong>SnmpSendMsg</strong></a>. Vedere <a href="sending-snmp-messages.md">Invio di messaggi SNMP</a>.<br/></td>
</tr>
<tr class="odd">
<td>Recuperare la risposta alla richiesta dell'operazione SNMP.</td>
<td>Usare <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg"><strong>SnmpRecvMsg</strong></a>. Vedere <a href="receiving-snmp-messages.md">Ricezione di messaggi SNMP</a>.<br/></td>
</tr>
<tr class="even">
<td>Elaborare la risposta della richiesta.</td>
<td>Usare la logica specifica dell'applicazione.</td>
</tr>
<tr class="odd">
<td>Chiudere ogni sessione WinSNMP.</td>
<td>Usare <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose"><strong>SnmpClose</strong></a>. Vedere <a href="opening-and-closing-a-winsnmp-session.md">Apertura e chiusura di una sessione WinSNMP</a>.<br/></td>
</tr>
<tr class="even">
<td>Chiudere l'applicazione WinSNMP.</td>
<td>Usare <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup"><strong>SnmpCleanup</strong></a>. Vedere <a href="opening-and-closing-a-winsnmp-application.md">Apertura e chiusura di un'applicazione WinSNMP</a>.<br/></td>
</tr>
</tbody>
</table>



 

Gli argomenti seguenti contengono informazioni aggiuntive su altri concetti di programmazione generali specifici dell'ambiente WinSNMP.



| Argomento                                                              | Concetti                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Attività di programmazione generali](general-winsnmp-programming-tasks.md) | [Gestione degli identificatori di oggetto](managing-object-identifiers.md)che[liberano i descrittori WinSNMP](freeing-winsnmp-descriptors.md)<br/> [Impostazione della modalità di conversione di entità e contesto](setting-the-entity-and-context-translation-mode.md)<br/> [Gestione dei criteri di ritrasmissione](managing-the-retransmission-policy.md)<br/> [Scrittura di applicazioni WinSNMP con più thread](writing-winsnmp-applications-with-multiple-threads.md)<br/> [Registrazione di un'applicazione agente SNMP](registering-an-snmp-agent-application.md)<br/> |



 

Inoltre, l'applicazione WinSNMP potrebbe dover incorporare chiamate alle funzioni WinSNMP seguenti: [**SnmpFreeVbl,**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl) [**SnmpFreeEntity,**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity) [**SnmpFreeDescriptor,**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) [**SnmpFreeContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext)e [**SnmpFreePdu.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu) Ciò consente all'implementazione Microsoft WinSNMP di liberare oggetti di memoria WinSNMP. Come regola generale, l'applicazione WinSNMP deve liberare tutte le risorse allocate come risultato di una chiamata a una funzione WinSNMP. Per altre informazioni sulla deallocazione delle risorse, vedere [Allocazione di oggetti di memoria WinSNMP](allocating-winsnmp-memory-objects.md).

 

 





