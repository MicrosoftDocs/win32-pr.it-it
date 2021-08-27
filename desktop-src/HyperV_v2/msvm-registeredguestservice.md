---
description: Rappresenta un'associazione tra un'istanza di Msvm GuestServiceInterfaceComponent e un'istanza di \_ Msvm GuestService, che rappresenta un servizio \_ in esecuzione nel guest.
ms.assetid: 246CFAC1-7D83-4DE7-B9D3-96326511E08B
title: Msvm_RegisteredGuestService classe
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
ms.openlocfilehash: cf2e551a30f169477f9dc73e58ecd9e6c3a78b708c047eb0088f36782623da3c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130441"
---
# <a name="msvm_registeredguestservice-class"></a>Classe Msvm \_ RegisteredGuestService

Rappresenta un'associazione tra un'istanza di [**Msvm \_ GuestServiceInterfaceComponent**](msvm-guestserviceinterfacecomponent.md) e un'istanza di [**Msvm \_ GuestService**](msvm-guestservice.md), che rappresenta un servizio in esecuzione nel guest. Questa classe deriva dalla [**classe \_ Dependency CIM.**](/windows/desktop/CIMWin32Prov/cim-dependency)

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

La **classe Msvm \_ RegisteredGuestService** include questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Msvm \_ RegisteredGuestService** ha queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **Msvm \_ GuestServiceInterfaceComponent**](msvm-guestserviceinterfacecomponent.md)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ Dependency.Antecedent")
</dt> </dl>

Riferimento al componente dell'interfaccia del servizio guest in questa associazione.

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **Msvm \_ GuestService**](msvm-guestservice.md)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ Dependency.Dependent")
</dt> </dl>

Riferimento al servizio guest registrato che dipende dalla **proprietà Antecedent.**

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8.1 solo app desktop\]<br/>                                                            |
| Server minimo supportato<br/> | Windows Server 2012 Solo \[ app desktop R2\]<br/>                                                 |
| Spazio dei nomi<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Dipendenza \_ CIM**](cim-dependency.md)
</dt> <dt>

[**Dipendenza \_ CIM**](/windows/desktop/CIMWin32Prov/cim-dependency)
</dt> </dl>

 

