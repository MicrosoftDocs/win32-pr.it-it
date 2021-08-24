---
description: Associa un dispositivo logico al sistema padre.
ms.assetid: 2BEAAEC8-F8F2-4CC7-A209-EE3EE3C6FA90
title: Msvm_SystemDevice classe
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
ms.openlocfilehash: 67c538d82657d1ac07246f21dc2688f968ce969d1bf20238b20eeb4eea6f71cb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746571"
---
# <a name="msvm_systemdevice-class"></a>Classe \_ SystemDevice msvm

I dispositivi logici possono essere aggregati da un sistema. Questa relazione viene resa esplicita dall'associazione del dispositivo di sistema.

La sintassi seguente è Managed Object Format codice MOF e include tutte le proprietà ereditate.

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

La **classe \_ SystemDevice msvm** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ SystemDevice msvm** ha queste proprietà.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **sistema \_ CIM**](/windows/desktop/CIMWin32Prov/cim-system)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) ( 1 ), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) ( 1 )
</dt> </dl>

Sistema padre nell'associazione. Questa proprietà viene ereditata dal [**componente CIM. \_**](/windows/desktop/CIMWin32Prov/cim-component)

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Dispositivo logico che è un elemento di un sistema. Questa proprietà viene ereditata dal [**componente CIM. \_**](/windows/desktop/CIMWin32Prov/cim-component)

</dd> </dl>

## <a name="remarks"></a>Commenti

L'accesso alla **classe \_ SystemDevice msvm** potrebbe essere limitato dal filtro di Controllo dell'account utente. Per altre informazioni, vedere [Controllo dell'account utente e WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                              |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                    |
| Spazio dei nomi<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CIM \_ SystemDevice**](cim-systemdevice.md)
</dt> <dt>

[**CIM \_ SystemDevice**](/windows/desktop/CIMWin32Prov/cim-systemdevice)
</dt> <dt>

[Classi di sistema virtuale](virtual-system-classes.md)
</dt> </dl>

 

