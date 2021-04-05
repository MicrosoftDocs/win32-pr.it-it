---
title: Livelli di supporto SNMP
description: L'implementazione di Microsoft WinSNMP fornisce supporto per le comunicazioni SNMP di livello 2.
ms.assetid: 9874ad9b-4eb9-4d63-816b-fe444c5b4d8a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92b48c930266073f10e5cb8019a7462317bd798c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104116752"
---
# <a name="levels-of-snmp-support"></a><span data-ttu-id="7deef-103">Livelli di supporto SNMP</span><span class="sxs-lookup"><span data-stu-id="7deef-103">Levels of SNMP Support</span></span>

<span data-ttu-id="7deef-104">L'implementazione di Microsoft WinSNMP fornisce supporto per le comunicazioni SNMP di livello 2.</span><span class="sxs-lookup"><span data-stu-id="7deef-104">The Microsoft WinSNMP implementation provides level 2 SNMP communications support.</span></span> <span data-ttu-id="7deef-105">Il livello 2 supporta il protocollo SNMPv2 standard IETF (Internet Engineering Task Force), come definito nella RFC 1902-1908.</span><span class="sxs-lookup"><span data-stu-id="7deef-105">Level 2 supports the Internet Engineering Task Force (IETF) standard SNMPv2 protocol as defined in RFCs 1902-1908.</span></span> <span data-ttu-id="7deef-106">Supporta inoltre il wrapper di messaggi basato sulla community come definito nella specifica RFC 1901 (SNMPv2C).</span><span class="sxs-lookup"><span data-stu-id="7deef-106">It also supports the community-based message wrapper as defined in RFC 1901 (SNMPv2C).</span></span>

<span data-ttu-id="7deef-107">Il supporto per le comunicazioni di livello 2 include i servizi di codifica e decodifica dei messaggi, in precedenza denominati supporto delle comunicazioni di livello 0 in WinSNMP versione 1.1 a.</span><span class="sxs-lookup"><span data-stu-id="7deef-107">Level 2 communications support includes message encoding and decoding services, previously called Level 0 communications support in WinSNMP version 1.1a.</span></span> <span data-ttu-id="7deef-108">Il livello 2 supporta inoltre tutte le operazioni del protocollo SNMPv1, in precedenza chiamate supporto per le comunicazioni di livello 1 in WinSNMP versione 1.1 a.</span><span class="sxs-lookup"><span data-stu-id="7deef-108">Level 2 also supports all SNMPv1 protocol operations, previously called Level 1 communications support in WinSNMP version 1.1a.</span></span>

<span data-ttu-id="7deef-109">L'implementazione restituisce il livello massimo di comunicazioni SNMP supportato in risposta a una chiamata da parte dell'applicazione WinSNMP alla funzione [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) .</span><span class="sxs-lookup"><span data-stu-id="7deef-109">The implementation returns the maximum level of SNMP communications it supports in response to a call by the WinSNMP application to the [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) function.</span></span>

<span data-ttu-id="7deef-110">Se l'applicazione WinSNMP usa l'implementazione solo per la codifica e la decodifica dei messaggi SNMP, l'applicazione deve eseguire le trasformazioni necessarie che l'implementazione avrebbe eseguito.</span><span class="sxs-lookup"><span data-stu-id="7deef-110">If the WinSNMP application uses the implementation for SNMP message encoding and decoding only, the application must perform required transformations that the implementation would have performed.</span></span> <span data-ttu-id="7deef-111">Ciò include la conversione dei trap SNMPv1 restituiti da una chiamata alla funzione [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) a trap SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="7deef-111">This includes translating SNMPv1 traps returned by a call to the [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) function, to SNMPv2C traps.</span></span> <span data-ttu-id="7deef-112">Include anche la traduzione dei tipi PDU definiti da SNMPv1 nel tipo PDU pertinente definito da SNMPv2C, in base allo standard RFC 1908.</span><span class="sxs-lookup"><span data-stu-id="7deef-112">It also includes translating PDU types defined by SNMPv1 to the relevant PDU type defined by SNMPv2C, in accordance with RFC 1908.</span></span>

 

 




