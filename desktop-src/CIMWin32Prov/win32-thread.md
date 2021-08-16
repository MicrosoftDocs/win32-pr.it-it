---
description: Thread Win32 \_&\# 8194; La classe WMI rappresenta un thread di esecuzione.
ms.assetid: a284616c-1977-441a-9173-dff4f56b2d39
ms.tgt_platform: multiple
title: Win32_Thread classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Thread
- Win32_Thread.Caption
- Win32_Thread.CreationClassName
- Win32_Thread.CSCreationClassName
- Win32_Thread.CSName
- Win32_Thread.Description
- Win32_Thread.ElapsedTime
- Win32_Thread.ExecutionState
- Win32_Thread.Handle
- Win32_Thread.InstallDate
- Win32_Thread.KernelModeTime
- Win32_Thread.Name
- Win32_Thread.OSCreationClassName
- Win32_Thread.OSName
- Win32_Thread.Priority
- Win32_Thread.PriorityBase
- Win32_Thread.ProcessCreationClassName
- Win32_Thread.ProcessHandle
- Win32_Thread.StartAddress
- Win32_Thread.Status
- Win32_Thread.ThreadState
- Win32_Thread.ThreadWaitReason
- Win32_Thread.UserModeTime
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f3add3a93cc974c2d6c5b20c360d099d46b688887f81cb646005568240a7cb52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118416717"
---
# <a name="win32_thread-class"></a>Classe Thread Win32 \_

La classe  [WMI](../wmisdk/retrieving-a-class.md) **\_ Thread Win32** rappresenta un thread di esecuzione. Mentre un processo deve avere un thread di esecuzione, il processo può creare altri thread per eseguire attività in parallelo. I thread condividono l'ambiente di processo, pertanto più thread nello stesso processo usano meno memoria rispetto allo stesso numero di processi.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà e i metodi sono in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4DD-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_Thread : CIM_Thread
{
  string   Caption;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
  uint64   ElapsedTime;
  uint16   ExecutionState;
  string   Handle;
  datetime InstallDate;
  uint64   KernelModeTime;
  string   Name;
  string   OSCreationClassName;
  string   OSName;
  uint32   Priority;
  uint32   PriorityBase;
  string   ProcessCreationClassName;
  string   ProcessHandle;
  uint32   StartAddress;
  string   Status;
  uint32   ThreadState;
  uint32   ThreadWaitReason;
  uint64   UserModeTime;
};
```

## <a name="members"></a>Members

La **classe \_ Thread Win32** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ Thread Win32** dispone di queste proprietà.

<dl> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")
</dt> </dl>

Breve descrizione dell'oggetto.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Cim \_ Key,**](../wmisdk/standard-wmi-qualifiers.md) [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Nome della prima classe concreta da visualizzare nella catena di ereditarietà utilizzata nella creazione di un'istanza. Se usata con le altre proprietà chiave della classe , questa proprietà consente l'identificazione univoca di tutte le istanze di questa classe e delle relative sottoclassi.

Questa proprietà viene ereditata dal [**\_ thread CIM.**](cim-thread.md)

</dd> <dt>

**CSCreationClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**propagati**](../wmisdk/standard-qualifiers.md) ("[**Processo CIM \_**](cim-process.md).**CSCreationClassName**"), [**Cim \_ Key,**](../wmisdk/standard-wmi-qualifiers.md) [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Nome della classe di creazione del sistema informatico di ambito.

Questa proprietà viene ereditata dal [**\_ thread CIM.**](cim-thread.md)

</dd> <dt>

**CSName**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**propagati**](../wmisdk/standard-qualifiers.md) ("[**Processo CIM \_**](cim-process.md).**CSName**"), [**Cim \_ Key,**](../wmisdk/standard-wmi-qualifiers.md) [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Nome del sistema informatico di ambito.

Questa proprietà viene ereditata dal [**\_ thread CIM.**](cim-thread.md)

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")
</dt> </dl>

Descrizione dell'oggetto.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**ElapsedTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Strutture dei dati delle prestazioni Win32API \| \| [**PERF \_ OBJECT \_ TYPE**](/windows/win32/api/winperf/ns-winperf-perf_object_type) \| PerfTime"), [**Unità**](../wmisdk/standard-qualifiers.md) ("millisecondi")
</dt> </dl>

Tempo di esecuzione totale, in millisecondi, assegnato a questo thread dalla creazione.

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**ExecutionState**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Condizione operativa corrente del thread.

Questa proprietà viene ereditata dal [**\_ thread CIM.**](cim-thread.md)

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Altro** (1)


</dt> <dd></dd> <dt>

<span id="Ready"></span><span id="ready"></span><span id="READY"></span>

**Pronto** (2)


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

**In** esecuzione (3)


</dt> <dd></dd> <dt>

<span id="Blocked"></span><span id="blocked"></span><span id="BLOCKED"></span>

**Bloccato** (4)


</dt> <dd></dd> <dt>

<span id="Suspended_Blocked"></span><span id="suspended_blocked"></span><span id="SUSPENDED_BLOCKED"></span>

**Sospeso bloccato** (5)


</dt> <dd></dd> <dt>

<span id="Suspended_Ready"></span><span id="suspended_ready"></span><span id="SUSPENDED_READY"></span>

**Pronto sospeso** (6)


</dt> <dd></dd> </dl>

</dd> <dt>

**Handle**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**Override**](../wmisdk/standard-qualifiers.md) ("Handle"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Tool Help Structures \| [**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32) \| th32ThreadID")
</dt> </dl>

Handle a un thread. L'handle ha diritti di accesso completi per impostazione predefinita. Con l'accesso di sicurezza corretto, l'handle può essere usato in qualsiasi funzione che accetta un handle di thread. A seconda del flag di ereditarietà specificato al momento della creazione, questo handle può essere ereditato dai processi figlio.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")
</dt> </dl>

L'oggetto è stato installato. Questa proprietà non richiede un valore per indicare che l'oggetto è installato.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**KernelModeTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Override**](../wmisdk/standard-qualifiers.md) ("KernelModeTime"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Strutture dei dati delle prestazioni Win32API \| \| [**PERF \_ OBJECT \_ TYPE**](/windows/win32/api/winperf/ns-winperf-perf_object_type) \| PrivilegedTime"), [**Unità**](../wmisdk/standard-qualifiers.md) ("100 nanosecondi")
</dt> </dl>

Tempo in modalità kernel, in unità da 100 nanosecondi. Se queste informazioni non sono disponibili, deve essere usato il valore 0 (zero).

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")
</dt> </dl>

Etichetta con cui l'oggetto è noto. Quando è sottoclassata, la proprietà può essere sottoposta a override per essere una proprietà chiave.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**OSCreationClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**propagati**](../wmisdk/standard-qualifiers.md) ("[**Processo CIM \_**](cim-process.md).**OSCreationClassName**"), [**Cim \_ Key,**](../wmisdk/standard-wmi-qualifiers.md) [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Nome della classe di creazione del sistema operativo di ambito.

Questa proprietà viene ereditata dal [**\_ thread CIM.**](cim-thread.md)

</dd> <dt>

**OSName**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**propagati**](../wmisdk/standard-qualifiers.md) ("[**Processo CIM \_**](cim-process.md).**OSName**"), [**Cim \_ Key,**](../wmisdk/standard-wmi-qualifiers.md) [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Nome del sistema operativo di ambito.

Questa proprietà viene ereditata dal [**\_ thread CIM.**](cim-thread.md)

</dd> <dt>

**Priorità**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Override**](../wmisdk/standard-qualifiers.md) ("Priority"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Tool Help Structures \| [**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32) \| tpDeltaPri")
</dt> </dl>

Priorità dinamica del thread. Ogni thread ha una priorità dinamica utilizzata dall'utilità di pianificazione per determinare quale thread eseguire. Inizialmente, la priorità dinamica di un thread corrisponde alla priorità di base. Il sistema può aumentare e ridurre la priorità dinamica, per garantire la velocità di risposta (garantendo che nessun thread sia affamato per il tempo del processore). Il sistema non aumenta la priorità dei thread con un livello di priorità di base compreso tra 16 e 31. Solo i thread con una priorità di base compresa tra 0 e 15 ricevono boost di priorità dinamica. I numeri più elevati indicano priorità più elevate.

</dd> <dt>

**PriorityBase**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Strutture dei dati delle prestazioni Win32API \| \| [**PERF \_ OBJECT \_ TYPE**](/windows/win32/api/winperf/ns-winperf-perf_object_type) \| PerfPriorityBase")
</dt> </dl>

Priorità di base corrente di un thread. Il sistema operativo può aumentare la priorità dinamica del thread sopra la priorità di base se il thread gestisce l'input dell'utente o abbassarlo verso la priorità di base se il thread diventa associato al calcolo. La **proprietà PriorityBase** può avere un valore compreso tra 0 e 31.

</dd> <dt>

**ProcessCreationClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**propagati**](../wmisdk/standard-qualifiers.md) ("[**Processo CIM \_**](cim-process.md).**CreationClassName**"), [**Cim \_ Key,**](../wmisdk/standard-wmi-qualifiers.md) [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Valore della proprietà **CreationClassName del processo di** ambito.

Questa proprietà viene ereditata dal [**\_ thread CIM.**](cim-thread.md)

</dd> <dt>

**ProcessHandle**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**Override**](../wmisdk/standard-qualifiers.md) ("ProcessHandle"), [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**PROCESSO CIM \_**](cim-process.md).**Handle**"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Tool Help Structures \| [**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32) \| th32OwnerProcessID")
</dt> </dl>

Processo che ha creato il thread. Il contenuto di questa proprietà può essere usato da Windows api (Application Programming Interface).

</dd> <dt>

**StartAddress**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Oggetto thread WIn32API \| \| LPTHREAD \_ START ROUTINE \_ \| lpStartAddress")
</dt> </dl>

Indirizzo iniziale del thread. Poiché qualsiasi applicazione con accesso appropriato al thread può modificare il contesto del thread, questo valore può essere solo un'approssimazione dell'indirizzo iniziale del thread.

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")
</dt> </dl>

Stato corrente dell'oggetto. È possibile definire vari stati operativi e non operativi. Gli stati operativi includono: "OK", "Degraded" e "Pred Fail" (un elemento, ad esempio un disco rigido abilitato per SMART, potrebbe funzionare correttamente ma prevedere un errore nel prossimo futuro). Gli stati non di operazione includono: "Error", "Starting", "Stopping" e "Service". Quest'ultimo, "Servizio", può essere applicato durante il ridimensionamento del mirror di un disco, il ricaricamento di un elenco di autorizzazioni utente o altro lavoro amministrativo. Non tutte queste operazioni sono online, ma l'elemento gestito non è né "OK" né in uno degli altri stati.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

I valori possibili sono:

<dt>

<span id="OK"></span><span id="ok"></span>

**OK** ("OK")


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Errore** ("Errore")


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**Degradato** ("Degraded")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** ("Sconosciuto")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Pred Fail** ("Pred Fail")


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**Avvio** ("Avvio")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Arresto** ("Arresto")


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Servizio** ("Servizio")


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Stressed** ("Stressed")


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

**NonRecover** ("NonRecover")


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Nessun contatto** ("Nessun contatto")


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Lost Comm** ("Lost Comm")


</dt> <dd></dd> </dl>

</dd> <dt>

**ThreadState**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Thread State")
</dt> </dl>

Stato di esecuzione corrente per il thread.

<dt>

<span id="Initialized"></span><span id="initialized"></span><span id="INITIALIZED"></span>

<span id="Initialized"></span><span id="initialized"></span><span id="INITIALIZED"></span>**Inizializzato** (0)


</dt> <dd>

Inizializzato: viene riconosciuto dal microkernel.

</dd> <dt>

<span id="Ready"></span><span id="ready"></span><span id="READY"></span>

<span id="Ready"></span><span id="ready"></span><span id="READY"></span>**Pronto** (1)


</dt> <dd>

Pronto: è pronto per l'esecuzione nel successivo processore disponibile.

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**In** esecuzione (2)


</dt> <dd>

In esecuzione: è in esecuzione.

</dd> <dt>

<span id="Standby"></span><span id="standby"></span><span id="STANDBY"></span>

<span id="Standby"></span><span id="standby"></span><span id="STANDBY"></span>**Standby** (3)


</dt> <dd>

Standby: sta per essere eseguito, un solo thread può essere in questo stato alla volta.

</dd> <dt>

<span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>

<span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>**Terminato** (4)


</dt> <dd>

Terminated: l'esecuzione è stata completata.

</dd> <dt>

<span id="Waiting"></span><span id="waiting"></span><span id="WAITING"></span>

<span id="Waiting"></span><span id="waiting"></span><span id="WAITING"></span>**In attesa** (5)


</dt> <dd>

In attesa: non è pronto per il processore, quando è pronto verrà riprogrammato.

</dd> <dt>

<span id="Transition"></span><span id="transition"></span><span id="TRANSITION"></span>

<span id="Transition"></span><span id="transition"></span><span id="TRANSITION"></span>**Transizione** (6)


</dt> <dd>

Transizione: il thread è in attesa di risorse diverse dal processore,

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (7)


</dt> <dd>

Sconosciuto: lo stato del thread è sconosciuto.

</dd> </dl>

</dd> <dt>

**ThreadWaitReason**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Thread Wait Reason")
</dt> </dl>

Motivo per cui il thread è in attesa. Questo valore è valido solo se il **membro ThreadState** è impostato su Transition (6). Le coppie di eventi consentono la comunicazione con i sottosistemi protetti.

<dt>

<span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>

<span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>**Executive** (0)


</dt> <dd></dd> <dt>

<span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>

<span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>**FreePage** (1)


</dt> <dd>

FreePage

</dd> <dt>

<span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>

<span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>**PageIn** (2)


</dt> <dd></dd> <dt>

<span id="PoolAllocation"></span><span id="poolallocation"></span><span id="POOLALLOCATION"></span>

<span id="PoolAllocation"></span><span id="poolallocation"></span><span id="POOLALLOCATION"></span>**PoolAllocation** (3)


</dt> <dd></dd> <dt>

<span id="ExecutionDelay"></span><span id="executiondelay"></span><span id="EXECUTIONDELAY"></span>

<span id="ExecutionDelay"></span><span id="executiondelay"></span><span id="EXECUTIONDELAY"></span>**ExecutionDelay** (4)


</dt> <dd></dd> <dt>

<span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>

<span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>**FreePage** (5)


</dt> <dd></dd> <dt>

<span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>

<span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>**PageIn** (6)


</dt> <dd></dd> <dt>

<span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>

<span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>**Executive** (7)


</dt> <dd></dd> <dt>

<span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>

<span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>**FreePage** (8)


</dt> <dd></dd> <dt>

<span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>

<span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>**PageIn** (9)


</dt> <dd></dd> <dt>

<span id="PoolAllocation"></span><span id="poolallocation"></span><span id="POOLALLOCATION"></span>

<span id="PoolAllocation"></span><span id="poolallocation"></span><span id="POOLALLOCATION"></span>**PoolAllocation** (10)


</dt> <dd></dd> <dt>

<span id="ExecutionDelay"></span><span id="executiondelay"></span><span id="EXECUTIONDELAY"></span>

<span id="ExecutionDelay"></span><span id="executiondelay"></span><span id="EXECUTIONDELAY"></span>**ExecutionDelay** (11)


</dt> <dd></dd> <dt>

<span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>

<span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>**FreePage** (12)


</dt> <dd></dd> <dt>

<span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>

<span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>**PageIn** (13)


</dt> <dd></dd> <dt>

<span id="EventPairHigh"></span><span id="eventpairhigh"></span><span id="EVENTPAIRHIGH"></span>

<span id="EventPairHigh"></span><span id="eventpairhigh"></span><span id="EVENTPAIRHIGH"></span>**EventPairHigh** (14)


</dt> <dd></dd> <dt>

<span id="EventPairLow"></span><span id="eventpairlow"></span><span id="EVENTPAIRLOW"></span>

<span id="EventPairLow"></span><span id="eventpairlow"></span><span id="EVENTPAIRLOW"></span>**EventPairLow** (15)


</dt> <dd></dd> <dt>

<span id="LPCReceive"></span><span id="lpcreceive"></span><span id="LPCRECEIVE"></span>

<span id="LPCReceive"></span><span id="lpcreceive"></span><span id="LPCRECEIVE"></span>**LPCReceive** (16)


</dt> <dd></dd> <dt>

<span id="LPCReply"></span><span id="lpcreply"></span><span id="LPCREPLY"></span>

<span id="LPCReply"></span><span id="lpcreply"></span><span id="LPCREPLY"></span>**LPCReply** (17)


</dt> <dd></dd> <dt>

<span id="VirtualMemory"></span><span id="virtualmemory"></span><span id="VIRTUALMEMORY"></span>

<span id="VirtualMemory"></span><span id="virtualmemory"></span><span id="VIRTUALMEMORY"></span>**VirtualMemory** (18)


</dt> <dd></dd> <dt>

<span id="PageOut"></span><span id="pageout"></span><span id="PAGEOUT"></span>

<span id="PageOut"></span><span id="pageout"></span><span id="PAGEOUT"></span>**PageOut** (19)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (20)


</dt> <dd></dd> </dl>

</dd> <dt>

**UserModeTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Override**](../wmisdk/standard-qualifiers.md) ("UserModeTime"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API Performance \| Data Structures \| [**PERF \_ OBJECT \_ TYPE**](/windows/win32/api/winperf/ns-winperf-perf_object_type) \| UserTime"), [**Units**](../wmisdk/standard-qualifiers.md) ("100 nanoseconds")
</dt> </dl>

Tempo in modalità utente, in unità di 100 nanosecondi. Se queste informazioni non sono disponibili, è necessario usare il valore 0 (zero).

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI.](../wmisdk/creating-a-wmi-script.md)

</dd> </dl>

## <a name="remarks"></a>Commenti

La **classe \_ Thread Win32** è derivata dal [**thread CIM \_**](cim-thread.md).

**Overview**

Per il monitoraggio quotidiano di routine, è in genere poco motivo per avere un elenco dettagliato dei thread e delle relative proprietà associate. I computer creano ed eliminano migliaia di thread nel corso di un giorno e alcune di queste creazioni o eliminazioni sono significative per chiunque, ad esempio lo sviluppatore che ha scritto il software.

Tuttavia, durante la risoluzione dei problemi relativi a un'applicazione, il rilevamento dei singoli thread per un processo consente di identificare quando i thread vengono creati e quando (o se) vengono distrutti. Poiché i thread creati ma non distrutti causano perdite di memoria, il rilevamento di singoli thread può essere utile per i tecnici del supporto tecnico. Analogamente, l'identificazione delle priorità dei thread può aiutare a individuare i thread che, eseguendo con una priorità anomala, prelevano i cicli della CPU necessari per altri thread e altri processi.

**Uso del thread \_ Win32**

Come implicito nel blocco di sintassi precedente, la classe **Thread Win32 \_** non segnala il nome del processo in cui viene eseguito ogni thread. Segnala invece l'ID del processo in cui viene eseguito il thread. Per restituire il nome di un processo e un elenco di tutti i relativi thread, lo script deve:

1.  Connessione alla classe [**Process Win32 \_**](win32-process.md) e restituire l'elenco dei processi e i relativi ID di processo.
2.  Archiviare temporaneamente queste informazioni in una matrice o in un oggetto Dictionary.
3.  Per ogni ID processo, restituire l'elenco dei thread per tale processo e quindi visualizzare il nome del processo e l'elenco dei thread.

## <a name="examples"></a>Esempio

Nell'esempio vbscript seguente vengono monitorati i thread in esecuzione in un computer.


```VB
Set objDictionary = CreateObject("Scripting.Dictionary")
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colProcesses = objWMIService.ExecQuery("SELECT * FROM Win32_Process")
For Each objProcess in colProcesses
 objDictionary.Add objProcess.ProcessID, objProcess.Name
Next
Set colThreads = objWMIService.ExecQuery("SELECT * FROM Win32_Thread")
For Each objThread in colThreads
 intProcessID = CInt(objThread.ProcessHandle)
 strProcessName = objDictionary.Item(intProcessID)
 Wscript.Echo strProcessName & VbTab & objThread.ProcessHandle & _
              VbTab & objThread.Handle & VbTab & objThread.ThreadState
Next
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CIM \_ Thread**](cim-thread.md)
</dt> <dt>

[Classi del sistema operativo](./operating-system-classes.md)
</dt> </dl>

 

 
