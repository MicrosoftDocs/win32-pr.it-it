---
title: Servizi di distribuzione Windows
description: Distribuire i sistemi operativi Windows. Configurare nuovi client con un'installazione basata sulla rete senza richiedere agli amministratori di visitare ogni computer o di installarli direttamente da supporti CD o DVD.
ms.assetid: 790abc27-03cc-4f93-bf04-a4eb37e614bb
keywords:
- Servizi di distribuzione Windows servizi di distribuzione Windows
- Servizi di distribuzione Windows servizi di distribuzione Windows, home page
- Servizi di distribuzione Windows servizi di distribuzione
- Servizi di distribuzione Windows WDS vedere Servizi di distribuzione Windows
- Servizi di installazione remota servizi di distribuzione Windows vedere Servizi di distribuzione Windows
- Servizi di distribuzione Windows RIS vedere Servizi di distribuzione Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b35bebb000b383552f12d259ca17552165e9247f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300358"
---
# <a name="windows-deployment-services"></a><span data-ttu-id="aa4ec-110">Servizi di distribuzione Windows</span><span class="sxs-lookup"><span data-stu-id="aa4ec-110">Windows Deployment Services</span></span>

## <a name="purpose"></a><span data-ttu-id="aa4ec-111">Scopo</span><span class="sxs-lookup"><span data-stu-id="aa4ec-111">Purpose</span></span>

<span data-ttu-id="aa4ec-112">Servizi di distribuzione Windows (WDS) è la versione aggiornata di servizi di installazione remota (RIS).</span><span class="sxs-lookup"><span data-stu-id="aa4ec-112">Windows Deployment Services (WDS) is the revised version of Remote Installation Services (RIS).</span></span> <span data-ttu-id="aa4ec-113">WDS consente la distribuzione dei sistemi operativi Windows.</span><span class="sxs-lookup"><span data-stu-id="aa4ec-113">WDS enables the deployment of Windows operating systems.</span></span> <span data-ttu-id="aa4ec-114">È possibile utilizzare WDS per configurare nuovi client con un'installazione basata su rete senza richiedere agli amministratori di visitare ogni computer o di installare direttamente da supporti CD o DVD.</span><span class="sxs-lookup"><span data-stu-id="aa4ec-114">You can use WDS to set up new clients with a network-based installation without requiring that administrators visit each computer or install directly from CD or DVD media.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="aa4ec-115">Sviluppatori</span><span class="sxs-lookup"><span data-stu-id="aa4ec-115">Developer audience</span></span>

<span data-ttu-id="aa4ec-116">Il principale pubblico per gli sviluppatori dell'API WDS è costituito dai gruppi che sviluppano strumenti e processi personalizzati per l'IT e altri gruppi di amministrazione del computer.</span><span class="sxs-lookup"><span data-stu-id="aa4ec-116">The primary developer audience of the WDS API is for groups that develop custom tools and processes for IT and other computer administration groups.</span></span> <span data-ttu-id="aa4ec-117">Negli ambienti in cui non è possibile usare la soluzione standard di servizi di distribuzione Windows (WDS), l'API WDS consente l'accesso programmatico ad alcuni componenti di WDS.</span><span class="sxs-lookup"><span data-stu-id="aa4ec-117">In environments where the standard Windows Deployment Services (WDS) solution cannot be used, the WDS API enables programmatic access to some WDS components.</span></span>

<span data-ttu-id="aa4ec-118">Original Equipment Manufacturer (OEM), System Builder e professionisti IT aziendali che cercano informazioni su come distribuire Windows in nuovi computer, dovrebbero visualizzare le informazioni sulla soluzione Servizi di distribuzione Windows (WDS) standard nella [Guida dettagliata all'aggiornamento di servizi di distribuzione Windows](/previous-versions/windows/it-pro/windows-vista/cc766320(v=ws.10)) e [Windows Automated Installation Kit (WAIK)](https://www.microsoft.com/download/details.aspx?id=10333).</span><span class="sxs-lookup"><span data-stu-id="aa4ec-118">Original Equipment Manufacturers (OEMs), system builders, and corporate IT professionals looking for information on how to deploy Windows onto new computers, should see the information about the standard Windows Deployment Services (WDS) solution in the [Windows Deployment Services Update Step-by-Step Guide](/previous-versions/windows/it-pro/windows-vista/cc766320(v=ws.10)) and the [Windows Automated Installation Kit (WAIK)](https://www.microsoft.com/download/details.aspx?id=10333).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="aa4ec-119">Requisiti di runtime</span><span class="sxs-lookup"><span data-stu-id="aa4ec-119">Run-time requirements</span></span>

<span data-ttu-id="aa4ec-120">WDS è disponibile come componente aggiuntivo per Windows Server 2003 con Service Pack 1 (SP1) ed è incluso nel sistema operativo a partire da Windows Server 2003 con Service Pack 2 (SP2) e Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="aa4ec-120">WDS is available as an add-on for Windows Server 2003 with Service Pack 1 (SP1) and is included in the operating system starting with Windows Server 2003 with Service Pack 2 (SP2) and Windows Server 2008.</span></span> <span data-ttu-id="aa4ec-121">L'API del server PXE WDS richiede il ruolo server WDS nel server per implementare i provider PXE personalizzati.</span><span class="sxs-lookup"><span data-stu-id="aa4ec-121">The WDS PXE Server API requires the WDS server role on the server to implement custom PXE providers.</span></span> <span data-ttu-id="aa4ec-122">Per l'API client WDS è necessaria la fase di elaborazione del programma di installazione di Microsoft Ambiente preinstallazione di Windows (Windows PE 2,0).</span><span class="sxs-lookup"><span data-stu-id="aa4ec-122">The WDS Client API requires the Microsoft Windows Preinstallation Environment (Windows PE 2.0) phase of setup processing.</span></span> <span data-ttu-id="aa4ec-123">Immagine di avvio RAMDISK di Windows PE 2,0 in. Per implementare client WDS personalizzati, è necessario scaricare il formato WIM come parte del processo di avvio di rete.</span><span class="sxs-lookup"><span data-stu-id="aa4ec-123">A RAMDISK bootable image of Windows PE 2.0 in the .WIM format must be downloaded as part of the network boot process to implement custom WDS clients.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="aa4ec-124">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="aa4ec-124">In this section</span></span>



| <span data-ttu-id="aa4ec-125">Argomento</span><span class="sxs-lookup"><span data-stu-id="aa4ec-125">Topic</span></span>                                                                                                 | <span data-ttu-id="aa4ec-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aa4ec-126">Description</span></span>                                                                    |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="aa4ec-127">Informazioni sull'API di servizi di distribuzione Windows</span><span class="sxs-lookup"><span data-stu-id="aa4ec-127">About the Windows Deployment Services API</span></span>](about-the-windows-deployment-services-api.md)<br/> | <span data-ttu-id="aa4ec-128">Informazioni generali sull'API del server WDS e sull'API client WDS.</span><span class="sxs-lookup"><span data-stu-id="aa4ec-128">General information about the WDS Server API and WDS Client API.</span></span><br/>    |
| [<span data-ttu-id="aa4ec-129">Guida di riferimento a servizi di distribuzione Windows</span><span class="sxs-lookup"><span data-stu-id="aa4ec-129">Windows Deployment Services Reference</span></span>](windows-deployment-services-reference.md)<br/>         | <span data-ttu-id="aa4ec-130">Vengono descritte le funzioni e le strutture di servizi di distribuzione Windows.</span><span class="sxs-lookup"><span data-stu-id="aa4ec-130">Describes the Windows Deployment Services functions and structures.</span></span><br/> |



 

 

