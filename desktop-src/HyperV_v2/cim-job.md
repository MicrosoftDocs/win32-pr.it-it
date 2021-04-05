---
description: Elemento logico che rappresenta un'unità di lavoro da eseguire, ad esempio uno script o un processo di stampa. Un processo è diverso da un processo perché un processo può essere pianificato o accodato e l'esecuzione non è limitata a un singolo sistema.
ms.assetid: 35e35c3f-617b-429b-b68f-fa0c0c330e92
title: Classe CIM_Job (gestione Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Job
- CIM_Job.JobStatus
- CIM_Job.TimeSubmitted
- CIM_Job.ScheduledStartTime
- CIM_Job.StartTime
- CIM_Job.ElapsedTime
- CIM_Job.JobRunTimes
- CIM_Job.RunMonth
- CIM_Job.RunDay
- CIM_Job.RunDayOfWeek
- CIM_Job.RunStartInterval
- CIM_Job.LocalOrUtcTime
- CIM_Job.UntilTime
- CIM_Job.Notify
- CIM_Job.Owner
- CIM_Job.Priority
- CIM_Job.PercentComplete
- CIM_Job.DeleteOnCompletion
- CIM_Job.ErrorCode
- CIM_Job.ErrorDescription
- CIM_Job.RecoveryAction
- CIM_Job.OtherRecoveryAction
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6b59a162d36ee677ad00c8cc574282f970bc1d80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968028"
---
# <a name="cim_job-class-hyper-v-management"></a>Classe CIM_Job (gestione Hyper-V)

Elemento logico che rappresenta un'unità di lavoro da eseguire, ad esempio uno script o un processo di stampa. Un processo è diverso da un processo perché un processo può essere pianificato o accodato e l'esecuzione non è limitata a un singolo sistema.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_Job : CIM_LogicalElement
{
  string   JobStatus;
  datetime TimeSubmitted;
  datetime ScheduledStartTime;
  datetime StartTime;
  datetime ElapsedTime;
  uint32   JobRunTimes = 1;
  uint8    RunMonth;
  sint8    RunDay;
  sint8    RunDayOfWeek;
  datetime RunStartInterval;
  uint16   LocalOrUtcTime;
  datetime UntilTime;
  string   Notify;
  string   Owner;
  uint32   Priority;
  uint16   PercentComplete;
  boolean  DeleteOnCompletion;
  uint16   ErrorCode;
  string   ErrorDescription;
  uint16   RecoveryAction;
  string   OtherRecoveryAction;
};
```

## <a name="members"></a>Members

La classe del **\_ processo CIM** presenta questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La classe del **\_ processo CIM** presenta questi metodi.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Metodo</th>
<th style="text-align: left;">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><a href="cim-job-killjob.md"><strong>KillJob</strong></a></td>
<td style="text-align: left;">Questo metodo è deprecato. Usare invece il metodo <strong>RequestStateChange</strong> .<br/>
<blockquote>
[!Note]<br />
Descrizione deprecata: arresta un processo.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a>Proprietà

La classe del **\_ processo CIM** dispone di queste proprietà.

<dl> <dt>

**DeleteOnCompletion**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

**True** per eliminare il processo al completamento; in caso contrario, **false**.

> [!Note]  
> Questa proprietà non eliminerà i processi che vengono completati prima che questa proprietà sia impostata su **true**.

 

</dd> <dt>

**ElapsedTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Durata dell'esecuzione del processo.

</dd> <dt>

**ErrorCode**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ processo CIM**.**ErrorDescription**")
</dt> </dl>

Codice di errore specifico del fornitore che acquisisce le informazioni di elaborazione per i processi ricorrenti. Se il processo è stato completato senza errori, il valore deve essere impostato su zero.

</dd> <dt>

**ErrorDescription**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ processo CIM**.**ErrorCode**")
</dt> </dl>

Stringa in formato libero che contiene una descrizione del codice di errore corrispondente nella proprietà **ErrorCode** .

</dd> <dt>

**JobRunTimes**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Il numero di volte in cui eseguire il processo.

</dd> <dt>

**Stato processo**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).**OperationalStatus**")
</dt> </dl>

Stringa in formato libero che rappresenta lo stato del processo.

</dd> <dt>

**LocalOrUtcTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Indica se le ore nelle proprietà **RunStartInterval** e **UntilTime** rappresentano le ore locali o l'ora UTC.

<dt>

<span id="Local_Time"></span><span id="local_time"></span><span id="LOCAL_TIME"></span>

**Ora locale** (1)


</dt> <dd></dd> <dt>

<span id="UTC_Time"></span><span id="utc_time"></span><span id="UTC_TIME"></span>

**Ora UTC** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**Notificare**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Utente a cui inviare una notifica quando un processo viene completato o ha esito negativo.

</dd> <dt>

**OtherRecoveryAction**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ processo CIM**.**RecoveryAction**")
</dt> </dl>

Stringa che descrive l'azione di ripristino quando la proprietà **RecoveryAction** è **diversa** ("1").

</dd> <dt>

**Proprietario**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ OwningJobElement**](cim-owningjobelement.md).")
</dt> </dl>

Utente che ha inviato il processo oppure il nome del servizio o del metodo che ha richiesto il processo.

</dd> <dt>

**PercentComplete**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("percentuale"), [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (101), **punito** ("percentuale")
</dt> </dl>

Percentuale del processo completato.

> [!Note]  
> Il valore "101" non è definito e non sarà consentito nella successiva revisione principale della specifica.

 

</dd> <dt>

**Priorità**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Importanza del processo. Più è basso il numero, maggiore sarà la priorità.

</dd> <dt>

**RecoveryAction**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ processo CIM**.**OtherRecoveryAction**")
</dt> </dl>

Descrive l'azione di ripristino da eseguire in caso di esito negativo di un processo di esecuzione.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)


</dt> <dd>

Non è noto come azione di ripristino da eseguire.

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)


</dt> <dd>

L'azione di ripristino verrà specificata nella proprietà **OtherRecoveryAction** .

</dd> <dt>

<span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>

<span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>**Non continuare** (2)


</dt> <dd>

Arrestare l'esecuzione del processo e aggiornarne lo stato in modo appropriato.

</dd> <dt>

<span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>

<span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>**Continua con il processo successivo** (3)


</dt> <dd>

Continuare con il processo successivo nella coda.

</dd> <dt>

<span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>

<span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>**Esegui di nuovo il processo** (4)


</dt> <dd>

Il processo deve essere eseguito nuovamente.

</dd> <dt>

<span id="Run_Recovery_Job"></span><span id="run_recovery_job"></span><span id="RUN_RECOVERY_JOB"></span>

<span id="Run_Recovery_Job"></span><span id="run_recovery_job"></span><span id="RUN_RECOVERY_JOB"></span>**Esegui processo di ripristino** (5)


</dt> <dd>

Eseguire il processo associato usando la relazione di **RecoveryJob** . Si noti che il processo di ripristino deve essere già presente nella coda da cui verrà eseguito.

</dd> </dl>

</dd> <dt>

**RunDay**
</dt> <dd> <dl> <dt>

Tipo di dati: **sint8**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (-31), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (31), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ processo CIM**.**RunMonth**","**\_ processo CIM**.**RunDayOfWeek**","**\_ processo CIM**.**RunStartInterval**")
</dt> </dl>

Intero utilizzato in combinazione con la proprietà **RunDayOfWeek** per indicare il giorno in cui il processo viene elaborato; in alternativa, se **RunDayOfWeek** è impostato su zero, **RunDay** indica il giorno del mese in cui viene elaborato il processo. Se **RunDay** è un numero intero negativo, specifica un giorno relativo alla fine del mese o, se **RunDay** è un numero intero positivo, specifica un giorno relativo all'inizio del mese.

</dd> <dt>

**RunDayOfWeek**
</dt> <dd> <dl> <dt>

Tipo di dati: **sint8**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ processo CIM**.**RunMonth**","**\_ processo CIM**.**RunDay**","**\_ processo CIM**.**RunStartInterval**")
</dt> </dl>

Intero utilizzato in combinazione con la proprietà **RunDay** per indicare il giorno in cui il processo viene elaborato; in alternativa, se **RunDayOfWeek** è impostato su zero, **RunDay** indica il giorno del mese in cui viene elaborato il processo.

<dt>

<span id="-Saturday"></span><span id="-saturday"></span><span id="-SATURDAY"></span>

**-Sabato** (-7)


</dt> <dd></dd> <dt>

<span id="-Friday"></span><span id="-friday"></span><span id="-FRIDAY"></span>

**-Venerdì** (-6)


</dt> <dd></dd> <dt>

<span id="-Thursday"></span><span id="-thursday"></span><span id="-THURSDAY"></span>

**-Giovedi** (-5)


</dt> <dd></dd> <dt>

<span id="-Wednesday"></span><span id="-wednesday"></span><span id="-WEDNESDAY"></span>

**-Mercoledì** (-4)


</dt> <dd></dd> <dt>

<span id="-Tuesday"></span><span id="-tuesday"></span><span id="-TUESDAY"></span>

**-Martedì** (-3)


</dt> <dd></dd> <dt>

<span id="-Monday"></span><span id="-monday"></span><span id="-MONDAY"></span>

**-Lunedì** (-2)


</dt> <dd></dd> <dt>

<span id="-Sunday"></span><span id="-sunday"></span><span id="-SUNDAY"></span>

**-Domenica** (-1)


</dt> <dd></dd> <dt>

<span id="ExactDayOfMonth"></span><span id="exactdayofmonth"></span><span id="EXACTDAYOFMONTH"></span>

**ExactDayOfMonth** (0)


</dt> <dd></dd> <dt>

<span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>

**Domenica** (1)


</dt> <dd></dd> <dt>

<span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>

**Lunedì** (2)


</dt> <dd></dd> <dt>

<span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>

**Martedì** (3)


</dt> <dd></dd> <dt>

<span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>

**Mercoledì** (4)


</dt> <dd></dd> <dt>

<span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>

**Giovedi** (5)


</dt> <dd></dd> <dt>

<span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>

**Venerdì** (6)


</dt> <dd></dd> <dt>

<span id="Saturday"></span><span id="saturday"></span><span id="SATURDAY"></span>

**Sabato** (7)


</dt> <dd></dd> </dl>

</dd> <dt>

**RunMonth**
</dt> <dd> <dl> <dt>

Tipo di dati: **Uint8**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ processo CIM**.**RunDay**","**\_ processo CIM**.**RunDayOfWeek**","**\_ processo CIM**.**RunStartInterval**")
</dt> </dl>

Mese in cui viene elaborato il processo.

<dt>

<span id="January"></span><span id="january"></span><span id="JANUARY"></span>

**Gennaio** (0)


</dt> <dd></dd> <dt>

<span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>

**Febbraio** (1)


</dt> <dd></dd> <dt>

<span id="March"></span><span id="march"></span><span id="MARCH"></span>

**Marzo** (2)


</dt> <dd></dd> <dt>

<span id="April"></span><span id="april"></span><span id="APRIL"></span>

**Aprile** (3)


</dt> <dd></dd> <dt>

<span id="May"></span><span id="may"></span><span id="MAY"></span>

**Maggio** (4)


</dt> <dd></dd> <dt>

<span id="June"></span><span id="june"></span><span id="JUNE"></span>

**Giugno** (5)


</dt> <dd></dd> <dt>

<span id="July"></span><span id="july"></span><span id="JULY"></span>

**Luglio** (6)


</dt> <dd></dd> <dt>

<span id="August"></span><span id="august"></span><span id="AUGUST"></span>

**Agosto** (7)


</dt> <dd></dd> <dt>

<span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>

**Settembre** (8)


</dt> <dd></dd> <dt>

<span id="October"></span><span id="october"></span><span id="OCTOBER"></span>

**Ottobre** (9)


</dt> <dd></dd> <dt>

<span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>

**Novembre** (10)


</dt> <dd></dd> <dt>

<span id="December"></span><span id="december"></span><span id="DECEMBER"></span>

**Dicembre** (11)


</dt> <dd></dd> </dl>

</dd> <dt>

**RunStartInterval**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ processo CIM**.**RunMonth**","**\_ processo CIM**.**RunDay**","**\_ processo CIM**.**RunDayOfWeek**","**\_ processo CIM**.**RunStartInterval**")
</dt> </dl>

Intervallo di tempo dopo la mezzanotte di elaborazione del processo. Ad esempio, "00000000020000.000000:000" indica che il processo viene eseguito in data o dopo due ore o ora locale o ora UTC (UTC viene specificato con la proprietà **LocalOrUtcTime** ).

</dd> <dt>

**ScheduledStartTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**\_ processo CIM**.**RunMonth**","**\_ processo CIM**.**RunDay**","**\_ processo CIM**.**RunDayOfWeek**","**\_ processo CIM**.**RunStartInterval**")
</dt> </dl>

> [!Note]  
> Questa proprietà è deprecata. È invece consigliabile usare le proprietà **RunMonth**, **RunDay**, **RunDayOfWeek** e **RunStartInterval** .

 

Ora pianificata per l'avvio del processo corrente. Questa ora può essere rappresentata da una data e un'ora oppure da un intervallo relativo all'ora in cui la proprietà viene richiesta. Un valore di tutti gli zeri indica che il processo è già in esecuzione.

</dd> <dt>

**StartTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ora di inizio del processo. Questa ora può essere rappresentata da una data e un'ora o da un intervallo relativo all'ora in cui è richiesta la proprietà.

</dd> <dt>

**TimeSubmitted**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ora di invio del processo. Un valore di tutti gli zeri indica che l'elemento padre non è in grado di segnalare una data e un'ora.

</dd> <dt>

**UntilTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ processo CIM**.**LocalOrUtcTime**")
</dt> </dl>

Tempo trascorso il quale il processo diventa non valido o deve essere arrestato. L'ora può essere rappresentata da una data e un'ora o da un intervallo relativo all'ora in cui questa proprietà è richiesta. Un valore di tutte le nove indica che il processo può essere eseguito A tempo indefinito.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                                    |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                                          |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_LogicalElement CIM**](cim-logicalelement.md)
</dt> </dl>

 

