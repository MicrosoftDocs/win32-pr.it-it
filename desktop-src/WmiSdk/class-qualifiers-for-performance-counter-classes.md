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
# <a name="class-qualifiers-for-performance-counter-classes"></a>Qualificatori di classe per le classi dei contatori delle prestazioni

I qualificatori di classe specificano le informazioni sull'oggetto prestazione a cui viene mappata la [classe del contatore delle prestazioni](/windows/desktop/CIMWin32Prov/performance-counter-classes) WMI. Per ulteriori informazioni, vedere [monitoraggio dei dati sulle prestazioni](monitoring-performance-data.md).

-   [Qualificatori per PerformanceClasses RAW e formattati](#qualifiers-for-raw-and-formatted-performanceclasses)
-   [Qualificatori per le classi di prestazioni non elaborate](#)
-   [Qualificatori per classi di prestazioni formattate](#)
-   [Argomenti correlati](#related-topics)


I qualificatori specifici del contatore delle prestazioni vengono automaticamente collegati dal provider "WbemPerfClass" alle classi e alle proprietà [**\_ PerfRawData Win32**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) in \\ CIMv2 radice.

Queste informazioni si applicano a tutte le istanze della classe. Alcuni qualificatori con valori **booleani** sempre **false** potrebbero non essere presenti in classi specifiche.

## <a name="qualifiers-for-raw-and-formatted-performanceclasses"></a>Qualificatori per PerformanceClasses RAW e formattati

I qualificatori seguenti si applicano a tutte le classi derivate da [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) e [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).

<dl> <dt>

<span id="Cooked"></span><span id="cooked"></span><span id="COOKED"></span>**Cotto**
</dt> <dd>

**boolean**

Indica se la classe contiene dati cotti.

</dd> <dt>

<span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>**DisplayName**
</dt> <dd>

**string**

Nome dell'oggetto prestazioni. Per altre informazioni, vedere [i contatori delle prestazioni](/windows/desktop/PerfCtrs/performance-counters-portal).

</dd> <dt>

<span id="DetailLevel"></span><span id="detaillevel"></span><span id="DETAILLEVEL"></span>**DetailLevel**
</dt> <dd>

**sint32**

Non fornisce dati dettaglio. Contiene sempre il valore 100.

</dd> <dt>

<span id="Dynamic"></span><span id="dynamic"></span><span id="DYNAMIC"></span>**Dinamico**
</dt> <dd>

**boolean**

Sempre impostato su **true** perché le istanze sono sempre dinamiche.

</dd> <dt>

<span id="GenericPerfCtr"></span><span id="genericperfctr"></span><span id="GENERICPERFCTR"></span>**GenericPerfCtr**
</dt> <dd>

**boolean**

Indica se la classe deriva da una libreria delle prestazioni legacy. Sempre impostato su **true**.

</dd> <dt>

<span id="HelpIndex"></span><span id="helpindex"></span><span id="HELPINDEX"></span>**HelpIndex**
</dt> <dd>

**sint32**

Gli indici non sono più validi. Questo qualificatore è sempre zero.

</dd> <dt>

<span id="HiPerf_"></span><span id="hiperf_"></span><span id="HIPERF_"></span>**HiPerf** 
</dt> <dd>

**boolean**

Indica che la classe è una classe a prestazioni elevate. Sempre impostato su **true**.

</dd> <dt>

<span id="Locale"></span><span id="locale"></span><span id="LOCALE"></span>**Locale**
</dt> <dd>

**sint32**

Identificatore delle impostazioni locali. Il valore è sempre 1033 (Inglese (Stati Uniti).

</dd> <dt>

<span id="PerfIndex"></span><span id="perfindex"></span><span id="PERFINDEX"></span>**PerfIndex**
</dt> <dd>

**int32**

Gli indici non sono più validi. Questo qualificatore è sempre zero.

</dd> <dt>

<span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>**Provider**
</dt> <dd>

**string**

Nome del provider di istanze. Il valore è "WbemPerfV2".

</dd> <dt>

<span id="RegistryKey"></span><span id="registrykey"></span><span id="REGISTRYKEY"></span>**RegistryKey**
</dt> <dd>

**string**

Nome del driver nella chiave dei **\_ \_ \\ \\ Servizi CurrentControlSet del computer locale HKEY** , in cui è possibile trovare la chiave delle prestazioni. Questo nome è anche il nome del servizio che fornisce il contatore delle prestazioni.

</dd> <dt>

<span id="Singleton"></span><span id="singleton"></span><span id="SINGLETON"></span>**Singleton**
</dt> <dd>

**boolean**

Se **true**, indica che esiste una sola istanza della classe.

</dd> </dl>

## <a name="qualifiers-for-raw-performance-classes"></a>Qualificatori per le classi di prestazioni non elaborate

I qualificatori seguenti si applicano a tutte le classi derivate da [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata).

<dl> <dt>

<span id="Costly"></span><span id="costly"></span><span id="COSTLY"></span>**Costose**
</dt> <dd>

**boolean**

Indica se il recupero di istanze di questa classe è un'operazione costosa. Sempre impostato su **true** per le classi con " \_ costose" accodato alla fine del nome della classe.

</dd> <dt>

<span id="DetailLevel"></span><span id="detaillevel"></span><span id="DETAILLEVEL"></span>**DetailLevel**
</dt> <dd>

**uint32**

Non fornisce dati dettaglio. Contiene sempre il valore 100.

</dd> <dt>

<span id="PerfDefault"></span><span id="perfdefault"></span><span id="PERFDEFAULT"></span>**PerfDefault**
</dt> <dd>

**boolean**

Il valore è sempre **false**.

</dd> </dl>

## <a name="qualifiers-for-formatted-performance-classes"></a>Qualificatori per classi di prestazioni formattate

I qualificatori seguenti si applicano a tutte le classi derivate da [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).

<dl> <dt>

<span id="AutoCook"></span><span id="autocook"></span><span id="AUTOCOOK"></span>**Autocook**
</dt> <dd>

**int32**

Indica che i valori nelle istanze della classe vengono calcolati automaticamente dalla classe di dati RAW corrispondente. Il valore è sempre 1.

</dd> <dt>

<span id="AutoCook_RawClass"></span><span id="autocook_rawclass"></span><span id="AUTOCOOK_RAWCLASS"></span>**RawClass autocook \_**
</dt> <dd>

**string**

Nome della classe non elaborata da utilizzare per il calcolo della classe formattata. Questo qualificatore è obbligatorio.

</dd> </dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Monitoraggio dei dati sulle prestazioni](monitoring-performance-data.md)
</dt> <dt>

[Qualificatori specifici delle classi di prestazioni WMI](qualifiers-specific-to-wmi-performance-classes.md)
</dt> <dt>

[Classi del contatore delle prestazioni](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[Accesso alle classi di prestazioni preinstallate WMI](accessing-wmi-preinstalled-performance-classes.md)
</dt> <dt>

[Attività WMI: monitoraggio delle prestazioni](wmi-tasks--performance-monitoring.md)
</dt> </dl>

 

 
