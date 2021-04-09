---
title: Servizio SNMP
description: L'implementazione di Microsoft Windows del Simple Network Management Protocol (SNMP) viene usata per configurare i dispositivi remoti, monitorare le prestazioni della rete, controllare l'utilizzo della rete e rilevare errori di rete o accedere in modo non appropriato. Importante l'API Microsoft Windows SNMP supporta solo le versioni di protocollo fino a SNMPv2C. Non supporta versioni successive del protocollo.
ms.assetid: fbaddb10-804b-4230-8986-717edc19a2f5
keywords:
- SNMP SNMP
- SNMP SNMP, pagina iniziale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71df55c79244c0f74ef685271834adc01ca7e981
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047241"
---
# <a name="snmp-service"></a><span data-ttu-id="387b1-106">Servizio SNMP</span><span class="sxs-lookup"><span data-stu-id="387b1-106">SNMP Service</span></span>

<span data-ttu-id="387b1-107">\[SNMP è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="387b1-107">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="387b1-108">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="387b1-108">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="387b1-109">Usare invece [gestione remota Windows](/windows/desktop/WinRM/portal), ovvero l'implementazione Microsoft di WS-Man.\]</span><span class="sxs-lookup"><span data-stu-id="387b1-109">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

## <a name="purpose"></a><span data-ttu-id="387b1-110">Scopo</span><span class="sxs-lookup"><span data-stu-id="387b1-110">Purpose</span></span>

<span data-ttu-id="387b1-111">L'implementazione di Microsoft Windows del Simple Network Management Protocol (SNMP) viene usata per configurare i dispositivi remoti, monitorare le prestazioni della rete, controllare l'utilizzo della rete e rilevare errori di rete o accedere in modo non appropriato.</span><span class="sxs-lookup"><span data-stu-id="387b1-111">The Microsoft Windows implementation of the Simple Network Management Protocol (SNMP) is used to configure remote devices, monitor network performance, audit network usage, and detect network faults or inappropriate access.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="387b1-112">L'API Microsoft Windows SNMP supporta solo le versioni di protocollo fino a SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="387b1-112">The Microsoft Windows SNMP API only supports protocol versions up to SNMPv2C.</span></span> <span data-ttu-id="387b1-113">Non supporta versioni successive del protocollo.</span><span class="sxs-lookup"><span data-stu-id="387b1-113">It does not support any later versions of the protocol.</span></span>

 

## <a name="where-applicable"></a><span data-ttu-id="387b1-114">Se applicabile</span><span class="sxs-lookup"><span data-stu-id="387b1-114">Where applicable</span></span>

<span data-ttu-id="387b1-115">SNMP utilizza un'architettura distribuita costituita da applicazioni di gestione e applicazioni agente.</span><span class="sxs-lookup"><span data-stu-id="387b1-115">SNMP uses a distributed architecture consisting of management applications and agent applications.</span></span> <span data-ttu-id="387b1-116">Il servizio SNMP implementa un agente SNMP.</span><span class="sxs-lookup"><span data-stu-id="387b1-116">The SNMP service implements an SNMP agent.</span></span> <span data-ttu-id="387b1-117">Per utilizzare le informazioni fornite dal servizio SNMP, è necessario disporre di almeno un host in cui sia in esecuzione un'applicazione di gestione SNMP.</span><span class="sxs-lookup"><span data-stu-id="387b1-117">To use the information the SNMP service provides, you must have at least one host that is running an SNMP management application.</span></span> <span data-ttu-id="387b1-118">È possibile utilizzare software di gestione SNMP di terze parti oppure sviluppare un'applicazione software di gestione SNMP personalizzata.</span><span class="sxs-lookup"><span data-stu-id="387b1-118">You can use third-party SNMP management software, or you can develop your own SNMP management software application.</span></span> <span data-ttu-id="387b1-119">A questo scopo sono disponibili le API seguenti:</span><span class="sxs-lookup"><span data-stu-id="387b1-119">The following APIs are available for this purpose:</span></span>

-   <span data-ttu-id="387b1-120">API di gestione SNMP, un set di funzioni che è possibile utilizzare per sviluppare rapidamente sistemi di gestione SNMP di base</span><span class="sxs-lookup"><span data-stu-id="387b1-120">SNMP Management API, a set of functions that can be used to quickly develop basic SNMP management systems</span></span>
-   <span data-ttu-id="387b1-121">API WinSNMP, versione 2,0, un set di funzioni per la codifica, la decodifica, l'invio e la ricezione di messaggi SNMP</span><span class="sxs-lookup"><span data-stu-id="387b1-121">WinSNMP API, version 2.0, a set of functions for encoding, decoding, sending, and receiving SNMP messages</span></span>

<span data-ttu-id="387b1-122">Inoltre, l'API dell'agente di estensione SNMP definisce l'interfaccia tra il servizio SNMP e le DLL dell'agente di estensione SNMP di terze parti.</span><span class="sxs-lookup"><span data-stu-id="387b1-122">Additionally, the SNMP Extension Agent API defines the interface between the SNMP service and third-party SNMP extension agent DLLs.</span></span> <span data-ttu-id="387b1-123">È possibile utilizzare le funzioni API dell'utilità SNMP per semplificare l'elaborazione dei messaggi SNMP.</span><span class="sxs-lookup"><span data-stu-id="387b1-123">The SNMP Utility API functions can be used to simplify the processing of SNMP messages.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="387b1-124">Sviluppatori</span><span class="sxs-lookup"><span data-stu-id="387b1-124">Developer audience</span></span>

<span data-ttu-id="387b1-125">Le API elencate nella sezione precedente sono progettate per l'uso da parte dei programmatori C/C++.</span><span class="sxs-lookup"><span data-stu-id="387b1-125">The APIs listed in the preceding section are designed for use by C/C++ programmers.</span></span> <span data-ttu-id="387b1-126">Sono necessari familiarità con SNMP e SNMPv2C, nonché una conoscenza pratica dei concetti di rete e di gestione della rete.</span><span class="sxs-lookup"><span data-stu-id="387b1-126">Familiarity with SNMP and SNMPv2C, as well as a working knowledge of networking and network management concepts, are required.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="387b1-127">Requisiti di runtime</span><span class="sxs-lookup"><span data-stu-id="387b1-127">Run-time requirements</span></span>

<span data-ttu-id="387b1-128">Per ulteriori informazioni sul sistema operativo necessario per utilizzare una particolare funzione, vedere la sezione requisiti della pagina di riferimento per tale funzione.</span><span class="sxs-lookup"><span data-stu-id="387b1-128">For more information about the operating system required to use a particular function, see the Requirements section of the reference page for that function.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="387b1-129">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="387b1-129">In this section</span></span>



| <span data-ttu-id="387b1-130">Argomento</span><span class="sxs-lookup"><span data-stu-id="387b1-130">Topic</span></span>                                                                                                | <span data-ttu-id="387b1-131">Descrizione</span><span class="sxs-lookup"><span data-stu-id="387b1-131">Description</span></span>                                                                                                                                     |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="387b1-132">Novità in SNMP</span><span class="sxs-lookup"><span data-stu-id="387b1-132">New in SNMP</span></span>](new-in-snmp.md)<br/>                                                            | <span data-ttu-id="387b1-133">Informazioni sugli aggiornamenti di SNMP.</span><span class="sxs-lookup"><span data-stu-id="387b1-133">Information on updates to SNMP.</span></span><br/>                                                                                                      |
| [<span data-ttu-id="387b1-134">Simple Network Management Protocol (SNMP)</span><span class="sxs-lookup"><span data-stu-id="387b1-134">Simple Network Management Protocol (SNMP)</span></span>](simple-network-management-protocol-snmp-.md)<br/> | <span data-ttu-id="387b1-135">Informazioni di riferimento sulle API per SNMP, tra cui l'API di gestione SNMP, l'API dell'agente di estensione SNMP e le funzioni API dell'utilità SNMP.</span><span class="sxs-lookup"><span data-stu-id="387b1-135">Information and API reference for SNMP, including the SNMP Management API, SNMP Extension Agent API, and SNMP Utility API functions.</span></span><br/> |
| [<span data-ttu-id="387b1-136">API WinSNMP</span><span class="sxs-lookup"><span data-stu-id="387b1-136">WinSNMP API</span></span>](snmp-reference.md)<br/>                                                         | <span data-ttu-id="387b1-137">Informazioni di riferimento sulle API per Microsoft Windows SNMP Application Programming Interface (API WinSNMP).</span><span class="sxs-lookup"><span data-stu-id="387b1-137">Information and API reference for the Microsoft Windows SNMP Application Programming Interface (WinSNMP API).</span></span> <br/>                       |



 

## <a name="related-topics"></a><span data-ttu-id="387b1-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="387b1-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="387b1-139">Dynamic Host Configuration Protocol (DHCP)</span><span class="sxs-lookup"><span data-stu-id="387b1-139">Dynamic Host Configuration Protocol (DHCP)</span></span>](/previous-versions/windows/desktop/dhcp/dhcp-start-page)
</dt> <dt>

[<span data-ttu-id="387b1-140">Gestione della rete</span><span class="sxs-lookup"><span data-stu-id="387b1-140">Network Management</span></span>](/windows/desktop/NetMgmt/network-management)
</dt> <dt>

[<span data-ttu-id="387b1-141">Routing and Remote Access Service</span><span class="sxs-lookup"><span data-stu-id="387b1-141">Routing and Remote Access Service</span></span>](/windows/desktop/RRAS/portal)
</dt> </dl>

 

