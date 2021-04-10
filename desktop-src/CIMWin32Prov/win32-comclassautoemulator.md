---
description: La \_ classe WMI dell'associazione ComClassAutoEmulator Win32 mette in correlazione una classe Component Object Model (com) e un'altra classe com che emula automaticamente.
ms.assetid: e060ba26-98e7-47cb-bf21-1ca80d0e8a07
ms.tgt_platform: multiple
title: Classe Win32_ComClassAutoEmulator
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
ms.openlocfilehash: 9442036d43859caa5fa277109c7e85553e7d42f0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127346"
---
# <a name="win32_comclassautoemulator-class"></a>Win32 \_ ComClassAutoEmulator (classe)

La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) dell'associazione **\_ ComClassAutoEmulator Win32** mette in correlazione una classe Component Object Model (com) e un'altra classe com che emula automaticamente.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

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

La classe **Win32 \_ ComClassAutoEmulator** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **Win32 \_ ComClassAutoEmulator** dispone di queste proprietà.

<dl> <dt>

**NewVersion**
</dt> <dd> <dl> <dt>

Tipo di dati: **Win32 \_ ClassicCOMClass**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ ClassicCOMClass")
</dt> </dl>

Riferimento all'istanza che rappresenta il componente COM in grado di emulare automaticamente il componente COM associato. Queste informazioni vengono ottenute tramite la voce del registro di sistema autotreats.

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
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

