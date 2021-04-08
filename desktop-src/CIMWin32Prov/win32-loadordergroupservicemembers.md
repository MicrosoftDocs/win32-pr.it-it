---
description: La \_ classe WMI dell'associazione LoadOrderGroupServiceMembers Win32 mette in correlazione un gruppo di ordini di carico e un servizio di base.
ms.assetid: 60fa8292-b9d1-48f2-bd26-e5c9276006fc
ms.tgt_platform: multiple
title: Classe Win32_LoadOrderGroupServiceMembers
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LoadOrderGroupServiceMembers
- Win32_LoadOrderGroupServiceMembers.GroupComponent
- Win32_LoadOrderGroupServiceMembers.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 557e9b029dcbdac06e24d1630f00488696792e25
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878294"
---
# <a name="win32_loadordergroupservicemembers-class"></a>Win32 \_ LoadOrderGroupServiceMembers (classe)

La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) dell'associazione **\_ LoadOrderGroupServiceMembers Win32** mette in correlazione un gruppo di ordini di carico e un servizio di base.

> [!Note]  
> [**Win32 \_**](win32-systemdriver.md) Gli oggetti SystemDriver sono membri del gruppo di ordini di caricamento. Non tutti i servizi sono membri dei gruppi e non tutti i gruppi dispongono di servizi al loro interno.

 

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4EF-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_LoadOrderGroupServiceMembers : CIM_Component
{
  Win32_LoadOrderGroup REF GroupComponent;
  Win32_BaseService    REF PartComponent;
};
```

## <a name="members"></a>Members

La classe **Win32 \_ LoadOrderGroupServiceMembers** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **Win32 \_ LoadOrderGroupServiceMembers** dispone di queste proprietà.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **Win32 \_ LoadOrderGroup**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ LoadOrderGroup")
</dt> </dl>

Riferimento all'istanza che rappresenta le proprietà del gruppo dell'ordine di caricamento associate al servizio di base.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **Win32 \_ BaseService**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ BaseService")
</dt> </dl>

Riferimento all'istanza di che rappresenta il servizio membro di un gruppo di ordine di caricamento.

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **Win32 \_ LoadOrderGroupServiceMembers** è derivata dal [**\_ componente CIM**](cim-component.md).

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

 

