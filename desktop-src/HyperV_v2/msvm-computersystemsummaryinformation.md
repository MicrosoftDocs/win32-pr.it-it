---
description: Contiene un riepilogo delle informazioni sul sistema di computer virtuale specificato.
ms.assetid: ab31d5db-a8d3-47bc-a024-0f4c4b93a34b
title: Classe Msvm_ComputerSystemSummaryInformation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ComputerSystemSummaryInformation
- Msvm_ComputerSystemSummaryInformation.Antecedent
- Msvm_ComputerSystemSummaryInformation.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 35248bcfa14609e8db25b148088b6feb8d161116
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879297"
---
# <a name="msvm_computersystemsummaryinformation-class"></a>\_Classe MSVM ComputerSystemSummaryInformation

Contiene un riepilogo delle informazioni sul sistema di computer virtuale specificato.

La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Association, Provider("VmmsWmiInstanceAndMethodProvider")]
class Msvm_ComputerSystemSummaryInformation : CIM_ElementView
{
  CIM_ComputerSystem          REF Antecedent;
  Msvm_SummaryInformationBase REF Dependent;
};
```

## <a name="members"></a>Members

La **classe \_ ComputerSystemSummaryInformation di MSVM** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ ComputerSystemSummaryInformation di MSVM** dispone di queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ ComputerSystem**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")
</dt> </dl>

Oggetto [**CIM \_ ComputerSystem**](cim-computersystem.md) che rappresenta un'istanza della rappresentazione normalizzata della risorsa gestita.

> [!Note]
>
> DataType aggiornato da [**MSVM \_ ComputerSystem**](msvm-computersystem.md) in Windows 10, versione 1703.

 

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **MSVM \_ SummaryInformationBase**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")
</dt> </dl>

Istanza di [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) che rappresenta una vista denormalizzata o aggregata della risorsa gestita rappresentata dal [**\_ ComputerSystem MSVM**](msvm-computersystem.md) a cui fa riferimento la proprietà precedente.

> [!Note]
>
> DataType aggiornato da [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) in Windows 10, versione 1703.

 

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

[**\_ELEMENTVIEW CIM**](cim-elementview.md)
</dt> </dl>

 

