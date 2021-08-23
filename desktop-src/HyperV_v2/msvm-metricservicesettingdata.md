---
description: Rappresenta le impostazioni per il servizio metrica. Le proprietà per questa classe non possono essere modificate direttamente. Il client deve chiamare il metodo ModifyServiceSettings per modificare una di queste proprietà.
ms.assetid: 578ddda7-4c8e-498e-8612-29c392390b73
title: Msvm_MetricServiceSettingData classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricServiceSettingData
- Msvm_MetricServiceSettingData.InstanceID
- Msvm_MetricServiceSettingData.Caption
- Msvm_MetricServiceSettingData.Description
- Msvm_MetricServiceSettingData.ElementName
- Msvm_MetricServiceSettingData.MetricsFlushInterval
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ff0c8b9e4212624f4643efb7f7ef67ea4bc72f9488caa1b43d6260c9949011ac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119521321"
---
# <a name="msvm_metricservicesettingdata-class"></a>Classe Msvm \_ MetricServiceSettingData

Rappresenta le impostazioni per il servizio metrica. Le proprietà per questa classe non possono essere modificate direttamente. Il client deve chiamare il [**metodo ModifyServiceSettings**](modifyservicesettings-msvm-metricservice.md) per modificare una di queste proprietà.

La sintassi seguente è Managed Object Format codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MetricServiceSettingData : CIM_SettingData
{
  string   InstanceID;
  string   Caption = "Hyper-V Metric Service Settings";
  string   Description = "Defines Hyper-V Metric Service Settings";
  string   ElementName = "Hyper-V Metric Service Settings";
  datetime MetricsFlushInterval;
};
```

## <a name="members"></a>Members

La **classe Msvm \_ MetricServiceSettingData** include questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Msvm \_ MetricServiceSettingData** ha queste proprietà.

<dl> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Breve descrizione dell'oggetto. Questa proprietà viene ereditata da [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Hyper-V Metric Service Impostazioni".

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione dell'oggetto . Questa proprietà viene ereditata da [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Defines Hyper-V Metric Service Impostazioni".

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome visualizzato per l'oggetto . Questa proprietà viene ereditata da [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Hyper-V Metric Service Impostazioni".

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **Chiave**
</dt> </dl>

Identifica in modo univoco un'istanza di questa classe. Questa proprietà viene ereditata da [**CIM \_ SettingData.**](/previous-versions//cc136911(v=vs.85))

</dd> <dt>

**MetricsFlushInterval**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Definisce l'intervallo in base al quale le metriche devono essere scaricate su disco.

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

[**CIM \_ SettingData**](cim-settingdata.md)
</dt> <dt>

[**ModifyServiceSettings**](modifyservicesettings-msvm-metricservice.md)
</dt> </dl>

 

