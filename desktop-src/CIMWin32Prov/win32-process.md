---
Description: Il \_ processo Win32&\# 32; La classe WMI rappresenta un processo in un sistema operativo.
ms.assetid: 51206aca-4784-4d18-95ca-bc0a45691f78
ms.tgt_platform: multiple
title: Classe Win32_Process
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/23/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process
- Win32_Process.CreationClassName
- Win32_Process.Caption
- Win32_Process.CommandLine
- Win32_Process.CreationDate
- Win32_Process.CSCreationClassName
- Win32_Process.CSName
- Win32_Process.Description
- Win32_Process.ExecutablePath
- Win32_Process.ExecutionState
- Win32_Process.Handle
- Win32_Process.HandleCount
- Win32_Process.InstallDate
- Win32_Process.KernelModeTime
- Win32_Process.MaximumWorkingSetSize
- Win32_Process.MinimumWorkingSetSize
- Win32_Process.Name
- Win32_Process.OSCreationClassName
- Win32_Process.OSName
- Win32_Process.OtherOperationCount
- Win32_Process.OtherTransferCount
- Win32_Process.PageFaults
- Win32_Process.PageFileUsage
- Win32_Process.ParentProcessId
- Win32_Process.PeakPageFileUsage
- Win32_Process.PeakVirtualSize
- Win32_Process.PeakWorkingSetSize
- Win32_Process.Priority
- Win32_Process.PrivatePageCount
- Win32_Process.ProcessId
- Win32_Process.QuotaNonPagedPoolUsage
- Win32_Process.QuotaPagedPoolUsage
- Win32_Process.QuotaPeakNonPagedPoolUsage
- Win32_Process.QuotaPeakPagedPoolUsage
- Win32_Process.ReadOperationCount
- Win32_Process.ReadTransferCount
- Win32_Process.SessionId
- Win32_Process.Status
- Win32_Process.TerminationDate
- Win32_Process.ThreadCount
- Win32_Process.UserModeTime
- Win32_Process.VirtualSize
- Win32_Process.WindowsVersion
- Win32_Process.WorkingSetSize
- Win32_Process.WriteOperationCount
- Win32_Process.WriteTransferCount
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: bb8d1d37bd5d4db59942aaab7170119283c5cc7b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327251"
---
# <a name="win32_process-class"></a>\_Classe processo Win32

La [classe WMI](../wmisdk/retrieving-a-class.md) del **\_ processo Win32** rappresenta un processo in un sistema operativo.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

> [!NOTE]
> Per una discussione generale su processi e thread in Windows, vedere l'argomento [processi e thread](/ProcThread/processes-and-threads.md).

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsCreate, CreateBy("Create"), SupportsDelete, DeleteBy("DeleteInstance"), UUID("{8502C4DC-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("Processes"), AMENDMENT]
class Win32_Process : CIM_Process
{
  string   CreationClassName;
  string   Caption;
  string   CommandLine;
  datetime CreationDate;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
  string   ExecutablePath;
  uint16   ExecutionState;
  string   Handle;
  uint32   HandleCount;
  datetime InstallDate;
  uint64   KernelModeTime;
  uint32   MaximumWorkingSetSize;
  uint32   MinimumWorkingSetSize;
  string   Name;
  string   OSCreationClassName;
  string   OSName;
  uint64   OtherOperationCount;
  uint64   OtherTransferCount;
  uint32   PageFaults;
  uint32   PageFileUsage;
  uint32   ParentProcessId;
  uint32   PeakPageFileUsage;
  uint64   PeakVirtualSize;
  uint32   PeakWorkingSetSize;
  uint32   Priority = NULL;
  uint64   PrivatePageCount;
  uint32   ProcessId;
  uint32   QuotaNonPagedPoolUsage;
  uint32   QuotaPagedPoolUsage;
  uint32   QuotaPeakNonPagedPoolUsage;
  uint32   QuotaPeakPagedPoolUsage;
  uint64   ReadOperationCount;
  uint64   ReadTransferCount;
  uint32   SessionId;
  string   Status;
  datetime TerminationDate;
  uint32   ThreadCount;
  uint64   UserModeTime;
  uint64   VirtualSize;
  string   WindowsVersion;
  uint64   WorkingSetSize;
  uint64   WriteOperationCount;
  uint64   WriteTransferCount;
};
```

## <a name="members"></a>Members

La classe di **\_ processo Win32** presenta questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La classe di **\_ processo Win32** presenta questi metodi.



| Metodo                                                                   | Descrizione                                                                                                                                                                                                                                                                               |
|:-------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AttachDebugger**](attachdebugger-method-in-class-win32-process.md)   | Avvia il debugger attualmente registrato per un processo.<br/>                                                                                                                                                                                                                      |
| [**Creare**](create-method-in-class-win32-process.md)                   | Crea un nuovo processo.<br/>                                                                                                                                                                                                                                                         |
| [**GetAvailableVirtualSize**](getavailablevirtualsize-win32-process.md) | Recupera le dimensioni correnti, in byte, dello spazio degli indirizzi virtuali libero disponibile per il processo.<br/> **Windows server 2012, Windows 8, Windows 7, Windows server 2008 e Windows Vista:** Questo metodo non è supportato prima di Windows 8.1 e Windows Server 2012 R2.<br/> |
| [**GetOwner**](getowner-method-in-class-win32-process.md)               | Recupera il nome utente e il nome di dominio in cui è in esecuzione il processo.<br/>                                                                                                                                                                                                    |
| [**GetOwnerSid**](getownersid-method-in-class-win32-process.md)         | Recupera l'ID di sicurezza (SID) per il proprietario di un processo.<br/>                                                                                                                                                                                                            |
| [**SetPriority**](setpriority-method-in-class-win32-process.md)         | Modifica la priorità di esecuzione di un processo.<br/>                                                                                                                                                                                                                                   |
| [**Terminare**](terminate-method-in-class-win32-process.md)             | Termina un processo e tutti i relativi thread.<br/>                                                                                                                                                                                                                                   |



 

### <a name="properties"></a>Proprietà

La classe di **\_ processo Win32** dispone di queste proprietà.

<dl> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")
</dt> </dl>

Breve descrizione di un oggetto, ovvero una stringa a una riga.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**CommandLine**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("riga di comando per avviare il processo")
</dt> </dl>

Riga di comando usata per avviare un processo specifico, se applicabile.

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("nome classe")
</dt> </dl>

Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di. Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.

Questa proprietà viene ereditata [**dal \_ processo CIM**](cim-process.md).

</dd> <dt>

**CreationDate**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**fixed**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("CreationDate")
</dt> </dl>

Data di inizio dell'esecuzione del processo.

Questa proprietà viene ereditata [**dal \_ processo CIM**](cim-process.md).

</dd> <dt>

**CSCreationClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**propagati**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**CSCreationClassName**"), [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" nome classe di sistema computer ")
</dt> </dl>

Nome della classe di creazione del computer di ambito.

Questa proprietà viene ereditata [**dal \_ processo CIM**](cim-process.md).

</dd> <dt>

**CSName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**propagati**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**CSName**"), [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" nome sistema computer ")
</dt> </dl>

Nome del sistema di ambito del computer.

Questa proprietà viene ereditata [**dal \_ processo CIM**](cim-process.md).

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")
</dt> </dl>

Descrizione di un oggetto.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**ExecutablePath**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualifiers: [**Privileges**](../wmisdk/standard-wmi-qualifiers.md) ("SeDebugPrivilege"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Tool Help Structures \| [**MODULEENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-moduleentry32) \| szExePath"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("percorso eseguibile")
</dt> </dl>

Percorso del file eseguibile del processo.

Esempio: "C: \\ Windows \\ System \\Explorer.Exe"

</dd> <dt>

**ExecutionState**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("stato esecuzione")
</dt> </dl>

Condizione operativa corrente del processo.

Questa proprietà viene ereditata [**dal \_ processo CIM**](cim-process.md).

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)


</dt> <dd>

Sconosciuto

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)


</dt> <dd>

Altro

</dd> <dt>

<span id="Ready"></span><span id="ready"></span><span id="READY"></span>

<span id="Ready"></span><span id="ready"></span><span id="READY"></span>**Pronto** (2)


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**In esecuzione** (3)


</dt> <dd></dd> <dt>

<span id="Blocked"></span><span id="blocked"></span><span id="BLOCKED"></span>

<span id="Blocked"></span><span id="blocked"></span><span id="BLOCKED"></span>**Bloccato** (4)


</dt> <dd>

Bloccato

</dd> <dt>

<span id="Suspended_Blocked"></span><span id="suspended_blocked"></span><span id="SUSPENDED_BLOCKED"></span>

<span id="Suspended_Blocked"></span><span id="suspended_blocked"></span><span id="SUSPENDED_BLOCKED"></span>**Sospeso bloccato** (5)


</dt> <dd></dd> <dt>

<span id="Suspended_Ready"></span><span id="suspended_ready"></span><span id="SUSPENDED_READY"></span>

<span id="Suspended_Ready"></span><span id="suspended_ready"></span><span id="SUSPENDED_READY"></span>**Pronto per sospensione** (6)


</dt> <dd></dd> <dt>

<span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>

<span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>**Terminato** (7)


</dt> <dd></dd> <dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrestato** (8)


</dt> <dd></dd> <dt>

<span id="Growing"></span><span id="growing"></span><span id="GROWING"></span>

<span id="Growing"></span><span id="growing"></span><span id="GROWING"></span>In **crescita** (9)


</dt> <dd></dd> </dl>

</dd> <dt>

**Handle**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("handle")
</dt> </dl>

Identificatore del processo.

Questa proprietà viene ereditata [**dal \_ processo CIM**](cim-process.md).

</dd> <dt>

**HandleCount**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process Status \| System \_ Process \_ Information \| HandleCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("handle count")
</dt> </dl>

Numero totale di handle aperti di proprietà del processo. **HandleCount** è la somma degli handle attualmente aperti da ogni thread di questo processo. Viene utilizzato un handle per esaminare o modificare le risorse di sistema. Ogni handle include una voce in una tabella gestita internamente. Le voci contengono gli indirizzi delle risorse e dei dati per identificare il tipo di risorsa.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data di installazione ")
</dt> </dl>

Data di installazione di un oggetto. L'oggetto può essere installato senza che venga scritto un valore in questa proprietà.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**KernelModeTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](../wmisdk/standard-qualifiers.md) ("KernelModeTime"), [**unità**](../wmisdk/standard-qualifiers.md) ("100 nanosecondi")
</dt> </dl>

Tempo in modalità kernel, in millisecondi. Se queste informazioni non sono disponibili, usare un valore pari a 0 (zero).

Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**MaximumWorkingSetSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualifiers: [**Privileges**](../wmisdk/standard-wmi-qualifiers.md) ("SeDebugPrivilege"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32 \| Winnt. H \| \_ limiti \| di quota MaximumWorkingSetSize "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" dimensioni massime working set "), [**unità**](../wmisdk/standard-qualifiers.md) (" kilobyte ")
</dt> </dl>

Dimensioni massime working set del processo. Il working set di un processo è il set di pagine di memoria visibile al processo nella RAM fisica. Queste pagine sono residenti e disponibili per l'uso da un'applicazione senza attivare un errore di pagina.

Esempio: 1413120

</dd> <dt>

**MinimumWorkingSetSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualifiers: [**Privileges**](../wmisdk/standard-wmi-qualifiers.md) ("SeDebugPrivilege"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32 \| Winnt. H \| limiti di quota \_ \| MinimumWorkingSetSize "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" dimensioni minime working set "), [**unità**](../wmisdk/standard-qualifiers.md) (" kilobytes ")
</dt> </dl>

Dimensioni minime working set del processo. Il working set di un processo è il set di pagine di memoria visibile al processo nella RAM fisica. Queste pagine sono residenti e disponibili per l'uso da un'applicazione senza attivare un errore di pagina.

Esempio: 20480

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")
</dt> </dl>

Nome del file eseguibile responsabile del processo, equivalente alla proprietà nome immagine in Gestione attività.

Se ereditato da una sottoclasse, è possibile eseguire l'override della proprietà in modo che sia una proprietà chiave. Il nome è hardcoded nell'applicazione stessa e non è interessato dalla modifica del nome del file. Ad esempio, anche se si rinomina Calc.exe, il nome Calc.exe verrà comunque visualizzato in Gestione attività e in tutti gli script WMI che recuperano il nome del processo.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**OSCreationClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**propagati**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**CreationClassName**"), [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" nome classe sistema operativo ")
</dt> </dl>

Nome della classe di creazione del sistema operativo di ambito.

Questa proprietà viene ereditata [**dal \_ processo CIM**](cim-process.md).

</dd> <dt>

**OSName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**propagati**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**Nome**"), [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" nome sistema operativo ")
</dt> </dl>

Nome del sistema operativo di ambito.

Questa proprietà viene ereditata [**dal \_ processo CIM**](cim-process.md).

</dd> <dt>

**OtherOperationCount**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| processi e strutture thread \| System \_ \_ Information \| OtherOperationCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("altro conteggio operazioni")
</dt> </dl>

Numero di operazioni di I/O eseguite che non sono operazioni di lettura o scrittura.

Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**OtherTransferCount**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| processi e strutture thread \| System \_ \_ Information \| OtherTransferCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("other Transfer count"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")
</dt> </dl>

Quantità di dati trasferiti durante le operazioni che non sono operazioni di lettura o scrittura.

Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**PageFaults**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process Status \| System \_ Process \_ Information \| PageFaultCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("numero di errori di pagina")
</dt> </dl>

Numero di errori di pagina generati da un processo.

Esempio: 10

</dd> <dt>

**PageFileUsage**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process Status \| System \_ Process \_ Information \| PagefileUsage"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Page file Usage"), [**unità**](../wmisdk/standard-qualifiers.md) ("kilobytes")
</dt> </dl>

Quantità di spazio del file di paging attualmente utilizzata da un processo. Questo valore è coerente con il valore **vmsize** in TaskMgr.exe.

Esempio: 102435

</dd> <dt>

**ParentProcessId**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API process \| status \| System \_ Process \_ Information \| InheritedFromUniqueProcessId"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("ID processo padre")
</dt> </dl>

Identificatore univoco del processo di creazione di un processo. I numeri degli identificatori di processo vengono riutilizzati, in modo che identifichino solo un processo per la durata di tale processo. È possibile che il processo identificato da **ParentProcessId** venga terminato, quindi **ParentProcessId** potrebbe non fare riferimento a un processo in esecuzione. È anche possibile che **ParentProcessId** si riferisca erroneamente a un processo che riutilizza un identificatore di processo. È possibile utilizzare la proprietà **CreationDate** per determinare se l'elemento padre specificato è stato creato dopo che è stato creato il processo rappresentato da questa istanza del **\_ processo Win32** .

</dd> <dt>

**PeakPageFileUsage**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process Status \| System \_ Process \_ Information \| PeakPagefileUsage"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Peak page file Usage"), [**unità**](../wmisdk/standard-qualifiers.md) ("kilobytes")
</dt> </dl>

Quantità massima di spazio per i file di paging utilizzata durante il ciclo di vita di un processo.

Esempio: 102367

</dd> <dt>

**PeakVirtualSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process Status \| System \_ Process \_ Information \| PeakVirtualSize"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Peak virual Address Space Usage"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")
</dt> </dl>

Spazio degli indirizzi virtuali massimo usato da un processo in qualsiasi momento. L'utilizzo dello spazio degli indirizzi virtuali non implica necessariamente l'utilizzo corrispondente di pagine del disco o della memoria principale. Tuttavia, lo spazio virtuale è finito e l'uso di un numero eccessivo di processi potrebbe non essere in grado di caricare le librerie.

Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**PeakWorkingSetSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process Status \| System \_ Process \_ Information \| PeakWorkingSetSize"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("picco working set size"), [**unità**](../wmisdk/standard-qualifiers.md) ("kilobytes")
</dt> </dl>

Picco working set dimensioni di un processo.

Esempio: 1413120

</dd> <dt>

**Priorità**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](../wmisdk/standard-qualifiers.md) ("Priority"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process Status \| System \_ Process \_ Information \| relativa BasePriority"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Priority")
</dt> </dl>

Priorità di pianificazione di un processo all'interno di un sistema operativo. Maggiore è il valore, maggiore è la priorità che un processo riceve. I valori di priorità possono variare da 0 (zero), ovvero la priorità più bassa a 31, che corrisponde alla priorità più alta.

Esempio: 7

</dd> <dt>

**PrivatePageCount**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process Status \| System \_ Process \_ Information \| PrivatePageCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("conteggio pagine private")
</dt> </dl>

Numero corrente di pagine allocate accessibili solo al processo rappresentato da questa istanza del **\_ processo Win32** .

Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**ProcessId**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API processi \| e strutture thread \| [**Process \_ Information**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_information) \| DwProcessId"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("ID processo")
</dt> </dl>

Identificatore numerico usato per distinguere un processo da un altro. ProcessIDs sono validi dalla fase di creazione del processo per la terminazione del processo. Alla chiusura, lo stesso identificatore numerico può essere applicato a un nuovo processo.

Ciò significa che non è possibile utilizzare solo ProcessId per monitorare un processo specifico. Ad esempio, un'applicazione può avere un ProcessId pari a 7 e quindi avere esito negativo. Quando viene avviato un nuovo processo, il nuovo processo può essere assegnato come ProcessId 7. Uno script controllato solo per un determinato ProcessId potrebbe quindi essere "ingannato" nel pensare che l'applicazione originale era ancora in esecuzione.

</dd> <dt>

**QuotaNonPagedPoolUsage**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process Status \| System \_ Process \_ Information \| QuotaNonPagedPoolUsage"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("quota di utilizzo del pool non di paging")
</dt> </dl>

Importo della quota di utilizzo del pool non di paging per un processo.

Esempio: 15

</dd> <dt>

**QuotaPagedPoolUsage**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process Status \| System \_ Process \_ Information \| QuotaPagedPoolUsage"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("quota di utilizzo del pool di paging")
</dt> </dl>

Importo della quota di utilizzo del pool di paging per un processo.

Esempio: 22

</dd> <dt>

**QuotaPeakNonPagedPoolUsage**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process Status \| System \_ Process \_ Information \| QuotaPeakNonPagedPoolUsage"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Peak non-paging pool Usage quota")
</dt> </dl>

Importo massimo della quota di utilizzo del pool non di paging per un processo.

Esempio: 31

</dd> <dt>

**QuotaPeakPagedPoolUsage**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process Status \| System \_ Process \_ Information \| QuotaPeakPagedPoolUsage"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("picco di utilizzo pool di paging")
</dt> </dl>

Importo massimo della quota di utilizzo del pool di paging per un processo.

Esempio: 31

</dd> <dt>

**ReadOperationCount**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| processi e strutture thread \| System \_ \_ Information \| ReadOperationCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Read operation count")
</dt> </dl>

Numero di operazioni di lettura eseguite.

Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**ReadTransferCount**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| processi e strutture thread \| System \_ \_ Information \| ReadTransferCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Read Transfer count"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")
</dt> </dl>

Quantità di dati letti.

Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**SessionId**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process Status \| System \_ Process \_ Information \| SessionID"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("ID sessione")
</dt> </dl>

Identificatore univoco generato da un sistema operativo al momento della creazione di una sessione. Una sessione si estende a un periodo di tempo dall'accesso fino alla disconnessione da un sistema specifico.

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")
</dt> </dl>

Questa proprietà non viene implementata e non viene popolata per nessuna istanza di questa classe. È sempre **null**.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

Sono inclusi i valori seguenti:

<dt>

<span id="OK"></span><span id="ok"></span>

**OK** ("OK")


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Errore** ("errore")


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

Ridotto **("danneggiato"** )


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** ("sconosciuto")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Errore di predazione** ("Predator fail")


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**Avvio** di ("avvio")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Arresto** in corso ("arresto")


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Servizio** ("servizio")


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Sottolineato** (sottolineato)


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

**Noncover** ("noncover")


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Nessun contatto** ("nessun contatto")


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Comunicazione persa** ("comunicazione persa")


</dt> <dd></dd> </dl>

</dd> <dt>

**TerminationDate**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("data di terminazione")
</dt> </dl>

Il processo è stato interrotto o terminato. Per ottenere il tempo di chiusura, è necessario che venga mantenuto aperto un handle per il processo. In caso contrario, la proprietà restituirà **null**.

Questa proprietà viene ereditata [**dal \_ processo CIM**](cim-process.md).

</dd> <dt>

**ThreadCount**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process Status \| System \_ Process \_ Information \| NumberOfThreads"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("conteggio thread")
</dt> </dl>

Numero di thread attivi in un processo. Un'istruzione è l'unità di base di esecuzione in un processore e un thread è l'oggetto che esegue un'istruzione. Ogni processo in esecuzione ha almeno un thread.

</dd> <dt>

**UserModeTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](../wmisdk/standard-qualifiers.md) ("UserModeTime"), [**unità**](../wmisdk/standard-qualifiers.md) ("100 nanosecondi")
</dt> </dl>

Tempo in modalità utente, in unità di 100 nanosecondi. Se queste informazioni non sono disponibili, usare un valore pari a 0 (zero).

Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**VirtualSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process Status \| System \_ Process \_ Information \| VirtualSize"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("utilizzo spazio indirizzi virtuali"), [**unità**](../wmisdk/standard-qualifiers.md) ("byte")
</dt> </dl>

Dimensioni correnti dello spazio degli indirizzi virtuali usato da un processo, non della memoria fisica o virtuale effettivamente utilizzata dal processo. L'utilizzo dello spazio degli indirizzi virtuali non implica necessariamente l'utilizzo corrispondente di pagine del disco o della memoria principale. Lo spazio virtuale è finito e, usando un numero eccessivo di operazioni, il processo potrebbe non essere in grado di caricare le librerie. Questo valore è coerente con quello visualizzato in Perfmon.exe.

Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**WindowsVersion**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process and thread Functions \| GetProcessVersion"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("versione di Windows")
</dt> </dl>

Versione di Windows in cui è in esecuzione il processo.

Esempio: 4,0

</dd> <dt>

**WorkingSetSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("working set size"), [**unità**](../wmisdk/standard-qualifiers.md) ("bytes")
</dt> </dl>

Quantità di memoria in byte che un processo deve eseguire in modo efficiente, per un sistema operativo che utilizza la gestione della memoria basata su pagine. Se il sistema non dispone di memoria sufficiente (inferiore alla dimensione working set), si verifica il thrashing. Se la dimensione dell'working set non è nota, utilizzare **null** o 0 (zero). Se vengono forniti working set dati, è possibile monitorare le informazioni per comprendere i requisiti di memoria modificabili di un processo.

Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](../wmisdk/creating-a-wmi-script.md).

Questa proprietà viene ereditata [**dal \_ processo CIM**](cim-process.md).

</dd> <dt>

**WriteOperationCount**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| processi e strutture thread \| System \_ \_ Information \| WriteOperationCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("write operation count")
</dt> </dl>

Numero di operazioni di scrittura eseguite.

Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**WriteTransferCount**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| processi e strutture thread \| System \_ \_ Information \| WriteTransferCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Write Transfer count"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")
</dt> </dl>

Quantità di dati scritti.

Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](../wmisdk/creating-a-wmi-script.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe di **\_ processo Win32** è derivata [**dal \_ processo CIM**](cim-process.md). Il processo chiamante che usa questa classe deve avere il privilegio **se \_ Restore \_ Name** nel computer in cui risiede il registro di sistema. Per altre informazioni, vedere [esecuzione di operazioni con privilegi](../wmisdk/executing-privileged-operations.md).

### <a name="overview"></a>Panoramica

I processi sono sottostanti quasi tutto ciò che accade in un computer. Infatti, la causa principale della maggior parte dei problemi del computer può essere tracciata ai processi; è possibile, ad esempio, che un numero eccessivo di processi sia in esecuzione in un computer (e che contenda un set limitato di risorse) oppure che un singolo processo stia usando più della relativa condivisione di risorse. Questi fattori rendono importante tenere sotto controllo i processi in esecuzione in un computer. Il monitoraggio dei processi, l'attività principale nella gestione dei processi, consente di determinare le operazioni effettivamente eseguite da un computer, le applicazioni eseguite dal computer e il modo in cui tali applicazioni sono interessate dalle modifiche apportate all'ambiente informatico.

### <a name="monitoring-a-process"></a>Monitoraggio di un processo

Il monitoraggio dei processi a intervalli regolari consente di garantire che un computer venga eseguito a picco di efficienza e che esegua le attività designate come previsto. Tramite il monitoraggio dei processi, ad esempio, è possibile ricevere notifiche immediate di qualsiasi applicazione che ha smesso di rispondere e quindi eseguire le operazioni necessarie per terminare il processo. Inoltre, il monitoraggio dei processi consente di identificare i problemi prima che si verifichino. Ad esempio, controllando ripetutamente la quantità di memoria usata da un processo, è possibile identificare una perdita di memoria. È quindi possibile arrestare il processo prima che l'applicazione errata utilizzi tutta la memoria disponibile e riporti un arresto del computer.

Il monitoraggio dei processi consente inoltre di ridurre al minimo le interruzioni dovute a interruzioni pianificate per aggiornamenti e manutenzione. Se ad esempio si controlla lo stato di un'applicazione di database in esecuzione nei computer client, è possibile determinare l'effetto della disconnessione del database per l'aggiornamento del software.

Monitoraggio della disponibilità del processo. Misura la percentuale di tempo disponibile per un processo. La disponibilità viene in genere monitorata usando un probe semplice, che indica se il processo è ancora in esecuzione. Tenendo traccia dei risultati di ogni Probe, è possibile calcolare la disponibilità del processo. Ad esempio, un processo con Probe 100 volte e risponde in 95 di tali occasioni ha una disponibilità pari al 95%. Questo tipo di monitoraggio è in genere riservato per database, programmi di posta elettronica e altre applicazioni che dovrebbero essere eseguite in qualsiasi momento. Non è appropriato per i programmi di elaborazione testi, i fogli di calcolo o altre applicazioni che vengono regolarmente avviate e arrestate più volte al giorno.

Per configurare il processo, è possibile creare un'istanza della classe [**Win32 \_ ProcessStartup**](win32-processstartup.md) .

È possibile monitorare le prestazioni del processo con la classe di [**\_ \_ \_ processo Win32 PerfFormattedData PerfProc**](../wmisdk/retrieving-raw-and-formatted-performance-data.md) e un oggetto di aggiornamento WMI, ad esempio [**SWbemRefresher**](../wmisdk/swbemrefresher.md). Per ulteriori informazioni, vedere [monitoraggio dei dati sulle prestazioni](../wmisdk/monitoring-performance-data.md).

## <a name="examples"></a>Esempio

L' [elenco delle proprietà delle classi WMI esempio di](https://Gallery.TechNet.Microsoft.Com/a7918bf3-bc03-4553-990f-aba13cf196b7) codice PowerShell nella raccolta TechNet descrive la classe di **\_ processo Win32** e restituisce i risultati in formato Excel.

Il [processo termina in esecuzione su più server](https://Gallery.TechNet.Microsoft.Com/698c2512-2bbd-40ee-b3bf-a9cebdad2faf) termina un processo in esecuzione in uno o più computer.

Nell'argomento [esempio: chiamata a un metodo del provider](../wmisdk/example--calling-a-provider-method.md) , il codice USA C++ per chiamare il **\_ processo Win32** per creare un processo.

La disponibilità è la forma più semplice di monitoraggio dei processi: con questo approccio è sufficiente assicurarsi che il processo sia in esecuzione. Quando si monitora la disponibilità dei processi, in genere si recupera un elenco di processi in esecuzione in un computer e quindi si verifica che un determinato processo sia ancora attivo. Se il processo è attivo, viene considerato disponibile. Se il processo non è attivo, non è disponibile. Nell'esempio VBScript seguente viene monitorata la disponibilità del processo controllando l'elenco dei processi in esecuzione in un computer e inviando una notifica se il processo di Database.exe non viene trovato.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colProcesses = objWMIService.ExecQuery("SELECT * FROM Win32_Process WHERE Name = 'Database.exe'")
If colProcesses.Count = 0 Then
 Wscript.Echo "Database.exe is not running."
Else
 Wscript.Echo "Database.exe is running."
End If
```



Nell'esempio VBScript seguente viene monitorata la creazione di processi utilizzando un consumer di eventi temporaneo.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colMonitoredProcesses = objWMIService.ExecNotificationQuery("SELECT * FROM __InstanceCreationEvent " _
                                                     & "WITHIN 10 WHERE TargetInstance ISA 'Win32_Process'")
i = 0
Do While i = 0
 Set objLatestProcess = colMonitoredProcesses.NextEvent
 Wscript.Echo objLatestProcess.TargetInstance.Name, Now
Loop
```



Il codice VBScript seguente monitora le informazioni sulle prestazioni del processo.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colProcessList = objWMIService.ExecQuery("SELECT * FROM Win32_Process")
For Each objProcess in colProcessList
 Wscript.Echo "Process: " & objProcess.Name
 Wscript.Echo "Process ID: " & objProcess.ProcessID
 Wscript.Echo "Thread Count: " & objProcess.ThreadCount
 Wscript.Echo "Page File Size: " & objProcess.PageFileUsage
 Wscript.Echo "Page Faults: " & objProcess.PageFaults
 Wscript.Echo "Working Set Size: " & objProcess.WorkingSetSize
Next
```



Nell'esempio di codice VBScript riportato di seguito viene illustrato come ottenere il proprietario di ogni processo in un computer locale. È possibile utilizzare questo script per ottenere i dati da un computer remoto, ad esempio, per determinare quali utenti dispongono di processi che eseguono Terminal Server, sostituire il nome del computer remoto con "." nella prima riga. È anche necessario essere un amministratore nel computer remoto.


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

Set colProcesses = objWMIService.ExecQuery("select * from win32_process" )
For Each objProcess in colProcesses

  If objProcess.GetOwner ( User, Domain ) = 0 Then
    Wscript.Echo "Process " & objProcess.Caption & " belongs to " & Domain & "\" & User
  Else
    Wscript.Echo "Problem " & Rtn & " getting the owner for process " & objProcess.Caption
  End If
Next
```



Nell'esempio di codice VBScript riportato di seguito viene illustrato come ottenere la sessione di accesso associata a un processo in esecuzione. Un processo deve essere in esecuzione Notepad.exe prima dell'avvio dello script. Nell'esempio vengono individuate le istanze [**di \_ LogonSession Win32**](win32-logonsession.md) associate al **\_ processo Win32** che rappresenta Notepad.exe. [**Win32 \_ SessionProcess**](win32-sessionprocess.md) viene specificato come classe Association. Per ulteriori informazioni, vedere [ASSOCIATORS of Statement.](../wmisdk/associators-of-statement.md)


```VB
On error resume next
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\.\root\cimv2")
Set colProcesses = objWMIService.ExecQuery("Select * from Win32_Process Where Name = 'Notepad.exe'")
For Each objProcess in colProcesses
  ProcessId = objProcess.ProcessId
  Set colLogonSessions = objWMIService.ExecQuery("Associators of {Win32_Process='" & ProcessId & "'} " _
                                               & "Where Resultclass = Win32_LogonSession Assocclass = Win32_SessionProcess", "WQL", 48)
  If Err <> 0 Then
    WScript.Echo "Error on associators query= " & Err.number & " " & Err.Description
    WScript.Quit
  End If
  For Each LogonSession in colLogonSessions
    Wscript.Echo " Logon id is " & LogonSession.LogonId
  Next
Next
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Processo CIM**](cim-process.md)
</dt> <dt>

[Classi del sistema operativo](./operating-system-classes.md)
</dt> <dt>

[Attività WMI: processi](../wmisdk/wmi-tasks--processes.md)
</dt> </dl>

 

 
