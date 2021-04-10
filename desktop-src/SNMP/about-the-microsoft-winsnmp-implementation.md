---
title: Informazioni sull'implementazione di Microsoft WinSNMP
description: L'implementazione di Microsoft WinSNMP è conforme alla versione 2,0 di WinSNMP.
ms.assetid: 99e11d30-d159-4d9b-94d0-baa6e49d82cf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cbf142ba85458374105af5b80ca5af30a6c5082
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955063"
---
# <a name="about-the-microsoft-winsnmp-implementation"></a><span data-ttu-id="22126-103">Informazioni sull'implementazione di Microsoft WinSNMP</span><span class="sxs-lookup"><span data-stu-id="22126-103">About the Microsoft WinSNMP Implementation</span></span>

<span data-ttu-id="22126-104">L'implementazione di Microsoft WinSNMP è conforme alla versione 2,0 di WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="22126-104">The Microsoft WinSNMP implementation complies with WinSNMP version 2.0.</span></span> <span data-ttu-id="22126-105">Supporta tutte le funzioni e le operazioni definite in WinSNMP versione 1.1 a specifica e WinSNMP versione 2,0 addendum.</span><span class="sxs-lookup"><span data-stu-id="22126-105">It supports all the functions and operations defined in both the WinSNMP version 1.1a specification and the WinSNMP version 2.0 Addendum.</span></span> <span data-ttu-id="22126-106">L'implementazione fornisce i servizi seguenti per le applicazioni WinSNMP:</span><span class="sxs-lookup"><span data-stu-id="22126-106">The implementation provides the following services for WinSNMP applications:</span></span>

-   <span data-ttu-id="22126-107">Gestisce le comunicazioni da e verso le entità di gestione.</span><span class="sxs-lookup"><span data-stu-id="22126-107">Manages communications to and from management entities.</span></span> <span data-ttu-id="22126-108">L'entità può risiedere nel computer locale o essere connessa tramite una rete locale o wide-area o Internet.</span><span class="sxs-lookup"><span data-stu-id="22126-108">The entity can reside on the local computer or be connected through a local or wide-area network, or the Internet.</span></span> <span data-ttu-id="22126-109">Per ulteriori informazioni, vedere [livelli di supporto SNMP](levels-of-snmp-support.md).</span><span class="sxs-lookup"><span data-stu-id="22126-109">For more information, see [Levels of SNMP Support](levels-of-snmp-support.md).</span></span>
-   <span data-ttu-id="22126-110">Nasconde i dettagli del protocollo SNMP, Abstract Syntax Notation One (ASN. 1) e le regole di codifica di base (BER) per la descrizione della sintassi di trasferimento.</span><span class="sxs-lookup"><span data-stu-id="22126-110">Hides the details of SNMP protocol, Abstract Syntax Notation One (ASN.1), and the Basic Encoding Rules (BER) for describing transfer syntax.</span></span>
-   <span data-ttu-id="22126-111">Verifica la correttezza di PDU e rifiuta PDU non validi.</span><span class="sxs-lookup"><span data-stu-id="22126-111">Verifies the correctness of PDUs and rejects invalid PDUs.</span></span> <span data-ttu-id="22126-112">Per altre informazioni, vedere [Working with Protocol Data Units](working-with-protocol-data-units.md).</span><span class="sxs-lookup"><span data-stu-id="22126-112">For more information, see [Working with Protocol Data Units](working-with-protocol-data-units.md).</span></span>
-   <span data-ttu-id="22126-113">Trasforma i tipi SNMPv2C PDU quando necessario in conformità con le RFC pertinenti.</span><span class="sxs-lookup"><span data-stu-id="22126-113">Transforms SNMPv2C PDU types when necessary in accordance with the relevant RFCs.</span></span>
-   <span data-ttu-id="22126-114">Converte SNMPv1 TRAP da un agente SNMPv1 a trap SNMPv2C in conformità con RFC 1908, "coesistenza tra la versione 1 e la versione 2 del Framework di gestione della rete Internet standard".</span><span class="sxs-lookup"><span data-stu-id="22126-114">Converts SNMPv1 traps from an SNMPv1 agent to SNMPv2C traps in accordance with RFC 1908, "Coexistence between Version 1 and Version 2 of the Internet-standard Network Management Framework."</span></span> <span data-ttu-id="22126-115">Per ulteriori informazioni, vedere la pagina relativa [alla conversione di trap da SNMPv1 a SNMPv2c](translating-traps-from-snmpv1-to-snmpv2c.md).</span><span class="sxs-lookup"><span data-stu-id="22126-115">For more information, see [Translating Traps from SNMPv1 to SNMPv2C](translating-traps-from-snmpv1-to-snmpv2c.md).</span></span>
-   <span data-ttu-id="22126-116">Supporta i criteri di ritrasmissione dell'applicazione e fornisce il supporto per l'esecuzione di ritrasmissione.</span><span class="sxs-lookup"><span data-stu-id="22126-116">Supports the application's retransmission policy and provides retransmission execution support.</span></span> <span data-ttu-id="22126-117">Per ulteriori informazioni, vedere [il database WinSNMP](the-winsnmp-database.md) e [informazioni sulla ritrasmissione](about-retransmission.md).</span><span class="sxs-lookup"><span data-stu-id="22126-117">For more information, see [The WinSNMP Database](the-winsnmp-database.md) and [About Retransmission](about-retransmission.md).</span></span>
-   <span data-ttu-id="22126-118">Fornisce supporto per l'entità e la conversione del contesto per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="22126-118">Provides entity and context translation support for the application.</span></span> <span data-ttu-id="22126-119">Per ulteriori informazioni, vedere [il database WinSNMP](the-winsnmp-database.md) e [impostazione della modalità di conversione dell'entità e del contesto](setting-the-entity-and-context-translation-mode.md).</span><span class="sxs-lookup"><span data-stu-id="22126-119">For more information, see [The WinSNMP Database](the-winsnmp-database.md) and [Setting the Entity and Context Translation Mode](setting-the-entity-and-context-translation-mode.md).</span></span>

<span data-ttu-id="22126-120">Per ulteriori informazioni sulla relazione tra un'applicazione WinSNMP e l'implementazione di, vedere [WinSNMP gestione dati Concepts](winsnmp-data-management-concepts.md) e [WinSNMP Sessions](winsnmp-sessions.md).</span><span class="sxs-lookup"><span data-stu-id="22126-120">For additional information about the relationship between a WinSNMP application and the implementation, see [WinSNMP Data Management Concepts](winsnmp-data-management-concepts.md) and [WinSNMP Sessions](winsnmp-sessions.md).</span></span>

 

 




