---
description: Rappresenta un'associazione tra una vista e un'istanza di che rappresenta la visualizzazione normalizzata di una risorsa gestita.
ms.assetid: 9c6eb3d5-7366-4954-9e64-12f889c64114
title: Classe CIM_ElementView
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementView
- CIM_ElementView.Antecedent
- CIM_ElementView.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b6ffc0e4b69667800b1880cae1a992a207cc95a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312931"
---
# <a name="cim_elementview-class"></a>CIM \_ ElementView (classe)

Rappresenta un'associazione tra una vista e un'istanza di che rappresenta la visualizzazione normalizzata di una risorsa gestita.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, Association, Experimental, Version("2.21.1"), UMLPackagePath("CIM::Core::CoreElements")]
class CIM_ElementView : CIM_Dependency
{
  CIM_ManagedElement REF Antecedent;
  CIM_View           REF Dependent;
};
```

## <a name="members"></a>Members

La classe **CIM \_ ElementView** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **CIM \_ ElementView** dispone di queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ Managed**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")
</dt> </dl>

Istanza di che rappresenta la visualizzazione normalizzata della risorsa gestita.

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati **: \_ visualizzazione CIM**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")
</dt> </dl>

Visualizzazione che rappresenta una vista denormalizzata o aggregata della risorsa gestita.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows 10\]<br/>                                                             |
| Server minimo supportato<br/> | Windows Server 2016<br/>                                                                          |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Dipendenza CIM**](cim-dependency.md)
</dt> </dl>

 

