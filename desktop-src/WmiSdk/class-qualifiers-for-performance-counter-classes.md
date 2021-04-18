---
description: Specificare le informazioni sull'oggetto prestazione a cui viene mappata la classe del contatore delle prestazioni WMI.
ms.assetid: 7b8b7f00-95d8-4c1e-8638-157d0f4c7c32
ms.tgt_platform: multiple
title: Qualificatori di classe per le classi dei contatori delle prestazioni
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e4910af88ce7f96fda1b5f9b7ecd7a33479fc130
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315243"
---
# <a name="class-qualifiers-for-performance-counter-classes"></a><span data-ttu-id="08cf4-103">Qualificatori di classe per le classi dei contatori delle prestazioni</span><span class="sxs-lookup"><span data-stu-id="08cf4-103">Class Qualifiers for Performance Counter Classes</span></span>

<span data-ttu-id="08cf4-104">I qualificatori di classe specificano le informazioni sull'oggetto prestazione a cui viene mappata la [classe del contatore delle prestazioni](/windows/desktop/CIMWin32Prov/performance-counter-classes) WMI.</span><span class="sxs-lookup"><span data-stu-id="08cf4-104">Class qualifiers specify information about the performance object to which the WMI [performance counter class](/windows/desktop/CIMWin32Prov/performance-counter-classes) is mapped.</span></span> <span data-ttu-id="08cf4-105">Per ulteriori informazioni, vedere [monitoraggio dei dati sulle prestazioni](monitoring-performance-data.md).</span><span class="sxs-lookup"><span data-stu-id="08cf4-105">For more information, see [Monitoring Performance Data](monitoring-performance-data.md).</span></span>

-   [<span data-ttu-id="08cf4-106">Qualificatori per PerformanceClasses RAW e formattati</span><span class="sxs-lookup"><span data-stu-id="08cf4-106">Qualifiers for Raw and Formatted PerformanceClasses</span></span>](#qualifiers-for-raw-and-formatted-performanceclasses)
-   [<span data-ttu-id="08cf4-107">Qualificatori per le classi di prestazioni non elaborate</span><span class="sxs-lookup"><span data-stu-id="08cf4-107">Qualifiers for Raw Performance Classes</span></span>](#)
-   [<span data-ttu-id="08cf4-108">Qualificatori per classi di prestazioni formattate</span><span class="sxs-lookup"><span data-stu-id="08cf4-108">Qualifiers for Formatted Performance Classes</span></span>](#)
-   [<span data-ttu-id="08cf4-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="08cf4-109">Related topics</span></span>](#related-topics)


<span data-ttu-id="08cf4-110">I qualificatori specifici del contatore delle prestazioni vengono automaticamente collegati dal provider "WbemPerfClass" alle classi e alle proprietà [**\_ PerfRawData Win32**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) in \\ CIMv2 radice.</span><span class="sxs-lookup"><span data-stu-id="08cf4-110">Performance counter–specific qualifiers are automatically attached by the "WbemPerfClass" provider to [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) classes and properties in Root\\CIMv2.</span></span>

<span data-ttu-id="08cf4-111">Queste informazioni si applicano a tutte le istanze della classe.</span><span class="sxs-lookup"><span data-stu-id="08cf4-111">This information applies to all instances of the class.</span></span> <span data-ttu-id="08cf4-112">Alcuni qualificatori con valori **booleani** sempre **false** potrebbero non essere presenti in classi specifiche.</span><span class="sxs-lookup"><span data-stu-id="08cf4-112">Some qualifiers with **Boolean** values that are always **False** may not be present on specific classes.</span></span>

## <a name="qualifiers-for-raw-and-formatted-performanceclasses"></a><span data-ttu-id="08cf4-113">Qualificatori per PerformanceClasses RAW e formattati</span><span class="sxs-lookup"><span data-stu-id="08cf4-113">Qualifiers for Raw and Formatted PerformanceClasses</span></span>

<span data-ttu-id="08cf4-114">I qualificatori seguenti si applicano a tutte le classi derivate da [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) e [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span><span class="sxs-lookup"><span data-stu-id="08cf4-114">The following qualifiers apply to all classes that are derived from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) and [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span></span>

<dl> <dt>

<span data-ttu-id="08cf4-115"><span id="Cooked"></span><span id="cooked"></span><span id="COOKED"></span>**Cotto**</span><span class="sxs-lookup"><span data-stu-id="08cf4-115"><span id="Cooked"></span><span id="cooked"></span><span id="COOKED"></span>**Cooked**</span></span>
</dt> <dd>

<span data-ttu-id="08cf4-116">**boolean**</span><span class="sxs-lookup"><span data-stu-id="08cf4-116">**boolean**</span></span>

<span data-ttu-id="08cf4-117">Indica se la classe contiene dati cotti.</span><span class="sxs-lookup"><span data-stu-id="08cf4-117">Indicates whether the class contains cooked data.</span></span>

</dd> <dt>

<span data-ttu-id="08cf4-118"><span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="08cf4-118"><span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>**DisplayName**</span></span>
</dt> <dd>

<span data-ttu-id="08cf4-119">**string**</span><span class="sxs-lookup"><span data-stu-id="08cf4-119">**string**</span></span>

<span data-ttu-id="08cf4-120">Nome dell'oggetto prestazioni.</span><span class="sxs-lookup"><span data-stu-id="08cf4-120">Performance object name.</span></span> <span data-ttu-id="08cf4-121">Per altre informazioni, vedere [i contatori delle prestazioni](/windows/desktop/PerfCtrs/performance-counters-portal).</span><span class="sxs-lookup"><span data-stu-id="08cf4-121">For more information, see [Performance Counters](/windows/desktop/PerfCtrs/performance-counters-portal).</span></span>

</dd> <dt>

<span data-ttu-id="08cf4-122"><span id="DetailLevel"></span><span id="detaillevel"></span><span id="DETAILLEVEL"></span>**DetailLevel**</span><span class="sxs-lookup"><span data-stu-id="08cf4-122"><span id="DetailLevel"></span><span id="detaillevel"></span><span id="DETAILLEVEL"></span>**DetailLevel**</span></span>
</dt> <dd>

<span data-ttu-id="08cf4-123">**sint32**</span><span class="sxs-lookup"><span data-stu-id="08cf4-123">**sint32**</span></span>

<span data-ttu-id="08cf4-124">Non fornisce dati dettaglio.</span><span class="sxs-lookup"><span data-stu-id="08cf4-124">Does not provide detail data.</span></span> <span data-ttu-id="08cf4-125">Contiene sempre il valore 100.</span><span class="sxs-lookup"><span data-stu-id="08cf4-125">Always contains value of 100.</span></span>

</dd> <dt>

<span data-ttu-id="08cf4-126"><span id="Dynamic"></span><span id="dynamic"></span><span id="DYNAMIC"></span>**Dinamico**</span><span class="sxs-lookup"><span data-stu-id="08cf4-126"><span id="Dynamic"></span><span id="dynamic"></span><span id="DYNAMIC"></span>**Dynamic**</span></span>
</dt> <dd>

<span data-ttu-id="08cf4-127">**boolean**</span><span class="sxs-lookup"><span data-stu-id="08cf4-127">**boolean**</span></span>

<span data-ttu-id="08cf4-128">Sempre impostato su **true** perché le istanze sono sempre dinamiche.</span><span class="sxs-lookup"><span data-stu-id="08cf4-128">Always set to **True** because instances are always dynamic.</span></span>

</dd> <dt>

<span data-ttu-id="08cf4-129"><span id="GenericPerfCtr"></span><span id="genericperfctr"></span><span id="GENERICPERFCTR"></span>**GenericPerfCtr**</span><span class="sxs-lookup"><span data-stu-id="08cf4-129"><span id="GenericPerfCtr"></span><span id="genericperfctr"></span><span id="GENERICPERFCTR"></span>**GenericPerfCtr**</span></span>
</dt> <dd>

<span data-ttu-id="08cf4-130">**boolean**</span><span class="sxs-lookup"><span data-stu-id="08cf4-130">**boolean**</span></span>

<span data-ttu-id="08cf4-131">Indica se la classe deriva da una libreria delle prestazioni legacy.</span><span class="sxs-lookup"><span data-stu-id="08cf4-131">Indicates whether the class comes from a legacy performance library.</span></span> <span data-ttu-id="08cf4-132">Sempre impostato su **true**.</span><span class="sxs-lookup"><span data-stu-id="08cf4-132">Always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="08cf4-133"><span id="HelpIndex"></span><span id="helpindex"></span><span id="HELPINDEX"></span>**HelpIndex**</span><span class="sxs-lookup"><span data-stu-id="08cf4-133"><span id="HelpIndex"></span><span id="helpindex"></span><span id="HELPINDEX"></span>**HelpIndex**</span></span>
</dt> <dd>

<span data-ttu-id="08cf4-134">**sint32**</span><span class="sxs-lookup"><span data-stu-id="08cf4-134">**sint32**</span></span>

<span data-ttu-id="08cf4-135">Gli indici non sono più validi.</span><span class="sxs-lookup"><span data-stu-id="08cf4-135">Indexes are no longer valid.</span></span> <span data-ttu-id="08cf4-136">Questo qualificatore è sempre zero.</span><span class="sxs-lookup"><span data-stu-id="08cf4-136">This qualifier is always zero.</span></span>

</dd> <dt>

<span data-ttu-id="08cf4-137"><span id="HiPerf_"></span><span id="hiperf_"></span><span id="HIPERF_"></span>**HiPerf**</span><span class="sxs-lookup"><span data-stu-id="08cf4-137"><span id="HiPerf_"></span><span id="hiperf_"></span><span id="HIPERF_"></span>**HiPerf**</span></span> 
</dt> <dd>

<span data-ttu-id="08cf4-138">**boolean**</span><span class="sxs-lookup"><span data-stu-id="08cf4-138">**boolean**</span></span>

<span data-ttu-id="08cf4-139">Indica che la classe è una classe a prestazioni elevate.</span><span class="sxs-lookup"><span data-stu-id="08cf4-139">Indicates that the class is a high-performance class.</span></span> <span data-ttu-id="08cf4-140">Sempre impostato su **true**.</span><span class="sxs-lookup"><span data-stu-id="08cf4-140">Always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="08cf4-141"><span id="Locale"></span><span id="locale"></span><span id="LOCALE"></span>**Locale**</span><span class="sxs-lookup"><span data-stu-id="08cf4-141"><span id="Locale"></span><span id="locale"></span><span id="LOCALE"></span>**Locale**</span></span>
</dt> <dd>

<span data-ttu-id="08cf4-142">**sint32**</span><span class="sxs-lookup"><span data-stu-id="08cf4-142">**sint32**</span></span>

<span data-ttu-id="08cf4-143">Identificatore delle impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="08cf4-143">Locale identifier.</span></span> <span data-ttu-id="08cf4-144">Il valore è sempre 1033 (Inglese (Stati Uniti).</span><span class="sxs-lookup"><span data-stu-id="08cf4-144">Value is always 1033 (U.S. English).</span></span>

</dd> <dt>

<span data-ttu-id="08cf4-145"><span id="PerfIndex"></span><span id="perfindex"></span><span id="PERFINDEX"></span>**PerfIndex**</span><span class="sxs-lookup"><span data-stu-id="08cf4-145"><span id="PerfIndex"></span><span id="perfindex"></span><span id="PERFINDEX"></span>**PerfIndex**</span></span>
</dt> <dd>

<span data-ttu-id="08cf4-146">**int32**</span><span class="sxs-lookup"><span data-stu-id="08cf4-146">**int32**</span></span>

<span data-ttu-id="08cf4-147">Gli indici non sono più validi.</span><span class="sxs-lookup"><span data-stu-id="08cf4-147">Indexes are no longer valid.</span></span> <span data-ttu-id="08cf4-148">Questo qualificatore è sempre zero.</span><span class="sxs-lookup"><span data-stu-id="08cf4-148">This qualifier is always zero.</span></span>

</dd> <dt>

<span data-ttu-id="08cf4-149"><span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>**Provider**</span><span class="sxs-lookup"><span data-stu-id="08cf4-149"><span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>**Provider**</span></span>
</dt> <dd>

<span data-ttu-id="08cf4-150">**string**</span><span class="sxs-lookup"><span data-stu-id="08cf4-150">**string**</span></span>

<span data-ttu-id="08cf4-151">Nome del provider di istanze.</span><span class="sxs-lookup"><span data-stu-id="08cf4-151">Name of the instance provider.</span></span> <span data-ttu-id="08cf4-152">Il valore è "WbemPerfV2".</span><span class="sxs-lookup"><span data-stu-id="08cf4-152">Value is "WbemPerfV2".</span></span>

</dd> <dt>

<span data-ttu-id="08cf4-153"><span id="RegistryKey"></span><span id="registrykey"></span><span id="REGISTRYKEY"></span>**RegistryKey**</span><span class="sxs-lookup"><span data-stu-id="08cf4-153"><span id="RegistryKey"></span><span id="registrykey"></span><span id="REGISTRYKEY"></span>**RegistryKey**</span></span>
</dt> <dd>

<span data-ttu-id="08cf4-154">**string**</span><span class="sxs-lookup"><span data-stu-id="08cf4-154">**string**</span></span>

<span data-ttu-id="08cf4-155">Nome del driver nella chiave dei **\_ \_ \\ \\ Servizi CurrentControlSet del computer locale HKEY** , in cui è possibile trovare la chiave delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="08cf4-155">Name of the driver in the **HKEY\_LOCAL\_MACHINE\\CurrentControlSet\\Services** key, under which the performance key can be located.</span></span> <span data-ttu-id="08cf4-156">Questo nome è anche il nome del servizio che fornisce il contatore delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="08cf4-156">This name is also the name of the service that provides the performance counter.</span></span>

</dd> <dt>

<span data-ttu-id="08cf4-157"><span id="Singleton"></span><span id="singleton"></span><span id="SINGLETON"></span>**Singleton**</span><span class="sxs-lookup"><span data-stu-id="08cf4-157"><span id="Singleton"></span><span id="singleton"></span><span id="SINGLETON"></span>**Singleton**</span></span>
</dt> <dd>

<span data-ttu-id="08cf4-158">**boolean**</span><span class="sxs-lookup"><span data-stu-id="08cf4-158">**boolean**</span></span>

<span data-ttu-id="08cf4-159">Se **true**, indica che esiste una sola istanza della classe.</span><span class="sxs-lookup"><span data-stu-id="08cf4-159">If **True**, indicates that only a single instance of the class exists.</span></span>

</dd> </dl>

## <a name="qualifiers-for-raw-performance-classes"></a><span data-ttu-id="08cf4-160">Qualificatori per le classi di prestazioni non elaborate</span><span class="sxs-lookup"><span data-stu-id="08cf4-160">Qualifiers for Raw Performance Classes</span></span>

<span data-ttu-id="08cf4-161">I qualificatori seguenti si applicano a tutte le classi derivate da [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata).</span><span class="sxs-lookup"><span data-stu-id="08cf4-161">The following qualifiers apply to all classes that are derived from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata).</span></span>

<dl> <dt>

<span data-ttu-id="08cf4-162"><span id="Costly"></span><span id="costly"></span><span id="COSTLY"></span>**Costose**</span><span class="sxs-lookup"><span data-stu-id="08cf4-162"><span id="Costly"></span><span id="costly"></span><span id="COSTLY"></span>**Costly**</span></span>
</dt> <dd>

<span data-ttu-id="08cf4-163">**boolean**</span><span class="sxs-lookup"><span data-stu-id="08cf4-163">**boolean**</span></span>

<span data-ttu-id="08cf4-164">Indica se il recupero di istanze di questa classe è un'operazione costosa.</span><span class="sxs-lookup"><span data-stu-id="08cf4-164">Indicates whether obtaining instances of this class is a costly operation.</span></span> <span data-ttu-id="08cf4-165">Sempre impostato su **true** per le classi con " \_ costose" accodato alla fine del nome della classe.</span><span class="sxs-lookup"><span data-stu-id="08cf4-165">Always set to **True** for classes with "\_Costly" appended to the end of the class name.</span></span>

</dd> <dt>

<span data-ttu-id="08cf4-166"><span id="DetailLevel"></span><span id="detaillevel"></span><span id="DETAILLEVEL"></span>**DetailLevel**</span><span class="sxs-lookup"><span data-stu-id="08cf4-166"><span id="DetailLevel"></span><span id="detaillevel"></span><span id="DETAILLEVEL"></span>**DetailLevel**</span></span>
</dt> <dd>

<span data-ttu-id="08cf4-167">**uint32**</span><span class="sxs-lookup"><span data-stu-id="08cf4-167">**uint32**</span></span>

<span data-ttu-id="08cf4-168">Non fornisce dati dettaglio.</span><span class="sxs-lookup"><span data-stu-id="08cf4-168">Does not provide detail data.</span></span> <span data-ttu-id="08cf4-169">Contiene sempre il valore 100.</span><span class="sxs-lookup"><span data-stu-id="08cf4-169">Always contains value of 100.</span></span>

</dd> <dt>

<span data-ttu-id="08cf4-170"><span id="PerfDefault"></span><span id="perfdefault"></span><span id="PERFDEFAULT"></span>**PerfDefault**</span><span class="sxs-lookup"><span data-stu-id="08cf4-170"><span id="PerfDefault"></span><span id="perfdefault"></span><span id="PERFDEFAULT"></span>**PerfDefault**</span></span>
</dt> <dd>

<span data-ttu-id="08cf4-171">**boolean**</span><span class="sxs-lookup"><span data-stu-id="08cf4-171">**boolean**</span></span>

<span data-ttu-id="08cf4-172">Il valore è sempre **false**.</span><span class="sxs-lookup"><span data-stu-id="08cf4-172">Value is always **False**.</span></span>

</dd> </dl>

## <a name="qualifiers-for-formatted-performance-classes"></a><span data-ttu-id="08cf4-173">Qualificatori per classi di prestazioni formattate</span><span class="sxs-lookup"><span data-stu-id="08cf4-173">Qualifiers for Formatted Performance Classes</span></span>

<span data-ttu-id="08cf4-174">I qualificatori seguenti si applicano a tutte le classi derivate da [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span><span class="sxs-lookup"><span data-stu-id="08cf4-174">The following qualifiers apply to all classes that are derived from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span></span>

<dl> <dt>

<span data-ttu-id="08cf4-175"><span id="AutoCook"></span><span id="autocook"></span><span id="AUTOCOOK"></span>**Autocook**</span><span class="sxs-lookup"><span data-stu-id="08cf4-175"><span id="AutoCook"></span><span id="autocook"></span><span id="AUTOCOOK"></span>**AutoCook**</span></span>
</dt> <dd>

<span data-ttu-id="08cf4-176">**int32**</span><span class="sxs-lookup"><span data-stu-id="08cf4-176">**int32**</span></span>

<span data-ttu-id="08cf4-177">Indica che i valori nelle istanze della classe vengono calcolati automaticamente dalla classe di dati RAW corrispondente.</span><span class="sxs-lookup"><span data-stu-id="08cf4-177">Indicates that the values in class instances are automatically calculated from the corresponding raw data class.</span></span> <span data-ttu-id="08cf4-178">Il valore è sempre 1.</span><span class="sxs-lookup"><span data-stu-id="08cf4-178">Value is always 1.</span></span>

</dd> <dt>

<span data-ttu-id="08cf4-179"><span id="AutoCook_RawClass"></span><span id="autocook_rawclass"></span><span id="AUTOCOOK_RAWCLASS"></span>**RawClass autocook \_**</span><span class="sxs-lookup"><span data-stu-id="08cf4-179"><span id="AutoCook_RawClass"></span><span id="autocook_rawclass"></span><span id="AUTOCOOK_RAWCLASS"></span>**AutoCook\_RawClass**</span></span>
</dt> <dd>

<span data-ttu-id="08cf4-180">**string**</span><span class="sxs-lookup"><span data-stu-id="08cf4-180">**string**</span></span>

<span data-ttu-id="08cf4-181">Nome della classe non elaborata da utilizzare per il calcolo della classe formattata.</span><span class="sxs-lookup"><span data-stu-id="08cf4-181">Name of the raw class to use for calculation for the formatted class.</span></span> <span data-ttu-id="08cf4-182">Questo qualificatore è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="08cf4-182">This qualifier is required.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="08cf4-183">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="08cf4-183">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08cf4-184">Monitoraggio dei dati sulle prestazioni</span><span class="sxs-lookup"><span data-stu-id="08cf4-184">Monitoring Performance Data</span></span>](monitoring-performance-data.md)
</dt> <dt>

[<span data-ttu-id="08cf4-185">Qualificatori specifici delle classi di prestazioni WMI</span><span class="sxs-lookup"><span data-stu-id="08cf4-185">Qualifiers Specific to WMI Performance Classes</span></span>](qualifiers-specific-to-wmi-performance-classes.md)
</dt> <dt>

[<span data-ttu-id="08cf4-186">Classi del contatore delle prestazioni</span><span class="sxs-lookup"><span data-stu-id="08cf4-186">Performance Counter Classes</span></span>](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[<span data-ttu-id="08cf4-187">Accesso alle classi di prestazioni preinstallate WMI</span><span class="sxs-lookup"><span data-stu-id="08cf4-187">Accessing WMI Preinstalled Performance Classes</span></span>](accessing-wmi-preinstalled-performance-classes.md)
</dt> <dt>

[<span data-ttu-id="08cf4-188">Attività WMI: monitoraggio delle prestazioni</span><span class="sxs-lookup"><span data-stu-id="08cf4-188">WMI Tasks: Performance Monitoring</span></span>](wmi-tasks--performance-monitoring.md)
</dt> </dl>

 

 
