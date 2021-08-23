---
description: Definisce l'associazione tra Msvm \_ BaseMetricDefinition e un elemento CIM \_ ManagedElement per definire le metriche per quest'ultimo. La definizione delle metriche viene data dal contesto da ManagedElement, motivo per cui la definizione dipende dall'elemento.
ms.assetid: 528d9b1a-089d-48ae-b5a6-40bc9d09191c
title: Msvm_MetricDefForME classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricDefForME
- Msvm_MetricDefForME.Antecedent
- Msvm_MetricDefForME.Dependent
- Msvm_MetricDefForME.MetricCollectionEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6c6da093c5f902657c51285e124593e0bf44a9be0bf32ed87a55d3349cbfba92
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119521601"
---
# <a name="msvm_metricdefforme-class"></a>Classe Msvm \_ MetricDefForME

Definisce l'associazione tra [**msvm \_ BaseMetricDefinition**](msvm-basemetricdefinition.md) e [**cim \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) per definire le metriche per quest'ultimo. La definizione delle metriche viene data dal contesto da ManagedElement, motivo per cui la definizione dipende dall'elemento.

La sintassi seguente è Managed Object Format codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MetricDefForME : CIM_MetricDefForME
{
  CIM_ManagedElement       REF Antecedent;
  CIM_BaseMetricDefinition REF Dependent;
  uint16                       MetricCollectionEnabled = 2;
};
```

## <a name="members"></a>Members

La **classe Msvm \_ MetricDefForME** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Msvm \_ MetricDefForME** ha queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Riferimento a un'istanza della [**classe CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) che rappresenta l'elemento gestito a cui possono essere applicate metriche del tipo definite da **Dependent.** Questa proprietà viene ereditata dalla [**dipendenza CIM. \_**](/windows/desktop/CIMWin32Prov/cim-dependency)

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Riferimento a un'istanza della [**classe \_ CIM BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) che rappresenta la definizione della metrica che **l'antecedente** può avere applicato. Questa proprietà viene ereditata dalla [**dipendenza CIM. \_**](/windows/desktop/CIMWin32Prov/cim-dependency)

</dd> <dt>

**MetricCollectionEnabled**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la metrica definita da **Dependent** viene raccolta per **antecedente.** Questo sarà uno dei valori seguenti.



| Valore                                                                                                                                                                                                                                                               | Significato                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <dt>**Abilitato**</dt> <dt>2</dt> </dl>                                         | La metrica viene raccolta.<br/>                                |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <dt>**Disabilitato**</dt> <dt>3</dt> </dl>                                     | La metrica non viene raccolta.<br/>                            |
| <span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span><dl> <dt>**Riservato**</dt> <dt>4</dt> </dl>                                     |                                                                          |
| <span id="PartiallyEnabled"></span><span id="partiallyenabled"></span><span id="PARTIALLYENABLED"></span><dl> <dt>**PartiallyEnabled**</dt> <dt>32768</dt> </dl> | La metrica viene raccolta per alcuni dispositivi, ma non per tutti.<br/> |



 

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                              |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                    |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

