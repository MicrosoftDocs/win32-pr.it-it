---
description: La \_ classe WMI associazione sottodirectory Win32 mette in relazione una directory (cartella) e una delle rispettive sottodirectory (sottocartelle).
ms.assetid: f0565b7b-d593-468b-96b1-3922428c61e1
ms.tgt_platform: multiple
title: Classe Win32_SubDirectory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SubDirectory
- Win32_SubDirectory.GroupComponent
- Win32_SubDirectory.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 046de6ad1e09874351b37d58f7277126e39e990a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127315"
---
# <a name="win32_subdirectory-class"></a>\_Classe della sottodirectory Win32

La [classe WMI](../wmisdk/retrieving-a-class.md) associazione **\_ sottodirectory Win32** mette in relazione una directory (cartella) e una delle rispettive sottodirectory (sottocartelle).

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{F25FE469-783E-11d2-90BF-0060081A46FD}"), AMENDMENT]
class Win32_SubDirectory : CIM_Component
{
  Win32_Directory REF GroupComponent;
  Win32_Directory REF PartComponent;
};
```

## <a name="members"></a>Members

La classe della **\_ sottodirectory Win32** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe della **\_ sottodirectory Win32** dispone di queste proprietà.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo di dati **: \_ directory Win32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| directory Win32 WMI \_ ")
</dt> </dl>

Riferimento all'istanza di che rappresenta le proprietà della directory padre (cartella) in questa associazione.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo di dati **: \_ directory Win32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| directory Win32 WMI \_ ")
</dt> </dl>

Riferimento all'istanza che rappresenta la parte della sottodirectory (sottocartella) dell'associazione.

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe della **\_ sottodirectory Win32** è derivata [**dal \_ componente CIM**](cim-component.md).

Per restituire una raccolta di sottocartelle per una cartella, creare una query di associazione che imposta *RESULTROLE* su *PartComponent*. Ciò indica che tutti gli elementi nella raccolta restituita devono svolgere il ruolo di PartComponent, o sottocartella, dell'oggetto cartella. Per restituire la cartella padre per una cartella, impostare *RESULTROLE* su *GroupComponent*.

La classe della **\_ sottodirectory Win32** funziona solo a livello di file System immediatamente sopra o immediatamente sotto la cartella specificata.

## <a name="examples"></a>Esempio

Nell'esempio VBScript seguente viene restituito un elenco di tutte le sottocartelle all'interno della cartella C: \\ Scripts.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colSubfolders = objWMIService.ExecQuery _
 ("ASSOCIATORS OF {Win32_Directory.Name='c:\scripts'} " _
 & "WHERE AssocClass = Win32_Subdirectory " _
 & "ResultRole = PartComponent")
For Each objFolder in colSubfolders
 Wscript.Echo objFolder.Name
Next
```



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

 

 
