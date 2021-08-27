---
title: Metodo RemoveResources della Win32_TSGatewayResourceGroup classe
description: Rimuove le risorse dal gruppo di risorse.
ms.assetid: 5f339990-8273-4658-843e-b6b7a85808e1
ms.tgt_platform: multiple
keywords:
- Metodo RemoveResources Servizi Desktop remoto
- Metodo RemoveResources Servizi Desktop remoto , Win32_TSGatewayResourceGroup classe
- Win32_TSGatewayResourceGroup classe Servizi Desktop remoto , metodo RemoveResources
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup.RemoveResources
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e852f2994c3302e4e53f316496b023c9e8fc115508ff522f384aa4701d2050ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118127516"
---
# <a name="removeresources-method-of-the-win32_tsgatewayresourcegroup-class"></a>Metodo RemoveResources della classe \_ TSGatewayResourceGroup Win32

Rimuove le risorse dal gruppo di risorse.

## <a name="syntax"></a>Sintassi


```mof
uint32 RemoveResources(
  [in] string Resources
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Risorse* \[ Pollici\]
</dt> <dd>

Elenco delimitato da punto e virgola delle risorse da rimuovere.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce zero. Se il metodo ha esito negativo, restituisce un valore diverso da zero. Per un elenco dei codici di errore, vedere Servizi Desktop remoto [di errore del provider WMI.](terminal-services-wmi-provider-error-codes.md)

## <a name="remarks"></a>Commenti

Se nel parametro *Resources sono* presenti più risorse e una delle risorse non può essere elaborata, nessuna delle risorse verrà elaborata.

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

[**Win32 \_ TSGatewayResourceGroup**](win32-tsgatewayresourcegroup.md)
</dt> </dl>

 

