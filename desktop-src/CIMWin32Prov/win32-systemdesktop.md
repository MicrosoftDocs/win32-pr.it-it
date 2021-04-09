---
description: La \_ classe WMI dell'associazione SystemDesktop Win32 mette in correlazione un computer e la relativa configurazione desktop.
ms.assetid: 2b024660-d707-4463-8207-73df74bfa7d6
ms.tgt_platform: multiple
title: Classe Win32_SystemDesktop
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDesktop
- Win32_SystemDesktop.Element
- Win32_SystemDesktop.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3e14cab58a445fd645b9d59c1aea713bf6c40ac0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966324"
---
# <a name="win32_systemdesktop-class"></a>Win32 \_ SystemDesktop (classe)

La [classe WMI](../wmisdk/retrieving-a-class.md) dell'associazione **\_ SystemDesktop Win32** mette in correlazione un computer e la relativa configurazione desktop.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C506-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemDesktop : Win32_SystemSetting
{
  Win32_ComputerSystem REF Element;
  Win32_Desktop        REF Setting;
};
```

## <a name="members"></a>Members

La classe **Win32 \_ SystemDesktop** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **Win32 \_ SystemDesktop** dispone di queste proprietà.

<dl> <dt>

**elemento**
</dt> <dd> <dl> <dt>

Tipo di dati: **Win32 \_ ComputerSystem**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](../wmisdk/standard-qualifiers.md) ("element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")
</dt> </dl>

Riferimento all'istanza di che rappresenta il computer in cui è presente la configurazione desktop.

</dd> <dt>

**Impostazione**
</dt> <dd> <dl> <dt>

Tipo di dati **: \_ desktop Win32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](../wmisdk/standard-qualifiers.md) ("impostazione"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| desktop Win32 Win32 \_ ")
</dt> </dl>

Riferimento all'istanza di che rappresenta la configurazione esistente nel computer.

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **Win32 \_ SystemDesktop** è derivata da [**Win32 \_ SystemSetting**](win32-systemsetting.md).

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

 

 
