---
description: Descrive le funzionalità dell'istanza msvm \_ MetricService associata.
ms.assetid: 4E24D675-8265-4B5E-9551-550510B138FE
title: Msvm_MetricServiceCapabilities classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricServiceCapabilities
- Msvm_MetricServiceCapabilities.InstanceID
- Msvm_MetricServiceCapabilities.Caption
- Msvm_MetricServiceCapabilities.Description
- Msvm_MetricServiceCapabilities.ElementName
- Msvm_MetricServiceCapabilities.ElementNameEditSupported
- Msvm_MetricServiceCapabilities.MaxElementNameLen
- Msvm_MetricServiceCapabilities.RequestedStatesSupported
- Msvm_MetricServiceCapabilities.ElementNameMask
- Msvm_MetricServiceCapabilities.ControllableMetrics
- Msvm_MetricServiceCapabilities.MetricsControlTypes
- Msvm_MetricServiceCapabilities.ControllableManagedElements
- Msvm_MetricServiceCapabilities.ManagedElementControlTypes
- Msvm_MetricServiceCapabilities.SupportedMethods
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 37fed3fead642ecfc5370d55c9f8b954477406b4b276cac392d9776a0cefb338
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119521331"
---
# <a name="msvm_metricservicecapabilities-class"></a>Classe Msvm \_ MetricServiceCapabilities

Descrive le funzionalità dell'istanza [**msvm \_ MetricService**](msvm-metricservice.md) associata.

La sintassi seguente è Managed Object Format codice MOF (Simplified Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MetricServiceCapabilities : CIM_MetricServiceCapabilities
{
  string  InstanceID;
  string  Caption = "Hyper-V Metric Service Capabilities";
  string  Description = "Defines Hyper-V Metric Service Capabilities";
  string  ElementName = "Hyper-V Metric Service Capabilities";
  boolean ElementNameEditSupported;
  unit16  MaxElementNameLen;
  unit16  RequestedStatesSupported[];
  string  ElementNameMask;
  string  ControllableMetrics[];
  uint16  MetricsControlTypes[];
  string  ControllableManagedElements[];
  uint16  ManagedElementControlTypes[];
  uint16  SupportedMethods[];
};
```

## <a name="members"></a>Members

La **classe Msvm \_ MetricServiceCapabilities** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Msvm \_ MetricServiceCapabilities** ha queste proprietà.

<dl> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Breve descrizione dell'oggetto. Questa proprietà viene ereditata da [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Hyper-V Metric Service Capabilities".

</dd> <dt>

**ControllableManagedElements**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **ArrayType** ("Indicizzato")
</dt> </dl>

Identifica le istanze di [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) che possono essere controllate **dall'istanza cim \_ MetricService** associata. Se questa proprietà è **Null,** è possibile controllare tutti gli elementi. Questa proprietà viene ereditata da **CIM \_ MetricServiceCapabilities.**

</dd> <dt>

**Metrica controllabile**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **ArrayType** ("Indicizzato")
</dt> </dl>

Identifica le istanze di **CIM \_ BaseMetricDefinition** che possono essere controllate **dall'istanza cim \_ MetricService** associata. Se questa proprietà è **Null,** è possibile controllare tutte le metriche. Questa proprietà viene ereditata da **CIM \_ MetricServiceCapabilities.**

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione dell'oggetto . Questa proprietà viene ereditata da [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Defines Hyper-V Metric Service Capabilities".

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome visualizzato per l'oggetto. Questa proprietà viene ereditata da [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Hyper-V Metric Service Capabilities".

</dd> <dt>

**ElementNameEditSupported**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la **proprietà ElementName** può essere modificata. Questa proprietà viene ereditata da **CIM \_ EnabledLogicalElementCapabilities.**

</dd> <dt>

**ElementNameMask**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica le restrizioni per **ElementName**, espresse come espressione regolare. Questa proprietà viene ereditata da **CIM \_ EnabledLogicalElementCapabilities.**

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **chiave**
</dt> </dl>

Identifica in modo univoco un'istanza di questa classe. Questa proprietà viene ereditata da [**CIM \_ ManagedElement.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**ManagedElementControlTypes**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **ArrayType** ("Indicizzato")
</dt> </dl>

Identifica il tipo di controllo supportato dall'istanza **cim \_ MetricService** associata per l'oggetto [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) identificato dal valore nello stesso indice di matrice nella proprietà **ControllableManagedElements.** Se questa proprietà è **Null,** sono supportati tutti i tipi di controllo. Questa proprietà viene ereditata da **CIM \_ MetricServiceCapabilities.**



| Valore                                                                                   | Significato                    |
|-----------------------------------------------------------------------------------------|----------------------------|
| <dl> <dt>0</dt> </dl>            | Sconosciuto<br/>         |
| <dl> <dt>2</dt> </dl>            | Discrete<br/>        |
| <dl> <dt>3</dt> </dl>            | In blocco<br/>            |
| <dl> <dt>4</dt> </dl>            | Entrambe<br/>            |
| <dl> <dt>5..32767</dt> </dl>     | DmTF riservato<br/>   |
| <dl> <dt>32768..65535</dt> </dl> | Specifico del fornitore<br/> |



 

</dd> <dt>

**MaxElementNameLen**
</dt> <dd> <dl> <dt>

Tipo di dati: **unit16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **MaxValue** (256)
</dt> </dl>

Specifica la lunghezza massima supportata della **proprietà ElementName.** Questa proprietà viene ereditata da **CIM \_ EnabledLogicalElementCapabilities.**

</dd> <dt>

**MetricsControlTypes**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **ArrayType** ("Indicizzato")
</dt> </dl>

Identifica il tipo di controllo supportato dall'istanza **cim \_ MetricService** associata per **CIM \_ BaseMetricDefinition** identificata dal valore nello stesso indice di matrice nella **proprietà ControllableMetrics.** Se questa proprietà è **Null,** sono supportati tutti i tipi di controllo. Questa proprietà viene ereditata da **CIM \_ MetricServiceCapabilities.**



| Valore                                                                                   | Significato                    |
|-----------------------------------------------------------------------------------------|----------------------------|
| <dl> <dt>0</dt> </dl>            | Sconosciuto<br/>         |
| <dl> <dt>2</dt> </dl>            | Discrete<br/>        |
| <dl> <dt>3</dt> </dl>            | In blocco<br/>            |
| <dl> <dt>4</dt> </dl>            | Entrambe<br/>            |
| <dl> <dt>5..32767</dt> </dl>     | DmTF riservato<br/>   |
| <dl> <dt>32768..65535</dt> </dl> | Specifico del fornitore<br/> |



 

</dd> <dt>

**RequestedStatesSupported**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice unit16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica i possibili stati che possono essere richiesti quando si usa il **metodo RequestStateChange** sull'elemento logico abilitato. Questa proprietà viene ereditata da **CIM \_ EnabledLogicalElementCapabilities.**



| Valore                                                                         | Significato              |
|-------------------------------------------------------------------------------|----------------------|
| <dl> <dt>2</dt> </dl>  | Attivato<br/>   |
| <dl> <dt>3</dt> </dl>  | Disattiva<br/>  |
| <dl> <dt>4</dt> </dl>  | Arresta<br/> |
| <dl> <dt>6</dt> </dl>  | Offline<br/>   |
| <dl> <dt>7</dt> </dl>  | Test<br/>      |
| <dl> <dt>8</dt> </dl>  | Rinviare<br/>     |
| <dl> <dt>9</dt> </dl>  | Disattivazione<br/>   |
| <dl> <dt>10</dt> </dl> | Riavvio<br/>    |
| <dl> <dt>11</dt> </dl> | Reset<br/>     |



 

</dd> <dt>

**Metodi supportati**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica i metodi supportati dal servizio metrica. Questa proprietà viene ereditata da **CIM \_ MetricServiceCapabilities.**



| Valore                                                                                   | Significato                                                                                         |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>2</dt> </dl>            | Il [**metodo ControlMetrics**](controlmetrics-msvm-metricservice.md) è supportato.<br/> |
| <dl> <dt>3</dt> </dl>            | Il **metodo ControlMetricsByClass** è supportato.<br/>                                   |
| <dl> <dt>4</dt> </dl>            | Il **metodo ShowMetrics** è supportato.<br/>                                             |
| <dl> <dt>5</dt> </dl>            | Il **metodo ShowMetricsByClass** è supportato.<br/>                                      |
| <dl> <dt>6</dt> </dl>            | Il **metodo GetMetricValues** è supportato.<br/>                                         |
| <dl> <dt>7</dt> </dl>            | Il **metodo ControlSampleTimes** è supportato.<br/>                                      |
| <dl> <dt>8..32767</dt> </dl>     | DmTF riservato<br/>                                                                        |
| <dl> <dt>32768..65535</dt> </dl> | Specifico del fornitore<br/>                                                                      |



 

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                              |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                    |
| Spazio dei nomi<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CIM \_ MetricServiceCapabilities**](cim-metricservicecapabilities.md)
</dt> <dt>

[**Msvm \_ MetricService**](msvm-metricservice.md)
</dt> </dl>

 

