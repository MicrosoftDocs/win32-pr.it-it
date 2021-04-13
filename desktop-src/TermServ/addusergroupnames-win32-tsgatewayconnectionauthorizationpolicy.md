---
title: Metodo AddUserGroupNames della classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Aggiunge i nomi dei gruppi di utenti specificati alla proprietà UserGroupNames.
ms.assetid: 01bbccc3-c2e4-46ad-8649-1a30e001c949
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo AddUserGroupNames
- Metodo AddUserGroupNames Servizi Desktop remoto, classe Win32_TSGatewayConnectionAuthorizationPolicy
- Classe Win32_TSGatewayConnectionAuthorizationPolicy Servizi Desktop remoto, metodo AddUserGroupNames
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.AddUserGroupNames
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93a4fe26b27f954e5ea9a0c7ac666592f74337a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400403"
---
# <a name="addusergroupnames-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>Metodo AddUserGroupNames della \_ classe TSGatewayConnectionAuthorizationPolicy Win32

Aggiunge i nomi dei gruppi di utenti specificati alla proprietà **UserGroupNames** .

## <a name="syntax"></a>Sintassi


```mof
uint32 AddUserGroupNames(
  [in] string UserGroupNames
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*UserGroupNames* \[ in\]
</dt> <dd>

Elenco delimitato da punti e virgola di nomi di gruppi di utenti da aggiungere alla proprietà **UserGroupNames** . I nomi dei gruppi di utenti devono essere nel formato *dominio \\ nomegruppoutenti*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce zero. Se il metodo ha esito negativo, restituisce un valore diverso da zero. Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Commenti

Se nel parametro *UserGroupNames* sono presenti più nomi di gruppi di utenti e uno dei nomi non può essere elaborato, nessuno dei nomi verrà elaborato.

Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.

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
</dt> </dl>

 

