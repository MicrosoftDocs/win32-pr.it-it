---
description: La \_ classe WMI dell'associazione LogicalProgramGroupDirectory Win32 mette in relazione i gruppi di programmi logici (raggruppamenti nel menu Start) e le directory dei file in cui sono archiviati.
ms.assetid: 31a8b56a-d4fd-4cc5-9997-ec6211fe9425
ms.tgt_platform: multiple
title: Classe Win32_LogicalProgramGroupDirectory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalProgramGroupDirectory
- Win32_LogicalProgramGroupDirectory.Antecedent
- Win32_LogicalProgramGroupDirectory.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d6ebaddd4455ba1b62832f940d78534c90cefeeb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304472"
---
# <a name="win32_logicalprogramgroupdirectory-class"></a>Win32 \_ LogicalProgramGroupDirectory (classe)

La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) dell'associazione **\_ LogicalProgramGroupDirectory Win32** mette in relazione i gruppi di programmi logici (raggruppamenti nel menu **Start** ) e le directory dei file in cui sono archiviati.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{F25FE467-783E-11d2-90BF-0060081A46FD}"), AMENDMENT]
class Win32_LogicalProgramGroupDirectory : CIM_Dependency
{
  Win32_LogicalProgramGroup REF Antecedent;
  Win32_Directory           REF Dependent;
};
```

## <a name="members"></a>Members

La classe **Win32 \_ LogicalProgramGroupDirectory** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **Win32 \_ LogicalProgramGroupDirectory** dispone di queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **Win32 \_ LogicalProgramGroup**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| WMI \_ Win32 LogicalProgramGroup")
</dt> </dl>

Riferimento all'istanza che rappresenta il gruppo di programmi logici.

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati **: \_ directory Win32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| directory Win32 WMI \_ ")
</dt> </dl>

Riferimento all'istanza di che rappresenta la directory di file per il gruppo di programmi logici.

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **Win32 \_ LogicalProgramGroupDirectory** è derivata dalla [**\_ dipendenza CIM**](cim-dependency.md).

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

 

