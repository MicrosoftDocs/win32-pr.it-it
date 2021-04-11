---
description: La \_ classe WMI COMApplicationClasses abstract Association di Win32 mette in correlazione un componente Component Object Model (com) e l'applicazione com in cui risiede.
ms.assetid: 7c188199-86fb-45ba-b318-9d9529b831b8
ms.tgt_platform: multiple
title: Classe Win32_COMApplicationClasses
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_COMApplicationClasses
- Win32_COMApplicationClasses.PartComponent
- Win32_COMApplicationClasses.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 01413128f7457049a4383c1148938e2136645337
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127347"
---
# <a name="win32_comapplicationclasses-class"></a>Win32 \_ COMApplicationClasses (classe)

La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ COMApplicationClasses** abstract Association di Win32 mette in correlazione un componente Component Object Model (COM) e l'applicazione com in cui risiede.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[abstract, UUID("{0F73ED51-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_COMApplicationClasses : CIM_Component
{
  Win32_COMClass       REF PartComponent;
  Win32_COMApplication REF GroupComponent;
};
```

## <a name="members"></a>Members

La classe **Win32 \_ COMApplicationClasses** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **Win32 \_ COMApplicationClasses** dispone di queste proprietà.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo di dati **: \_ comApplicazione Win32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ comapplication")
</dt> </dl>

[**ComApplicazione \_ Win32**](win32-comapplication.md) che rappresenta l'applicazione com contenente il componente com.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo di dati **: \_ Comclasse Win32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| classe Win32 di WMI \_ ")
</dt> </dl>

[**Comclasse \_ Win32**](win32-comclass.md) che rappresenta il componente com raggruppato nell'applicazione com.

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **Win32 \_ COMApplicationClasses** è derivata dal [**\_ componente CIM**](cim-component.md).

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

[**\_Componente CIM**](cim-component.md)
</dt> <dt>

[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

