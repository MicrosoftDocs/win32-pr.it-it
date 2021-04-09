---
description: Rappresenta un processo creato con il comando AT.
ms.assetid: 2fa69e3f-9a6c-4aa9-8a6c-ea28eb4342ca
ms.tgt_platform: multiple
title: Classe Win32_ScheduledJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ScheduledJob
- Win32_ScheduledJob.Caption
- Win32_ScheduledJob.Description
- Win32_ScheduledJob.InstallDate
- Win32_ScheduledJob.Name
- Win32_ScheduledJob.Status
- Win32_ScheduledJob.ElapsedTime
- Win32_ScheduledJob.Notify
- Win32_ScheduledJob.Owner
- Win32_ScheduledJob.Priority
- Win32_ScheduledJob.TimeSubmitted
- Win32_ScheduledJob.UntilTime
- Win32_ScheduledJob.Command
- Win32_ScheduledJob.DaysOfMonth
- Win32_ScheduledJob.DaysOfWeek
- Win32_ScheduledJob.InteractWithDesktop
- Win32_ScheduledJob.JobId
- Win32_ScheduledJob.JobStatus
- Win32_ScheduledJob.RunRepeatedly
- Win32_ScheduledJob.StartTime
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 50162221e7ca18e07e3599deca2dba67b18ba708
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049117"
---
# <a name="win32_scheduledjob-class"></a>Win32 \_ ScheduledJob (classe)

La  [classe WMI](../wmisdk/retrieving-a-class.md) **\_ ScheduledJob Win32**   rappresenta un processo creato con il comando **at** .

> [!Note]  
> La classe **Win32 \_ ScheduledJob** non rappresenta un processo creato con la creazione guidata attività pianificata dal pannello di controllo. Non è possibile modificare un'attività creata da WMI nell'interfaccia utente delle attività pianificate. Per altre informazioni, vedere la sezione Osservazioni.

 

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4E0-5FBB-11D2-AAC1-006008C78BC7}"), SupportsCreate, CreateBy("Create"), SupportsDelete, DeleteBy("Delete"), AMENDMENT]
class Win32_ScheduledJob : CIM_Job
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  datetime ElapsedTime;
  string   Notify;
  string   Owner;
  uint32   Priority;
  datetime TimeSubmitted;
  datetime UntilTime;
  string   Command;
  uint32   DaysOfMonth;
  uint32   DaysOfWeek;
  boolean  InteractWithDesktop;
  uint32   JobId;
  string   JobStatus;
  boolean  RunRepeatedly;
  datetime StartTime;
};
```

## <a name="members"></a>Members

La classe **Win32 \_ ScheduledJob** presenta questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La classe **Win32 \_ ScheduledJob** presenta questi metodi.



| Metodo                                                      | Descrizione                                                                                                           |
|:------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------|
| [**Creare**](create-method-in-class-win32-scheduledjob.md) | Metodo della classe che invia un processo al sistema operativo per l'esecuzione in una data e ora future specificate.<br/> |
| [**Delete**](delete-method-in-class-win32-scheduledjob.md) | Metodo della classe che elimina un processo pianificato.<br/>                                                                 |



 

### <a name="properties"></a>Proprietà

La classe **Win32 \_ ScheduledJob** dispone di queste proprietà.

<dl> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")
</dt> </dl>

Breve descrizione testuale dell'oggetto.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**Comando**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**at \_ info**](/windows/win32/api/lmat/ns-lmat-at_info) \| **Command**")
</dt> </dl>

Nome del comando, del programma batch o del file binario (e degli argomenti della riga di comando) usati dal servizio Schedule per richiamare il processo.

Esempio: "**Defrag** **/q/f**"

</dd> <dt>

**DaysOfMonth**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**at \_ info**](/windows/win32/api/lmat/ns-lmat-at_info) \| **DaysOfMonth**")
</dt> </dl>

Giorni del mese in cui è pianificata l'esecuzione del processo. Se un processo è pianificato per essere eseguito in più giorni del mese, questi valori possono essere Uniti in un OR logico. Se, ad esempio, un processo deve essere eseguito il 1 ° e il sedicesimo di ogni mese, il valore della proprietà **DaysOfMonth** sarà 1 o 32768.

<dt>

<span id="1"></span>

<span id="1"></span>**1** (1)


</dt> <dd>

1 °

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2** (2)


</dt> <dd>

secondo

</dd> <dt>

<span id="3"></span>

<span id="3"></span>**3** (4)


</dt> <dd>

3°

</dd> <dt>

<span id="4"></span>

<span id="4"></span>**4** (8)


</dt> <dd>

4°

</dd> <dt>

<span id="5"></span>

<span id="5"></span>**5** (16)


</dt> <dd>

5°

</dd> <dt>

<span id="6"></span>

<span id="6"></span>**6** (32)


</dt> <dd>

6°

</dd> <dt>

<span id="7"></span>

<span id="7"></span>**7** (64)


</dt> <dd>

7°

</dd> <dt>

<span id="8"></span>

<span id="8"></span>**8** (128)


</dt> <dd>

8°

</dd> <dt>

<span id="9"></span>

<span id="9"></span>**9** (256)


</dt> <dd>

9°

</dd> <dt>

<span id="10"></span>

<span id="10"></span>**10** (512)


</dt> <dd>

10

</dd> <dt>

<span id="11"></span>

<span id="11"></span>**11** (1024)


</dt> <dd>

11°

</dd> <dt>

<span id="12"></span>

<span id="12"></span>**12** (2048)


</dt> <dd>

12°

</dd> <dt>

<span id="13"></span>

<span id="13"></span>**13** (4096)


</dt> <dd>

13°

</dd> <dt>

<span id="14"></span>

<span id="14"></span>**14** (8192)


</dt> <dd>

14

</dd> <dt>

<span id="15"></span>

<span id="15"></span>**15** (16384)


</dt> <dd>

15

</dd> <dt>

<span id="16"></span>

<span id="16"></span>**16** (32768)


</dt> <dd>

16

</dd> <dt>

<span id="17"></span>

<span id="17"></span>**17** (65536)


</dt> <dd>

17

</dd> <dt>

<span id="18"></span>

<span id="18"></span>**18** (131072)


</dt> <dd>

18

</dd> <dt>

<span id="19"></span>

<span id="19"></span>**19** (262144)


</dt> <dd>

19

</dd> <dt>

<span id="20"></span>

<span id="20"></span>**20** (524288)


</dt> <dd>

20

</dd> <dt>

<span id="21"></span>

<span id="21"></span>**21** (1048576)


</dt> <dd>

21°

</dd> <dt>

<span id="22"></span>

<span id="22"></span>**22** (2097152)


</dt> <dd>

22°

</dd> <dt>

<span id="23"></span>

<span id="23"></span>**23** (4194304)


</dt> <dd>

23°

</dd> <dt>

<span id="24"></span>

<span id="24"></span>**24** (8388608)


</dt> <dd>

24

</dd> <dt>

<span id="25"></span>

<span id="25"></span>**25** (16777216)


</dt> <dd>

25

</dd> <dt>

<span id="26"></span>

<span id="26"></span>**26** (33554432)


</dt> <dd>

26

</dd> <dt>

<span id="27"></span>

<span id="27"></span>**27** (67108864)


</dt> <dd>

27

</dd> <dt>

<span id="28"></span>

<span id="28"></span>**28** (134217728)


</dt> <dd>

28

</dd> <dt>

<span id="29"></span>

<span id="29"></span>**29** (268435456)


</dt> <dd>

29

</dd> <dt>

<span id="30"></span>

<span id="30"></span>**30** (536870912)


</dt> <dd>

30

</dd> <dt>

<span id="31"></span>

<span id="31"></span>**31** (1073741824)


</dt> <dd>

31

</dd> </dl>

</dd> <dt>

**DaysOfWeek**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**at \_ info**](/windows/win32/api/lmat/ns-lmat-at_info) \| **DaysOfWeek**")
</dt> </dl>

Giorni della settimana in cui è pianificata l'esecuzione di un processo. Se un processo è pianificato per essere eseguito in più giorni della settimana, i valori possono essere Uniti in un OR logico. Se, ad esempio, si pianifica l'esecuzione di un processo lunedì, mercoledì e venerdì, il valore della proprietà **DaysOfWeek** sarà 1 o 4 o 16.

<dt>

<span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>

**Lunedì** (1)


</dt> <dd></dd> <dt>

<span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>

**Martedì** (2)


</dt> <dd></dd> <dt>

<span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>

**Mercoledì** (4)


</dt> <dd></dd> <dt>

<span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>

**Giovedi** (8)


</dt> <dd></dd> <dt>

<span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>

**Venerdì** (16)


</dt> <dd></dd> <dt>

<span id="Saturday"></span><span id="saturday"></span><span id="SATURDAY"></span>

**Sabato** (32)


</dt> <dd></dd> <dt>

<span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>

**Domenica** (64)


</dt> <dd></dd> </dl>

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")
</dt> </dl>

Descrizione testuale dell'oggetto.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**ElapsedTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Periodo di tempo durante il quale il processo è stato eseguito.

Questa proprietà viene ereditata [**dal \_ processo CIM**](cim-job.md).

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data di installazione ")
</dt> </dl>

Indica quando l'oggetto è stato installato. La mancanza di un valore non indica che l'oggetto non è installato.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**InteractWithDesktop**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**at \_ info**](/windows/win32/api/lmat/ns-lmat-at_info) \| **Flags** \| **Job \_ Interactive**")
</dt> </dl>

Il processo specificato è interattivo, il che significa che un utente può fornire l'input a un processo pianificato mentre è in esecuzione.

</dd> <dt>

**JobId**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**at \_ enum**](/windows/win32/api/lmat/ns-lmat-at_enum) \| **JobID**")
</dt> </dl>

Numero di identificazione del processo. Viene usato dai metodi come handle per un processo pianificato in questo computer.

</dd> <dt>

**Stato processo**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](../wmisdk/standard-qualifiers.md) ("JobStatus"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**at \_ enum**](/windows/win32/api/lmat/ns-lmat-at_enum) \| **Flags** \| **Job \_ Exec \_ Error**")
</dt> </dl>

Stato di esecuzione dell'ultima volta in cui è stato pianificato l'esecuzione del processo.

<dt>

<span id="Success"></span><span id="success"></span><span id="SUCCESS"></span>

**Esito positivo** ("operazione riuscita")


</dt> <dd></dd> <dt>

<span id="Failure"></span><span id="failure"></span><span id="FAILURE"></span>

**Errore** ("errore")


</dt> <dd></dd> </dl>

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")
</dt> </dl>

Etichetta con cui l'oggetto è noto. Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**Notificare**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

L'utente riceve una notifica al completamento o all'esito negativo del processo.

Questa proprietà viene ereditata [**dal \_ processo CIM**](cim-job.md).

</dd> <dt>

**Proprietario**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Utente che ha inviato il processo.

Questa proprietà viene ereditata [**dal \_ processo CIM**](cim-job.md).

</dd> <dt>

**Priorità**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Importanza dell'esecuzione di un processo.

Questa proprietà viene ereditata [**dal \_ processo CIM**](cim-job.md).

</dd> <dt>

**RunRepeatedly**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API le \| strutture \| [**di gestione di rete nel processo di flag \_ info**](/windows/win32/api/lmat/ns-lmat-at_info) \|  \| **\_ vengono eseguite \_ periodicamente**")
</dt> </dl>

Il processo pianificato viene eseguito ripetutamente nei giorni in cui il processo è pianificato. Se **false**, il processo viene eseguito una sola volta.

</dd> <dt>

**StartTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](../wmisdk/standard-qualifiers.md) ("StartTime"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**at \_ enum**](/windows/win32/api/lmat/ns-lmat-at_enum) \| **JobTime**")
</dt> </dl>

Ora UTC in cui eseguire il processo, nel formato "ad aaaammgghhmmss. MMMMMM (+-) OOO ", dove" AAAAMMGG "deve essere sostituito da" \* \* \* \* \* \* \* \* ". La sostituzione è necessaria perché il servizio di pianificazione consente solo la configurazione dei processi per l'esecuzione una sola volta o l'esecuzione in un giorno del mese o settimana. Un processo non può essere eseguito in una data specifica.

La sezione "(+-) OOO" del valore della proprietà **StartTime** è la distorsione corrente per la conversione dell'ora locale. La distorsione è la differenza tra l'ora UTC e l'ora locale. Per calcolare la distorsione per il fuso orario, moltiplicare il numero di ore per cui il fuso orario è in anticipo o dietro la ora di Greenwich (GMT) di 60 (usare un numero positivo per il numero di ore se il fuso orario è preceduto da GMT e un numero negativo se il fuso orario è dietro GMT). Aggiungere un ulteriore 60 al calcolo se il fuso orario USA l'ora legale. Ad esempio, il fuso orario Pacifico standard è di otto ore dietro GMT, quindi la distorsione è uguale a-420 (-8 \* 60 + 60) quando l'ora legale è in uso e-480 (-8 \* 60) quando l'ora legale non è in uso. È anche possibile determinare il valore della distorsione eseguendo una query sulla proprietà bias della classe [**del \_ fuso orario Win32**](win32-timezone.md) .

Ad esempio: " \* \* \* \* \* \* \* \* 123000.000000-420" specifica 14,30 (2:30) PST con ora legale in vigore.

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")
</dt> </dl>

Stringa che indica lo stato corrente dell'oggetto. È possibile definire lo stato operativo e non operativo. Lo stato operativo può includere "OK", "danneggiato" e "errore predazione". "Predator fail" indica che un elemento funziona correttamente, ma sta stimando un errore, ad esempio un'unità disco rigido abilitata per SMART.

Lo stato non operativo può includere "Error", "starting", "stoping" e "Service". Il "servizio" può essere applicato durante il mirroring del disco, ovvero la riattivazione, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative. Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.

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

**TimeSubmitted**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ora di invio del processo.

Questa proprietà viene ereditata [**dal \_ processo CIM**](cim-job.md).

</dd> <dt>

**UntilTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ora in cui il processo non è valido o deve essere arrestato.

Questa proprietà viene ereditata [**dal \_ processo CIM**](cim-job.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

Ogni processo pianificato per il servizio Schedule viene archiviato in modo permanente (l'utilità di pianificazione può avviare un processo dopo un riavvio) e viene eseguito all'ora e al giorno della settimana o del mese specificati. Se il computer non è attivo o se il servizio pianificato non è in esecuzione all'ora del processo specificata, il servizio Schedule esegue il processo specificato il giorno successivo all'ora specificata.

I processi sono pianificati in base all'ora UTC (Coordinated Universal Time) con offset di distorsione rispetto all'ora di Greenwich (GMT), il che significa che è possibile specificare un processo usando qualsiasi fuso orario. La classe **Win32 \_ ScheduledJob** restituisce l'ora locale con offset UTC durante l'enumerazione di un oggetto e viene convertita nell'ora locale durante la creazione di nuovi processi. Ad esempio, un processo specificato per l'esecuzione in un computer a Boston alle ore 10:30. Il tempo di lunedì PST verrà pianificato per essere eseguito localmente alle ore 1:30. Martedì EST.

> [!Note]  
> Un client deve prendere in considerazione se l'ora legale è in esecuzione nel computer locale e, in tal caso, sottrarre un bias di 60 minuti dall'offset UTC.

 

La classe **Win32 \_ ScheduledJob** è derivata dal [**\_ processo CIM**](cim-job.md). Per creare un processo pianificato utilizzando questa classe, è necessario essere membri del gruppo Administrators.

La classe **Win32 \_ ScheduledJob** utilizza internamente il protocollo at, che è associato a deprecazione a partire da Windows 8 e Windows Server 2012. Come primo passaggio, il protocollo AT è disabilitato per impostazione predefinita. Se il protocollo è disabilitato, ad esempio la chiamata al metodo [**create**](create-method-in-class-win32-scheduledjob.md) su un oggetto **Win32 \_ ScheduledJob** avrà esito negativo con errore 0x8. È possibile attivare di nuovo il protocollo AT aggiungendo la seguente voce del registro di sistema:

``` syntax
Key: HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Schedule\Configuration 
Name: EnableAt 
Type: REG_DWORD
Value: 1
```

Potrebbe essere necessario riavviare il computer per rendere effettiva l'impostazione.

Poiché **Win32 \_ ScheduledJob** è basato sull'API Win32 [**NetScheduleJobGetInfo**](/windows/win32/api/lmat/nf-lmat-netschedulejobgetinfo) , non è possibile usare questa classe insieme al utilità di pianificazione. Se si desidera utilizzare Utilità di pianificazione, utilizzare l'API Utilità di pianificazione. Per ulteriori informazioni, vedere il [riferimento utilità di pianificazione](../taskschd/task-scheduler-reference.md).

## <a name="examples"></a>Esempio

Nell'esempio di codice VBScript seguente viene pianificato Notepad.exe per l'esecuzione interattiva a 1:25 dall'ora del computer locale ogni mercoledì.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\Root\CIMv2")
Set objNewJob = objWMIService.Get("Win32_ScheduledJob")
errJobCreated = objNewJob.Create("Notepad.exe", "********012500.000000-420", True , 4, , True, JobId) 
If errJobCreated <> 0 Then
Wscript.Echo "Error on task creation"
Else
Wscript.Echo "Task created"
End If
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

[**\_Processo CIM**](cim-job.md)
</dt> <dt>

[Classi del sistema operativo](./operating-system-classes.md)
</dt> <dt>

[Attività WMI: attività pianificate](../wmisdk/wmi-tasks--scheduled-tasks.md)
</dt> </dl>

 

 
