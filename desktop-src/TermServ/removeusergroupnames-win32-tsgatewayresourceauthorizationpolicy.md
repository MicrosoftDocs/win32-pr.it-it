---
title: Metodo RemoveUserGroupNames della classe Win32_TSGatewayResourceAuthorizationPolicy
description: Rimuove i nomi dei gruppi di utenti specificati dai gruppi di utenti esistenti nella proprietà UserGroupNames.
ms.assetid: 8538e41a-b9ae-43ce-b19a-40a40f9a12f5
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo RemoveUserGroupNames
- Metodo RemoveUserGroupNames Servizi Desktop remoto, classe Win32_TSGatewayResourceAuthorizationPolicy
- Classe Win32_TSGatewayResourceAuthorizationPolicy Servizi Desktop remoto, metodo RemoveUserGroupNames
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.RemoveUserGroupNames
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e6746eaa9d6a7c3cfd82512a4b9f632c873bc9f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301616"
---
# <a name="removeusergroupnames-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a>Metodo RemoveUserGroupNames della \_ classe TSGatewayResourceAuthorizationPolicy Win32

Rimuove i nomi dei gruppi di utenti specificati dai gruppi di utenti esistenti nella proprietà **UserGroupNames** .

## <a name="syntax"></a>Sintassi


```mof
uint32 RemoveUserGroupNames(
  [in] string UserGroupNames
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*UserGroupNames* \[ in\]
</dt> <dd>

Elenco delimitato da punti e virgola di nomi di gruppi di utenti.

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

[**\_TSGatewayResourceAuthorizationPolicy Win32**](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

