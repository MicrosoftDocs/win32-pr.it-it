---
description: Descrive le funzionalità di un \_ oggetto METRICSERVICE CIM.
ms.assetid: 3b4da02f-5298-46d4-876c-404baca38c03
title: Classe CIM_MetricServiceCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricServiceCapabilities
- CIM_MetricServiceCapabilities.ControllableMetrics
- CIM_MetricServiceCapabilities.MetricsControlTypes
- CIM_MetricServiceCapabilities.ControllableManagedElements
- CIM_MetricServiceCapabilities.ManagedElementControlTypes
- CIM_MetricServiceCapabilities.SupportedMethods
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f878cb0e616cb710a33d350df866160fc0eebb83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313377"
---
# <a name="cim_metricservicecapabilities-class"></a>CIM \_ MetricServiceCapabilities (classe)

Descrive le funzionalità di un [**oggetto \_ MetricService CIM**](cim-metricservice.md) .

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Metrics::BaseMetrics"), AMENDMENT]
class CIM_MetricServiceCapabilities : CIM_EnabledLogicalElementCapabilities
{
  string ControllableMetrics[];
  uint16 MetricsControlTypes[];
  string ControllableManagedElements[];
  uint16 ManagedElementControlTypes[];
  uint16 SupportedMethods[];
};
```

## <a name="members"></a>Members

La classe **CIM \_ MetricServiceCapabilities** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **CIM \_ MetricServiceCapabilities** dispone di queste proprietà.

<dl> <dt>

**ControllableManagedElements**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ MetricServiceCapabilities**.**ManagedElementControlTypes**")
</dt> </dl>

Matrice che contiene gli identificatori delle istanze di [**CIM \_ gestite**](cim-managedelement.md) che sono controllate dal servizio metrico. Gli identificatori devono essere formattati come URI WBEM (Web-Based Enterprise Management). Per usare questa proprietà, il servizio metrico deve supportare l'abilitazione o la disabilitazione di almeno una metrica definita per l'istanza **CIM \_ gestitaelement** .

</dd> <dt>

**ControllableMetrics**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ MetricServiceCapabilities**.**MetricControlTypes**")
</dt> </dl>

Matrice contenente gli identificatori del [**\_ BaseMetricDefinition CIM**](cim-basemetricdefinition.md) che definisce le metriche gestite dal servizio metrico. Gli identificatori devono essere formattati come URI WBEM (Web-Based Enterprise Management).

Per usare questa proprietà, un'istanza di [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) deve essere associata a un'istanza [**CIM \_ MetricService**](cim-metricservice.md) tramite la classe [**CIM \_ ServiceAffectsElement**](cim-serviceaffectselement.md) . Il servizio metrico deve inoltre supportare l'abilitazione o la disabilitazione di almeno una metrica definita dall'istanza **CIM \_ BaseMetricDefinition** .

</dd> <dt>

**ManagedElementControlTypes**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ MetricServiceCapabilities**.**ControllableManagedElements**")
</dt> </dl>

Matrice che indica i tipi di controllo supportati dal servizio metrico per gli elementi gestiti nella matrice **ControllableManagedElements** . Questa matrice corrisponde alla matrice **ControllableManagedElements** . I tipi di controllo in questa matrice sono associati alle metriche tramite la matrice **ControllableManagedElements** .

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="Discrete"></span><span id="discrete"></span><span id="DISCRETE"></span>

**Discreto** (2)


</dt> <dd></dd> <dt>

<span id="Bulk"></span><span id="bulk"></span><span id="BULK"></span>

**Bulk** (3)


</dt> <dd></dd> <dt>

<span id="Both"></span><span id="both"></span><span id="BOTH"></span>

**Entrambi** (4)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF riservato** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

**Specifico del fornitore** (32768.. 65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**MetricsControlTypes**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ MetricServiceCapabilities**.**ControllableMetrics**")
</dt> </dl>

Matrice che indica i tipi di controllo supportati dal servizio metrico. Questa matrice corrisponde alla matrice **ControllableMetrics** . I tipi di controllo in questa matrice sono associati alle metriche tramite la matrice **ControllableMetrics** .

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="Discrete"></span><span id="discrete"></span><span id="DISCRETE"></span>

**Discreto** (2)


</dt> <dd></dd> <dt>

<span id="Bulk"></span><span id="bulk"></span><span id="BULK"></span>

**Bulk** (3)


</dt> <dd></dd> <dt>

<span id="Both"></span><span id="both"></span><span id="BOTH"></span>

**Entrambi** (4)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF riservato** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

**Specifico del fornitore** (32768.. 65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**SupportedMethods**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Matrice che contiene i nomi dei metodi supportati dal servizio metrico.

<dt>

<span id="ControlMetrics"></span><span id="controlmetrics"></span><span id="CONTROLMETRICS"></span>

**ControlMetrics** (2)


</dt> <dd></dd> <dt>

<span id="ControlMetricsByClass"></span><span id="controlmetricsbyclass"></span><span id="CONTROLMETRICSBYCLASS"></span>

**ControlMetricsByClass** (3)


</dt> <dd></dd> <dt>

<span id="ShowMetrics"></span><span id="showmetrics"></span><span id="SHOWMETRICS"></span>

**ShowMetrics** (4)


</dt> <dd></dd> <dt>

<span id="ShowMetricsByClass"></span><span id="showmetricsbyclass"></span><span id="SHOWMETRICSBYCLASS"></span>

**ShowMetricsByClass** (5)


</dt> <dd></dd> <dt>

<span id="GetMetricValues"></span><span id="getmetricvalues"></span><span id="GETMETRICVALUES"></span>

**GetMetricValues** (6)


</dt> <dd></dd> <dt>

<span id="ControlSampleTimes"></span><span id="controlsampletimes"></span><span id="CONTROLSAMPLETIMES"></span>

**ControlSampleTimes** (7)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF riservato** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

**Specifico del fornitore** (0x8000..)


</dt> <dd></dd> </dl>

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

[**\_ENABLEDLOGICALELEMENTCAPABILITIES CIM**](cim-enabledlogicalelementcapabilities.md)
</dt> </dl>

 

