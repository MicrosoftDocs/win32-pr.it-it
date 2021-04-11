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
# <a name="obtaining-statistical-performance-data"></a>Recupero di dati statistici sulle prestazioni

In WMI è possibile definire dati statistici sulle prestazioni in base ai dati in classi di prestazioni formattate derivate da [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata). Le statistiche disponibili sono medio, minimo, massimo, intervallo e varianza, come definito nei [tipi di contatori statistici](statistical-counter-types.md).

Nell'elenco seguente sono inclusi i tipi di contatori statistici speciali:

-   [media COOKer \_](cooker-average.md)
-   [MIN COOKer \_](cooker-min.md)
-   [massimo COOKer \_](cooker-max.md)
-   [intervallo di cottura \_](cooker-range.md)
-   [varianza del COOKer \_](cooker-variance.md)

Gli esempi seguenti illustrano come:

-   Creare un file MOF che definisce una classe di dati calcolati.
-   Scrivere uno script che crea un'istanza della classe e aggiorna periodicamente i dati nell'istanza di con i valori statistici ricalcolati.

## <a name="mof-file"></a>File MOF

Nell'esempio di codice MOF seguente viene creata una nuova classe di dati calcolata denominata **Win32 \_ PerfFormattedData \_ AvailableMBytes**. Questa classe contiene i dati della proprietà **AvailableMBytes** della classe RAW [**Win32 \_ PerfRawData \_ PerfOS \_ Memory**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data). La **classe Win32 \_ PerfFormattedData \_ AvailableBytes** definisce le proprietà **Average**, **min**, **Max**, **Range** e **Variance**.

Il file MOF utilizza i [**qualificatori di proprietà per le classi del contatore delle prestazioni formattate**](property-qualifiers-for-performance-counter-classes.md) per definire l'origine dati della proprietà e la formula di calcolo.

-   La proprietà **Average** ottiene dati non elaborati dalla [**\_ \_ \_ memoria delle prestazioni PerfRawData Win32**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data).**Proprietà AvailableMBytes** .
-   Il **qualificatore** del contatore per la proprietà **Average** specifica l'origine dati non elaborata.
-   Il qualificatore **CookingType** specifica il valore [ \_ minimo della formula Cooker](cooker-min.md) per il calcolo dei dati.
-   Il qualificatore **SampleWindow** specifica il numero di campioni da eseguire prima di eseguire il calcolo.


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



## <a name="script"></a>Script

Il seguente esempio di codice di script ottiene le statistiche sulla memoria disponibile, in megabyte, usando il file MOF creato in precedenza. Lo script utilizza l'oggetto di scripting [**SWbemRefresher**](swbemrefresher.md) per creare un aggiornamento che contiene un'istanza della classe Statistics creata dal file MOF, che è **Win32 \_ PerfFormattedData \_ MemoryStatistics**. Per ulteriori informazioni sull'utilizzo degli script, vedere [aggiornamento dei dati WMI negli script](refreshing-wmi-data-in-scripts.md). Se si utilizza C++, vedere [accesso ai dati sulle prestazioni in c++](accessing-performance-data-in-c--.md).

> [!Note]  
> È necessario chiamare [**SWbemRefreshableItem. Object**](swbemrefreshableitem-object.md) dopo avere ottenuto l'elemento dalla chiamata a [**SWbemRefresher. Add**](swbemrefresher-add.md) oppure lo script avrà esito negativo. È necessario chiamare [**SWbemRefresher. Refresh**](swbemrefresher-refresh.md) prima di immettere il ciclo per ottenere i valori di base oppure le proprietà statistiche sono pari a zero (0) al primo passaggio.

 


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



## <a name="running-the-script"></a>Esecuzione dello script

Nella procedura seguente viene descritto come eseguire l'esempio.

**Per eseguire lo script di esempio**

1.  Copiare il codice MOF e lo script nei file del computer.
2.  Assegnare al file MOF un'estensione MOF e la descrizione del file di script a. vbs.
3.  Nella riga di comando passare alla directory in cui sono archiviati i file ed eseguire [**mofcomp**](mofcomp.md) sul file MOF. Se ad esempio si rinomina il file *CalculatedData. mof*, il comando sarà **mofcomp** *CalculatedData. mof*
4.  Eseguire lo script.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Monitoraggio dei dati sulle prestazioni](monitoring-performance-data.md)
</dt> <dt>

[Accesso alle classi di prestazioni preinstallate WMI](accessing-wmi-preinstalled-performance-classes.md)
</dt> <dt>

[**Qualificatori di proprietà per le classi del contatore delle prestazioni formattate**](property-qualifiers-for-performance-counter-classes.md)
</dt> <dt>

[Tipi di contatori statistici](statistical-counter-types.md)
</dt> </dl>

 

 
