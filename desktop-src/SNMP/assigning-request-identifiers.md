---
title: Assegnazione di identificatori di richiesta
description: Un'applicazione WinSNMP può chiamare la funzione SnmpCreatePdu o la funzione SnmpSetPduData per assegnare un identificatore di richiesta generato dall'applicazione a una PDU. L'applicazione deve passare il valore nel \_ parametro ID richiesta.
ms.assetid: 72559054-982f-4c2b-83d2-268f130f6ea2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 753f0ec1f5f3ca4347b6344aa111b91e735f06ba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707318"
---
# <a name="assigning-request-identifiers"></a>Assegnazione di identificatori di richiesta

Un'applicazione WinSNMP può chiamare la funzione [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) o la funzione [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) per assegnare un identificatore di richiesta generato dall'applicazione a una PDU. L'applicazione deve passare il valore nel parametro *\_ ID richiesta* .

Un'applicazione può richiedere che l'implementazione di Microsoft WinSNMP generi e assegni un identificatore di richiesta a una PDU passando zero nel *parametro \_ ID della richiesta* della funzione [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) . L'applicazione può recuperare l'identificatore della richiesta assegnato con una chiamata alla funzione [**SnmpGetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) .

Per assegnare un identificatore della richiesta uguale a un valore specifico, incluso zero, l'applicazione deve passare tale valore nel *parametro \_ ID richiesta* della funzione [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) .

Quando l'implementazione esegue i criteri di ritrasmissione dell'applicazione, include il campo **\_ ID richiesta** della PDU originale in ogni messaggio SNMP ritrasmesso. Per ulteriori informazioni, vedere [informazioni sulla ritrasmissione](about-retransmission.md) e [la gestione dei criteri di ritrasmissione](managing-the-retransmission-policy.md).

> [!Note]  
> Quando l'implementazione riceve trap da un'entità SNMPv1, assegna un valore diverso da zero al campo **\_ ID richiesta** della PDU. Questo valore può duplicare un identificatore di richiesta utilizzato dall'applicazione in un PDU della richiesta. Le applicazioni devono verificare la duplicazione.

 

 

 




