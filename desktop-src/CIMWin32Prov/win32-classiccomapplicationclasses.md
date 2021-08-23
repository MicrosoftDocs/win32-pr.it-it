---
description: La classe WMI di associazione Win32 ClassicCOMApplicationClasses mette in relazione un'applicazione COM e un \_ componente COM raggruppati al di sotto di essa.
ms.assetid: 77f24461-9ca0-4fc3-8728-4a4b9a1edbc3
ms.tgt_platform: multiple
title: Win32_ClassicCOMApplicationClasses classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ClassicCOMApplicationClasses
- Win32_ClassicCOMApplicationClasses.PartComponent
- Win32_ClassicCOMApplicationClasses.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 24bc2871afa5916644a3bcdb3ddb4ad2f653e7aa1cd0522c52782ef17bb2352c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751391"
---
# <a name="win32_classiccomapplicationclasses-class"></a>Classe Win32 \_ ClassicCOMApplicationClasses

La classe [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **di associazione \_ Win32 ClassicCOMApplicationClasses** mette in relazione un'applicazione COM e un componente COM raggruppati al di sotto di essa.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{0F73ED54-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_ClassicCOMApplicationClasses : Win32_COMApplicationClasses
{
  Win32_ClassicCOMClass REF PartComponent;
  Win32_DCOMApplication REF GroupComponent;
};
```

## <a name="members"></a>Members

La **classe Win32 \_ ClassicCOMApplicationClasses** include questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Win32 \_ ClassicCOMApplicationClasses** ha queste proprietà.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **Win32 \_ DCOMApplication**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ DCOMApplication")
</dt> </dl>

Oggetto [**\_ DCOMApplication Win32 che**](win32-dcomapplication.md) rappresenta un'applicazione DCOM che contiene o usa il componente COM.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **Win32 \_ ClassicCOMClass**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ ClassicCOMClass")
</dt> </dl>

Classe [**Win32 \_ ClassicCOMClass**](win32-classiccomclass.md) che rappresenta il componente COM esistente in o usato dall'applicazione DCOM.

</dd> </dl>

## <a name="remarks"></a>Commenti

La **classe Win32 \_ ClassicCOMApplicationClasses** è derivata da [**\_ WIN32 COMApplicationClasses.**](win32-comapplicationclasses.md)

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

[**Classi \_ COMApplicationClasses Win32**](win32-comapplicationclasses.md)
</dt> <dt>

[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

