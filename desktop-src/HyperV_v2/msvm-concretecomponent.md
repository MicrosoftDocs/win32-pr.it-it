---
description: Associazione generica utilizzata per stabilire parte delle relazioni tra elementi gestiti.
ms.assetid: 4D237D68-0A63-4A19-B6AD-E3C781090994
title: Msvm_ConcreteComponent classe
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
ms.openlocfilehash: 24b813e7b8460f3de24207ed91b2e113f0d6b9633e17263806ef8447c166bdf7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119531751"
---
# <a name="msvm_concretecomponent-class"></a>Classe Msvm \_ ConcreteComponent

Associazione generica usata per stabilire relazioni "parte di" tra elementi gestiti. [**CIM \_ ConcreteComponent**](/previous-versions//cc150665(v=vs.85)) è definito come sottoclasse concreta della classe [**CiM \_ Component**](/windows/desktop/CIMWin32Prov/cim-component) astratta, da usare al posto di molte sottoclassi specifiche del componente che non aggiungono semantica, ovvero sottoclassi che non chiariscono il tipo di composizione, aggiornano cardinalità o aggiungono o rimuovono qualificatori.

La sintassi seguente è Managed Object Format codice MOF (Simplified Managed Object Format) e include tutte le proprietà ereditate.

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

La **classe Msvm \_ ConcreteComponent** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Msvm \_ ConcreteComponent** ha queste proprietà.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Elemento padre nell'associazione. Questa proprietà viene ereditata da [**CIM \_ ConcreteComponent.**](/previous-versions//cc150665(v=vs.85))

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Elemento figlio nell'associazione. Questa proprietà viene ereditata da [**CIM \_ ConcreteComponent.**](/previous-versions//cc150665(v=vs.85))

</dd> </dl>

## <a name="remarks"></a>Commenti

L'accesso alla **classe Msvm \_ ConcreteComponent** potrebbe essere limitato dal filtro del controllo dell'account utente. Per altre informazioni, vedere [Controllo dell'account utente e WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                              |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                    |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CIM \_ ConcreteComponent**](cim-concretecomponent.md)
</dt> <dt>

[**CIM \_ ConcreteComponent**](/previous-versions//cc150665(v=vs.85))
</dt> <dt>

[Classi di sistema virtuale](virtual-system-classes.md)
</dt> </dl>

 

