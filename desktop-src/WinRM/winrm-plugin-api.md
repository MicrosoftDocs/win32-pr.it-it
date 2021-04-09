---
title: API del plug-in WinRM
description: Il plug-in WinRM Application Programming Interface (API) fornisce funzionalità che consentono a un utente di scrivere plug-in implementando determinate API per le operazioni e gli URI delle risorse supportati.
ms.assetid: d3e103c1-221b-441b-8bcb-883e3f2a4c1a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ccc8920f7df788b4df355b0cbc23478e97111d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955627"
---
# <a name="winrm-plug-in-api"></a><span data-ttu-id="a617d-103">API del plug-in WinRM</span><span class="sxs-lookup"><span data-stu-id="a617d-103">WinRM Plug-in API</span></span>

<span data-ttu-id="a617d-104">I plug-in Gestione remota Windows sono librerie di collegamento dinamico (dll) native che consentono di collegare ed estendere le funzionalità di WinRM.</span><span class="sxs-lookup"><span data-stu-id="a617d-104">Windows Remote Management plug-ins are native dynamic-link libraries (DLLs) that plug into and extend the functionality of WinRM.</span></span> <span data-ttu-id="a617d-105">Il plug-in WinRM Application Programming Interface (API) fornisce funzionalità che consentono a un utente di scrivere plug-in implementando determinate API per le operazioni e gli [*URI delle risorse*](windows-remote-management-glossary.md) supportati.</span><span class="sxs-lookup"><span data-stu-id="a617d-105">The WinRM Plug-in application programming interface (API) provides functionality that enables a user to write plug-ins by implementing certain APIs for supported [*resource URIs*](windows-remote-management-glossary.md) and operations.</span></span> <span data-ttu-id="a617d-106">Una volta configurati i plug-in per il servizio WinRM o Internet Information Services (IIS), vengono caricati rispettivamente nell'host WinRM o nell'host IIS.</span><span class="sxs-lookup"><span data-stu-id="a617d-106">After the plug-ins are configured for either the WinRM service or Internet Information Services (IIS), they are loaded into the WinRM host or IIS host, respectively.</span></span> <span data-ttu-id="a617d-107">Le richieste remote vengono instradate a questi punti di ingresso plug-in per eseguire le operazioni.</span><span class="sxs-lookup"><span data-stu-id="a617d-107">Remote requests are routed to these plug-in entry points to carry out operations.</span></span>

<span data-ttu-id="a617d-108">La sezione di riferimento dell'API del plug-in WinRM contiene informazioni dettagliate sugli elementi API seguenti:</span><span class="sxs-lookup"><span data-stu-id="a617d-108">The WinRM Plug-in API reference section contains detailed information about the following API elements:</span></span>

-   [<span data-ttu-id="a617d-109">Punti di ingresso del plug-in di autorizzazione</span><span class="sxs-lookup"><span data-stu-id="a617d-109">Authorization Plug-in Entry Points</span></span>](authorization-plug-in-entry-points.md)
-   [<span data-ttu-id="a617d-110">Metodi plug-in di autorizzazione</span><span class="sxs-lookup"><span data-stu-id="a617d-110">Authorization Plug-in Methods</span></span>](authorization-plug-in-methods.md)
-   [<span data-ttu-id="a617d-111">Punti di ingresso del plug-in per le operazioni</span><span class="sxs-lookup"><span data-stu-id="a617d-111">Operations Plug-in Entry Points</span></span>](operations-plug-in-entry-points.md)
-   [<span data-ttu-id="a617d-112">Metodi del plug-in per le operazioni</span><span class="sxs-lookup"><span data-stu-id="a617d-112">Operations Plug-in Methods</span></span>](operations-plug-in-methods.md)
-   [<span data-ttu-id="a617d-113">Strutture</span><span class="sxs-lookup"><span data-stu-id="a617d-113">Structures</span></span>](winrm-plug-in-api-structures.md)

 

 




