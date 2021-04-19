---
title: Classe Win32_TSGatewayResourceGroup
description: Descrive un gruppo di risorse, che esegue il mapping di un set di risorse (nomi computer) a una singola entità.
ms.assetid: 5715a2ea-9bbc-4704-835e-ba6d93a72368
ms.tgt_platform: multiple
keywords:
- Classe Win32_TSGatewayResourceGroup Servizi Desktop remoto
- Classe Win32_TSGatewayResourceGroup Servizi Desktop remoto, descritta
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
ms.openlocfilehash: 9ffeda42abafd24526360f5e549f004cae0c3140
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301503"
---
# <a name="win32_tsgatewayresourcegroup-class"></a>Win32 \_ TSGatewayResourceGroup (classe)

Descrive un gruppo di risorse, che esegue il mapping di un set di risorse (nomi computer) a una singola entità.

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

La classe **Win32 \_ TSGatewayResourceGroup** presenta questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La classe **Win32 \_ TSGatewayResourceGroup** presenta questi metodi.



| Metodo                                                                  | Descrizione                                                                           |
|:------------------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [**AddResources**](addresources-win32-tsgatewayresourcegroup.md)       | Aggiunge risorse alla proprietà **Resources** per questo gruppo di risorse.<br/>      |
| [**Creare**](create-win32-tsgatewayresourcegroup.md)                   | Crea un gruppo di risorse.<br/>                                                  |
| [**Delete**](delete-win32-tsgatewayresourcegroup.md)                   | Elimina questo gruppo di risorse.<br/>                                               |
| [**RemoveResources**](removeresources-win32-tsgatewayresourcegroup.md) | Elimina le risorse dalla proprietà **Resources** per questo gruppo di risorse.<br/> |
| [**SetDescription**](setdescription-win32-tsgatewayresourcegroup.md)   | Imposta la proprietà **Description** per questo gruppo di risorse.<br/>                 |
| [**SetName**](setname-win32-tsgatewayresourcegroup.md)                 | Imposta la proprietà del **nome** per questo gruppo di risorse.<br/>                        |
| [**SetResources**](setresources-win32-tsgatewayresourcegroup.md)       | Imposta la proprietà **Resources** per questo gruppo di risorse.<br/>                   |
| [**Aggiornamento**](update-win32-tsgatewayresourcegroup.md)                   | Aggiorna questo gruppo di risorse.<br/>                                               |



 

### <a name="properties"></a>Proprietà

La classe **Win32 \_ TSGatewayResourceGroup** dispone di queste proprietà.

<dl> <dt>

**AssociatedRAPs**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Elenco delimitato da punti e virgola dei criteri di autorizzazione delle risorse Servizi Desktop remoto associati a questo gruppo di risorse.

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione del gruppo di risorse. Questa proprietà può essere modificata con il metodo [**sedescription**](setdescription-win32-tsgatewayresourcegroup.md) .

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nome del gruppo di risorse. Questa proprietà può essere modificata con il metodo [**Sename**](setname-win32-tsgatewayresourcegroup.md) .

</dd> <dt>

**Risorse**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Elenco di risorse separate da punto e virgola in questo gruppo di risorse. " \* " Indica tutte le risorse. Questa proprietà può essere modificata con i metodi [**Seresources**](setresources-win32-tsgatewayresourcegroup.md), [**AddResources**](addresources-win32-tsgatewayresourcegroup.md), [**RemoveResources**](removeresources-win32-tsgatewayresourcegroup.md)e [**Update**](update-win32-tsgatewayresourcegroup.md) .

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

[**\_TSGatewayResourceAuthorizationPolicy Win32**](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[**\_TSGatewayServerSettings Win32**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

