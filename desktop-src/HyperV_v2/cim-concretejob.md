---
description: Versione concreta della classe di \_ processi CIM. Questa classe rappresenta un'unità di lavoro istanziabile generica da eseguire, ad esempio un batch o un processo di stampa.
ms.assetid: fad4d894-d1f5-428d-819f-74966dd9f410
title: Classe CIM_ConcreteJob
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
ms.openlocfilehash: 949d7c85643919f784a82e7722c9d49a9d9d2e97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308366"
---
# <a name="cim_concretejob-class"></a>CIM \_ ConcreteJob (classe)

Versione concreta della classe [**di \_ processi CIM**](cim-job.md) . Questa classe rappresenta un'unità di lavoro istanziabile generica da eseguire, ad esempio un batch o un processo di stampa.

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

La classe **CIM \_ ConcreteJob** presenta questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La classe **CIM \_ ConcreteJob** presenta questi metodi.



| Metodo                                                           | Descrizione                                                                          |
|:-----------------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [**GetError**](cim-concretejob-geterror.md)                     | Recupera le informazioni sull'errore per lo stato operativo di un processo concreto.<br/> |
| [**RequestStateChange**](cim-concretejob-requeststatechange.md) | Richiede la modifica dello stato specificato in un processo concreto.<br/>                    |



 

### <a name="properties"></a>Proprietà

La classe **CIM \_ ConcreteJob** dispone di queste proprietà.

<dl> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceId")
</dt> </dl>

Identifica in modo univoco e opaco un'istanza di questa classe nell'ambito dello spazio dei nomi che lo contiene.

> [!IMPORTANT]
>
> Per garantire l'univocità all'interno dello spazio dei nomi, il valore della proprietà **InstanceID** deve essere costruito nel modello seguente: *OrgID*:*LocalId*
>
> *OrgID* deve includere un nome con copyright, marchio o in altro modo univoco, di proprietà dell'entità di business che definisce **InstanceID**, oppure essere un ID registrato assegnato da un'autorità globale riconosciuta. Questo modello è simile alla struttura dei nomi delle classi dello schema. Inoltre, per garantire l'univocità, i primi due punti in **InstanceID** devono essere compresi tra *OrgID* e *LocalId*. Pertanto *OrgID* non deve contenere i due punti (':').
>
> Il *localizzato* viene scelto dall'entità di business e non deve essere riutilizzato per identificare diversi elementi reali sottostanti.
>
> Se il criterio precedente non viene utilizzato, l'entità di definizione deve assicurare che il valore **InstanceID** risultante non venga riutilizzato nelle proprietà **InstanceID** generate dal provider o da altri provider per questo spazio dei nomi.
>
> Per le istanze definite DMTF (Distributed Management Task Force), il modello deve essere usato con *OrgID* impostato su CIM.

 

</dd> <dt>

**JobState**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Lo stato operativo del processo e la transizione tra questi Stati.

<dt>

<span id="New"></span><span id="new"></span><span id="NEW"></span>

<span id="New"></span><span id="new"></span><span id="NEW"></span>**Nuovo** (2)


</dt> <dd>

il processo non è mai stato avviato.

</dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Avvio** (3)


</dt> <dd>

Il processo viene spostato dagli Stati ' New ',' suspended ' o ' Service ' nello stato ' running '.

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**In esecuzione** (4)


</dt> <dd>

Il processo è in esecuzione.

</dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Sospeso** (5)


</dt> <dd>

Il processo è stato interrotto, ma può essere riavviato in modo uniforme.

</dd> <dt>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arresto** in corso (6)


</dt> <dd>

Lo stato del processo è' completed ',' terminate ' o ' Killed '.

</dd> <dt>

<span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>

<span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completato** (7)


</dt> <dd>

Il processo è stato completato normalmente.

</dd> <dt>

<span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>

<span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>**Terminata** (8)


</dt> <dd>

Il processo è stato interrotto da una richiesta di modifica dello stato ' terminate '. Il processo e tutti i processi sottostanti sono terminati e possono essere riavviati (specifici del processo) solo come nuovo processo.

</dd> <dt>

<span id="Killed"></span><span id="killed"></span><span id="KILLED"></span>

<span id="Killed"></span><span id="killed"></span><span id="KILLED"></span>**Terminata (9** )


</dt> <dd>

Il processo è stato interrotto da una richiesta di modifica dello stato ' Kill '. I processi sottostanti potrebbero essere stati lasciati in esecuzione e la pulizia potrebbe essere necessaria per liberare risorse.

</dd> <dt>

<span id="Exception"></span><span id="exception"></span><span id="EXCEPTION"></span>

<span id="Exception"></span><span id="exception"></span><span id="EXCEPTION"></span>**Eccezione** (10)


</dt> <dd>

Il processo è in uno stato anomalo che potrebbe essere indicativo di una condizione di errore. Lo stato effettivo potrebbe essere visualizzato anche se gli oggetti specifici del processo.

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Servizio** (11)


</dt> <dd>

Il processo è in uno stato specifico del fornitore che supporta l'individuazione o la risoluzione dei problemi o entrambi

</dd> <dt>

<span id="Query_Pending"></span><span id="query_pending"></span><span id="QUERY_PENDING"></span>

<span id="Query_Pending"></span><span id="query_pending"></span><span id="QUERY_PENDING"></span>**Query in sospeso** (12)


</dt> <dd>

In attesa della risoluzione di una query da un client.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (13.. 32767)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornitore riservato** (32768.. 65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**obbligatorio**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")
</dt> </dl>

Nome descrittivo dell'istanza. Inoltre, è possibile utilizzare il nome descrittivo come proprietà per una ricerca o una query.

> [!Note]  
> Non è necessario che il nome sia univoco all'interno dello spazio dei nomi.

 

</dd> <dt>

**TimeBeforeRemoval**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [ **obbligatorio**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Indica per quanto tempo viene mantenuto un processo completato. Il valore predefinito è "00000000000500.000000:000" (cinque minuti).

</dd> <dt>

**TimeOfLastStateChange**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Data o ora dell'Ultima modifica apportata allo stato del processo.

> [!Note]  
> Se lo stato del processo non è stato modificato e questa proprietà è popolata, deve essere impostata su un valore di intervallo zero.

 

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

[**\_Processo CIM**](cim-job.md)
</dt> </dl>

 

