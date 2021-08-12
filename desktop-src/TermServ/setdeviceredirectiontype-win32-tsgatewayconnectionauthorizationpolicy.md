---
title: Metodo SetDeviceRedirectionType della classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Imposta la proprietà DeviceRedirectionType, che controlla i dispositivi che verranno reindirizzati.
ms.assetid: d97a0a7d-a08e-4703-b0f0-ba5d20688dc8
ms.tgt_platform: multiple
keywords:
- Metodo SetDeviceRedirectionType Servizi Desktop remoto
- Metodo SetDeviceRedirectionType Servizi Desktop remoto , Win32_TSGatewayConnectionAuthorizationPolicy classe
- Win32_TSGatewayConnectionAuthorizationPolicy classe Servizi Desktop remoto, metodo SetDeviceRedirectionType
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetDeviceRedirectionType
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdd3ccbe06acbc75e8c7c29632d7fd83dc0af222eb004c6b83976e3f6478f705
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118604660"
---
# <a name="setdeviceredirectiontype-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>Metodo SetDeviceRedirectionType della classe \_ Win32 TSGatewayConnectionAuthorizationPolicy

Imposta la **proprietà DeviceRedirectionType,** che controlla i dispositivi che verranno reindirizzati.

## <a name="syntax"></a>Sintassi


```mof
uint32 SetDeviceRedirectionType(
  [in] uint32 DeviceRedirectionType
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*DeviceRedirectionType* \[ Pollici\]
</dt> <dd>

Tipo di reindirizzamento del dispositivo.

<dt>

0
</dt> <dd>

Tutti i dispositivi verranno reindirizzati.

</dd> <dt>

1
</dt> <dd>

Nessun dispositivo verrà reindirizzato.

</dd> <dt>

2
</dt> <dd>

I dispositivi specificati non verranno reindirizzati. Le proprietà **DiskDrivesDisabled**, **PrintersDisabled**, **SerialPortsDisabled**, **ClipboardDisabled** e **PlugAndPlayDevicesDisabled** controllano quali dispositivi non verranno reindirizzati.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce zero. Se il metodo ha esito negativo, restituisce un valore diverso da zero. Per un elenco di codici di errore, vedere Servizi Desktop remoto [di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Commenti

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

[**Win32 \_ TSGatewayConnectionAuthorizationPolicy**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

