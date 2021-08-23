---
title: Metodo RefreshCertContext della Win32_TSGatewayServerSettings classe
description: Aggiorna il certificato usato dal server Desktop remoto Gateway Desktop remoto.
ms.assetid: caefeb85-1c7a-4868-9ee8-10ab09354595
ms.tgt_platform: multiple
keywords:
- Metodo RefreshCertContext Servizi Desktop remoto
- Il metodo RefreshCertContext Servizi Desktop remoto , Win32_TSGatewayServerSettings classe
- Win32_TSGatewayServerSettings classe Servizi Desktop remoto , metodo RefreshCertContext
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.RefreshCertContext
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b81d25944e77a2c80c3f7823283cf0bef813ab51600a1a0a5f3b8aaf9dfb8eab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769671"
---
# <a name="refreshcertcontext-method-of-the-win32_tsgatewayserversettings-class"></a>Metodo RefreshCertContext della classe \_ Win32 TSGatewayServerSettings

Aggiorna il certificato usato dal server Desktop remoto Gateway Desktop remoto.

## <a name="syntax"></a>Sintassi


```mof
uint32 RefreshCertContext(
  [in] uint8 CertHash[]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*CertHash* \[ Pollici\]
</dt> <dd>

Hash del certificato usato dal server Gateway Desktop remoto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce zero. Se il metodo ha esito negativo, restituisce un valore diverso da zero. Per un elenco di codici di errore, vedere Servizi Desktop remoto [di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Commenti

Per chiamare questo metodo, è necessario essere un membro del gruppo Administrators.

Managed Object Format (MOF) contengono le definizioni per le Windows WMI (Management Instrumentation). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, [vedere Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

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

[**Win32 \_ TSGatewayServerSettings**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

