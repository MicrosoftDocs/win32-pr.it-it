---
description: Il modello di programmazione della telefonia Microsoft astrae il controllo delle comunicazioni dal controllo dei dispositivi, liberando le applicazioni degli utenti finali e i produttori di dispositivi dalla necessità di procedere in contemporanea.
ms.assetid: 07dd8447-08dc-4ae3-9a22-70e914c392db
title: Modello di programmazione di telefonia Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0efb8947f3b428ab4a252301e3fdd5f94e29f6ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305586"
---
# <a name="microsoft-telephony-programming-model"></a><span data-ttu-id="fadd6-103">Modello di programmazione di telefonia Microsoft</span><span class="sxs-lookup"><span data-stu-id="fadd6-103">Microsoft Telephony Programming Model</span></span>

<span data-ttu-id="fadd6-104">Il modello di programmazione della telefonia Microsoft astrae il controllo delle comunicazioni dal controllo dei dispositivi, liberando le applicazioni degli utenti finali e i produttori di dispositivi dalla necessità di procedere in contemporanea.</span><span class="sxs-lookup"><span data-stu-id="fadd6-104">The Microsoft Telephony programming model abstracts communications control from device control, freeing end-user applications and device manufacturers from the need to march in lockstep.</span></span> <span data-ttu-id="fadd6-105">Utilizzando questo modello, un'applicazione server o un utente finale non richiede informazioni dettagliate sul controllo del dispositivo e non è necessario che il dispositivo sia personalizzato per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="fadd6-105">Using this model, an end-user or server application does not require detailed information on device control and the device does not need to be tailored to the application.</span></span> <span data-ttu-id="fadd6-106">Le applicazioni e i dispositivi possono essere sottoposti a Innovation and Change senza renderli inutili ai clienti.</span><span class="sxs-lookup"><span data-stu-id="fadd6-106">Applications and devices can undergo innovation and change without rendering each other useless to customers.</span></span>

<span data-ttu-id="fadd6-107">Il diagramma seguente illustra il modo in cui questa astrazione viene eseguita.</span><span class="sxs-lookup"><span data-stu-id="fadd6-107">The following diagram illustrates how this abstraction is accomplished.</span></span>

![come TAPI astrae il controllo delle comunicazioni dal controllo del dispositivo](images/tapicomp.png)

<span data-ttu-id="fadd6-109">Questi componenti possono essere visualizzati come repository di conoscenze specializzate.</span><span class="sxs-lookup"><span data-stu-id="fadd6-109">These components can be viewed as repositories of specialized knowledge.</span></span> <span data-ttu-id="fadd6-110">L'applicazione TAPI (Telephony Application Programming Interface) è in grado di riconoscere le esigenze degli utenti, la DLL TAPI e TAPISRV comprendere la telefonia generale e i provider di servizi (TSP e MSP) conoscono il controllo dei dispositivi dettagliato.</span><span class="sxs-lookup"><span data-stu-id="fadd6-110">The Telephony Application Programming Interface (TAPI) application knows user needs, the TAPI DLL and TAPISRV understand general telephony, and the service providers (TSP and MSP) know detailed device control.</span></span> <span data-ttu-id="fadd6-111">Gli sviluppatori di applicazioni e i produttori di dispositivi richiedono solo una conoscenza generale degli altri requisiti.</span><span class="sxs-lookup"><span data-stu-id="fadd6-111">Application writers and device manufacturers require only general knowledge of each other's requirements.</span></span>

-   <span data-ttu-id="fadd6-112">Un'applicazione carica la DLL TAPI nello spazio di elaborazione e USA TAPI per comunicare le esigenze.</span><span class="sxs-lookup"><span data-stu-id="fadd6-112">An application loads the TAPI DLL into its process space and uses TAPI to communicate needs.</span></span>
-   <span data-ttu-id="fadd6-113">TAPI stabilisce le comunicazioni di collegamento RPC con il server TAPI.</span><span class="sxs-lookup"><span data-stu-id="fadd6-113">TAPI establishes an RPC link communications with the TAPI Server.</span></span>
-   <span data-ttu-id="fadd6-114">Inoltre, TAPI 3. x crea un oggetto MSP e comunica con esso utilizzando un set di comandi definito, Media Service Provider Interface (MSPI).</span><span class="sxs-lookup"><span data-stu-id="fadd6-114">In addition, TAPI 3.x creates an MSP object and communicates with it using a defined set of commands, the Media Service Provider Interface (MSPI).</span></span>
-   <span data-ttu-id="fadd6-115">Quando un'applicazione chiama un'operazione TAPI, la libreria a collegamento dinamico TAPI convalida ed effettua il marshalling dei parametri, quindi le invia a TAPISRV.</span><span class="sxs-lookup"><span data-stu-id="fadd6-115">When an application calls a TAPI operation, the TAPI dynamic-link library validates and marshals the parameters, then forwards the information to TAPISRV.</span></span>
-   <span data-ttu-id="fadd6-116">TAPISRV tiene traccia delle risorse di comunicazione disponibili per il computer locale e le interfacce con i provider di servizi di telefonia (TSPs) tramite l'interfaccia di telefonia del provider di servizi (TSPI).</span><span class="sxs-lookup"><span data-stu-id="fadd6-116">TAPISRV tracks communications resources available to the local machine and interfaces with the Telephony Service Providers (TSPs) using the Telephony Service Provider Interface (TSPI).</span></span>
-   <span data-ttu-id="fadd6-117">Le comunicazioni tra un TSP e un MSP avvengono utilizzando una connessione virtuale che passa attraverso la DLL TAPI e TAPISRV.</span><span class="sxs-lookup"><span data-stu-id="fadd6-117">Communications between a TSP and an MSP take place using a virtual connection that passes through the TAPI DLL and TAPISRV.</span></span>
-   <span data-ttu-id="fadd6-118">La coppia TSP/MSP fornisce informazioni sullo stato e sulle funzionalità del dispositivo e implementa i comandi specifici richiesti per una risposta desiderata.</span><span class="sxs-lookup"><span data-stu-id="fadd6-118">The TSP/MSP pair supplies information on device state and capabilities and implements the specific commands required for a desired response.</span></span>

<span data-ttu-id="fadd6-119">Il risultato dell'uso di questo modello di programmazione è che le applicazioni possono ignorare o modificare le modifiche apportate ai dispositivi e i nuovi dispositivi possono essere immediatamente utili anziché attendere le modifiche di base del codice.</span><span class="sxs-lookup"><span data-stu-id="fadd6-119">The result of using this programming model is that applications can ignore or adjust to device changes and new devices can be instantly useful instead of waiting on code base changes.</span></span> <span data-ttu-id="fadd6-120">La potenziale quota di mercato viene espansa sia per writer di applicazioni che per produttori di dispositivi.</span><span class="sxs-lookup"><span data-stu-id="fadd6-120">Potential market share is expanded for both application writers and device manufacturers.</span></span>

<span data-ttu-id="fadd6-121">Gli argomenti seguenti descrivono i componenti di telefonia Microsoft in modo più dettagliato:</span><span class="sxs-lookup"><span data-stu-id="fadd6-121">The following topics describe the Microsoft Telephony components in more detail:</span></span>

-   [<span data-ttu-id="fadd6-122">Applicazioni TAPI</span><span class="sxs-lookup"><span data-stu-id="fadd6-122">TAPI Applications</span></span>](tapi-applications.md)
-   [<span data-ttu-id="fadd6-123">DLL TAPI</span><span class="sxs-lookup"><span data-stu-id="fadd6-123">TAPI DLL</span></span>](tapi-dll.md)
-   [<span data-ttu-id="fadd6-124">Server TAPI</span><span class="sxs-lookup"><span data-stu-id="fadd6-124">TAPI Server</span></span>](tapi-server.md)
-   [<span data-ttu-id="fadd6-125">Provider di servizi</span><span class="sxs-lookup"><span data-stu-id="fadd6-125">Service Providers</span></span>](service-providers.md)
-   [<span data-ttu-id="fadd6-126">Modello sincrono/asincrono</span><span class="sxs-lookup"><span data-stu-id="fadd6-126">Synchronous/Asynchronous Model</span></span>](synchronous-asynchronous-model.md)
-   [<span data-ttu-id="fadd6-127">Strutture di dati TAPI</span><span class="sxs-lookup"><span data-stu-id="fadd6-127">TAPI Data Structures</span></span>](tapi-data-structures.md)
-   [<span data-ttu-id="fadd6-128">Livelli di servizio TAPI</span><span class="sxs-lookup"><span data-stu-id="fadd6-128">TAPI Levels of Service</span></span>](tapi-levels-of-service.md)

 

 



