---
title: Registrazione di un'applicazione agente SNMP
description: Oltre alle operazioni di gestione SNMP, l'API WinSNMP versione 2,0 supporta anche le operazioni dell'agente SNMP.
ms.assetid: 473560b5-4611-410e-aeae-764c9c76e765
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40922469c52e33e4b5c2f408c1c107b6784529f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955645"
---
# <a name="registering-an-snmp-agent-application"></a>Registrazione di un'applicazione agente SNMP

Oltre alle operazioni di gestione SNMP, l'API WinSNMP versione 2,0 supporta anche le operazioni dell'agente SNMP.

Per registrare un'applicazione WinSNMP come agente SNMP, l'applicazione può chiamare la funzione [**SnmpListen**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmplisten) . Questa funzione informa l'implementazione di Microsoft WinSNMP che un'entità SNMP fungerà da ruolo di agente SNMP. L'applicazione può anche chiamare **SnmpListen** per informare l'implementazione quando non funzionerà più come un agente.

Se un'applicazione chiama la funzione [**SnmpListen**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmplisten) e passa il valore snmpapi \_ on nel parametro *lStatus* , si verificano le azioni seguenti:

1.  L'entità che funzionerà in un ruolo di agente SNMP viene associata alla relativa porta assegnata e "è in ascolto" per le richieste di messaggi SNMP in ingresso.
2.  L'agente utilizza la logica specifica dell'applicazione per elaborare ogni richiesta SNMP.
3.  L'agente crea risposte appropriate a ogni richiesta.
4.  L'agente trasmette la risposta all'entità richiedente chiamando la funzione [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) . Quando l'agente chiama **SnmpSendMsg**, specifica l'indirizzo dell'agente nel parametro *srcEntity* e l'indirizzo dell'entità gestione remota nel parametro *dstEntity* . Questi valori sono il contrario dei valori ricevuti dall'entità Agent in questi parametri quando ha chiamato la funzione [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) per recuperare una richiesta SNMP.

Per ulteriori informazioni sulle applicazioni di gestione SNMP e sulle applicazioni agente, vedere [informazioni su SNMP](about-snmp.md).

 

 




