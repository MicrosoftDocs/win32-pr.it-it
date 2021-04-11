---
title: Errori di trasporto di rete
description: L'implementazione di Microsoft WinSNMP è in grado di rilevare un errore di trasporto di rete dopo la trasmissione di un messaggio SNMP.
ms.assetid: 2ff535b1-76cb-42aa-baeb-14c1a1bc41ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64cf6b7610fbfe8d19a375bd3e3146263b9e9f0b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872834"
---
# <a name="network-transport-errors"></a><span data-ttu-id="00a68-103">Errori di trasporto di rete</span><span class="sxs-lookup"><span data-stu-id="00a68-103">Network Transport Errors</span></span>

<span data-ttu-id="00a68-104">\[SNMP è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="00a68-104">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="00a68-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="00a68-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="00a68-106">Usare invece [gestione remota Windows](/windows/desktop/WinRM/portal), ovvero l'implementazione Microsoft di WS-Man.\]</span><span class="sxs-lookup"><span data-stu-id="00a68-106">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="00a68-107">L'implementazione di Microsoft WinSNMP è in grado di rilevare un errore di trasporto di rete dopo la trasmissione di un messaggio SNMP.</span><span class="sxs-lookup"><span data-stu-id="00a68-107">The Microsoft WinSNMP implementation can detect a network transport error after it transmits an SNMP message.</span></span> <span data-ttu-id="00a68-108">Quando si verifica questa situazione, l'implementazione invia una notifica di ricezione dati alla sessione WinSNMP che ha avviato la richiesta di comunicazione.</span><span class="sxs-lookup"><span data-stu-id="00a68-108">When this occurs, the implementation sends a data receipt notification to the WinSNMP session that initiated the communication request.</span></span> <span data-ttu-id="00a68-109">L'implementazione restituisce anche un \_ errore snmpapi alla chiamata successiva alla funzione [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) per la sessione.</span><span class="sxs-lookup"><span data-stu-id="00a68-109">The implementation also returns SNMPAPI\_FAILURE on the next call to the [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) function for the session.</span></span> <span data-ttu-id="00a68-110">La funzione **SnmpRecvMsg** ha esito negativo con un codice di errore esteso che indica un errore di livello del trasporto di rete.</span><span class="sxs-lookup"><span data-stu-id="00a68-110">The **SnmpRecvMsg** function fails with an extended error code that indicates a network transport layer error.</span></span>

<span data-ttu-id="00a68-111">Per un elenco di errori specifici del livello di trasporto, vedere le pagine di riferimento per le funzioni [**SnmpRegister**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister), [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg)e [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) .</span><span class="sxs-lookup"><span data-stu-id="00a68-111">For a list of specific transport layer errors, see the reference pages for the [**SnmpRegister**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister), [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg), and [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) functions.</span></span>

 

 