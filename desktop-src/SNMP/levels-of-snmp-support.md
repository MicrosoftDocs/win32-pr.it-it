---
title: Livelli di supporto SNMP
description: L'implementazione Microsoft WinSNMP fornisce il supporto per le comunicazioni SNMP di livello 2.
ms.assetid: 9874ad9b-4eb9-4d63-816b-fe444c5b4d8a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa76a475ed266a7a4928a79f809b7011a537c777c89ea0a97d06983d6656a9ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009459"
---
# <a name="levels-of-snmp-support"></a>Livelli di supporto SNMP

L'implementazione Microsoft WinSNMP fornisce il supporto per le comunicazioni SNMP di livello 2. Il livello 2 supporta il protocollo SNMPv2 standard IETF (Internet Engineering Task Force), come definito nelle RFC 1902-1908. Supporta anche il wrapper di messaggi basato sulla community, come definito in RFC 1901 (SNMPv2C).

Il supporto per le comunicazioni di livello 2 include servizi di codifica e decodifica dei messaggi, denominati in precedenza supporto delle comunicazioni di livello 0 in WinSNMP versione 1.1a. Il livello 2 supporta anche tutte le operazioni del protocollo SNMPv1, precedentemente denominate supporto delle comunicazioni di livello 1 in WinSNMP versione 1.1a.

L'implementazione restituisce il livello massimo di comunicazioni SNMP supportate in risposta a una chiamata dell'applicazione WinSNMP alla [**funzione SnmpStartup.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup)

Se l'applicazione WinSNMP usa l'implementazione solo per la codifica e la decodifica dei messaggi SNMP, l'applicazione deve eseguire le trasformazioni necessarie che l'implementazione avrebbe eseguito. Ciò include la conversione di trap SNMPv1 restituite da una chiamata alla [**funzione SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) in trap SNMPv2C. Include anche la conversione dei tipi PDU definiti da SNMPv1 nel tipo PDU pertinente definito da SNMPv2C, in conformità con RFC 1908.

 

 




