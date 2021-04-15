---
title: Classe Win32_VirtualDesktopSession
description: Gestisce una sessione desktop virtuale.
ms.assetid: a5a0d2a4-6e19-42ac-988c-2d3787946325
ms.tgt_platform: multiple
keywords:
- Classe Win32_VirtualDesktopSession Servizi Desktop remoto
- Classe Win32_VirtualDesktopSession Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_VirtualDesktopSession
- Win32_VirtualDesktopSession.VMHostName
- Win32_VirtualDesktopSession.SessionId
- Win32_VirtualDesktopSession.VMName
- Win32_VirtualDesktopSession.ConnectState
- Win32_VirtualDesktopSession.UserName
- Win32_VirtualDesktopSession.DomainName
- Win32_VirtualDesktopSession.CollectionId
- Win32_VirtualDesktopSession.ClientMachineName
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f343c1dc022dcb4759f813de956ade27e1aff213
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475449"
---
# <a name="win32_virtualdesktopsession-class"></a>Win32 \_ VirtualDesktopSession (classe)

Gestisce una sessione desktop virtuale.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_VirtualDesktopSession
{
  string VMHostName;
  uint32 SessionId;
  string VMName;
  uint32 ConnectState;
  string UserName;
  string DomainName;
  string CollectionId;
  string ClientMachineName;
};
```

## <a name="members"></a>Members

La classe **Win32 \_ VirtualDesktopSession** presenta questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La classe **Win32 \_ VirtualDesktopSession** presenta questi metodi.



| Metodo                                                         | Descrizione                                                                |
|:---------------------------------------------------------------|:---------------------------------------------------------------------------|
| [**Disconnetti**](disconnect-win32-virtualdesktopsession.md)   | Disconnette la sessione desktop virtuale.<br/>                        |
| [**Disconnessione**](logoff-win32-virtualdesktopsession.md)           | Disconnette l'utente dalla sessione desktop virtuale.<br/>             |
| [**SendMessage**](sendmessage-win32-virtualdesktopsession.md) | Inviare un messaggio all'utente tramite la sessione desktop virtuale.<br/> |



 

### <a name="properties"></a>Proprietà

La classe **Win32 \_ VirtualDesktopSession** dispone di queste proprietà.

<dl> <dt>

**ClientMachineName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene il nome del computer client connesso alla sessione.

</dd> <dt>

**CollectionId**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene il nome dell'insieme di desktop virtuali che ospita la macchina virtuale.

</dd> <dt>

**ConnectState**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene lo stato della connessione alla sessione.

</dd> <dt>

**NomeDominio**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene il nome di dominio dell'utente.

</dd> <dt>

**SessionId**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Ottiene l'ID della sessione desktop virtuale.

</dd> <dt>

**UserName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene il nome dell'account utente assegnato alla sessione.

</dd> <dt>

**VMHostName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Ottiene il nome del server host di virtualizzazione Desktop remoto che ospita la macchina virtuale.

</dd> <dt>

**VMName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene il nome della macchina virtuale assegnata alla sessione.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                   |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                              |
| Spazio dei nomi<br/>                | Radice \\ CIMV2 \\ RDBMS<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Provider di Desktop remoto Management Services](rdms-api-reference.md)
</dt> </dl>

 

