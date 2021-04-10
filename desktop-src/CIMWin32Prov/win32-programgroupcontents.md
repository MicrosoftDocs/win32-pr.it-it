---
description: La \_ classe WMI dell'associazione ProgramGroupContents Win32 mette in correlazione un ordine del gruppo di programmi e un singolo gruppo o elemento del programma contenuto.
ms.assetid: 687794d1-acc1-498a-9886-0c9ac762ebf4
ms.tgt_platform: multiple
title: Classe Win32_ProgramGroupContents
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ProgramGroupContents
- Win32_ProgramGroupContents.GroupComponent
- Win32_ProgramGroupContents.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5f77a61052357f7c67009ee7a89da018abeadda8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049118"
---
# <a name="win32_programgroupcontents-class"></a>Win32 \_ ProgramGroupContents (classe)

La [classe WMI](../wmisdk/retrieving-a-class.md) dell'associazione **\_ ProgramGroupContents Win32** mette in correlazione un ordine del gruppo di programmi e un singolo gruppo o elemento del programma contenuto.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{86E30E83-7DB2-11d2-90CB-0060081A46FD}"), AMENDMENT]
class Win32_ProgramGroupContents : CIM_Component
{
  Win32_LogicalProgramGroup REF GroupComponent;
  Win32_ProgramGroupOrItem  REF PartComponent;
};
```

## <a name="members"></a>Members

La classe **Win32 \_ ProgramGroupContents** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **Win32 \_ ProgramGroupContents** dispone di queste proprietà.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **Win32 \_ LogicalProgramGroup**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ LogicalProgramGroup")
</dt> </dl>

Riferimento all'istanza di che rappresenta il gruppo di programmi logici per questa associazione.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **Win32 \_ ProgramGroupOrItem**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ProgramGroupOrItem")
</dt> </dl>

Riferimento all'istanza di che rappresenta il gruppo o l'elemento del menu **Start** per questa associazione.

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **Win32 \_ ProgramGroupContents** è derivata dal [**\_ componente CIM**](cim-component.md).

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

[Classi del sistema operativo](./operating-system-classes.md)
</dt> </dl>

 

 
