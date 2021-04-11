---
description: La \_ classe WMI dell'associazione LogicalProgramGroupItemDataFile Win32 mette in relazione gli elementi del gruppo di programmi del menu Start e i file in cui sono archiviati.
ms.assetid: 9327c205-d0ad-4f2b-a65e-2a648e7c13e0
ms.tgt_platform: multiple
title: Classe Win32_LogicalProgramGroupItemDataFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalProgramGroupItemDataFile
- Win32_LogicalProgramGroupItemDataFile.Antecedent
- Win32_LogicalProgramGroupItemDataFile.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: beec7074104482e4c6bc91ba7efeaea89104a011
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127718"
---
# <a name="win32_logicalprogramgroupitemdatafile-class"></a>Win32 \_ LogicalProgramGroupItemDataFile (classe)

La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) dell'associazione **\_ LogicalProgramGroupItemDataFile Win32** mette in relazione gli elementi del gruppo di programmi del menu **Start** e i file in cui sono archiviati.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{08FFAD62-8050-11d2-90CE-0060081A46FD}"), AMENDMENT]
class Win32_LogicalProgramGroupItemDataFile : CIM_Dependency
{
  Win32_LogicalProgramGroupItem REF Antecedent;
  CIM_DataFile                  REF Dependent;
};
```

## <a name="members"></a>Members

La classe **Win32 \_ LogicalProgramGroupItemDataFile** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **Win32 \_ LogicalProgramGroupItemDataFile** dispone di queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **Win32 \_ LogicalProgramGroupItem**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| WMI \_ Win32 LogicalProgramGroupItem")
</dt> </dl>

Riferimento all'istanza che rappresenta i raggruppamenti di programmi nel menu **Start** .

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati **: \_ DataFile CIM**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| DataFile CIM CIM \_ ")
</dt> </dl>

Riferimento all'istanza di che rappresenta la classe associata al gruppo di programmi.

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **Win32 \_ LogicalProgramGroupItemDataFile** è derivata dalla [**\_ dipendenza CIM**](cim-dependency.md).

Il processo chiamante che usa questa classe deve avere il privilegio **se \_ Restore \_ Name** nel computer in cui risiede il registro di sistema. Se ad esempio si enumera questa classe nel computer locale, l'account con cui viene eseguita l'applicazione deve disporre di questo privilegio. Per altre informazioni, vedere [esecuzione di operazioni con privilegi](/windows/desktop/WmiSdk/executing-privileged-operations).

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

 

