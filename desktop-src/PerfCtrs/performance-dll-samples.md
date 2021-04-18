---
description: Il Windows SDK (WSDK) contiene tre DLL di prestazioni di esempio complete.
ms.assetid: 862be53a-3d58-42b9-adf0-2f913dc6fb06
title: Esempi di DLL di prestazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13e2210899651a065218474eb49175553a05aa8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312102"
---
# <a name="performance-dll-samples"></a><span data-ttu-id="47311-103">Esempi di DLL di prestazioni</span><span class="sxs-lookup"><span data-stu-id="47311-103">Performance DLL Samples</span></span>

<span data-ttu-id="47311-104">Il Windows SDK (WSDK) contiene tre DLL di prestazioni di esempio complete.</span><span class="sxs-lookup"><span data-stu-id="47311-104">The Windows SDK (WSDK) contains three complete sample performance DLLs.</span></span> <span data-ttu-id="47311-105">Questi esempi si trovano nella directory Samples \\ winbase \\ WinNT \\ PerfTool \\ PerfDlls</span><span class="sxs-lookup"><span data-stu-id="47311-105">These samples are located in the Samples\\WinBase\\WinNT\\PerfTool\\PerfDlls directory.</span></span> <span data-ttu-id="47311-106">La radice di questo percorso è la directory di installazione di base di WSDK.</span><span class="sxs-lookup"><span data-stu-id="47311-106">The root of this path is the base installation directory of the WSDK.</span></span> <span data-ttu-id="47311-107">È possibile scaricare WSDK dal [Software Development Kit (SDK) di Microsoft Windows](https://developer.microsoft.com/windows/downloads/windows-10-sdk/) (cercare Windows SDK e selezionare il download per l'ultimo sistema operativo rilasciato).</span><span class="sxs-lookup"><span data-stu-id="47311-107">You can download the WSDK from the [Microsoft Windows Software Development Kit (SDK)](https://developer.microsoft.com/windows/downloads/windows-10-sdk/) (search for Windows SDK and select the download for the latest released operating system).</span></span>

<span data-ttu-id="47311-108">Gli esempi contenuti in questa directory sono:</span><span class="sxs-lookup"><span data-stu-id="47311-108">The samples contained in this directory are:</span></span>

-   <span data-ttu-id="47311-109">**AppMem**: fornisce le controparti delle funzioni [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc), [**GlobalReAlloc**](/windows/desktop/api/winbase/nf-winbase-globalrealloc)e [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) che segnalano le informazioni sulle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="47311-109">**AppMem**—Provides counterparts of the [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc), [**GlobalReAlloc**](/windows/desktop/api/winbase/nf-winbase-globalrealloc), and [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) functions that report performance information.</span></span> <span data-ttu-id="47311-110">I contatori delle prestazioni nel registro di sistema e lo strumento prestazioni possono leggere le informazioni sulle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="47311-110">Performance counters in the registry and the Performance tool can read the performance information.</span></span>
-   <span data-ttu-id="47311-111">**LeakyBin**: illustra l'uso dei contatori delle prestazioni dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="47311-111">**LeakyBin**—Demonstrates the use of application performance counters.</span></span>
-   <span data-ttu-id="47311-112">**PerfGen**: offre tre forme d'onda a cinque periodi diversi per l'uso con lo strumento prestazioni per fornire dati con una velocità e un valore noti.</span><span class="sxs-lookup"><span data-stu-id="47311-112">**PerfGen**—Provides three waveforms at five different periods for use with the Performance tool to provide data at a known rate and value.</span></span> <span data-ttu-id="47311-113">Questa operazione può essere utile per il test di applicazioni che utilizzano dati sulle prestazioni e richiedono valori stimabili per i test.</span><span class="sxs-lookup"><span data-stu-id="47311-113">This can be useful in testing applications that use performance data and need predictable values to test against.</span></span>

 

 
