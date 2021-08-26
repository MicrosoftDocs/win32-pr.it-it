---
description: La classe WMI di associazione SystemDevices Win32 mette in relazione un sistema computer e un dispositivo \_ logico installato in tale sistema.
ms.assetid: 84dfcb75-3b44-4b27-8eee-779be522eb1f
ms.tgt_platform: multiple
title: Win32_SystemDevices classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDevices
- Win32_SystemDevices.GroupComponent
- Win32_SystemDevices.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 698b827e2dd3f9097f2348c83cbb52120186b0694a836fd2468396c542e535c4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119971471"
---
# <a name="win32_systemdevices-class"></a>Classe SystemDevices Win32 \_

La classe [WMI](../wmisdk/retrieving-a-class.md) di **associazione \_ SystemDevices Win32** mette in relazione un sistema di computer e un dispositivo logico installato in tale sistema.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà e i metodi sono in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F4-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemDevices : CIM_SystemDevice
{
  Win32_ComputerSystem REF GroupComponent;
  CIM_LogicalDevice    REF PartComponent;
};
```

## <a name="members"></a>Members

La **classe \_ SystemDevices Win32** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ SystemDevices Win32** ha queste proprietà.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **\_ ComputerSystem Win32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Wmi \| Win32 \_ ComputerSystem")
</dt> </dl>

Riferimento all'istanza che rappresenta le proprietà del sistema informatico in cui è presente il dispositivo logico.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ LogicalDevice**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**key,**](../wmisdk/key-qualifier.md) [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) \| ("CIM CIM \_ LogicalDevice")
</dt> </dl>

Riferimento all'istanza che rappresenta le proprietà di un dispositivo logico presente nel sistema del computer.

</dd> </dl>

## <a name="remarks"></a>Commenti

La **classe \_ SystemDevices Win32** è derivata da [**CIM \_ SystemDevice**](cim-systemdevice.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CIM \_ SystemDevice**](cim-systemdevice.md)
</dt> <dt>

[Classi del sistema operativo](./operating-system-classes.md)
</dt> </dl>

 

 
