---
title: Invio di messaggi SNMP
description: Un'applicazione WinSNMP avvia una richiesta di trasmissione inviando un messaggio SNMP. I messaggi SNMP includono un'unità dati del protocollo SNMP. Per altre informazioni, vedere Working with Protocol Data units.
ms.assetid: a7439cd2-af13-4e2b-a0a6-5cc271a011e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 613ac7079f7dc206280b8d8077d2d5ea8db7151c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331348"
---
# <a name="sending-snmp-messages"></a><span data-ttu-id="ca352-105">Invio di messaggi SNMP</span><span class="sxs-lookup"><span data-stu-id="ca352-105">Sending SNMP Messages</span></span>

<span data-ttu-id="ca352-106">Un'applicazione WinSNMP avvia una richiesta di trasmissione inviando un messaggio SNMP.</span><span class="sxs-lookup"><span data-stu-id="ca352-106">A WinSNMP application initiates a transmission request by sending an SNMP message.</span></span> <span data-ttu-id="ca352-107">I messaggi SNMP includono un'unità dati del protocollo SNMP.</span><span class="sxs-lookup"><span data-stu-id="ca352-107">SNMP messages include an SNMP protocol data unit.</span></span> <span data-ttu-id="ca352-108">Per altre informazioni, vedere [Working with Protocol Data Units](working-with-protocol-data-units.md).</span><span class="sxs-lookup"><span data-stu-id="ca352-108">For more information, see [Working with Protocol Data Units](working-with-protocol-data-units.md).</span></span>

<span data-ttu-id="ca352-109">Un'applicazione WinSNMP deve chiamare la funzione [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) per richiedere che l'implementazione di Microsoft WinSNMP trasmetta la PDU, con gli altri elementi di messaggio richiesti definiti dalla specifica RFC.</span><span class="sxs-lookup"><span data-stu-id="ca352-109">A WinSNMP application must call the [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) function to request that the Microsoft WinSNMP implementation transmit the PDU, with the other required message elements defined by the relevant RFC.</span></span> <span data-ttu-id="ca352-110">Oltre all'entità di destinazione, l'applicazione deve specificare l'entità di origine e un contesto per la richiesta.</span><span class="sxs-lookup"><span data-stu-id="ca352-110">In addition to the destination entity, the application must specify the source entity and a context for the request.</span></span> <span data-ttu-id="ca352-111">La funzione [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) viene eseguita in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="ca352-111">The [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) function executes asynchronously.</span></span>

<span data-ttu-id="ca352-112">L'applicazione WinSNMP deve chiamare la funzione [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) per recuperare la risposta a una richiesta **SnmpSendMsg** .</span><span class="sxs-lookup"><span data-stu-id="ca352-112">The WinSNMP application must call the [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) function to retrieve the response to an **SnmpSendMsg** request.</span></span>

<span data-ttu-id="ca352-113">L'implementazione verifica la validità della PDU e degli altri elementi del messaggio quando un'applicazione chiama [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg).</span><span class="sxs-lookup"><span data-stu-id="ca352-113">The implementation verifies the validity of the PDU and the other message elements when an application calls [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg).</span></span>

 

 




