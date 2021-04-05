---
title: Classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Descrive un criterio di autorizzazione della connessione Desktop remoto (RD \ 160; LIMITE). RD \ 160; I tappi vengono usati per determinare se un utente è autorizzato a connettersi al server gateway gateway di Desktop remoto (Gateway Desktop remoto).
ms.assetid: 50ff3f97-0818-4e9c-9db7-a822cfed0e82
ms.tgt_platform: multiple
keywords:
- Classe Win32_TSGatewayConnectionAuthorizationPolicy Servizi Desktop remoto
- Classe Win32_TSGatewayConnectionAuthorizationPolicy Servizi Desktop remoto, descritta
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
ms.openlocfilehash: 27384ec3a5f17c3e41fe0ceccf0ee1f7f9d08044
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873689"
---
# <a name="win32_tsgatewayconnectionauthorizationpolicy-class"></a>Win32 \_ TSGatewayConnectionAuthorizationPolicy (classe)

Descrive un criterio di autorizzazione della connessione Desktop remoto. I tappi desktop remoto vengono usati per determinare se un utente è autorizzato a connettersi al server gateway di Desktop remoto (Gateway Desktop remoto).

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

La classe **Win32 \_ TSGatewayConnectionAuthorizationPolicy** presenta questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La classe **Win32 \_ TSGatewayConnectionAuthorizationPolicy** presenta questi metodi.



| Metodo                                                                                                                | Descrizione                                                                                                                                                                     |
|:----------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddComputerGroupNames**](addcomputergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                   | Aggiunge i nomi dei gruppi di computer specificati alla proprietà **ComputerGroupNames** .<br/>                                                                                      |
| [**AddUserGroupNames**](addusergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                           | Aggiunge i nomi dei gruppi di utenti specificati alla proprietà **UserGroupNames** .<br/>                                                                                              |
| [**Creare**](create-win32-tsgatewayconnectionauthorizationpolicy.md)                                                 | Crea un CAP RD.<br/>                                                                                                                                                   |
| [**Delete**](delete-win32-tsgatewayconnectionauthorizationpolicy.md)                                                 | Elimina il CAP di RD corrente.<br/>                                                                                                                                          |
| [**DisableClipboard**](disableclipboard-win32-tsgatewayconnectionauthorizationpolicy.md)                             | Imposta la proprietà **ClipboardDisabled** .<br/>                                                                                                                             |
| [**DisableDiskDrives**](disablediskdrives-win32-tsgatewayconnectionauthorizationpolicy.md)                           | Imposta la proprietà **DiskDrivesDisabled** .<br/>                                                                                                                            |
| [**DisablePlugAndPlayDevices**](disableplugandplaydevices-win32-tsgatewayconnectionauthorizationpolicy.md)           | Imposta la proprietà **PlugAndPlayDevicesDisabled** .<br/>                                                                                                                    |
| [**DisablePrinters**](disableprinters-win32-tsgatewayconnectionauthorizationpolicy.md)                               | Imposta la proprietà **PrintersDisabled** .<br/>                                                                                                                              |
| [**DisableSerialPorts**](disableserialports-win32-tsgatewayconnectionauthorizationpolicy.md)                         | Imposta la proprietà **SerialPortsDisabled** .<br/>                                                                                                                           |
| [**EnableAllowOnlySDRServers**](win32-tsgatewayconnectionauthorizationpolicy-enableallowonlysdrservers.md)           | Usato per impostare o disabilitare la proprietà **AllowOnlySDRServers**<br/> **Windows Server 2008:** Questo metodo non è disponibile prima di Windows Server 2008 R2.<br/>                  |
| [**MoveDown**](movedown-win32-tsgatewayconnectionauthorizationpolicy.md)                                             | Sposta l'estremità corrente di una posizione verso il basso nell'elenco.<br/>                                                                                                              |
| [**MoveUp**](moveup-win32-tsgatewayconnectionauthorizationpolicy.md)                                                 | Sposta il CAP di RD corrente di una posizione verso l'alto nell'elenco.<br/>                                                                                                                |
| [**RemoveComputerGroupNames**](removecomputergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)             | Rimuove i nomi dei gruppi di computer specificati dalla proprietà **ComputerGroupNames** .<br/>                                                                                 |
| [**RemoveUserGroupNames**](removeusergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                     | Rimuove i nomi dei gruppi di utenti specificati dalla proprietà **UserGroupNames** .<br/>                                                                                             |
| [**SetComputerGroupNames**](setcomputergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                   | Imposta la proprietà **ComputerGroupNames** .<br/>                                                                                                                            |
| [**SetCookieAuthenticationAllowed**](setcookieauthenticationallowed-win32-tsgatewayconnectionauthorizationpolicy.md) | Imposta la proprietà **CookieAuthenticationAllowed** .<br/> **Windows Server 2008:** Questo metodo non è disponibile.<br/>                                                 |
| [**SetDeviceRedirectionType**](setdeviceredirectiontype-win32-tsgatewayconnectionauthorizationpolicy.md)             | Imposta la proprietà **DeviceRedirectionType** .<br/>                                                                                                                         |
| [**SetEnabled**](setenabled-win32-tsgatewayconnectionauthorizationpolicy.md)                                         | Abilita o Disabilita il criterio di autorizzazione connessioni Desktop remoto corrente.<br/>                                                                                                                              |
| [**SetIdleTimeout**](setidletimeout-win32-tsgatewayconnectionauthorizationpolicy.md)                                 | Imposta la proprietà **IdleTimeout** .<br/> **Windows Server 2008:** Questo metodo non è disponibile prima di Windows Server 2008 R2.<br/>                                   |
| [**SetName**](setname-win32-tsgatewayconnectionauthorizationpolicy.md)                                               | Imposta un nuovo nome per il CAP di desktop remoto. Questo metodo assicura che i nomi siano univoci.<br/>                                                                                      |
| [**SetPasswordAllowed**](setpasswordallowed-win32-tsgatewayconnectionauthorizationpolicy.md)                         | Imposta la proprietà **PasswordAllowed** .<br/>                                                                                                                               |
| [**SetSecureIdAllowed**](setsecureidallowed-win32-tsgatewayconnectionauthorizationpolicy.md)                         | Imposta la proprietà **SecureIdAllowed** .<br/> **Windows Server 2008:** Questo metodo è riservato per utilizzi futuri.<br/>                                                   |
| [**SetSessionTimeout**](setsessiontimeout-win32-tsgatewayconnectionauthorizationpolicy.md)                           | Imposta le proprietà **SessionTimeout** e **SessionTimeoutAction** .<br/> **Windows Server 2008:** Questo metodo non è disponibile prima di Windows Server 2008 R2.<br/> |
| [**SetSmartcardAllowed**](setsmartcardallowed-win32-tsgatewayconnectionauthorizationpolicy.md)                       | Imposta la proprietà **SmartcardAllowed** .<br/>                                                                                                                              |
| [**SetUserGroupNames**](setusergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                           | Imposta la proprietà **UserGroupNames** .<br/>                                                                                                                                |
| [**Aggiornamento**](update-win32-tsgatewayconnectionauthorizationpolicy.md)                                                 | Aggiorna l'estremità del desktop remoto corrente.<br/>                                                                                                                                          |



 

### <a name="properties"></a>Proprietà

La classe **Win32 \_ TSGatewayConnectionAuthorizationPolicy** dispone di queste proprietà.

<dl> <dt>

**AllowOnlySDRServers**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se le connessioni sono consentite solo per i server RDS (Secure Device Reindirizzamento). Questa proprietà può essere impostata tramite il metodo [**EnableAllowOnlySDRServers**](win32-tsgatewayconnectionauthorizationpolicy-enableallowonlysdrservers.md) .

**Windows Server 2008:** Questa proprietà non è disponibile prima di Windows Server 2008 R2.

</dd> <dt>

**ClipboardDisabled**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se il reindirizzamento degli appunti verrà disabilitato. Questa proprietà ha effetto solo se il valore della proprietà **DeviceRedirectionType** è "2".

</dd> <dt>

**ComputerGroupNames**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Elenco di nomi di gruppi di computer separati da punto e virgola. Questo valore può essere vuoto. I nomi sono nel formato *dominio \\ ComputerGroupName*. Se viene specificato un valore, il computer client deve appartenere a uno di questi gruppi di computer in modo che l'utente acceda al server Gateway Desktop remoto.

</dd> <dt>

**CookieAuthenticationAllowed**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se l'autenticazione del cookie può essere utilizzata per la connessione al server Gateway Desktop remoto. Questa proprietà può essere impostata tramite il metodo [**SetCookieAuthenticationAllowed**](setcookieauthenticationallowed-win32-tsgatewayconnectionauthorizationpolicy.md) .

**Windows Server 2008:** Questa proprietà non è disponibile.

</dd> <dt>

**DeviceRedirectionType**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica i dispositivi che verranno reindirizzati.

<dt>

0
</dt> <dd>

Verranno reindirizzati tutti i dispositivi.

</dd> <dt>

1
</dt> <dd>

Non verrà reindirizzato alcun dispositivo.

</dd> <dt>

2
</dt> <dd>

I dispositivi specificati non verranno reindirizzati. Le proprietà **DiskDrivesDisabled**, **PrintersDisabled**, **SerialPortsDisabled**, **ClipboardDisabled** e **PlugAndPlayDevicesDisabled** controllano i dispositivi che non verranno reindirizzati.

</dd> </dl>

</dd> <dt>

**DiskDrivesDisabled**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se il reindirizzamento dell'unità disco verrà disabilitato. Questa proprietà ha effetto solo se il valore della proprietà **DeviceRedirectionType** è "2".

</dd> <dt>

**Enabled**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se il CAP RD verrà utilizzato per valutare l'autorizzazione di un utente.

</dd> <dt>

**HasNapAttributes**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se il CAP RD utilizza gli attributi di protezione accesso alla rete (NAP).

</dd> <dt>

**IdleTimeout**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Valore del timeout di inattività, espresso in minuti. Il valore 0 indica che non esiste alcun timeout. Questa proprietà può essere impostata tramite il metodo [**SetIdleTimeout**](setidletimeout-win32-tsgatewayconnectionauthorizationpolicy.md) .

**Windows Server 2008:** Questa proprietà non è disponibile.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nome del CAP di desktop remoto.

</dd> <dt>

**Ordine**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ordine di valutazione del CAP di desktop remoto. Il primo CAP RD valutato ha un valore pari a "1". È possibile modificare la proprietà **Order** quando vengono chiamati i metodi [**create**](create-win32-tsgatewayconnectionauthorizationpolicy.md), [**Delete**](delete-win32-tsgatewayconnectionauthorizationpolicy.md), [**MoveUp**](moveup-win32-tsgatewayconnectionauthorizationpolicy.md)o [**MoveDown**](movedown-win32-tsgatewayconnectionauthorizationpolicy.md) .

</dd> <dt>

**PasswordAllowed**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se è possibile utilizzare una password per la connessione al server Gateway Desktop remoto. Questa proprietà può essere modificata tramite il metodo [**SetPasswordAllowed**](setpasswordallowed-win32-tsgatewayconnectionauthorizationpolicy.md) .

</dd> <dt>

**PlugAndPlayDevicesDisabled**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se il reindirizzamento dei dispositivi Plug and Play sarà disabilitato. Questa proprietà ha effetto solo se il valore della proprietà **DeviceRedirectionType** è "2".

</dd> <dt>

**PrintersDisabled**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se il reindirizzamento della stampante verrà disabilitato. Questa proprietà ha effetto solo se il valore della proprietà **DeviceRedirectionType** è "2".

</dd> <dt>

**SecureIdAllowed**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se è possibile utilizzare un identificatore sicuro per la connessione al server Gateway Desktop remoto.

**Windows Server 2008:** Questa proprietà non viene utilizzata.

</dd> <dt>

**SerialPortsDisabled**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se il reindirizzamento della porta seriale verrà disabilitato. Questa proprietà ha effetto solo se il valore della proprietà **DeviceRedirectionType** è "2".

</dd> <dt>

**SessionTimeout**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Valore di timeout della sessione, espresso in minuti. Il valore 0 indica che non esiste alcun timeout. Questa proprietà può essere impostata tramite il metodo [**SetSessionTimeout**](setsessiontimeout-win32-tsgatewayconnectionauthorizationpolicy.md) .

**Windows Server 2008:** Questa proprietà non è disponibile.

</dd> <dt>

**SessionTimeoutAction**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica l'azione da intraprendere in caso di timeout di sessione. Questa proprietà può essere impostata tramite il metodo [**SetSessionTimeout**](setsessiontimeout-win32-tsgatewayconnectionauthorizationpolicy.md) .

Può corrispondere a uno dei valori seguenti.

**Windows Server 2008:** Questa proprietà non è disponibile.

<dt>

0
</dt> <dd>

Disconnettere la sessione.

</dd> <dt>

1
</dt> <dd>

Tentativo di autorizzare nuovamente la sessione.

</dd> </dl>

</dd> <dt>

**SmartcardAllowed**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se è possibile utilizzare una smart card per la connessione al server Gateway Desktop remoto. Questa proprietà può essere modificata tramite il metodo [**SetSmartcardAllowed**](setsmartcardallowed-win32-tsgatewayconnectionauthorizationpolicy.md) .

</dd> <dt>

**UserGroupNames**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Elenco di nomi di gruppi di utenti separati da punti e virgola. I nomi sono nel formato *dominio \\ nomegruppoutenti*. Se l'utente appartiene a uno di questi gruppi di utenti, l'utente sarà autorizzato ad accedere al server Gateway Desktop remoto.

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

 

