---
title: Win32_VirtualDesktopSession classe
description: Gestisce una sessione desktop virtuale.
ms.assetid: a5a0d2a4-6e19-42ac-988c-2d3787946325
ms.tgt_platform: multiple
keywords:
- Win32_VirtualDesktopSession classe Servizi Desktop remoto
- Win32_VirtualDesktopSession classe Servizi Desktop remoto , descritto
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
ms.openlocfilehash: 01e039df658ded4534e3e2582f08ba4e5f5a04530d810349fff5633730a84332
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137424"
---
# <a name="win32_virtualdesktopsession-class"></a>Classe \_ VirtualDesktopSession Win32

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

La **classe \_ VirtualDesktopSession Win32** include questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe \_ VirtualDesktopSession Win32** include questi metodi.



| Metodo                                                         | Descrizione                                                                |
|:---------------------------------------------------------------|:---------------------------------------------------------------------------|
| [**Disconnetti**](disconnect-win32-virtualdesktopsession.md)   | Disconnette la sessione desktop virtuale.<br/>                        |
| [**Disconnessione**](logoff-win32-virtualdesktopsession.md)           | Disconnette l'utente dalla sessione desktop virtuale.<br/>             |
| [**SendMessage**](sendmessage-win32-virtualdesktopsession.md) | Inviare un messaggio all'utente tramite la sessione desktop virtuale.<br/> |



 

### <a name="properties"></a>Proprietà

La **classe \_ VirtualDesktopSession Win32** ha queste proprietà.

<dl> <dt>

**ClientMachineName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene il nome del computer client connesso alla sessione.

</dd> <dt>

**CollectionId**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene il nome dell'insieme di desktop virtuali che ospita la macchina virtuale.

</dd> <dt>

**ConnectState**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene lo stato della connessione alla sessione.

</dd> <dt>

**Domainname**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene il nome di dominio dell'utente.

</dd> <dt>

**SessionId**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Ottiene l'ID della sessione desktop virtuale.

</dd> <dt>

**UserName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene il nome dell'account utente assegnato alla sessione.

</dd> <dt>

**VMHostName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Ottiene il nome del server Desktop remoto host di virtualizzazione che ospita la macchina virtuale.

</dd> <dt>

**VMName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
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
| Spazio dei nomi<br/>                | Radice \\ cimv2 \\ rdms<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[provider Desktop remoto Management Services](rdms-api-reference.md)
</dt> </dl>

 

