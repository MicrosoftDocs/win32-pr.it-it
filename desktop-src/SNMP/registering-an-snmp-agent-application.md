---
title: Registrazione di un'applicazione agente SNMP
description: Oltre alle operazioni di gestione SNMP, l'API WinSNMP versione 2,0 supporta anche le operazioni dell'agente SNMP.
ms.assetid: 473560b5-4611-410e-aeae-764c9c76e765
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40922469c52e33e4b5c2f408c1c107b6784529f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955645"
---
# <a name="registering-an-snmp-agent-application"></a><span data-ttu-id="13450-103">Registrazione di un'applicazione agente SNMP</span><span class="sxs-lookup"><span data-stu-id="13450-103">Registering an SNMP Agent Application</span></span>

<span data-ttu-id="13450-104">Oltre alle operazioni di gestione SNMP, l'API WinSNMP versione 2,0 supporta anche le operazioni dell'agente SNMP.</span><span class="sxs-lookup"><span data-stu-id="13450-104">In addition to SNMP manager operations, the WinSNMP API version 2.0 also supports SNMP agent operations.</span></span>

<span data-ttu-id="13450-105">Per registrare un'applicazione WinSNMP come agente SNMP, l'applicazione può chiamare la funzione [**SnmpListen**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmplisten) .</span><span class="sxs-lookup"><span data-stu-id="13450-105">To register a WinSNMP application as an SNMP agent, the application can call the [**SnmpListen**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmplisten) function.</span></span> <span data-ttu-id="13450-106">Questa funzione informa l'implementazione di Microsoft WinSNMP che un'entità SNMP fungerà da ruolo di agente SNMP.</span><span class="sxs-lookup"><span data-stu-id="13450-106">This function informs the Microsoft WinSNMP implementation that an SNMP entity will be acting in the role of an SNMP agent.</span></span> <span data-ttu-id="13450-107">L'applicazione può anche chiamare **SnmpListen** per informare l'implementazione quando non funzionerà più come un agente.</span><span class="sxs-lookup"><span data-stu-id="13450-107">The application can also call **SnmpListen** to inform the implementation when it will no longer be acting as an agent.</span></span>

<span data-ttu-id="13450-108">Se un'applicazione chiama la funzione [**SnmpListen**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmplisten) e passa il valore snmpapi \_ on nel parametro *lStatus* , si verificano le azioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="13450-108">If an application calls the [**SnmpListen**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmplisten) function and passes the value SNMPAPI\_ON in the *lStatus* parameter, the following actions occur:</span></span>

1.  <span data-ttu-id="13450-109">L'entità che funzionerà in un ruolo di agente SNMP viene associata alla relativa porta assegnata e "è in ascolto" per le richieste di messaggi SNMP in ingresso.</span><span class="sxs-lookup"><span data-stu-id="13450-109">The entity that will be functioning in an SNMP agent role binds to its assigned port, and "listens" for incoming SNMP message requests.</span></span>
2.  <span data-ttu-id="13450-110">L'agente utilizza la logica specifica dell'applicazione per elaborare ogni richiesta SNMP.</span><span class="sxs-lookup"><span data-stu-id="13450-110">The agent uses application-specific logic to process each SNMP request.</span></span>
3.  <span data-ttu-id="13450-111">L'agente crea risposte appropriate a ogni richiesta.</span><span class="sxs-lookup"><span data-stu-id="13450-111">The agent forms appropriate responses to each request.</span></span>
4.  <span data-ttu-id="13450-112">L'agente trasmette la risposta all'entità richiedente chiamando la funzione [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) .</span><span class="sxs-lookup"><span data-stu-id="13450-112">The agent transmits the response to the requesting entity by calling the [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) function.</span></span> <span data-ttu-id="13450-113">Quando l'agente chiama **SnmpSendMsg**, specifica l'indirizzo dell'agente nel parametro *srcEntity* e l'indirizzo dell'entità gestione remota nel parametro *dstEntity* .</span><span class="sxs-lookup"><span data-stu-id="13450-113">When the agent calls **SnmpSendMsg**, it specifies the address of the agent in the *srcEntity* parameter, and the address of the remote manager entity in the *dstEntity* parameter.</span></span> <span data-ttu-id="13450-114">Questi valori sono il contrario dei valori ricevuti dall'entità Agent in questi parametri quando ha chiamato la funzione [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) per recuperare una richiesta SNMP.</span><span class="sxs-lookup"><span data-stu-id="13450-114">(These values are the reverse of the values the agent entity received in these parameters when it called the [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) function to retrieve an SNMP request.)</span></span>

<span data-ttu-id="13450-115">Per ulteriori informazioni sulle applicazioni di gestione SNMP e sulle applicazioni agente, vedere [informazioni su SNMP](about-snmp.md).</span><span class="sxs-lookup"><span data-stu-id="13450-115">For more information about SNMP management applications and agent applications, see [About SNMP](about-snmp.md).</span></span>

 

 




