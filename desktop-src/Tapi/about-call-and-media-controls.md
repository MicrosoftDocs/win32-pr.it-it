---
description: I controlli della chiamata e dei supporti TAPI 3 sono un set generico di oggetti COM, interfacce e metodi per effettuare chiamate tra due o più computer.
ms.assetid: e345df2f-1b68-41be-ac2d-b771136ee831
title: Informazioni sui controlli Call e media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae65d1a10d004cb16e0ba8753c27665cb7a30ff3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "103886010"
---
# <a name="about-call-and-media-controls"></a><span data-ttu-id="71a36-103">Informazioni sui controlli Call e media</span><span class="sxs-lookup"><span data-stu-id="71a36-103">About Call And Media Controls</span></span>

<span data-ttu-id="71a36-104">I controlli della chiamata e dei supporti TAPI 3 sono un set generico di oggetti COM, interfacce e metodi per effettuare chiamate tra due o più computer.</span><span class="sxs-lookup"><span data-stu-id="71a36-104">TAPI 3 call and media controls are a generic set of COM objects, interfaces, and methods for making calls between two or more machines.</span></span> <span data-ttu-id="71a36-105">Nel contesto di TAPI 3, *Call* si riferisce non solo alla trasmissione vocale sulla rete PSTN (Public Switched Telephone), ma a qualsiasi meccanismo di supporto e trasporto per cui sono presenti i provider di servizi, ad esempio una conferenza multicast multimediale in esecuzione su una rete Intranet aziendale.</span><span class="sxs-lookup"><span data-stu-id="71a36-105">In the context of TAPI 3, *call* refers not just to voice transmission over the public switched telephone network (PSTN) but to any medium and transport mechanism for which service providers exist: for example, a multimedia multicast conference running on a corporate intranet.</span></span>

<span data-ttu-id="71a36-106">I cinque oggetti principali nella chiamata TAPI 3 e nell'architettura del controllo multimediale sono [TAPI](tapi-object.md), [Address](address-object.md), [Terminal](terminal-object.md), [Call](call-object.md)e [CallHub](callhub-object.md).</span><span class="sxs-lookup"><span data-stu-id="71a36-106">The five main objects in the TAPI 3 call and media control architecture are [TAPI](tapi-object.md), [Address](address-object.md), [Terminal](terminal-object.md), [Call](call-object.md), and [CallHub](callhub-object.md).</span></span> <span data-ttu-id="71a36-107">Inoltre, è stato effettuato il provisioning per [interfacce specifiche del provider](provider-specific-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="71a36-107">In addition, provision has been made for [provider-specific interfaces](provider-specific-interfaces.md).</span></span>

<span data-ttu-id="71a36-108">Il diagramma seguente illustra il modo in cui questi oggetti interagiscono.</span><span class="sxs-lookup"><span data-stu-id="71a36-108">The following diagram illustrates how these objects interact.</span></span>

![interazioni tra la chiamata a TAPI 3,0 e gli oggetti di controllo multimediale](images/sdkobj2.png)

## <a name="features"></a><span data-ttu-id="71a36-110">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="71a36-110">Features</span></span>

-   <span data-ttu-id="71a36-111">Astrae sia la funzionalità chiamata che la funzionalità multimediale per consentire protocolli di comunicazione diversi e apparentemente incompatibili per esporre un'interfaccia comune alle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="71a36-111">Abstracts both call and media functionality to allow different and seemingly incompatible communication protocols to expose a common interface to applications.</span></span>
-   <span data-ttu-id="71a36-112">In base alla Component Object Model (COM), le applicazioni possono essere scritte in quasi tutti i linguaggi.</span><span class="sxs-lookup"><span data-stu-id="71a36-112">Based on the Component Object Model (COM) so applications can be written in nearly any language.</span></span> <span data-ttu-id="71a36-113">Se sono necessarie ulteriori informazioni su COM, consultare Platform Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="71a36-113">If you require additional information on COM, please consult the Platform Software Development Kit (SDK).</span></span>
-   <span data-ttu-id="71a36-114">Controllo delle chiamate fornito da provider di servizi di telefonia (TSPs), che implementano meccanismi specifici del trasporto.</span><span class="sxs-lookup"><span data-stu-id="71a36-114">Call control provided by Telephony Service Providers (TSPs), which implement transport-specific mechanisms.</span></span>
-   <span data-ttu-id="71a36-115">Controllo multimediale fornito da provider di servizi multimediali (MSPs).</span><span class="sxs-lookup"><span data-stu-id="71a36-115">Media control provided by Media Service providers (MSPs).</span></span> <span data-ttu-id="71a36-116">MSPs correnti usano DirectShow.</span><span class="sxs-lookup"><span data-stu-id="71a36-116">Current MSPs use DirectShow.</span></span> <span data-ttu-id="71a36-117">DirectShow è un sistema modulare di componenti collegabili, denominati filtri, disposti in una configurazione denominata grafico a filtro.</span><span class="sxs-lookup"><span data-stu-id="71a36-117">DirectShow is a modular system of pluggable components called filters, arranged in a configuration called a filter graph.</span></span> <span data-ttu-id="71a36-118">Il gestore del grafo dei filtri controlla la connessione di questi filtri e controlla il flusso di dati del flusso.</span><span class="sxs-lookup"><span data-stu-id="71a36-118">The filter graph manager oversees the connection of these filters and controls the stream's data flow.</span></span> <span data-ttu-id="71a36-119">Per ulteriori informazioni su DirectShow, consultare Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="71a36-119">If you require additional information on DirectShow, please consult the Platform SDK.</span></span>

 

 



