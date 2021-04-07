---
description: La \_ classe WMI dell'associazione ImplementedCategory Win32 mette in relazione una categoria di componenti e la classe Component Object Model (com) utilizzando le relative interfacce.
ms.assetid: 7cf32b50-9ae6-44e5-b364-bc74dea3dc17
ms.tgt_platform: multiple
title: Classe Win32_ImplementedCategory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ImplementedCategory
- Win32_ImplementedCategory.Category
- Win32_ImplementedCategory.Component
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1d885c8c8e92ea661e06b46f338924355438ff9a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749015"
---
# <a name="win32_implementedcategory-class"></a>Win32 \_ ImplementedCategory (classe)

La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) dell'associazione **\_ ImplementedCategory Win32** mette in relazione una categoria di componenti e la classe Component Object Model (com) utilizzando le relative interfacce.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Association, Dynamic, Provider("CIMWin32"), UUID("{0F73ED5B-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_ImplementedCategory
{
  Win32_ComponentCategory REF Category;
  Win32_ClassicCOMClass   REF Component;
};
```

## <a name="members"></a>Members

La classe **Win32 \_ ImplementedCategory** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **Win32 \_ ImplementedCategory** dispone di queste proprietà.

<dl> <dt>

**Categoria**
</dt> <dd> <dl> <dt>

Tipo di dati: **Win32 \_ ComponentCategory**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ ComponentCategory")
</dt> </dl>

Riferimento all'istanza di che rappresenta la categoria di componenti utilizzata dalla classe COM.

</dd> <dt>

**Componente**
</dt> <dd> <dl> <dt>

Tipo di dati: **Win32 \_ ClassicCOMClass**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ ClassicCOMClass")
</dt> </dl>

Riferimento all'istanza di che rappresenta la classe COM utilizzando la categoria associata.

</dd> </dl>

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

[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

