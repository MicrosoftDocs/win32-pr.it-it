---
description: È possibile utilizzare lo strumento logman per raccogliere informazioni di traccia per le applicazioni VSS che utilizzano il ripristino automatico del sistema (ASR).
ms.assetid: 872609c8-a123-40a8-96ca-58f34d37f3d8
title: Uso degli strumenti di traccia con le applicazioni ASR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c13eee1c62cd6636eebe5bcfd35bd5abb119645
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307183"
---
# <a name="using-tracing-tools-with-asr-applications"></a><span data-ttu-id="be276-103">Uso degli strumenti di traccia con le applicazioni ASR</span><span class="sxs-lookup"><span data-stu-id="be276-103">Using Tracing Tools with ASR Applications</span></span>

<span data-ttu-id="be276-104">È possibile utilizzare lo strumento logman per raccogliere informazioni di traccia per le applicazioni VSS che utilizzano il [Ripristino automatico del sistema (ASR)](using-vss-automated-system-recovery-for-disaster-recovery.md).</span><span class="sxs-lookup"><span data-stu-id="be276-104">You can use the Logman tool to collect tracing information for VSS applications that use [Automated System Recovery (ASR)](using-vss-automated-system-recovery-for-disaster-recovery.md).</span></span> <span data-ttu-id="be276-105">Logman (logman.exe) è un controller di traccia per gli eventi di traccia e i contatori delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="be276-105">Logman (logman.exe) is a trace controller for trace events and performance counters.</span></span> <span data-ttu-id="be276-106">È incluso in Windows XP e nelle versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="be276-106">It is included in Windows XP and later versions of Windows.</span></span> <span data-ttu-id="be276-107">In alternativa, se si preferisce, è possibile usare lo strumento tracelog per raccogliere le stesse informazioni di traccia di ASR.</span><span class="sxs-lookup"><span data-stu-id="be276-107">Or, if you prefer, you can use the Tracelog tool to collect the same ASR tracing information.</span></span> <span data-ttu-id="be276-108">Tracelog è incluso in Windows Driver Kit (WDK).</span><span class="sxs-lookup"><span data-stu-id="be276-108">Tracelog is included in the Windows Driver Kit (WDK).</span></span>

<span data-ttu-id="be276-109">Per usare gli strumenti di traccia con VSS, vedere [uso degli strumenti di traccia con VSS](using-tracing-tools-with-vss.md).</span><span class="sxs-lookup"><span data-stu-id="be276-109">To use tracing tools with VSS, see [Using Tracing Tools with VSS](using-tracing-tools-with-vss.md).</span></span>

## <a name="using-logman"></a><span data-ttu-id="be276-110">Uso di logman</span><span class="sxs-lookup"><span data-stu-id="be276-110">Using Logman</span></span>

<span data-ttu-id="be276-111">Nella procedura seguente viene descritto come utilizzare logman con l'applicazione ASR.</span><span class="sxs-lookup"><span data-stu-id="be276-111">The following procedure describes how to use Logman with your ASR application.</span></span>

<span data-ttu-id="be276-112">**Per usare logman con l'applicazione ASR**</span><span class="sxs-lookup"><span data-stu-id="be276-112">**To use Logman with your ASR application**</span></span>

1.  <span data-ttu-id="be276-113">Usare il comando seguente per avviare la traccia:</span><span class="sxs-lookup"><span data-stu-id="be276-113">Use the following command to start tracing:</span></span>

    <span data-ttu-id="be276-114">**logman avviare ASR-o** *x: \\ \* \* \* ASR. etl-ETS-p {6407345b-94F2-44c8-b3db-4e076be46816} 0xFF 0xFF*\*</span><span class="sxs-lookup"><span data-stu-id="be276-114">**logman start asr -o** *x:\\*\*\*asr.etl -ets -p {6407345b-94f2-44c8-b3db-4e076be46816} 0xff 0xff*\*</span></span>

    > [!Note]  
    > <span data-ttu-id="be276-115">Sostituire "x: \\ " con il percorso della directory in cui si desidera archiviare il file di log di traccia.</span><span class="sxs-lookup"><span data-stu-id="be276-115">Replace "x:\\" with the path to the directory where you would like the trace log file to be stored.</span></span> <span data-ttu-id="be276-116">Per prestazioni ottimali, il file di log di traccia deve trovarsi in un volume che non fa parte della copia shadow.</span><span class="sxs-lookup"><span data-stu-id="be276-116">For best performance, the trace log file should be located on a volume that is not part of the shadow copy.</span></span>

     

2.  <span data-ttu-id="be276-117">Usare il comando seguente per arrestare la traccia:</span><span class="sxs-lookup"><span data-stu-id="be276-117">Use the following command to stop tracing:</span></span>

    <span data-ttu-id="be276-118">**logman stop ASR-ETS**</span><span class="sxs-lookup"><span data-stu-id="be276-118">**logman stop asr -ets**</span></span>

<span data-ttu-id="be276-119">Il file di log di traccia è *x: \\* ASR. etl.</span><span class="sxs-lookup"><span data-stu-id="be276-119">The trace log file is *x:\\* asr.etl.</span></span>

<span data-ttu-id="be276-120">Per ulteriori informazioni sullo strumento Logman, vedere [logman](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc753820(v=ws.11)).</span><span class="sxs-lookup"><span data-stu-id="be276-120">For more information about the Logman tool, see [Logman](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc753820(v=ws.11)).</span></span>

## <a name="using-tracelog"></a><span data-ttu-id="be276-121">Uso di tracelog</span><span class="sxs-lookup"><span data-stu-id="be276-121">Using Tracelog</span></span>

<span data-ttu-id="be276-122">Nella procedura seguente viene descritto come utilizzare tracelog.</span><span class="sxs-lookup"><span data-stu-id="be276-122">The following procedure describes how to use Tracelog.</span></span>

<span data-ttu-id="be276-123">**Per usare tracelog**</span><span class="sxs-lookup"><span data-stu-id="be276-123">**To use Tracelog**</span></span>

1.  <span data-ttu-id="be276-124">Creare un file di testo denominato ASR. CTL che contiene solo il testo seguente:</span><span class="sxs-lookup"><span data-stu-id="be276-124">Create a text file named asr.ctl that contains only the following text:</span></span>

    <span data-ttu-id="be276-125">**6407345b-94F2-44c8-b3db-4e076be46816 ASR**</span><span class="sxs-lookup"><span data-stu-id="be276-125">**6407345b-94f2-44c8-b3db-4e076be46816 asr**</span></span>

2.  <span data-ttu-id="be276-126">Usare il comando seguente per avviare la traccia:</span><span class="sxs-lookup"><span data-stu-id="be276-126">Use the following command to start tracing:</span></span>

    <span data-ttu-id="be276-127">**tracelog-avviare ASR-f** *x: \\ \* \* \* ASR. etl-GUID ASR. CTL-flag 0xFF-Level 0xFF*\*</span><span class="sxs-lookup"><span data-stu-id="be276-127">**tracelog -start asr -f** *x:\\*\*\*asr.etl -guid asr.ctl -flag 0xff -level 0xff*\*</span></span>

    > [!Note]  
    > <span data-ttu-id="be276-128">Sostituire "x: \\ " con il percorso della directory in cui si desidera archiviare il file di log di traccia.</span><span class="sxs-lookup"><span data-stu-id="be276-128">Replace "x:\\" with the path to the directory where you would like the trace log file to be stored.</span></span> <span data-ttu-id="be276-129">Per prestazioni ottimali, il file di log di traccia deve trovarsi in un volume che non fa parte della copia shadow.</span><span class="sxs-lookup"><span data-stu-id="be276-129">For best performance, the trace log file should be located on a volume that is not part of the shadow copy.</span></span>

     

3.  <span data-ttu-id="be276-130">Usare il comando seguente per arrestare la traccia:</span><span class="sxs-lookup"><span data-stu-id="be276-130">Use the following command to stop tracing:</span></span>

    <span data-ttu-id="be276-131">**tracelog-arresta ASR**</span><span class="sxs-lookup"><span data-stu-id="be276-131">**tracelog -stop asr**</span></span>

<span data-ttu-id="be276-132">Il file di log di traccia è *x: \\* ASR. etl.</span><span class="sxs-lookup"><span data-stu-id="be276-132">The trace log file is *x:\\* asr.etl.</span></span>

<span data-ttu-id="be276-133">Per ulteriori informazioni sullo strumento tracelog, vedere [tracelog](https://msdn.microsoft.com/library/ms797927.aspx).</span><span class="sxs-lookup"><span data-stu-id="be276-133">For more information about the Tracelog tool, see [Tracelog](https://msdn.microsoft.com/library/ms797927.aspx).</span></span>

 

 
