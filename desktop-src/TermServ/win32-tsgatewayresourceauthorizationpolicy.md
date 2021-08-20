---
title: Win32_TSGatewayResourceAuthorizationPolicy classe
description: Descrive un criterio Desktop remoto di autorizzazione delle risorse (RD \ 160; RAP). Un desktop remoto \ 160; VIENE usato per decidere se un utente è autorizzato a connettersi a una risorsa specificata tramite Desktop remoto Gateway Desktop remoto.
ms.assetid: 284a868d-7856-4a25-ba7b-b4beba8ffffc
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayResourceAuthorizationPolicy classe Servizi Desktop remoto
- Win32_TSGatewayResourceAuthorizationPolicy classe Servizi Desktop remoto , descritto
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy
- Win32_TSGatewayResourceAuthorizationPolicy.Name
- Win32_TSGatewayResourceAuthorizationPolicy.Description
- Win32_TSGatewayResourceAuthorizationPolicy.Enabled
- Win32_TSGatewayResourceAuthorizationPolicy.ResourceGroupType
- Win32_TSGatewayResourceAuthorizationPolicy.ResourceGroupName
- Win32_TSGatewayResourceAuthorizationPolicy.UserGroupNames
- Win32_TSGatewayResourceAuthorizationPolicy.ProtocolNames
- Win32_TSGatewayResourceAuthorizationPolicy.PortNumbers
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9748ddc4feccd504d823025ea70877004417717d625c904ccae4445f05e6eb03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999821"
---
# <a name="win32_tsgatewayresourceauthorizationpolicy-class"></a>Classe \_ Win32 TSGatewayResourceAuthorizationPolicy

Descrive un criterio Desktop remoto di autorizzazione delle risorse di desktop remoto. Un account di accesso remoto viene usato per decidere se un utente è autorizzato a connettersi a una risorsa specificata tramite Desktop remoto Gateway Desktop remoto.

## <a name="syntax"></a>Sintassi

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayResourceAuthorizationPolicy
{
  string  Name;
  string  Description;
  boolean Enabled;
  string  ResourceGroupType;
  string  ResourceGroupName;
  string  UserGroupNames;
  string  ProtocolNames;
  string  PortNumbers;
};
```

## <a name="members"></a>Members

La **classe \_ Win32 TSGatewayResourceAuthorizationPolicy** include questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe \_ Win32 TSGatewayResourceAuthorizationPolicy** include questi metodi.



| Metodo                                                                                          | Descrizione                                                                                                         |
|:------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------|
| [**AddUserGroupNames**](addusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md)       | Aggiunge i nomi dei gruppi di utenti specificati ai gruppi di utenti esistenti nella **proprietà UserGroupNames.**<br/>      |
| [**Crea**](create-win32-tsgatewayresourceauthorizationpolicy.md)                             | Crea un gruppo di risorse di Desktop remoto.<br/>                                                                                       |
| [**Elimina**](delete-win32-tsgatewayresourceauthorizationpolicy.md)                             | Elimina l'istanza corrente di RD RAP.<br/>                                                                              |
| [**RemoveUserGroupNames**](removeusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md) | Rimuove i nomi dei gruppi di utenti specificati dai gruppi di utenti esistenti nella **proprietà UserGroupNames.**<br/> |
| [**SetDescription**](setdescription-win32-tsgatewayresourceauthorizationpolicy.md)             | Imposta la **proprietà Description** per RD RAP.<br/>                                                        |
| [**SetEnabled**](setenabled-win32-tsgatewayresourceauthorizationpolicy.md)                     | Abilita o disabilita l'applicazione di criteri di protezione desktop remoto impostando la **proprietà Enabled.**<br/>                                      |
| [**SetName**](setname-win32-tsgatewayresourceauthorizationpolicy.md)                           | Imposta la **proprietà Name** per RD RAP.<br/>                                                               |
| [**SetPortNumbers**](setportnumbers-win32-tsgatewayresourceauthorizationpolicy.md)             | Imposta la **proprietà PortNumbers** per RD RAP.<br/>                                                        |
| [**SetResourceGroup**](setresourcegroup-win32-tsgatewayresourceauthorizationpolicy.md)         | Imposta le **proprietà ResourceGroupType** **e ResourceGroupName.**<br/>                                     |
| [**SetUserGroupNames**](setusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md)       | Imposta la **proprietà UserGroupNames** per RD RAP.<br/>                                                     |
| [**Aggiornamento**](update-win32-tsgatewayresourceauthorizationpolicy.md)                             | Aggiorna l'istanza corrente di RD RAP.<br/>                                                                              |



 

### <a name="properties"></a>Proprietà

La **classe \_ Win32 TSGatewayResourceAuthorizationPolicy** ha queste proprietà.

<dl> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione di RD RAP. Questa proprietà viene modificata con il [**metodo SetDescription.**](setdescription-win32-tsgatewayresourceauthorizationpolicy.md)

</dd> <dt>

**Enabled**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se l'applicazione di criteri di accesso remoto è abilitata. Questa proprietà viene modificata con il [**metodo SetEnabled.**](setenabled-win32-tsgatewayresourceauthorizationpolicy.md)

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nome dell'istanza di Criteri di gruppo di Desktop remoto. Questa proprietà viene modificata con il [**metodo SetName.**](setname-win32-tsgatewayresourceauthorizationpolicy.md)

</dd> <dt>

**Numeroporta**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Elenco di numeri di porta separati da punto e virgola consentiti per questo criterio. Per consentire qualsiasi numero di porta, impostare " \* ".

</dd> <dt>

**ProtocolNames**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Elenco di nomi di protocollo separati da punto e virgola abilitati per questo criterio. I nomi devono corrispondere alla restituzione [**del metodo GetProtocolName**](getprotocolname-win32-tsgatewayserversettings.md) della [**classe Win32 \_ TSGatewayServerSettings.**](win32-tsgatewayserversettings.md)

</dd> <dt>

**ResourceGroupName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome del gruppo di risorse. Questa proprietà viene modificata con il [**metodo SetResourceGroup.**](setresourcegroup-win32-tsgatewayresourceauthorizationpolicy.md)

</dd> <dt>

**ResourceGroupType**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Identifica il tipo del gruppo di risorse. Questa proprietà viene modificata con il [**metodo SetResourceGroup.**](setresourcegroup-win32-tsgatewayresourceauthorizationpolicy.md)

<dt>

"RG"
</dt> <dd>

Gruppo di risorse.

</dd> <dt>

"CG"
</dt> <dd>

Gruppo di computer, come archiviato in Active Directory Domain Services.

</dd> <dt>

"ALL"
</dt> <dd>

Tutte le risorse.

</dd> </dl>

</dd> <dt>

**UserGroupNames**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Elenco di nomi di gruppi di utenti separati da punto e virgola. Se l'utente appartiene a uno di questi gruppi di utenti, l'accesso sarà consentito. Questa proprietà viene modificata con i [**metodi SetUserGroupNames,**](setusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md) [**AddUserGroupNames**](addusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md)e [**RemoveUserGroupNames.**](removeusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md)

</dd> </dl>

## <a name="remarks"></a>Commenti

Per utilizzare questa classe, è necessario essere un membro del gruppo Administrators.

Managed Object Format (MOF) contengono le definizioni per le Windows WMI (Management Instrumentation). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, [vedere Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

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

[**Win32 \_ TSGatewayRADIUSServer**](win32-tsgatewayradiusserver.md)
</dt> <dt>

[**Win32 \_ TSGatewayResourceGroup**](win32-tsgatewayresourcegroup.md)
</dt> <dt>

[**Win32 \_ TSGatewayServerSettings**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

