---
title: Classe Win32_TSGatewayConnection
description: Rappresenta una connessione da un computer client a un server Gateway Desktop remoto di Desktop remoto.
ms.assetid: 6e76ae25-409d-436a-8eef-8f047194c29c
ms.tgt_platform: multiple
keywords:
- Classe Win32_TSGatewayConnection Servizi Desktop remoto
- Classe Win32_TSGatewayConnection Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnection
- Win32_TSGatewayConnection.ConnectionKey
- Win32_TSGatewayConnection.TunnelId
- Win32_TSGatewayConnection.ChannelId
- Win32_TSGatewayConnection.UserName
- Win32_TSGatewayConnection.FullUserName
- Win32_TSGatewayConnection.ClientAddress
- Win32_TSGatewayConnection.ConnectedTime
- Win32_TSGatewayConnection.IdleTime
- Win32_TSGatewayConnection.ConnectedResource
- Win32_TSGatewayConnection.ProtocolName
- Win32_TSGatewayConnection.ConnectedPort
- Win32_TSGatewayConnection.NumberOfKilobytesSent
- Win32_TSGatewayConnection.NumberOfKilobytesReceived
- Win32_TSGatewayConnection.ConnectionDuration
- Win32_TSGatewayConnection.TransportProtocol
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6dbaa79213282a70b2f29e6bee9f94901700dddf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121206"
---
# <a name="win32_tsgatewayconnection-class"></a>Win32 \_ TSGatewayConnection (classe)

Rappresenta una connessione da un computer client a un server Gateway Desktop remoto di Desktop remoto.

## <a name="syntax"></a>Sintassi

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayConnection
{
  string ConnectionKey;
  uint64 TunnelId;
  uint32 ChannelId;
  string UserName;
  string FullUserName;
  string ClientAddress;
  string ConnectedTime;
  string IdleTime;
  string ConnectedResource;
  string ProtocolName;
  uint32 ConnectedPort;
  uint64 NumberOfKilobytesSent;
  uint64 NumberOfKilobytesReceived;
  string ConnectionDuration;
  uint32 TransportProtocol;
};
```

## <a name="members"></a>Members

La classe **Win32 \_ TSGatewayConnection** presenta questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La classe **Win32 \_ TSGatewayConnection** presenta questi metodi.



| Metodo                                                                     | Descrizione                                                                                                                      |
|:---------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------|
| [**CheckStatus**](checkstatus-win32-tsgatewayconnection.md)               | Controlla lo stato di una connessione al server Gateway Desktop remoto e indica se il server di destinazione è configurato per il bilanciamento del carico.<br/> |
| [**Disconnetti**](disconnect-win32-tsgatewayconnection.md)                 | Termina la connessione.<br/>                                                                                                  |
| [**DisconnectProtocol**](disconnectprotocol-win32-tsgatewayconnection.md) | Termina tutte le connessioni che utilizzano il protocollo specificato.<br/>                                                                 |
| [**DisconnectUser**](disconnectuser-win32-tsgatewayconnection.md)         | Termina tutte le connessioni dell'utente specificato.<br/>                                                                           |



 

### <a name="properties"></a>Proprietà

La classe **Win32 \_ TSGatewayConnection** dispone di queste proprietà.

<dl> <dt>

**ChannelId**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Identificatore del canale.

</dd> <dt>

**ClientAddress**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indirizzo IP del client.

</dd> <dt>

**ConnectedPort**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Porta sulla risorsa connessa a cui è connesso l'utente.

</dd> <dt>

**ConnectedResource**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome del computer (o cluster) a cui è connesso il client.

</dd> <dt>

**ConnectedTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Timestamp relativo al momento in cui è stata stabilita la connessione. Questa volta viene reimpostato quando la connessione viene reimpostata, anche se viene riconnessa automaticamente.

</dd> <dt>

**ConnectionDuration**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tempo trascorso dall'ora di connessione.

</dd> <dt>

**ConnectionKey**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identificatore di connessione nel formato "tunnelId: channelID".

</dd> <dt>

**FullUserName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome utente completo dell'utente connesso.

</dd> <dt>

**Tempoinattività**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tempo di inattività della connessione.

</dd> <dt>

**NumberOfKilobytesReceived**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di kilobyte ricevuti dal computer client dal server Gateway Desktop remoto.

</dd> <dt>

**NumberOfKilobytesSent**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di kilobyte inviati al computer client dal server Gateway Desktop remoto.

</dd> <dt>

**ProtocolName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Protocollo utilizzato per la connessione al server Gateway Desktop remoto.

<dt>

RDP
</dt> <dd>

Protocollo per il server Gateway Desktop remoto.

</dd> </dl>

</dd> <dt>

**TransportProtocol**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica il tipo di trasporto per la connessione. Deve essere uno dei valori seguenti.

<dt>

0
</dt> <dd>

RPC sul trasporto HTTP.

</dd> <dt>

1
</dt> <dd>

Trasporto HTTP.

</dd> <dt>

2
</dt> <dd>

Trasporto UDP.

</dd> </dl>

</dd> <dt>

**TunnelId**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Identificatore del tunnel.

</dd> <dt>

**UserName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome utente connesso al server Gateway Desktop remoto.

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

[**\_TSGatewayConnectionAuthorizationPolicy Win32**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[**\_TSGatewayLoadBalancer Win32**](win32-tsgatewayloadbalancer.md)
</dt> <dt>

[**\_TSGatewayRADIUSServer Win32**](win32-tsgatewayradiusserver.md)
</dt> <dt>

[**\_TSGatewayResourceAuthorizationPolicy Win32**](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[**\_TSGatewayResourceGroup Win32**](win32-tsgatewayresourcegroup.md)
</dt> <dt>

[**\_TSGatewayServerSettings Win32**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

