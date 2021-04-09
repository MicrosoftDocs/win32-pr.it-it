---
title: Panoramica dell'interfaccia di programmazione Microsoft Agent
description: Panoramica dell'interfaccia di programmazione Microsoft Agent
ms.assetid: 8709441b-9739-4f11-a2de-40a5f5eefb72
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad89249e064eb89d37f497fb79cb8982c79cb83c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856214"
---
# <a name="microsoft-agent-programming-interface-overview"></a><span data-ttu-id="15011-103">Panoramica dell'interfaccia di programmazione Microsoft Agent</span><span class="sxs-lookup"><span data-stu-id="15011-103">Microsoft Agent Programming Interface Overview</span></span>

<span data-ttu-id="15011-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="15011-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="15011-105">L'API dell'agente Microsoft fornisce servizi che supportano la visualizzazione e l'animazione dei caratteri animati.</span><span class="sxs-lookup"><span data-stu-id="15011-105">The Microsoft Agent API provides services that support the display and animation of animated characters.</span></span> <span data-ttu-id="15011-106">Implementato come server di automazione OLE (Component Object Model \[ com \] ), Microsoft Agent consente a più applicazioni, denominate client o applicazioni client, di ospitare e accedere ai servizi di animazione, input e output allo stesso tempo.</span><span class="sxs-lookup"><span data-stu-id="15011-106">Implemented as an OLE Automation (Component Object Model \[COM\]) server, Microsoft Agent enables multiple applications, called clients or client applications, to host and access its animation, input, and output services at the same time.</span></span> <span data-ttu-id="15011-107">Un client può essere qualsiasi applicazione che si connette alle interfacce COM di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="15011-107">A client can be any application that connects to the Microsoft Agent's COM interfaces.</span></span>

<span data-ttu-id="15011-108">In quanto server COM, Microsoft Agent viene avviato automaticamente solo quando un'applicazione client usa le interfacce COM e le richieste per la connessione.</span><span class="sxs-lookup"><span data-stu-id="15011-108">As a COM server, Microsoft Agent automatically starts up only when a client application uses the COM interfaces and requests to connect to it.</span></span> <span data-ttu-id="15011-109">Rimane in esecuzione fino a quando tutti i client non chiudono le connessioni.</span><span class="sxs-lookup"><span data-stu-id="15011-109">It remains running until all clients close their connections.</span></span> <span data-ttu-id="15011-110">Quando non viene mantenuto alcun client connesso, l'agente Microsoft viene chiuso automaticamente.</span><span class="sxs-lookup"><span data-stu-id="15011-110">When no connected clients remain, Microsoft Agent automatically exits.</span></span>

<span data-ttu-id="15011-111">Sebbene sia possibile chiamare direttamente le interfacce COM di Microsoft Agent, Microsoft Agent include anche un controllo Microsoft ActiveX.</span><span class="sxs-lookup"><span data-stu-id="15011-111">Although you can call Microsoft Agent's COM interfaces directly, Microsoft Agent also includes a Microsoft ActiveX control.</span></span> <span data-ttu-id="15011-112">Questo controllo consente di accedere facilmente ai servizi di Microsoft Agent dai linguaggi di programmazione che supportano l'interfaccia di controllo ActiveX.</span><span class="sxs-lookup"><span data-stu-id="15011-112">This control makes it easy to access Microsoft Agent's services from programming languages that support the ActiveX control interface.</span></span>

<span data-ttu-id="15011-113">Oltre a supportare i programmi autonomi scritti per Windows, è possibile creare script per Agent per supportare pagine Web, purché il browser supporti l'interfaccia ActiveX.</span><span class="sxs-lookup"><span data-stu-id="15011-113">In addition to supporting stand-alone programs written for Windows, Agent can be scripted to support webpages, provided that the browser supports the ActiveX interface.</span></span> <span data-ttu-id="15011-114">Microsoft Internet Explorer include il supporto per ActiveX e per i linguaggi di scripting che è possibile utilizzare per programmare Agent.</span><span class="sxs-lookup"><span data-stu-id="15011-114">Microsoft Internet Explorer includes support for ActiveX as well as scripting languages that you can use to program Agent.</span></span> <span data-ttu-id="15011-115">Se non si usa Internet Explorer, consultare il fornitore o il fornitore per informazioni sul supporto del browser per ActiveX.</span><span class="sxs-lookup"><span data-stu-id="15011-115">If you are not using Internet Explorer, consult with your vendor or supplier about the browser's support for ActiveX.</span></span>

<span data-ttu-id="15011-116">Le informazioni seguenti forniscono una breve panoramica delle interfacce di programmazione per il software dell'agente Microsoft.</span><span class="sxs-lookup"><span data-stu-id="15011-116">The following information provides a brief overview of the programming interfaces for the Microsoft Agent software.</span></span>

-   [<span data-ttu-id="15011-117">Servizi di animazione</span><span class="sxs-lookup"><span data-stu-id="15011-117">Animation Services</span></span>](animation-services.md)
-   [<span data-ttu-id="15011-118">Servizi di input</span><span class="sxs-lookup"><span data-stu-id="15011-118">Input Services</span></span>](input-services.md)
-   [<span data-ttu-id="15011-119">Finestra comandi vocali</span><span class="sxs-lookup"><span data-stu-id="15011-119">The Voice Commands Window</span></span>](the-voice-commands-window.md)
-   [<span data-ttu-id="15011-120">Servizi di output</span><span class="sxs-lookup"><span data-stu-id="15011-120">Output Services</span></span>](output-services.md)

 

 




