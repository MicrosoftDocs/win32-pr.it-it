---
title: Classe Win32_TSGatewayLoadBalancer
description: Viene descritto un set di server di bilanciamento del carico di Desktop remoto Gateway Desktop remoto. Questi vengono usati per il bilanciamento del carico delle connessioni Gateway Desktop remoto su più server.
ms.assetid: aa7e7b77-7233-4c6a-8f41-cc332fa509d5
ms.tgt_platform: multiple
keywords:
- Classe Win32_TSGatewayLoadBalancer Servizi Desktop remoto
- Classe Win32_TSGatewayLoadBalancer Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_TSGatewayLoadBalancer
- Win32_TSGatewayLoadBalancer.Servers
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4956ed4dc9536ff6f7e3263071a2a477cb0f515
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741250"
---
# <a name="win32_tsgatewayloadbalancer-class"></a>Win32 \_ TSGatewayLoadBalancer (classe)

Viene descritto un set di server di bilanciamento del carico di Desktop remoto Gateway Desktop remoto. Questi vengono usati per il bilanciamento del carico delle connessioni Gateway Desktop remoto su più server.

## <a name="syntax"></a>Sintassi

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayLoadBalancer
{
  string Servers;
};
```

## <a name="members"></a>Members

La classe **Win32 \_ TSGatewayLoadBalancer** presenta questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La classe **Win32 \_ TSGatewayLoadBalancer** presenta questi metodi.



| Metodo                                                                             | Descrizione                                                                                                      |
|:-----------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------|
| [**AddServers**](addservers-win32-tsgatewayloadbalancer.md)                       | Aggiunge server alla proprietà **Servers** .<br/>                                                             |
| [**DeleteAllServers**](deleteallservers-win32-tsgatewayloadbalancer.md)           | Elimina tutti i server di bilanciamento del carico Gateway Desktop remoto che partecipano alla farm di bilanciamento del carico.<br/>               |
| [**DeleteServers**](deleteservers-win32-tsgatewayloadbalancer.md)                 | Elimina i server dalla proprietà **Servers** .<br/>                                                        |
| [**IsLoadBalancingServer**](win32-tsgatewayloadbalancer-isloadbalancingserver.md) | Determina se il server è in grado di eseguire il bilanciamento del carico.<br/>                                             |
| [**Server**](setservers-win32-tsgatewayloadbalancer.md)                       | Imposta la proprietà **Servers** con l'elenco delimitato da punti e virgola dei server di bilanciamento del carico di Gateway Desktop remoto.<br/> |



 

### <a name="properties"></a>Proprietà

La classe **Win32 \_ TSGatewayLoadBalancer** dispone di queste proprietà.

<dl> <dt>

**Server**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Elenco delimitato da punti e virgola di server di bilanciamento del carico di Gateway Desktop remoto. Questa proprietà può essere modificata con i metodi [**Seservers**](setservers-win32-tsgatewayloadbalancer.md), [**AddServers**](addservers-win32-tsgatewayloadbalancer.md), [**DeleteServers**](deleteservers-win32-tsgatewayloadbalancer.md)e [**DeleteAllServers**](deleteallservers-win32-tsgatewayloadbalancer.md) .

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

[**\_TSGatewayRADIUSServer Win32**](win32-tsgatewayradiusserver.md)
</dt> <dt>

[**\_TSGatewayResourceAuthorizationPolicy Win32**](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[**\_TSGatewayResourceGroup Win32**](win32-tsgatewayresourcegroup.md)
</dt> <dt>

[**\_TSGatewayServerSettings Win32**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

