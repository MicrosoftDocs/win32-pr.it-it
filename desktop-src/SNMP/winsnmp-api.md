---
title: WinSNMP API
description: Microsoft Windows SNMP Application Programming Interface (API WinSNMP) versioni 1.1a e 2.0 consente di sviluppare applicazioni di gestione di rete basate su SNMP eseguite nell'ambiente Windows.
ms.assetid: 54d9b61a-815a-41c3-9365-ec4478acc3f2
keywords:
- WinSNMP API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c38f6205b8d5ad2315be877f62f0f81f17b5737e557d5db2683163ff26edf62c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142984"
---
# <a name="winsnmp-api"></a>WinSNMP API

\[SNMP è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. Usare invece Windows [gestione remota](/windows/desktop/WinRM/portal), ovvero l'implementazione Microsoft di WS-Man.\]

Microsoft Windows SNMP Application Programming Interface (API WinSNMP) versioni 1.1a e 2.0 consente di sviluppare applicazioni di gestione di rete basate su SNMP eseguite nell'ambiente Windows. Il Simple Network Management Protocol (SNMP) è un protocollo di richiesta-risposta che trasferisce le informazioni di gestione tra le entità del protocollo.

WinSNMP è stato sviluppato congiuntamente con la cooperazione, l'input e il supporto di diverse aziende, associazioni e singoli utenti.

La prima parte di questa panoramica fornisce informazioni su WinSNMP 2.0 Addendum, versioni SNMP e un elenco delle RFC pertinenti. Descrive anche il modello WinSNMP e i componenti e le funzionalità dell'implementazione di Microsoft WinSNMP. Fornisce anche informazioni sui concetti relativi alla gestione dei dati e alle comunicazioni che è necessario programmare nell'ambiente WinSNMP.

La seconda sezione illustra le funzioni WinSNMP e le attività di programmazione WinSNMP correlate seguenti:

-   [Apertura e chiusura di un'applicazione WinSNMP](opening-and-closing-a-winsnmp-application.md)
-   [Apertura e chiusura di una sessione WinSNMP](opening-and-closing-a-winsnmp-session.md)
-   [Gestione di trap e notifiche](managing-traps-and-notifications.md)
-   [Uso di elenchi di associazioni di variabili](working-with-variable-binding-lists.md)
-   [Uso delle unità dati del protocollo](working-with-protocol-data-units.md)
-   [Invio di messaggi SNMP](sending-snmp-messages.md)
-   [Ricezione di messaggi SNMP](receiving-snmp-messages.md)
-   [Gestione degli identificatori di oggetto](managing-object-identifiers.md)
-   [Freeing WinSNMP descriptors (Liberare descrittori WinSNMP)](freeing-winsnmp-descriptors.md)
-   [Impostazione della modalità di conversione dell'entità e del contesto](setting-the-entity-and-context-translation-mode.md)
-   [Gestione dei criteri di ritrasmissione](managing-the-retransmission-policy.md)
-   [Scrittura di applicazioni WinSNMP con più thread](writing-winsnmp-applications-with-multiple-threads.md)
-   [Registrazione di un'applicazione agente SNMP](registering-an-snmp-agent-application.md)

Prima di leggere questa panoramica, è necessario avere familiarità con i concetti di base di SNMP e Windows programmazione. Per altre informazioni su SNMP, vedere [Simple Network Management Protocol](simple-network-management-protocol-snmp-.md) e le rfc (Requests for Comments) pertinenti pubblicate da Internet Engineering Task Force (IETF).

 

 