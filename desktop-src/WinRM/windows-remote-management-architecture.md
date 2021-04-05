---
title: Architettura Gestione remota Windows
description: L'architettura Gestione remota Windows è costituita da componenti nei computer client e server.
ms.assetid: 82e67851-fe46-4bb0-8278-9718b5e0c7ae
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0f5576913c5e4a1f2a105fb77e2282dc682c6659
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729186"
---
# <a name="windows-remote-management-architecture"></a><span data-ttu-id="5858d-103">Architettura Gestione remota Windows</span><span class="sxs-lookup"><span data-stu-id="5858d-103">Windows Remote Management Architecture</span></span>

<span data-ttu-id="5858d-104">L'architettura Gestione remota Windows è costituita da componenti nei computer client e server.</span><span class="sxs-lookup"><span data-stu-id="5858d-104">The Windows Remote Management architecture consists of components on the client and server computers.</span></span> <span data-ttu-id="5858d-105">Nella figura seguente sono illustrati i componenti di entrambi i computer, il modo in cui i componenti interagiscono con altri componenti e il protocollo utilizzato per la comunicazione tra i computer.</span><span class="sxs-lookup"><span data-stu-id="5858d-105">The following illustration shows the components on both computers, how the components interact with other components, and the protocol that is used to communicate between the computers.</span></span>

![architettura WinRM](images/winrm-architecture.png)

## <a name="requesting-client"></a><span data-ttu-id="5858d-107">Client richiedente</span><span class="sxs-lookup"><span data-stu-id="5858d-107">Requesting Client</span></span>

<span data-ttu-id="5858d-108">I componenti WinRM seguenti si trovano nel computer in cui è in esecuzione lo script che richiede i dati.</span><span class="sxs-lookup"><span data-stu-id="5858d-108">The following WinRM components reside on the computer that is running the script that requests data.</span></span>

-   <span data-ttu-id="5858d-109">Applicazione WinRM</span><span class="sxs-lookup"><span data-stu-id="5858d-109">WinRM application</span></span>

    <span data-ttu-id="5858d-110">Questo è lo script o lo strumento da riga di comando **WinRM** che utilizza l'API di scripting WinRM per effettuare chiamate ai dati della richiesta o per eseguire metodi.</span><span class="sxs-lookup"><span data-stu-id="5858d-110">This is the script or **Winrm** command-line tool that uses the WinRM scripting API to make calls to request data or to execute methods.</span></span> <span data-ttu-id="5858d-111">Per ulteriori informazioni, vedere l' [API di scripting WinRM](winrm-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="5858d-111">For more information, see the [WinRM Scripting API](winrm-scripting-api.md).</span></span>

-   <span data-ttu-id="5858d-112">WSMAuto.dll</span><span class="sxs-lookup"><span data-stu-id="5858d-112">WSMAuto.dll</span></span>

    <span data-ttu-id="5858d-113">Livello di automazione che fornisce supporto per gli script.</span><span class="sxs-lookup"><span data-stu-id="5858d-113">The Automation layer that provides scripting support.</span></span>

-   <span data-ttu-id="5858d-114">WsmCL.dll</span><span class="sxs-lookup"><span data-stu-id="5858d-114">WsmCL.dll</span></span>

    <span data-ttu-id="5858d-115">Livello API C all'interno del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="5858d-115">C API layer within the operating system.</span></span>

-   <span data-ttu-id="5858d-116">API HTTP</span><span class="sxs-lookup"><span data-stu-id="5858d-116">HTTP API</span></span>

    <span data-ttu-id="5858d-117">WinRM richiede il supporto per il trasporto HTTP e HTTPS.</span><span class="sxs-lookup"><span data-stu-id="5858d-117">WinRM requires support for HTTP and HTTPS transport.</span></span>

## <a name="responding-server"></a><span data-ttu-id="5858d-118">Server di risposta</span><span class="sxs-lookup"><span data-stu-id="5858d-118">Responding Server</span></span>

<span data-ttu-id="5858d-119">I componenti WinRM seguenti risiedono nel computer che risponde.</span><span class="sxs-lookup"><span data-stu-id="5858d-119">The following WinRM components reside on the responding computer.</span></span>

-   <span data-ttu-id="5858d-120">API HTTP</span><span class="sxs-lookup"><span data-stu-id="5858d-120">HTTP API</span></span>

    <span data-ttu-id="5858d-121">WinRM richiede il supporto per il trasporto HTTP e HTTPS.</span><span class="sxs-lookup"><span data-stu-id="5858d-121">WinRM requires support for HTTP and HTTPS transport.</span></span>

-   <span data-ttu-id="5858d-122">WSMAuto.dll</span><span class="sxs-lookup"><span data-stu-id="5858d-122">WSMAuto.dll</span></span>

    <span data-ttu-id="5858d-123">Livello di automazione che fornisce supporto per gli script.</span><span class="sxs-lookup"><span data-stu-id="5858d-123">The Automation layer that provides scripting support.</span></span>

-   <span data-ttu-id="5858d-124">WsmCL.dll</span><span class="sxs-lookup"><span data-stu-id="5858d-124">WsmCL.dll</span></span>

    <span data-ttu-id="5858d-125">Livello API C all'interno del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="5858d-125">C API layer within the operating system.</span></span>

-   <span data-ttu-id="5858d-126">WsmSvc.dll</span><span class="sxs-lookup"><span data-stu-id="5858d-126">WsmSvc.dll</span></span>

    <span data-ttu-id="5858d-127">Servizio [*listener*](windows-remote-management-glossary.md) WinRM.</span><span class="sxs-lookup"><span data-stu-id="5858d-127">WinRM [*listener*](windows-remote-management-glossary.md) service.</span></span>

-   <span data-ttu-id="5858d-128">WsmProv.dll</span><span class="sxs-lookup"><span data-stu-id="5858d-128">WsmProv.dll</span></span>

    <span data-ttu-id="5858d-129">Sottosistema del provider.</span><span class="sxs-lookup"><span data-stu-id="5858d-129">Provider subsystem.</span></span>

-   <span data-ttu-id="5858d-130">WsmRes.dll</span><span class="sxs-lookup"><span data-stu-id="5858d-130">WsmRes.dll</span></span>

    <span data-ttu-id="5858d-131">File di risorse.</span><span class="sxs-lookup"><span data-stu-id="5858d-131">Resource file.</span></span>

-   <span data-ttu-id="5858d-132">WsmWmiPl.dll</span><span class="sxs-lookup"><span data-stu-id="5858d-132">WsmWmiPl.dll</span></span>

    <span data-ttu-id="5858d-133">[*Plug-in WMI*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="5858d-133">[*WMI plug-in*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="5858d-134">In questo modo è possibile ottenere dati WMI tramite WinRM.</span><span class="sxs-lookup"><span data-stu-id="5858d-134">This allows you to obtain WMI data through WinRM.</span></span>

-   <span data-ttu-id="5858d-135">Driver IPMI (Intelligent Platform Management Interface) e provider IPMI WMI</span><span class="sxs-lookup"><span data-stu-id="5858d-135">Intelligent Platform Management Interface (IPMI) driver and WMI IPMI provider</span></span>

    <span data-ttu-id="5858d-136">Questi componenti forniscono tutti i dati hardware richiesti usando le classi IPMI.</span><span class="sxs-lookup"><span data-stu-id="5858d-136">These components supply any hardware data that is requested using the IPMI classes.</span></span> <span data-ttu-id="5858d-137">Per ulteriori informazioni, vedere [provider IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider).</span><span class="sxs-lookup"><span data-stu-id="5858d-137">For more information, see [IPMI Provider](/previous-versions/windows/desktop/ipmiprv/ipmi-provider).</span></span> <span data-ttu-id="5858d-138">L'hardware BMC deve essere stato rilevato da SMBIOS o dal dispositivo creato manualmente mediante il caricamento del driver.</span><span class="sxs-lookup"><span data-stu-id="5858d-138">BMC hardware must have been detected by the SMBIOS or the device created manually by loading the driver.</span></span> <span data-ttu-id="5858d-139">Per ulteriori informazioni, vedere [installazione e configurazione per gestione remota Windows](installation-and-configuration-for-windows-remote-management.md).</span><span class="sxs-lookup"><span data-stu-id="5858d-139">For more information, see [Installation and Configuration for Windows Remote Management](installation-and-configuration-for-windows-remote-management.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5858d-140">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5858d-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5858d-141">Informazioni su Gestione remota Windows</span><span class="sxs-lookup"><span data-stu-id="5858d-141">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> </dl>

 

 