---
description: Il provider WMIPerfClass e il provider WMIPerfInst forniscono dinamicamente i dati dei contatori delle prestazioni per le classi del contatore delle prestazioni WMI.
ms.assetid: 8bf6d218-9a31-4efd-a809-222aca364138
ms.tgt_platform: multiple
title: Librerie di prestazioni e WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4dedc9b98f492b3ab57e22cd1507f9e3651980a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308844"
---
# <a name="performance-libraries-and-wmi"></a><span data-ttu-id="8dbf8-103">Librerie di prestazioni e WMI</span><span class="sxs-lookup"><span data-stu-id="8dbf8-103">Performance Libraries and WMI</span></span>

<span data-ttu-id="8dbf8-104">Il [provider WMIPerfClass](wmiperfclass-provider.md) e il [provider WMIPerfInst](wmiperfinst-provider.md) forniscono dinamicamente i dati dei contatori delle prestazioni per le [classi del contatore delle prestazioni](/windows/desktop/CIMWin32Prov/performance-counter-classes)WMI.</span><span class="sxs-lookup"><span data-stu-id="8dbf8-104">The [WMIPerfClass Provider](wmiperfclass-provider.md) and the [WMIPerfInst Provider](wmiperfinst-provider.md) dynamically provide performance counter data for the WMI [Performance Counter Classes](/windows/desktop/CIMWin32Prov/performance-counter-classes).</span></span>

## <a name="wmiperfclass-and-wmiperfinst-providers"></a><span data-ttu-id="8dbf8-105">Provider WMIPerfClass e WMIPerfInst</span><span class="sxs-lookup"><span data-stu-id="8dbf8-105">WMIPerfClass and WMIPerfInst Providers</span></span>

<span data-ttu-id="8dbf8-106">Il [provider WMIPerfClass](wmiperfclass-provider.md) crea [classi del contatore delle prestazioni](/windows/desktop/CIMWin32Prov/performance-counter-classes) WMI all'inizializzazione del sistema.</span><span class="sxs-lookup"><span data-stu-id="8dbf8-106">[WMIPerfClass Provider](wmiperfclass-provider.md) creates WMI [Performance Counter Classes](/windows/desktop/CIMWin32Prov/performance-counter-classes) at system initialization.</span></span> <span data-ttu-id="8dbf8-107">Il [provider WMIPerfInst](wmiperfinst-provider.md) fornisce dinamicamente i dati dei contatori delle prestazioni per queste classi.</span><span class="sxs-lookup"><span data-stu-id="8dbf8-107">The [WMIPerfInst Provider](wmiperfinst-provider.md) dynamically provides performance counter data for these classes.</span></span> <span data-ttu-id="8dbf8-108">Il provider del provider WMIPerfClass fornisce le classi per i [contatori delle prestazioni](/windows/desktop/PerfCtrs/performance-counters-portal)versione 1 e versione 2.</span><span class="sxs-lookup"><span data-stu-id="8dbf8-108">The WMIPerfClass Provider provider supplies classes for both version 1 and version 2 [Performance Counters](/windows/desktop/PerfCtrs/performance-counters-portal).</span></span>

<span data-ttu-id="8dbf8-109">I contatori versione 1 si trovano nel registro di **sistema in HKEY \_ Local \_ Machine \\ System \\ CurrentControlSet \\ Services**.</span><span class="sxs-lookup"><span data-stu-id="8dbf8-109">Version 1 counters are found in the registry under **HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Services**.</span></span> <span data-ttu-id="8dbf8-110">I servizi che forniscono dati sulle prestazioni hanno una sottochiave **delle prestazioni** .</span><span class="sxs-lookup"><span data-stu-id="8dbf8-110">Services that provide performance data have a **Performance** subkey.</span></span> <span data-ttu-id="8dbf8-111">Le classi di prestazioni WMI create dai contatori della versione 1 non includono "contatori" come parte del nome.</span><span class="sxs-lookup"><span data-stu-id="8dbf8-111">WMI performance classes created from version 1 counters do not have "Counters" as part of their name.</span></span>

<span data-ttu-id="8dbf8-112">Il **GUID** che identifica un provider del contatore delle prestazioni versione 2 si trova nel registro di sistema in **HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Perflib \\ \_ V2Providers**.</span><span class="sxs-lookup"><span data-stu-id="8dbf8-112">The **GUID** s identifying a version 2 performance counter provider are found in the registry under **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Perflib\\\_V2Providers**.</span></span>

<span data-ttu-id="8dbf8-113">WMIPerfClass viene registrato come provider di classi WMI normale.</span><span class="sxs-lookup"><span data-stu-id="8dbf8-113">WMIPerfClass is registered as a normal WMI class provider.</span></span> <span data-ttu-id="8dbf8-114">WMIPerfInst è un provider di istanze WMI che fornisce dati dall'helper dei dati sulle prestazioni (PDH) per i contatori versione 1 e versione 2.</span><span class="sxs-lookup"><span data-stu-id="8dbf8-114">WMIPerfInst is a WMI instance provider that supplies data from Performance Data Helper (PDH) for both version 1 and version 2 counters.</span></span> <span data-ttu-id="8dbf8-115">Per ulteriori informazioni, vedere [utilizzo delle funzioni PDH per utilizzare i dati del contatore](/windows/desktop/PerfCtrs/using-the-pdh-functions-to-consume-counter-data).</span><span class="sxs-lookup"><span data-stu-id="8dbf8-115">For more information, see [Using the PDH Functions to Consume Counter Data](/windows/desktop/PerfCtrs/using-the-pdh-functions-to-consume-counter-data).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8dbf8-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8dbf8-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8dbf8-117">Informazioni su WMI</span><span class="sxs-lookup"><span data-stu-id="8dbf8-117">About WMI</span></span>](about-wmi.md)
</dt> <dt>

[<span data-ttu-id="8dbf8-118">Monitoraggio dei dati sulle prestazioni</span><span class="sxs-lookup"><span data-stu-id="8dbf8-118">Monitoring Performance Data</span></span>](monitoring-performance-data.md)
</dt> </dl>

 

 
