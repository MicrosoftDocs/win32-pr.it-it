---
description: Rappresenta un'associazione tra un'istanza di MSVM \_ GuestServiceInterfaceComponent e un'istanza di MSVM \_ GuestService, che rappresenta un servizio in esecuzione nel guest.
ms.assetid: 246CFAC1-7D83-4DE7-B9D3-96326511E08B
title: Classe Msvm_RegisteredGuestService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_RegisteredGuestService
- Msvm_RegisteredGuestService.Antecedent
- Msvm_RegisteredGuestService.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 850d7f081b070fd34ef11bc56e8cd1f914e498b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103756893"
---
# <a name="msvm_registeredguestservice-class"></a>\_Classe MSVM RegisteredGuestService

Rappresenta un'associazione tra un'istanza di [**MSVM \_ GuestServiceInterfaceComponent**](msvm-guestserviceinterfacecomponent.md) e un'istanza di [**MSVM \_ GuestService**](msvm-guestservice.md), che rappresenta un servizio in esecuzione nel guest. Questa classe deriva dalla classe di [**\_ dipendenza CIM**](/windows/desktop/CIMWin32Prov/cim-dependency) .

La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_RegisteredGuestService : CIM_Dependency
{
  Msvm_GuestServiceInterfaceComponent REF Antecedent;
  Msvm_GuestService                   REF Dependent;
};
```

## <a name="members"></a>Members

La **classe \_ RegisteredGuestService di MSVM** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ RegisteredGuestService di MSVM** dispone di queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **MSVM \_ GuestServiceInterfaceComponent**](msvm-guestserviceinterfacecomponent.md)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ Dependency. Antecedent")
</dt> </dl>

Riferimento al componente dell'interfaccia del servizio Guest in questa associazione.

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **MSVM \_ GuestService**](msvm-guestservice.md)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ Dependency. dependent")
</dt> </dl>

Riferimento al servizio Guest registrato che dipende dalla proprietà **precedente** .

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1 \[ solo app desktop\]<br/>                                                            |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2012 R2 \[\]<br/>                                                 |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Dipendenza CIM**](cim-dependency.md)
</dt> <dt>

[**\_Dipendenza CIM**](/windows/desktop/CIMWin32Prov/cim-dependency)
</dt> </dl>

 

