---
title: Metodo SetIdleTimeout della classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Imposta la proprietà IdleTimeout.
ms.assetid: 162224dd-e4d4-483f-9ec4-b87731bc5014
ms.tgt_platform: multiple
keywords:
- Metodo SetIdleTimeout Servizi Desktop remoto
- Metodo SetIdleTimeout Servizi Desktop remoto , Win32_TSGatewayConnectionAuthorizationPolicy classe
- Win32_TSGatewayConnectionAuthorizationPolicy classe Servizi Desktop remoto metodo SetIdleTimeout
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetIdleTimeout
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 483369505f08e6bb28d2933296ea7da50a4706d9762e2e105dbf34526f734af4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119988021"
---
# <a name="setidletimeout-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>Metodo SetIdleTimeout della classe \_ Win32 TSGatewayConnectionAuthorizationPolicy

Imposta la **proprietà IdleTimeout.**

## <a name="syntax"></a>Sintassi


```mof
uint32 SetIdleTimeout(
  [in] uint32 IdleTimeout
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*IdleTimeout* \[ Pollici\]
</dt> <dd>

Tipo: **uint32**

Nuovo valore di timeout, in minuti. Il valore 0 indica che non è presente alcun timeout.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

Se il metodo ha esito positivo, restituisce zero. Se il metodo ha esito negativo, restituisce un valore diverso da zero. Per un elenco di codici di errore, vedere Servizi Desktop remoto [di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Commenti

Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.

Managed Object Format (MOF) contengono le definizioni per le classi WMI (Windows Management Instrumentation). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008 R2<br/>                                                        |
| Spazio dei nomi<br/>                | TerminalServices \\ CIMv2 \\ radice<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ TSGatewayConnectionAuthorizationPolicy**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

