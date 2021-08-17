---
description: La classe WMI di associazione PrinterDriverDll Win32 mette in relazione \_ una stampante locale e il relativo file di driver.
ms.assetid: decbd1de-8091-47f7-94a1-42862070b920
ms.tgt_platform: multiple
title: Win32_PrinterDriverDll classe
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
ms.openlocfilehash: 884c52e388da62529a2aceb49c68ca888f18e0fd7701e05d951880774c3ed035
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119971861"
---
# <a name="win32_printerdriverdll-class"></a>Classe \_ PrinterDriverDll Win32

La classe [WMI](../wmisdk/retrieving-a-class.md) **di associazione \_ PrinterDriverDll Win32** mette in relazione una stampante locale e il relativo file di driver.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class Win32_PrinterDriverDll : CIM_Dependency
{
  CIM_DataFile  REF Antecedent;
  Win32_Printer REF Dependent;
};
```

## <a name="members"></a>Members

La **classe \_ PrinterDriverDll Win32** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ PrinterDriverDll Win32** ha queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ DataFile**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **Chiave**](../wmisdk/standard-qualifiers.md)
</dt> </dl>

Riferimento [**all'istanza di CIM \_ DataFile**](cim-datafile.md) che rappresenta il file del driver per questa Windows basata su dispositivo.

Questa proprietà viene ereditata dalla [**dipendenza CIM \_**](cim-dependency.md).

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **Stampante Win32 \_**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **Chiave**](../wmisdk/standard-qualifiers.md)
</dt> </dl>

Riferimento [**all'istanza \_ della stampante Win32.**](win32-printer.md)

Questa proprietà viene ereditata dalla [**dipendenza CIM \_**](cim-dependency.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

La **classe \_ PrinterDriverDll Win32** è derivata dalla [**dipendenza \_ CIM**](cim-dependency.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                      |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                        |
| MOF<br/>                      | <dl> <dt>Win32 \_ Printer.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Dipendenza \_ CIM**](cim-dependency.md)
</dt> <dt>

[Classi hardware del sistema informatico](computer-system-hardware-classes.md)
</dt> </dl>

 

 
