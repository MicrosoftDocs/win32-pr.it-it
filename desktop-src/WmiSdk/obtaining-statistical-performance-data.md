---
description: In WMI è possibile definire dati statistici sulle prestazioni in base ai dati in classi di prestazioni formattate derivate da Win32 \_ PerfFormattedData. Le statistiche disponibili sono medio, minimo, massimo, intervallo e varianza, come definito nei tipi di contatori statistici.
ms.assetid: 5552d5fc-df8c-4353-8593-c106ee19dc84
ms.tgt_platform: multiple
title: Recupero di dati statistici sulle prestazioni
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 65892608e642b675440d81127ef9afa0badd1d36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128075"
---
# <a name="obtaining-statistical-performance-data"></a><span data-ttu-id="8af3f-104">Recupero di dati statistici sulle prestazioni</span><span class="sxs-lookup"><span data-stu-id="8af3f-104">Obtaining Statistical Performance Data</span></span>

<span data-ttu-id="8af3f-105">In WMI è possibile definire dati statistici sulle prestazioni in base ai dati in classi di prestazioni formattate derivate da [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span><span class="sxs-lookup"><span data-stu-id="8af3f-105">In WMI, you can define statistical performance data based on data in formatted performance classes derived from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span></span> <span data-ttu-id="8af3f-106">Le statistiche disponibili sono medio, minimo, massimo, intervallo e varianza, come definito nei [tipi di contatori statistici](statistical-counter-types.md).</span><span class="sxs-lookup"><span data-stu-id="8af3f-106">The available statistics are average, minimum, maximum, range, and variance, as defined in [Statistical Counter Types](statistical-counter-types.md).</span></span>

<span data-ttu-id="8af3f-107">Nell'elenco seguente sono inclusi i tipi di contatori statistici speciali:</span><span class="sxs-lookup"><span data-stu-id="8af3f-107">The following list includes the special statistical counter types:</span></span>

-   [<span data-ttu-id="8af3f-108">media COOKer \_</span><span class="sxs-lookup"><span data-stu-id="8af3f-108">COOKER\_AVERAGE</span></span>](cooker-average.md)
-   [<span data-ttu-id="8af3f-109">MIN COOKer \_</span><span class="sxs-lookup"><span data-stu-id="8af3f-109">COOKER\_MIN</span></span>](cooker-min.md)
-   [<span data-ttu-id="8af3f-110">massimo COOKer \_</span><span class="sxs-lookup"><span data-stu-id="8af3f-110">COOKER\_MAX</span></span>](cooker-max.md)
-   [<span data-ttu-id="8af3f-111">intervallo di cottura \_</span><span class="sxs-lookup"><span data-stu-id="8af3f-111">COOKER\_RANGE</span></span>](cooker-range.md)
-   [<span data-ttu-id="8af3f-112">varianza del COOKer \_</span><span class="sxs-lookup"><span data-stu-id="8af3f-112">COOKER\_VARIANCE</span></span>](cooker-variance.md)

<span data-ttu-id="8af3f-113">Gli esempi seguenti illustrano come:</span><span class="sxs-lookup"><span data-stu-id="8af3f-113">The following examples show how to:</span></span>

-   <span data-ttu-id="8af3f-114">Creare un file MOF che definisce una classe di dati calcolati.</span><span class="sxs-lookup"><span data-stu-id="8af3f-114">Create a MOF file that defines a class of calculated data.</span></span>
-   <span data-ttu-id="8af3f-115">Scrivere uno script che crea un'istanza della classe e aggiorna periodicamente i dati nell'istanza di con i valori statistici ricalcolati.</span><span class="sxs-lookup"><span data-stu-id="8af3f-115">Write a script that creates an instance of the class, and periodically refreshes the data in the instance with the recalculated statistical values.</span></span>

## <a name="mof-file"></a><span data-ttu-id="8af3f-116">File MOF</span><span class="sxs-lookup"><span data-stu-id="8af3f-116">MOF File</span></span>

<span data-ttu-id="8af3f-117">Nell'esempio di codice MOF seguente viene creata una nuova classe di dati calcolata denominata **Win32 \_ PerfFormattedData \_ AvailableMBytes**.</span><span class="sxs-lookup"><span data-stu-id="8af3f-117">The following MOF code example creates a new calculated data class named **Win32\_PerfFormattedData\_AvailableMBytes**.</span></span> <span data-ttu-id="8af3f-118">Questa classe contiene i dati della proprietà **AvailableMBytes** della classe RAW [**Win32 \_ PerfRawData \_ PerfOS \_ Memory**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data).</span><span class="sxs-lookup"><span data-stu-id="8af3f-118">This class contains data from the **AvailableMBytes** property of the raw class [**Win32\_PerfRawData\_PerfOS\_Memory**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data).</span></span> <span data-ttu-id="8af3f-119">La **classe Win32 \_ PerfFormattedData \_ AvailableBytes** definisce le proprietà **Average**, **min**, **Max**, **Range** e **Variance**.</span><span class="sxs-lookup"><span data-stu-id="8af3f-119">The **Win32\_PerfFormattedData\_AvailableBytes** class defines the properties **Average**, **Min**, **Max**, **Range**, and **Variance**.</span></span>

<span data-ttu-id="8af3f-120">Il file MOF utilizza i [**qualificatori di proprietà per le classi del contatore delle prestazioni formattate**](property-qualifiers-for-performance-counter-classes.md) per definire l'origine dati della proprietà e la formula di calcolo.</span><span class="sxs-lookup"><span data-stu-id="8af3f-120">The MOF file uses the [**Property Qualifiers for Formatted Performance Counter Classes**](property-qualifiers-for-performance-counter-classes.md) to define the property data source and the calculation formula.</span></span>

-   <span data-ttu-id="8af3f-121">La proprietà **Average** ottiene dati non elaborati dalla [**\_ \_ \_ memoria delle prestazioni PerfRawData Win32**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data).**Proprietà AvailableMBytes** .</span><span class="sxs-lookup"><span data-stu-id="8af3f-121">The **Average** property obtains raw data from the [**Win32\_PerfRawData\_PerfOS\_Memory**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data).**AvailableMBytes** property.</span></span>
-   <span data-ttu-id="8af3f-122">Il **qualificatore** del contatore per la proprietà **Average** specifica l'origine dati non elaborata.</span><span class="sxs-lookup"><span data-stu-id="8af3f-122">The Counter **qualifier** for the **Average** property specifies the raw data source.</span></span>
-   <span data-ttu-id="8af3f-123">Il qualificatore **CookingType** specifica il valore [ \_ minimo della formula Cooker](cooker-min.md) per il calcolo dei dati.</span><span class="sxs-lookup"><span data-stu-id="8af3f-123">The **CookingType** qualifier specifies the formula [COOKER\_MIN](cooker-min.md) for calculating the data.</span></span>
-   <span data-ttu-id="8af3f-124">Il qualificatore **SampleWindow** specifica il numero di campioni da eseguire prima di eseguire il calcolo.</span><span class="sxs-lookup"><span data-stu-id="8af3f-124">The **SampleWindow** qualifier specifies how many samples to take before performing the calculation.</span></span>


```mof
// Store the new Win32_PerfFormattedData_MemoryStatistics
//     class in the Root\Cimv2 namespace
#pragma autorecover
#pragma namespace("\\\\.\\Root\\CimV2")

qualifier vendor:ToInstance;
qualifier guid:ToInstance;
qualifier displayname:ToInstance;
qualifier perfindex:ToInstance;
qualifier helpindex:ToInstance;
qualifier perfdetail:ToInstance;
qualifier countertype:ToInstance;
qualifier perfdefault:ToInstance;
qualifier defaultscale:ToInstance;

qualifier dynamic:ToInstance;
qualifier hiperf:ToInstance;
qualifier AutoCook:ToInstance;
qualifier AutoCook_RawClass:ToInstance;
qualifier CookingType:ToInstance;
qualifier Counter:ToInstance;


// Define the Win32_PerFormattedData_MemoryStatistics
//     class, derived from Win32_PerfFormattedData
[
  dynamic,
  // Name of formatted data provider: "WMIPerfInst" for Vista 
  //   and later
  provider("HiPerfCooker_v1"), 
  // Text that will identify new counter in Perfmon
  displayname("My Calculated Counter"),                            
  // A high performance class     
  Hiperf,
  // Contains calculated data 
  Cooked, 
  // Value must be 1 
  AutoCook(1), 
  // Raw performance class to get data for calculations
  AutoCook_RawClass("Win32_PerfRawData_PerfOS_Memory"),
  // Value must be 1        
  AutoCook_RawDefault(1),
  // Name of raw class property to use for timestamp in formulas 
  PerfSysTimeStamp("Timestamp_PerfTime"), 
  // Name of raw class property to use for frequency in formulas
  PerfSysTimeFreq("Frequency_PerfTime"), 
  // Name of raw class property to use for timestamp in formulas
  Perf100NSTimeStamp("Timestamp_Sys100NS"),
  // Name of raw class property to use for frequency in formulas
  Perf100NSTimeFreq("Frequency_Sys100NS"),
  // Name of raw class property to use for timestamp in formulas
  PerfObjTimeStamp("Timestamp_Object"),
  // Name of raw class property to use for frequency in formulas 
  PerfObjTimeFreq("Frequency_Object"),
  // Only one instance of class allowed in namespace
  singleton                                                   
]

class Win32_PerfFormattedData_MemoryStatistics
          : Win32_PerfFormattedData
{

// Define the properties for the class. 
// All the properties perform different
//     statistical operations on the same
//     property, AvailableMBytes, in the raw class

// Define the Average property,
//     which uses the "COOKER_AVERAGE" counter type and 
//     gets its data from the AvailableMBytes 
//     property in the raw class

    [
     CookingType("COOKER_AVERAGE"),
     Counter("AvailableMBytes"),
     SampleWindow(10)
    ]
    uint64 Average = 0;

// Define the Min property, which uses
//     the "COOKER_MIN" counter type and 
//     gets its data from the AvailableMBytes
//     property in the raw class

    [
     CookingType("COOKER_MIN"),
     Counter("AvailableMBytes"),
     SampleWindow(10)
    ]
    uint64 Min = 0;

// Define the Max property, which uses
//     the "COOKER_MAX" counter type and 
//     gets its data from the
//     AvailableMBytes property in the raw class

    [
     CookingType("COOKER_MAX"),
     Counter("AvailableMBytes"),
     SampleWindow(10)
    ]
    uint64 Max = 0;

// Define the Range property, which uses
//     the "COOKER_RANGE" counter type and 
//     gets its data from the AvailableMBytes
//     property in the raw class

    [
     CookingType("COOKER_RANGE"),
     Counter("AvailableMBytes"),
     SampleWindow(10)
    ]
    uint64 Range = 0;

// Define the Variance property, which uses
//     the "COOKER_VARIANCE" counter type and 
//     gets its data from the AvailableMBytes
//     property in the raw class

    [
     CookingType("COOKER_VARIANCE"),
     Counter("AvailableMBytes"),
     SampleWindow(10)
    ]
    uint64 Variance = 0;
};
```



## <a name="script"></a><span data-ttu-id="8af3f-125">Script</span><span class="sxs-lookup"><span data-stu-id="8af3f-125">Script</span></span>

<span data-ttu-id="8af3f-126">Il seguente esempio di codice di script ottiene le statistiche sulla memoria disponibile, in megabyte, usando il file MOF creato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="8af3f-126">The following script code example obtains statistics about available memory, in megabytes, using the MOF created previously.</span></span> <span data-ttu-id="8af3f-127">Lo script utilizza l'oggetto di scripting [**SWbemRefresher**](swbemrefresher.md) per creare un aggiornamento che contiene un'istanza della classe Statistics creata dal file MOF, che è **Win32 \_ PerfFormattedData \_ MemoryStatistics**.</span><span class="sxs-lookup"><span data-stu-id="8af3f-127">The script uses the [**SWbemRefresher**](swbemrefresher.md) scripting object to create a refresher that contains one instance of the statistics class that the MOF file creates, which is **Win32\_PerfFormattedData\_MemoryStatistics**.</span></span> <span data-ttu-id="8af3f-128">Per ulteriori informazioni sull'utilizzo degli script, vedere [aggiornamento dei dati WMI negli script](refreshing-wmi-data-in-scripts.md).</span><span class="sxs-lookup"><span data-stu-id="8af3f-128">For more information about using scripts, see [Refreshing WMI Data in Scripts](refreshing-wmi-data-in-scripts.md).</span></span> <span data-ttu-id="8af3f-129">Se si utilizza C++, vedere [accesso ai dati sulle prestazioni in c++](accessing-performance-data-in-c--.md).</span><span class="sxs-lookup"><span data-stu-id="8af3f-129">If working in C++, see [Accessing Performance Data in C++](accessing-performance-data-in-c--.md).</span></span>

> [!Note]  
> <span data-ttu-id="8af3f-130">È necessario chiamare [**SWbemRefreshableItem. Object**](swbemrefreshableitem-object.md) dopo avere ottenuto l'elemento dalla chiamata a [**SWbemRefresher. Add**](swbemrefresher-add.md) oppure lo script avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="8af3f-130">[**SWbemRefreshableItem.Object**](swbemrefreshableitem-object.md) must be called after obtaining the item from the call to [**SWbemRefresher.Add**](swbemrefresher-add.md) or the script will fail.</span></span> <span data-ttu-id="8af3f-131">È necessario chiamare [**SWbemRefresher. Refresh**](swbemrefresher-refresh.md) prima di immettere il ciclo per ottenere i valori di base oppure le proprietà statistiche sono pari a zero (0) al primo passaggio.</span><span class="sxs-lookup"><span data-stu-id="8af3f-131">[**SWbemRefresher.Refresh**](swbemrefresher-refresh.md) must be called before entering the loop to obtain baseline values, or the statistical properties is zero (0) on the first pass.</span></span>

 


```VB
' Connect to the Root\Cimv2 namespace
strComputer = "."
Set objService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" _
    & strComputer & "\root\cimv2")

' Create a refresher
Set Refresher = CreateObject("WbemScripting.SWbemRefresher")
If Err <> 0 Then
WScript.Echo Err
WScript.Quit
End If

' Add the single instance of the statistics
'    class to the refresher
Set obMemoryStatistics = Refresher.Add(objService, _
    "Win32_PerfFormattedData_MemoryStatistics=@").Object

' Refresh once to obtain base values for cooking calculations
Refresher.Refresh

Const REFRESH_INTERVAL = 10

' Refresh every REFRESH_INTERVAL seconds 
For I=1 to 3
  WScript.Sleep REFRESH_INTERVAL * 1000
  Refresher.Refresh

  WScript.Echo "System memory statistics" _
      & "(Available Megabytes) " _
      & "for the past 100 seconds - pass " & i 
  WScript.Echo "Average = " _
     & obMemoryStatistics.Average & VBNewLine & "Max = " _
     & obMemoryStatistics.Max & VBNewLine & "Min = " _
     & obMemoryStatistics.Min & VBNewLine & "Range = " _ 
     & obMemoryStatistics.Range & VBNewLine & "Variance = " _
     & obMemoryStatistics.Variance 
Next
```



## <a name="running-the-script"></a><span data-ttu-id="8af3f-132">Esecuzione dello script</span><span class="sxs-lookup"><span data-stu-id="8af3f-132">Running the Script</span></span>

<span data-ttu-id="8af3f-133">Nella procedura seguente viene descritto come eseguire l'esempio.</span><span class="sxs-lookup"><span data-stu-id="8af3f-133">The following procedure describes how to run the example.</span></span>

<span data-ttu-id="8af3f-134">**Per eseguire lo script di esempio**</span><span class="sxs-lookup"><span data-stu-id="8af3f-134">**To run the example script**</span></span>

1.  <span data-ttu-id="8af3f-135">Copiare il codice MOF e lo script nei file del computer.</span><span class="sxs-lookup"><span data-stu-id="8af3f-135">Copy both the MOF code and script to files on your computer.</span></span>
2.  <span data-ttu-id="8af3f-136">Assegnare al file MOF un'estensione MOF e la descrizione del file di script a. vbs.</span><span class="sxs-lookup"><span data-stu-id="8af3f-136">Give the MOF file a .mof extension and the script file a .vbs description.</span></span>
3.  <span data-ttu-id="8af3f-137">Nella riga di comando passare alla directory in cui sono archiviati i file ed eseguire [**mofcomp**](mofcomp.md) sul file MOF.</span><span class="sxs-lookup"><span data-stu-id="8af3f-137">On the command line, change to the directory where the files are stored, and run [**Mofcomp**](mofcomp.md) on the MOF file.</span></span> <span data-ttu-id="8af3f-138">Se ad esempio si rinomina il file *CalculatedData. mof*, il comando sarà **mofcomp** *CalculatedData. mof*</span><span class="sxs-lookup"><span data-stu-id="8af3f-138">For example, if you name the file *CalculatedData.mof*, then the command is **Mofcomp** *CalculatedData.mof*</span></span>
4.  <span data-ttu-id="8af3f-139">Eseguire lo script.</span><span class="sxs-lookup"><span data-stu-id="8af3f-139">Run the script.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8af3f-140">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8af3f-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8af3f-141">Monitoraggio dei dati sulle prestazioni</span><span class="sxs-lookup"><span data-stu-id="8af3f-141">Monitoring Performance Data</span></span>](monitoring-performance-data.md)
</dt> <dt>

[<span data-ttu-id="8af3f-142">Accesso alle classi di prestazioni preinstallate WMI</span><span class="sxs-lookup"><span data-stu-id="8af3f-142">Accessing WMI Preinstalled Performance Classes</span></span>](accessing-wmi-preinstalled-performance-classes.md)
</dt> <dt>

[<span data-ttu-id="8af3f-143">**Qualificatori di proprietà per le classi del contatore delle prestazioni formattate**</span><span class="sxs-lookup"><span data-stu-id="8af3f-143">**Property Qualifiers for Formatted Performance Counter Classes**</span></span>](property-qualifiers-for-performance-counter-classes.md)
</dt> <dt>

[<span data-ttu-id="8af3f-144">Tipi di contatori statistici</span><span class="sxs-lookup"><span data-stu-id="8af3f-144">Statistical Counter Types</span></span>](statistical-counter-types.md)
</dt> </dl>

 

 
