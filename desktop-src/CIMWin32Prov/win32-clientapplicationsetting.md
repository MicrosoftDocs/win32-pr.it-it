---
description: La classe WMI di associazione Win32 ClientApplicationSetting mette in relazione un file eseguibile e un'applicazione Component Object Model (COM) che contiene le opzioni di configurazione COM per \_ il file eseguibile.
ms.assetid: c43d80ee-0f29-4452-b51f-f18543bc1d35
ms.tgt_platform: multiple
title: Win32_ClientApplicationSetting classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ClientApplicationSetting
- Win32_ClientApplicationSetting.Application
- Win32_ClientApplicationSetting.Client
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 359478d7cf6069e17ae02358f4ea48ffc44169f6822f4f8b3e33dad332fab020
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119546371"
---
# <a name="win32_clientapplicationsetting-class"></a>Classe ClientApplicationSetting Win32 \_

La classe [WMI](/windows/desktop/WmiSdk/retrieving-a-class) di associazione **\_ Win32 ClientApplicationSetting** mette in relazione un file eseguibile e un'applicazione Component Object Model (COM) che contiene le opzioni di configurazione COM per il file eseguibile.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Association, Dynamic, Provider("CIMWin32"), UUID("{0F73ED5E-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_ClientApplicationSetting
{
  Win32_DCOMApplication REF Application;
  CIM_DataFile          REF Client;
};
```

## <a name="members"></a>Members

La **classe Win32 \_ ClientApplicationSetting** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Win32 \_ ClientApplicationSetting** ha queste proprietà.

<dl> <dt>

**Applicazione**
</dt> <dd> <dl> <dt>

Tipo di dati: **Win32 \_ DCOMApplication**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ DCOMApplication")
</dt> </dl>

Riferimento all'istanza di che rappresenta l'applicazione COM che contiene le opzioni di configurazione del file eseguibile.

</dd> <dt>

**Client**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ DataFile**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) \| ("CIM CIM \_ DataFile")
</dt> </dl>

Riferimento all'istanza di che rappresenta il file eseguibile che utilizza le impostazioni COM.

</dd> </dl>

## <a name="remarks"></a>Commenti

**Win32 \_ ClientApplicationSetting non** supporta l'enumerazione.

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

 

