---
title: PDU di risposta e richiesta corrispondenti
description: L'ordine in cui l'applicazione WinSNMP riceve le risposte SNMP potrebbe non corrispondere all'ordine in cui l'applicazione invia richieste di operazioni SNMP.
ms.assetid: cd09cc4b-2ef6-4d2f-8f0f-b83d8df8599a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30e669b3e15652b8df68cb8fc27437106e644909e99bf0b7aee21a128194cf7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009319"
---
# <a name="matching-response-and-request-pdus"></a>PDU di risposta e richiesta corrispondenti

L'ordine in cui l'applicazione WinSNMP riceve le risposte SNMP potrebbe non corrispondere all'ordine in cui l'applicazione invia richieste di operazioni SNMP. Per associare la risposta alla richiesta, l'applicazione deve usare il campo dell'identificatore della richiesta **\_ (ID** richiesta ) della risposta.

Il **campo \_ id** richiesta è un valore numerico univoco che identifica la PDU. Le applicazioni possono assegnare identificatori di richiesta chiamando [**la funzione SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) o [**la funzione SnmpSetPduData.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) Chiamare la [**funzione SnmpGetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) per recuperare l'ID richiesta **di una \_** PDU.

 

 




