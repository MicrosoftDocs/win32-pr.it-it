---
title: Metodo DisablePlugAndPlayDevices della classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Imposta la proprietà PlugAndPlayDevicesDisabled.
ms.assetid: 0cfe9fea-da93-47fa-a9ea-868c78890a53
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo DisablePlugAndPlayDevices
- Metodo DisablePlugAndPlayDevices Servizi Desktop remoto, classe Win32_TSGatewayConnectionAuthorizationPolicy
- Classe Win32_TSGatewayConnectionAuthorizationPolicy Servizi Desktop remoto, metodo DisablePlugAndPlayDevices
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
ms.openlocfilehash: fc7432d69fc8cd088af5d5a44a07b90f9d697348
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400325"
---
# <a name="disableplugandplaydevices-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>Metodo DisablePlugAndPlayDevices della \_ classe TSGatewayConnectionAuthorizationPolicy Win32

Imposta la proprietà **PlugAndPlayDevicesDisabled** . Se il valore della proprietà **DeviceRedirectionType** è "2", la proprietà **PlugAndPlayDevicesDisabled** controlla il reindirizzamento dei dispositivi Plug and Play per le sessioni stabilite tramite il server gateway di desktop remoto (Gateway Desktop remoto).

## <a name="syntax"></a>Sintassi


```mof
uint32 DisablePlugAndPlayDevices(
  [in] boolean Disabled
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Disabilitato* \[ in\]
</dt> <dd>

Nuovo valore per la proprietà **PlugAndPlayDevicesDisabled** .

</dd> </dl>

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

 

