---
title: Ricezione di messaggi SNMP
description: L'applicazione WinSNMP deve chiamare la funzione SnmpRecvMsg per recuperare la risposta a una richiesta SnmpSendMsg.
ms.assetid: 323a5565-a8a5-4efd-aa4e-e4623b581d09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 529420deaf637cec8598a8e8becc87ab514b40b4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713063"
---
# <a name="receiving-snmp-messages"></a><span data-ttu-id="e9d6e-103">Ricezione di messaggi SNMP</span><span class="sxs-lookup"><span data-stu-id="e9d6e-103">Receiving SNMP Messages</span></span>

<span data-ttu-id="e9d6e-104">L'applicazione WinSNMP deve chiamare la funzione [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) per recuperare la risposta a una richiesta [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) .</span><span class="sxs-lookup"><span data-stu-id="e9d6e-104">The WinSNMP application must call the [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) function to retrieve the response to an [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) request.</span></span>

<span data-ttu-id="e9d6e-105">La funzione [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession) passa un handle della finestra dell'applicazione e un identificatore del messaggio di notifica all'implementazione di Microsoft WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="e9d6e-105">The [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession) function passes an application window handle and a notification message identifier to the Microsoft WinSNMP implementation.</span></span> <span data-ttu-id="e9d6e-106">Quando la finestra dell'applicazione riceve questo messaggio, segnala all'applicazione di chiamare la funzione [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) usando l'handle di sessione restituito da [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession).</span><span class="sxs-lookup"><span data-stu-id="e9d6e-106">When the application window receives this message, it signals the application to call the [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) function using the session handle returned by [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession).</span></span>

<span data-ttu-id="e9d6e-107">La funzione [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) restituisce due handle di entità, un handle di contesto e l'handle a una PDU.</span><span class="sxs-lookup"><span data-stu-id="e9d6e-107">The [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) function returns two entity handles, a context handle, and the handle to a PDU.</span></span> <span data-ttu-id="e9d6e-108">È consigliabile che l'applicazione WinSNMP liberi queste risorse usando le funzioni [**SnmpFreeEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity), [**SnmpFreeContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext)e [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu) .</span><span class="sxs-lookup"><span data-stu-id="e9d6e-108">It is recommended that the WinSNMP application free these resources using the [**SnmpFreeEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity), [**SnmpFreeContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext), and [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu) functions.</span></span>

<span data-ttu-id="e9d6e-109">Per ulteriori informazioni sulla gestione del tempo che intercorre tra una chiamata alla funzione [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) e la ricezione della risposta corrispondente, vedere [informazioni sulla ritrasmissione](about-retransmission.md).</span><span class="sxs-lookup"><span data-stu-id="e9d6e-109">For additional information about managing the time between a call to the [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) function and the receipt of the corresponding response, see [About Retransmission](about-retransmission.md).</span></span> <span data-ttu-id="e9d6e-110">Per altre informazioni sull'uso del campo **Richiedi \_ ID** PDU per trovare la corrispondenza con la PDU della risposta con la relativa richiesta PDU, vedere [corrispondenza della risposta e della richiesta PDU](matching-response-and-request-pdus.md).</span><span class="sxs-lookup"><span data-stu-id="e9d6e-110">For additional information about using the **request\_id** PDU field to match a response PDU with its request PDU, see [Matching Response and Request PDUs](matching-response-and-request-pdus.md).</span></span>

 

 




