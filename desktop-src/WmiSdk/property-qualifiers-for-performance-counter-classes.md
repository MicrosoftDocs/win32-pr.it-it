---
description: I qualificatori di proprietà specificano le informazioni sul contatore delle prestazioni a cui viene eseguito il mapping della proprietà.
ms.assetid: f1761f71-af4e-4b89-aba7-b7f294c30ffc
ms.tgt_platform: multiple
title: Qualificatori di proprietà per le classi dei contatori delle prestazioni
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4e060d072c34d248f9faf634aec7710f5638721b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233676"
---
# <a name="property-qualifiers-for-performance-counter-classes"></a><span data-ttu-id="4005e-103">Qualificatori di proprietà per le classi dei contatori delle prestazioni</span><span class="sxs-lookup"><span data-stu-id="4005e-103">Property Qualifiers for Performance Counter Classes</span></span>

<span data-ttu-id="4005e-104">I qualificatori di proprietà specificano le informazioni sul contatore delle prestazioni a cui viene eseguito il mapping della proprietà.</span><span class="sxs-lookup"><span data-stu-id="4005e-104">Property qualifiers specify information about the performance counter to which the property maps.</span></span>

-   [<span data-ttu-id="4005e-105">Qualificatori di proprietà per classi di prestazioni raw e formattate</span><span class="sxs-lookup"><span data-stu-id="4005e-105">Property Qualifiers for Raw and Formatted Performance Classes</span></span>](#property-qualifiers-for-raw-and-formatted-performance-classes)
-   [<span data-ttu-id="4005e-106">Qualificatori di proprietà per classi di prestazioni non elaborate</span><span class="sxs-lookup"><span data-stu-id="4005e-106">Property Qualifiers for Raw Performance Classes</span></span>](#property-qualifiers-for-raw-and-formatted-performance-classes)
-   [<span data-ttu-id="4005e-107">Qualificatori di proprietà per classi di prestazioni formattate</span><span class="sxs-lookup"><span data-stu-id="4005e-107">Property Qualifiers for Formatted Performance Classes</span></span>](#property-qualifiers-for-raw-and-formatted-performance-classes)
-   [<span data-ttu-id="4005e-108">Come interpretare i qualificatori di proprietà</span><span class="sxs-lookup"><span data-stu-id="4005e-108">How to Interpret Property Qualifiers</span></span>](#how-to-interpret-property-qualifiers)
-   [<span data-ttu-id="4005e-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4005e-109">Related topics</span></span>](#related-topics)

<span data-ttu-id="4005e-110">Il contatore delle prestazioni fa parte di un oggetto prestazioni rappresentato da un contatore delle prestazioni WMI. i qualificatori specifici del contatore [delle prestazioni vengono](/windows/desktop/CIMWin32Prov/performance-counter-classes) automaticamente associati al provider WbemPerfClass per le classi e le proprietà [**\_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) in \\ CIMv2 radice.</span><span class="sxs-lookup"><span data-stu-id="4005e-110">The performance counter is part of a performance object represented by a WMI [performance counter class](/windows/desktop/CIMWin32Prov/performance-counter-classes) Performance counter–specific qualifiers are automatically attached by the WbemPerfClass provider to [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) classes and properties in Root\\CIMv2.</span></span>

<span data-ttu-id="4005e-111">Queste informazioni si applicano a tutte le istanze della classe performance.</span><span class="sxs-lookup"><span data-stu-id="4005e-111">This information applies to all instances of the performance class.</span></span> <span data-ttu-id="4005e-112">Alcuni qualificatori con valori **booleani** sempre false potrebbero non essere presenti in classi specifiche.</span><span class="sxs-lookup"><span data-stu-id="4005e-112">Some qualifiers with **Boolean** values that are always false may not be present on specific classes.</span></span>

## <a name="property-qualifiers-for-raw-and-formatted-performance-classes"></a><span data-ttu-id="4005e-113">Qualificatori di proprietà per classi di prestazioni raw e formattate</span><span class="sxs-lookup"><span data-stu-id="4005e-113">Property Qualifiers for Raw and Formatted Performance Classes</span></span>

<span data-ttu-id="4005e-114">Nell'elenco seguente sono elencati i qualificatori che si applicano alle proprietà nelle classi derivate da [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) o [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span><span class="sxs-lookup"><span data-stu-id="4005e-114">The following list lists qualifiers that apply to properties in classes that are derived either from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) or [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span></span>

<dl> <dt>

<span data-ttu-id="4005e-115"><span id="CounterType"></span><span id="countertype"></span><span id="COUNTERTYPE"></span>[**CounterType**](countertype-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="4005e-115"><span id="CounterType"></span><span id="countertype"></span><span id="COUNTERTYPE"></span>[**CounterType**](countertype-qualifier.md)</span></span>
</dt> <dd>

<span data-ttu-id="4005e-116">**sint32**</span><span class="sxs-lookup"><span data-stu-id="4005e-116">**sint32**</span></span>

<span data-ttu-id="4005e-117">Valore intero nell'enumerazione del tipo di contatore, come definito in Winperf. h o Perflib. h.</span><span class="sxs-lookup"><span data-stu-id="4005e-117">Integer value in the counter type enumeration, as defined in Winperf.h or Perflib.h.</span></span> <span data-ttu-id="4005e-118">Il qualificatore [**CounterType**](countertype-qualifier.md)indica la formula o l'algoritmo utilizzato per calcolare il valore visualizzato in Monitor di sistema per il contatore rappresentato dalla proprietà.</span><span class="sxs-lookup"><span data-stu-id="4005e-118">The [**CounterType**](countertype-qualifier.md)qualifier indicates the formula or algorithm used to calculate the value shown in System Monitor for the counter which the property represents.</span></span>

</dd> <dt>

<span data-ttu-id="4005e-119"><span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="4005e-119"><span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>**DisplayName**</span></span>
</dt> <dd>

<span data-ttu-id="4005e-120">**string**</span><span class="sxs-lookup"><span data-stu-id="4005e-120">**string**</span></span>

<span data-ttu-id="4005e-121">Nome del contatore delle prestazioni, come specificato dall'helper dei dati sulle prestazioni (PDH).</span><span class="sxs-lookup"><span data-stu-id="4005e-121">The performance Counter name, as specified by Performance Data Helper (PDH).</span></span>

</dd> <dt>

<span data-ttu-id="4005e-122"><span id="HelpIndex"></span><span id="helpindex"></span><span id="HELPINDEX"></span>**HelpIndex**</span><span class="sxs-lookup"><span data-stu-id="4005e-122"><span id="HelpIndex"></span><span id="helpindex"></span><span id="HELPINDEX"></span>**HelpIndex**</span></span>
</dt> <dd>

<span data-ttu-id="4005e-123">**sint32**</span><span class="sxs-lookup"><span data-stu-id="4005e-123">**sint32**</span></span>

<span data-ttu-id="4005e-124">Non usato.</span><span class="sxs-lookup"><span data-stu-id="4005e-124">Not used.</span></span> <span data-ttu-id="4005e-125">Contiene sempre 0.</span><span class="sxs-lookup"><span data-stu-id="4005e-125">Always contains 0.</span></span>

</dd> <dt>

<span data-ttu-id="4005e-126"><span id="PerfIndex"></span><span id="perfindex"></span><span id="PERFINDEX"></span>**PerfIndex**</span><span class="sxs-lookup"><span data-stu-id="4005e-126"><span id="PerfIndex"></span><span id="perfindex"></span><span id="PERFINDEX"></span>**PerfIndex**</span></span>
</dt> <dd>

<span data-ttu-id="4005e-127">**sint32**</span><span class="sxs-lookup"><span data-stu-id="4005e-127">**sint32**</span></span>

<span data-ttu-id="4005e-128">Non usato.</span><span class="sxs-lookup"><span data-stu-id="4005e-128">Not used.</span></span> <span data-ttu-id="4005e-129">Contiene sempre 0.</span><span class="sxs-lookup"><span data-stu-id="4005e-129">Always contains 0.</span></span>

</dd> </dl>

## <a name="property-qualifiers-for-raw-performance-classes"></a><span data-ttu-id="4005e-130">Qualificatori di proprietà per classi di prestazioni non elaborate</span><span class="sxs-lookup"><span data-stu-id="4005e-130">Property Qualifiers for Raw Performance Classes</span></span>

<span data-ttu-id="4005e-131">Nell'elenco seguente sono elencati i qualificatori che si applicano a tutte le proprietà delle classi derivate da [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata).</span><span class="sxs-lookup"><span data-stu-id="4005e-131">The following list lists qualifiers that apply to all properties of classes that are derived from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata).</span></span>

<dl> <dt>

<span data-ttu-id="4005e-132"><span id="PerfDefault"></span><span id="perfdefault"></span><span id="PERFDEFAULT"></span>**PerfDefault**</span><span class="sxs-lookup"><span data-stu-id="4005e-132"><span id="PerfDefault"></span><span id="perfdefault"></span><span id="PERFDEFAULT"></span>**PerfDefault**</span></span>
</dt> <dd>

<span data-ttu-id="4005e-133">**boolean**</span><span class="sxs-lookup"><span data-stu-id="4005e-133">**boolean**</span></span>

<span data-ttu-id="4005e-134">Indica se questa proprietà è il contatore predefinito da utilizzare nelle caselle di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="4005e-134">Indicates whether this property is the default counter to use in list boxes.</span></span> <span data-ttu-id="4005e-135">Per impostazione predefinita, questo qualificatore è **false** per i contatori delle prestazioni versione 6,0 perché non forniscono dati.</span><span class="sxs-lookup"><span data-stu-id="4005e-135">This qualifier defaults to **False** for Performance Counters Version 6.0 because they do not supply data for it.</span></span> <span data-ttu-id="4005e-136">Per altre informazioni, vedere [i contatori delle prestazioni](/windows/desktop/PerfCtrs/performance-counters-portal).</span><span class="sxs-lookup"><span data-stu-id="4005e-136">For more information, see [Performance Counters](/windows/desktop/PerfCtrs/performance-counters-portal).</span></span>

</dd> <dt>

<span data-ttu-id="4005e-137"><span id="DefaultScale"></span><span id="defaultscale"></span><span id="DEFAULTSCALE"></span>**DefaultScale**</span><span class="sxs-lookup"><span data-stu-id="4005e-137"><span id="DefaultScale"></span><span id="defaultscale"></span><span id="DEFAULTSCALE"></span>**DefaultScale**</span></span>
</dt> <dd>

<span data-ttu-id="4005e-138">**sint32**</span><span class="sxs-lookup"><span data-stu-id="4005e-138">**sint32**</span></span>

<span data-ttu-id="4005e-139">Potenza di 10 da usare per la visualizzazione del contatore.</span><span class="sxs-lookup"><span data-stu-id="4005e-139">Power of 10 to use for display of the counter.</span></span> <span data-ttu-id="4005e-140">Per zero, il valore massimo stimato è 10 ^ 0 o 1.</span><span class="sxs-lookup"><span data-stu-id="4005e-140">For zero, the estimated maximum is 10^0, or 1.</span></span>

</dd> <dt>

<span data-ttu-id="4005e-141"><span id="PerfDetail"></span><span id="perfdetail"></span><span id="PERFDETAIL"></span>[**PerfDetail**](perfdetail-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="4005e-141"><span id="PerfDetail"></span><span id="perfdetail"></span><span id="PERFDETAIL"></span>[**PerfDetail**](perfdetail-qualifier.md)</span></span>
</dt> <dd>

<span data-ttu-id="4005e-142">**sint32**</span><span class="sxs-lookup"><span data-stu-id="4005e-142">**sint32**</span></span>

<span data-ttu-id="4005e-143">Livello di conoscenza del pubblico.</span><span class="sxs-lookup"><span data-stu-id="4005e-143">Audience level of knowledge.</span></span> <span data-ttu-id="4005e-144">Non usato.</span><span class="sxs-lookup"><span data-stu-id="4005e-144">Not used.</span></span> <span data-ttu-id="4005e-145">Il valore è sempre 100.</span><span class="sxs-lookup"><span data-stu-id="4005e-145">The value is always 100.</span></span>

</dd> </dl>

## <a name="property-qualifiers-for-formatted-performance-classes"></a><span data-ttu-id="4005e-146">Qualificatori di proprietà per classi di prestazioni formattate</span><span class="sxs-lookup"><span data-stu-id="4005e-146">Property Qualifiers for Formatted Performance Classes</span></span>

<span data-ttu-id="4005e-147">Nell'elenco seguente sono elencati i qualificatori che si applicano a tutte le proprietà delle classi derivate da [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span><span class="sxs-lookup"><span data-stu-id="4005e-147">The following list lists qualifiers that apply to all properties of classes that are derived from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span></span>

<dl> <dt>

<span data-ttu-id="4005e-148"><span id="CookingType"></span><span id="cookingtype"></span><span id="COOKINGTYPE"></span>**CookingType**</span><span class="sxs-lookup"><span data-stu-id="4005e-148"><span id="CookingType"></span><span id="cookingtype"></span><span id="COOKINGTYPE"></span>**CookingType**</span></span>
</dt> <dd>

<span data-ttu-id="4005e-149">**string**</span><span class="sxs-lookup"><span data-stu-id="4005e-149">**string**</span></span>

<span data-ttu-id="4005e-150">Tipo di formula usato per produrre il risultato.</span><span class="sxs-lookup"><span data-stu-id="4005e-150">Formula type used to produce the result.</span></span> <span data-ttu-id="4005e-151">Ogni tipo di contatore utilizza gli altri qualificatori di proprietà per calcolare il risultato visualizzato come valore della proprietà corrente.</span><span class="sxs-lookup"><span data-stu-id="4005e-151">Each counter type uses the other property qualifiers to calculate the result shown as the value of the current property.</span></span> <span data-ttu-id="4005e-152">I qualificatori **Counter**, **PerfTimeStamp** e **PerfTimeFreq** vengono mappati alle proprietà in una classe RAW che forniscono i dati.</span><span class="sxs-lookup"><span data-stu-id="4005e-152">The **Counter**, **PerfTimeStamp**, and **PerfTimeFreq** qualifiers map to properties in a raw class which supply the data.</span></span>

<span data-ttu-id="4005e-153">Per ulteriori informazioni, vedere [qualificatore CounterType](countertype-qualifier.md).</span><span class="sxs-lookup"><span data-stu-id="4005e-153">For more information, see [CounterType Qualifier](countertype-qualifier.md).</span></span>

</dd> <dt>

<span data-ttu-id="4005e-154"><span id="Counter"></span><span id="counter"></span><span id="COUNTER"></span>**Counter**</span><span class="sxs-lookup"><span data-stu-id="4005e-154"><span id="Counter"></span><span id="counter"></span><span id="COUNTER"></span>**Counter**</span></span>
</dt> <dd>

<span data-ttu-id="4005e-155">**string**</span><span class="sxs-lookup"><span data-stu-id="4005e-155">**string**</span></span>

<span data-ttu-id="4005e-156">Nome di una proprietà obbligatoria nella classe RAW corrispondente da utilizzare come valore del contatore nella formula di cottura.</span><span class="sxs-lookup"><span data-stu-id="4005e-156">Name of a required property in the corresponding raw class to use as the counter value in the cooking formula.</span></span> <span data-ttu-id="4005e-157">Il valore deve corrispondere al nome della proprietà dell'origine dati nella classe RAW corrispondente.</span><span class="sxs-lookup"><span data-stu-id="4005e-157">The value must be the property name of the data source property in the corresponding raw class.</span></span>

</dd> <dt>

<span data-ttu-id="4005e-158"><span id="PerfTimeStamp"></span><span id="perftimestamp"></span><span id="PERFTIMESTAMP"></span>**PerfTimeStamp**</span><span class="sxs-lookup"><span data-stu-id="4005e-158"><span id="PerfTimeStamp"></span><span id="perftimestamp"></span><span id="PERFTIMESTAMP"></span>**PerfTimeStamp**</span></span>
</dt> <dd>

<span data-ttu-id="4005e-159">**string**</span><span class="sxs-lookup"><span data-stu-id="4005e-159">**string**</span></span>

<span data-ttu-id="4005e-160">Nome di una proprietà in una classe RAW da utilizzare come frequenza nella formula di cottura.</span><span class="sxs-lookup"><span data-stu-id="4005e-160">Name of a property in a raw class to use as a frequency in the cooking formula.</span></span> <span data-ttu-id="4005e-161">Se questo qualificatore non è presente per la proprietà, verrà utilizzato il valore predefinito appropriato a livello di classe.</span><span class="sxs-lookup"><span data-stu-id="4005e-161">The appropriate default value at the class level will be used if this qualifier is not present for the property.</span></span> <span data-ttu-id="4005e-162">La frequenza rappresenta i cicli al secondo del timestamp.</span><span class="sxs-lookup"><span data-stu-id="4005e-162">The frequency represents the ticks per second of the time stamp.</span></span>

</dd> <dt>

<span data-ttu-id="4005e-163"><span id="PerfTimeFreq"></span><span id="perftimefreq"></span><span id="PERFTIMEFREQ"></span>**PerfTimeFreq**</span><span class="sxs-lookup"><span data-stu-id="4005e-163"><span id="PerfTimeFreq"></span><span id="perftimefreq"></span><span id="PERFTIMEFREQ"></span>**PerfTimeFreq**</span></span>
</dt> <dd>

<span data-ttu-id="4005e-164">**string**</span><span class="sxs-lookup"><span data-stu-id="4005e-164">**string**</span></span>

<span data-ttu-id="4005e-165">Nome di una proprietà in una classe RAW da utilizzare come timestamp nella formula di cottura.</span><span class="sxs-lookup"><span data-stu-id="4005e-165">Name of a property in a raw class to use as a timestamp in the cooking formula.</span></span> <span data-ttu-id="4005e-166">Se questo qualificatore non è presente per la proprietà, viene utilizzato il valore predefinito appropriato a livello di classe.</span><span class="sxs-lookup"><span data-stu-id="4005e-166">The appropriate default value at the class level is used if this qualifier is not present for the property.</span></span> <span data-ttu-id="4005e-167">Un timestamp generato automaticamente può comportare un errore in un calcolo perché il timestamp è un'approssimazione e non tiene conto dell'overhead causato dal marshalling e dalla raccolta di dati effettivi.</span><span class="sxs-lookup"><span data-stu-id="4005e-167">An automatically generated time stamp may introduce error in a calculation because the timestamp is an approximation and does not account for overhead incurred by marshaling and actual data collection.</span></span>

</dd> </dl>

## <a name="how-to-interpret-property-qualifiers"></a><span data-ttu-id="4005e-168">Come interpretare i qualificatori di proprietà</span><span class="sxs-lookup"><span data-stu-id="4005e-168">How to Interpret Property Qualifiers</span></span>

<span data-ttu-id="4005e-169">Le proprietà nelle classi [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) contengono i dati calcolati forniti dal [provider di dati delle prestazioni formattato](formatted-performance-data-provider.md).</span><span class="sxs-lookup"><span data-stu-id="4005e-169">Properties in the [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) classes contain the calculated data supplied by the [Formatted Performance Data Provider](formatted-performance-data-provider.md).</span></span> <span data-ttu-id="4005e-170">Il valore della proprietà è il risultato calcolato finale.</span><span class="sxs-lookup"><span data-stu-id="4005e-170">The property value is the final calculated result.</span></span> <span data-ttu-id="4005e-171">I qualificatori forniscono una ricetta.</span><span class="sxs-lookup"><span data-stu-id="4005e-171">The qualifiers supply a recipe.</span></span>

<span data-ttu-id="4005e-172">Il **contatore** e i qualificatori di **base** puntano alle origini dei dati e **CookingType** specifica la formula usata per produrre il risultato.</span><span class="sxs-lookup"><span data-stu-id="4005e-172">The **Counter** and **Base** qualifiers point to the sources of data and **CookingType** specifies the formula used to produce the result.</span></span> <span data-ttu-id="4005e-173">Il timestamp e la frequenza di campionamento provengono anche dalla classe RAW corrispondente e sono denominati in **PerfTimeStamp** e **PerfTimeFreq**.</span><span class="sxs-lookup"><span data-stu-id="4005e-173">The timestamp and sample frequency also come from the corresponding raw class and are named in **PerfTimeStamp** and **PerfTimeFreq**.</span></span>

<span data-ttu-id="4005e-174">Ad esempio, una delle classi formattate fornite da WMI, [**Win32 \_ PerfFormattedData \_ perfdisk \_ disco logico**](./retrieving-raw-and-formatted-performance-data.md), contiene una proprietà denominata **AvgDiskBytesPerRead**.</span><span class="sxs-lookup"><span data-stu-id="4005e-174">For example, one of the formatted classes supplied by WMI, [**Win32\_PerfFormattedData\_PerfDisk\_LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md), contains a property named **AvgDiskBytesPerRead**.</span></span> <span data-ttu-id="4005e-175">Il nome della proprietà nella classe formattata deve corrispondere alla proprietà della classe non elaborata.</span><span class="sxs-lookup"><span data-stu-id="4005e-175">The name of the property in the formatted class must be the same as the property in the raw class.</span></span> <span data-ttu-id="4005e-176">La proprietà **AvgDiskBytesPerRead** presenta i qualificatori seguenti.</span><span class="sxs-lookup"><span data-stu-id="4005e-176">The **AvgDiskBytesPerRead** property has the following qualifiers.</span></span>

<span data-ttu-id="4005e-177">Nell'elenco seguente sono elencati i qualificatori di proprietà disponibili per le proprietà di tutte le classi derivate da [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span><span class="sxs-lookup"><span data-stu-id="4005e-177">The following list lists the available property qualifiers for properties of all classes derived from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span></span>



| <span data-ttu-id="4005e-178">Qualifier</span><span class="sxs-lookup"><span data-stu-id="4005e-178">Qualifier</span></span>         | <span data-ttu-id="4005e-179">Valore</span><span class="sxs-lookup"><span data-stu-id="4005e-179">Value</span></span>                     |
|-------------------|---------------------------|
| <span data-ttu-id="4005e-180">**CookingType**</span><span class="sxs-lookup"><span data-stu-id="4005e-180">**CookingType**</span></span>   | <span data-ttu-id="4005e-181">media prestazioni in \_ \_ blocco</span><span class="sxs-lookup"><span data-stu-id="4005e-181">PERF\_AVERAGE\_BULK</span></span>       |
| <span data-ttu-id="4005e-182">**Contatore**</span><span class="sxs-lookup"><span data-stu-id="4005e-182">**Counter**</span></span>       | <span data-ttu-id="4005e-183">AvgDiskBytesPerRead</span><span class="sxs-lookup"><span data-stu-id="4005e-183">AvgDiskBytesPerRead</span></span>       |
| <span data-ttu-id="4005e-184">**PerfTimeStamp**</span><span class="sxs-lookup"><span data-stu-id="4005e-184">**PerfTimeStamp**</span></span> | <span data-ttu-id="4005e-185">Timestamp \_ PerfTime</span><span class="sxs-lookup"><span data-stu-id="4005e-185">Timestamp\_PerfTime</span></span>       |
| <span data-ttu-id="4005e-186">**PerfTimeFreq**</span><span class="sxs-lookup"><span data-stu-id="4005e-186">**PerfTimeFreq**</span></span>  | <span data-ttu-id="4005e-187">Frequenza \_ PerfTime</span><span class="sxs-lookup"><span data-stu-id="4005e-187">Frequency\_PerfTime</span></span>       |
| <span data-ttu-id="4005e-188">**PerfIndex**</span><span class="sxs-lookup"><span data-stu-id="4005e-188">**PerfIndex**</span></span>     | <span data-ttu-id="4005e-189">408</span><span class="sxs-lookup"><span data-stu-id="4005e-189">408</span></span>                       |
| <span data-ttu-id="4005e-190">**HelpIndex**</span><span class="sxs-lookup"><span data-stu-id="4005e-190">**HelpIndex**</span></span>     | <span data-ttu-id="4005e-191">409</span><span class="sxs-lookup"><span data-stu-id="4005e-191">409</span></span>                       |
| <span data-ttu-id="4005e-192">**Base**</span><span class="sxs-lookup"><span data-stu-id="4005e-192">**Base**</span></span>          | <span data-ttu-id="4005e-193">\_Base AvgDiskBytesPerRead</span><span class="sxs-lookup"><span data-stu-id="4005e-193">AvgDiskBytesPerRead\_Base</span></span> |



 

<span data-ttu-id="4005e-194">La proprietà **AvgDiskBytesPerRead** indica il numero medio di byte trasferiti dal disco durante le operazioni di lettura.</span><span class="sxs-lookup"><span data-stu-id="4005e-194">The **AvgDiskBytesPerRead** property reports the average number of bytes transferred from the disk during read operations.</span></span> <span data-ttu-id="4005e-195">La formula per la \_ media delle prestazioni \_ è:</span><span class="sxs-lookup"><span data-stu-id="4005e-195">The formula for PERF\_AVERAGE\_BULK is:</span></span>

<span data-ttu-id="4005e-196">(Sample2-Sample1)/(base sample2-base Sample1)</span><span class="sxs-lookup"><span data-stu-id="4005e-196">(Sample2 - Sample1) / (Base Sample2 - Base Sample1)</span></span>

<span data-ttu-id="4005e-197">L'operazione di lettura viene campionata in base alla frequenza specificata da **PerfTimeFreq** con il valore **PerfTimeStamp** che indica l'esempio più recente.</span><span class="sxs-lookup"><span data-stu-id="4005e-197">The read operation is sampled at the frequency specified by **PerfTimeFreq** with the **PerfTimeStamp** value indicating the most recent sample.</span></span> <span data-ttu-id="4005e-198">I dati del contatore non elaborati in byte vengono ricavati dalla proprietà **AvgDiskBytesPerRead** nella classe [**Win32 \_ PerfRawData \_ perfdisk \_ disco logico**](./retrieving-raw-and-formatted-performance-data.md) .</span><span class="sxs-lookup"><span data-stu-id="4005e-198">The raw counter data in bytes is taken from the **AvgDiskBytesPerRead** property in the [**Win32\_PerfRawData\_PerfDisk\_LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) class.</span></span> <span data-ttu-id="4005e-199">Il numero di base dei dati delle operazioni viene ricavato dalla proprietà di **\_ base AvgDiskBytesPerRead** nella stessa classe.</span><span class="sxs-lookup"><span data-stu-id="4005e-199">The base number of operations data is taken from the **AvgDiskBytesPerRead\_Base** property in that same class.</span></span>

<span data-ttu-id="4005e-200">Per ulteriori informazioni, vedere [acquisizione di dati statistici sulle prestazioni](obtaining-statistical-performance-data.md) e [monitoraggio dei dati sulle prestazioni](monitoring-performance-data.md).</span><span class="sxs-lookup"><span data-stu-id="4005e-200">For more information, see [Obtaining Statistical Performance Data](obtaining-statistical-performance-data.md) and [Monitoring Performance Data](monitoring-performance-data.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4005e-201">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4005e-201">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4005e-202">Monitoraggio dei dati sulle prestazioni</span><span class="sxs-lookup"><span data-stu-id="4005e-202">Monitoring Performance Data</span></span>](monitoring-performance-data.md)
</dt> <dt>

[<span data-ttu-id="4005e-203">Qualificatori specifici delle classi di prestazioni WMI</span><span class="sxs-lookup"><span data-stu-id="4005e-203">Qualifiers Specific to WMI Performance Classes</span></span>](qualifiers-specific-to-wmi-performance-classes.md)
</dt> <dt>

[<span data-ttu-id="4005e-204">Classi del contatore delle prestazioni</span><span class="sxs-lookup"><span data-stu-id="4005e-204">Performance Counter Classes</span></span>](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[<span data-ttu-id="4005e-205">Accesso alle classi di prestazioni preinstallate WMI</span><span class="sxs-lookup"><span data-stu-id="4005e-205">Accessing WMI Preinstalled Performance Classes</span></span>](accessing-wmi-preinstalled-performance-classes.md)
</dt> <dt>

[<span data-ttu-id="4005e-206">Attività WMI: monitoraggio delle prestazioni</span><span class="sxs-lookup"><span data-stu-id="4005e-206">WMI Tasks: Performance Monitoring</span></span>](wmi-tasks--performance-monitoring.md)
</dt> </dl>

 

 
