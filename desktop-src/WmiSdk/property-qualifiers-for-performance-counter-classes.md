---
description: I qualificatori di proprietà specificano informazioni sul contatore delle prestazioni a cui viene eseguito il mapping della proprietà.
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
ms.openlocfilehash: 105bd010704364dc3865b2e704b3daeaafdb29a772d4f3b3fe036b88da2d43cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996181"
---
# <a name="property-qualifiers-for-performance-counter-classes"></a>Qualificatori di proprietà per le classi dei contatori delle prestazioni

I qualificatori di proprietà specificano informazioni sul contatore delle prestazioni a cui viene eseguito il mapping della proprietà.

-   [Qualificatori di proprietà per classi di prestazioni non elaborate e formattate](#property-qualifiers-for-raw-and-formatted-performance-classes)
-   [Qualificatori di proprietà per classi di prestazioni non elaborati](#property-qualifiers-for-raw-and-formatted-performance-classes)
-   [Qualificatori di proprietà per classi di prestazioni formattate](#property-qualifiers-for-raw-and-formatted-performance-classes)
-   [Come interpretare i qualificatori di proprietà](#how-to-interpret-property-qualifiers)
-   [Argomenti correlati](#related-topics)

Il contatore delle prestazioni fa parte di un oggetto prestazioni rappresentato da una classe di contatori delle prestazioni [WMI](/windows/desktop/CIMWin32Prov/performance-counter-classes) I qualificatori specifici del contatore delle prestazioni vengono collegati automaticamente dal provider WbemPerfClass alle classi e alle proprietà [**\_ Win32 PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) in \\ CIMv2 radice.

Queste informazioni si applicano a tutte le istanze della classe di prestazioni. Alcuni qualificatori con **valori booleani** sempre false potrebbero non essere presenti in classi specifiche.

## <a name="property-qualifiers-for-raw-and-formatted-performance-classes"></a>Qualificatori di proprietà per classi di prestazioni non elaborate e formattate

Nell'elenco seguente sono elencati i qualificatori applicabili alle proprietà nelle classi derivate da [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) o [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).

<dl> <dt>

<span id="CounterType"></span><span id="countertype"></span><span id="COUNTERTYPE"></span>[**CounterType**](countertype-qualifier.md)
</dt> <dd>

**sint32**

Valore intero nell'enumerazione del tipo di contatore, come definito in Winperf.h o Perflib.h. Il [**qualificatore CounterType**](countertype-qualifier.md)indica la formula o l'algoritmo usato per calcolare il valore visualizzato in Monitoraggio di sistema per il contatore rappresentato dalla proprietà .

</dd> <dt>

<span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>**Displayname**
</dt> <dd>

**string**

Nome del contatore delle prestazioni, come specificato da PDH (Performance Data Helper).

</dd> <dt>

<span id="HelpIndex"></span><span id="helpindex"></span><span id="HELPINDEX"></span>**HelpIndex**
</dt> <dd>

**sint32**

Non usato. Contiene sempre 0.

</dd> <dt>

<span id="PerfIndex"></span><span id="perfindex"></span><span id="PERFINDEX"></span>**PerfIndex**
</dt> <dd>

**sint32**

Non usato. Contiene sempre 0.

</dd> </dl>

## <a name="property-qualifiers-for-raw-performance-classes"></a>Qualificatori di proprietà per classi di prestazioni non elaborati

Nell'elenco seguente sono elencati i qualificatori applicabili a tutte le proprietà delle classi derivate da [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata).

<dl> <dt>

<span id="PerfDefault"></span><span id="perfdefault"></span><span id="PERFDEFAULT"></span>**PerfDefault**
</dt> <dd>

**boolean**

Indica se questa proprietà è il contatore predefinito da utilizzare nelle caselle di riepilogo. Il valore predefinito di questo qualificatore **è False** per i contatori delle prestazioni versione 6.0 perché non forniscono dati. Per altre informazioni, vedere [i contatori delle prestazioni](/windows/desktop/PerfCtrs/performance-counters-portal).

</dd> <dt>

<span id="DefaultScale"></span><span id="defaultscale"></span><span id="DEFAULTSCALE"></span>**Scalabilità predefinita**
</dt> <dd>

**sint32**

Potenza di 10 da usare per la visualizzazione del contatore. Per zero, il valore massimo stimato è 10^0 o 1.

</dd> <dt>

<span id="PerfDetail"></span><span id="perfdetail"></span><span id="PERFDETAIL"></span>[**PerfDetail**](perfdetail-qualifier.md)
</dt> <dd>

**sint32**

Livello di conoscenza del pubblico. Non usato. Il valore è sempre 100.

</dd> </dl>

## <a name="property-qualifiers-for-formatted-performance-classes"></a>Qualificatori di proprietà per classi di prestazioni formattate

Nell'elenco seguente sono elencati i qualificatori applicabili a tutte le proprietà delle classi derivate da [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).

<dl> <dt>

<span id="CookingType"></span><span id="cookingtype"></span><span id="COOKINGTYPE"></span>**Tipo di cucina**
</dt> <dd>

**string**

Tipo di formula usato per produrre il risultato. Ogni tipo di contatore usa gli altri qualificatori di proprietà per calcolare il risultato visualizzato come valore della proprietà corrente. I **qualificatori Counter**, **PerfTimeStamp** e **PerfTimeFreq** vengono mappati alle proprietà in una classe non elaborata che forniscono i dati.

Per altre informazioni, vedere [Qualificatore CounterType](countertype-qualifier.md).

</dd> <dt>

<span id="Counter"></span><span id="counter"></span><span id="COUNTER"></span>**Contatore**
</dt> <dd>

**string**

Nome di una proprietà obbligatoria nella classe non elaborata corrispondente da utilizzare come valore del contatore nella formula di preparazione. Il valore deve essere il nome della proprietà dell'origine dati nella classe non elaborata corrispondente.

</dd> <dt>

<span id="PerfTimeStamp"></span><span id="perftimestamp"></span><span id="PERFTIMESTAMP"></span>**PerfTimeStamp**
</dt> <dd>

**string**

Nome di una proprietà in una classe non elaborata da utilizzare come frequenza nella formula di cucina. Se questo qualificatore non è presente per la proprietà, verrà usato il valore predefinito appropriato a livello di classe. La frequenza rappresenta i tick al secondo del timestamp.

</dd> <dt>

<span id="PerfTimeFreq"></span><span id="perftimefreq"></span><span id="PERFTIMEFREQ"></span>**PerfTimeFreq**
</dt> <dd>

**string**

Nome di una proprietà in una classe non elaborata da utilizzare come timestamp nella formula di preparazione. Il valore predefinito appropriato a livello di classe viene usato se questo qualificatore non è presente per la proprietà . Un timestamp generato automaticamente può introdurre un errore in un calcolo perché il timestamp è un'approssimazione e non rappresenta l'overhead dovuto al marshalling e alla raccolta effettiva dei dati.

</dd> </dl>

## <a name="how-to-interpret-property-qualifiers"></a>Come interpretare i qualificatori di proprietà

Le proprietà nelle [**classi Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) contengono i dati calcolati forniti dalla classe [Formatted Performance provider di dati](formatted-performance-data-provider.md). Il valore della proprietà è il risultato finale calcolato. I qualificatori forniscono una ricetta.

I **qualificatori Counter** e **Base** puntano alle origini dati e Il **tipo di** preparazione specifica la formula usata per produrre il risultato. Il timestamp e la frequenza di campionamento provengono anche dalla classe non elaborata corrispondente e sono denominati in **PerfTimeStamp** e **PerfTimeFreq**.

Ad esempio, una delle classi formattate fornite da WMI, [**Win32 \_ PerfFormattedData \_ PerfDisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md), contiene una proprietà denominata **AvgDiskBytesPerRead.** Il nome della proprietà nella classe formattata deve corrispondere a quello della proprietà nella classe non elaborata. La **proprietà AvgDiskBytesPerRead** include i qualificatori seguenti.

Nell'elenco seguente sono elencati i qualificatori di proprietà disponibili per le proprietà di tutte le classi derivate da [**Win32 \_ PerfFormattedData.**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata)



| Qualifier         | Valore                     |
|-------------------|---------------------------|
| **Tipo di cucina**   | PERF \_ AVERAGE \_ BULK       |
| **Contatore**       | AvgDiskBytesPerRead       |
| **PerfTimeStamp** | Timestamp \_ PerfTime       |
| **PerfTimeFreq**  | Frequenza \_ perfTime       |
| **PerfIndex**     | 408                       |
| **HelpIndex**     | 409                       |
| **Base**          | AvgDiskBytesPerRead \_ Base |



 

La **proprietà AvgDiskBytesPerRead** indica il numero medio di byte trasferiti dal disco durante le operazioni di lettura. La formula per PERF \_ AVERAGE \_ BULK è:

(Sample2 - Sample1) / (Esempio di base2 - Esempio di base1)

L'operazione di lettura viene campionata alla frequenza specificata da **PerfTimeFreq con** il **valore PerfTimeStamp** che indica l'esempio più recente. I dati del contatore non elaborati in byte vengono presi dalla **proprietà AvgDiskBytesPerRead** nella [**classe Win32 \_ PerfRawData \_ PerfDisk \_ LogicalDisk.**](./retrieving-raw-and-formatted-performance-data.md) Il numero di base di dati delle operazioni viene derivato dalla **proprietà AvgDiskBytesPerRead \_ Base** nella stessa classe.

Per altre informazioni, vedere [Recupero di dati statistici sulle prestazioni](obtaining-statistical-performance-data.md) e Monitoraggio dei dati sulle [prestazioni](monitoring-performance-data.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Monitoraggio dei dati sulle prestazioni](monitoring-performance-data.md)
</dt> <dt>

[Qualificatori specifici delle classi di prestazioni WMI](qualifiers-specific-to-wmi-performance-classes.md)
</dt> <dt>

[Classi di contatori delle prestazioni](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[Accesso alle classi di prestazioni preinstallate WMI](accessing-wmi-preinstalled-performance-classes.md)
</dt> <dt>

[Attività WMI: Monitoraggio delle prestazioni](wmi-tasks--performance-monitoring.md)
</dt> </dl>

 

 
