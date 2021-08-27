---
title: Attività di programmazione WinSNMP
description: Nella tabella seguente sono riepilogate le procedure di programmazione di base che è necessario eseguire per codificare un'applicazione WinSNMP e gli argomenti che forniscono informazioni su queste attività.
ms.assetid: 70c24042-bf44-4484-8e5e-d117e2ba28d5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bb83d6d61311866ddb84d3980f5742f82f51405
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479397"
---
# <a name="winsnmp-programming-tasks"></a>Attività di programmazione WinSNMP

Nella tabella seguente sono riepilogate le procedure di programmazione di base che è necessario eseguire per codificare un'applicazione WinSNMP e gli argomenti che forniscono informazioni su queste attività.




| Attività di programmazione | Funzione e argomenti correlati alle attività | 
|------------------|----------------------------------|
| Aprire l'applicazione WinSNMP. | Usare <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup"><strong>SnmpStartup</strong></a>. Vedere <a href="opening-and-closing-a-winsnmp-application.md">Apertura e chiusura di un'applicazione WinSNMP.</a><br /> | 
| Aprire una o più sessioni WinSNMP. | Usare <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession"><strong>SnmpCreateSession</strong></a>. Vedere <a href="opening-and-closing-a-winsnmp-session.md">Apertura e chiusura di una sessione WinSNMP.</a><br /> | 
| Registrarsi per ricevere trap o notifiche. | Usare <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister"><strong>SnmpRegister</strong></a>. Vedere <a href="managing-traps-and-notifications.md">Gestione di trap e notifiche.</a><br /> | 
| Creare uno o più elenchi di associazioni di variabili per l'incorporamento in una PDU. | Usare <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl"><strong>SnmpCreateVbl</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl"><strong>SnmpDuplicateVbl</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetvb"><strong>SnmpSetVb</strong></a>. Vedere <a href="working-with-variable-binding-lists.md">Uso degli elenchi di associazioni di variabili</a>.<br /><blockquote>[!Note]<br />L'applicazione potrebbe dover chiamare altre funzioni di <a href="winsnmp-functions.md">associazione di variabili per</a> creare l'elenco di associazioni delle variabili.</blockquote><br /> | 
| Creare uno o più PDU per la trasmissione e l'elaborazione. | Usare <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu"><strong>SnmpCreatePDU</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata"><strong>SnmpSetPduData</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatepdu"><strong>SnmpDuplicatePDU</strong></a>. Vedere <a href="working-with-protocol-data-units.md">Uso delle unità dati di protocollo.</a><br /><blockquote>[!Note]<br />L'applicazione potrebbe dover chiamare altre <a href="winsnmp-functions.md">funzioni PDU e</a> funzioni di utilità WinSNMP <a href="winsnmp-functions.md"></a> per creare la PDU.</blockquote><br /> | 
| Inviare una o più richieste di operazioni SNMP. | Usare <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg"><strong>SnmpSendMsg</strong></a>. Vedere <a href="sending-snmp-messages.md">Invio di messaggi SNMP.</a><br /> | 
| Recuperare la risposta alla richiesta dell'operazione SNMP. | Usare <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg"><strong>SnmpRecvMsg</strong></a>. Vedere <a href="receiving-snmp-messages.md">Ricezione di messaggi SNMP.</a><br /> | 
| Elaborare la risposta della richiesta. | Usare la logica specifica dell'applicazione. | 
| Chiudere ogni sessione WinSNMP. | Usare <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose"><strong>SnmpClose</strong></a>. Vedere <a href="opening-and-closing-a-winsnmp-session.md">Apertura e chiusura di una sessione WinSNMP.</a><br /> | 
| Chiudere l'applicazione WinSNMP. | Usare <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup"><strong>SnmpCleanup</strong></a>. Vedere <a href="opening-and-closing-a-winsnmp-application.md">Apertura e chiusura di un'applicazione WinSNMP.</a><br /> | 




 

Gli argomenti seguenti contengono informazioni aggiuntive su altri concetti di programmazione generali specifici dell'ambiente WinSNMP.



| Argomento                                                              | Concetti                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Attività di programmazione generali](general-winsnmp-programming-tasks.md) | [Gestione degli identificatori di oggetto](managing-object-identifiers.md)che[liberano descrittori WinSNMP](freeing-winsnmp-descriptors.md)<br/> [Impostazione della modalità di conversione di entità e contesto](setting-the-entity-and-context-translation-mode.md)<br/> [Gestione dei criteri di ritrasmissione](managing-the-retransmission-policy.md)<br/> [Scrittura di applicazioni WinSNMP con più thread](writing-winsnmp-applications-with-multiple-threads.md)<br/> [Registrazione di un'applicazione agente SNMP](registering-an-snmp-agent-application.md)<br/> |



 

Inoltre, l'applicazione WinSNMP potrebbe dover incorporare chiamate alle funzioni WinSNMP [**seguenti: SnmpFreeVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl), [**SnmpFreeEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity), [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor), [**SnmpFreeContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext)e [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu). Ciò consente all'implementazione Microsoft WinSNMP di liberare oggetti di memoria WinSNMP. Come regola generale, l'applicazione WinSNMP deve liberare tutte le risorse allocate come risultato di una chiamata a una funzione WinSNMP. Per altre informazioni sulla deallocazione delle risorse, vedere [Allocazione di oggetti di memoria WinSNMP.](allocating-winsnmp-memory-objects.md)

 

 





