---
description: Rappresenta l'associazione tra un'estensione del Commuter Ethernet padre e un'estensione del Commuter Ethernet figlio.
ms.assetid: a0a60214-d85d-4c64-b720-1c34abc25287
title: Classe Msvm_ParentEthernetSwitchExtension
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ParentEthernetSwitchExtension
- Msvm_ParentEthernetSwitchExtension.Antecedent
- Msvm_ParentEthernetSwitchExtension.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8e215a01c9de98baa545dbb32b8279db4555f9cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318319"
---
# <a name="msvm_parentethernetswitchextension-class"></a>\_Classe MSVM ParentEthernetSwitchExtension

Rappresenta l'associazione tra un'estensione del Commuter Ethernet padre e un'estensione del Commuter Ethernet figlio.

La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ParentEthernetSwitchExtension : CIM_Dependency
{
  Msvm_EthernetSwitchExtension REF Antecedent;
  Msvm_EthernetSwitchExtension REF Dependent;
};
```

## <a name="members"></a>Members

La **classe \_ ParentEthernetSwitchExtension di MSVM** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ ParentEthernetSwitchExtension di MSVM** dispone di queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **MSVM \_ EthernetSwitchExtension**](msvm-ethernetswitchextension.md)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")
</dt> </dl>

Riferimento a un'istanza della classe [**MSVM \_ EthernetSwitchExtension**](msvm-ethernetswitchextension.md) che rappresenta l'estensione del comcambio padre.

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **MSVM \_ EthernetSwitchExtension**](msvm-ethernetswitchextension.md)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")
</dt> </dl>

Riferimento a un'istanza della classe [**\_ EthernetSwitchExtension di MSVM**](msvm-ethernetswitchextension.md) che rappresenta l'estensione del commutire figlio.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                                    |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

