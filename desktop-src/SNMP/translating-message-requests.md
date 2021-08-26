---
title: Traduzione delle richieste di messaggi
description: Questo argomento descrive il processo di conversione delle richieste SNMPv1 in richieste SNMPv2.
ms.assetid: 7671ae36-99b1-47b1-930a-f376021d56a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1775d59a8de0bd0473570f3028018a1a25cad2ebd4ee004025ad11a38e37e69c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119885891"
---
# <a name="translating-message-requests"></a>Traduzione delle richieste di messaggi

Questo argomento descrive il processo di conversione delle richieste SNMPv1 in richieste SNMPv2.

Se un'applicazione WinSNMP richiede funzionalità disponibili nel framework SNMP versione 2C (SNMPv2C), ma l'entità di destinazione supporta solo il framework SNMP versione 1 (SNMPv1), l'implementazione Microsoft WinSNMP tenta di convertire la richiesta nel formato SNMPv1. A tale scopo, l'implementazione usa le procedure definite in RFC 1908, "Coesistenza tra la versione 1 e la versione 2 di Internet-Standard Network Management Framework". Se la conversione non è possibile, la [**funzione SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) ha esito negativo con il codice di errore esteso SNMPAPI \_ OPERATION \_ INVALID.

 

 




