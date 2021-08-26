---
title: Metodo SetResources della classe Win32_TSGatewayResourceGroup
description: Imposta la proprietà Resources per questo gruppo di risorse.
ms.assetid: 0043ee04-26d1-4907-87cc-a15f72cb0b93
ms.tgt_platform: multiple
keywords:
- Metodo SetResources Servizi Desktop remoto
- Metodo SetResources Servizi Desktop remoto , Win32_TSGatewayResourceGroup classe
- Win32_TSGatewayResourceGroup classe Servizi Desktop remoto metodo SetResources
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup.SetResources
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77f357b08e554c5fa97cc26d15c52e65a0668512eeef20bceeba8d194510bdf0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119987671"
---
# <a name="setresources-method-of-the-win32_tsgatewayresourcegroup-class"></a>Metodo SetResources della classe \_ TSGatewayResourceGroup Win32

Imposta la **proprietà Resources** per questo gruppo di risorse.

## <a name="syntax"></a>Sintassi


```mof
uint32 SetResources(
  [in] string Resources
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Risorse* \[ Pollici\]
</dt> <dd>

Elenco di risorse separate da punti e virgola in questo gruppo di risorse. " \* " indica tutte le risorse.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce zero. Se il metodo ha esito negativo, restituisce un valore diverso da zero. Per un elenco di codici di errore, vedere Servizi Desktop remoto [di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Commenti

Se nel parametro *Resources* sono presenti più risorse e una delle risorse non può essere elaborata, nessuna delle risorse verrà elaborata.

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

[**Win32 \_ TSGatewayResourceGroup**](win32-tsgatewayresourcegroup.md)
</dt> </dl>

 

