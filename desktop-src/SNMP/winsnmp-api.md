---
title: API WinSNMP
description: L'interfaccia di programmazione delle applicazioni di Microsoft Windows (l'API WinSNMP) versione 1.1 a e 2,0 consentono di sviluppare applicazioni di gestione della rete basate su SNMP eseguite nell'ambiente Windows.
ms.assetid: 54d9b61a-815a-41c3-9365-ec4478acc3f2
keywords:
- API WinSNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12d502060daa2931ca67c4476448347602159c98
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047079"
---
# <a name="winsnmp-api"></a>API WinSNMP

\[SNMP è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. Usare invece [gestione remota Windows](/windows/desktop/WinRM/portal), ovvero l'implementazione Microsoft di WS-Man.\]

L'interfaccia di programmazione delle applicazioni di Microsoft Windows (l'API WinSNMP) versione 1.1 a e 2,0 consentono di sviluppare applicazioni di gestione della rete basate su SNMP eseguite nell'ambiente Windows. Il Simple Network Management Protocol (SNMP) è un protocollo di richiesta-risposta che trasferisce le informazioni di gestione tra le entità del protocollo.

WinSNMP è stato sviluppato congiuntamente con la collaborazione, l'input e il supporto di diverse società, associazioni e singoli utenti.

Nella prima parte di questa panoramica vengono fornite informazioni sull'addendum WinSNMP 2,0, le versioni SNMP e un elenco delle richieste di commenti (RFC) pertinenti. Viene inoltre descritto il modello WinSNMP e i componenti e le funzionalità dell'implementazione Microsoft WinSNMP. Vengono inoltre fornite informazioni sui concetti di gestione e comunicazione dei dati necessari per programmare nell'ambiente WinSNMP.

La seconda sezione illustra le funzioni WinSNMP e le attività di programmazione WinSNMP correlate seguenti:

-   [Apertura e chiusura di un'applicazione WinSNMP](opening-and-closing-a-winsnmp-application.md)
-   [Apertura e chiusura di una sessione WinSNMP](opening-and-closing-a-winsnmp-session.md)
-   [Gestione di trap e notifiche](managing-traps-and-notifications.md)
-   [Utilizzo degli elenchi di associazioni variabili](working-with-variable-binding-lists.md)
-   [Utilizzo delle unità dati del protocollo](working-with-protocol-data-units.md)
-   [Invio di messaggi SNMP](sending-snmp-messages.md)
-   [Ricezione di messaggi SNMP](receiving-snmp-messages.md)
-   [Gestione degli identificatori di oggetto](managing-object-identifiers.md)
-   [Liberazione di descrittori WinSNMP](freeing-winsnmp-descriptors.md)
-   [Impostazione della modalità di conversione dell'entità e del contesto](setting-the-entity-and-context-translation-mode.md)
-   [Gestione dei criteri di ritrasmissione](managing-the-retransmission-policy.md)
-   [Scrittura di applicazioni WinSNMP con più thread](writing-winsnmp-applications-with-multiple-threads.md)
-   [Registrazione di un'applicazione agente SNMP](registering-an-snmp-agent-application.md)

Prima di leggere questa panoramica, è necessario avere familiarità con i concetti di base relativi alla programmazione SNMP e Windows. Per ulteriori informazioni su SNMP, vedere [Simple Network Management Protocol](simple-network-management-protocol-snmp-.md) e le relative richieste di commenti (RFC) pubblicate da Internet Engineering Task Force (IETF).

 

 