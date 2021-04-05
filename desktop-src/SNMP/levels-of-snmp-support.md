---
title: Livelli di supporto SNMP
description: L'implementazione di Microsoft WinSNMP fornisce supporto per le comunicazioni SNMP di livello 2.
ms.assetid: 9874ad9b-4eb9-4d63-816b-fe444c5b4d8a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92b48c930266073f10e5cb8019a7462317bd798c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104116752"
---
# <a name="levels-of-snmp-support"></a>Livelli di supporto SNMP

L'implementazione di Microsoft WinSNMP fornisce supporto per le comunicazioni SNMP di livello 2. Il livello 2 supporta il protocollo SNMPv2 standard IETF (Internet Engineering Task Force), come definito nella RFC 1902-1908. Supporta inoltre il wrapper di messaggi basato sulla community come definito nella specifica RFC 1901 (SNMPv2C).

Il supporto per le comunicazioni di livello 2 include i servizi di codifica e decodifica dei messaggi, in precedenza denominati supporto delle comunicazioni di livello 0 in WinSNMP versione 1.1 a. Il livello 2 supporta inoltre tutte le operazioni del protocollo SNMPv1, in precedenza chiamate supporto per le comunicazioni di livello 1 in WinSNMP versione 1.1 a.

L'implementazione restituisce il livello massimo di comunicazioni SNMP supportato in risposta a una chiamata da parte dell'applicazione WinSNMP alla funzione [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) .

Se l'applicazione WinSNMP usa l'implementazione solo per la codifica e la decodifica dei messaggi SNMP, l'applicazione deve eseguire le trasformazioni necessarie che l'implementazione avrebbe eseguito. Ciò include la conversione dei trap SNMPv1 restituiti da una chiamata alla funzione [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) a trap SNMPv2C. Include anche la traduzione dei tipi PDU definiti da SNMPv1 nel tipo PDU pertinente definito da SNMPv2C, in base allo standard RFC 1908.

 

 




