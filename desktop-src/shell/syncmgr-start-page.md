---
description: Gestione sincronizzazione fornisce una tecnologia standard centralizzata per la sincronizzazione dei file per l'utilizzo offline in un computer portatile o in un computer connesso a una rete locale.
title: Gestione sincronizzazione
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 6cdac7e5-8985-407a-98bb-936bb20ed069
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbOrient
ms.openlocfilehash: 2fc56b2afec4fdedf98fe213437a27f2592ce72b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104994784"
---
# <a name="synchronization-manager"></a><span data-ttu-id="3ca66-103">Gestione sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="3ca66-103">Synchronization Manager</span></span>

## <a name="purpose"></a><span data-ttu-id="3ca66-104">Scopo</span><span class="sxs-lookup"><span data-stu-id="3ca66-104">Purpose</span></span>

<span data-ttu-id="3ca66-105">Gestione sincronizzazione fornisce una tecnologia standard centralizzata per la sincronizzazione dei file per l'utilizzo offline in un computer portatile o in un computer connesso a una rete locale.</span><span class="sxs-lookup"><span data-stu-id="3ca66-105">The Synchronization Manager provides a centralized, standard technology for synchronizing files for offline use on a mobile computer or a computer connected to a local area network.</span></span> <span data-ttu-id="3ca66-106">Con le funzioni di connettività, le notifiche (servizio di notifica degli eventi di sistema) e la memorizzazione nella cache sul lato client, Gestione sincronizzazione fornisce un'infrastruttura per il supporto del calcolo mobile.</span><span class="sxs-lookup"><span data-stu-id="3ca66-106">Together with the connectivity functions, notifications (System Event Notification Service), and client side caching, the Synchronization Manager provides an infrastructure to support mobile computing.</span></span> <span data-ttu-id="3ca66-107">Anziché ogni applicazione che implementa la propria tecnologia per memorizzare nella cache e sincronizzare le risorse di rete per l'utilizzo locale, il sistema operativo fornisce un modello integrato che può essere utilizzato da tutte le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="3ca66-107">Instead of each application implementing its own technology to cache and synchronize network resources for local use, the operating system provides an integrated model that all applications can use.</span></span> <span data-ttu-id="3ca66-108">I file sono sincronizzati indipendentemente dal protocollo.</span><span class="sxs-lookup"><span data-stu-id="3ca66-108">Files are synchronized independent of the protocol.</span></span> <span data-ttu-id="3ca66-109">Un programma di posta elettronica, ad esempio, può trasferire i messaggi utilizzando SMTP, NMTP o POP3, mentre un browser può utilizzare HTTP e un database può utilizzare RPC (Remote Procedure Call).</span><span class="sxs-lookup"><span data-stu-id="3ca66-109">For example, an email program can transfer its messages using SMTP, NMTP, or POP3, while a browser can use HTTP, and a database can use remote procedure call (RPC) (RPC).</span></span> <span data-ttu-id="3ca66-110">Gli sviluppatori possono utilizzare l'interfaccia comune di gestione sincronizzazione nelle proprie applicazioni per sincronizzare i file tra il computer locale dell'utente e l'archiviazione di rete.</span><span class="sxs-lookup"><span data-stu-id="3ca66-110">Developers can use the common interface to the Synchronization Manager in their applications to synchronize files between the user's local computer and network storage.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="3ca66-111">Se applicabile</span><span class="sxs-lookup"><span data-stu-id="3ca66-111">Where applicable</span></span>

<span data-ttu-id="3ca66-112">Gestione sincronizzazione è progettato per le applicazioni che vengono eseguite principalmente sui computer portatili.</span><span class="sxs-lookup"><span data-stu-id="3ca66-112">The Synchronization Manager is intended for applications that run primarily on mobile computers.</span></span> <span data-ttu-id="3ca66-113">Anche le applicazioni in esecuzione su computer connessi a reti locali a latenza elevata possono trarre vantaggio dall'utilizzo di gestione sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="3ca66-113">Applications that run on computers connected to high latency local area networks may also benefit from using the Synchronization Manager.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="3ca66-114">Sviluppatori</span><span class="sxs-lookup"><span data-stu-id="3ca66-114">Developer audience</span></span>

<span data-ttu-id="3ca66-115">Questo documento è destinato agli sviluppatori di software che sviluppano applicazioni per il mobile computing e le reti locali a latenza elevata.</span><span class="sxs-lookup"><span data-stu-id="3ca66-115">This document is intended for software developers who develop applications for mobile computing and high latency local area networks.</span></span> <span data-ttu-id="3ca66-116">Questo documento fornisce un riferimento completo di tutte le parti del gestore della sincronizzazione, inclusi i metodi e le interfacce per la gestione della sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="3ca66-116">This document provides a complete reference of all parts of the Synchronization Manager including the methods and interfaces to the Synchronization Manager.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="3ca66-117">Requisiti di runtime</span><span class="sxs-lookup"><span data-stu-id="3ca66-117">Run-time requirements</span></span>

<span data-ttu-id="3ca66-118">Richiede Windows Server 2003, Windows XP, Windows 2000 o Windows Millennium Edition (Windows Me).</span><span class="sxs-lookup"><span data-stu-id="3ca66-118">Requires Windows Server 2003, Windows XP, Windows 2000, or Windows Millennium Edition (Windows Me).</span></span> <span data-ttu-id="3ca66-119">Disponibile anche come ridistribuibile per Microsoft Windows NT 4,0, Windows 98 e Windows 95.</span><span class="sxs-lookup"><span data-stu-id="3ca66-119">Also available as a redistributable for Microsoft Windows NT 4.0, Windows 98, and Windows 95.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="3ca66-120">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="3ca66-120">In this section</span></span>



| <span data-ttu-id="3ca66-121">Argomento</span><span class="sxs-lookup"><span data-stu-id="3ca66-121">Topic</span></span>                                                                                       | <span data-ttu-id="3ca66-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3ca66-122">Description</span></span>                                                                                                                                         |
|---------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3ca66-123">Informazioni su Gestione sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="3ca66-123">About Synchronization Manager</span></span>](syncmgr-about.md)<br/>                               | <span data-ttu-id="3ca66-124">Gestione sincronizzazione fornisce una tecnologia standard centralizzata per la sincronizzazione dei file per l'utilizzo offline in un computer locale.</span><span class="sxs-lookup"><span data-stu-id="3ca66-124">The Synchronization Manager provides a centralized, standard technology for synchronizing files for offline use on a local computer.</span></span><br/>     |
| [<span data-ttu-id="3ca66-125">Configurazioni di mobile computing</span><span class="sxs-lookup"><span data-stu-id="3ca66-125">Mobile Computing Configurations</span></span>](syncmgr-mobile-computing-configs.md)<br/>          | <span data-ttu-id="3ca66-126">Le applicazioni possono utilizzare sincronizzazione Manager per gestire i file e le risorse memorizzati nella cache in locale e sincronizzati nei computer desktop e portatili.</span><span class="sxs-lookup"><span data-stu-id="3ca66-126">Applications can use Sychronization Manager to keep files and resources cached locally and synchronized on mobile and desktop computers.</span></span><br/> |
| [<span data-ttu-id="3ca66-127">Scenari applicativi</span><span class="sxs-lookup"><span data-stu-id="3ca66-127">Application Scenarios</span></span>](syncmgr-app-scenarios.md)<br/>                               | <span data-ttu-id="3ca66-128">Applicazioni e servizi che possono usare Gestione sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="3ca66-128">Applications and services that can use Synchronization Manager.</span></span><br/>                                                                          |
| [<span data-ttu-id="3ca66-129">Architettura di gestione sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="3ca66-129">Synchronization Manager Architecture</span></span>](syncmgr-architecture.md)<br/>                 |                                                                                                                                                     |
| [<span data-ttu-id="3ca66-130">Utilizzo di gestione sincronizzazione da un programma</span><span class="sxs-lookup"><span data-stu-id="3ca66-130">Using Synchronization Manager from a Program</span></span>](syncmgr-using-from-a-program.md)<br/> |                                                                                                                                                     |
| [<span data-ttu-id="3ca66-131">Informazioni di riferimento su Gestione sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="3ca66-131">Synchronization Manager Reference</span></span>](syncmgr-reference.md)<br/>                       | <span data-ttu-id="3ca66-132">Gli elementi di programmazione seguenti costituiscono l'API per Gestione sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="3ca66-132">The following programming elements make up the API for Synchronization Manager.</span></span><br/>                                                          |



 

## <a name="related-topics"></a><span data-ttu-id="3ca66-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3ca66-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3ca66-134">Informazioni sul servizio di notifica eventi di sistema</span><span class="sxs-lookup"><span data-stu-id="3ca66-134">About System Event Notification Service</span></span>](../sens/about-system-event-notification-service.md)
</dt> </dl>

 

 
