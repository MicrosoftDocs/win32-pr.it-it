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
# <a name="matching-response-and-request-pdus"></a><span data-ttu-id="349d5-103">PDU di risposta e richiesta corrispondenti</span><span class="sxs-lookup"><span data-stu-id="349d5-103">Matching Response and Request PDUs</span></span>

<span data-ttu-id="349d5-104">L'ordine in cui l'applicazione WinSNMP riceve risposte SNMP potrebbe non corrispondere all'ordine in cui l'applicazione invia le richieste di operazioni SNMP.</span><span class="sxs-lookup"><span data-stu-id="349d5-104">The order in which the WinSNMP application receives SNMP responses may not match the order in which the application submits SNMP operation requests.</span></span> <span data-ttu-id="349d5-105">Per trovare la corrispondenza con la risposta con la richiesta, l'applicazione deve usare il campo identificatore richiesta ( **\_ ID richiesta**) della risposta.</span><span class="sxs-lookup"><span data-stu-id="349d5-105">To match the response with the request, the application must use the request identifier field (the **request\_id**) of the response.</span></span>

<span data-ttu-id="349d5-106">Il **campo \_ ID richiesta** è un valore numerico univoco che identifica la PDU.</span><span class="sxs-lookup"><span data-stu-id="349d5-106">The **request\_id** field is a unique numeric value that identifies the PDU.</span></span> <span data-ttu-id="349d5-107">Le applicazioni possono assegnare identificatori di richiesta chiamando la funzione [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) o la funzione [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) .</span><span class="sxs-lookup"><span data-stu-id="349d5-107">Applications can assign request identifiers by calling the [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) function or the [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) function.</span></span> <span data-ttu-id="349d5-108">Chiamare la funzione [**SnmpGetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) per recuperare l' **\_ ID richiesta** di PDU.</span><span class="sxs-lookup"><span data-stu-id="349d5-108">Call the [**SnmpGetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) function to retrieve a PDU's **request\_id**.</span></span>

 

 




