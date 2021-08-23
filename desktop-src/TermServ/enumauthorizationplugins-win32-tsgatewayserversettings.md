---
title: Metodo EnumAuthorizationPlugins della Win32_TSGatewayServerSettings classe
description: Enumera tutti i plug-in di autorizzazione registrati.
ms.assetid: 525b4001-b89c-43cc-986a-00db47dd5518
ms.tgt_platform: multiple
keywords:
- Metodo EnumAuthorizationPlugins Servizi Desktop remoto
- Metodo EnumAuthorizationPlugins Servizi Desktop remoto , Win32_TSGatewayServerSettings classe
- Win32_TSGatewayServerSettings classe Servizi Desktop remoto metodo , EnumAuthorizationPlugins
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.EnumAuthorizationPlugins
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40447b6befd3042c766b4bd312619563617119b114c329867bfc3ca0b3e7bfce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119574631"
---
# <a name="enumauthorizationplugins-method-of-the-win32_tsgatewayserversettings-class"></a>Metodo EnumAuthorizationPlugins della classe \_ Win32 TSGatewayServerSettings

Enumera tutti i plug-in di autorizzazione registrati.

## <a name="syntax"></a>Sintassi


```mof
uint32 EnumAuthorizationPlugins(
  [out] string PluginNames[],
  [out] string CLSIDs[],
  [out] string Descriptions[]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PluginNames* \[ Cambio\]
</dt> <dd>

Tipo: **\[ \] stringa**

Matrice **di** stringhe che riceve i nomi dei plug-in di autorizzazione registrati.

</dd> <dt>

*CLSID* \[ Cambio\]
</dt> <dd>

Tipo: **\[ \] stringa**

Matrice **di** stringhe che riceve i CLSID dei plug-in di autorizzazione registrati.

</dd> <dt>

*Descrizioni* \[ Cambio\]
</dt> <dd>

Tipo: **\[ \] stringa**

Matrice **di** stringhe che riceve le descrizioni dei plug-in di autorizzazione registrati.

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

[**Win32 \_ TSGatewayServerSettings**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

