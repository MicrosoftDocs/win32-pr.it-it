---
title: Servizio trasferimento intelligente in background
description: Servizio trasferimento intelligente in background (BITS) consente di trasferire file (download o caricamenti) tra un client e un server e offre informazioni sullo stato correlate ai trasferimenti.
ms.assetid: ce91f87c-8273-4a1c-99e0-ef55e2a50334
keywords:
- Servizio trasferimento intelligente in background
- Servizio trasferimento intelligente in background, pagina iniziale
- BITS (vedere Servizio trasferimento intelligente in background)
- download dei bit di file
- BIT di trasferimento file in background
- caricamento di bit di file
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: a531821665490735b391ab2714f5b37146c6bc1e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963330"
---
# <a name="background-intelligent-transfer-service"></a><span data-ttu-id="8ce0e-109">Servizio trasferimento intelligente in background</span><span class="sxs-lookup"><span data-stu-id="8ce0e-109">Background Intelligent Transfer Service</span></span>

## <a name="purpose"></a><span data-ttu-id="8ce0e-110">Scopo</span><span class="sxs-lookup"><span data-stu-id="8ce0e-110">Purpose</span></span>

<span data-ttu-id="8ce0e-111">Servizio trasferimento intelligente in background (BITS) viene usato dai programmatori e dagli amministratori di sistema per scaricare file o caricare file in server Web HTTP e condivisioni file SMB.</span><span class="sxs-lookup"><span data-stu-id="8ce0e-111">Background Intelligent Transfer Service (BITS) is used by programmers and system administrators to download files from or upload files to HTTP web servers and SMB file shares.</span></span> <span data-ttu-id="8ce0e-112">BITS prenderà in considerazione il costo del trasferimento e l'utilizzo della rete, in modo che il lavoro in primo piano dell'utente abbia il minor impatto possibile.</span><span class="sxs-lookup"><span data-stu-id="8ce0e-112">BITS will take the cost of the transfer into consideration, as well as the network usage so that the user's foreground work has as little impact as possible.</span></span> <span data-ttu-id="8ce0e-113">BITS gestisce anche il interuptions di rete, la sospensione e la ripresa automatica di trasferimenti, anche dopo un riavvio.</span><span class="sxs-lookup"><span data-stu-id="8ce0e-113">BITS also handles network interuptions, pausing and automatically resuming transfers, even after a reboot.</span></span> <span data-ttu-id="8ce0e-114">BITS include i cmdlet di PowerShell per la creazione e la gestione dei trasferimenti, nonché l'utilità della riga di comando BitsAdmin.</span><span class="sxs-lookup"><span data-stu-id="8ce0e-114">BITS includes PowerShell cmdlets for creating and managing transfers as well as the BitsAdmin command-line utility.</span></span>

> [!Note]  
> <span data-ttu-id="8ce0e-115">BITS può essere usato da Windows per scaricare gli aggiornamenti nel sistema locale.</span><span class="sxs-lookup"><span data-stu-id="8ce0e-115">BITS can be used by Windows to download updates to your local system.</span></span> <span data-ttu-id="8ce0e-116">Se si è un utente finale che cerca modi per risolvere i problemi di installazione BITS, vedere [risolvere i problemi di Windows Update](https://support.microsoft.com/help/10164/fix-windows-update-errors).</span><span class="sxs-lookup"><span data-stu-id="8ce0e-116">If you are an end-user searching for ways to troubleshoot your BITS installation, see [Fix Windows Update Issues](https://support.microsoft.com/help/10164/fix-windows-update-errors).</span></span> 
 

## <a name="where-applicable"></a><span data-ttu-id="8ce0e-117">Se applicabile</span><span class="sxs-lookup"><span data-stu-id="8ce0e-117">Where applicable</span></span>

<span data-ttu-id="8ce0e-118">Usare BITS per le applicazioni che devono:</span><span class="sxs-lookup"><span data-stu-id="8ce0e-118">Use BITS for applications that need to:</span></span>

-   <span data-ttu-id="8ce0e-119">Scaricare o caricare file in un server Web HTTP o REST o in un file server SMB.</span><span class="sxs-lookup"><span data-stu-id="8ce0e-119">Download from or upload files to an HTTP or REST web server or SMB file server.</span></span>
-   <span data-ttu-id="8ce0e-120">Riavvia automaticamente i trasferimenti di file dopo la disconnessione della rete e il riavvio del computer.</span><span class="sxs-lookup"><span data-stu-id="8ce0e-120">Automatically resume file transfers after network disconnects and computer restarts.</span></span>
-   <span data-ttu-id="8ce0e-121">Mantenere la velocità di risposta delle altre applicazioni di rete.</span><span class="sxs-lookup"><span data-stu-id="8ce0e-121">Preserve the responsiveness of other network applications.</span></span>
-   <span data-ttu-id="8ce0e-122">Tenere in considerazione il costo di rete, ad esempio le reti mobili</span><span class="sxs-lookup"><span data-stu-id="8ce0e-122">Be mindful of the network cost on e.g. roaming networks</span></span>
-   <span data-ttu-id="8ce0e-123">Usare facoltativamente [BranchCache](/windows-server/networking/branchcache/branchcache) per ottimizzare il traffico di Wide Area Network (WAN)</span><span class="sxs-lookup"><span data-stu-id="8ce0e-123">Optionally work with [BranchCache](/windows-server/networking/branchcache/branchcache) to optimize wide area network (WAN) traffic</span></span>

## <a name="developer-audience"></a><span data-ttu-id="8ce0e-124">Sviluppatori</span><span class="sxs-lookup"><span data-stu-id="8ce0e-124">Developer audience</span></span>

<span data-ttu-id="8ce0e-125">BITS è un'interfaccia COM progettata per sviluppatori C e C++ che può essere usata anche dagli sviluppatori .NET.</span><span class="sxs-lookup"><span data-stu-id="8ce0e-125">BITS is a COM interface designed for C and C++ developers that can also be used by .NET developers.</span></span> <span data-ttu-id="8ce0e-126">Gli sviluppatori UWP devono usare l'API [Windows. Networking. BackgroundTransfer](/uwp/api/Windows.Networking.BackgroundTransfer) e non l'API BITS.</span><span class="sxs-lookup"><span data-stu-id="8ce0e-126">UWP developers should use the [Windows.Networking.BackgroundTransfer](/uwp/api/Windows.Networking.BackgroundTransfer) API and not the BITS API.</span></span>

## <a name="bits-versions"></a><span data-ttu-id="8ce0e-127">Versioni BITS</span><span class="sxs-lookup"><span data-stu-id="8ce0e-127">BITS versions</span></span>

<span data-ttu-id="8ce0e-128">Per informazioni complete sulla cronologia delle versioni e informazioni sul sistema operativo precedente [, vedere Novità](what-s-new.md).</span><span class="sxs-lookup"><span data-stu-id="8ce0e-128">For complete version history and information on earlier operating system, see [What's New](what-s-new.md).</span></span>


## <a name="in-this-section"></a><span data-ttu-id="8ce0e-129">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="8ce0e-129">In this section</span></span>



| <span data-ttu-id="8ce0e-130">Argomento</span><span class="sxs-lookup"><span data-stu-id="8ce0e-130">Topic</span></span>                                                           | <span data-ttu-id="8ce0e-131">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8ce0e-131">Description</span></span>                                                                                                                                                                     |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8ce0e-132">Informazioni su BITS</span><span class="sxs-lookup"><span data-stu-id="8ce0e-132">About BITS</span></span>](about-bits.md)<br/>                         | <span data-ttu-id="8ce0e-133">Informazioni generali sui bit.</span><span class="sxs-lookup"><span data-stu-id="8ce0e-133">General information about BITS.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="8ce0e-134">Uso di BITS</span><span class="sxs-lookup"><span data-stu-id="8ce0e-134">Using BITS</span></span>](using-bits.md)<br/>                         | <span data-ttu-id="8ce0e-135">Guida procedurale per lo sviluppo di client BITS che trasferiscono file tra un client e un server.</span><span class="sxs-lookup"><span data-stu-id="8ce0e-135">Procedural guide for developing BITS clients that transfer files between a client and server.</span></span><br/>                                                                        |
| [<span data-ttu-id="8ce0e-136">Riferimenti BITS</span><span class="sxs-lookup"><span data-stu-id="8ce0e-136">BITS Reference</span></span>](bits-reference.md)<br/>                 | <span data-ttu-id="8ce0e-137">Informazioni di riferimento per le interfacce di programmazione BITS.</span><span class="sxs-lookup"><span data-stu-id="8ce0e-137">Reference information for the BITS programming interfaces.</span></span> <span data-ttu-id="8ce0e-138">Contiene inoltre informazioni su esempi, strumenti, impostazioni server per i processi di caricamento e il protocollo di caricamento.</span><span class="sxs-lookup"><span data-stu-id="8ce0e-138">Also contains information about samples, tools, server settings for upload jobs, and the upload protocol.</span></span><br/> |
| [<span data-ttu-id="8ce0e-139">Procedure consigliate</span><span class="sxs-lookup"><span data-stu-id="8ce0e-139">Best Practices</span></span>](best-practices-when-using-bits.md)<br/> | <span data-ttu-id="8ce0e-140">Informazioni da considerare quando si progetta un'applicazione che utilizza BITS.</span><span class="sxs-lookup"><span data-stu-id="8ce0e-140">Information to consider when designing an application that uses BITS.</span></span><br/>                                                                                                |



 

## <a name="additional-resources"></a><span data-ttu-id="8ce0e-141">Risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="8ce0e-141">Additional resources</span></span>

<span data-ttu-id="8ce0e-142">Di seguito sono riportate altre risorse.</span><span class="sxs-lookup"><span data-stu-id="8ce0e-142">The following are additional resources.</span></span>


|             |                                                                                                                                                 |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ce0e-143">DLL di riferimento .NET</span><span class="sxs-lookup"><span data-stu-id="8ce0e-143">.NET Reference DLL</span></span>   | <span data-ttu-id="8ce0e-144">Per informazioni sull'uso di BITS da .NET con le DLL di riferimento, vedere la pagina relativa alla [chiamata a BITS da .NET tramite dll di riferimento](/windows/desktop/Bits/bits-dot-net)</span><span class="sxs-lookup"><span data-stu-id="8ce0e-144">For information on using BITS from .NET using reference DLLs, see [Calling into BITS from .NET using Reference DLLs](/windows/desktop/Bits/bits-dot-net)</span></span>      |
| <span data-ttu-id="8ce0e-145">Wrapper .NET</span><span class="sxs-lookup"><span data-stu-id="8ce0e-145">.NET Wrapper</span></span>   | <span data-ttu-id="8ce0e-146">Per gli altri wrapper .NET per BITS, è possibile cercare i progetti contrassegnati con il tag BITS in [NuGet](https://www.nuget.org/packages?q=Tags%3A%22BITS%22) .</span><span class="sxs-lookup"><span data-stu-id="8ce0e-146">For other .NET wrappers for BITS, you can search [nuget](https://www.nuget.org/packages?q=Tags%3A%22BITS%22) for projects tagged with the BITS tag.</span></span>        |



 

 

