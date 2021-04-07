---
title: Metodo SetDeviceRedirectionType della classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Imposta la proprietà DeviceRedirectionType, che consente di controllare i dispositivi da reindirizzare.
ms.assetid: d97a0a7d-a08e-4703-b0f0-ba5d20688dc8
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetDeviceRedirectionType
- Metodo SetDeviceRedirectionType Servizi Desktop remoto, classe Win32_TSGatewayConnectionAuthorizationPolicy
- Classe Win32_TSGatewayConnectionAuthorizationPolicy Servizi Desktop remoto, metodo SetDeviceRedirectionType
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
ms.openlocfilehash: 98b369e0b6031aa503e2f7f55860d004f63b7f93
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964137"
---
# <a name="setdeviceredirectiontype-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>Metodo SetDeviceRedirectionType della \_ classe TSGatewayConnectionAuthorizationPolicy Win32

Imposta la proprietà **DeviceRedirectionType** , che consente di controllare i dispositivi da reindirizzare.

## <a name="syntax"></a>Sintassi


```mof
uint32 SetDeviceRedirectionType(
  [in] uint32 DeviceRedirectionType
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*DeviceRedirectionType* \[ in\]
</dt> <dd>

Tipo di reindirizzamento del dispositivo.

<dt>

0
</dt> <dd>

Verranno reindirizzati tutti i dispositivi.

</dd> <dt>

1
</dt> <dd>

Non verrà reindirizzato alcun dispositivo.

</dd> <dt>

2
</dt> <dd>

I dispositivi specificati non verranno reindirizzati. Le proprietà **DiskDrivesDisabled**, **PrintersDisabled**, **SerialPortsDisabled**, **ClipboardDisabled** e **PlugAndPlayDevicesDisabled** controllano i dispositivi che non verranno reindirizzati.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce zero. Se il metodo ha esito negativo, restituisce un valore diverso da zero. Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Commenti

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

 

