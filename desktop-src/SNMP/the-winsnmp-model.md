---
title: Modello WinSNMP
description: Il modello conforme a WinSNMP include i componenti di base seguenti.
ms.assetid: 491df017-0b91-4fcf-97c3-4e296c3324bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8814786b6ae44527460930daf5a9e8164645ca0ecfce52824831b2dbc7e61e80
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127581"
---
# <a name="the-winsnmp-model"></a>Modello WinSNMP

Il modello conforme a WinSNMP include i componenti di base seguenti:

-   Un'applicazione di gestione di rete SNMP abilitata per WinSNMP, ad esempio un'applicazione conforme a *WinSNMP*
-   Livello funzione WinSNMP
-   Un provider di servizi SNMP abilitato per WinSNMP, ad  esempio un'implementazione conforme a WinSNMP

Le applicazioni di gestione di rete che devono comunicare i messaggi SNMP funzionano in modo efficiente in un ambiente basato su eventi. Questo perché SNMP è un protocollo basato su datagrammi o senza connessione tra entità remote che non stabiliscono circuiti virtuali.

Poiché anche le Windows Microsoft Windows sono guidate dagli eventi, WinSNMP usa un modello di programmazione in cui la ricezione e l'elaborazione di eventi *di* messaggio asincroni guidano le applicazioni di gestione. Un evento di messaggio asincrono può essere una richiesta di operazione SNMP da un'applicazione di gestione o la risposta a una richiesta da parte di un'applicazione agente.

SNMP invia richieste e risposte come messaggi SNMP. Un messaggio SNMP è un'unità PDU (Protocol Data Unit) SNMP e altri elementi di intestazione del messaggio definiti dalla RFC pertinente. Per altre informazioni, vedere [About SNMP Messages](about-snmp-messages.md), [Working with Variable Binding Lists](working-with-variable-binding-lists.md) e Working with Protocol [Data Units.](working-with-protocol-data-units.md)

 

 




