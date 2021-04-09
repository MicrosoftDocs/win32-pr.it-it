---
title: Modello WinSNMP
description: Il modello conforme a WinSNMP include i componenti di base seguenti.
ms.assetid: 491df017-0b91-4fcf-97c3-4e296c3324bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff7ae4fa1c1ee56fc534e4aa4c9bffefb8d7f4d2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044370"
---
# <a name="the-winsnmp-model"></a><span data-ttu-id="49e3f-103">Modello WinSNMP</span><span class="sxs-lookup"><span data-stu-id="49e3f-103">The WinSNMP Model</span></span>

<span data-ttu-id="49e3f-104">Il modello conforme a WinSNMP include i componenti di base seguenti:</span><span class="sxs-lookup"><span data-stu-id="49e3f-104">The WinSNMP-compliant model includes the following basic components:</span></span>

-   <span data-ttu-id="49e3f-105">Un'applicazione di gestione di rete SNMP abilitata per WinSNMP, ovvero un' *applicazione* conforme a WinSNMP</span><span class="sxs-lookup"><span data-stu-id="49e3f-105">A WinSNMP-enabled SNMP network management application, that is, a WinSNMP-compliant *application*</span></span>
-   <span data-ttu-id="49e3f-106">Livello della funzione WinSNMP</span><span class="sxs-lookup"><span data-stu-id="49e3f-106">The WinSNMP function layer</span></span>
-   <span data-ttu-id="49e3f-107">Un provider di servizi SNMP abilitato per WinSNMP, ovvero un' *implementazione* conforme a WinSNMP</span><span class="sxs-lookup"><span data-stu-id="49e3f-107">A WinSNMP-enabled SNMP service provider, that is, a WinSNMP-compliant *implementation*</span></span>

<span data-ttu-id="49e3f-108">Le applicazioni di gestione della rete che devono fornire messaggi SNMP funzionano in modo efficiente in un ambiente basato su eventi.</span><span class="sxs-lookup"><span data-stu-id="49e3f-108">Network management applications that must convey SNMP messages operate efficiently in an event-driven environment.</span></span> <span data-ttu-id="49e3f-109">Questo perché SNMP è un protocollo basato su datagramma o senza connessione tra entità remote che non stabiliscono circuiti virtuali.</span><span class="sxs-lookup"><span data-stu-id="49e3f-109">This is because SNMP is a datagram-based or connectionless protocol between remote entities that do not establish virtual circuits.</span></span>

<span data-ttu-id="49e3f-110">Poiché le applicazioni di Microsoft Windows sono anche basate sugli eventi, WinSNMP utilizza un modello di programmazione in cui la ricezione e l'elaborazione di applicazioni di gestione degli *eventi di messaggio* asincrono.</span><span class="sxs-lookup"><span data-stu-id="49e3f-110">Since Microsoft Windows applications are also event-driven, WinSNMP uses a programming model in which the receipt and processing of asynchronous *message-events* drive management applications.</span></span> <span data-ttu-id="49e3f-111">Un evento di messaggio asincrono può essere una richiesta di operazione SNMP da parte di un'applicazione di gestione o la risposta a una richiesta da parte di un'applicazione di Agent.</span><span class="sxs-lookup"><span data-stu-id="49e3f-111">An asynchronous message-event can be an SNMP operation request by a manager application, or the response to a request by an agent application.</span></span>

<span data-ttu-id="49e3f-112">SNMP invia richieste e risposte come messaggi SNMP.</span><span class="sxs-lookup"><span data-stu-id="49e3f-112">SNMP sends requests and responses as SNMP messages.</span></span> <span data-ttu-id="49e3f-113">Un messaggio SNMP è un'unità dati del protocollo SNMP, oltre a elementi di intestazione del messaggio aggiuntivi definiti dalla relativa RFC.</span><span class="sxs-lookup"><span data-stu-id="49e3f-113">An SNMP message is an SNMP protocol data unit (PDU) plus additional message header elements defined by the relevant RFC.</span></span> <span data-ttu-id="49e3f-114">Per ulteriori informazioni, vedere [informazioni sui messaggi SNMP](about-snmp-messages.md), [utilizzo di elenchi di associazioni variabili](working-with-variable-binding-lists.md) e [utilizzo delle unità dati del protocollo](working-with-protocol-data-units.md).</span><span class="sxs-lookup"><span data-stu-id="49e3f-114">For more information, see [About SNMP Messages](about-snmp-messages.md), [Working with Variable Binding Lists](working-with-variable-binding-lists.md) and [Working with Protocol Data Units](working-with-protocol-data-units.md).</span></span>

 

 




