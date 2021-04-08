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
# <a name="winsnmp-programming-tasks"></a>Attività di programmazione WinSNMP

Nella tabella seguente sono riepilogate le procedure di programmazione di base che è necessario eseguire per codificare un'applicazione WinSNMP e gli argomenti che forniscono informazioni su tali attività.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Attività di programmazione</th>
<th>Funzioni e argomenti correlati alle attività</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Aprire l'applicazione WinSNMP.</td>
<td>Usare <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup"><strong>SnmpStartup</strong></a>. Vedere <a href="opening-and-closing-a-winsnmp-application.md">apertura e chiusura di un'applicazione WinSNMP</a>.<br/></td>
</tr>
<tr class="even">
<td>Aprire una o più sessioni di WinSNMP.</td>
<td>Usare <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession"><strong>SnmpCreateSession</strong></a>. Vedere <a href="opening-and-closing-a-winsnmp-session.md">apertura e chiusura di una sessione WinSNMP</a>.<br/></td>
</tr>
<tr class="odd">
<td>Eseguire la registrazione per ricevere trap o notifiche.</td>
<td>Usare <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister"><strong>SnmpRegister</strong></a>. Vedere <a href="managing-traps-and-notifications.md">gestione di trap e notifiche</a>.<br/></td>
</tr>
<tr class="even">
<td>Creare uno o più elenchi di associazioni variabili per l'integrazione in una PDU.</td>
<td>Usare <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl"><strong>SnmpCreateVbl</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl"><strong>SnmpDuplicateVbl</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetvb"><strong>SnmpSetVb</strong></a>. Vedere <a href="working-with-variable-binding-lists.md">utilizzo degli elenchi di associazioni variabili</a>.<br/>
<blockquote>
[!Note]<br />
È possibile che l'applicazione debba chiamare altre <a href="winsnmp-functions.md">funzioni di associazione variabili</a> per creare l'elenco di associazioni variabili.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>Creare uno o più PDU per la trasmissione e l'elaborazione.</td>
<td>Usare <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu"><strong>SnmpCreatePDU</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata"><strong>SnmpSetPduData</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatepdu"><strong>SnmpDuplicatePDU</strong></a>. Vedere <a href="working-with-protocol-data-units.md">utilizzo delle unità dati del protocollo</a>.<br/>
<blockquote>
[!Note]<br />
Per creare la PDU, potrebbe essere necessario che l'applicazione chiami altre <a href="winsnmp-functions.md">funzioni PDU</a> e <a href="winsnmp-functions.md">funzioni di utilità</a> WinSNMP.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Inviare una o più richieste di operazione SNMP.</td>
<td>Usare <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg"><strong>SnmpSendMsg</strong></a>. Vedere <a href="sending-snmp-messages.md">invio di messaggi SNMP</a>.<br/></td>
</tr>
<tr class="odd">
<td>Recuperare la risposta alla richiesta dell'operazione SNMP.</td>
<td>Usare <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg"><strong>SnmpRecvMsg</strong></a>. Vedere <a href="receiving-snmp-messages.md">ricezione di messaggi SNMP</a>.<br/></td>
</tr>
<tr class="even">
<td>Elaborare la risposta alla richiesta.</td>
<td>Usare la logica specifica dell'applicazione.</td>
</tr>
<tr class="odd">
<td>Chiudere ogni sessione WinSNMP.</td>
<td>Usare <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose"><strong>SnmpClose</strong></a>. Vedere <a href="opening-and-closing-a-winsnmp-session.md">apertura e chiusura di una sessione WinSNMP</a>.<br/></td>
</tr>
<tr class="even">
<td>Chiudere l'applicazione WinSNMP.</td>
<td>Usare <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup"><strong>SnmpCleanup</strong></a>. Vedere <a href="opening-and-closing-a-winsnmp-application.md">apertura e chiusura di un'applicazione WinSNMP</a>.<br/></td>
</tr>
</tbody>
</table>



 

Gli argomenti seguenti contengono informazioni aggiuntive su altri concetti di programmazione generali specifici per l'ambiente WinSNMP.



|                                                                    |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Attività di programmazione generali](general-winsnmp-programming-tasks.md) | [Gestione degli identificatori di oggetto](managing-object-identifiers.md)che[liberano descrittori WinSNMP](freeing-winsnmp-descriptors.md)<br/> [Impostazione della modalità di conversione dell'entità e del contesto](setting-the-entity-and-context-translation-mode.md)<br/> [Gestione dei criteri di ritrasmissione](managing-the-retransmission-policy.md)<br/> [Scrittura di applicazioni WinSNMP con più thread](writing-winsnmp-applications-with-multiple-threads.md)<br/> [Registrazione di un'applicazione agente SNMP](registering-an-snmp-agent-application.md)<br/> |



 

Inoltre, è possibile che l'applicazione WinSNMP debba incorporare le chiamate alle funzioni WinSNMP seguenti: [**SnmpFreeVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl), [**SnmpFreeEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity), [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor), [**SnmpFreeContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext)e [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu). Ciò consente all'implementazione di Microsoft WinSNMP di liberare oggetti di memoria WinSNMP. Come regola generale, l'applicazione WinSNMP deve liberare tutte le risorse allocate come risultato di una chiamata a una funzione WinSNMP. Per ulteriori informazioni sulla deallocazione delle risorse, vedere [allocazione di oggetti memoria WinSNMP](allocating-winsnmp-memory-objects.md).

 

 





