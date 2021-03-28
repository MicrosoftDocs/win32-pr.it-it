---
description: Classe del tipo di evento per l'evento di intestazione del file di log. Questa classe contiene informazioni sulla sessione di traccia eventi.
ms.assetid: 3d0c4044-da06-4850-95c4-99b4ea28fcd9
title: Classe EventTrace_Header
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EventTrace_Header
- EventTrace_Header.BufferSize
- EventTrace_Header.Version
- EventTrace_Header.ProviderVersion
- EventTrace_Header.NumberOfProcessors
- EventTrace_Header.EndTime
- EventTrace_Header.TimerResolution
- EventTrace_Header.MaxFileSize
- EventTrace_Header.LogFileMode
- EventTrace_Header.BuffersWritten
- EventTrace_Header.StartBuffers
- EventTrace_Header.PointerSize
- EventTrace_Header.EventsLost
- EventTrace_Header.CPUSpeed
- EventTrace_Header.LoggerName
- EventTrace_Header.LogFileName
- EventTrace_Header.TimeZoneInformation
- EventTrace_Header.BootTime
- EventTrace_Header.PerfFreq
- EventTrace_Header.StartTime
- EventTrace_Header.ReservedFlags
- EventTrace_Header.BuffersLost
api_type:
- NA
api_location: ''
ms.openlocfilehash: dea803849d6aa15c2a3a14deb850d85ade569116
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526863"
---
# <a name="eventtrace_header-class"></a>\_Classe di intestazione EventTrace

Classe del tipo di evento per l'evento di intestazione del file di log. Questa classe contiene informazioni sulla sessione di traccia eventi.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[EventType(0)]
class EventTrace_Header : EventTraceEvent
{
  uint32 BufferSize;
  uint32 Version;
  uint32 ProviderVersion;
  uint32 NumberOfProcessors;
  uint64 EndTime;
  uint32 TimerResolution;
  uint32 MaxFileSize;
  uint32 LogFileMode;
  uint32 BuffersWritten;
  uint32 StartBuffers;
  uint32 PointerSize;
  uint32 EventsLost;
  uint32 CPUSpeed;
  uint32 LoggerName;
  uint32 LogFileName;
  uint8  TimeZoneInformation[];
  uint64 BootTime;
  uint64 PerfFreq;
  uint64 StartTime;
  uint32 ReservedFlags;
  uint32 BuffersLost;
};
```

## <a name="members"></a>Members

La classe dell' **\_ intestazione EventTrace** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe dell' **\_ intestazione EventTrace** include queste proprietà.

<dl> <dt>

**BootTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (17)
</dt> </dl>

Ora in cui il sistema è stato avviato, in intervalli di 100 nanosecondi dalla mezzanotte del 1 ° gennaio 1601.

</dd> <dt>

**BufferSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (1)
</dt> </dl>

Dimensioni dei buffer della sessione di traccia eventi, in kilobyte.

</dd> <dt>

**BuffersLost**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (21)
</dt> </dl>

Numero totale di buffer persi.

</dd> <dt>

**BuffersWritten**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (9)
</dt> </dl>

Numero totale di buffer scritti dalla sessione di traccia eventi.

</dd> <dt>

**CPUSpeed**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (13)
</dt> </dl>

Velocità della CPU, in megahertz.

**Windows 2000:** Non supportato.

</dd> <dt>

**EndTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (5)
</dt> </dl>

Ora di arresto della sessione di traccia eventi, in intervalli di 100 nanosecondi dalla mezzanotte del 1 ° gennaio 1601. Questo valore può essere 0 se si utilizzano eventi in tempo reale o da un file di log in cui l'oggetto fornisce ancora la registrazione degli eventi.

</dd> <dt>

**EventsLost**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (12)
</dt> </dl>

Numero di eventi persi durante la sessione di traccia eventi.

</dd> <dt>

**LogFileMode**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (8), **Format ("x")**
</dt> </dl>

Modalità di registrazione corrente per la sessione di traccia eventi. Per un elenco di valori, vedere costanti della modalità di registrazione.

</dd> <dt>

**LogFileName**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (15), **puntatore**
</dt> </dl>

Nome del file di log di traccia eventi che contiene gli eventi.

</dd> <dt>

**Loggername**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (14), **puntatore**
</dt> </dl>

Nome della sessione di traccia eventi.

</dd> <dt>

**MaxFileSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (7)
</dt> </dl>

Dimensioni massime del file di log, in megabyte.

</dd> <dt>

**NumberOfProcessors**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (4)
</dt> </dl>

Numero di processori nel sistema.

</dd> <dt>

**PerfFreq**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (18)
</dt> </dl>

Frequenza del contatore delle prestazioni ad alta risoluzione, se disponibile.

</dd> <dt>

**PointerSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (11)
</dt> </dl>

Dimensioni in byte del tipo di dati di un puntatore.

</dd> <dt>

**ProviderVersion**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (3)
</dt> </dl>

Numero di build del sistema operativo.

</dd> <dt>

**ReservedFlags**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (20)
</dt> </dl>

Riservato.

</dd> <dt>

**StartBuffers**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (10)
</dt> </dl>

Riservato.

</dd> <dt>

**StartTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (19)
</dt> </dl>

Ora di inizio della sessione di traccia eventi, in intervalli di 100 nanosecondi dalla mezzanotte del 1 ° gennaio 1601.

</dd> <dt>

**TimerResolution**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (6)
</dt> </dl>

Risoluzione del timer hardware, in unità di 100 nanosecondi.

</dd> <dt>

**TimeZoneInformation**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **Uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (16), **estensione ("NoPrint")**, **Max** (176)
</dt> </dl>

Struttura [**di \_ \_ informazioni sul fuso orario**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) che contiene il fuso orario per i membri **BootTime**, **EndTime** e **StartTime** .

</dd> <dt>

**Versione**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (2)
</dt> </dl>

Numero di versione del sistema operativo. A partire dai byte di ordine inferiore, i primi due byte contengono la versione principale, i due byte successivi contengono la versione secondaria, i due byte successivi contengono Service Pack versione principale e gli ultimi due byte contengono Service Pack versione secondaria.

</dd> </dl>

## <a name="remarks"></a>Commenti

In genere, si desidera salvare i valori per le seguenti proprietà da utilizzare in un secondo momento durante l'elaborazione degli eventi dal file di log.

-   **TimerResolution**: utilizzare con i membri **KernelTime** e **UserTime** della struttura [**dell' \_ \_ intestazione della traccia eventi**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) per determinare il costo della CPU per un set di istruzioni. Per informazioni dettagliate, vedere la sezione Osservazioni [**dell' \_ \_ intestazione della traccia dell'evento**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header).
-   **POINTERSIZE**: per le proprietà che contengono il qualificatore del **puntatore** , usare questo valore per determinare la dimensione del puntatore. Si noti che questo valore potrebbe non essere accurato. Ad esempio, in un computer a 64 bit, un'applicazione a 32 bit registrerà puntatori a 4 byte. Tuttavia, la sessione imposterà **POINTERSIZE** su 8.
-   **LogFileMode**: consente di determinare se questa sessione è una sessione di logger privata. Sono disponibili alcune proprietà che non contengono dati per le sessioni di logger privati. Ad esempio, i membri **KernelTime** e **UserTime** della struttura [**dell' \_ \_ intestazione della traccia eventi**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/> |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**EventTraceEvent**](eventtraceevent.md)
</dt> <dt>

[**\_intestazione logfile \_ traccia**](/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header)
</dt> </dl>

 

 
