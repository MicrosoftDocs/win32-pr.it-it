---
title: PDU di risposta e richiesta corrispondenti
description: L'ordine in cui l'applicazione WinSNMP riceve risposte SNMP potrebbe non corrispondere all'ordine in cui l'applicazione invia le richieste di operazioni SNMP.
ms.assetid: cd09cc4b-2ef6-4d2f-8f0f-b83d8df8599a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a75a05f4a450ac1712d7cdd01a3c0e79dfddeb2d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955647"
---
# <a name="matching-response-and-request-pdus"></a>PDU di risposta e richiesta corrispondenti

L'ordine in cui l'applicazione WinSNMP riceve risposte SNMP potrebbe non corrispondere all'ordine in cui l'applicazione invia le richieste di operazioni SNMP. Per trovare la corrispondenza con la risposta con la richiesta, l'applicazione deve usare il campo identificatore richiesta ( **\_ ID richiesta**) della risposta.

Il **campo \_ ID richiesta** è un valore numerico univoco che identifica la PDU. Le applicazioni possono assegnare identificatori di richiesta chiamando la funzione [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) o la funzione [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) . Chiamare la funzione [**SnmpGetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) per recuperare l' **\_ ID richiesta** di PDU.

 

 




