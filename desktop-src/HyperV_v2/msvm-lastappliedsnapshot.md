---
description: Rappresenta un'associazione tra un sistema virtuale e i dati di impostazione dello snapshot applicato più di recente al sistema virtuale.
ms.assetid: 9231b441-20c4-468b-905f-5baabc32a8cc
title: Msvm_LastAppliedSnapshot classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_LastAppliedSnapshot
- Msvm_LastAppliedSnapshot.Antecedent
- Msvm_LastAppliedSnapshot.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e34260e0bfe77b847437e9b3d49794334b3897d8425981fecb2032098e24fa7a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119521921"
---
# <a name="msvm_lastappliedsnapshot-class"></a>Classe Msvm \_ LastAppliedSnapshot

Rappresenta un'associazione tra un sistema virtuale e i dati di impostazione dello snapshot applicato più di recente al sistema virtuale.

La sintassi seguente è Managed Object Format codice MOF (Simplified Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_LastAppliedSnapshot : CIM_LastAppliedSnapshot
{
  CIM_VirtualSystemSettingData REF Antecedent;
  CIM_ComputerSystem           REF Dependent;
};
```

## <a name="members"></a>Members

La **classe Msvm \_ LastAppliedSnapshot** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Msvm \_ LastAppliedSnapshot** ha queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ VirtualSystemSettingData**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **Override**, **Min** ( 0 ), **Max** ( 1 )
</dt> </dl>

Riferimento a un'istanza della [**classe Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) che rappresenta lo snapshot del sistema virtuale applicato per ultimo al sistema virtuale. Questa proprietà viene ereditata dalla **dipendenza CIM. \_**

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ ComputerSystem**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **Override**, **Min** ( 0 ), **Max** ( 1 )
</dt> </dl>

Riferimento a un'istanza della [**classe Msvm \_ ComputerSystem**](msvm-computersystem.md) che rappresenta il sistema virtuale su cui è stato applicato più di recente lo snapshot del sistema virtuale rappresentato dalla proprietà **Antecedent.** Questa proprietà viene ereditata dalla **dipendenza CIM. \_**

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                              |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                    |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

 




