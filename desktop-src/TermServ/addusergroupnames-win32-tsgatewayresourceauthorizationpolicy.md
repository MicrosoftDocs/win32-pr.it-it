---
title: Metodo AddUserGroupNames della classe Win32_TSGatewayResourceAuthorizationPolicy
description: Aggiunge l'elenco delimitato da punto e virgola specificato di nomi di gruppi di utenti ai gruppi di utenti esistenti nella proprietà UserGroupNames.
ms.assetid: 9cd18ecd-ad56-49c7-954a-2d67bbd7b1db
ms.tgt_platform: multiple
keywords:
- Metodo AddUserGroupNames Servizi Desktop remoto
- Metodo AddUserGroupNames Servizi Desktop remoto , Win32_TSGatewayResourceAuthorizationPolicy classe
- Win32_TSGatewayResourceAuthorizationPolicy classe Servizi Desktop remoto , metodo AddUserGroupNames
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.AddUserGroupNames
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be87eb72790d5852861fe0066bc32e319f0a74ba00af3d0ea38dc0ebcbee9850
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118610175"
---
# <a name="addusergroupnames-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a>Metodo AddUserGroupNames della classe \_ TSGatewayResourceAuthorizationPolicy Win32

Aggiunge l'elenco delimitato da punto e virgola specificato di nomi di gruppi di utenti ai gruppi di utenti esistenti nella **proprietà UserGroupNames.**

## <a name="syntax"></a>Sintassi


```mof
uint32 AddUserGroupNames(
  [in] string UserGroupNames
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*UserGroupNames* \[ Pollici\]
</dt> <dd>

Elenco delimitato da punti e virgola di nomi di gruppi di utenti da aggiungere alla **proprietà UserGroupNames.** I nomi dei gruppi utenti devono essere nel formato *\\ DominioNomeGruppoUtente*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce zero. Se il metodo ha esito negativo, restituisce un valore diverso da zero. Per un elenco di codici di errore, vedere Servizi Desktop remoto [di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Commenti

Se nel parametro *UserGroupNames* sono presenti più nomi di gruppi di utenti e uno dei nomi non può essere elaborato, non verrà elaborato nessuno dei nomi.

Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.

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

[**Win32 \_ TSGatewayResourceAuthorizationPolicy**](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

