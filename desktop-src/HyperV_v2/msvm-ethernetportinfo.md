---
description: Associazione tra un'istanza della \_ classe MSVM EthernetSwitchPort e un'istanza della \_ classe MSVM EthernetPortData che rappresenta i dati raccolti sulla porta da un'estensione del commutire.
ms.assetid: 08677914-af09-47b7-9d4d-406696e1f504
title: Classe Msvm_EthernetPortInfo
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
ms.openlocfilehash: 7c78dca7adedcf52d93530efdab0da6113855c6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312913"
---
# <a name="msvm_ethernetportinfo-class"></a>\_Classe MSVM EthernetPortInfo

Associazione tra un'istanza della classe [**MSVM \_ EthernetSwitchPort**](msvm-ethernetswitchport.md) e un'istanza della classe [**MSVM \_ EthernetPortData**](msvm-ethernetportdata.md) che rappresenta i dati raccolti sulla porta da un'estensione del commutire.

La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.

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

La **classe \_ EthernetPortInfo di MSVM** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ EthernetPortInfo di MSVM** dispone di queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **MSVM \_ EthernetSwitchPort**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ Dependency. Antecedent")
</dt> </dl>

Istanza della classe [**MSVM \_ EthernetSwitchPort**](msvm-ethernetswitchport.md) che rappresenta la porta di commutazione.

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **MSVM \_ EthernetPortData**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ Dependency. dependent")
</dt> </dl>

Istanza della classe [**\_ EthernetPortData MSVM**](msvm-ethernetportdata.md) che rappresenta i dati della porta.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                                    |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

