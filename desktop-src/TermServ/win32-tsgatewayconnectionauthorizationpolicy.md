---
title: Win32_TSGatewayConnectionAuthorizationPolicy classe
description: Descrive un criterio Desktop remoto di autorizzazione della connessione (Rd \ 160; CAP). RD \ 160; I CAP vengono usati per determinare se un utente è autorizzato a connettersi al server Desktop remoto Gateway Desktop remoto.
ms.assetid: 50ff3f97-0818-4e9c-9db7-a822cfed0e82
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayConnectionAuthorizationPolicy classe Servizi Desktop remoto
- Win32_TSGatewayConnectionAuthorizationPolicy classe Servizi Desktop remoto , descritto
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy
- Win32_TSGatewayConnectionAuthorizationPolicy.Name
- Win32_TSGatewayConnectionAuthorizationPolicy.Order
- Win32_TSGatewayConnectionAuthorizationPolicy.SmartcardAllowed
- Win32_TSGatewayConnectionAuthorizationPolicy.PasswordAllowed
- Win32_TSGatewayConnectionAuthorizationPolicy.SecureIdAllowed
- Win32_TSGatewayConnectionAuthorizationPolicy.CookieAuthenticationAllowed
- Win32_TSGatewayConnectionAuthorizationPolicy.Enabled
- Win32_TSGatewayConnectionAuthorizationPolicy.IdleTimeout
- Win32_TSGatewayConnectionAuthorizationPolicy.SessionTimeout
- Win32_TSGatewayConnectionAuthorizationPolicy.SessionTimeoutAction
- Win32_TSGatewayConnectionAuthorizationPolicy.DeviceRedirectionType
- Win32_TSGatewayConnectionAuthorizationPolicy.DiskDrivesDisabled
- Win32_TSGatewayConnectionAuthorizationPolicy.PrintersDisabled
- Win32_TSGatewayConnectionAuthorizationPolicy.SerialPortsDisabled
- Win32_TSGatewayConnectionAuthorizationPolicy.ClipboardDisabled
- Win32_TSGatewayConnectionAuthorizationPolicy.PlugAndPlayDevicesDisabled
- Win32_TSGatewayConnectionAuthorizationPolicy.UserGroupNames
- Win32_TSGatewayConnectionAuthorizationPolicy.ComputerGroupNames
- Win32_TSGatewayConnectionAuthorizationPolicy.HasNapAttributes
- Win32_TSGatewayConnectionAuthorizationPolicy.AllowOnlySDRServers
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bfaefb0a3062db27622afe90023928507c6d127c64edb60041347f73c1b261c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118349246"
---
# <a name="win32_tsgatewayconnectionauthorizationpolicy-class"></a>Classe \_ TSGatewayConnectionAuthorizationPolicy Win32

Descrive un criterio Desktop remoto di autorizzazione connessione Desktop remoto. I CAP di Servizi Desktop remoto vengono usati per determinare se un utente è autorizzato a connettersi al server Desktop remoto Gateway Desktop remoto.

## <a name="syntax"></a>Sintassi

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayConnectionAuthorizationPolicy
{
  string  Name;
  uint32  Order;
  boolean SmartcardAllowed;
  boolean PasswordAllowed;
  boolean SecureIdAllowed;
  boolean CookieAuthenticationAllowed;
  boolean Enabled;
  uint32  IdleTimeout;
  uint32  SessionTimeout;
  uint32  SessionTimeoutAction;
  uint32  DeviceRedirectionType;
  boolean DiskDrivesDisabled;
  boolean PrintersDisabled;
  boolean SerialPortsDisabled;
  boolean ClipboardDisabled;
  boolean PlugAndPlayDevicesDisabled;
  string  UserGroupNames;
  string  ComputerGroupNames;
  boolean HasNapAttributes;
  boolean AllowOnlySDRServers;
};
```

## <a name="members"></a>Members

La **classe \_ Win32 TSGatewayConnectionAuthorizationPolicy** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe Win32 \_ TSGatewayConnectionAuthorizationPolicy** include questi metodi.



| Metodo                                                                                                                | Descrizione                                                                                                                                                                     |
|:----------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddComputerGroupNames**](addcomputergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                   | Aggiunge i nomi dei gruppi di computer specificati alla **proprietà ComputerGroupNames.**<br/>                                                                                      |
| [**AddUserGroupNames**](addusergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                           | Aggiunge i nomi dei gruppi di utenti specificati alla **proprietà UserGroupNames.**<br/>                                                                                              |
| [**Crea**](create-win32-tsgatewayconnectionauthorizationpolicy.md)                                                 | Crea un'istanza di Criteri di autorizzazione connessioni Desktop remoto.<br/>                                                                                                                                                   |
| [**Elimina**](delete-win32-tsgatewayconnectionauthorizationpolicy.md)                                                 | Elimina l'oggetto Criteri di autorizzazione connessioni Desktop remoto corrente.<br/>                                                                                                                                          |
| [**DisableClipboard**](disableclipboard-win32-tsgatewayconnectionauthorizationpolicy.md)                             | Imposta la **proprietà ClipboardDisabled.**<br/>                                                                                                                             |
| [**DisableDiskDrives**](disablediskdrives-win32-tsgatewayconnectionauthorizationpolicy.md)                           | Imposta la **proprietà DiskDrivesDisabled.**<br/>                                                                                                                            |
| [**DisablePlugAndPlayDevices**](disableplugandplaydevices-win32-tsgatewayconnectionauthorizationpolicy.md)           | Imposta la **proprietà PlugAndPlayDevicesDisabled.**<br/>                                                                                                                    |
| [**DisablePrinters**](disableprinters-win32-tsgatewayconnectionauthorizationpolicy.md)                               | Imposta la **proprietà PrintersDisabled.**<br/>                                                                                                                              |
| [**DisableSerialPorts**](disableserialports-win32-tsgatewayconnectionauthorizationpolicy.md)                         | Imposta la **proprietà SerialPortsDisabled.**<br/>                                                                                                                           |
| [**EnableAllowOnlySDRServers**](win32-tsgatewayconnectionauthorizationpolicy-enableallowonlysdrservers.md)           | Usato per attivare o **disattivare la proprietà AllowOnlySDRServers**<br/> **Windows Server 2008:** Questo metodo non è disponibile prima Windows Server 2008 R2.<br/>                  |
| [**MoveDown**](movedown-win32-tsgatewayconnectionauthorizationpolicy.md)                                             | Sposta l'oggetto RD CAP corrente di una posizione verso il basso nell'elenco.<br/>                                                                                                              |
| [**MoveUp**](moveup-win32-tsgatewayconnectionauthorizationpolicy.md)                                                 | Sposta la posizione corrente di RD CAP di una posizione verso l'alto nell'elenco.<br/>                                                                                                                |
| [**RemoveComputerGroupNames**](removecomputergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)             | Rimuove i nomi dei gruppi di computer specificati dalla **proprietà ComputerGroupNames.**<br/>                                                                                 |
| [**RemoveUserGroupNames**](removeusergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                     | Rimuove i nomi dei gruppi di utenti specificati **dalla proprietà UserGroupNames.**<br/>                                                                                             |
| [**SetComputerGroupNames**](setcomputergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                   | Imposta la **proprietà ComputerGroupNames.**<br/>                                                                                                                            |
| [**SetCookieAuthenticationAllowed**](setcookieauthenticationallowed-win32-tsgatewayconnectionauthorizationpolicy.md) | Imposta la **proprietà CookieAuthenticationAllowed.**<br/> **Windows Server 2008:** Questo metodo non è disponibile.<br/>                                                 |
| [**SetDeviceRedirectionType**](setdeviceredirectiontype-win32-tsgatewayconnectionauthorizationpolicy.md)             | Imposta la **proprietà DeviceRedirectionType.**<br/>                                                                                                                         |
| [**SetEnabled**](setenabled-win32-tsgatewayconnectionauthorizationpolicy.md)                                         | Abilita o disabilita il criterio di autorizzazione connessioni Desktop remoto corrente.<br/>                                                                                                                              |
| [**SetIdleTimeout**](setidletimeout-win32-tsgatewayconnectionauthorizationpolicy.md)                                 | Imposta la **proprietà IdleTimeout.**<br/> **Windows Server 2008:** Questo metodo non è disponibile prima Windows Server 2008 R2.<br/>                                   |
| [**SetName**](setname-win32-tsgatewayconnectionauthorizationpolicy.md)                                               | Imposta un nuovo nome per l'applicazione di criteri di autorizzazione connessioni Desktop remoto. Questo metodo garantisce che i nomi siano univoci.<br/>                                                                                      |
| [**SetPasswordAllowed**](setpasswordallowed-win32-tsgatewayconnectionauthorizationpolicy.md)                         | Imposta la **proprietà PasswordAllowed.**<br/>                                                                                                                               |
| [**SetSecureIdAllowed**](setsecureidallowed-win32-tsgatewayconnectionauthorizationpolicy.md)                         | Imposta la **proprietà SecureIdAllowed.**<br/> **Windows Server 2008:** Questo metodo è riservato per un uso futuro.<br/>                                                   |
| [**SetSessionTimeout**](setsessiontimeout-win32-tsgatewayconnectionauthorizationpolicy.md)                           | Imposta le **proprietà SessionTimeout** **e SessionTimeoutAction.**<br/> **Windows Server 2008:** Questo metodo non è disponibile prima Windows Server 2008 R2.<br/> |
| [**SetSmartcardAllowed**](setsmartcardallowed-win32-tsgatewayconnectionauthorizationpolicy.md)                       | Imposta la **proprietà SmartcardAllowed.**<br/>                                                                                                                              |
| [**SetUserGroupNames**](setusergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                           | Imposta la **proprietà UserGroupNames.**<br/>                                                                                                                                |
| [**Aggiornamento**](update-win32-tsgatewayconnectionauthorizationpolicy.md)                                                 | Aggiorna l'istanza corrente di Criteri di autorizzazione connessioni Desktop remoto.<br/>                                                                                                                                          |



 

### <a name="properties"></a>Proprietà

La **classe Win32 \_ TSGatewayConnectionAuthorizationPolicy** ha queste proprietà.

<dl> <dt>

**AllowOnlySDRServers**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se le connessioni sono consentite solo ai server Servizi Desktop remoto di reindirizzamento dei dispositivi (SDR). Questa proprietà può essere impostata usando [**il metodo EnableAllowOnlySDRServers.**](win32-tsgatewayconnectionauthorizationpolicy-enableallowonlysdrservers.md)

**Windows Server 2008:** Questa proprietà non è disponibile prima Windows Server 2008 R2.

</dd> <dt>

**AppuntiDisabled**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se il reindirizzamento degli Appunti verrà disabilitato. Questa proprietà ha effetto solo se il valore della **proprietà DeviceRedirectionType** è "2".

</dd> <dt>

**ComputerGroupNames**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Elenco di nomi di gruppi di computer separati da punti e virgola. Questo valore può essere vuoto. I nomi sono nel formato *Dominio \\ ComputerGroupName*. Se viene specificato un valore, il computer client deve appartenere a uno di questi gruppi di computer per l'accesso dell'utente al server Gateway Desktop remoto.

</dd> <dt>

**CookieAuthenticationAllowed**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se è possibile usare l'autenticazione tramite cookie per connettersi al server Gateway Desktop remoto. Questa proprietà può essere impostata usando il [**metodo SetCookieAuthenticationAllowed.**](setcookieauthenticationallowed-win32-tsgatewayconnectionauthorizationpolicy.md)

**Windows Server 2008:** Questa proprietà non è disponibile.

</dd> <dt>

**DeviceRedirectionType**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica i dispositivi che verranno reindirizzati.

<dt>

0
</dt> <dd>

Tutti i dispositivi verranno reindirizzati.

</dd> <dt>

1
</dt> <dd>

Nessun dispositivo verrà reindirizzato.

</dd> <dt>

2
</dt> <dd>

I dispositivi specificati non verranno reindirizzati. Le proprietà **DiskDrivesDisabled**, **PrintersDisabled**, **SerialPortsDisabled**, **ClipboardDisabled** e **PlugAndPlayDevicesDisabled** controllano quali dispositivi non verranno reindirizzati.

</dd> </dl>

</dd> <dt>

**DiskDrivesDisabled**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se il reindirizzamento delle unità disco sarà disabilitato. Questa proprietà ha effetto solo se il valore della **proprietà DeviceRedirectionType** è "2".

</dd> <dt>

**Enabled**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se questo criterio di autorizzazione desktop remoto verrà usato per valutare un utente per l'autorizzazione.

</dd> <dt>

**HasNapAttributes**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se il cap Desktop remoto usa gli attributi di Protezione accesso alla rete.

</dd> <dt>

**IdleTimeout**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Valore di timeout di inattività, in minuti. Il valore 0 indica che non è presente alcun timeout. Questa proprietà può essere impostata usando il [**metodo SetIdleTimeout.**](setidletimeout-win32-tsgatewayconnectionauthorizationpolicy.md)

**Windows Server 2008:** Questa proprietà non è disponibile.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nome del cap rd.

</dd> <dt>

**Ordine**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ordine di valutazione di Criteri di autorizzazione connessioni Desktop remoto. Il primo valore di Criteri di autorizzazione connessioni Desktop remoto valutato è "1". La **proprietà Order** può essere modificata quando vengono chiamati i metodi [**Create**](create-win32-tsgatewayconnectionauthorizationpolicy.md), [**Delete**](delete-win32-tsgatewayconnectionauthorizationpolicy.md), [**MoveUp**](moveup-win32-tsgatewayconnectionauthorizationpolicy.md) [**o MoveDown.**](movedown-win32-tsgatewayconnectionauthorizationpolicy.md)

</dd> <dt>

**PasswordAllowed**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se è possibile usare una password per connettersi al server Gateway Desktop remoto. Questa proprietà può essere modificata usando il [**metodo SetPasswordAllowed.**](setpasswordallowed-win32-tsgatewayconnectionauthorizationpolicy.md)

</dd> <dt>

**PlugAndPlayDevicesDisabled**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se il reindirizzamento dei Plug and Play dispositivi verrà disabilitato. Questa proprietà ha effetto solo se il valore della **proprietà DeviceRedirectionType** è "2".

</dd> <dt>

**StampantiDisabled**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se il reindirizzamento della stampante verrà disabilitato. Questa proprietà ha effetto solo se il valore della **proprietà DeviceRedirectionType** è "2".

</dd> <dt>

**SecureIdAllowed**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se è possibile usare un identificatore sicuro per connettersi al server Gateway Desktop remoto.

**Windows Server 2008:** Questa proprietà non viene utilizzata.

</dd> <dt>

**SerialPortsDisabled**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se il reindirizzamento delle porte seriali sarà disabilitato. Questa proprietà ha effetto solo se il valore della **proprietà DeviceRedirectionType** è "2".

</dd> <dt>

**SessionTimeout**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Valore di timeout della sessione, in minuti. Il valore 0 indica che non è presente alcun timeout. Questa proprietà può essere impostata usando il [**metodo SetSessionTimeout.**](setsessiontimeout-win32-tsgatewayconnectionauthorizationpolicy.md)

**Windows Server 2008:** Questa proprietà non è disponibile.

</dd> <dt>

**SessionTimeoutAction**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica l'azione da eseguire in caso di timeout della sessione. Questa proprietà può essere impostata usando il [**metodo SetSessionTimeout.**](setsessiontimeout-win32-tsgatewayconnectionauthorizationpolicy.md)

Può essere uno dei valori seguenti.

**Windows Server 2008:** Questa proprietà non è disponibile.

<dt>

0
</dt> <dd>

Disconnettere la sessione.

</dd> <dt>

1
</dt> <dd>

Provare a autorizzare nuovamente la sessione.

</dd> </dl>

</dd> <dt>

**SmartcardAllowed**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se un smart card può essere usato per connettersi al server Gateway Desktop remoto. Questa proprietà può essere modificata usando il [**metodo SetSmartcardAllowed.**](setsmartcardallowed-win32-tsgatewayconnectionauthorizationpolicy.md)

</dd> <dt>

**UserGroupNames**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Elenco di nomi di gruppi di utenti separati da punto e virgola. I nomi sono nel formato *Dominio \\ UserGroupName*. Se l'utente appartiene a uno di questi gruppi di utenti, all'utente sarà consentito l'accesso al server Gateway Desktop remoto.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per usare questa classe, è necessario essere membri del gruppo Administrators.

Managed Object Format (MOF) contengono le definizioni per le classi WMI (Windows Management Instrumentation). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                           |
| Spazio dei nomi<br/>                | TerminalServices \\ CIMv2 \\ radice<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ TSGatewayConnection**](win32-tsgatewayconnection.md)
</dt> <dt>

[**Win32 \_ TSGatewayLoadBalancer**](win32-tsgatewayloadbalancer.md)
</dt> <dt>

[**Win32 \_ TSGatewayRADIUSServer**](win32-tsgatewayradiusserver.md)
</dt> <dt>

[**Win32 \_ TSGatewayResourceAuthorizationPolicy**](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[**Win32 \_ TSGatewayResourceGroup**](win32-tsgatewayresourcegroup.md)
</dt> <dt>

[**Win32 \_ TSGatewayServerSettings**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

