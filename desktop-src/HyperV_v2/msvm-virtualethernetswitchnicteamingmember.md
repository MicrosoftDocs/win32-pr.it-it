---
description: Rappresenta l'associazione tra un team ExternalEthernetPort e un membro ExternalEthernetPort.
ms.assetid: e21bea94-d6a8-4788-958e-78ce255837aa
title: Msvm_VirtualEthernetSwitchNicTeamingMember classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchNicTeamingMember
- Msvm_VirtualEthernetSwitchNicTeamingMember.Antecedent
- Msvm_VirtualEthernetSwitchNicTeamingMember.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f6662e2af84b2af1d23ed9941a5ecd5199f7c757161b65933a2154817d717c10
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755111"
---
# <a name="msvm_virtualethernetswitchnicteamingmember-class"></a>Classe Msvm \_ VirtualEthernetSwitchNicTeamingMember

Rappresenta l'associazione tra un team ExternalEthernetPort e un membro ExternalEthernetPort.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualEthernetSwitchNicTeamingMember : CIM_Dependency
{
  Msvm_ExternalEthernetPort REF Antecedent;
  Msvm_ExternalEthernetPort REF Dependent;
};
```

## <a name="members"></a>Members

La **classe Msvm \_ VirtualEthernetSwitchNicTeamingMember** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Msvm \_ VirtualEthernetSwitchNicTeamingMember** ha queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **Msvm \_ ExternalEthernetPort**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

Oggetto [**Msvm \_ ExternalEthernetPort**](msvm-externalethernetport.md) che fa riferimento all'istanza della porta ethernet esterna del team.

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **Msvm \_ ExternalEthernetPort**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dipendente")
</dt> </dl>

Riferimento [**all'istanza msvm \_ ExternalEthernetPort**](msvm-externalethernetport.md) del membro.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                                             |
| Server minimo supportato<br/> | Windows Server 2016<br/>                                                                          |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Dipendenza \_ CIM**](cim-dependency.md)
</dt> </dl>

 

