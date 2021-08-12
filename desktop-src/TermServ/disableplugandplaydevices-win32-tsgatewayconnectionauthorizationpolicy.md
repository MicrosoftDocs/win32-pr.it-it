---
title: Metodo DisablePlugAndPlayDevices della Win32_TSGatewayConnectionAuthorizationPolicy classe
description: Imposta la proprietà PlugAndPlayDevicesDisabled.
ms.assetid: 0cfe9fea-da93-47fa-a9ea-868c78890a53
ms.tgt_platform: multiple
keywords:
- Metodo DisablePlugAndPlayDevices Servizi Desktop remoto
- Il metodo DisablePlugAndPlayDevices Servizi Desktop remoto , Win32_TSGatewayConnectionAuthorizationPolicy classe
- Win32_TSGatewayConnectionAuthorizationPolicy classe Servizi Desktop remoto, metodo DisablePlugAndPlayDevices
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.DisablePlugAndPlayDevices
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84bbd9c6f44c120d5a47e74219ed071a6e405e70ab0a46b54f707671ff5b2e6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118609437"
---
# <a name="disableplugandplaydevices-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>Metodo DisablePlugAndPlayDevices della classe \_ Win32 TSGatewayConnectionAuthorizationPolicy

Imposta la **proprietà PlugAndPlayDevicesDisabled.** Se il valore della proprietà **DeviceRedirectionType** è "2", la proprietà **PlugAndPlayDevicesDisabled** controlla il reindirizzamento dei dispositivi Plug and Play per le sessioni stabilite tramite il server Gateway Desktop remoto .

## <a name="syntax"></a>Sintassi


```mof
uint32 DisablePlugAndPlayDevices(
  [in] boolean Disabled
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Disabilitato* \[ Pollici\]
</dt> <dd>

Nuovo valore per **la proprietà PlugAndPlayDevicesDisabled.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce zero. Se il metodo ha esito negativo, restituisce un valore diverso da zero. Per un elenco dei codici di errore, vedere Servizi Desktop remoto [di errore del provider WMI.](terminal-services-wmi-provider-error-codes.md)

## <a name="remarks"></a>Commenti

Per chiamare questo metodo, è necessario essere un membro del gruppo Administrators.

Managed Object Format (MOF) contengono le definizioni per Windows di Strumentazione gestione Windows (WMI). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, [vedere Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

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

[**Win32 \_ TSGatewayConnectionAuthorizationPolicy**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

