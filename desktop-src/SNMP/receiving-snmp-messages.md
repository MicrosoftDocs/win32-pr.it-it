---
title: Ricezione di messaggi SNMP
description: L'applicazione WinSNMP deve chiamare la funzione SnmpRecvMsg per recuperare la risposta a una richiesta SnmpSendMsg.
ms.assetid: 323a5565-a8a5-4efd-aa4e-e4623b581d09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 529420deaf637cec8598a8e8becc87ab514b40b4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713063"
---
# <a name="receiving-snmp-messages"></a>Ricezione di messaggi SNMP

L'applicazione WinSNMP deve chiamare la funzione [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) per recuperare la risposta a una richiesta [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) .

La funzione [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession) passa un handle della finestra dell'applicazione e un identificatore del messaggio di notifica all'implementazione di Microsoft WinSNMP. Quando la finestra dell'applicazione riceve questo messaggio, segnala all'applicazione di chiamare la funzione [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) usando l'handle di sessione restituito da [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession).

La funzione [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) restituisce due handle di entità, un handle di contesto e l'handle a una PDU. È consigliabile che l'applicazione WinSNMP liberi queste risorse usando le funzioni [**SnmpFreeEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity), [**SnmpFreeContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext)e [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu) .

Per ulteriori informazioni sulla gestione del tempo che intercorre tra una chiamata alla funzione [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) e la ricezione della risposta corrispondente, vedere [informazioni sulla ritrasmissione](about-retransmission.md). Per altre informazioni sull'uso del campo **Richiedi \_ ID** PDU per trovare la corrispondenza con la PDU della risposta con la relativa richiesta PDU, vedere [corrispondenza della risposta e della richiesta PDU](matching-response-and-request-pdus.md).

 

 




