---
title: Classe Win32_TSVirtualDesktopServerSettings
description: Contiene informazioni di configurazione per un server di Host di virtualizzazione Desktop remoto (host di virtualizzazione Desktop remoto).
ms.assetid: 749018aa-a8aa-433e-985b-40b44ef8aa7f
ms.tgt_platform: multiple
keywords:
- Classe Win32_TSVirtualDesktopServerSettings Servizi Desktop remoto
- Classe Win32_TSVirtualDesktopServerSettings Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_TSVirtualDesktopServerSettings
- Win32_TSVirtualDesktopServerSettings.SessionBrokerName
- Win32_TSVirtualDesktopServerSettings.PolicySourceSessionBrokerName
- Win32_TSVirtualDesktopServerSettings.Concurrency
api_location:
- TSVmHostWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c39635aee7b32430ace0ead0e3b007051a3c049d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743266"
---
# <a name="win32_tsvirtualdesktopserversettings-class"></a>Win32 \_ TSVirtualDesktopServerSettings (classe)

Contiene informazioni di configurazione per un server di Host di virtualizzazione Desktop remoto (host di virtualizzazione Desktop remoto).

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[singleton, dynamic, provider("Win32_TSVmHost_Prov"), AMENDMENT]
class Win32_TSVirtualDesktopServerSettings
{
  string SessionBrokerName;
  sint32 PolicySourceSessionBrokerName;
  uint32 Concurrency;
};
```

## <a name="members"></a>Members

La classe **Win32 \_ TSVirtualDesktopServerSettings** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **Win32 \_ TSVirtualDesktopServerSettings** dispone di queste proprietà.

<dl> <dt>

**Concorrenza**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Il numero massimo consentito di richieste di provisioning simultanee per questo server desktop virtuale.

</dd> <dt>

**PolicySourceSessionBrokerName**
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se impostato su 0, indica che la proprietà **SessionBrokerName** è configurata dal server. Se impostato su 1, indica che la proprietà **SessionBrokerName** è configurata da criteri di gruppo.

</dd> <dt>

**SessionBrokerName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Nome distinto completo del broker di sessione per il server host di virtualizzazione Desktop remoto.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                  |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                             |
| Spazio dei nomi<br/>                | Radice \\ CIMV2 \\ TerminalServices<br/>                                                   |
| MOF<br/>                      | <dl> <dt>TSVmHost. mof</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>TSVmHostWmi.dll</dt> </dl> |



 

 





