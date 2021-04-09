---
title: Modello WinSNMP
description: Il modello conforme a WinSNMP include i componenti di base seguenti.
ms.assetid: 491df017-0b91-4fcf-97c3-4e296c3324bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff7ae4fa1c1ee56fc534e4aa4c9bffefb8d7f4d2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044370"
---
# <a name="the-winsnmp-model"></a>Modello WinSNMP

Il modello conforme a WinSNMP include i componenti di base seguenti:

-   Un'applicazione di gestione di rete SNMP abilitata per WinSNMP, ovvero un' *applicazione* conforme a WinSNMP
-   Livello della funzione WinSNMP
-   Un provider di servizi SNMP abilitato per WinSNMP, ovvero un' *implementazione* conforme a WinSNMP

Le applicazioni di gestione della rete che devono fornire messaggi SNMP funzionano in modo efficiente in un ambiente basato su eventi. Questo perché SNMP è un protocollo basato su datagramma o senza connessione tra entità remote che non stabiliscono circuiti virtuali.

Poiché le applicazioni di Microsoft Windows sono anche basate sugli eventi, WinSNMP utilizza un modello di programmazione in cui la ricezione e l'elaborazione di applicazioni di gestione degli *eventi di messaggio* asincrono. Un evento di messaggio asincrono può essere una richiesta di operazione SNMP da parte di un'applicazione di gestione o la risposta a una richiesta da parte di un'applicazione di Agent.

SNMP invia richieste e risposte come messaggi SNMP. Un messaggio SNMP è un'unità dati del protocollo SNMP, oltre a elementi di intestazione del messaggio aggiuntivi definiti dalla relativa RFC. Per ulteriori informazioni, vedere [informazioni sui messaggi SNMP](about-snmp-messages.md), [utilizzo di elenchi di associazioni variabili](working-with-variable-binding-lists.md) e [utilizzo delle unità dati del protocollo](working-with-protocol-data-units.md).

 

 




