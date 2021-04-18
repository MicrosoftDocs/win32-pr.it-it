---
title: Conversione di richieste di messaggi
description: Questo argomento descrive il processo di conversione delle richieste SNMPv1 in richieste SNMPv2.
ms.assetid: 7671ae36-99b1-47b1-930a-f376021d56a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa2a67ecb78b16f818ea50158faf827e19d4eba5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515580"
---
# <a name="translating-message-requests"></a>Conversione di richieste di messaggi

Questo argomento descrive il processo di conversione delle richieste SNMPv1 in richieste SNMPv2.

Se un'applicazione WinSNMP richiede la funzionalità disponibile in SNMP versione 2C Framework (SNMPv2C), ma l'entità di destinazione supporta solo il Framework SNMP versione 1 (SNMPv1), l'implementazione di Microsoft WinSNMP tenta di convertire la richiesta nel formato SNMPv1. A tale scopo, l'implementazione utilizza le procedure definite in RFC 1908, "coesistenza tra la versione 1 e la versione 2 del Internet-Standard Framework di gestione della rete". Se la conversione non è possibile, la funzione [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) ha esito negativo e il codice di errore esteso snmpapi \_ operazione \_ non è valida.

 

 




