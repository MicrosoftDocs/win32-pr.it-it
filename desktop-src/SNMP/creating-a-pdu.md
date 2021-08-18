---
title: Creazione di una PDU
description: Per creare e inizializzare una PDU, un'applicazione WinSNMP chiama la funzione SnmpCreatePdu.
ms.assetid: 7f02a2c6-19bc-456f-bf04-3297d19000f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ef0598c08c27d988825b3f0db3d8172362e9e6daf2ed4dbad049e2808b01034
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009599"
---
# <a name="creating-a-pdu"></a>Creazione di una PDU

Per creare e inizializzare una PDU, un'applicazione WinSNMP chiama la [**funzione SnmpCreatePdu.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) L'applicazione deve chiamare **SnmpCreatePdu** prima di chiamare la [**funzione SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) per richiedere che l'implementazione Microsoft WinSNMP trasmia una PDU. L'applicazione deve chiamare [**anche SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) prima di chiamare la [**funzione SnmpEncodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg) per richiedere la codifica di un messaggio SNMP.

L'applicazione deve chiamare la [**funzione SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu) per rilasciare le risorse allocate dalla funzione [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) per le nuove PDU.

 

 




