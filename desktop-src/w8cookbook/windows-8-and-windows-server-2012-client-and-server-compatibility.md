---
title: Compatibilità con client e server-Windows 8
description: Compatibilità tra client e server di Windows 8 e Windows Server 2012
ms.assetid: 5067219A-EBA2-4FAF-8C17-7AB22C5EADD0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca5b685ae10b97a7b8197737944ea7231d226514
ms.sourcegitcommit: 477b1efe7d9c2f91d5f2ac588a20edf348b1c734
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2019
ms.locfileid: "104335919"
---
# <a name="windows-8-and-windows-server-2012-client-and-server-compatibility"></a><span data-ttu-id="f95d1-103">Compatibilità tra client e server di Windows 8 e Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f95d1-103">Windows 8 and Windows Server 2012 client and server compatibility</span></span>

<span data-ttu-id="f95d1-104">In questa sezione vengono descritte le modifiche apportate al sistema operativo a cui è necessario prestare particolare attenzione a causa del potenziale impatto sulle app esistenti e del modo in cui le nuove app devono essere progettate nei client, nei server o nei client e nei server.</span><span class="sxs-lookup"><span data-stu-id="f95d1-104">This section describes changes in the operating system that you should pay special attention to due to the potential impacts on existing apps and how new apps should be designed on clients, on servers, or on both clients and servers.</span></span> <span data-ttu-id="f95d1-105">Di seguito è riportato l'elenco degli argomenti trattati in questa sezione, raggruppati per area funzionale:</span><span class="sxs-lookup"><span data-stu-id="f95d1-105">Following is the list of topics covered in this section, grouped by feature area:</span></span>

<span data-ttu-id="f95d1-106">**AppCompat**</span><span class="sxs-lookup"><span data-stu-id="f95d1-106">**AppCompat**</span></span>

-   <span data-ttu-id="f95d1-107">Aggiornamento delle regole di rilevamento delle app di sicurezza</span><span class="sxs-lookup"><span data-stu-id="f95d1-107">Security app detection rules update</span></span>
-   <span data-ttu-id="f95d1-108">Determinazione dello stato dello shim</span><span class="sxs-lookup"><span data-stu-id="f95d1-108">Determining shim status</span></span>
-   <span data-ttu-id="f95d1-109">Le app Server devono poter essere eseguite senza la shell grafica server</span><span class="sxs-lookup"><span data-stu-id="f95d1-109">Server apps must be able to run without the Server Graphical Shell</span></span>
-   <span data-ttu-id="f95d1-110">Componenti server RDS rimossi da Windows 8</span><span class="sxs-lookup"><span data-stu-id="f95d1-110">RDS server components are removed from Windows 8</span></span>
-   <span data-ttu-id="f95d1-111">Modello di tipo di file e associazioni di protocollo</span><span class="sxs-lookup"><span data-stu-id="f95d1-111">File type and protocol associations model</span></span>
-   <span data-ttu-id="f95d1-112">Desktop Activity Moderator</span><span class="sxs-lookup"><span data-stu-id="f95d1-112">Desktop Activity Moderator</span></span>
-   <span data-ttu-id="f95d1-113">.NET Framework 4,5 è il valore predefinito e .NET Framework 3,5 è facoltativo</span><span class="sxs-lookup"><span data-stu-id="f95d1-113">.NET Framework 4.5 is default and .NET Framework 3.5 is optional</span></span>
-   <span data-ttu-id="f95d1-114">Le applicazioni desktop potrebbero non essere visibili dopo l'avvio del Web browser predefinito</span><span class="sxs-lookup"><span data-stu-id="f95d1-114">Desktop apps may not be visible after launching the default web browser</span></span>
-   <span data-ttu-id="f95d1-115">Modalità a contrasto elevato</span><span class="sxs-lookup"><span data-stu-id="f95d1-115">High-contrast mode</span></span>
-   <span data-ttu-id="f95d1-116">Manifesto app (eseguibile)</span><span class="sxs-lookup"><span data-stu-id="f95d1-116">App (executable) manifest</span></span>
-   <span data-ttu-id="f95d1-117">Il modello presente in coda verrà deprecato</span><span class="sxs-lookup"><span data-stu-id="f95d1-117">Queued present model is being deprecated</span></span>
-   <span data-ttu-id="f95d1-118">Scenari di compatibilità dei programmi per Windows 8</span><span class="sxs-lookup"><span data-stu-id="f95d1-118">Program Compatibility Assistant scenarios for Windows 8</span></span>
-   <span data-ttu-id="f95d1-119">Gadget desktop rimossi</span><span class="sxs-lookup"><span data-stu-id="f95d1-119">Desktop gadgets removed</span></span>

<span data-ttu-id="f95d1-120">**Archiviazione e file System**</span><span class="sxs-lookup"><span data-stu-id="f95d1-120">**Storage and File System**</span></span>

-   <span data-ttu-id="f95d1-121">Aggiornamento della compatibilità del disco con formato avanzato (4K)</span><span class="sxs-lookup"><span data-stu-id="f95d1-121">Advanced format (4K) disk compatibility update</span></span>
-   <span data-ttu-id="f95d1-122">Thin provisioning di unità logiche</span><span class="sxs-lookup"><span data-stu-id="f95d1-122">Thin provisioning of logical units</span></span>
-   <span data-ttu-id="f95d1-123">Archiviazione avanzata è ora facoltativa per Ambiente preinstallazione di Windows (WinPE) e SKU del server</span><span class="sxs-lookup"><span data-stu-id="f95d1-123">Enhanced storage is now optional for Windows Preinstallation Environment (WinPE) and server SKU</span></span>
-   <span data-ttu-id="f95d1-124">Il servizio dischi virtuali sta passando all'API di gestione dell'archiviazione di Windows basata su Strumentazione gestione Windows (WMI)</span><span class="sxs-lookup"><span data-stu-id="f95d1-124">Virtual Disk Service is transitioning to the Windows Management Instrumentation (WMI)-based Windows Storage Management API</span></span>
-   <span data-ttu-id="f95d1-125">Interfaccia utente delle versioni precedenti rimosse per i volumi locali</span><span class="sxs-lookup"><span data-stu-id="f95d1-125">Previous versions UI removed for local volumes</span></span>
-   <span data-ttu-id="f95d1-126">StorAHCI sostituisce MSAHCI</span><span class="sxs-lookup"><span data-stu-id="f95d1-126">StorAHCI replaces MSAHCI</span></span>
-   <span data-ttu-id="f95d1-127">Backup e ripristino di Windows 7 deprecato</span><span class="sxs-lookup"><span data-stu-id="f95d1-127">Windows 7 backup and restore deprecated</span></span>
-   <span data-ttu-id="f95d1-128">Trasferimenti dati scaricati</span><span class="sxs-lookup"><span data-stu-id="f95d1-128">Offloaded data transfers</span></span>

<span data-ttu-id="f95d1-129">**Altri**</span><span class="sxs-lookup"><span data-stu-id="f95d1-129">**Other**</span></span>

-   <span data-ttu-id="f95d1-130">Gestione finestre desktop è sempre attiva</span><span class="sxs-lookup"><span data-stu-id="f95d1-130">Desktop Window Manager is always on</span></span>
-   <span data-ttu-id="f95d1-131">Direct2D non supporta il rendering in metafile "avanzati" in Internet Explorer 9</span><span class="sxs-lookup"><span data-stu-id="f95d1-131">Direct2D does not support rendering to "rich" metafiles in Internet Explorer 9</span></span>
-   <span data-ttu-id="f95d1-132">Modifiche al supporto hardware legacy di DX9</span><span class="sxs-lookup"><span data-stu-id="f95d1-132">Changes in DX9 legacy hardware support</span></span>
-   <span data-ttu-id="f95d1-133">MSAA non è disponibile per le app di Windows Store</span><span class="sxs-lookup"><span data-stu-id="f95d1-133">MSAA is not available to Windows Store apps</span></span>
-   <span data-ttu-id="f95d1-134">La porta 3 è deprecata per i driver NDIS 6,30</span><span class="sxs-lookup"><span data-stu-id="f95d1-134">Port 3 is deprecated for NDIS 6.30 drivers</span></span>

 

 
