---
title: Win32_TSVirtualDesktopServerSettings classe
description: Contiene informazioni di configurazione per Desktop remoto server Host di virtualizzazione Desktop remoto.
ms.assetid: 749018aa-a8aa-433e-985b-40b44ef8aa7f
ms.tgt_platform: multiple
keywords:
- Win32_TSVirtualDesktopServerSettings classe Servizi Desktop remoto
- Win32_TSVirtualDesktopServerSettings classe Servizi Desktop remoto , descritto
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
ms.openlocfilehash: f40e7d51ee0c92e50afca023629bb92de9f506b3e47ee9e520aa16c09640375b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137464"
---
# <a name="win32_tsvirtualdesktopserversettings-class"></a>Classe \_ Win32 TSVirtualDesktopServerSettings

Contiene informazioni di configurazione per Desktop remoto server Host di virtualizzazione Desktop remoto.

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

La **classe \_ Win32 TSVirtualDesktopServerSettings** include questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ Win32 TSVirtualDesktopServerSettings** ha queste proprietà.

<dl> <dt>

**Concorrenza**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Numero massimo di richieste di provisioning simultanee consentite per questo server Desktop virtuale.

</dd> <dt>

**PolicySourceSessionBrokerName**
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se impostato su 0, indica che la **proprietà SessionBrokerName** è configurata dal server. Se impostato su 1, indica che la **proprietà SessionBrokerName** è configurata da criteri di gruppo.

</dd> <dt>

**SessionBrokerName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Nome distinto completo del broker di sessione per il server Host di virtualizzazione Desktop remoto.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                  |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                             |
| Spazio dei nomi<br/>                | Radice \\ CIMV2 \\ TerminalServices<br/>                                                   |
| MOF<br/>                      | <dl> <dt>TSVmHost.mof</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>TSVmHostWmi.dll</dt> </dl> |



 

 





