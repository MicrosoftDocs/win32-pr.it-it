---
description: Il provider del contatore delle prestazioni è un provider a prestazioni elevate che fornisce dati del contatore delle prestazioni non elaborati alle classi del contatore delle prestazioni WMI derivate da Win32 \_ PerfRawData. Il \_ \_ nome dell'istanza di Win32Provider è &\# 0034; NT5 \_ GenericPerfProvider \_ V1&\# 0034;.
ms.assetid: 2c7206e7-f5f8-4d40-b993-56122e48069b
ms.tgt_platform: multiple
title: Provider contatore prestazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9288da5ac20bff6340950ba2a3506d9128200cfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058221"
---
# <a name="performance-counter-provider"></a><span data-ttu-id="6577c-104">Provider contatore prestazioni</span><span class="sxs-lookup"><span data-stu-id="6577c-104">Performance Counter Provider</span></span>

<span data-ttu-id="6577c-105">\[Il provider del contatore delle prestazioni non è più disponibile per l'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="6577c-105">\[The Performance Counter Provider is no longer available for use.</span></span> <span data-ttu-id="6577c-106">Usare invece il provider [wmiperfinst](wmiperfinst-provider.md) .\]</span><span class="sxs-lookup"><span data-stu-id="6577c-106">Instead, use the [WMIPerfInst](wmiperfinst-provider.md) provider.\]</span></span>

<span data-ttu-id="6577c-107">Il provider del contatore delle prestazioni è un provider a prestazioni elevate che fornisce dati del contatore delle prestazioni non elaborati alle [classi del contatore delle prestazioni](/windows/desktop/CIMWin32Prov/performance-counter-classes) WMI derivate da [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata).</span><span class="sxs-lookup"><span data-stu-id="6577c-107">The Performance Counter provider is a high-performance provider that provides raw performance counter data to the WMI [Performance Counter Classes](/windows/desktop/CIMWin32Prov/performance-counter-classes) derived from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata).</span></span> <span data-ttu-id="6577c-108">Il nome dell'istanza di [**\_ \_ Win32Provider**](--win32provider.md) è "NT5 \_ GenericPerfProvider \_ V1".</span><span class="sxs-lookup"><span data-stu-id="6577c-108">The [**\_\_Win32Provider**](--win32provider.md) instance name is "NT5\_GenericPerfProvider\_V1".</span></span>

<span data-ttu-id="6577c-109">Le classi [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) si trovano nello \\ spazio dei nomi WMI "root CIMv2".</span><span class="sxs-lookup"><span data-stu-id="6577c-109">The [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) classes are located in the WMI "Root\\CIMv2" namespace.</span></span> <span data-ttu-id="6577c-110">Ogni classe di prestazioni WMI corrisponde a un oggetto prestazione in una libreria delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="6577c-110">Each WMI performance class corresponds to a performance object in a performance library.</span></span> <span data-ttu-id="6577c-111">Le proprietà di queste classi rappresentano i contatori per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="6577c-111">The properties of these classes represent the counters for the object.</span></span> <span data-ttu-id="6577c-112">Il nome della classe WMI per un oggetto contatore non elaborato ha il formato \*\* \_ Win32 \_ \_ PerfRawData\* nome servizio nome \_ *\_* oggetto \_ \* \* \*.</span><span class="sxs-lookup"><span data-stu-id="6577c-112">The WMI class name for a raw counter object is of the form \**Win32\_PerfRawData\_\_* service\_name *\_* object\_name\*\*\*.</span></span> <span data-ttu-id="6577c-113">Ad esempio, il nome della classe WMI che contiene i contatori del disco logico è [**Win32 \_ PerfRawData \_ perfdisk \_ disco logico**](./retrieving-raw-and-formatted-performance-data.md).</span><span class="sxs-lookup"><span data-stu-id="6577c-113">For example, the WMI class name that contains the logical disk counters is [**Win32\_PerfRawData\_PerfDisk\_LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md).</span></span>

<span data-ttu-id="6577c-114">È possibile utilizzare la classe [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) corrispondente per ottenere i dati sulle prestazioni pre-calcolati visualizzati in [*Monitor di sistema*](gloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="6577c-114">You can use the corresponding [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) class to get the pre-calculated performance data shown in [*System Monitor*](gloss-s.md).</span></span> <span data-ttu-id="6577c-115">Ad esempio, usare la classe [**Win32 \_ PerfFormattedData \_ perfdisk \_ disco logico**](./retrieving-raw-and-formatted-performance-data.md) per ottenere i dati del disco precalcolati.</span><span class="sxs-lookup"><span data-stu-id="6577c-115">For example, use the [**Win32\_PerfFormattedData\_PerfDisk\_LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) class to get pre-calculated disk data.</span></span>

<span data-ttu-id="6577c-116">Per ulteriori informazioni su come scrivere un client in grado di accedere ai dati sulle prestazioni non elaborati, vedere [accesso ai dati sulle prestazioni in C++](accessing-performance-data-in-c--.md).</span><span class="sxs-lookup"><span data-stu-id="6577c-116">For more information about how to write a client that can access raw performance data, see [Accessing Performance Data in C++](accessing-performance-data-in-c--.md).</span></span>

<span data-ttu-id="6577c-117">Come provider a prestazioni elevate, il provider del contatore delle prestazioni implementa l'interfaccia [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) standard, nonché il metodo [**IWbemRefresher:: Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) e i metodi [**IWbemHiPerfProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemhiperfprovider) seguenti:</span><span class="sxs-lookup"><span data-stu-id="6577c-117">As a high-performance provider, the Performance Counter provider implements the standard [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) interface, as well as the [**IWbemRefresher::Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) method and the following [**IWbemHiPerfProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemhiperfprovider) methods:</span></span>

-   [<span data-ttu-id="6577c-118">**CreateRefreshableEnum**</span><span class="sxs-lookup"><span data-stu-id="6577c-118">**CreateRefreshableEnum**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableenum)
-   [<span data-ttu-id="6577c-119">**CreateRefreshableObject**</span><span class="sxs-lookup"><span data-stu-id="6577c-119">**CreateRefreshableObject**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableobject)
-   [<span data-ttu-id="6577c-120">**CreateRefresher**</span><span class="sxs-lookup"><span data-stu-id="6577c-120">**CreateRefresher**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefresher)
-   [<span data-ttu-id="6577c-121">**GetObjects**</span><span class="sxs-lookup"><span data-stu-id="6577c-121">**GetObjects**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-getobjects)
-   [<span data-ttu-id="6577c-122">**QueryInstances**</span><span class="sxs-lookup"><span data-stu-id="6577c-122">**QueryInstances**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-queryinstances)
-   [<span data-ttu-id="6577c-123">**StopRefreshing**</span><span class="sxs-lookup"><span data-stu-id="6577c-123">**StopRefreshing**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-stoprefreshing)

## <a name="related-topics"></a><span data-ttu-id="6577c-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6577c-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6577c-125">Provider WMI</span><span class="sxs-lookup"><span data-stu-id="6577c-125">WMI Providers</span></span>](wmi-providers.md)
</dt> </dl>

 

 
