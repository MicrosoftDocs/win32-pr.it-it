---
title: HTTP.sys gestibilità in Windows Vista e Windows Server 2008
description: Con Windows Vista e Windows Server 2008, i professionisti IT troveranno funzionalità di gestibilità migliorate per il componente API server HTTP, oltre al supporto per la registrazione HTTP introdotto in Windows Server 2003.
ms.assetid: c5fc006c-e50d-49e8-8835-faa0732b7d88
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 790dd8ad7429d13d89c6f3a59c0c2c2efc8c554e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221140"
---
# <a name="httpsys-manageability-in-windows-vista-and-windows-server-2008"></a><span data-ttu-id="d218b-103">HTTP.sys gestibilità in Windows Vista e Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d218b-103">HTTP.sys Manageability in Windows Vista and Windows Server 2008</span></span>

<span data-ttu-id="d218b-104">Con Windows Vista e Windows Server 2008, i professionisti IT troveranno funzionalità di gestibilità migliorate per il componente API server HTTP, oltre al supporto per la registrazione HTTP introdotto in Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="d218b-104">With Windows Vista and Windows Server 2008, IT professionals will find improved manageability functionality for the HTTP Server API component, in addition to the HTTP logging support introduced in Windows Server 2003.</span></span> <span data-ttu-id="d218b-105">Per diagnosticare e configurare il componente API server HTTP, i professionisti IT possono usare tre strumenti:</span><span class="sxs-lookup"><span data-stu-id="d218b-105">To diagnose and configure the HTTP Server API component, IT professionals can use three tools:</span></span>

-   <span data-ttu-id="d218b-106">Nuova funzionalità di traccia ETW</span><span class="sxs-lookup"><span data-stu-id="d218b-106">New ETW tracing functionality</span></span>
-   <span data-ttu-id="d218b-107">Contatori delle prestazioni</span><span class="sxs-lookup"><span data-stu-id="d218b-107">Performance counters</span></span>
-   <span data-ttu-id="d218b-108">Comandi di configurazione netsh</span><span class="sxs-lookup"><span data-stu-id="d218b-108">Netsh configuration commands</span></span>

<span data-ttu-id="d218b-109">L'API server HTTP consente alle applicazioni di comunicare tramite HTTP e include il supporto SSL, in modo che le applicazioni possano scambiare dati tramite connessioni HTTP protette.</span><span class="sxs-lookup"><span data-stu-id="d218b-109">The HTTP Server API enables applications to communicate over HTTP and includes SSL support so that applications can exchange data over secure HTTP connections.</span></span> <span data-ttu-id="d218b-110">L'API server HTTP è supportata nei sistemi operativi Windows Server 2003 e in Windows XP SP2.</span><span class="sxs-lookup"><span data-stu-id="d218b-110">The HTTP Server API is supported on the Windows Server 2003 operating systems, and on Windows XP SP2.</span></span>

<span data-ttu-id="d218b-111">Vedere le sezioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="d218b-111">See the following sections:</span></span>

-   [<span data-ttu-id="d218b-112"> Scenari di gestibilitàHTTP.sys</span><span class="sxs-lookup"><span data-stu-id="d218b-112">HTTP.sys Manageability Scenarios</span></span>](http-sys-manageability-scenarios.md)
-   [<span data-ttu-id="d218b-113">Comandi Netsh per HTTP</span><span class="sxs-lookup"><span data-stu-id="d218b-113">Netsh commands for HTTP</span></span>](netsh-commands-for-http.md)
-   [<span data-ttu-id="d218b-114">Convenzioni di formattazione</span><span class="sxs-lookup"><span data-stu-id="d218b-114">Formatting Legend</span></span>](formatting-legend.md)

 

 




