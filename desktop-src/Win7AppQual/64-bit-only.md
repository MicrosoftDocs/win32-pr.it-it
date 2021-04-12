---
description: .
ms.assetid: 5d0188a5-ef5f-409e-9d2d-7639d99edc1d
title: Solo 64 bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d3178a15ec0a138a73789233dd2d787964a96b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234000"
---
# <a name="64-bit-only"></a><span data-ttu-id="fcdc9-103">Solo 64 bit</span><span class="sxs-lookup"><span data-stu-id="fcdc9-103">64-Bit Only</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="fcdc9-104">Piattaforme interessate</span><span class="sxs-lookup"><span data-stu-id="fcdc9-104">Affected Platforms</span></span>

<span data-ttu-id="fcdc9-105">**Server** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="fcdc9-105">**Servers** - Windows Server 2008 R2</span></span>  



## <a name="feature-impact"></a><span data-ttu-id="fcdc9-106">Effetto sulle funzionalità</span><span class="sxs-lookup"><span data-stu-id="fcdc9-106">Feature Impact</span></span>

 <span data-ttu-id="fcdc9-107">**Gravità** -bassa</span><span class="sxs-lookup"><span data-stu-id="fcdc9-107">**Severity** - Low</span></span>  
<span data-ttu-id="fcdc9-108">**Frequenza** -alta</span><span class="sxs-lookup"><span data-stu-id="fcdc9-108">**Frequency** - High</span></span>  






## <a name="description"></a><span data-ttu-id="fcdc9-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fcdc9-109">Description</span></span>

<span data-ttu-id="fcdc9-110">Windows Server 2008 R2 viene fornito solo con SKU a 64 bit. non sono disponibili SKU a 32 bit per la versione server del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="fcdc9-110">Windows Server 2008 R2 ships with a 64-bit SKU only; no 32-bit SKU is available for the server version of the operating system.</span></span> <span data-ttu-id="fcdc9-111">Tuttavia, uno SKU a 32 bit continua a essere disponibile per il client di Windows 7.</span><span class="sxs-lookup"><span data-stu-id="fcdc9-111">However, a 32-bit SKU continues to be available for the Windows 7 client.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="fcdc9-112">Manifesto di effetto</span><span class="sxs-lookup"><span data-stu-id="fcdc9-112">Manifestation of Impact</span></span>

<span data-ttu-id="fcdc9-113">Questa operazione avrà effetto su tre aree:</span><span class="sxs-lookup"><span data-stu-id="fcdc9-113">This will impact three areas:</span></span>

-   <span data-ttu-id="fcdc9-114">driver a 32 bit</span><span class="sxs-lookup"><span data-stu-id="fcdc9-114">32-bit drivers</span></span>
-   <span data-ttu-id="fcdc9-115">plug-in a 32 bit</span><span class="sxs-lookup"><span data-stu-id="fcdc9-115">32-bit plug-ins</span></span>
-   <span data-ttu-id="fcdc9-116">eseguibili a 16 bit</span><span class="sxs-lookup"><span data-stu-id="fcdc9-116">16-bit executables</span></span>

## <a name="solution-for-32-bit-drivers"></a><span data-ttu-id="fcdc9-117">Soluzione per driver a 32 bit</span><span class="sxs-lookup"><span data-stu-id="fcdc9-117">Solution for 32-bit Drivers</span></span>

<span data-ttu-id="fcdc9-118">Ricompilare i driver a 32 bit come driver 64 bit firmati.</span><span class="sxs-lookup"><span data-stu-id="fcdc9-118">Recompile 32-bit drivers as signed 64-bit drivers.</span></span>

## <a name="solution-for-32-bit-plug-ins"></a><span data-ttu-id="fcdc9-119">Soluzione per plug-in a 32 bit</span><span class="sxs-lookup"><span data-stu-id="fcdc9-119">Solution for 32-bit Plug-ins</span></span>

<span data-ttu-id="fcdc9-120">WoW64, un emulatore x86, consente alle applicazioni basate su Windows a 32 bit di funzionare facilmente in Windows a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="fcdc9-120">WoW64, an x86 emulator, allows 32-bit Windows-based applications to run seamlessly on 64-bit Windows.</span></span> <span data-ttu-id="fcdc9-121">WoW64 è ora una funzionalità facoltativa che è necessario installare se è necessario eseguire codice a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="fcdc9-121">WoW64 is now an optional feature that you must install if it is necessary to run 32-bit code.</span></span>

<span data-ttu-id="fcdc9-122">Il sistema isola le applicazioni a 32 bit dalle applicazioni a 64 bit, inclusa la prevenzione dei conflitti tra file e registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="fcdc9-122">The system isolates 32-bit applications from 64-bit applications, which includes preventing file and registry collisions.</span></span> <span data-ttu-id="fcdc9-123">Sono supportate le applicazioni console, GUI e di servizio.</span><span class="sxs-lookup"><span data-stu-id="fcdc9-123">Console, GUI, and service applications are supported.</span></span> <span data-ttu-id="fcdc9-124">Il sistema garantisce l'interoperabilità oltre il limite di 32/64 per scenari quali taglia e incolla e COM.</span><span class="sxs-lookup"><span data-stu-id="fcdc9-124">The system provides interoperability across the 32/64 boundary for scenarios such as cut and paste and COM.</span></span> <span data-ttu-id="fcdc9-125">Tuttavia, i processi a 32 bit non possono caricare le dll a 64 bit e i processi a 64 bit non possono caricare le dll a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="fcdc9-125">However, 32-bit processes cannot load 64-bit DLLs, and 64-bit processes cannot load 32-bit DLLs.</span></span> <span data-ttu-id="fcdc9-126">Questa operazione è comunemente visibile nei plug-in della shell scritti per Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="fcdc9-126">We commonly see this in shell plug-ins written for Windows Explorer.</span></span>

<span data-ttu-id="fcdc9-127">Un'applicazione a 32 bit può rilevare se è in esecuzione in WOW64 chiamando la funzione IsWow64Process.</span><span class="sxs-lookup"><span data-stu-id="fcdc9-127">A 32-bit application can detect whether it is running under WOW64 by calling the IsWow64Process function.</span></span> <span data-ttu-id="fcdc9-128">L'applicazione può ottenere ulteriori informazioni sul processore tramite la funzione GetNativeSystemInfo</span><span class="sxs-lookup"><span data-stu-id="fcdc9-128">The application can obtain additional information about the processor by using the GetNativeSystemInfo function</span></span>

<span data-ttu-id="fcdc9-129">Si noti che Windows a 64 bit non supporta l'esecuzione di applicazioni basate su Windows a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="fcdc9-129">Note that 64-bit Windows does not support running 16-bit Windows-based applications.</span></span> <span data-ttu-id="fcdc9-130">Il motivo principale è che gli handle hanno 32 bit significativi in Windows a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="fcdc9-130">The primary reason is that handles have 32 significant bits on 64-bit Windows.</span></span> <span data-ttu-id="fcdc9-131">Non è pertanto possibile troncare gli handle e passarli a applicazioni a 16 bit senza perdita di dati.</span><span class="sxs-lookup"><span data-stu-id="fcdc9-131">Therefore, handles cannot be truncated and passed to 16-bit applications without loss of data.</span></span> <span data-ttu-id="fcdc9-132">I tentativi di avvio delle applicazioni a 16 bit hanno esito negativo con l'errore seguente: errore del \_ \_ formato exe errato \_ .</span><span class="sxs-lookup"><span data-stu-id="fcdc9-132">Attempts to launch 16-bit applications fail with the following error: ERROR\_BAD\_EXE\_FORMAT.</span></span>

## <a name="solution-for-16-bit-executables"></a><span data-ttu-id="fcdc9-133">Soluzione per eseguibili a 16 bit</span><span class="sxs-lookup"><span data-stu-id="fcdc9-133">Solution for 16-bit Executables</span></span>

<span data-ttu-id="fcdc9-134">Windows a 64 bit riconosce un numero limitato di programmi programma di installazione a 16 bit specifici e sostituisce una versione a 32 bit portata.</span><span class="sxs-lookup"><span data-stu-id="fcdc9-134">64-bit Windows recognizes a limited number of specific 16-bit installer programs and substitutes a ported 32-bit version.</span></span> <span data-ttu-id="fcdc9-135">L'elenco di sostituzioni viene archiviato nel registro di sistema con la chiave seguente: HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ NtVdm64 è disponibile il supporto incorporato per diversi motori di installazione, inclusi i programmi di installazione di InstallShield 5. x.</span><span class="sxs-lookup"><span data-stu-id="fcdc9-135">The list of substitutions is stored in the registry under the following key: HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows NT\\CurrentVersion\\NtVdm64 There is built-in support for several installer engines, including InstallShield 5.x installers.</span></span> <span data-ttu-id="fcdc9-136">Si noti che la Windows Installer a 64 bit può installare facilmente applicazioni basate su MSI a 32 bit in Windows a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="fcdc9-136">Note that the 64-bit Windows Installer can seamlessly install 32-bit MSI-based applications on 64-bit Windows.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="fcdc9-137">Collegamenti ad altre risorse</span><span class="sxs-lookup"><span data-stu-id="fcdc9-137">Links to Other Resources</span></span>

-   [<span data-ttu-id="fcdc9-138">Esecuzione di applicazioni a 32 bit</span><span class="sxs-lookup"><span data-stu-id="fcdc9-138">Running 32-bit Applications</span></span>](/windows/desktop/WinProg64/running-32-bit-applications)
-   [<span data-ttu-id="fcdc9-139">Prestazioni e utilizzo di memoria</span><span class="sxs-lookup"><span data-stu-id="fcdc9-139">Performance and Memory Consumption</span></span>](/windows/desktop/WinProg64/performance-and-memory-consumption)
-   [<span data-ttu-id="fcdc9-140">Dettagli di implementazione di WOW64</span><span class="sxs-lookup"><span data-stu-id="fcdc9-140">WOW64 Implementation Details</span></span>](/windows/desktop/WinProg64/wow64-implementation-details)
-   [<span data-ttu-id="fcdc9-141">Redirector del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="fcdc9-141">Registry Redirector</span></span>](/windows/desktop/WinProg64/registry-redirector)
-   [<span data-ttu-id="fcdc9-142">Redirector del file System</span><span class="sxs-lookup"><span data-stu-id="fcdc9-142">File System Redirector</span></span>](/windows/desktop/WinProg64/file-system-redirector)
-   [<span data-ttu-id="fcdc9-143">Gestione della memoria</span><span class="sxs-lookup"><span data-stu-id="fcdc9-143">Memory Management</span></span>](/windows/desktop/WinProg64/memory-management)
-   [<span data-ttu-id="fcdc9-144">Affinità processori</span><span class="sxs-lookup"><span data-stu-id="fcdc9-144">Processor Affinity</span></span>](/windows/desktop/WinProg64/processor-affinity)
-   [<span data-ttu-id="fcdc9-145">Comunicazione interprocesso</span><span class="sxs-lookup"><span data-stu-id="fcdc9-145">Interprocess Communication</span></span>](/windows/desktop/WinProg64/interprocess-communication)
-   [<span data-ttu-id="fcdc9-146">Installazione di applicazioni su sistemi a 64 bit</span><span class="sxs-lookup"><span data-stu-id="fcdc9-146">Application Installation on 64-bit Systems</span></span>](/windows/desktop/WinProg64/application-installation)
-   [<span data-ttu-id="fcdc9-147">Debug di WOW64</span><span class="sxs-lookup"><span data-stu-id="fcdc9-147">Debugging WOW64</span></span>](/windows/desktop/WinProg64/debugging-wow64)
-   [<span data-ttu-id="fcdc9-148">**IsWow64Process (funzione)**</span><span class="sxs-lookup"><span data-stu-id="fcdc9-148">**IsWow64Process Function**</span></span>](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process)
-   [<span data-ttu-id="fcdc9-149">**GetNativeSystemInfo (funzione)**</span><span class="sxs-lookup"><span data-stu-id="fcdc9-149">**GetNativeSystemInfo Function**</span></span>](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getnativesysteminfo)

 

 
