---
title: Creazione di una PDU
description: Per creare e inizializzare una PDU, un'applicazione WinSNMP chiama la funzione SnmpCreatePdu.
ms.assetid: 7f02a2c6-19bc-456f-bf04-3297d19000f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1aba7a4ca42e2a5d63169d2521410773ca018c4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856186"
---
# <a name="creating-a-pdu"></a>Creazione di una PDU

Per creare e inizializzare una PDU, un'applicazione WinSNMP chiama la funzione [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) . L'applicazione deve chiamare **SnmpCreatePdu** prima di chiamare la funzione [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) per richiedere che l'implementazione di Microsoft WinSNMP trasmetta una PDU. L'applicazione deve inoltre chiamare [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) prima di chiamare la funzione [**SnmpEncodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg) per richiedere la codifica di un messaggio SNMP.

L'applicazione deve chiamare la funzione [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu) per rilasciare le risorse allocate dalla funzione [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) per la nuova PDU.

 

 




