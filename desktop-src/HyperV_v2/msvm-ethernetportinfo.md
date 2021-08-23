---
description: Associazione tra un'istanza della classe Msvm EthernetSwitchPort e un'istanza della \_ classe Msvm EthernetPortData che rappresenta i dati raccolti sulla porta da un'estensione \_ switch.
ms.assetid: 08677914-af09-47b7-9d4d-406696e1f504
title: Msvm_EthernetPortInfo classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetPortInfo
- Msvm_EthernetPortInfo.Antecedent
- Msvm_EthernetPortInfo.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3ef8f8f4ab7191400cfead94d20c4f601b97e48d46ee160d31c7b26b8e567b92
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119524891"
---
# <a name="msvm_ethernetportinfo-class"></a>Classe Msvm \_ EthernetPortInfo

Associazione tra un'istanza della [**classe Msvm \_ EthernetSwitchPort**](msvm-ethernetswitchport.md) e un'istanza della [**classe Msvm \_ EthernetPortData**](msvm-ethernetportdata.md) che rappresenta i dati raccolti sulla porta da un'estensione switch.

La sintassi seguente è Managed Object Format codice MOF (Simplified Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetPortInfo : CIM_Dependency
{
  Msvm_EthernetSwitchPort REF Antecedent;
  Msvm_EthernetPortData   REF Dependent;
};
```

## <a name="members"></a>Members

La **classe Msvm \_ EthernetPortInfo** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Msvm \_ EthernetPortInfo** ha queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **Msvm \_ EthernetSwitchPort**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ Dependency.Antecedent")
</dt> </dl>

Istanza della classe [**Msvm \_ EthernetSwitchPort**](msvm-ethernetswitchport.md) che rappresenta la porta del commutatore.

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **Msvm \_ EthernetPortData**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ Dependency.Dependent")
</dt> </dl>

Istanza della classe [**Msvm \_ EthernetPortData**](msvm-ethernetportdata.md) che rappresenta i dati della porta.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                              |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                    |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

