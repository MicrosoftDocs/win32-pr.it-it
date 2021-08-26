---
description: La classe WMI di associazione Win32 ComClassAutoEmulator mette in relazione una classe COMPONENT OBJECT MODEL (COM) e un'altra classe \_ COM emulata automaticamente.
ms.assetid: e060ba26-98e7-47cb-bf21-1ca80d0e8a07
ms.tgt_platform: multiple
title: Win32_ComClassAutoEmulator classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComClassAutoEmulator
- Win32_ComClassAutoEmulator.NewVersion
- Win32_ComClassAutoEmulator.OldVersion
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ba849eed744ff342cfde10d0f31072d4e898cf52cf4e6966760f780236c56df4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986381"
---
# <a name="win32_comclassautoemulator-class"></a>Classe \_ ComClassAutoEmulator Win32

La classe [WMI](/windows/desktop/WmiSdk/retrieving-a-class) di associazione **\_ Win32 ComClassAutoEmulator** mette in relazione una classe COMPONENT OBJECT MODEL (COM) e un'altra classe COM emulata automaticamente.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Association, Dynamic, Provider("CIMWin32"), UUID("{0F73ED5D-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_ComClassAutoEmulator
{
  Win32_ClassicCOMClass REF NewVersion;
  Win32_ClassicCOMClass REF OldVersion;
};
```

## <a name="members"></a>Members

La **classe Win32 \_ ComClassAutoEmulator** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Win32 \_ ComClassAutoEmulator** ha queste proprietà.

<dl> <dt>

**NewVersion**
</dt> <dd> <dl> <dt>

Tipo di dati: **Win32 \_ ClassicCOMClass**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ ClassicCOMClass")
</dt> </dl>

Riferimento all'istanza che rappresenta il componente COM che può emulare automaticamente il componente COM associato. Queste informazioni vengono ottenute tramite la voce del Registro di sistema AutoTreatAs.

</dd> <dt>

**OldVersion**
</dt> <dd> <dl> <dt>

Tipo di dati: **Win32 \_ ClassicCOMClass**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ ClassicCOMClass")
</dt> </dl>

Riferimento all'istanza che rappresenta il componente COM emulato automaticamente da un altro componente.

</dd> </dl>

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

[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

