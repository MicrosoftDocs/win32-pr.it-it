---
description: Descrive i dati dell'impostazione per una porta seriale virtuale.
ms.assetid: 8b257bbf-495a-4eef-86a1-70e31e4a85a5
title: Classe Msvm_SerialPortSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SerialPortSettingData
- Msvm_SerialPortSettingData.DebuggerMode
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 21a1ab58608c5631a328795272d6a04aa56aedf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882157"
---
# <a name="msvm_serialportsettingdata-class"></a>\_Classe MSVM SerialPortSettingData

Descrive i dati dell'impostazione per una porta seriale virtuale.

La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SerialPortSettingData : CIM_ResourceAllocationSettingData
{
  boolean DebuggerMode;
};
```

## <a name="members"></a>Members

La **classe \_ SerialPortSettingData di MSVM** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ SerialPortSettingData di MSVM** dispone di queste proprietà.

<dl> <dt>

**DebuggerMode**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

**true** se la modalità del debugger è abilitata su una porta seriale virtuale; in caso contrario, **false**. La modalità debugger consente di migliorare l'utilizzo di un debugger del kernel di Microsoft Windows su una porta seriale virtuale.

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

[**\_RESOURCEALLOCATIONSETTINGDATA CIM**](cim-resourceallocationsettingdata.md)
</dt> </dl>

 

 




