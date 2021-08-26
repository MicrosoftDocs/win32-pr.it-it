---
title: Win32_TSGatewayServerSettings classe
description: Fornisce metodi e proprietà per visualizzare e configurare Desktop remoto impostazioni del server Gateway Desktop remoto.
ms.assetid: f772bf71-68ef-4345-8123-f6ad50ee4d61
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayServerSettings classe Servizi Desktop remoto
- Win32_TSGatewayServerSettings classe Servizi Desktop remoto , descritto
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings
- Win32_TSGatewayServerSettings.MaxConnections
- Win32_TSGatewayServerSettings.UnlimitedConnections
- Win32_TSGatewayServerSettings.MaximumAllowedConnectionsBySku
- Win32_TSGatewayServerSettings.SkuName
- Win32_TSGatewayServerSettings.MaxProtocols
- Win32_TSGatewayServerSettings.MaxLogEvents
- Win32_TSGatewayServerSettings.adminMessageText
- Win32_TSGatewayServerSettings.adminMessageStartTime
- Win32_TSGatewayServerSettings.adminMessageEndTime
- Win32_TSGatewayServerSettings.consentMessageText
- Win32_TSGatewayServerSettings.OnlyConsentCapableClients
- Win32_TSGatewayServerSettings.CentralCAPEnabled
- Win32_TSGatewayServerSettings.RequestSOH
- Win32_TSGatewayServerSettings.AuthenticationPluginName
- Win32_TSGatewayServerSettings.AuthenticationPluginCLSID
- Win32_TSGatewayServerSettings.AuthenticationPluginDescription
- Win32_TSGatewayServerSettings.AuthorizationPluginName
- Win32_TSGatewayServerSettings.AuthorizationPluginCLSID
- Win32_TSGatewayServerSettings.AuthorizationPluginDescription
- Win32_TSGatewayServerSettings.SslBridging
- Win32_TSGatewayServerSettings.IsConfigured
- Win32_TSGatewayServerSettings.CertHash
- Win32_TSGatewayServerSettings.EnforceChannelBinding
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00c199b4b8e98832dcc8dbe65b8fc2ef636df71c8bd6e3c096670e6333f83a75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008521"
---
# <a name="win32_tsgatewayserversettings-class"></a>Classe \_ TSGatewayServerSettings Win32

Fornisce metodi e proprietà per visualizzare e configurare Desktop remoto impostazioni del server Gateway Desktop remoto. Un amministratore può usare questa classe per configurare un set di protocolli, il set di eventi che verranno scritti nel registro eventi e il numero massimo di connessioni tramite Gateway Desktop remoto.

## <a name="syntax"></a>Sintassi

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayServerSettings
{
  uint32  MaxConnections;
  boolean UnlimitedConnections;
  uint32  MaximumAllowedConnectionsBySku;
  string  SkuName;
  uint32  MaxProtocols;
  uint32  MaxLogEvents;
  string  adminMessageText;
  string  adminMessageStartTime;
  string  adminMessageEndTime;
  string  consentMessageText;
  boolean OnlyConsentCapableClients;
  boolean CentralCAPEnabled;
  boolean RequestSOH;
  string  AuthenticationPluginName;
  string  AuthenticationPluginCLSID;
  string  AuthenticationPluginDescription;
  string  AuthorizationPluginName;
  string  AuthorizationPluginCLSID;
  string  AuthorizationPluginDescription;
  uint32  SslBridging;
  boolean IsConfigured;
  uint8   CertHash[];
  boolean EnforceChannelBinding;
};
```

## <a name="members"></a>Members

La **classe \_ Win32 TSGatewayServerSettings** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe Win32 \_ TSGatewayServerSettings** include questi metodi.



| Metodo                                                                                                                                             | Descrizione                                                                                                                                                                                                                                                      |
|:---------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Configurare**](configure-win32-tsgatewayserversettings.md)                                                                                       | Configura le impostazioni IIS e RPC richieste dal servizio Gateway Desktop remoto.<br/> **Windows Server 2008:** Questo metodo non è disponibile prima Windows Server 2008 R2.<br/>                                                                               |
| [**EnableCentralCAP**](enablecentralcap-win32-tsgatewayserversettings.md)                                                                         | Abilita o disabilita la proprietà **CentralCAPEnabled,** che controlla se i server dei criteri di autorizzazione delle connessioni Desktop remoto (RD CAP) centrali vengono usati per controllare i criteri di autorizzazione della connessione per questo server.<br/>                    |
| [**EnableLogEvent**](enablelogevent-win32-tsgatewayserversettings.md)                                                                             | Abilita o disabilita la registrazione del tipo di evento specificato.<br/>                                                                                                                                                                                              |
| [**EnableOnlyConsentCapableClients**](enableonlyconsentcapableclients-win32-tsgatewayserversettings.md)                                           | Imposta la **proprietà OnlyConsentCapableClients.**<br/> **Windows Server 2008:** Questo metodo non è disponibile prima Windows Server 2008 R2.<br/>                                                                                                      |
| [**EnableRequestSoH**](win32-tsgatewayserversettings-enablerequestsoh.md)                                                                         | Questo metodo non è supportato a partire da Windows Server 2016.<br/> **Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 e Windows Server 2008:** Abilita o disabilita le richieste per un'istruzione di integrità (SoH).<br/> <br/> |
| [**EnableTransport**](enabletransport-win32-tsgatewayserversettings.md)                                                                           | Abilita o disabilita il trasporto specificato.<br/> **Windows Server 2008 R2 e Windows Server 2008:** Questo metodo non è disponibile prima di Windows Server 2012.<br/>                                                                                  |
| [**EnumAuthenticationPlugins**](enumauthenticationplugins-win32-tsgatewayserversettings.md)                                                       | Enumera tutti i plug-in di autenticazione registrati.<br/> **Windows Server 2008:** Questo metodo non è disponibile.<br/>                                                                                                                                  |
| [**EnumAuthorizationPlugins**](enumauthorizationplugins-win32-tsgatewayserversettings.md)                                                         | Enumera tutti i plug-in di autorizzazione registrati.<br/> **Windows Server 2008:** Questo metodo non è disponibile prima Windows Server 2008 R2.<br/>                                                                                                     |
| [**GetIPAndPort**](getipandport-win32-tsgatewayserversettings.md)                                                                                 | Ottiene l'indirizzo IP di ascolto e il numero di porta per il trasporto specificato.<br/> **Windows Server 2008 R2 e Windows Server 2008:** Questo metodo non è disponibile prima di Windows Server 2012.<br/>                                                 |
| [**GetLogEventName**](getlogeventname-win32-tsgatewayserversettings.md)                                                                           | Restituisce il nome dell'evento di log per l'indice eventi del log specificato.<br/>                                                                                                                                                                                         |
| [**GetProtocolName**](getprotocolname-win32-tsgatewayserversettings.md)                                                                           | Restituisce il nome del protocollo per l'indice del protocollo specificato.<br/>                                                                                                                                                                                           |
| [**IsLogEventEnabled**](islogeventenabled-win32-tsgatewayserversettings.md)                                                                       | Indica se il tipo di registro eventi specificato è abilitato.<br/>                                                                                                                                                                                            |
| [**IsTransportEnabled**](istransportenabled-win32-tsgatewayserversettings.md)                                                                     | Determina se il trasporto specificato è abilitato.<br/> **Windows Server 2008 R2 e Windows Server 2008:** Questo metodo non è disponibile prima di Windows Server 2012.<br/>                                                                        |
| [**QueryCertContext**](win32-tsgatewayserversettings-querycertcontext.md)                                                                         | Indica se il certificato specificato è installato.<br/>                                                                                                                                                                                             |
| [**RecycleRpcApplicationPools**](recyclerpcapplicationpools-win32-tsgatewayserversettings.md)                                                     | Ricicla i pool di applicazioni RPC in IIS.<br/> **Windows Server 2008:** Questo metodo non è disponibile prima Windows Server 2008 R2.<br/>                                                                                                            |
| [**RefreshCertContext**](win32-tsgatewayserversettings-refreshcertcontext.md)                                                                     | Aggiorna il certificato usato dal server Gateway Desktop remoto.<br/>                                                                                                                                                                                      |
| [**SetAuthenticationPlugin**](setauthenticationplugin-win32-tsgatewayserversettings.md)                                                           | Imposta il plug-in di autenticazione corrente per il server Gateway Desktop remoto.<br/> **Windows Server 2008:** Questo metodo non è disponibile prima Windows Server 2008 R2.<br/>                                                                                    |
| [**SetAuthenticationPluginAndRecycleRpcApplicationPools**](setauthenticationpluginandrecyclerpcapplicationpools-win32-tsgatewayserversettings.md) | Imposta il plug-in di autenticazione corrente per il server Gateway Desktop remoto e ricicla i pool di applicazioni RPC in IIS.<br/> **Windows Server 2008:** Questo metodo non è disponibile prima Windows Server 2008 R2.<br/>                                      |
| [**SetAuthorizationPlugin**](setauthorizationplugin-win32-tsgatewayserversettings.md)                                                             | Imposta il plug-in di autorizzazione corrente per il server Gateway Desktop remoto.<br/> **Windows Server 2008:** Questo metodo non è disponibile prima Windows Server 2008 R2.<br/>                                                                                     |
| [**SetCertificate**](setcertificate-win32-tsgatewayserversettings.md)                                                                             | Imposta l'hash del certificato per l'associazione HTTPS sulla porta 443 in IIS.<br/> **Windows Server 2008:** Questo metodo non è disponibile prima Windows Server 2008 R2.<br/>                                                                                       |
| [**SetCertificateACL**](setcertificateacl-win32-tsgatewayserversettings.md)                                                                       | Imposta gli elenchi di controllo di accesso (ACL) del certificato per questo server.<br/>                                                                                                                                                                                     |
| [**SetDefaultPluginsAndRecycleRpcApplicationPools**](setdefaultpluginsandrecyclerpcapplicationpools-win32-tsgatewayserversettings.md)             | Imposta i plug-in di autenticazione e autorizzazione correnti per il server Gateway Desktop remoto e ricicla i pool di applicazioni RPC in IIS.<br/> **Windows Server 2008:** Questo metodo non è disponibile prima Windows Server 2008 R2.<br/>                   |
| [**SetEnforceChannelBinding**](setenforcechannelbinding-win32-tsgatewayserversettings.md)                                                         | Imposta la **proprietà EnforceChannelBinding.**<br/> **Windows Server 2008 R2 e Windows Server 2008:** Questo metodo non è disponibile prima di Windows Server 2012.<br/>                                                                                  |
| [**SetIPAndPort**](setipandport-win32-tsgatewayserversettings.md)                                                                                 | Imposta l'indirizzo IP di ascolto e il numero di porta per il trasporto specificato.<br/> **Windows Server 2008 R2 e Windows Server 2008:** Questo metodo non è disponibile prima di Windows Server 2012.<br/>                                                    |
| [**SetMaxConnections**](setmaxconnections-win32-tsgatewayserversettings.md)                                                                       | Imposta il numero massimo di connessioni consentite tramite Gateway Desktop remoto. Questo metodo modifica le **proprietà MaxConnections** **e UnlimitedConnections.**<br/>                                                                                                |
| [**SetSslBridging**](setsslbridging-win32-tsgatewayserversettings.md)                                                                             | Imposta il tipo di bridging SSL che deve essere usato dal server Gateway Desktop remoto.<br/> **Windows Server 2008:** Questo metodo non è disponibile prima Windows Server 2008 R2.<br/>                                                                                    |
| [**TSGRemoveAdminMsg**](tsgremoveadminmsg-win32-tsgatewayserversettings.md)                                                                       | Rimuove il messaggio amministrativo per il server gateway.<br/> **Windows Server 2008:** Questo metodo non è disponibile prima Windows Server 2008 R2.<br/>                                                                                            |
| [**TSGRemoveConsentMsg**](tsgremoveconsentmsg-win32-tsgatewayserversettings.md)                                                                   | Rimuove il messaggio amministrativo per il server gateway.<br/> **Windows Server 2008:** Questo metodo non è disponibile prima Windows Server 2008 R2.<br/>                                                                                            |
| [**TSGStoreAdminMsg**](tsgstoreadminmsg-win32-tsgatewayserversettings.md)                                                                         | Aggiorna il messaggio amministrativo per il server gateway.<br/> **Windows Server 2008:** Questo metodo non è disponibile prima Windows Server 2008 R2.<br/>                                                                                            |
| [**TSGStoreConsentMsg**](tsgstoreconsentmsg-win32-tsgatewayserversettings.md)                                                                     | Aggiorna il messaggio di consenso per il server gateway.<br/> **Windows Server 2008:** Questo metodo non è disponibile prima Windows Server 2008 R2.<br/>                                                                                                   |



 

### <a name="properties"></a>Proprietà

La **classe Win32 \_ TSGatewayServerSettings** ha queste proprietà.

<dl> <dt>

**adminMessageEndTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ora di fine del messaggio amministrativo.

**Windows Server 2008:** Questa proprietà non è disponibile prima Windows Server 2008 R2.

</dd> <dt>

**adminMessageStartTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ora di inizio del messaggio amministrativo.

**Windows Server 2008:** Questa proprietà non è disponibile prima Windows Server 2008 R2.

</dd> <dt>

**adminMessageText**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Testo del messaggio amministrativo.

**Windows Server 2008:** Questa proprietà non è disponibile prima Windows Server 2008 R2.

</dd> <dt>

**AuthenticationPluginCLSID**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

CLSID del plug-in di autenticazione corrente.

**Windows Server 2008:** Questa proprietà non è disponibile prima Windows Server 2008 R2.

</dd> <dt>

**AuthenticationPluginDescription**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione del plug-in di autenticazione corrente.

**Windows Server 2008:** Questa proprietà non è disponibile prima Windows Server 2008 R2.

</dd> <dt>

**AuthenticationPluginName**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome del plug-in di autenticazione corrente.

**Windows Server 2008:** Questa proprietà non è disponibile prima Windows Server 2008 R2.

</dd> <dt>

**AuthorizationPluginCLSID**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

CLSID del plug-in di autorizzazione corrente.

**Windows Server 2008:** Questa proprietà non è disponibile prima Windows Server 2008 R2.

</dd> <dt>

**AuthorizationPluginDescription**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione del plug-in di autorizzazione corrente.

**Windows Server 2008:** Questa proprietà non è disponibile prima Windows Server 2008 R2.

</dd> <dt>

**AuthorizationPluginName**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome del plug-in di autorizzazione corrente.

**Windows Server 2008:** Questa proprietà non è disponibile prima Windows Server 2008 R2.

</dd> <dt>

**CentralCAPEnabled**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica se per il controllo di questo server vengono utilizzati server di Criteri di autorizzazione Connessioni Desktop remoto centrali. Questa proprietà può essere modificata chiamando il [**metodo EnableCentralCAP.**](enablecentralcap-win32-tsgatewayserversettings.md)

</dd> <dt>

**CertHash**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica l'hash del certificato per l'associazione HTTPS sulla porta 443 in IIS.

**Windows Server 2008:** Questa proprietà non è disponibile prima Windows Server 2008 R2.

</dd> <dt>

**consentMessageText**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Testo del messaggio di consenso.

**Windows Server 2008:** Questa proprietà non è disponibile prima Windows Server 2008 R2.

</dd> <dt>

**EnforceChannelBinding**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se l'associazione di canale viene applicata per il trasporto HTTP. Questo valore della proprietà può essere modificato usando il [**metodo SetEnforceChannelBinding.**](setenforcechannelbinding-win32-tsgatewayserversettings.md)

**Windows Server 2008 R2 e Windows Server 2008:** Questa proprietà non è disponibile prima di Windows Server 2012.

</dd> <dt>

**IsConfigured**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica se sono configurate le impostazioni IIS e RPC richieste dal servizio Gateway Desktop remoto.

**Windows Server 2008:** Questa proprietà non è disponibile prima Windows Server 2008 R2.

</dd> <dt>

**MaxConnections**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Restituisce il numero massimo di connessioni consentite tramite Gateway Desktop remoto. Questa proprietà può essere impostata usando il [**metodo SetMaxConnections.**](setmaxconnections-win32-tsgatewayserversettings.md)

</dd> <dt>

**MaximumAllowedConnectionsBySku**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero massimo di connessioni consentite dall'unità di mantenimento scorte (SKU).

</dd> <dt>

**MaxLogEvents**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Restituisce il numero massimo di eventi di log.

</dd> <dt>

**MaxProtocols**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di protocolli supportati da Gateway Desktop remoto.

</dd> <dt>

**OnlyConsentCapableClients**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica se solo i client in grado di ricevere messaggi di consenso possono connettersi al Gateway Desktop remoto.

**Windows Server 2008:** Questa proprietà non è disponibile prima Windows Server 2008 R2.

<dt>

diverso da zero
</dt> <dd>

Solo i client che supportano i messaggi di consenso possono connettersi.

</dd> <dt>

zero
</dt> <dd>

Anche i client che non supportano il messaggio di consenso possono connettersi.

</dd> </dl>

</dd> <dt>

**RequestSoH**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Questa proprietà non è supportata a partire da Windows Server 2016.

**Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 e Windows Server 2008: **

Specifica se il server deve richiedere un'istruzione di integrità (SoH) dal client. Questa proprietà può essere modificata usando il [**metodo EnableRequestSOH.**](win32-tsgatewayserversettings-enablerequestsoh.md)

</dd> <dt>

**SkuName**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome della SKU.

</dd> <dt>

**SslBridging**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica il tipo di bridging SSL che deve essere usato dal server Gateway Desktop remoto. Può essere uno dei valori seguenti.

**Windows Server 2008:** Questa proprietà non è disponibile prima Windows Server 2008 R2.

<dt>

0
</dt> <dd>

Nessun bridging SSL.

</dd> <dt>

1
</dt> <dd>

Bridging da HTTPS a HTTP.

</dd> <dt>

2
</dt> <dd>

Bridging da HTTPS a HTTPS.

</dd> </dl>

</dd> <dt>

**UnlimitedConnections**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se è consentito un numero illimitato di connessioni tramite Gateway Desktop remoto. Questa proprietà può essere impostata tramite il [**metodo SetMaxConnections.**](setmaxconnections-win32-tsgatewayserversettings.md)

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

[**Win32 \_ TSGatewayConnectionAuthorizationPolicy**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[**Win32 \_ TSGatewayLoadBalancer**](win32-tsgatewayloadbalancer.md)
</dt> <dt>

[**Win32 \_ TSGatewayRADIUSServer**](win32-tsgatewayradiusserver.md)
</dt> <dt>

[**Win32 \_ TSGatewayResourceAuthorizationPolicy**](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[**Win32 \_ TSGatewayResourceGroup**](win32-tsgatewayresourcegroup.md)
</dt> </dl>

 

