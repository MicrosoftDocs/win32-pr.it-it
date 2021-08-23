---
description: Rappresenta un'associazione di oggetti valore della metrica con le relative definizioni di metrica.
ms.assetid: 98ad9390-78b4-4c18-b068-d05efa2f1866
title: Msvm_MetricInstance classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricInstance
- Msvm_MetricInstance.Antecedent
- Msvm_MetricInstance.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 18a15ff6479caa690a8645e89d9b68f4a15f523bd7cee56fedb6957e20373214
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119521541"
---
# <a name="msvm_metricinstance-class"></a>Classe \_ Msvm MetricInstance

Rappresenta un'associazione di oggetti valore della metrica con le relative definizioni di metrica. Questa associazione consente di aggiungere un'istanza di [**Msvm \_ BaseMetricValue**](msvm-basemetricvalue.md) al relativo [**oggetto \_ BaseMetricDefinition msvm.**](msvm-basemetricdefinition.md)

La sintassi seguente è Managed Object Format codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MetricInstance : CIM_MetricInstance
{
  CIM_ManagedElement REF Antecedent;
  CIM_ManagedElement REF Dependent;
};
```

## <a name="members"></a>Members

La **classe Msvm \_ MetricInstance** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Msvm \_ MetricInstance** ha queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: ****CIM \_ ManagedElement****
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **Chiave**
</dt> </dl>

Riferimento a un'istanza della classe [**Msvm \_ BaseMetricDefinition**](msvm-basemetricdefinition.md) che rappresenta le definizioni delle metriche.

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: ****CIM \_ ManagedElement****
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **Chiave**
</dt> </dl>

Riferimento a un'istanza della [**classe \_ BaseMetricValue msvm**](msvm-basemetricvalue.md) che rappresenta le metriche dipendenti dall'oggetto **precedente.**

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                              |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                    |
| Spazio dei nomi<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

 




