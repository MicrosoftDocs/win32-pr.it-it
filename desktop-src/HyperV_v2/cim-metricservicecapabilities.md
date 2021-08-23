---
description: Descrive le funzionalità di un oggetto \_ CIM MetricService.
ms.assetid: 3b4da02f-5298-46d4-876c-404baca38c03
title: CIM_MetricServiceCapabilities classe
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
ms.openlocfilehash: c784fc9fac067c0cde07ad3e8911f9e09cd81b5cd3d7c76c16b1dd2407536838
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119694960"
---
# <a name="cim_metricservicecapabilities-class"></a>Classe CIM \_ MetricServiceCapabilities

Descrive le funzionalità di un [**oggetto \_ CIM MetricService.**](cim-metricservice.md)

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

La **classe CIM \_ MetricServiceCapabilities** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe CIM \_ MetricServiceCapabilities** ha queste proprietà.

<dl> <dt>

**ControllableManagedElements**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ MetricServiceCapabilities**.**ManagedElementControlTypes**")
</dt> </dl>

Matrice che contiene gli identificatori delle [**istanze \_ CiM ManagedElement**](cim-managedelement.md) controllate dal servizio metrica. Gli identificatori devono essere formattati come Web-Based ENTERPRISE Management (WBEM). Per usare questa proprietà, il servizio metrica deve supportare l'abilitazione o la disabilitazione di almeno una metrica definita per **l'istanza \_ CiM ManagedElement.**

</dd> <dt>

**Metrica controllabile**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ MetricServiceCapabilities**.**MetricControlTypes**")
</dt> </dl>

Matrice che contiene gli identificatori di [**\_ CiM BaseMetricDefinition**](cim-basemetricdefinition.md) che definisce le metriche gestite dal servizio metrica. Gli identificatori devono essere formattati come Web-Based ENTERPRISE Management (WBEM).

Per usare questa proprietà, è necessario associare un'istanza [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) a [**un'istanza di \_ CIM MetricService**](cim-metricservice.md) tramite la classe [**\_ CIM ServiceAffectsElement.**](cim-serviceaffectselement.md) Inoltre, il servizio metrica deve supportare l'abilitazione o la disabilitazione di almeno una metrica definita **dall'istanza \_ baseMetricDefinition di CIM.**

</dd> <dt>

**ManagedElementControlTypes**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ MetricServiceCapabilities**.**ControllableManagedElements**")
</dt> </dl>

Matrice che indica i tipi di controllo supportati dal servizio metrica per gli elementi gestiti nella matrice **ControllableManagedElements.** Questa matrice corrisponde alla **matrice ControllableManagedElements.** I tipi di controllo in questa matrice sono associati alle metriche tramite la **matrice ControllableManagedElements.**

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

**DmTF Reserved** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

**Specifico del** fornitore (32768..65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**Tipi di controllo delle metriche**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ MetricServiceCapabilities**.**ControllableMetrics**")
</dt> </dl>

Matrice che indica i tipi di controllo supportati dal servizio metrica. Questa matrice corrisponde alla **matrice ControllableMetrics.** I tipi di controllo in questa matrice sono associati alle metriche tramite la **matrice ControllableMetrics.**

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

**DmTF Reserved** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

**Specifico del** fornitore (32768..65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**Metodi supportati**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Matrice che contiene i nomi dei metodi supportati dal servizio metrica.

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

**DmTF Reserved** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

**Specifico del** fornitore (0x8000.)


</dt> <dd></dd> </dl>

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

[**CIM \_ EnabledLogicalElementCapabilities**](cim-enabledlogicalelementcapabilities.md)
</dt> </dl>

 

