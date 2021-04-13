---
title: Classe Win32_SessionDirectorySession
description: Fornisce le proprietà per la visualizzazione delle proprietà di una sessione di gestore connessione Desktop remoto (Connessione Desktop remoto Broker).
ms.assetid: 34b5a898-3952-493c-ba62-dd0d298b0600
ms.tgt_platform: multiple
keywords:
- Classe Win32_SessionDirectorySession Servizi Desktop remoto
- Classe Win32_SessionDirectorySession Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_SessionDirectorySession
- Win32_SessionDirectorySession.ServerName
- Win32_SessionDirectorySession.SessionID
- Win32_SessionDirectorySession.UserName
- Win32_SessionDirectorySession.DomainName
- Win32_SessionDirectorySession.ServerIPAddress
- Win32_SessionDirectorySession.TSProtocol
- Win32_SessionDirectorySession.ApplicationType
- Win32_SessionDirectorySession.ResolutionWidth
- Win32_SessionDirectorySession.ResolutionHeight
- Win32_SessionDirectorySession.ColorDepth
- Win32_SessionDirectorySession.CreateTime
- Win32_SessionDirectorySession.DisconnectTime
- Win32_SessionDirectorySession.SessionState
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fba8fdbdffc764c3bdcc1a8f5bc53aa479f318d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400369"
---
# <a name="win32_sessiondirectorysession-class"></a>Win32 \_ SessionDirectorySession (classe)

Fornisce le proprietà per la visualizzazione delle proprietà di una sessione di gestore connessione Desktop remoto (Connessione Desktop remoto Broker).

> [!Note]  
> In Windows Server 2008 R2 il nome di gestore sessioni Servizi terminal è stato modificato in Gestore connessione Desktop remoto. Queste proprietà si applicano a tutti i sistemi operativi supportati se non diversamente specificato.

 

## <a name="syntax"></a>Sintassi

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONDIRECTORYSESSION_Prov"), AMENDMENT]
class Win32_SessionDirectorySession
{
  string   ServerName;
  uint32   SessionID;
  string   UserName;
  string   DomainName;
  string   ServerIPAddress;
  uint32   TSProtocol;
  string   ApplicationType;
  uint32   ResolutionWidth;
  uint32   ResolutionHeight;
  uint32   ColorDepth;
  DateTime CreateTime;
  DateTime DisconnectTime;
  uint32   SessionState;
};
```

## <a name="members"></a>Members

La classe **Win32 \_ SessionDirectorySession** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **Win32 \_ SessionDirectorySession** dispone di queste proprietà.

<dl> <dt>

**ApplicationType**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Applicazione avviata con questa sessione. Corrisponde alla proprietà **StartProgram** di [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md).

</dd> <dt>

**ColorDepth**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Profondità di colore della sessione, misurata in bit per pixel.

</dd> <dt>

**CreateTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Data e ora di creazione della sessione. Questo valore non viene reimpostato quando una sessione viene disconnessa e riconnessa.

</dd> <dt>

**DisconnectTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Data e ora in cui la sessione è stata disconnessa (se applicabile).

</dd> <dt>

**NomeDominio**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome di dominio dell'utente connesso a questa sessione.

</dd> <dt>

**ResolutionHeight**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Altezza della sessione, in pixel, per questa sessione.

</dd> <dt>

**ResolutionWidth**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Larghezza della sessione, in pixel, per questa sessione.

</dd> <dt>

**ServerIPAddress**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indirizzo IP del server Gestore connessione Desktop remoto per questa sessione.

</dd> <dt>

**ServerName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nome del server Gestore connessione Desktop remoto per la sessione.

</dd> <dt>

**SessionID**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

ID sessione per questa sessione.

</dd> <dt>

**SessionState**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stato della sessione.

<dt>

0
</dt> <dd>

La sessione è attiva.

</dd> <dt>

1
</dt> <dd>

La sessione è disconnessa.

</dd> </dl>

</dd> <dt>

**TSProtocol**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Protocollo per questa sessione.

<dt>

0
</dt> <dd>

Questa sessione è in esecuzione su una console fisica.

</dd> <dt>

1
</dt> <dd>

Per questa sessione viene usato un protocollo di terze parti proprietario.

</dd> <dt>

2
</dt> <dd>

Per questa sessione viene usato Remote Desktop Protocol (RDP).

</dd> </dl>

</dd> <dt>

**UserName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome utente dell'utente che ha effettuato l'accesso a questa sessione.

</dd> </dl>

## <a name="remarks"></a>Commenti

I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                              |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                         |
| Spazio dei nomi<br/>                | Root\\CIMv2<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>TssdWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_SessionDirectoryCluster Win32**](win32-sessiondirectorycluster.md)
</dt> <dt>

[**\_SessionDirectoryServer Win32**](win32-sessiondirectoryserver.md)
</dt> </dl>

 

