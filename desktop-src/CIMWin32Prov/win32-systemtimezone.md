---
description: La \_ classe WMI dell'associazione SystemTimeZone Win32 mette in correlazione un computer e un fuso orario.
ms.assetid: 53c74a61-c91d-4daa-933e-4cc7b9583d98
ms.tgt_platform: multiple
title: Classe Win32_SystemTimeZone
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemTimeZone
- Win32_SystemTimeZone.Element
- Win32_SystemTimeZone.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9ec294600fdc81f085bf29f5e664bcbec961417c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877801"
---
# <a name="win32_systemtimezone-class"></a>Win32 \_ SystemTimeZone (classe)

La [classe WMI](../wmisdk/retrieving-a-class.md) dell'associazione **\_ SystemTimeZone Win32** mette in correlazione un computer e un fuso orario.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C504-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemTimeZone : Win32_SystemSetting
{
  Win32_ComputerSystem REF Element;
  Win32_TimeZone       REF Setting;
};
```

## <a name="members"></a>Members

La classe **Win32 \_ SystemTimeZone** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **Win32 \_ SystemTimeZone** dispone di queste proprietà.

<dl> <dt>

**elemento**
</dt> <dd> <dl> <dt>

Tipo di dati: **Win32 \_ ComputerSystem**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](../wmisdk/standard-qualifiers.md) ("element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")
</dt> </dl>

Riferimento all'istanza che rappresenta il sistema del computer che tiene traccia del fuso orario di sistema.

</dd> <dt>

**Impostazione**
</dt> <dd> <dl> <dt>

Tipo di dati **: \_ fuso orario Win32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](../wmisdk/standard-qualifiers.md) ("setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ TimeZone")
</dt> </dl>

Riferimento all'istanza di che rappresenta le proprietà del fuso orario registrate dal sistema del computer.

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **Win32 \_ SystemTimeZone** è derivata da [**Win32 \_ SystemSetting**](win32-systemsetting.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_SystemSetting Win32**](win32-systemsetting.md)
</dt> <dt>

[Classi del sistema operativo](./operating-system-classes.md)
</dt> </dl>

 

 
