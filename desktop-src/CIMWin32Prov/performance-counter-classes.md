---
description: Le classi dei contatori delle prestazioni consentono l'accesso allo script e al programma ai dati sulle prestazioni del sistema calcolati dai provider a prestazioni elevate esistenti.
ms.assetid: 71746363-6fec-4344-8c5e-5cc057ebdf76
ms.tgt_platform: multiple
title: Classi del contatore delle prestazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d147e5ebc18dfe532ceec7a2fb55bb21c6fa13f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878390"
---
# <a name="performance-counter-classes"></a><span data-ttu-id="dfe76-103">Classi del contatore delle prestazioni</span><span class="sxs-lookup"><span data-stu-id="dfe76-103">Performance Counter Classes</span></span>

<span data-ttu-id="dfe76-104">Le classi dei contatori delle prestazioni consentono l'accesso allo script e al programma ai dati sulle prestazioni del sistema calcolati dai provider a prestazioni elevate esistenti.</span><span class="sxs-lookup"><span data-stu-id="dfe76-104">Performance Counter classes allow script and program access to system performance data calculated by existing high-performance providers.</span></span> <span data-ttu-id="dfe76-105">Queste classi sono costituite da classi di contatori delle prestazioni non elaborate e classi di contatori delle prestazioni formattate</span><span class="sxs-lookup"><span data-stu-id="dfe76-105">These classes consist of raw performance counter classes and formatted performance counter classes.</span></span>

<span data-ttu-id="dfe76-106">Provider diversi forniscono dati della libreria delle prestazioni tramite WMI.</span><span class="sxs-lookup"><span data-stu-id="dfe76-106">Different providers supply performance library data through WMI.</span></span> <span data-ttu-id="dfe76-107">I provider [wmiperfclass](/windows/desktop/WmiSdk/wmiperfclass-provider) e [wmiperfinst](/windows/desktop/WmiSdk/wmiperfinst-provider) forniscono classi per i [contatori delle prestazioni](/windows/desktop/PerfCtrs/performance-counters-portal)versione 1 e versione 2.</span><span class="sxs-lookup"><span data-stu-id="dfe76-107">The [WMIPerfClass](/windows/desktop/WmiSdk/wmiperfclass-provider) and [WMIPerfInst](/windows/desktop/WmiSdk/wmiperfinst-provider) providers supply classes for both version 1 and version 2 [Performance Counters](/windows/desktop/PerfCtrs/performance-counters-portal).</span></span> <span data-ttu-id="dfe76-108">Questi provider mantengono la compatibilità con le classi disponibili nei sistemi operativi precedenti.</span><span class="sxs-lookup"><span data-stu-id="dfe76-108">These providers maintain compatibility with the classes available in earlier operating systems.</span></span>

<span data-ttu-id="dfe76-109">Le classi in questa sezione sono le classi di base astratte utilizzate per creare classi dei contatori delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="dfe76-109">The classes in this section are the abstract base classes used to create performance counter classes.</span></span> <span data-ttu-id="dfe76-110">Non si tratta di un elenco completo delle classi che è possibile trovare nel sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="dfe76-110">This is not a complete list of classes that you may find on your operating system.</span></span> <span data-ttu-id="dfe76-111">Per ulteriori informazioni, vedere [librerie di prestazioni e WMI](/windows/desktop/WmiSdk/performance-libraries-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="dfe76-111">For more information, see [Performance Libraries and WMI](/windows/desktop/WmiSdk/performance-libraries-and-wmi).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="dfe76-112">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="dfe76-112">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="dfe76-113">**\_Prestazioni Win32**</span><span class="sxs-lookup"><span data-stu-id="dfe76-113">**Win32\_Perf**</span></span>](win32-perf.md)
</dt> <dd>

<span data-ttu-id="dfe76-114">Classe base per le classi del contatore delle prestazioni [**Win32 \_ PerfRawData**](win32-perfrawdata.md) e [**Win32 \_ PerfFormattedData**](win32-perfformatteddata.md).</span><span class="sxs-lookup"><span data-stu-id="dfe76-114">The base class for the performance counter classes [**Win32\_PerfRawData**](win32-perfrawdata.md) and [**Win32\_PerfFormattedData**](win32-perfformatteddata.md).</span></span>

</dd> <dt>

[<span data-ttu-id="dfe76-115">**\_PerfFormattedData Win32**</span><span class="sxs-lookup"><span data-stu-id="dfe76-115">**Win32\_PerfFormattedData**</span></span>](win32-perfformatteddata.md)
</dt> <dd>

<span data-ttu-id="dfe76-116">classe di base astratta per le classi di dati calcolate pre-installate.</span><span class="sxs-lookup"><span data-stu-id="dfe76-116">an abstract base class for the pre-installed, calculated data classes.</span></span>

</dd> <dt>

[<span data-ttu-id="dfe76-117">**\_PerfRawData Win32**</span><span class="sxs-lookup"><span data-stu-id="dfe76-117">**Win32\_PerfRawData**</span></span>](win32-perfrawdata.md)
</dt> <dd>

<span data-ttu-id="dfe76-118">Classe di base astratta per tutte le classi del contatore delle prestazioni raw concrete.</span><span class="sxs-lookup"><span data-stu-id="dfe76-118">The abstract base class for all concrete raw performance counter classes.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="dfe76-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="dfe76-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dfe76-120">Classi Win32</span><span class="sxs-lookup"><span data-stu-id="dfe76-120">Win32 Classes</span></span>](win32-provider.md)
</dt> </dl>

 

 
