---
description: La classe WMI di associazione Win32 OperatingSystemQFE mette in relazione un sistema operativo e gli aggiornamenti del prodotto applicati come \_ rappresentato in Win32 \_ QuickFixEngineering.
ms.assetid: 71985759-7e45-44df-82a9-f9a93e3b923e
ms.tgt_platform: multiple
title: Win32_OperatingSystemQFE classe
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
ms.openlocfilehash: 60fa11faaf7b6d85ce7d3494e1081afc4742b65e27f11fc2cebcd94949373745
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119972351"
---
# <a name="win32_operatingsystemqfe-class"></a>Classe \_ OperatingSystemQFE Win32

La classe [WMI](../wmisdk/retrieving-a-class.md) di associazione **\_ Win32 OperatingSystemQFE** mette in relazione un sistema operativo e gli aggiornamenti del prodotto applicati come rappresentato in [**Win32 \_ QuickFixEngineering**](win32-quickfixengineering.md).

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà e i metodi sono in ordine alfabetico, non in ordine MOF.

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

La **classe \_ OperatingSystemQFE Win32** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Win32 \_ OperatingSystemQFE** ha queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **Win32 \_ OperatingSystem**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key,**](../wmisdk/key-qualifier.md) [**Override**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Wmi \| Win32 \_ OperatingSystem")
</dt> </dl>

Riferimento all'istanza che rappresenta il sistema interessato dall'aggiornamento del prodotto in questa associazione.

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **Win32 \_ QuickFixEngineering**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key,**](../wmisdk/key-qualifier.md) [**Weak,**](../wmisdk/standard-qualifiers.md) [**Override**](../wmisdk/standard-qualifiers.md) ("Dependent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ QuickFixEngineering")
</dt> </dl>

Riferimento all'istanza che rappresenta l'istanza dell'oggetto applicata al sistema operativo in questa associazione.

</dd> </dl>

## <a name="remarks"></a>Commenti

La **classe \_ OperatingSystemQFE Win32** deriva dalla [**dipendenza CIM \_**](cim-dependency.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Dipendenza \_ CIM**](cim-dependency.md)
</dt> <dt>

[Classi del sistema operativo](./operating-system-classes.md)
</dt> </dl>

 

 
