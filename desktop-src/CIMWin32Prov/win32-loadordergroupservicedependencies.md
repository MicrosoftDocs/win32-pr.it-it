---
description: La \_ classe WMI dell'associazione LoadOrderGroupServiceDependencies Win32 mette in relazione un servizio di base e un gruppo di ordini di carico da cui il servizio dipende per avviare l'esecuzione.
ms.assetid: 56739b80-9028-4a2e-85ed-973a078860c1
ms.tgt_platform: multiple
title: Classe Win32_LoadOrderGroupServiceDependencies
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LoadOrderGroupServiceDependencies
- Win32_LoadOrderGroupServiceDependencies.Antecedent
- Win32_LoadOrderGroupServiceDependencies.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b95d1aa01def951802434e787931ce348d04ccb6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127482"
---
# <a name="win32_loadordergroupservicedependencies-class"></a>Win32 \_ LoadOrderGroupServiceDependencies (classe)

La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) dell'associazione **\_ LoadOrderGroupServiceDependencies Win32** mette in relazione un servizio di base e un gruppo di ordini di carico da cui il servizio dipende per avviare l'esecuzione.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4FC-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_LoadOrderGroupServiceDependencies : CIM_Dependency
{
  Win32_LoadOrderGroup REF Antecedent;
  Win32_BaseService    REF Dependent;
};
```

## <a name="members"></a>Members

La classe **Win32 \_ LoadOrderGroupServiceDependencies** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **Win32 \_ LoadOrderGroupServiceDependencies** dispone di queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **Win32 \_ LoadOrderGroup**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| WMI \_ Win32 LoadOrderGroup")
</dt> </dl>

Riferimento all'istanza di che rappresenta le proprietà del gruppo dell'ordine di caricamento che deve iniziare prima che il servizio di base dipendente di questa classe possa essere avviato.

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **Win32 \_ BaseService**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ BaseService")
</dt> </dl>

Riferimento all'istanza di che rappresenta le proprietà del servizio di base che dipende dal gruppo dell'ordine di caricamento per avviare l'esecuzione.

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **Win32 \_ LoadOrderGroupServiceDependencies** è derivata dalla [**\_ dipendenza CIM**](cim-dependency.md).

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

[**\_Dipendenza CIM**](cim-dependency.md)
</dt> <dt>

[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

