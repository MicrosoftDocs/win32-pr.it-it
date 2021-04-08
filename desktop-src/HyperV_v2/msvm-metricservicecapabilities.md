---
description: Descrive le funzionalità dell'istanza MetricService di MSVM associata \_ .
ms.assetid: 4E24D675-8265-4B5E-9551-550510B138FE
title: Classe Msvm_MetricServiceCapabilities
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
ms.openlocfilehash: 635e153d3184e74ea581a045e3d6d54a5fea199f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885145"
---
# <a name="msvm_metricservicecapabilities-class"></a>\_Classe MSVM MetricServiceCapabilities

Descrive le funzionalità dell'istanza [**\_ MetricService di MSVM**](msvm-metricservice.md) associata.

La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.

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

La **classe \_ MetricServiceCapabilities di MSVM** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ MetricServiceCapabilities di MSVM** dispone di queste proprietà.

<dl> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Breve descrizione dell'oggetto. Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "funzionalità del servizio metrica Hyper-V".

</dd> <dt>

**ControllableManagedElements**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **arrayType** ("indicizzato")
</dt> </dl>

Identifica le istanze di [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) che possono essere controllate dall'istanza **\_ MetricService CIM** associata. Se questa proprietà è **null**, è possibile controllare tutti gli elementi. Questa proprietà viene ereditata da **CIM \_ MetricServiceCapabilities**.

</dd> <dt>

**ControllableMetrics**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **arrayType** ("indicizzato")
</dt> </dl>

Identifica le istanze di **\_ BaseMetricDefinition CIM** che possono essere controllate dall'istanza **\_ MetricService CIM** associata. Se questa proprietà è **null**, è possibile controllare tutte le metriche. Questa proprietà viene ereditata da **CIM \_ MetricServiceCapabilities**.

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione dell'oggetto . Questa proprietà viene ereditata da [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "definisce le funzionalità del servizio metrica Hyper-V".

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome visualizzato per l'oggetto. Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "funzionalità del servizio metrica Hyper-V".

</dd> <dt>

**ElementNameEditSupported**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la proprietà **ElementName** può essere modificata. Questa proprietà viene ereditata da **CIM \_ EnabledLogicalElementCapabilities**.

</dd> <dt>

**ElementNameMask**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica le restrizioni per **ElementName**, espresse come espressione regolare. Questa proprietà viene ereditata da **CIM \_ EnabledLogicalElementCapabilities**.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **chiave**
</dt> </dl>

Identifica in modo univoco un'istanza di questa classe. Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**ManagedElementControlTypes**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **arrayType** ("indicizzato")
</dt> </dl>

Identifica il tipo di controllo supportato dall'istanza del **\_ MetricService CIM** associata per l'oggetto [**CIM \_ gestitoelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) identificato dal valore in corrispondenza dello stesso indice di matrice nella proprietà **ControllableManagedElements** . Se questa proprietà è **null**, sono supportati tutti i tipi di controllo. Questa proprietà viene ereditata da **CIM \_ MetricServiceCapabilities**.



| Valore                                                                                   | Significato                    |
|-----------------------------------------------------------------------------------------|----------------------------|
| <dl> <dt>0</dt> </dl>            | Sconosciuto<br/>         |
| <dl> <dt>2</dt> </dl>            | Discrete<br/>        |
| <dl> <dt>3</dt> </dl>            | In blocco<br/>            |
| <dl> <dt>4</dt> </dl>            | Entrambi<br/>            |
| <dl> <dt>5.. 32767</dt> </dl>     | DMTF riservato<br/>   |
| <dl> <dt>32768.. 65535</dt> </dl> | Specifico del fornitore<br/> |



 

</dd> <dt>

**MaxElementNameLen**
</dt> <dd> <dl> <dt>

Tipo di dati: **unit16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **MaxValue** (256)
</dt> </dl>

Specifica la lunghezza massima supportata della proprietà **ElementName** . Questa proprietà viene ereditata da **CIM \_ EnabledLogicalElementCapabilities**.

</dd> <dt>

**MetricsControlTypes**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **arrayType** ("indicizzato")
</dt> </dl>

Identifica il tipo di controllo supportato dall'istanza **\_ MetricService CIM** associata per il **\_ BaseMetricDefinition CIM** identificato dal valore in corrispondenza dello stesso indice di matrice nella proprietà **ControllableMetrics** . Se questa proprietà è **null**, sono supportati tutti i tipi di controllo. Questa proprietà viene ereditata da **CIM \_ MetricServiceCapabilities**.



| Valore                                                                                   | Significato                    |
|-----------------------------------------------------------------------------------------|----------------------------|
| <dl> <dt>0</dt> </dl>            | Sconosciuto<br/>         |
| <dl> <dt>2</dt> </dl>            | Discrete<br/>        |
| <dl> <dt>3</dt> </dl>            | In blocco<br/>            |
| <dl> <dt>4</dt> </dl>            | Entrambi<br/>            |
| <dl> <dt>5.. 32767</dt> </dl>     | DMTF riservato<br/>   |
| <dl> <dt>32768.. 65535</dt> </dl> | Specifico del fornitore<br/> |



 

</dd> <dt>

**RequestedStatesSupported**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **unit16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica gli stati possibili che è possibile richiedere quando si utilizza il metodo **RequestStateChange** sull'elemento logico Enabled. Questa proprietà viene ereditata da **CIM \_ EnabledLogicalElementCapabilities**.



| Valore                                                                         | Significato              |
|-------------------------------------------------------------------------------|----------------------|
| <dl> <dt>2</dt> </dl>  | Abilitato<br/>   |
| <dl> <dt>3</dt> </dl>  | Disabilita<br/>  |
| <dl> <dt>4</dt> </dl>  | Arresta<br/> |
| <dl> <dt>6</dt> </dl>  | Offline<br/>   |
| <dl> <dt>7</dt> </dl>  | Test<br/>      |
| <dl> <dt>8</dt> </dl>  | Rinviare<br/>     |
| <dl> <dt>9</dt> </dl>  | Disattivazione<br/>   |
| <dl> <dt>10</dt> </dl> | Riavvio<br/>    |
| <dl> <dt>11</dt> </dl> | Reset<br/>     |



 

</dd> <dt>

**SupportedMethods**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica i metodi supportati dal servizio metrico. Questa proprietà viene ereditata da **CIM \_ MetricServiceCapabilities**.



| Valore                                                                                   | Significato                                                                                         |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>2</dt> </dl>            | Il metodo [**ControlMetrics**](controlmetrics-msvm-metricservice.md) è supportato.<br/> |
| <dl> <dt>3</dt> </dl>            | Il metodo **ControlMetricsByClass** è supportato.<br/>                                   |
| <dl> <dt>4</dt> </dl>            | Il metodo **ShowMetrics** è supportato.<br/>                                             |
| <dl> <dt>5</dt> </dl>            | Il metodo **ShowMetricsByClass** è supportato.<br/>                                      |
| <dl> <dt>6</dt> </dl>            | Il metodo **GetMetricValues** è supportato.<br/>                                         |
| <dl> <dt>7</dt> </dl>            | Il metodo **ControlSampleTimes** è supportato.<br/>                                      |
| <dl> <dt>8.. 32767</dt> </dl>     | DMTF riservato<br/>                                                                        |
| <dl> <dt>32768.. 65535</dt> </dl> | Specifico del fornitore<br/>                                                                      |



 

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                                    |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_METRICSERVICECAPABILITIES CIM**](cim-metricservicecapabilities.md)
</dt> <dt>

[**\_MetricService MSVM**](msvm-metricservice.md)
</dt> </dl>

 

