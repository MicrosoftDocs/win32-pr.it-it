---
title: API WinSNMP
description: L'interfaccia di programmazione delle applicazioni di Microsoft Windows (l'API WinSNMP) versione 1.1 a e 2,0 consentono di sviluppare applicazioni di gestione della rete basate su SNMP eseguite nell'ambiente Windows.
ms.assetid: 54d9b61a-815a-41c3-9365-ec4478acc3f2
keywords:
- API WinSNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12d502060daa2931ca67c4476448347602159c98
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047079"
---
# <a name="winsnmp-api"></a><span data-ttu-id="3fd0f-104">API WinSNMP</span><span class="sxs-lookup"><span data-stu-id="3fd0f-104">WinSNMP API</span></span>

<span data-ttu-id="3fd0f-105">\[SNMP è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="3fd0f-105">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="3fd0f-106">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="3fd0f-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="3fd0f-107">Usare invece [gestione remota Windows](/windows/desktop/WinRM/portal), ovvero l'implementazione Microsoft di WS-Man.\]</span><span class="sxs-lookup"><span data-stu-id="3fd0f-107">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="3fd0f-108">L'interfaccia di programmazione delle applicazioni di Microsoft Windows (l'API WinSNMP) versione 1.1 a e 2,0 consentono di sviluppare applicazioni di gestione della rete basate su SNMP eseguite nell'ambiente Windows.</span><span class="sxs-lookup"><span data-stu-id="3fd0f-108">The Microsoft Windows SNMP Application Programming Interface (the WinSNMP API) versions 1.1a and 2.0 allow you to develop SNMP-based network management applications that execute in the Windows environment.</span></span> <span data-ttu-id="3fd0f-109">Il Simple Network Management Protocol (SNMP) è un protocollo di richiesta-risposta che trasferisce le informazioni di gestione tra le entità del protocollo.</span><span class="sxs-lookup"><span data-stu-id="3fd0f-109">The Simple Network Management Protocol (SNMP) is a request-response protocol that transfers management information between protocol entities.</span></span>

<span data-ttu-id="3fd0f-110">WinSNMP è stato sviluppato congiuntamente con la collaborazione, l'input e il supporto di diverse società, associazioni e singoli utenti.</span><span class="sxs-lookup"><span data-stu-id="3fd0f-110">WinSNMP has been jointly developed with the cooperation, input, and support from several companies, associations and individuals.</span></span>

<span data-ttu-id="3fd0f-111">Nella prima parte di questa panoramica vengono fornite informazioni sull'addendum WinSNMP 2,0, le versioni SNMP e un elenco delle richieste di commenti (RFC) pertinenti.</span><span class="sxs-lookup"><span data-stu-id="3fd0f-111">The first part of this overview provides information about the WinSNMP 2.0 Addendum, SNMP versions, and a list of the relevant Requests for Comments (RFCs).</span></span> <span data-ttu-id="3fd0f-112">Viene inoltre descritto il modello WinSNMP e i componenti e le funzionalità dell'implementazione Microsoft WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="3fd0f-112">It also describes the WinSNMP model, and the components and features of the Microsoft WinSNMP implementation.</span></span> <span data-ttu-id="3fd0f-113">Vengono inoltre fornite informazioni sui concetti di gestione e comunicazione dei dati necessari per programmare nell'ambiente WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="3fd0f-113">It also provides information about data management and communications concepts you need to program in the WinSNMP environment.</span></span>

<span data-ttu-id="3fd0f-114">La seconda sezione illustra le funzioni WinSNMP e le attività di programmazione WinSNMP correlate seguenti:</span><span class="sxs-lookup"><span data-stu-id="3fd0f-114">The second section discusses the WinSNMP functions and the following related WinSNMP programming tasks:</span></span>

-   [<span data-ttu-id="3fd0f-115">Apertura e chiusura di un'applicazione WinSNMP</span><span class="sxs-lookup"><span data-stu-id="3fd0f-115">Opening and closing a WinSNMP application</span></span>](opening-and-closing-a-winsnmp-application.md)
-   [<span data-ttu-id="3fd0f-116">Apertura e chiusura di una sessione WinSNMP</span><span class="sxs-lookup"><span data-stu-id="3fd0f-116">Opening and closing a WinSNMP session</span></span>](opening-and-closing-a-winsnmp-session.md)
-   [<span data-ttu-id="3fd0f-117">Gestione di trap e notifiche</span><span class="sxs-lookup"><span data-stu-id="3fd0f-117">Managing traps and notifications</span></span>](managing-traps-and-notifications.md)
-   [<span data-ttu-id="3fd0f-118">Utilizzo degli elenchi di associazioni variabili</span><span class="sxs-lookup"><span data-stu-id="3fd0f-118">Working with variable binding lists</span></span>](working-with-variable-binding-lists.md)
-   [<span data-ttu-id="3fd0f-119">Utilizzo delle unità dati del protocollo</span><span class="sxs-lookup"><span data-stu-id="3fd0f-119">Working with protocol data units</span></span>](working-with-protocol-data-units.md)
-   [<span data-ttu-id="3fd0f-120">Invio di messaggi SNMP</span><span class="sxs-lookup"><span data-stu-id="3fd0f-120">Sending SNMP messages</span></span>](sending-snmp-messages.md)
-   [<span data-ttu-id="3fd0f-121">Ricezione di messaggi SNMP</span><span class="sxs-lookup"><span data-stu-id="3fd0f-121">Receiving SNMP messages</span></span>](receiving-snmp-messages.md)
-   [<span data-ttu-id="3fd0f-122">Gestione degli identificatori di oggetto</span><span class="sxs-lookup"><span data-stu-id="3fd0f-122">Managing object identifiers</span></span>](managing-object-identifiers.md)
-   [<span data-ttu-id="3fd0f-123">Liberazione di descrittori WinSNMP</span><span class="sxs-lookup"><span data-stu-id="3fd0f-123">Freeing WinSNMP descriptors</span></span>](freeing-winsnmp-descriptors.md)
-   [<span data-ttu-id="3fd0f-124">Impostazione della modalità di conversione dell'entità e del contesto</span><span class="sxs-lookup"><span data-stu-id="3fd0f-124">Setting the entity and context translation mode</span></span>](setting-the-entity-and-context-translation-mode.md)
-   [<span data-ttu-id="3fd0f-125">Gestione dei criteri di ritrasmissione</span><span class="sxs-lookup"><span data-stu-id="3fd0f-125">Managing the retransmission policy</span></span>](managing-the-retransmission-policy.md)
-   [<span data-ttu-id="3fd0f-126">Scrittura di applicazioni WinSNMP con più thread</span><span class="sxs-lookup"><span data-stu-id="3fd0f-126">Writing WinSNMP applications with multiple threads</span></span>](writing-winsnmp-applications-with-multiple-threads.md)
-   [<span data-ttu-id="3fd0f-127">Registrazione di un'applicazione agente SNMP</span><span class="sxs-lookup"><span data-stu-id="3fd0f-127">Registering an SNMP agent application</span></span>](registering-an-snmp-agent-application.md)

<span data-ttu-id="3fd0f-128">Prima di leggere questa panoramica, è necessario avere familiarità con i concetti di base relativi alla programmazione SNMP e Windows.</span><span class="sxs-lookup"><span data-stu-id="3fd0f-128">You should be familiar with the basic concepts of SNMP and Windows programming before reading this overview.</span></span> <span data-ttu-id="3fd0f-129">Per ulteriori informazioni su SNMP, vedere [Simple Network Management Protocol](simple-network-management-protocol-snmp-.md) e le relative richieste di commenti (RFC) pubblicate da Internet Engineering Task Force (IETF).</span><span class="sxs-lookup"><span data-stu-id="3fd0f-129">For more information about SNMP, see [Simple Network Management Protocol](simple-network-management-protocol-snmp-.md) and the relevant Requests for Comments (RFCs) which are published by the Internet Engineering Task Force (IETF).</span></span>

 

 