---
title: Classe Win32_SessionBrokerTarget
description: Definisce la query per una destinazione di Service Broker di sessione.
ms.assetid: 35de25da-cb89-4836-be14-9544b1264248
ms.tgt_platform: multiple
keywords:
- Classe Win32_SessionBrokerTarget Servizi Desktop remoto
- Classe Win32_SessionBrokerTarget Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_SessionBrokerTarget
- Win32_SessionBrokerTarget.PluginName
- Win32_SessionBrokerTarget.TargetName
- Win32_SessionBrokerTarget.FarmName
- Win32_SessionBrokerTarget.Guid
- Win32_SessionBrokerTarget.Environment
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16ceca0df64eeb9cd285737fee7c6ca6fa3a2e63
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874530"
---
# <a name="win32_sessionbrokertarget-class"></a>Win32 \_ SessionBrokerTarget (classe)

Definisce la query per una destinazione di Service Broker di sessione.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONBROKERTARGET_Prov"), AMENDMENT]
class Win32_SessionBrokerTarget
{
  string PluginName;
  string TargetName;
  string FarmName;
  string Guid;
  string Environment;
};
```

## <a name="members"></a>Members

La classe **Win32 \_ SessionBrokerTarget** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **Win32 \_ SessionBrokerTarget** dispone di queste proprietà.

<dl> <dt>

**Environment**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome dell'ambiente. Nel caso di una macchina virtuale (VM) destinazione, potrebbe essere il nome host della VM.

</dd> <dt>

**Farmname**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome della farm a cui appartiene la destinazione.

</dd> <dt>

**GUID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Il GUID (se presente) della destinazione.

</dd> <dt>

**PluginName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nome del plug-in.

</dd> <dt>

**TargetName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome della destinazione.

</dd> </dl>

## <a name="examples"></a>Esempio

Nella stringa di query seguente viene illustrato il modo in cui la \_ classe Win32 SessionBrokerTarget viene utilizzata in una query.


```CSharp
queryString = string.Format("SELECT * FROM Win32_SessionBrokerTarget WHERE PluginName = '{0}'", pluginName);
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                              |
| Server minimo supportato<br/> | Windows Server 2008 R2<br/>                                                      |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                               |
| MOF<br/>                      | <dl> <dt>TssdWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



 

