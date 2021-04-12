---
title: Metodo SetAuthorizationPlugin della classe Win32_TSGatewayServerSettings
description: Imposta il plug-in di autorizzazione corrente per il server Gateway Desktop remoto (Gateway Desktop remoto).
ms.assetid: 236c9cca-4efc-433a-8f1f-e3044e0588b3
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetAuthorizationPlugin
- Metodo SetAuthorizationPlugin Servizi Desktop remoto, classe Win32_TSGatewayServerSettings
- Classe Win32_TSGatewayServerSettings Servizi Desktop remoto, metodo SetAuthorizationPlugin
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetAuthorizationPlugin
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cdb3cb07a7c0a30e84245a2d22e383dea168247
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518172"
---
# <a name="setauthorizationplugin-method-of-the-win32_tsgatewayserversettings-class"></a>Metodo SetAuthorizationPlugin della \_ classe TSGatewayServerSettings Win32

Imposta il plug-in di autorizzazione corrente per il server Gateway Desktop remoto (Gateway Desktop remoto).

## <a name="syntax"></a>Sintassi


```mof
uint32 SetAuthorizationPlugin(
  [in] string PluginName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Plug-in* \[ in\]
</dt> <dd>

Tipo: **stringa**

Nome del nuovo plug-in di autorizzazione corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **UInt32**

Se il metodo ha esito positivo, restituisce zero. Se il metodo ha esito negativo, restituisce un valore diverso da zero. Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Commenti

È necessario chiamare il metodo [**RecycleRpcApplicationPools**](recyclerpcapplicationpools-win32-tsgatewayserversettings.md) per consentire il funzionamento del plug-in di autorizzazione.

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

[**\_TSGatewayServerSettings Win32**](win32-tsgatewayserversettings.md)
</dt> <dt>

[**RecycleRpcApplicationPools**](recyclerpcapplicationpools-win32-tsgatewayserversettings.md)
</dt> </dl>

 

