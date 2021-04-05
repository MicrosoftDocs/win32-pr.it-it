---
title: API di HTTP Server
description: L'API server HTTP consente alle applicazioni di comunicare tramite HTTP senza utilizzare Microsoft Internet Information Server (IIS).
ms.assetid: ef18716c-7511-4c8a-99bc-28369c3e46f4
keywords:
- API di HTTP Server
- API server HTTP, pagina iniziale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8f99045b24d0ef79c267615791c62da50ed8e40
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104117734"
---
# <a name="http-server-api"></a><span data-ttu-id="5776f-105">API di HTTP Server</span><span class="sxs-lookup"><span data-stu-id="5776f-105">HTTP Server API</span></span>

## <a name="purpose"></a><span data-ttu-id="5776f-106">Scopo</span><span class="sxs-lookup"><span data-stu-id="5776f-106">Purpose</span></span>

<span data-ttu-id="5776f-107">L'API server HTTP consente alle applicazioni di comunicare tramite HTTP senza utilizzare Microsoft Internet Information Server (IIS).</span><span class="sxs-lookup"><span data-stu-id="5776f-107">The HTTP Server API enables applications to communicate over HTTP without using Microsoft Internet Information Server (IIS).</span></span> <span data-ttu-id="5776f-108">Le applicazioni possono eseguire la registrazione per ricevere richieste HTTP per URL specifici, ricevere richieste HTTP e inviare risposte HTTP.</span><span class="sxs-lookup"><span data-stu-id="5776f-108">Applications can register to receive HTTP requests for particular URLs, receive HTTP requests, and send HTTP responses.</span></span> <span data-ttu-id="5776f-109">L'API server HTTP include il supporto SSL, in modo che le applicazioni possano scambiare dati tramite connessioni HTTP sicure senza IIS.</span><span class="sxs-lookup"><span data-stu-id="5776f-109">The HTTP Server API includes SSL support so that applications can exchange data over secure HTTP connections without IIS.</span></span> <span data-ttu-id="5776f-110">È anche progettato per funzionare con le porte di completamento I/O.</span><span class="sxs-lookup"><span data-stu-id="5776f-110">It is also designed to work with I/O completion ports.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="5776f-111">Sviluppatori</span><span class="sxs-lookup"><span data-stu-id="5776f-111">Developer audience</span></span>

<span data-ttu-id="5776f-112">Questa API è progettata per l'uso da programmatori C/C++.</span><span class="sxs-lookup"><span data-stu-id="5776f-112">This API is designed for use by C/C++ programmers.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="5776f-113">Requisiti di runtime</span><span class="sxs-lookup"><span data-stu-id="5776f-113">Run-time requirements</span></span>

<span data-ttu-id="5776f-114">L'API server HTTP è supportata nei sistemi operativi Windows Server 2003 e in Windows XP con Service Pack 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="5776f-114">The HTTP Server API is supported on Windows Server 2003 operating systems and on Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="5776f-115">Tenere presente che Microsoft IIS 5 in esecuzione su Windows XP con SP2 non è in grado di condividere la porta 80 con altre applicazioni HTTP eseguite simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="5776f-115">Be aware that Microsoft IIS 5 running on Windows XP with SP2 is not able to share port 80 with other HTTP applications running simultaneously.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="5776f-116">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="5776f-116">In this section</span></span>



| <span data-ttu-id="5776f-117">Argomento</span><span class="sxs-lookup"><span data-stu-id="5776f-117">Topic</span></span>                                                                           | <span data-ttu-id="5776f-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5776f-118">Description</span></span>                                                                                             |
|---------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5776f-119">Informazioni sull'API server HTTP</span><span class="sxs-lookup"><span data-stu-id="5776f-119">About HTTP Server API</span></span>](about-http-server-api.md)<br/>                   | <span data-ttu-id="5776f-120">Informazioni generali sul protocollo HTTP.</span><span class="sxs-lookup"><span data-stu-id="5776f-120">General information about HTTP.</span></span><br/>                                                              |
| [<span data-ttu-id="5776f-121">Uso dell'API server HTTP</span><span class="sxs-lookup"><span data-stu-id="5776f-121">Using HTTP Server API</span></span>](using-http-server-api.md)<br/>                   | <span data-ttu-id="5776f-122">Guida procedurale per l'utilizzo di HTTP.</span><span class="sxs-lookup"><span data-stu-id="5776f-122">Procedural guide for using HTTP.</span></span><br/>                                                             |
| [<span data-ttu-id="5776f-123">Riferimento all'API del server HTTP</span><span class="sxs-lookup"><span data-stu-id="5776f-123">HTTP Server API Reference</span></span>](http-server-api-reference.md)<br/>           | <span data-ttu-id="5776f-124">Documentazione di funzioni, strutture e tipi di enumerazione specifici disponibili in HTTP.</span><span class="sxs-lookup"><span data-stu-id="5776f-124">Documentation of specific functions, structures, and enumeration types available in HTTP.</span></span><br/>    |
| [<span data-ttu-id="5776f-125">Applicazione di esempio server HTTP</span><span class="sxs-lookup"><span data-stu-id="5776f-125">HTTP Server Sample Application</span></span>](http-server-sample-application.md)<br/> | <span data-ttu-id="5776f-126">Applicazione di esempio in cui viene illustrato come utilizzare l'API del server HTTP per eseguire attività lato server.</span><span class="sxs-lookup"><span data-stu-id="5776f-126">A sample application that shows how to use the HTTP Server API to perform server-side tasks.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="5776f-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5776f-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5776f-128">Servizi HTTP di Windows (WinHTTP)</span><span class="sxs-lookup"><span data-stu-id="5776f-128">Windows HTTP Services (WinHTTP)</span></span>](/windows/desktop/WinHttp/winhttp-start-page)
</dt> </dl>

 

