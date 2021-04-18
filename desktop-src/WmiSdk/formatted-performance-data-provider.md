---
description: Fornisce calcolato (&\# 0034; cotto&\# 0034;) dati del contatore delle prestazioni. Fornisce dati dinamici alle classi WMI derivate da Win32 \_ PerfFormattedData. Noto anche come provider di contatori cotti.
ms.assetid: 59823f7c-3046-4608-99df-1f43e2934e7e
ms.tgt_platform: multiple
title: provider di dati delle prestazioni formattate
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0db075ebdafcd31c7aa0980d191ed565873f686f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310352"
---
# <a name="formatted-performance-data-provider"></a><span data-ttu-id="c643c-105">provider di dati delle prestazioni formattate</span><span class="sxs-lookup"><span data-stu-id="c643c-105">Formatted Performance Data Provider</span></span>

<span data-ttu-id="c643c-106">\[Il provider di dati delle prestazioni formattato, noto anche come "provider del contatore cotto", non è più disponibile per l'uso.</span><span class="sxs-lookup"><span data-stu-id="c643c-106">\[The Formatted Performance Data Provider, also known as the "Cooked Counter Provider," is no longer available for use.</span></span> <span data-ttu-id="c643c-107">Usare invece il provider [wmiperfinst](wmiperfinst-provider.md) .\]</span><span class="sxs-lookup"><span data-stu-id="c643c-107">Instead, use the [WMIPerfInst](wmiperfinst-provider.md) provider.\]</span></span>

<span data-ttu-id="c643c-108">Il provider di dati prestazioni formattato a prestazioni elevate fornisce dati del contatore delle prestazioni calcolati (cotti), ad esempio la percentuale di tempo impiegato da un disco per la scrittura dei dati.</span><span class="sxs-lookup"><span data-stu-id="c643c-108">The high-performance Formatted Performance Data provider supplies calculated ("cooked") performance counter data, such as the percentage of time a disk spends writing data.</span></span> <span data-ttu-id="c643c-109">Questo provider fornisce dati dinamici alle classi WMI derivate da [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span><span class="sxs-lookup"><span data-stu-id="c643c-109">This provider supplies dynamic data to the WMI classes derived from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span></span> <span data-ttu-id="c643c-110">La differenza tra questo provider e il [provider del contatore delle](performance-counter-provider.md) prestazioni è che il provider del contatore delle prestazioni fornisce dati non elaborati e il provider del contatore cotto fornisce dati sulle prestazioni che vengono visualizzati esattamente come in [*Monitor di sistema*](gloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="c643c-110">The difference between this provider and the [Performance Counter provider](performance-counter-provider.md) is that the Performance Counter provider supplies raw data and the Cooked Counter provider supplies performance data that appears exactly as in [*System Monitor*](gloss-s.md).</span></span> <span data-ttu-id="c643c-111">Il nome dell'istanza di [**\_ \_ Win32Provider**](--win32provider.md) è "HiPerfCooker \_ V1".</span><span class="sxs-lookup"><span data-stu-id="c643c-111">The [**\_\_Win32Provider**](--win32provider.md) instance name is "HiPerfCooker\_v1".</span></span>

<span data-ttu-id="c643c-112">Il nome della classe formattata WMI per un oggetto contatore è nel formato " \_ nome \_ *oggetto \_ nome servizio* PerfFormattedData Win32 \_ *\_*".</span><span class="sxs-lookup"><span data-stu-id="c643c-112">The WMI formatted class name for a counter object is of the form "Win32\_PerfFormattedData\_*service\_name*\_*object\_name*".</span></span> <span data-ttu-id="c643c-113">Ad esempio, il nome della classe WMI che contiene i contatori del disco logico è **Win32 \_ PerfFormattedData \_ perfdisk \_ disco logico**.</span><span class="sxs-lookup"><span data-stu-id="c643c-113">For example, the WMI class name that contains the logical disk counters is **Win32\_PerfFormattedData\_PerfDisk\_LogicalDisk**.</span></span> <span data-ttu-id="c643c-114">Queste classi si trovano nello \\ spazio dei nomi "root CIMv2".</span><span class="sxs-lookup"><span data-stu-id="c643c-114">These classes are located in the "Root\\CIMv2" namespace.</span></span>

<span data-ttu-id="c643c-115">Poiché le classi di dati sulle prestazioni vengono aggiunte e modificate in modo dinamico in un determinato sistema, non è possibile documentare formalmente le proprietà di tutti gli oggetti prestazioni noti.</span><span class="sxs-lookup"><span data-stu-id="c643c-115">Because performance data classes are added and modified dynamically on a given system, it is not possible to formally document the properties of all known performance objects.</span></span> <span data-ttu-id="c643c-116">Per determinare quali classi sono disponibili e per identificare i membri di tali classi, vedere [recupero della documentazione per oggetti dati sulle prestazioni non elaborati e formattati](retrieving-raw-and-formatted-performance-data.md).</span><span class="sxs-lookup"><span data-stu-id="c643c-116">To determine what classes are available to you, and to identify what members those classes have, see [Retrieving Documentation for Raw and Formatted Performance Data Objects](retrieving-raw-and-formatted-performance-data.md).</span></span>

<span data-ttu-id="c643c-117">Le classi [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) utilizzano il qualificatore **CookingType** nei [tipi di contatori delle prestazioni WMI](wmi-performance-counter-types.md) per specificare la formula per il calcolo dei dati sulle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="c643c-117">The [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) classes use the **CookingType** qualifier in [WMI Performance Counter Types](wmi-performance-counter-types.md) to specify the formula for calculating performance data.</span></span> <span data-ttu-id="c643c-118">Questo qualificatore è uguale al qualificatore **CounterType** nelle classi [**\_ PerfRawData Win32**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) .</span><span class="sxs-lookup"><span data-stu-id="c643c-118">This qualifier is the same as the **CounterType** qualifier in the [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) classes.</span></span>

<span data-ttu-id="c643c-119">Come provider a prestazioni elevate, il provider del contatore cotto implementa l'interfaccia [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) standard, nonché il metodo [**IWbemRefresher:: Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) e i metodi [**IWbemHiPerfProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemhiperfprovider) seguenti:</span><span class="sxs-lookup"><span data-stu-id="c643c-119">As a high-performance provider, the Cooked Counter provider implements the standard [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) interface, as well as the [**IWbemRefresher::Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) method and the following [**IWbemHiPerfProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemhiperfprovider) methods:</span></span>

-   [<span data-ttu-id="c643c-120">**CreateRefreshableEnum**</span><span class="sxs-lookup"><span data-stu-id="c643c-120">**CreateRefreshableEnum**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableenum)
-   [<span data-ttu-id="c643c-121">**CreateRefreshableObject**</span><span class="sxs-lookup"><span data-stu-id="c643c-121">**CreateRefreshableObject**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableobject)
-   [<span data-ttu-id="c643c-122">**CreateRefresher**</span><span class="sxs-lookup"><span data-stu-id="c643c-122">**CreateRefresher**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefresher)
-   [<span data-ttu-id="c643c-123">**GetObjects**</span><span class="sxs-lookup"><span data-stu-id="c643c-123">**GetObjects**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-getobjects)
-   [<span data-ttu-id="c643c-124">**QueryInstances**</span><span class="sxs-lookup"><span data-stu-id="c643c-124">**QueryInstances**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-queryinstances)
-   [<span data-ttu-id="c643c-125">**StopRefreshing**</span><span class="sxs-lookup"><span data-stu-id="c643c-125">**StopRefreshing**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-stoprefreshing)

## <a name="related-topics"></a><span data-ttu-id="c643c-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c643c-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c643c-127">Provider WMI</span><span class="sxs-lookup"><span data-stu-id="c643c-127">WMI Providers</span></span>](wmi-providers.md)
</dt> </dl>

 

 
