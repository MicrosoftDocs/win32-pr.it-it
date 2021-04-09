---
description: La \_ classe WMI dell'associazione OperatingSystemQFE Win32 mette in correlazione un sistema operativo e gli aggiornamenti del prodotto applicati come rappresentati in Win32 \_ QuickFixEngineering.
ms.assetid: 71985759-7e45-44df-82a9-f9a93e3b923e
ms.tgt_platform: multiple
title: Classe Win32_OperatingSystemQFE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystemQFE
- Win32_OperatingSystemQFE.Antecedent
- Win32_OperatingSystemQFE.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a3b357e3c6efb62217c137bc6c785185154ed984
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966294"
---
# <a name="win32_operatingsystemqfe-class"></a>Win32 \_ OperatingSystemQFE (classe)

La [classe WMI](../wmisdk/retrieving-a-class.md) dell'associazione **\_ OperatingSystemQFE Win32** mette in correlazione un sistema operativo e gli aggiornamenti del prodotto applicati come rappresentati in [**Win32 \_ QuickFixEngineering**](win32-quickfixengineering.md).

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{2CB2C452-C516-11D2-B364-00105A1F77A1}"), AMENDMENT]
class Win32_OperatingSystemQFE : CIM_Dependency
{
  Win32_OperatingSystem     REF Antecedent;
  Win32_QuickFixEngineering REF Dependent;
};
```

## <a name="members"></a>Members

La classe **Win32 \_ OperatingSystemQFE** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **Win32 \_ OperatingSystemQFE** dispone di queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **Win32 \_ OperatingSystem**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("antecedente"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| WMI \_ Win32 OperatingSystem")
</dt> </dl>

Riferimento all'istanza di che rappresenta il sistema interessato dall'aggiornamento del prodotto nell'associazione.

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **Win32 \_ QuickFixEngineering**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**debole**](../wmisdk/standard-qualifiers.md), [**override**](../wmisdk/standard-qualifiers.md) ("dipendente"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ QuickFixEngineering")
</dt> </dl>

Riferimento all'istanza di che rappresenta l'istanza dell'oggetto applicata al sistema operativo in questa associazione.

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **Win32 \_ OperatingSystemQFE** è derivata dalla [**\_ dipendenza CIM**](cim-dependency.md).

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

[Classi del sistema operativo](./operating-system-classes.md)
</dt> </dl>

 

 
