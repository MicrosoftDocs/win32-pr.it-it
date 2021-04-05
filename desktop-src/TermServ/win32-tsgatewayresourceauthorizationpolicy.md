---
title: Classe Win32_TSGatewayResourceAuthorizationPolicy
description: Descrive i criteri di autorizzazione delle risorse di Desktop remoto (RD \ 160; RAP). RD \ 160; Il RAP viene usato per decidere se un utente è autorizzato a connettersi a una risorsa specificata tramite Desktop remoto Gateway (Gateway Desktop remoto).
ms.assetid: 284a868d-7856-4a25-ba7b-b4beba8ffffc
ms.tgt_platform: multiple
keywords:
- Classe Win32_TSGatewayResourceAuthorizationPolicy Servizi Desktop remoto
- Classe Win32_TSGatewayResourceAuthorizationPolicy Servizi Desktop remoto, descritta
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
ms.openlocfilehash: 0c262cb1ce3351c89dc5d7edf3b0d106116e83b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048286"
---
# <a name="win32_tsgatewayresourceauthorizationpolicy-class"></a>Win32 \_ TSGatewayResourceAuthorizationPolicy (classe)

Descrive un criterio di autorizzazione risorse Desktop remoto (RD RAP). Un criterio di autorizzazione risorse Desktop remoto viene usato per decidere se un utente è autorizzato a connettersi a una risorsa specificata tramite Desktop remoto Gateway (Gateway Desktop remoto).

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

La classe **Win32 \_ TSGatewayResourceAuthorizationPolicy** presenta questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La classe **Win32 \_ TSGatewayResourceAuthorizationPolicy** presenta questi metodi.



| Metodo                                                                                          | Descrizione                                                                                                         |
|:------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------|
| [**AddUserGroupNames**](addusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md)       | Aggiunge i nomi dei gruppi di utenti specificati ai gruppi di utenti esistenti nella proprietà **UserGroupNames** .<br/>      |
| [**Creare**](create-win32-tsgatewayresourceauthorizationpolicy.md)                             | Creazione di un criterio di autorizzazione connessioni Desktop remoto.<br/>                                                                                       |
| [**Delete**](delete-win32-tsgatewayresourceauthorizationpolicy.md)                             | Elimina il RAP RD corrente.<br/>                                                                              |
| [**RemoveUserGroupNames**](removeusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md) | Rimuove i nomi dei gruppi di utenti specificati dai gruppi di utenti esistenti nella proprietà **UserGroupNames** .<br/> |
| [**SetDescription**](setdescription-win32-tsgatewayresourceauthorizationpolicy.md)             | Imposta la proprietà **Description** per il criterio di autorizzazione connessioni Desktop remoto.<br/>                                                        |
| [**SetEnabled**](setenabled-win32-tsgatewayresourceauthorizationpolicy.md)                     | Abilita o Disabilita il criterio di autorizzazione connessioni Desktop remoto impostando la proprietà **Enabled** .<br/>                                      |
| [**SetName**](setname-win32-tsgatewayresourceauthorizationpolicy.md)                           | Imposta la proprietà **Name** per il criterio di autorizzazione connessioni Desktop remoto.<br/>                                                               |
| [**SetPortNumbers**](setportnumbers-win32-tsgatewayresourceauthorizationpolicy.md)             | Imposta la proprietà **PortNumbers** per il criterio di autorizzazione connessioni Desktop remoto.<br/>                                                        |
| [**SetResourceGroup**](setresourcegroup-win32-tsgatewayresourceauthorizationpolicy.md)         | Imposta le proprietà **ResourceGroupType** e **ResourceGroupName** .<br/>                                     |
| [**SetUserGroupNames**](setusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md)       | Imposta la proprietà **UserGroupNames** per il criterio di autorizzazione connessioni Desktop remoto.<br/>                                                     |
| [**Aggiornamento**](update-win32-tsgatewayresourceauthorizationpolicy.md)                             | Aggiorna il RAP RD corrente.<br/>                                                                              |



 

### <a name="properties"></a>Proprietà

La classe **Win32 \_ TSGatewayResourceAuthorizationPolicy** dispone di queste proprietà.

<dl> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione del criterio di autorizzazione connessioni Desktop remoto. Questa proprietà viene modificata con il metodo [**sedescription**](setdescription-win32-tsgatewayresourceauthorizationpolicy.md) .

</dd> <dt>

**Enabled**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se l'autorizzazione RD è abilitata. Questa proprietà viene modificata con il metodo [**Seenabled**](setenabled-win32-tsgatewayresourceauthorizationpolicy.md) .

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nome dei criteri di autorizzazione connessioni Desktop remoto. Questa proprietà viene modificata con il metodo [**Sename**](setname-win32-tsgatewayresourceauthorizationpolicy.md) .

</dd> <dt>

**PortNumbers**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Elenco di numeri di porta separati da punti e virgola consentiti per questo criterio. Per consentire qualsiasi numero di porta, impostare " \* ".

</dd> <dt>

**ProtocolNames**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Elenco di nomi di protocollo delimitati da punti e virgola abilitati per questo criterio. I nomi devono corrispondere alla restituzione del metodo [**Getprotocolname**](getprotocolname-win32-tsgatewayserversettings.md) della [**classe \_ Win32 TSGatewayServerSettings**](win32-tsgatewayserversettings.md) .

</dd> <dt>

**ResourceGroupName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome del gruppo di risorse. Questa proprietà viene modificata con il metodo [**SetResourceGroup**](setresourcegroup-win32-tsgatewayresourceauthorizationpolicy.md) .

</dd> <dt>

**ResourceGroupType**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Identifica il tipo del gruppo di risorse. Questa proprietà viene modificata con il metodo [**SetResourceGroup**](setresourcegroup-win32-tsgatewayresourceauthorizationpolicy.md) .

<dt>

RG
</dt> <dd>

Gruppo di risorse.

</dd> <dt>

CG
</dt> <dd>

Gruppo di computer, come Archiviato in Active Directory Domain Services.

</dd> <dt>

TUTTI
</dt> <dd>

Tutte le risorse.

</dd> </dl>

</dd> <dt>

**UserGroupNames**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Elenco delimitato da punti e virgola di nomi di gruppi di utenti. Se l'utente appartiene a uno di questi gruppi di utenti, sarà consentito l'accesso. Questa proprietà viene modificata con i metodi [**SetUserGroupNames**](setusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md), [**AddUserGroupNames**](addusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md)e [**RemoveUserGroupNames**](removeusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md) .

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

[**\_TSGatewayRADIUSServer Win32**](win32-tsgatewayradiusserver.md)
</dt> <dt>

[**\_TSGatewayResourceGroup Win32**](win32-tsgatewayresourcegroup.md)
</dt> <dt>

[**\_TSGatewayServerSettings Win32**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

