---
title: Metodo SetIdleTimeout della classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Imposta la proprietà IdleTimeout.
ms.assetid: 162224dd-e4d4-483f-9ec4-b87731bc5014
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetIdleTimeout
- Metodo SetIdleTimeout Servizi Desktop remoto, classe Win32_TSGatewayConnectionAuthorizationPolicy
- Classe Win32_TSGatewayConnectionAuthorizationPolicy Servizi Desktop remoto, metodo SetIdleTimeout
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
ms.openlocfilehash: 2c166311477dc9de94ca6c9614e14ac98907b406
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302571"
---
# <a name="setidletimeout-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>Metodo SetIdleTimeout della \_ classe TSGatewayConnectionAuthorizationPolicy Win32

Imposta la proprietà **IdleTimeout** .

## <a name="syntax"></a>Sintassi


```mof
uint32 SetIdleTimeout(
  [in] uint32 IdleTimeout
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*IdleTimeout* \[ in\]
</dt> <dd>

Tipo: **UInt32**

Nuovo valore di timeout, in minuti. Il valore 0 indica che non esiste alcun timeout.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **UInt32**

Se il metodo ha esito positivo, restituisce zero. Se il metodo ha esito negativo, restituisce un valore diverso da zero. Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Commenti

Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.

I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008 R2<br/>                                                        |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_TSGatewayConnectionAuthorizationPolicy Win32**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

