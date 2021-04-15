---
title: Invio di messaggi SNMP
description: Un'applicazione WinSNMP avvia una richiesta di trasmissione inviando un messaggio SNMP. I messaggi SNMP includono un'unità dati del protocollo SNMP. Per altre informazioni, vedere Working with Protocol Data units.
ms.assetid: a7439cd2-af13-4e2b-a0a6-5cc271a011e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 613ac7079f7dc206280b8d8077d2d5ea8db7151c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331348"
---
# <a name="sending-snmp-messages"></a>Invio di messaggi SNMP

Un'applicazione WinSNMP avvia una richiesta di trasmissione inviando un messaggio SNMP. I messaggi SNMP includono un'unità dati del protocollo SNMP. Per altre informazioni, vedere [Working with Protocol Data Units](working-with-protocol-data-units.md).

Un'applicazione WinSNMP deve chiamare la funzione [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) per richiedere che l'implementazione di Microsoft WinSNMP trasmetta la PDU, con gli altri elementi di messaggio richiesti definiti dalla specifica RFC. Oltre all'entità di destinazione, l'applicazione deve specificare l'entità di origine e un contesto per la richiesta. La funzione [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) viene eseguita in modo asincrono.

L'applicazione WinSNMP deve chiamare la funzione [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) per recuperare la risposta a una richiesta **SnmpSendMsg** .

L'implementazione verifica la validità della PDU e degli altri elementi del messaggio quando un'applicazione chiama [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg).

 

 




