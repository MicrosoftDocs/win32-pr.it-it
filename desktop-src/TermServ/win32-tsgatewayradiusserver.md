---
title: Win32_TSGatewayRADIUSServer classe
description: Descrive un server Remote Authentication Dial-In User Service (RADIUS), che dispone di un set di criteri Servizi Desktop remoto di autorizzazione della connessione (RD \ 160; CAP).
ms.assetid: 40254354-f446-4e17-b7ec-649c98dd94f9
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayRADIUSServer classe Servizi Desktop remoto
- Win32_TSGatewayRADIUSServer classe Servizi Desktop remoto , descritto
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
ms.openlocfilehash: 9997494f9e93980ac4d6e4b1dcb9c95b0d7665a70226f77d1cd4c7ca3ad751d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769841"
---
# <a name="win32_tsgatewayradiusserver-class"></a>Classe \_ Win32 TSGatewayRADIUSServer

Descrive un server Remote Authentication Dial-In User Service (RADIUS), che dispone di un set di criteri di autorizzazione Servizi Desktop remoto connessione remota (CAP).

RADIUS è un protocollo standard del settore usato per trasmettere le informazioni di autenticazione, autorizzazione e configurazione tra un computer server e un server di autenticazione, denominato server RADIUS, con un database che archivia le informazioni utente. Per altre informazioni, vedere [Protocollo RADIUS.](/previous-versions/windows/it-pro/windows-server-2003/cc781821(v=ws.10))

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

La **classe \_ Win32 TSGatewayRADIUSServer** include questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe \_ Win32 TSGatewayRADIUSServer** include questi metodi.



| Metodo                                                                 | Descrizione                                                                  |
|:-----------------------------------------------------------------------|:-----------------------------------------------------------------------------|
| [**Aggiungere**](win32-tsgatewayradiusserver-add.md)                         | Aggiunge un nuovo server RADIUS.<br/>                                         |
| [**MoveDown**](movedown-win32-tsgatewayradiusserver.md)               | Sposta il server RADIUS di una posizione verso il basso nell'ordine di priorità.<br/> |
| [**MoveUp**](moveup-win32-tsgatewayradiusserver.md)                   | Sposta il server RADIUS di una posizione verso l'alto nell'ordine di priorità.<br/>   |
| [**Rimuovi**](win32-tsgatewayradiusserver-remove.md)                   | Rimuove il server RADIUS corrente.<br/>                                |
| [**SetName**](setname-win32-tsgatewayradiusserver.md)                 | Imposta la **proprietà Name** per questo server RADIUS.<br/>                |
| [**SetSharedSecret**](setsharedsecret-win32-tsgatewayradiusserver.md) | Imposta la **proprietà SharedSecret** per questo server RADIUS.<br/>        |
| [**Aggiornamento**](update-win32-tsgatewayradiusserver.md)                   | Aggiorna il server RADIUS corrente.<br/>                                |



 

### <a name="properties"></a>Proprietà

La **classe \_ Win32 TSGatewayRADIUSServer** ha queste proprietà.

<dl> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nome del server RADIUS. Questa proprietà può essere modificata con il [**metodo SetName.**](setname-win32-tsgatewayradiusserver.md)

</dd> <dt>

**Priorità**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Priorità del server RADIUS. Il server Gateway Desktop remoto cerca i criteri di accesso client Desktop remoto nei server RADIUS in base alla priorità. Questa proprietà può essere modificata con [**i metodi MoveUp,**](moveup-win32-tsgatewayradiusserver.md) [**MoveDown,**](movedown-win32-tsgatewayradiusserver.md) [**Add**](win32-tsgatewayradiusserver-add.md) [**e Remove.**](win32-tsgatewayradiusserver-remove.md)

</dd> <dt>

**SharedSecret**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Segreto condiviso per il server RADIUS. Questa proprietà può essere modificata con [**il metodo SetSharedSecret.**](setsharedsecret-win32-tsgatewayradiusserver.md)

</dd> </dl>

## <a name="remarks"></a>Commenti

Per utilizzare questa classe, è necessario essere un membro del gruppo Administrators.

Managed Object Format (MOF) contengono le definizioni per le Windows WMI (Management Instrumentation). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, [vedere Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                           |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Connessione \_ TSGateway Win32**](win32-tsgatewayconnection.md)
</dt> <dt>

[**Win32 \_ TSGatewayConnectionAuthorizationPolicy**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[**Win32 \_ TSGatewayLoadBalancer**](win32-tsgatewayloadbalancer.md)
</dt> <dt>

[**Win32 \_ TSGatewayResourceAuthorizationPolicy**](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[**Win32 \_ TSGatewayResourceGroup**](win32-tsgatewayresourcegroup.md)
</dt> <dt>

[**Win32 \_ TSGatewayServerSettings**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

