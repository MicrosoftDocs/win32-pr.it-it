---
title: Classe Win32_TSGatewayRADIUSServer
description: Descrive un server Remote Authentication Dial-In User Service (RADIUS), che dispone di un set di criteri di autorizzazione della connessione Servizi Desktop remoto (RD \ 160; CAPs).
ms.assetid: 40254354-f446-4e17-b7ec-649c98dd94f9
ms.tgt_platform: multiple
keywords:
- Classe Win32_TSGatewayRADIUSServer Servizi Desktop remoto
- Classe Win32_TSGatewayRADIUSServer Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_TSGatewayRADIUSServer
- Win32_TSGatewayRADIUSServer.Name
- Win32_TSGatewayRADIUSServer.Priority
- Win32_TSGatewayRADIUSServer.SharedSecret
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4157d89dc942a1c2f8ff7d778f9f8048971902ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476385"
---
# <a name="win32_tsgatewayradiusserver-class"></a>Win32 \_ TSGatewayRADIUSServer (classe)

Viene descritto un server Remote Authentication Dial-In User Service (RADIUS), che dispone di un set di criteri di autorizzazione della connessione Servizi Desktop remoto (RD CAPs).

RADIUS è un protocollo standard del settore utilizzato per trasmettere le informazioni di autenticazione, autorizzazione e configurazione tra un computer server e un server di autenticazione, denominato server RADIUS, con un database in cui sono archiviate le informazioni dell'utente. Per ulteriori informazioni, vedere [protocollo RADIUS](/previous-versions/windows/it-pro/windows-server-2003/cc781821(v=ws.10)).

## <a name="syntax"></a>Sintassi

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayRADIUSServer
{
  string Name;
  uint32 Priority;
  string SharedSecret;
};
```

## <a name="members"></a>Members

La classe **Win32 \_ TSGatewayRADIUSServer** presenta questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La classe **Win32 \_ TSGatewayRADIUSServer** presenta questi metodi.



| Metodo                                                                 | Descrizione                                                                  |
|:-----------------------------------------------------------------------|:-----------------------------------------------------------------------------|
| [**Aggiungere**](win32-tsgatewayradiusserver-add.md)                         | Aggiunge un nuovo server RADIUS.<br/>                                         |
| [**MoveDown**](movedown-win32-tsgatewayradiusserver.md)               | Sposta il server RADIUS una posizione verso il basso nell'ordine di priorità.<br/> |
| [**MoveUp**](moveup-win32-tsgatewayradiusserver.md)                   | Sposta questo server RADIUS una posizione verso l'alto nell'ordine di priorità.<br/>   |
| [**Rimuovi**](win32-tsgatewayradiusserver-remove.md)                   | Rimuove il server RADIUS corrente.<br/>                                |
| [**SetName**](setname-win32-tsgatewayradiusserver.md)                 | Imposta la proprietà **Name** per il server RADIUS.<br/>                |
| [**SetSharedSecret**](setsharedsecret-win32-tsgatewayradiusserver.md) | Imposta la proprietà **SharedSecret** per questo server RADIUS.<br/>        |
| [**Aggiornamento**](update-win32-tsgatewayradiusserver.md)                   | Aggiorna il server RADIUS corrente.<br/>                                |



 

### <a name="properties"></a>Proprietà

La classe **Win32 \_ TSGatewayRADIUSServer** dispone di queste proprietà.

<dl> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nome del server RADIUS. Questa proprietà può essere modificata con il metodo [**Sename**](setname-win32-tsgatewayradiusserver.md) .

</dd> <dt>

**Priorità**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Priorità del server RADIUS. Il server Gateway Desktop remoto cerca i CAPs RD nei server RADIUS in base alla priorità. Questa proprietà può essere modificata con i metodi [**MoveUp**](moveup-win32-tsgatewayradiusserver.md), [**MoveDown**](movedown-win32-tsgatewayradiusserver.md), [**Add**](win32-tsgatewayradiusserver-add.md)e [**Remove**](win32-tsgatewayradiusserver-remove.md) .

</dd> <dt>

**SharedSecret**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Segreto condiviso per il server RADIUS. Questa proprietà può essere modificata con il metodo [**SetSharedSecret**](setsharedsecret-win32-tsgatewayradiusserver.md) .

</dd> </dl>

## <a name="remarks"></a>Commenti

Per utilizzare questa classe, è necessario essere membri del gruppo Administrators.

I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                           |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_TSGatewayConnection Win32**](win32-tsgatewayconnection.md)
</dt> <dt>

[**\_TSGatewayConnectionAuthorizationPolicy Win32**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[**\_TSGatewayLoadBalancer Win32**](win32-tsgatewayloadbalancer.md)
</dt> <dt>

[**\_TSGatewayResourceAuthorizationPolicy Win32**](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[**\_TSGatewayResourceGroup Win32**](win32-tsgatewayresourcegroup.md)
</dt> <dt>

[**\_TSGatewayServerSettings Win32**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

