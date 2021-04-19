---
description: La versione 3,1 di TAPI è un'API basata su COM che unisce la telefonia classica e IP. Le applicazioni possibili variano da chiamate vocali semplici sulla rete PSTN (Public Switched Telephone) a multicast IP multimediale con qualità del servizio (QOS).
ms.assetid: 1f7ccef8-5aad-48e7-90e9-a378dd83a870
title: Panoramica di TAPI 3,1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b30b70ccdc1c4a0985107d2bd2fc36bfbe4e3fca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311858"
---
# <a name="tapi-31-overview"></a><span data-ttu-id="cea1a-104">Panoramica di TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="cea1a-104">TAPI 3.1 Overview</span></span>

<span data-ttu-id="cea1a-105">La versione 3,1 di TAPI è un'API basata su COM che unisce la telefonia classica e IP.</span><span class="sxs-lookup"><span data-stu-id="cea1a-105">TAPI version 3.1 is a COM-based API that merges classic and IP telephony.</span></span> <span data-ttu-id="cea1a-106">Le applicazioni possibili variano da chiamate vocali semplici sulla rete PSTN (Public Switched Telephone) a multicast IP multimediale con qualità del servizio (QOS).</span><span class="sxs-lookup"><span data-stu-id="cea1a-106">Possible applications range from simple voice calls over the Public Switched Telephone Network (PSTN) to multicast multimedia IP conferencing with quality of service (QOS).</span></span>

<span data-ttu-id="cea1a-107">Per ulteriori informazioni sulle funzionalità di telefonia IP di TAPI 3,1, consultare la pagina relativa alla "telefonia IP con TAPI 3" white paper, disponibile nel sito Web Microsoft.</span><span class="sxs-lookup"><span data-stu-id="cea1a-107">For additional information on TAPI 3.1 IP Telephony capabilities, please consult the "IP Telephony with TAPI 3" white paper, which can be found on the Microsoft web site.</span></span>

<span data-ttu-id="cea1a-108">Sono disponibili quattro componenti principali per TAPI 3,1:</span><span class="sxs-lookup"><span data-stu-id="cea1a-108">There are four major components to TAPI 3.1:</span></span>

-   <span data-ttu-id="cea1a-109">API COM</span><span class="sxs-lookup"><span data-stu-id="cea1a-109">COM API</span></span>
-   <span data-ttu-id="cea1a-110">Server TAPI</span><span class="sxs-lookup"><span data-stu-id="cea1a-110">TAPI Server</span></span>
-   <span data-ttu-id="cea1a-111">Provider di servizi di telefonia (TSPs)</span><span class="sxs-lookup"><span data-stu-id="cea1a-111">Telephony Service Providers (TSPs)</span></span>
-   <span data-ttu-id="cea1a-112">Provider di flussi multimediali (MSPs)</span><span class="sxs-lookup"><span data-stu-id="cea1a-112">Media Stream Providers (MSPs)</span></span>

<span data-ttu-id="cea1a-113">Il diagramma seguente illustra l'architettura di TAPI 3,1:</span><span class="sxs-lookup"><span data-stu-id="cea1a-113">The following diagram illustrates the TAPI 3.1 architecture:</span></span>

![architettura di TAPI 3](images/callarc-gif-1.png)

<span data-ttu-id="cea1a-115">L'API viene implementata come un gruppo di oggetti Component Object Model (COM).</span><span class="sxs-lookup"><span data-stu-id="cea1a-115">The API is implemented as a suite of Component Object Model (COM) objects.</span></span> <span data-ttu-id="cea1a-116">Lo sviluppo di TAPI nel modello COM orientato a oggetti consente agli sviluppatori di scrivere applicazioni abilitate per TAPI in molti linguaggi, ad esempio Java, Visual Basic o C/C++.</span><span class="sxs-lookup"><span data-stu-id="cea1a-116">Moving TAPI to the object-oriented COM model allows developers to write TAPI-enabled applications in many languages, such as Java, Visual Basic, or C/C++.</span></span> <span data-ttu-id="cea1a-117">L'uso di COM Abilita gli aggiornamenti dei componenti delle funzionalità TAPI.</span><span class="sxs-lookup"><span data-stu-id="cea1a-117">Use of COM enables component upgrades of TAPI features.</span></span>

<span data-ttu-id="cea1a-118">Il processo del server TAPI (TAPISRV) astrae l'interfaccia del provider di servizi TAPI (TSPI) da TAPI 3. x e TAPI 2. x, consentendo l'uso dei provider di servizi di telefonia TAPI 2. x con TAPI 3. x, mantenendo lo stato interno di TAPI.</span><span class="sxs-lookup"><span data-stu-id="cea1a-118">The TAPI Server process (TAPISRV) abstracts the TAPI Service Provider Interface (TSPI) from TAPI 3.x and TAPI 2.x, allowing TAPI 2.x Telephony Service Providers to be used with TAPI 3.x, maintaining the internal state of TAPI.</span></span> <span data-ttu-id="cea1a-119">TAPISRV viene implementato come processo del servizio all'interno di SVCHOST.</span><span class="sxs-lookup"><span data-stu-id="cea1a-119">TAPISRV is implemented as a service process within SVCHOST.</span></span>

<span data-ttu-id="cea1a-120">[Provider di servizi](./tapi-service-providers.md) meccanismi astratti di trasporto multimediale specifici del provider.</span><span class="sxs-lookup"><span data-stu-id="cea1a-120">[Service Providers](./tapi-service-providers.md) abstract provider-specific media transport mechanisms.</span></span> <span data-ttu-id="cea1a-121">Si trovano in genere in coppie, ovvero un provider di servizi di telefonia (TSP) per il controllo delle chiamate e un provider di servizi multimediali (MSP) per il controllo multimediale.</span><span class="sxs-lookup"><span data-stu-id="cea1a-121">They typically exist in pairs – a Telephony Service Provider (TSP) for call control and a Media Service Provider (MSP) for media control.</span></span>

<span data-ttu-id="cea1a-122">I [provider di servizi di telefonia](./telephony-service-providers-start-page.md) (TSPs) sono responsabili della risoluzione del modello di chiamata indipendente dal protocollo di TAPI in meccanismi di controllo delle chiamate specifici del protocollo.</span><span class="sxs-lookup"><span data-stu-id="cea1a-122">[Telephony Service Providers](./telephony-service-providers-start-page.md) (TSPs) are responsible for resolving the protocol-independent call model of TAPI into protocol-specific call control mechanisms.</span></span> <span data-ttu-id="cea1a-123">TAPI 3,1 fornisce la compatibilità con le versioni precedenti di TAPI 2,1 TSPs.</span><span class="sxs-lookup"><span data-stu-id="cea1a-123">TAPI 3.1 provides backward compatibility with TAPI 2.1 TSPs.</span></span> <span data-ttu-id="cea1a-124">Per impostazione predefinita, due provider di servizi di telefonia IP (e i MSPs associati) con TAPI 3,1: H. 323 TSP e il TSP per la conferenza multicast IP.</span><span class="sxs-lookup"><span data-stu-id="cea1a-124">Two IP Telephony service providers (and their associated MSPs) ship by default with TAPI 3.1: the H.323 TSP and the IP Multicast Conferencing TSP.</span></span>

<span data-ttu-id="cea1a-125">I [provider di servizi multimediali](media-service-providers-start-page.md) (MSPS) forniscono un modo uniforme per accedere ai flussi multimediali in una chiamata, supportando l'API DirectShow<sup>TM</sup> come gestore principale del flusso multimediale.</span><span class="sxs-lookup"><span data-stu-id="cea1a-125">[Media Service Providers](media-service-providers-start-page.md) (MSPs) provide a uniform way to access the media streams in a call, supporting the DirectShow<sup>TM</sup> API as the primary media stream handler.</span></span> <span data-ttu-id="cea1a-126">TAPI MSPs implementa le interfacce DirectShow per un determinato TSP e sono necessarie per qualsiasi servizio di telefonia che usa lo streaming DirectShow.</span><span class="sxs-lookup"><span data-stu-id="cea1a-126">TAPI MSPs implement DirectShow interfaces for a particular TSP and are required for any telephony service that makes use of DirectShow streaming.</span></span> <span data-ttu-id="cea1a-127">I flussi generici vengono gestiti dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="cea1a-127">Generic streams are handled by the application.</span></span>

 

 
