---
title: Classe Win32_SessionDirectoryServer
description: Fornisce le proprietà per la visualizzazione delle proprietà di un server Gestore connessione Desktop remoto (Connessione Desktop remoto Broker).
ms.assetid: 73017b71-eff9-4ef6-aba0-71ddb969491f
ms.tgt_platform: multiple
keywords:
- Classe Win32_SessionDirectoryServer Servizi Desktop remoto
- Classe Win32_SessionDirectoryServer Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryServer
- Win32_SessionDirectoryServer.ServerName
- Win32_SessionDirectoryServer.ServerIPAddress
- Win32_SessionDirectoryServer.ClusterName
- Win32_SessionDirectoryServer.NumberOfSessions
- Win32_SessionDirectoryServer.SingleSessionMode
- Win32_SessionDirectoryServer.ServerWeight
- Win32_SessionDirectoryServer.NumPendRedir
- Win32_SessionDirectoryServer.LoadIndicator
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9e96efb19e4db56e582cd44d05f3e9865e5282c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964077"
---
# <a name="win32_sessiondirectoryserver-class"></a>Win32 \_ SessionDirectoryServer (classe)

Fornisce le proprietà per la visualizzazione delle proprietà di un server Gestore connessione Desktop remoto (Connessione Desktop remoto Broker).

> [!Note]  
> In Windows Server 2008 R2 il nome di gestore sessioni Servizi terminal è stato modificato in Gestore connessione Desktop remoto. Queste proprietà si applicano a tutti i sistemi operativi supportati se non diversamente specificato.

 

## <a name="syntax"></a>Sintassi

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONDIRECTORYSERVER_Prov"), AMENDMENT]
class Win32_SessionDirectoryServer
{
  string ServerName;
  string ServerIPAddress;
  string ClusterName;
  uint32 NumberOfSessions;
  uint32 SingleSessionMode;
  uint32 ServerWeight;
  uint32 NumPendRedir;
  uint32 LoadIndicator;
};
```

## <a name="members"></a>Members

La classe **Win32 \_ SessionDirectoryServer** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **Win32 \_ SessionDirectoryServer** dispone di queste proprietà.

<dl> <dt>

**ClusterName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome della farm che include il server.

</dd> <dt>

**LoadIndicator**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero relativo che rappresenta il carico del server Host sessione Desktop remoto quando viene utilizzato l'algoritmo di bilanciamento del carico predefinito. Il valore della proprietà *LoadIndicator* è basato sul numero di sessioni, sul numero di richieste di reindirizzamento in sospeso e sul valore del peso del server.

</dd> <dt>

**NumberOfSessions**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di sessioni nel server Gestore connessione Desktop remoto.

</dd> <dt>

**NumPendRedir**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di richieste di reindirizzamento in sospeso.

</dd> <dt>

**ServerIPAddress**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indirizzo IP del server Gestore connessione Desktop remoto. Se il server è configurato per gli indirizzi IPv4 e IPv6, questo conterrà l'indirizzo IPv4.

</dd> <dt>

**ServerName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nome del server Gestore connessione Desktop remoto.

</dd> <dt>

**ServerWeight**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Valore del peso del server, usato per il bilanciamento del carico.

</dd> <dt>

**SingleSessionMode**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Impostazione della modalità sessione singola del server Gestore connessione Desktop remoto.

<dt>

0
</dt> <dd>

La farm non è in modalità sessione singola.

</dd> <dt>

1
</dt> <dd>

La farm in è in modalità sessione singola.

</dd> </dl>

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

[**\_SessionDirectorySession Win32**](win32-sessiondirectorysession.md)
</dt> </dl>

 

