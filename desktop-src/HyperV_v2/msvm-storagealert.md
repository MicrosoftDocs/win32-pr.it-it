---
description: Rappresenta un evento generato ogni volta che viene modificata la proprietà OperationalStatus della \_ classe MSVM ResourcePool o MSVM \_ disco logico.
ms.assetid: 20E7C22A-A151-4EDC-90D8-4BCD53C42355
title: Classe Msvm_StorageAlert
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StorageAlert
- Msvm_StorageAlert.AlertingManagedElement
- Msvm_StorageAlert.AlertingElementFormat
- Msvm_StorageAlert.OtherAlertingElementFormat
- Msvm_StorageAlert.AlertType
- Msvm_StorageAlert.PerceivedSeverity
- Msvm_StorageAlert.ProbableCause
- Msvm_StorageAlert.ProbableCauseDescription
- Msvm_StorageAlert.EventTime
- Msvm_StorageAlert.OwningEntity
- Msvm_StorageAlert.MessageArguments
- Msvm_StorageAlert.MessageID
- Msvm_StorageAlert.Message
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: fa7f0430631082a9690cf2083f6b075ca62ee26b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104057820"
---
# <a name="msvm_storagealert-class"></a>\_Classe MSVM StorageAlert

Rappresenta un evento generato ogni volta che viene modificata la proprietà **OperationalStatus** della classe [**MSVM \_ ResourcePool**](msvm-resourcepool.md) o [**MSVM \_ disco logico**](msvm-logicaldisk.md) .

La sintassi seguente è semplificata dal codice MOF e include queste proprietà.

## <a name="syntax"></a>Sintassi

``` syntax
[Indication, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_StorageAlert : CIM_AlertIndication
{
  string   AlertingManagedElement[];
  uint16   AlertingElementFormat;
  uint16   OtherAlertingElementFormat;
  uint16   AlertType;
  uint16   PerceivedSeverity;
  uint16   ProbableCause;
  string   ProbableCauseDescription;
  datetime EventTime;
  string   OwningEntity;
  string   MessageArguments[];
  string   MessageID;
  string   Message;
};
```

## <a name="members"></a>Members

La **classe \_ StorageAlert di MSVM** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ StorageAlert di MSVM** dispone di queste proprietà.

<dl> <dt>

**AlertingElementFormat**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **ModelCorrespondence** ("CIM \_ AlertIndication. AlertingManagedElement", "CIM \_ AlertIndication. OtherAlertingElementFormat")
</dt> </dl>

Specifica il formato della proprietà **AlertingManagedElement** . Il formato è CIMObjectPath, con formato *<NamespacePath> : <ClassName> . <Prop1> = \\ " <Value1> \\ ", " <Prop2> = \\ " <Value2> \\ "*, che specifica un'istanza nello schema CIM.

Questa proprietà viene ereditata dalla classe **CIM \_ AlertIndication** .

I valori possibili sono:

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)
</dt> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)
</dt> <dt>

<span id="CIMObjectPath"></span><span id="cimobjectpath"></span><span id="CIMOBJECTPATH"></span>**CIMObjectPath** (2)
</dt> </dl>

</dd> <dt>

**AlertingManagedElement**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Percorsi WMI dell'istanza per la quale viene generato l'avviso.

</dd> <dt>

**AlertType**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica la classificazione primaria dell'avviso. I valori possibili per questa proprietà sono:

<dl> <dt>

<span id="Quality_of_Service_Alert"></span><span id="quality_of_service_alert"></span><span id="QUALITY_OF_SERVICE_ALERT"></span>**Avviso di qualità del servizio** (3)
</dt> </dl>

</dd> <dt>

**EventTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Data e ora in cui è stato rilevato l'evento sottostante.

</dd> <dt>

**Messaggio**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Messaggio formattato costruito combinando alcuni o tutti gli elementi dinamici specificati nella proprietà **MessageArguments** con gli elementi statici identificati in modo univoco dalla proprietà **MessageID** in un registro messaggi o in un altro catalogo associato alla proprietà **OwningEntity** .

</dd> <dt>

**MessageArguments**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Matrice che contiene il contenuto dinamico del messaggio. Se il valore di **MessageID** è 32930, l'argomento nella posizione 0 è il **PoolID** dell'istanza di [**MSVM \_ ResourcePool**](msvm-resourcepoolcomponent.md) per la quale viene generato l'avviso.

</dd> <dt>

**MessageID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Identifica in modo univoco, all'interno dell'ambito della proprietà **OwningEntity** , il formato della proprietà del **messaggio** . I valori possibili per questa proprietà sono:

32930 ("messaggio di velocità effettiva di QoS insufficiente nel pool di archiviazione")

</dd> <dt>

**OtherAlertingElementFormat**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringa che definisce i valori "other" per **AlertingManagedElement**. Questo valore deve essere impostato su un valore non NULL quando **AlertingManagedElement** è impostato su un valore pari a 1 ("altro"). Per tutti gli altri valori di **AlertingManagedElement**, il valore di questa stringa deve essere impostato su null.

Questa proprietà viene ereditata dalla classe **CIM \_ AlertIndication** .

</dd> <dt>

**OwningEntity**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Identifica in modo univoco l'entità a cui appartiene la definizione del formato del **messaggio** descritto in questa istanza. Il valore di questa proprietà è sempre "Microsoft-Windows-Hyper-V".

"Microsoft-Windows-Hyper-V"

</dd> <dt>

**PerceivedSeverity**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrive il livello di gravità dell'indicazione di avviso. I valori possibili per questa proprietà sono:

<dl> <dt>

<span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>**Informazioni** (2)
</dt> <dt>

<span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>**Danneggiato/avviso** (3)
</dt> </dl>

</dd> <dt>

**ProbableCause**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrive la causa probabile della situazione che ha generato l'indicazione di avviso.

<dl> <dt>

<span id="Storage_Capacity_Problem"></span><span id="storage_capacity_problem"></span><span id="STORAGE_CAPACITY_PROBLEM"></span>**Problema di capacità di archiviazione** (50)
</dt> <dt>

<span id="Previous_Alert_Cleared"></span><span id="previous_alert_cleared"></span><span id="PREVIOUS_ALERT_CLEARED"></span>**Avviso precedente cancellato** (59)
</dt> </dl>

</dd> <dt>

**ProbableCauseDescription**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione testuale che corrisponde al valore della proprietà **ProbableCause** .

</dd> </dl>

## <a name="remarks"></a>Commenti

Il provider WMI Hyper-V non genera eventi per i singoli dischi virtuali, in modo da evitare che i client vengano sovraccaricati con eventi in caso di malfunzionamenti su larga scala dei sistemi di archiviazione sottostanti.

Quando un client riceve un evento **MSVM \_ StorageAlert** , se il valore della proprietà **ProbableCause** è 50 (problema di capacità di archiviazione), il client può individuare i dischi virtuali che operano al di fuori dei criteri QoS usando una di queste procedure:

-   Eseguire una query su tutte le istanze di [**\_ disco logico MSVM**](msvm-logicaldisk.md) allocate dal pool di risorse per il quale è stato generato l'evento. Queste **istanze \_ disco logico di MSVM** sono associate al pool di risorse tramite l'associazione [**MSVM \_ ElementAllocatedFromPool**](msvm-elementallocatedfrompool.md) .
-   Filtrare l'elenco dei risultati selezionando le istanze il cui OperationalStatus contiene una velocità effettiva insufficiente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1 \[ solo app desktop\]<br/>                                                            |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2012 R2 \[\]<br/>                                                 |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_ALERTINDICATION CIM**](cim-alertindication.md)
</dt> <dt>

[**\_Disco logico MSVM**](msvm-logicaldisk.md)
</dt> <dt>

[**\_ResourcePool MSVM**](msvm-resourcepoolcomponent.md)
</dt> </dl>

 

 




