---
description: Rappresenta un evento generato ogni volta che la proprietà OperationalStatus della classe Msvm ResourcePool o \_ Msvm \_ LogicalDisk cambia.
ms.assetid: 20E7C22A-A151-4EDC-90D8-4BCD53C42355
title: Msvm_StorageAlert classe
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
ms.openlocfilehash: 41af5f29f54dc0b5c7e63203c43160539bcaa870
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886586"
---
# <a name="msvm_storagealert-class"></a>Classe Msvm \_ StorageAlert

Rappresenta un evento generato ogni volta che la **proprietà OperationalStatus** della [**classe Msvm \_ ResourcePool**](msvm-resourcepool.md) o [**Msvm \_ LogicalDisk**](msvm-logicaldisk.md) cambia.

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

La **classe Msvm \_ StorageAlert** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Msvm \_ StorageAlert** ha queste proprietà.

<dl> <dt>

**AlertingElementFormat**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **ModelCorrespondence** ("CIM \_ AlertIndication.AlertingManagedElement", "CIM \_ AlertIndication.OtherAlertingElementFormat")
</dt> </dl>

Specifica il formato della **proprietà AlertingManagedElement.** Il formato è CIMObjectPath, con il formato *&lt; NamespacePath &gt; : &lt; ClassName &gt; . &lt; Prop1 &gt; = \\ " &lt; Value1 &gt; \\ ", " &lt; Prop2 &gt; = \\ " &lt; Value2 &gt; \\ "*, che specifica un'istanza nello schema CIM.

Questa proprietà viene ereditata dalla **classe CIM \_ AlertIndication.**

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

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Percorsi WMI dell'istanza per cui viene generato l'avviso.

</dd> <dt>

**AlertType**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
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

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Data e ora in cui è stato rilevato l'evento sottostante.

</dd> <dt>

**Messaggio**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Messaggio formattato costruito combinando alcuni o tutti gli elementi dinamici specificati nella proprietà **MessageArguments** con gli elementi statici identificati in modo univoco dalla **proprietà MessageID** in un registro messaggi o in un altro catalogo associato alla **proprietà OwningEntity.**

</dd> <dt>

**Argomenti di messaggio**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Matrice contenente il contenuto dinamico del messaggio. Se il valore di **MessageID** è 32930, l'argomento nella posizione 0 è **il PoolID** dell'istanza [**di Msvm \_ ResourcePool**](msvm-resourcepoolcomponent.md) per cui viene generato l'avviso.

</dd> <dt>

**MessageID**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Identifica in modo univoco, nell'ambito **della proprietà OwningEntity,** il formato della **proprietà Message.** I valori possibili per questa proprietà sono:

32930 ("messaggio Archiviazione di velocità effettiva insufficiente del pool QoS")

</dd> <dt>

**OtherAlertingElementFormat**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringa che definisce i valori "Other" per **AlertingManagedElement.** Questo valore DEVE essere impostato su un valore non NULL quando **AlertingManagedElement** è impostato su un valore pari a 1 ("Altro"). Per tutti gli altri valori **di AlertingManagedElement,** il valore di questa stringa deve essere impostato su NULL.

Questa proprietà viene ereditata dalla **classe CIM \_ AlertIndication.**

</dd> <dt>

**ProprietàEntity**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Identifica in modo univoco l'entità proprietaria della definizione del formato del **messaggio** descritto in questa istanza. Il valore di questa proprietà è sempre "Microsoft-Windows- Hyper-V".

"Microsoft-Windows- Hyper-V"

</dd> <dt>

**PerceivedSeverity**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrive la gravità dell'indicazione di avviso. I valori possibili per questa proprietà sono:

<dl> <dt>

<span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>**Informazioni** (2)
</dt> <dt>

<span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>**Danneggiato/Avviso** (3)
</dt> </dl>

</dd> <dt>

**ProbableCause**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrive la causa probabile della situazione che ha causato l'indicazione di avviso.

<dl> <dt>

<span id="Storage_Capacity_Problem"></span><span id="storage_capacity_problem"></span><span id="STORAGE_CAPACITY_PROBLEM"></span>**Archiviazione problema di capacità** (50)
</dt> <dt>

<span id="Previous_Alert_Cleared"></span><span id="previous_alert_cleared"></span><span id="PREVIOUS_ALERT_CLEARED"></span>**Avviso precedente cancellato** (59)
</dt> </dl>

</dd> <dt>

**ProbableCauseDescription**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione testuale corrispondente al valore della **proprietà ProbableCause.**

</dd> </dl>

## <a name="remarks"></a>Commenti

Il provider WMI Hyper-V non genererà eventi per i singoli dischi virtuali per evitare di inondare i client di eventi in caso di malfunzionamenti su larga scala dei sistemi di archiviazione sottostanti.

Quando un client riceve un evento **Msvm \_ StorageAlert,** se il valore della proprietà **ProbableCause** è 50 ( Archiviazione Capacity Problem ), il client può individuare quali dischi virtuali operano al di fuori dei criteri QoS usando una delle procedure seguenti:

-   Eseguire una query [**su tutte le istanze di \_ Msvm LogicalDisk**](msvm-logicaldisk.md) allocate dal pool di risorse per cui è stato generato l'evento. Queste **istanze di Msvm \_ LogicalDisk** sono associate al pool di risorse tramite [**l'associazione Msvm \_ ElementAllocatedFromPool.**](msvm-elementallocatedfrompool.md)
-   Filtrare l'elenco dei risultati selezionando le istanze il cui OperationalStatus contiene Velocità effettiva insufficiente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8.1 solo app desktop\]<br/>                                                            |
| Server minimo supportato<br/> | Windows Server 2012 Solo app desktop R2 \[\]<br/>                                                 |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Avviso \_ CIMIndication**](cim-alertindication.md)
</dt> <dt>

[**Msvm \_ LogicalDisk**](msvm-logicaldisk.md)
</dt> <dt>

[**Msvm \_ ResourcePool**](msvm-resourcepoolcomponent.md)
</dt> </dl>

 

 




