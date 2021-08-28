---
description: Elemento logico che rappresenta un'unità di lavoro da eseguire, ad esempio uno script o un processo di stampa. Un processo è distinto da un processo perché un processo può essere pianificato o accodato e la relativa esecuzione non è limitata a un singolo sistema.
ms.assetid: 35e35c3f-617b-429b-b68f-fa0c0c330e92
title: CIM_Job classe (gestione Hyper-V)
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
ms.openlocfilehash: 8eb8f63ec9d2cdd881a2ba0946f83a40fb8be866
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474587"
---
# <a name="cim_job-class-hyper-v-management"></a>CIM_Job classe (gestione Hyper-V)

Elemento logico che rappresenta un'unità di lavoro da eseguire, ad esempio uno script o un processo di stampa. Un processo è distinto da un processo perché un processo può essere pianificato o accodato e la relativa esecuzione non è limitata a un singolo sistema.

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

La **classe \_ Di processo CIM** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe di \_ processo CIM** include questi metodi.




| Metodo | Descrizione | 
|--------|-------------|
| <a href="cim-job-killjob.md"><strong>KillJob</strong></a> | Questo metodo è deprecato. Usare invece il <strong>metodo RequestStateChange.</strong><br /><blockquote>[!Note]<br />Descrizione deprecata: arresta un processo.</blockquote><br /> | 




 

### <a name="properties"></a>Proprietà

La **classe \_ di processo CIM** ha queste proprietà.

<dl> <dt>

**DeleteOnCompletion**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

**True** per eliminare il processo al completamento. in caso contrario, **false**.

> [!Note]  
> Questa proprietà non eliminerà i processi completati prima che questa proprietà sia impostata su **True.**

 

</dd> <dt>

**ElapsedTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Durata dell'esecuzione del processo.

</dd> <dt>

**ErrorCode**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**PROCESSO CIM \_**.**ErrorDescription**")
</dt> </dl>

Codice di errore specifico del fornitore che acquisisce le informazioni di elaborazione per i processi ricorrenti. Il valore deve essere impostato su zero se il processo è stato completato senza errori.

</dd> <dt>

**ErrorDescription**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**PROCESSO CIM \_**.**ErrorCode**")
</dt> </dl>

Stringa in formato libero contenente una descrizione del codice di errore corrispondente nella **proprietà ErrorCode.**

</dd> <dt>

**JobRunTimes**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Numero di volte in cui eseguire il processo.

</dd> <dt>

**Stato processo**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).**OperationalStatus**")
</dt> </dl>

Stringa in formato libero che rappresenta lo stato del processo.

</dd> <dt>

**LocalOrUtcTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Indica se le ore nelle proprietà **RunStartInterval** e **UntilTime** rappresentano ora locale o ora UTC.

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

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

L'utente a cui inviare una notifica quando un processo viene completato o ha esito negativo.

</dd> <dt>

**OtherRecoveryAction**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**PROCESSO CIM \_**.**RecoveryAction ")**
</dt> </dl>

Stringa che descrive l'azione di ripristino quando la **proprietà RecoveryAction** **è Other** ("1").

</dd> <dt>

**Proprietario**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ OwningJobElement**](cim-owningjobelement.md).")
</dt> </dl>

L'utente che ha inviato il processo o il nome del servizio o del metodo che ha richiesto il processo.

</dd> <dt>

**PercentComplete**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Percent"), [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (101), **PUnit** ("percent")
</dt> </dl>

Percentuale di completamento del processo.

> [!Note]  
> Il valore "101" non è definito e non sarà consentito nella successiva revisione principale della specifica.

 

</dd> <dt>

**Priorità**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Importanza del processo. Più è basso il numero, maggiore sarà la priorità.

</dd> <dt>

**RecoveryAction**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**PROCESSO CIM \_**.**OtherRecoveryAction**")
</dt> </dl>

Descrive l'azione di ripristino da eseguire quando un processo di esecuzione ha esito negativo.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)


</dt> <dd>

Non si sa quale azione di ripristino intraprendere.

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)


</dt> <dd>

L'azione di ripristino verrà specificata nella **proprietà OtherRecoveryAction.**

</dd> <dt>

<span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>

<span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>**Non continuare** (2)


</dt> <dd>

Arrestare l'esecuzione del processo e aggiornarne in modo appropriato lo stato.

</dd> <dt>

<span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>

<span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>**Continua con processo successivo** (3)


</dt> <dd>

Continuare con il processo successivo nella coda.

</dd> <dt>

<span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>

<span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>**Eseguire di nuovo il processo** (4)


</dt> <dd>

Il processo deve essere rieseguiti.

</dd> <dt>

<span id="Run_Recovery_Job"></span><span id="run_recovery_job"></span><span id="RUN_RECOVERY_JOB"></span>

<span id="Run_Recovery_Job"></span><span id="run_recovery_job"></span><span id="RUN_RECOVERY_JOB"></span>**Esegui processo di ripristino** (5)


</dt> <dd>

Eseguire il processo associato usando la **relazione RecoveryJob.** Si noti che il processo di ripristino deve essere già presente nella coda da cui verrà eseguito.

</dd> </dl>

</dd> <dt>

**RunDay**
</dt> <dd> <dl> <dt>

Tipo di dati: **sint8**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> <dt>

Qualificatori: [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (-31), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (31), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ Job**.**RunMonth**", "**PROCESSO CIM \_**.**RunDayOfWeek**", "**Processo CIM \_**.**RunStartInterval**")
</dt> </dl>

Intero utilizzato in combinazione con la **proprietà RunDayOfWeek** per indicare il giorno di elaborazione del processo. oppure, se **RunDayOfWeek** è impostato su zero, **RunDay** indica il giorno del mese in cui viene elaborato il processo. Se **RunDay** è un numero intero negativo, specifica un giorno relativo alla fine del mese oppure, se **RunDay** è un numero intero positivo, specifica un giorno relativo all'inizio del mese.

</dd> <dt>

**RunDayOfWeek**
</dt> <dd> <dl> <dt>

Tipo di dati: **sint8**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**PROCESSO CIM \_**.**RunMonth**", "**PROCESSO CIM \_**.**RunDay**", "**PROCESSO CIM \_**.**RunStartInterval**")
</dt> </dl>

Intero utilizzato in combinazione con la **proprietà RunDay** per indicare il giorno in cui viene elaborato il processo. oppure, se **RunDayOfWeek** è impostato su zero, **RunDay** indica il giorno del mese in cui viene elaborato il processo.

<dt>

<span id="-Saturday"></span><span id="-saturday"></span><span id="-SATURDAY"></span>

**-Saturday** (-7)


</dt> <dd></dd> <dt>

<span id="-Friday"></span><span id="-friday"></span><span id="-FRIDAY"></span>

**-Friday** (-6)


</dt> <dd></dd> <dt>

<span id="-Thursday"></span><span id="-thursday"></span><span id="-THURSDAY"></span>

**-Thursday** (-5)


</dt> <dd></dd> <dt>

<span id="-Wednesday"></span><span id="-wednesday"></span><span id="-WEDNESDAY"></span>

**-Mercoledì** (-4)


</dt> <dd></dd> <dt>

<span id="-Tuesday"></span><span id="-tuesday"></span><span id="-TUESDAY"></span>

**-Tuesday** (-3)


</dt> <dd></dd> <dt>

<span id="-Monday"></span><span id="-monday"></span><span id="-MONDAY"></span>

**-Monday** (-2)


</dt> <dd></dd> <dt>

<span id="-Sunday"></span><span id="-sunday"></span><span id="-SUNDAY"></span>

**-Sunday** (-1)


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

**Giovedì** (5)


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

Tipo di dati: **uint8**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**PROCESSO CIM \_**.**RunDay**", "**PROCESSO CIM \_**.**RunDayOfWeek**", "**Processo CIM \_**.**RunStartInterval**")
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

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**PROCESSO CIM \_**.**RunMonth**", "**PROCESSO CIM \_**.**RunDay**", "**PROCESSO CIM \_**.**RunDayOfWeek**", "**Processo CIM \_**.**RunStartInterval**")
</dt> </dl>

Intervallo di tempo dopo la mezzanotte in cui viene elaborato il processo. Ad esempio, "00000000020000.000000:000" indica che il processo deve essere eseguito in o dopo le due ore dell'ora locale o ora UTC (l'ora UTC è specificata con la **proprietà LocalOrUtcTime).**

</dd> <dt>

**ScheduledStartTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> <dt>

Qualificatori: [**deprecati**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**Processo CIM \_**.**RunMonth**", "**PROCESSO CIM \_**.**RunDay**", "**PROCESSO CIM \_**.**RunDayOfWeek**", "**Processo CIM \_**.**RunStartInterval**")
</dt> </dl>

> [!Note]  
> Questa proprietà è deprecata. È invece consigliabile usare le **proprietà RunMonth**, **RunDay**, **RunDayOfWeek** e **RunStartInterval.**

 

Ora pianificata per l'avvio del processo corrente. Questa ora può essere rappresentata da una data e un'ora o da un intervallo relativo all'ora in cui è richiesta la proprietà . Un valore di tutti gli zeri indica che il processo è già in esecuzione.

</dd> <dt>

**StartTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ora di avvio del processo. Questa ora può essere rappresentata da una data e un'ora o da un intervallo relativo all'ora in cui è richiesta la proprietà .

</dd> <dt>

**TimeSubmitted**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ora di invio del processo. Un valore di tutti gli zeri indica che l'elemento padre non è in grado di segnalare una data e un'ora.

</dd> <dt>

**UntilTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**PROCESSO CIM \_**.**LocalOrUtcTime**")
</dt> </dl>

Ora dopo la quale il processo diventa non valido o deve essere arrestato. L'ora può essere rappresentata da una data e da un'ora oppure da un intervallo relativo all'ora in cui è richiesta questa proprietà. Un valore di tutte le nove indica che il processo può essere eseguito per un periodo illimitato.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                                    |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                                          |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CIM \_ LogicalElement**](cim-logicalelement.md)
</dt> </dl>

 

