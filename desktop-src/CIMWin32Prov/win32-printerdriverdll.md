---
description: La \_ classe WMI dell'associazione PrinterDriverDll Win32 mette in relazione una stampante locale e il relativo file del driver.
ms.assetid: decbd1de-8091-47f7-94a1-42862070b920
ms.tgt_platform: multiple
title: Classe Win32_PrinterDriverDll
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterDriverDll
- Win32_PrinterDriverDll.Antecedent
- Win32_PrinterDriverDll.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 41484c39d9e1b59efd79d7aee08719b3a241de97
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483693"
---
# <a name="win32_printerdriverdll-class"></a>Win32 \_ PrinterDriverDll (classe)

La [classe WMI](../wmisdk/retrieving-a-class.md) dell'associazione **\_ PrinterDriverDll Win32** mette in relazione una stampante locale e il relativo file del driver.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class Win32_PrinterDriverDll : CIM_Dependency
{
  CIM_DataFile  REF Antecedent;
  Win32_Printer REF Dependent;
};
```

## <a name="members"></a>Members

La classe **Win32 \_ PrinterDriverDll** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **Win32 \_ PrinterDriverDll** dispone di queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati **: \_ DataFile CIM**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](../wmisdk/standard-qualifiers.md)
</dt> </dl>

Riferimento all'istanza [**di \_ DataFile DataFile**](cim-datafile.md) che rappresenta il file del driver per la stampante basata su Windows.

Questa proprietà viene ereditata [**dalla \_ dipendenza CIM**](cim-dependency.md).

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati **: \_ stampante Win32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](../wmisdk/standard-qualifiers.md)
</dt> </dl>

Riferimento all'istanza [**della \_ stampante Win32**](win32-printer.md) .

Questa proprietà viene ereditata [**dalla \_ dipendenza CIM**](cim-dependency.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **Win32 \_ PrinterDriverDll** è derivata dalla [**\_ dipendenza CIM**](cim-dependency.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                      |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                        |
| MOF<br/>                      | <dl> <dt>Win32 \_ Printer. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Dipendenza CIM**](cim-dependency.md)
</dt> <dt>

[Classi hardware del sistema del computer](computer-system-hardware-classes.md)
</dt> </dl>

 

 
