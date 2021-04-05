---
title: Funzionamento di SNMP
description: Il modo in cui un'applicazione console di gestione SNMP di terze parti restituisce informazioni dal servizio SNMP.
ms.assetid: 2edbf9ff-b9e3-4103-affc-a5c0f22b80a1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39d58943f0765b60f9c235094642d3fa759402db
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955329"
---
# <a name="how-snmp-works"></a><span data-ttu-id="bd3e1-103">Funzionamento di SNMP</span><span class="sxs-lookup"><span data-stu-id="bd3e1-103">How SNMP Works</span></span>

<span data-ttu-id="bd3e1-104">Nei passaggi seguenti viene illustrato il modo in cui un'applicazione console di gestione SNMP di terze parti restituisce informazioni dal servizio SNMP:</span><span class="sxs-lookup"><span data-stu-id="bd3e1-104">The following steps outline how a third-party SNMP management console application returns information from the SNMP service:</span></span>

1.  <span data-ttu-id="bd3e1-105">L'applicazione console di gestione SNMP formula un messaggio SNMP basato sull'input dell'utente.</span><span class="sxs-lookup"><span data-stu-id="bd3e1-105">The SNMP management console application formulates an SNMP message based on input from the user.</span></span> <span data-ttu-id="bd3e1-106">Il messaggio include un'unità dati di protocollo (PDU) e le informazioni di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="bd3e1-106">The message includes a protocol data unit (PDU) and authentication information.</span></span> <span data-ttu-id="bd3e1-107">L'applicazione console di gestione può utilizzare la libreria API di gestione SNMP Microsoft (MGMTAPI.DLL) o la libreria [API Microsoft WinSNMP](winsnmp-api.md) (WSNMP32.DLL) per eseguire questo passaggio.</span><span class="sxs-lookup"><span data-stu-id="bd3e1-107">The management console application can use the Microsoft SNMP Management API library (MGMTAPI.DLL) or the Microsoft [WinSNMP API](winsnmp-api.md) library (WSNMP32.DLL) to perform this step.</span></span>
2.  <span data-ttu-id="bd3e1-108">L'applicazione console di gestione SNMP Invia il messaggio SNMP al servizio SNMP utilizzando le librerie del servizio SNMP.</span><span class="sxs-lookup"><span data-stu-id="bd3e1-108">The SNMP management console application sends the SNMP message to the SNMP service, using the SNMP service libraries.</span></span>
3.  <span data-ttu-id="bd3e1-109">Il servizio SNMP riceve la richiesta.</span><span class="sxs-lookup"><span data-stu-id="bd3e1-109">The SNMP service receives the request.</span></span> <span data-ttu-id="bd3e1-110">Verifica le informazioni di autenticazione e l'indirizzo IP di origine.</span><span class="sxs-lookup"><span data-stu-id="bd3e1-110">It verifies the authentication information and the source IP address.</span></span>
4.  <span data-ttu-id="bd3e1-111">Il servizio SNMP seleziona l'agente di estensione appropriato e richiede che l'agente recuperi le informazioni richieste.</span><span class="sxs-lookup"><span data-stu-id="bd3e1-111">The SNMP service selects the appropriate extension agent and requests that the agent retrieve the requested information.</span></span>
5.  <span data-ttu-id="bd3e1-112">Il servizio SNMP Invia la risposta all'applicazione console di gestione SNMP.</span><span class="sxs-lookup"><span data-stu-id="bd3e1-112">The SNMP service sends the response to the SNMP management console application.</span></span>

 

 




