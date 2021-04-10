---
title: Gestione di trap e notifiche
description: L'applicazione WinSNMP deve registrarsi per ricevere trap e notifiche chiamando la funzione SnmpRegister con SNMPAPI \_ on. L'applicazione può annullare la registrazione e disabilitare i trap e le notifiche chiamando la funzione con SNMPAPI \_ off.
ms.assetid: 2bccba35-bf5c-4e5c-94e4-59980f2b9776
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51e3a2d9fed1f7c34dd8191550d1dbc68ed984e5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856633"
---
# <a name="managing-traps-and-notifications"></a>Gestione di trap e notifiche

L'applicazione WinSNMP deve registrarsi per ricevere trap e notifiche chiamando la funzione [**SnmpRegister**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister) con snmpapi \_ on. L'applicazione può annullare la registrazione e disabilitare i trap e le notifiche chiamando la funzione con SNMPAPI \_ off.

Quando l'applicazione chiama **SnmpRegister**, sono disponibili diverse opzioni. È possibile registrare o annullare la registrazione dell'applicazione per le seguenti trap e notifiche:

-   Un tipo di trap o notifica
-   Tutti i trap e le notifiche
-   Tutte le origini di trap e richieste di notifica
-   Trap e notifiche da tutte le entità di gestione
-   Trap e notifiche per ogni contesto

Per registrare e ricevere un trap o un tipo di notifica predefinito, è necessario che l'applicazione definisca un identificatore di oggetto (struttura [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) ) per ogni tipo predefinito. La struttura deve contenere una sequenza di corrispondenza dei modelli per il tipo di trap o di notifica. RFC 1907, "Information Management base per la versione 2 del Simple Network Management Protocol (SNMPv2)", definisce gli identificatori degli oggetti trap e Notification.

Per recuperare le notifiche e i dati trap in attesa per una sessione WinSNMP, è necessario che un'applicazione WinSNMP chiami la funzione [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) con l'handle di sessione restituito dalla funzione [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession) .

Per ulteriori informazioni, vedere [invio di messaggi SNMP](sending-snmp-messages.md) e [ricezione di messaggi SNMP](receiving-snmp-messages.md). Per ulteriori informazioni sull'allocazione e la deallocazione di risorse per trap e notifiche, vedere [allocazione di oggetti memoria WinSNMP](allocating-winsnmp-memory-objects.md).

 

 




