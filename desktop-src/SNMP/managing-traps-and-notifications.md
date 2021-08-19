---
title: Gestione di trap e notifiche
description: L'applicazione WinSNMP deve registrarsi per ricevere trap e notifiche chiamando la funzione SnmpRegister con SNMPAPI \_ ON. L'applicazione può annullare la registrazione e disabilitare trap e notifiche chiamando la funzione con SNMPAPI \_ OFF.
ms.assetid: 2bccba35-bf5c-4e5c-94e4-59980f2b9776
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 402a768aa28efb6f2fdc18994d749cfca2f2c412f748f853fb76fcd7fe3e41d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009379"
---
# <a name="managing-traps-and-notifications"></a>Gestione di trap e notifiche

L'applicazione WinSNMP deve registrarsi per ricevere trap e notifiche chiamando la [**funzione SnmpRegister**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister) con SNMPAPI \_ ON. L'applicazione può annullare la registrazione e disabilitare trap e notifiche chiamando la funzione con SNMPAPI \_ OFF.

Sono disponibili diverse opzioni quando l'applicazione chiama **SnmpRegister**. L'applicazione può registrare o annullare la registrazione per le trap e le notifiche seguenti:

-   Un tipo di trap o notifica
-   Tutte le trap e le notifiche
-   Tutte le origini delle richieste trap e di notifica
-   Trap e notifiche da tutte le entità di gestione
-   Trap e notifiche per ogni contesto

Per registrare e ricevere un tipo di trap o di notifica predefinito, l'applicazione deve definire un identificatore di oggetto [**(una struttura smiOID)**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) per ogni tipo predefinito. La struttura deve contenere una sequenza di criteri di ricerca per il tipo di trap o di notifica. RFC 1907, "Management Information Base for Version 2 of the Simple Network Management Protocol (SNMPv2)," definisce gli identificatori di oggetti trap e di notifica.

Per recuperare le notifiche e i dati trap in sospeso per una sessione WinSNMP, un'applicazione WinSNMP deve chiamare la [**funzione SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) con l'handle di sessione restituito dalla [**funzione SnmpCreateSession.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession)

Per altre informazioni, vedere [Invio di messaggi SNMP](sending-snmp-messages.md) e [Ricezione di messaggi SNMP](receiving-snmp-messages.md). Per altre informazioni sull'allocazione e la deallocazione delle risorse per trap e notifiche, vedere Allocazione di oggetti di [memoria WinSNMP](allocating-winsnmp-memory-objects.md).

 

 




