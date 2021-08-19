---
description: Versione concreta della classe Job \_ CIM. Questa classe rappresenta un'unità di lavoro generica di cui è possibile creare istanze da eseguire, ad esempio un batch o un processo di stampa.
ms.assetid: fad4d894-d1f5-428d-819f-74966dd9f410
title: CIM_ConcreteJob classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ConcreteJob
- CIM_ConcreteJob.InstanceID
- CIM_ConcreteJob.Name
- CIM_ConcreteJob.JobState
- CIM_ConcreteJob.TimeOfLastStateChange
- CIM_ConcreteJob.TimeBeforeRemoval
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a62ab2392ce2c069aa88ebb465f7028368f30bd5432cf96559c7eebe6edb8bdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117813162"
---
# <a name="cim_concretejob-class"></a>Classe CIM \_ ConcreteJob

Versione concreta della [**classe \_ Job CIM.**](cim-job.md) Questa classe rappresenta un'unità di lavoro generica di cui è possibile creare istanze da eseguire, ad esempio un batch o un processo di stampa.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_ConcreteJob : CIM_Job
{
  string   InstanceID;
  string   Name;
  uint16   JobState;
  datetime TimeOfLastStateChange;
  datetime TimeBeforeRemoval = "00000000000500.000000:000";
};
```

## <a name="members"></a>Members

La **classe \_ CIM ConcreteJob** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe \_ CIM ConcreteJob** include questi metodi.



| Metodo                                                           | Descrizione                                                                          |
|:-----------------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [**GetError**](cim-concretejob-geterror.md)                     | Recupera informazioni sull'errore per lo stato operativo di un processo concreto.<br/> |
| [**RequestStateChange**](cim-concretejob-requeststatechange.md) | Richiede la modifica dello stato specificato a un processo concreto.<br/>                    |



 

### <a name="properties"></a>Proprietà

La **classe CIM \_ ConcreteJob** ha queste proprietà.

<dl> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceID")
</dt> </dl>

Identifica in modo univoco e opaco un'istanza di questa classe all'interno dell'ambito dello spazio dei nomi contenitore.

> [!IMPORTANT]
>
> Per garantire l'univocità all'interno dello spazio dei nomi, il valore della proprietà **InstanceID** deve essere costruito nel modello seguente: *OrgID*:*LocalID*
>
> *OrgID* deve includere un nome protetto da copyright, registrato o altrimenti univoco di proprietà dell'entità aziendale che definisce **InstanceID** o essere un ID registrato assegnato da un'autorità globale riconosciuta. Questo modello è simile alla struttura dei nomi delle classi dello schema. Inoltre, per garantire l'univocità, i primi due punti in **InstanceID** devono essere compresi tra *OrgID* e *LocalID*. *L'ORGID non* deve pertanto contenere i due punti (':').
>
> *LocalID* viene scelto dall'entità business e non deve essere usato nuovamente per identificare diversi elementi reali sottostanti.
>
> Se il modello precedente non viene usato, l'entità di definizione deve garantire che il valore **InstanceID** risultante non sia usato di nuovo in tutte le proprietà **InstanceID** prodotte da questo provider o da altri provider per questo spazio dei nomi.
>
> Per le istanze definite da DmTF (Distributed Management Task Force), il modello deve essere usato con *OrgID* impostato su CIM.

 

</dd> <dt>

**JobState**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stato operativo del processo e transizione tra tali stati.

<dt>

<span id="New"></span><span id="new"></span><span id="NEW"></span>

<span id="New"></span><span id="new"></span><span id="NEW"></span>**Nuovo** (2)


</dt> <dd>

il processo non è mai stato avviato.

</dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Avvio** (3)


</dt> <dd>

Il processo viene spostata dallo stato "Nuovo", "Sospeso" o "Servizio" allo stato "In esecuzione".

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**In** esecuzione (4)


</dt> <dd>

Il processo è in esecuzione.

</dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Sospeso** (5)


</dt> <dd>

Il processo viene arrestato, ma può essere riavviato in modo trasparente.

</dd> <dt>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arresto in fase di** arresto (6)


</dt> <dd>

Il processo è in stato "Completato", "Terminato" o "Terminato".

</dd> <dt>

<span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>

<span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completato** (7)


</dt> <dd>

Il processo è stato completato normalmente.

</dd> <dt>

<span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>

<span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>**Terminato** (8)


</dt> <dd>

Il processo è stato arrestato da una richiesta di modifica dello stato "Terminate". Il processo e tutti i processi sottostanti vengono terminati e possono essere riavviati (specifici del processo) solo come nuovo processo.

</dd> <dt>

<span id="Killed"></span><span id="killed"></span><span id="KILLED"></span>

<span id="Killed"></span><span id="killed"></span><span id="KILLED"></span>**Killed** (9)


</dt> <dd>

Il processo è stato arrestato da una richiesta di modifica dello stato "Kill". È possibile che i processi sottostanti siano stati lasciati in esecuzione e che sia necessario eseguire la pulizia per liberare risorse.

</dd> <dt>

<span id="Exception"></span><span id="exception"></span><span id="EXCEPTION"></span>

<span id="Exception"></span><span id="exception"></span><span id="EXCEPTION"></span>**Eccezione** (10)


</dt> <dd>

Il processo si trova in uno stato anomalo che potrebbe essere indicativo di una condizione di errore. Lo stato effettivo potrebbe essere visualizzato anche se gli oggetti specifici del processo.

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Servizio** (11)


</dt> <dd>

Il processo si trova in uno stato specifico del fornitore che supporta l'individuazione o la risoluzione dei problemi o entrambi

</dd> <dt>

<span id="Query_Pending"></span><span id="query_pending"></span><span id="QUERY_PENDING"></span>

<span id="Query_Pending"></span><span id="query_pending"></span><span id="QUERY_PENDING"></span>**Query in sospeso** (12)


</dt> <dd>

In attesa che un client risolva una query.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DmTF Reserved** (13..32767)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**obbligatori,**](/windows/desktop/WmiSdk/standard-qualifiers) [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")
</dt> </dl>

Nome descrittivo dell'istanza. Inoltre, il nome descrittivo può essere usato come proprietà per una ricerca o una query.

> [!Note]  
> Il nome non deve essere univoco all'interno dello spazio dei nomi .

 

</dd> <dt>

**TimeBeforeRemoval**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> <dt>

Qualificatori: [ **obbligatorio**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Indica per quanto tempo viene mantenuto un processo completato. Il valore predefinito è "00000000000500.000000:000" (cinque minuti).

</dd> <dt>

**TimeOfLastStateChange**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Data o ora dell'ultima modifica dello stato del processo.

> [!Note]  
> Se lo stato del processo non è stato modificato e questa proprietà è popolata, deve essere impostata su un valore di intervallo pari a zero.

 

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                                    |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                                          |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Processo \_ CIM**](cim-job.md)
</dt> </dl>

 

