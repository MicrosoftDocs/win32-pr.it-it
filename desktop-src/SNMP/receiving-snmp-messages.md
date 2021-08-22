---
title: Ricezione di messaggi SNMP
description: L'applicazione WinSNMP deve chiamare la funzione SnmpRecvMsg per recuperare la risposta a una richiesta SnmpSendMsg.
ms.assetid: 323a5565-a8a5-4efd-aa4e-e4623b581d09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bd341e71aa6b8387b82f6576599fb6cb7d3545f34e01f80267f19a73edb7cba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009179"
---
# <a name="receiving-snmp-messages"></a>Ricezione di messaggi SNMP

L'applicazione WinSNMP deve chiamare la [**funzione SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) per recuperare la risposta a una [**richiesta SnmpSendMsg.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg)

La [**funzione SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession) passa un handle della finestra dell'applicazione e un identificatore del messaggio di notifica all'implementazione Microsoft WinSNMP. Quando la finestra dell'applicazione riceve questo messaggio, segnala all'applicazione di chiamare la [**funzione SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) usando l'handle di sessione [**restituito da SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession).

La [**funzione SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) restituisce due handle di entità, un handle di contesto e l'handle a una PDU. È consigliabile che l'applicazione WinSNMP liberi queste risorse usando le [**funzioni SnmpFreeEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity), [**SnmpFreeContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext)e [**SnmpFreePdu.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu)

Per altre informazioni sulla gestione del tempo tra una chiamata alla [**funzione SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) e la ricezione della risposta corrispondente, vedere [Informazioni sulla ritrasmissione](about-retransmission.md). Per altre informazioni sull'uso del campo PDU **\_ id** richiesta per la corrispondenza di una PDU di risposta con la PDU della richiesta, vedere Corrispondenza tra PDU di risposta e [richiesta](matching-response-and-request-pdus.md).

 

 




