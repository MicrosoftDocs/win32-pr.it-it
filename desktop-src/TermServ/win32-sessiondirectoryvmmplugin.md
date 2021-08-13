---
title: Win32_SessionDirectoryVMMPlugin classe
description: Rappresenta un plug-in virtual machine manager (VMM) registrato con un broker di sessione.
ms.assetid: b5c5deb1-6c1b-4547-a24a-db3ce6654144
ms.tgt_platform: multiple
keywords:
- Win32_SessionDirectoryVMMPlugin classe Servizi Desktop remoto
- Win32_SessionDirectoryVMMPlugin classe Servizi Desktop remoto , descritto
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin
- Win32_SessionDirectoryVMMPlugin.sName
- Win32_SessionDirectoryVMMPlugin.sProvider
- Win32_SessionDirectoryVMMPlugin.sClassID
- Win32_SessionDirectoryVMMPlugin.sServiceLocation
- Win32_SessionDirectoryVMMPlugin.Priority
- Win32_SessionDirectoryVMMPlugin.Enabled
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7481022951664b49b912b854e96e2d30895b0716ee67b6eb01ce1a9f1b1561ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119422361"
---
# <a name="win32_sessiondirectoryvmmplugin-class"></a>Classe \_ Win32 SessionDirectoryVMMPlugin

Rappresenta un plug-in virtual machine manager (VMM) registrato con un broker di sessione.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONDIRECTORYVMMPLUGIN_Prov"), AMENDMENT]
class Win32_SessionDirectoryVMMPlugin
{
  string  sName;
  string  sProvider;
  string  sClassID;
  string  sServiceLocation;
  sint32  Priority = 0;
  boolean Enabled = FALSE;
};
```

## <a name="members"></a>Members

La **classe Win32 \_ SessionDirectoryVMMPlugin** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe Win32 \_ SessionDirectoryVMMPlugin** include questi metodi.



| Metodo                                                                             | Descrizione                                                   |
|:-----------------------------------------------------------------------------------|:--------------------------------------------------------------|
| [**GetCurrentVMMPlugin**](getcurrentvmmplugin-win32-sessiondirectoryvmmplugin.md) | Ottiene il plug-in con priorità più alta abilitato.<br/> |
| [**RegisterVMMPlugin**](registervmmplugin-win32-sessiondirectoryvmmplugin.md)     | Registra un nuovo plug-in VMM.<br/>                       |
| [**SetEnabled**](setenabled-win32-sessiondirectoryvmmplugin.md)                   | Abilita o disabilita il plug-in.<br/>                   |
| [**SetName**](setname-win32-sessiondirectoryvmmplugin.md)                         | Imposta il nome del plug-in.<br/>                      |
| [**SetPriority**](setpriority-win32-sessiondirectoryvmmplugin.md)                 | Imposta la priorità del plug-in.<br/>                  |
| [**SetProvider**](setprovider-win32-sessiondirectoryvmmplugin.md)                 | Imposta il nome del provider del plug-in.<br/>             |
| [**SetServiceLocation**](setservicelocation-win32-sessiondirectoryvmmplugin.md)   | Imposta il percorso del servizio del plug-in.<br/>          |
| [**Annulla registrazioneVMMPlugin**](unregistervmmplugin-win32-sessiondirectoryvmmplugin.md) | Annulla la registrazione del plug-in.<br/>                           |



 

### <a name="properties"></a>Proprietà

La **classe Win32 \_ SessionDirectoryVMMPlugin** ha queste proprietà.

<dl> <dt>

**Enabled**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se il plug-in è abilitato o disabilitato. **True** se il plug-in è abilitato o false in **caso contrario.** Il plug-in è disabilitato per impostazione predefinita.

</dd> <dt>

**Priorità**
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Priorità del plug-in. Maggiore è il valore, maggiore è la priorità del plug-in. La priorità è zero per impostazione predefinita.

</dd> <dt>

**sClassID**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Identificatore di classe del plug-in.

</dd> <dt>

**sName**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome del plug-in.

</dd> <dt>

**sProvider**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome del provider di plug-in.

</dd> <dt>

**sServiceLocation**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Percorso del servizio che il plug-in deve contattare.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                              |
| Server minimo supportato<br/> | Windows Server 2008 R2<br/>                                                      |
| Spazio dei nomi<br/>                | TerminalServices \\ CIMv2 \\ radice<br/>                                               |
| MOF<br/>                      | <dl> <dt>TssdWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



 

