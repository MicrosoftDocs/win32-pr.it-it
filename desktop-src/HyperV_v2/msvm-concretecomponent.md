---
description: Associazione generica utilizzata per stabilire parte delle relazioni tra gli elementi gestiti.
ms.assetid: 4D237D68-0A63-4A19-B6AD-E3C781090994
title: Classe Msvm_ConcreteComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ConcreteComponent
- Msvm_ConcreteComponent.GroupComponent
- Msvm_ConcreteComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2ef9e286f4c7ca296ee6b3638ffb9511ccea4115
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314340"
---
# <a name="msvm_concretecomponent-class"></a>\_Classe MSVM ConcreteComponent

Associazione generica utilizzata per stabilire le relazioni ' parte di ' tra gli elementi gestiti. [**CIM \_ ConcreteComponent**](/previous-versions//cc150665(v=vs.85)) è definito come una sottoclasse concreta della classe del [**\_ componente CIM**](/windows/desktop/CIMWin32Prov/cim-component) astratta, da usare al posto di molte sottoclassi specifiche del componente che non aggiungono alcuna semantica (ovvero sottoclassi che non chiariscono il tipo di composizione, aggiornano le cardinalità o aggiungono o rimuovono i qualificatori).

La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ConcreteComponent : CIM_ConcreteComponent
{
  CIM_ManagedElement REF GroupComponent;
  CIM_ManagedElement REF PartComponent;
};
```

## <a name="members"></a>Members

La **classe \_ ConcreteComponent di MSVM** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ ConcreteComponent di MSVM** dispone di queste proprietà.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Elemento padre nell'associazione. Questa proprietà viene ereditata da [**CIM \_ ConcreteComponent**](/previous-versions//cc150665(v=vs.85)).

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Elemento figlio nell'associazione. Questa proprietà viene ereditata da [**CIM \_ ConcreteComponent**](/previous-versions//cc150665(v=vs.85)).

</dd> </dl>

## <a name="remarks"></a>Commenti

L'accesso alla **classe \_ ConcreteComponent di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente. Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                                    |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_CONCRETECOMPONENT CIM**](cim-concretecomponent.md)
</dt> <dt>

[**\_CONCRETECOMPONENT CIM**](/previous-versions//cc150665(v=vs.85))
</dt> <dt>

[Classi di sistema virtuali](virtual-system-classes.md)
</dt> </dl>

 

