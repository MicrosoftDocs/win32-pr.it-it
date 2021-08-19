---
title: Registrazione di un'applicazione agente SNMP
description: Oltre alle operazioni di gestione SNMP, l'API WinSNMP versione 2.0 supporta anche le operazioni dell'agente SNMP.
ms.assetid: 473560b5-4611-410e-aeae-764c9c76e765
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c3415e511639c7cbbc18455ed93be74e11414c1f442797c8b72f7456092757c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009129"
---
# <a name="registering-an-snmp-agent-application"></a>Registrazione di un'applicazione agente SNMP

Oltre alle operazioni di gestione SNMP, l'API WinSNMP versione 2.0 supporta anche le operazioni dell'agente SNMP.

Per registrare un'applicazione WinSNMP come agente SNMP, l'applicazione può chiamare la [**funzione SnmpListen.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmplisten) Questa funzione informa l'implementazione Microsoft WinSNMP che un'entità SNMP agirà nel ruolo di un agente SNMP. L'applicazione può anche chiamare **SnmpListen** per informare l'implementazione quando non fungerà più da agente.

Se un'applicazione chiama la [**funzione SnmpListen**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmplisten) e passa il valore SNMPAPI ON nel \_ parametro *lStatus,* si verificano le azioni seguenti:

1.  L'entità che funzionerà in un ruolo agente SNMP viene associata alla porta assegnata e "rimane in ascolto" per le richieste di messaggi SNMP in ingresso.
2.  L'agente usa la logica specifica dell'applicazione per elaborare ogni richiesta SNMP.
3.  L'agente forma le risposte appropriate a ogni richiesta.
4.  L'agente trasmette la risposta all'entità richiedente chiamando la [**funzione SnmpSendMsg.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) Quando l'agente chiama **SnmpSendMsg,** specifica l'indirizzo dell'agente nel parametro *srcEntity* e l'indirizzo dell'entità di gestione remota nel *parametro dstEntity.* Questi valori sono l'inverso dei valori ricevuti dall'entità agente in questi parametri quando ha chiamato la [**funzione SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) per recuperare una richiesta SNMP.

Per altre informazioni sulle applicazioni di gestione SNMP e sulle applicazioni agente, vedere [Informazioni su SNMP.](about-snmp.md)

 

 




