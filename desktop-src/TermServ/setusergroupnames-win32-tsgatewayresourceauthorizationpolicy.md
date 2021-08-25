---
title: Metodo SetUserGroupNames della classe Win32_TSGatewayResourceAuthorizationPolicy
description: Imposta la proprietà UserGroupNames per i criteri Desktop remoto di autorizzazione delle risorse (RD \ 160; RAP).
ms.assetid: 91b77cd6-779e-460a-88a3-eda7a6fe99e5
ms.tgt_platform: multiple
keywords:
- Metodo SetUserGroupNames Servizi Desktop remoto
- Metodo SetUserGroupNames Servizi Desktop remoto , Win32_TSGatewayResourceAuthorizationPolicy classe
- Win32_TSGatewayResourceAuthorizationPolicy classe Servizi Desktop remoto metodo SetUserGroupNames
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.SetUserGroupNames
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18d4a54f042ebf99ff5a3b1bf16081ce0719578ef7fc2fd272e9ccc07a832822
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008571"
---
# <a name="setusergroupnames-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a>Metodo SetUserGroupNames della classe \_ Win32 TSGatewayResourceAuthorizationPolicy

Imposta la **proprietà UserGroupNames** per i criteri Desktop remoto di autorizzazione risorse desktop remoto.

## <a name="syntax"></a>Sintassi


```mof
uint32 SetUserGroupNames(
  [in] string UserGroupNames
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*UserGroupNames* \[ Pollici\]
</dt> <dd>

Elenco di nomi di gruppi di utenti separati da punti e virgola. I nomi sono nel formato *Dominio \\ UserGroupName*. Se l'utente appartiene a uno di questi gruppi di utenti, l'accesso sarà consentito.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce zero. Se il metodo ha esito negativo, restituisce un valore diverso da zero. Per un elenco di codici di errore, vedere Servizi Desktop remoto [di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Commenti

Se nel parametro *UserGroupNames* sono presenti più nomi di gruppi di utenti e uno dei nomi non può essere elaborato, non verrà elaborato nessuno dei nomi.

Per chiamare questo metodo, è necessario essere un membro del gruppo Administrators.

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

 

