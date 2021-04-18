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
# <a name="translating-message-requests"></a><span data-ttu-id="5e81a-103">Conversione di richieste di messaggi</span><span class="sxs-lookup"><span data-stu-id="5e81a-103">Translating Message Requests</span></span>

<span data-ttu-id="5e81a-104">Questo argomento descrive il processo di conversione delle richieste SNMPv1 in richieste SNMPv2.</span><span class="sxs-lookup"><span data-stu-id="5e81a-104">This topic describes the process of translating SNMPv1 requests into SNMPv2 requests.</span></span>

<span data-ttu-id="5e81a-105">Se un'applicazione WinSNMP richiede la funzionalità disponibile in SNMP versione 2C Framework (SNMPv2C), ma l'entità di destinazione supporta solo il Framework SNMP versione 1 (SNMPv1), l'implementazione di Microsoft WinSNMP tenta di convertire la richiesta nel formato SNMPv1.</span><span class="sxs-lookup"><span data-stu-id="5e81a-105">If a WinSNMP application requests functionality that is available under the SNMP version 2C framework (SNMPv2C), but the target entity supports only the SNMP version 1 framework (SNMPv1), the Microsoft WinSNMP implementation attempts to translate the request to the SNMPv1 format.</span></span> <span data-ttu-id="5e81a-106">A tale scopo, l'implementazione utilizza le procedure definite in RFC 1908, "coesistenza tra la versione 1 e la versione 2 del Internet-Standard Framework di gestione della rete".</span><span class="sxs-lookup"><span data-stu-id="5e81a-106">To do this, the implementation uses the procedures defined in RFC 1908, "Coexistence Between Version 1 and Version 2 of the Internet-Standard Network Management Framework."</span></span> <span data-ttu-id="5e81a-107">Se la conversione non è possibile, la funzione [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) ha esito negativo e il codice di errore esteso snmpapi \_ operazione \_ non è valida.</span><span class="sxs-lookup"><span data-stu-id="5e81a-107">If translation is not possible, the [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) function fails with the extended error code SNMPAPI\_OPERATION\_INVALID.</span></span>

 

 




