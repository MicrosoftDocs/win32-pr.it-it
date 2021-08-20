---
description: Specificare le informazioni sull'oggetto prestazioni a cui viene mappata la classe del contatore delle prestazioni WMI.
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
ms.openlocfilehash: 5b8168dcc0523c629202ac4d5c4a0ea51ecc8bd68d5ac4498fb38059b940fd83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118820097"
---
# <a name="class-qualifiers-for-performance-counter-classes"></a>Qualificatori di classe per le classi dei contatori delle prestazioni

I qualificatori di classe specificano informazioni sull'oggetto prestazioni a cui viene mappata la classe del [contatore delle](/windows/desktop/CIMWin32Prov/performance-counter-classes) prestazioni WMI. Per altre informazioni, vedere [Monitoraggio dei dati sulle prestazioni](monitoring-performance-data.md).

-   [Qualificatori per le prestazioni non elaborato e formattatoClassi](#qualifiers-for-raw-and-formatted-performanceclasses)
-   [Qualificatori per le classi di prestazioni non elaborati](#)
-   [Qualificatori per classi di prestazioni formattate](#)
-   [Argomenti correlati](#related-topics)


I qualificatori specifici del contatore delle prestazioni vengono collegati automaticamente dal provider "WbemPerfClass" alle classi e alle proprietà [**\_ Win32 PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) in \\ CIMv2 radice.

Queste informazioni si applicano a tutte le istanze della classe . Alcuni qualificatori con **valori booleani** che sono sempre **False** potrebbero non essere presenti in classi specifiche.

## <a name="qualifiers-for-raw-and-formatted-performanceclasses"></a>Qualificatori per le prestazioni non elaborato e formattatoClassi

I qualificatori seguenti si applicano a tutte le classi derivate da [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) e [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).

<dl> <dt>

<span id="Cooked"></span><span id="cooked"></span><span id="COOKED"></span>**Cucinato**
</dt> <dd>

**boolean**

Indica se la classe contiene dati cotti.

</dd> <dt>

<span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>**Displayname**
</dt> <dd>

**string**

Nome dell'oggetto prestazioni. Per altre informazioni, vedere [i contatori delle prestazioni](/windows/desktop/PerfCtrs/performance-counters-portal).

</dd> <dt>

<span id="DetailLevel"></span><span id="detaillevel"></span><span id="DETAILLEVEL"></span>**DetailLevel**
</dt> <dd>

**sint32**

Non fornisce dati di dettaglio. Contiene sempre il valore 100.

</dd> <dt>

<span id="Dynamic"></span><span id="dynamic"></span><span id="DYNAMIC"></span>**Dinamico**
</dt> <dd>

**boolean**

Impostare sempre su **True perché** le istanze sono sempre dinamiche.

</dd> <dt>

<span id="GenericPerfCtr"></span><span id="genericperfctr"></span><span id="GENERICPERFCTR"></span>**GenericPerfCtr**
</dt> <dd>

**boolean**

Indica se la classe proviene da una libreria di prestazioni legacy. Impostare sempre su **True.**

</dd> <dt>

<span id="HelpIndex"></span><span id="helpindex"></span><span id="HELPINDEX"></span>**HelpIndex**
</dt> <dd>

**sint32**

Gli indici non sono più validi. Questo qualificatore è sempre zero.

</dd> <dt>

<span id="HiPerf_"></span><span id="hiperf_"></span><span id="HIPERF_"></span>**HiPerf** 
</dt> <dd>

**boolean**

Indica che la classe è una classe ad alte prestazioni. Impostare sempre su **True.**

</dd> <dt>

<span id="Locale"></span><span id="locale"></span><span id="LOCALE"></span>**Impostazioni internazionali**
</dt> <dd>

**sint32**

Identificatore delle impostazioni locali. Il valore è sempre 1033 (inglese Stati Uniti).

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

<span id="RegistryKey"></span><span id="registrykey"></span><span id="REGISTRYKEY"></span>**Registrykey**
</dt> <dd>

**string**

Nome del driver nella **chiave HKEY \_ LOCAL MACHINE \_ \\ CurrentControlSet \\ Services,** in cui è possibile trovare la chiave delle prestazioni. Questo nome è anche il nome del servizio che fornisce il contatore delle prestazioni.

</dd> <dt>

<span id="Singleton"></span><span id="singleton"></span><span id="SINGLETON"></span>**Singleton**
</dt> <dd>

**boolean**

Se **True**, indica che esiste una sola istanza della classe .

</dd> </dl>

## <a name="qualifiers-for-raw-performance-classes"></a>Qualificatori per le classi di prestazioni non elaborati

I qualificatori seguenti si applicano a tutte le classi derivate da [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata).

<dl> <dt>

<span id="Costly"></span><span id="costly"></span><span id="COSTLY"></span>**Costoso**
</dt> <dd>

**boolean**

Indica se ottenere istanze di questa classe è un'operazione disasserta. Impostare sempre su **True per** le classi con \_ "Costly" aggiunto alla fine del nome della classe.

</dd> <dt>

<span id="DetailLevel"></span><span id="detaillevel"></span><span id="DETAILLEVEL"></span>**DetailLevel**
</dt> <dd>

**uint32**

Non fornisce dati di dettaglio. Contiene sempre il valore 100.

</dd> <dt>

<span id="PerfDefault"></span><span id="perfdefault"></span><span id="PERFDEFAULT"></span>**PerfDefault**
</dt> <dd>

**boolean**

Il valore è sempre **False.**

</dd> </dl>

## <a name="qualifiers-for-formatted-performance-classes"></a>Qualificatori per classi di prestazioni formattate

I qualificatori seguenti si applicano a tutte le classi derivate da [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).

<dl> <dt>

<span id="AutoCook"></span><span id="autocook"></span><span id="AUTOCOOK"></span>**AutoCook**
</dt> <dd>

**int32**

Indica che i valori nelle istanze della classe vengono calcolati automaticamente dalla classe di dati non elaborati corrispondente. Il valore è sempre 1.

</dd> <dt>

<span id="AutoCook_RawClass"></span><span id="autocook_rawclass"></span><span id="AUTOCOOK_RAWCLASS"></span>**RawClass di AutoCook \_**
</dt> <dd>

**string**

Nome della classe non elaborata da utilizzare per il calcolo per la classe formattata. Questo qualificatore è obbligatorio.

</dd> </dl>

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

 

 
