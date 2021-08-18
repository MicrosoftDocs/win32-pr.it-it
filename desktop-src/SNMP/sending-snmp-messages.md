---
title: Invio di messaggi SNMP
description: Un'applicazione WinSNMP avvia una richiesta di trasmissione inviando un messaggio SNMP. I messaggi SNMP includono un'unità dati del protocollo SNMP. Per altre informazioni, vedere Uso delle unità dati del protocollo.
ms.assetid: a7439cd2-af13-4e2b-a0a6-5cc271a011e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4461c5d554444b2a7a5384a0ca79825b27ebe3c3bc489b6152c81ae71d172f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009069"
---
# <a name="sending-snmp-messages"></a>Invio di messaggi SNMP

Un'applicazione WinSNMP avvia una richiesta di trasmissione inviando un messaggio SNMP. I messaggi SNMP includono un'unità dati del protocollo SNMP. Per altre informazioni, vedere [Uso delle unità dati del protocollo](working-with-protocol-data-units.md).

Un'applicazione WinSNMP deve chiamare la [**funzione SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) per richiedere che l'implementazione Microsoft WinSNMP trasmini la PDU, con gli altri elementi di messaggio necessari definiti dalla RFC pertinente. Oltre all'entità di destinazione, l'applicazione deve specificare l'entità di origine e un contesto per la richiesta. La [**funzione SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) viene eseguita in modo asincrono.

L'applicazione WinSNMP deve chiamare la [**funzione SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) per recuperare la risposta a una **richiesta SnmpSendMsg.**

L'implementazione verifica la validità della PDU e degli altri elementi del messaggio quando un'applicazione chiama [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg).

 

 




