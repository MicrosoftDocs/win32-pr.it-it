---
title: Win32_TSGatewayResourceGroup classe
description: Descrive un gruppo di risorse, che esegue il mapping di un set di risorse (nomi di computer) a una singola entità.
ms.assetid: 5715a2ea-9bbc-4704-835e-ba6d93a72368
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayResourceGroup classe Servizi Desktop remoto
- Win32_TSGatewayResourceGroup classe Servizi Desktop remoto , descritto
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup
- Win32_TSGatewayResourceGroup.Name
- Win32_TSGatewayResourceGroup.Description
- Win32_TSGatewayResourceGroup.AssociatedRAPs
- Win32_TSGatewayResourceGroup.Resources
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81ba4ec4545502d82a3449cee39954deb9b5b2e68bf7c657423e673c582d1c18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118603886"
---
# <a name="win32_tsgatewayresourcegroup-class"></a>Classe \_ TSGatewayResourceGroup Win32

Descrive un gruppo di risorse, che esegue il mapping di un set di risorse (nomi di computer) a una singola entità.

## <a name="syntax"></a>Sintassi

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayResourceGroup
{
  string Name;
  string Description;
  string AssociatedRAPs;
  string Resources;
};
```

## <a name="members"></a>Members

La **classe \_ TSGatewayResourceGroup Win32** include questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe \_ Win32 TSGatewayResourceGroup** include questi metodi.



| Metodo                                                                  | Descrizione                                                                           |
|:------------------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [**Risorse AddResources**](addresources-win32-tsgatewayresourcegroup.md)       | Aggiunge risorse alla proprietà **Risorse** per questo gruppo di risorse.<br/>      |
| [**Crea**](create-win32-tsgatewayresourcegroup.md)                   | Crea un gruppo di risorse.<br/>                                                  |
| [**Delete**](delete-win32-tsgatewayresourcegroup.md)                   | Elimina questo gruppo di risorse.<br/>                                               |
| [**RemoveResources**](removeresources-win32-tsgatewayresourcegroup.md) | Elimina le risorse dalla **proprietà Risorse** per questo gruppo di risorse.<br/> |
| [**SetDescription**](setdescription-win32-tsgatewayresourcegroup.md)   | Imposta la **proprietà Description** per questo gruppo di risorse.<br/>                 |
| [**SetName**](setname-win32-tsgatewayresourcegroup.md)                 | Imposta la **proprietà Name** per questo gruppo di risorse.<br/>                        |
| [**SetResources**](setresources-win32-tsgatewayresourcegroup.md)       | Imposta la **proprietà Resources** per questo gruppo di risorse.<br/>                   |
| [**Aggiornamento**](update-win32-tsgatewayresourcegroup.md)                   | Aggiorna questo gruppo di risorse.<br/>                                               |



 

### <a name="properties"></a>Proprietà

La **classe \_ Win32 TSGatewayResourceGroup** ha queste proprietà.

<dl> <dt>

**AssociatedRAPs**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Elenco delimitato da punto e virgola Servizi Desktop remoto criteri di autorizzazione delle risorse desktop remoto associati a questo gruppo di risorse.

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione del gruppo di risorse. Questa proprietà può essere modificata con il [**metodo SetDescription.**](setdescription-win32-tsgatewayresourcegroup.md)

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nome del gruppo di risorse. Questa proprietà può essere modificata con il [**metodo SetName.**](setname-win32-tsgatewayresourcegroup.md)

</dd> <dt>

**Risorse**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Elenco di risorse separate da punto e virgola in questo gruppo di risorse. " \* " indica tutte le risorse. Questa proprietà può essere modificata con [**i metodi SetResources,**](setresources-win32-tsgatewayresourcegroup.md) [**AddResources,**](addresources-win32-tsgatewayresourcegroup.md) [**RemoveResources**](removeresources-win32-tsgatewayresourcegroup.md)e [**Update.**](update-win32-tsgatewayresourcegroup.md)

</dd> </dl>

## <a name="remarks"></a>Commenti

Per utilizzare questa classe, è necessario essere un membro del gruppo Administrators.

Managed Object Format (MOF) contengono le definizioni per Windows di Strumentazione gestione Windows (WMI). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, vedere [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

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

[**Win32 \_ TSGatewayResourceAuthorizationPolicy**](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[**Win32 \_ TSGatewayServerSettings**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

