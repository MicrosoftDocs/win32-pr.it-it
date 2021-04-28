---
description: Solo a 64 bit
ms.assetid: 5d0188a5-ef5f-409e-9d2d-7639d99edc1d
title: Solo a 64 bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2d896fcaf4b8c4ebeadf7cfd5a5c22e511cb659
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088809"
---
# <a name="64-bit-only"></a><span data-ttu-id="b1e5b-103">Solo a 64 bit</span><span class="sxs-lookup"><span data-stu-id="b1e5b-103">64-Bit Only</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="b1e5b-104">Piattaforme interessate</span><span class="sxs-lookup"><span data-stu-id="b1e5b-104">Affected Platforms</span></span>

<span data-ttu-id="b1e5b-105">**Server** - Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b1e5b-105">**Servers** - Windows Server 2008 R2</span></span>  



## <a name="feature-impact"></a><span data-ttu-id="b1e5b-106">Impatto sulle funzionalità</span><span class="sxs-lookup"><span data-stu-id="b1e5b-106">Feature Impact</span></span>

 <span data-ttu-id="b1e5b-107">**Gravità** - Bassa</span><span class="sxs-lookup"><span data-stu-id="b1e5b-107">**Severity** - Low</span></span>  
<span data-ttu-id="b1e5b-108">**Frequenza** - Alta</span><span class="sxs-lookup"><span data-stu-id="b1e5b-108">**Frequency** - High</span></span>  






## <a name="description"></a><span data-ttu-id="b1e5b-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b1e5b-109">Description</span></span>

<span data-ttu-id="b1e5b-110">Windows Server 2008 R2 viene fornito solo con uno SKU a 64 bit. non sono disponibili SKU a 32 bit per la versione server del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="b1e5b-110">Windows Server 2008 R2 ships with a 64-bit SKU only; no 32-bit SKU is available for the server version of the operating system.</span></span> <span data-ttu-id="b1e5b-111">Tuttavia, uno SKU a 32 bit continua a essere disponibile per il client Windows 7.</span><span class="sxs-lookup"><span data-stu-id="b1e5b-111">However, a 32-bit SKU continues to be available for the Windows 7 client.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="b1e5b-112">Impatto significativo</span><span class="sxs-lookup"><span data-stu-id="b1e5b-112">Manifestation of Impact</span></span>

<span data-ttu-id="b1e5b-113">Ciò inciderà su tre aree:</span><span class="sxs-lookup"><span data-stu-id="b1e5b-113">This will impact three areas:</span></span>

-   <span data-ttu-id="b1e5b-114">Driver a 32 bit</span><span class="sxs-lookup"><span data-stu-id="b1e5b-114">32-bit drivers</span></span>
-   <span data-ttu-id="b1e5b-115">Plug-in a 32 bit</span><span class="sxs-lookup"><span data-stu-id="b1e5b-115">32-bit plug-ins</span></span>
-   <span data-ttu-id="b1e5b-116">Eseguibili a 16 bit</span><span class="sxs-lookup"><span data-stu-id="b1e5b-116">16-bit executables</span></span>

## <a name="solution-for-32-bit-drivers"></a><span data-ttu-id="b1e5b-117">Soluzione per driver a 32 bit</span><span class="sxs-lookup"><span data-stu-id="b1e5b-117">Solution for 32-bit Drivers</span></span>

<span data-ttu-id="b1e5b-118">Ricompilare i driver a 32 bit come driver a 64 bit firmati.</span><span class="sxs-lookup"><span data-stu-id="b1e5b-118">Recompile 32-bit drivers as signed 64-bit drivers.</span></span>

## <a name="solution-for-32-bit-plug-ins"></a><span data-ttu-id="b1e5b-119">Soluzione per plug-in a 32 bit</span><span class="sxs-lookup"><span data-stu-id="b1e5b-119">Solution for 32-bit Plug-ins</span></span>

<span data-ttu-id="b1e5b-120">WoW64, un emulatore x86, consente l'esecuzione senza problemi delle applicazioni basate su Windows a 32 bit in Windows a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="b1e5b-120">WoW64, an x86 emulator, allows 32-bit Windows-based applications to run seamlessly on 64-bit Windows.</span></span> <span data-ttu-id="b1e5b-121">WoW64 è ora una funzionalità facoltativa che è necessario installare se è necessario eseguire codice a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="b1e5b-121">WoW64 is now an optional feature that you must install if it is necessary to run 32-bit code.</span></span>

<span data-ttu-id="b1e5b-122">Il sistema isola le applicazioni a 32 bit dalle applicazioni a 64 bit, che includono la prevenzione di conflitti tra file e Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="b1e5b-122">The system isolates 32-bit applications from 64-bit applications, which includes preventing file and registry collisions.</span></span> <span data-ttu-id="b1e5b-123">Sono supportate console, interfaccia utente grafica e applicazioni di servizio.</span><span class="sxs-lookup"><span data-stu-id="b1e5b-123">Console, GUI, and service applications are supported.</span></span> <span data-ttu-id="b1e5b-124">Il sistema garantisce l'interoperabilità attraverso il limite 32/64 per scenari come taglia e incolla e COM.</span><span class="sxs-lookup"><span data-stu-id="b1e5b-124">The system provides interoperability across the 32/64 boundary for scenarios such as cut and paste and COM.</span></span> <span data-ttu-id="b1e5b-125">Tuttavia, i processi a 32 bit non possono caricare DLL a 64 bit e i processi a 64 bit non possono caricare DLL a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="b1e5b-125">However, 32-bit processes cannot load 64-bit DLLs, and 64-bit processes cannot load 32-bit DLLs.</span></span> <span data-ttu-id="b1e5b-126">Questo si verifica in genere nei plug-in della shell scritti per Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="b1e5b-126">We commonly see this in shell plug-ins written for Windows Explorer.</span></span>

<span data-ttu-id="b1e5b-127">Un'applicazione a 32 bit può rilevare se è in esecuzione in WOW64 chiamando la funzione IsWow64Process.</span><span class="sxs-lookup"><span data-stu-id="b1e5b-127">A 32-bit application can detect whether it is running under WOW64 by calling the IsWow64Process function.</span></span> <span data-ttu-id="b1e5b-128">L'applicazione può ottenere informazioni aggiuntive sul processore usando la funzione GetNativeSystemInfo</span><span class="sxs-lookup"><span data-stu-id="b1e5b-128">The application can obtain additional information about the processor by using the GetNativeSystemInfo function</span></span>

<span data-ttu-id="b1e5b-129">Si noti che Windows a 64 bit non supporta l'esecuzione di applicazioni basate su Windows a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="b1e5b-129">Note that 64-bit Windows does not support running 16-bit Windows-based applications.</span></span> <span data-ttu-id="b1e5b-130">Il motivo principale è che gli handle hanno 32 bit significativi in Windows a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="b1e5b-130">The primary reason is that handles have 32 significant bits on 64-bit Windows.</span></span> <span data-ttu-id="b1e5b-131">Pertanto, gli handle non possono essere troncati e passati alle applicazioni a 16 bit senza perdita di dati.</span><span class="sxs-lookup"><span data-stu-id="b1e5b-131">Therefore, handles cannot be truncated and passed to 16-bit applications without loss of data.</span></span> <span data-ttu-id="b1e5b-132">I tentativi di avviare applicazioni a 16 bit hanno esito negativo con l'errore seguente: ERRORE \_ BAD \_ EXE \_ FORMAT.</span><span class="sxs-lookup"><span data-stu-id="b1e5b-132">Attempts to launch 16-bit applications fail with the following error: ERROR\_BAD\_EXE\_FORMAT.</span></span>

## <a name="solution-for-16-bit-executables"></a><span data-ttu-id="b1e5b-133">Soluzione per file eseguibili a 16 bit</span><span class="sxs-lookup"><span data-stu-id="b1e5b-133">Solution for 16-bit Executables</span></span>

<span data-ttu-id="b1e5b-134">Windows a 64 bit riconosce un numero limitato di programmi di installazione a 16 bit specifici e sostituisce una versione a 32 bit con porta.</span><span class="sxs-lookup"><span data-stu-id="b1e5b-134">64-bit Windows recognizes a limited number of specific 16-bit installer programs and substitutes a ported 32-bit version.</span></span> <span data-ttu-id="b1e5b-135">L'elenco delle sostituzioni viene archiviato nel Registro di sistema nella chiave seguente: HKEY LOCAL MACHINE Software Microsoft Windows NT CurrentVersion NtVdm64 È disponibile il supporto predefinito per diversi motori di installazione, inclusi i programmi di installazione \_ \_ \\ \\ \\ \\ \\ InstallShield 5.x.</span><span class="sxs-lookup"><span data-stu-id="b1e5b-135">The list of substitutions is stored in the registry under the following key: HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows NT\\CurrentVersion\\NtVdm64 There is built-in support for several installer engines, including InstallShield 5.x installers.</span></span> <span data-ttu-id="b1e5b-136">Si noti che il Windows Installer a 64 bit può installare facilmente applicazioni basate su MSI a 32 bit in Windows a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="b1e5b-136">Note that the 64-bit Windows Installer can seamlessly install 32-bit MSI-based applications on 64-bit Windows.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="b1e5b-137">Collegamenti ad altre risorse</span><span class="sxs-lookup"><span data-stu-id="b1e5b-137">Links to Other Resources</span></span>

-   [<span data-ttu-id="b1e5b-138">Esecuzione di applicazioni a 32 bit</span><span class="sxs-lookup"><span data-stu-id="b1e5b-138">Running 32-bit Applications</span></span>](/windows/desktop/WinProg64/running-32-bit-applications)
-   [<span data-ttu-id="b1e5b-139">Prestazioni e utilizzo della memoria</span><span class="sxs-lookup"><span data-stu-id="b1e5b-139">Performance and Memory Consumption</span></span>](/windows/desktop/WinProg64/performance-and-memory-consumption)
-   [<span data-ttu-id="b1e5b-140">Dettagli sull'implementazione di WOW64</span><span class="sxs-lookup"><span data-stu-id="b1e5b-140">WOW64 Implementation Details</span></span>](/windows/desktop/WinProg64/wow64-implementation-details)
-   [<span data-ttu-id="b1e5b-141">Redirector del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="b1e5b-141">Registry Redirector</span></span>](/windows/desktop/WinProg64/registry-redirector)
-   [<span data-ttu-id="b1e5b-142">File System Redirector</span><span class="sxs-lookup"><span data-stu-id="b1e5b-142">File System Redirector</span></span>](/windows/desktop/WinProg64/file-system-redirector)
-   [<span data-ttu-id="b1e5b-143">Gestione della memoria</span><span class="sxs-lookup"><span data-stu-id="b1e5b-143">Memory Management</span></span>](/windows/desktop/WinProg64/memory-management)
-   [<span data-ttu-id="b1e5b-144">Affinità processori</span><span class="sxs-lookup"><span data-stu-id="b1e5b-144">Processor Affinity</span></span>](/windows/desktop/WinProg64/processor-affinity)
-   [<span data-ttu-id="b1e5b-145">Comunicazione interprocesso</span><span class="sxs-lookup"><span data-stu-id="b1e5b-145">Interprocess Communication</span></span>](/windows/desktop/WinProg64/interprocess-communication)
-   [<span data-ttu-id="b1e5b-146">Installazione di applicazioni in sistemi a 64 bit</span><span class="sxs-lookup"><span data-stu-id="b1e5b-146">Application Installation on 64-bit Systems</span></span>](/windows/desktop/WinProg64/application-installation)
-   [<span data-ttu-id="b1e5b-147">Debug di WOW64</span><span class="sxs-lookup"><span data-stu-id="b1e5b-147">Debugging WOW64</span></span>](/windows/desktop/WinProg64/debugging-wow64)
-   [<span data-ttu-id="b1e5b-148">**Funzione IsWow64Process**</span><span class="sxs-lookup"><span data-stu-id="b1e5b-148">**IsWow64Process Function**</span></span>](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process)
-   [<span data-ttu-id="b1e5b-149">**Funzione GetNativeSystemInfo**</span><span class="sxs-lookup"><span data-stu-id="b1e5b-149">**GetNativeSystemInfo Function**</span></span>](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getnativesysteminfo)

 

 
