---
description: Associa un dispositivo logico al sistema padre.
ms.assetid: 2BEAAEC8-F8F2-4CC7-A209-EE3EE3C6FA90
title: Classe Msvm_SystemDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SystemDevice
- Msvm_SystemDevice.GroupComponent
- Msvm_SystemDevice.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: be31a51ad4e24bd31785e64400bf5b266624d8d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306023"
---
# <a name="msvm_systemdevice-class"></a>\_Classe MSVM SystemDevice

I dispositivi logici possono essere aggregati da un sistema. Questa relazione viene resa esplicita dall'associazione di dispositivi di sistema.

La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SystemDevice : CIM_SystemDevice
{
  CIM_System        REF GroupComponent;
  CIM_LogicalDevice REF PartComponent;
};
```

## <a name="members"></a>Members

La **classe \_ SystemDevice di MSVM** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ SystemDevice di MSVM** dispone di queste proprietà.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **\_ sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Sistema padre nell'associazione. Questa proprietà viene ereditata [**dal \_ componente CIM**](/windows/desktop/CIMWin32Prov/cim-component).

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Il dispositivo logico che è un elemento di un sistema. Questa proprietà viene ereditata [**dal \_ componente CIM**](/windows/desktop/CIMWin32Prov/cim-component).

</dd> </dl>

## <a name="remarks"></a>Commenti

L'accesso alla **classe \_ SystemDevice di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente. Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**\_SYSTEMDEVICE CIM**](cim-systemdevice.md)
</dt> <dt>

[**\_SYSTEMDEVICE CIM**](/windows/desktop/CIMWin32Prov/cim-systemdevice)
</dt> <dt>

[Classi di sistema virtuali](virtual-system-classes.md)
</dt> </dl>

 

